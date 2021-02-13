---
title: '[!DNL Adobe Experience Manager] 데스크탑 앱 버전 1.x 모범 사례'
description: '주요 기능 및 권장 데스크탑 앱 버전 1.x 사용 [!DNL Adobe Experience Manager] '
translation-type: tm+mt
source-git-commit: 95e252504a4fbb3b60a2c6bc9b57a8a0d8ecb51c
workflow-type: tm+mt
source-wordcount: '1677'
ht-degree: 0%

---


# AEM 데스크탑 앱 v1.x 모범 사례 {#aem-desktop-app-best-practices}

## 개요 {#overview}

[!DNL Adobe Experience Manager] 데스크탑 앱은 데스크탑에 DAM(Digital Asset Management) 솔루션을 연결하여 데스크탑에서 바로 AEM 웹 UI에서 사용할 수 있는 파일을 열 수 있습니다. 데스크톱에서 자산을 저장하면 적절한 위치의 AEM에 업로드됩니다.

AEM 데스크탑 앱을 사용하면 AEM에서 잘못된 로컬 복사본을 업데이트하거나 잘못된 에셋을 업데이트할 수 없습니다. 데스크탑 앱의 사용이 간편한 워크플로우는 데스크탑 운영 체제에서 제공하는 네트워크 공유 기술을 사용하여 활성화됩니다.

데스크탑 앱은 AEM Assets 저장소를 데스크탑에서 네트워크 공유로 마운트합니다. 따라서 폴더와 파일은 로컬인 것처럼 표시됩니다. 그러나 Finder 또는 탐색기에서 마운트된 네트워크 공유의 데스크탑에서 바로 디지털 자산 관리 작업을 수행하는 것은 권장되지 않습니다. 대신 Adobe에서는 AEM Assets 웹 UI를 사용하여 많은 수의 자산을 복사 또는 이동하는 등의 작업을 수행하는 것이 좋습니다.

>[!NOTE]
>
>이 문서를 읽기 전에 전체 [AEM 및 Creative Cloud 통합 우수 사례](https://experienceleague.adobe.com/docs/experience-manager-65/assets/administer/aem-cc-integration-best-practices.html)를 검토하여 해당 항목의 개요 수준을 높일 수 있습니다.

## AEM 데스크탑 앱 아키텍처 {#aem-desktop-app-architecture}

AEM 데스크탑 앱은 WebDAV(Windows) 또는 SMB(Mac) 네트워크 공유를 사용하여 네트워크 공유를 마운트합니다. 마운트된 네트워크 공유는 로컬 전용입니다. AEM 데스크탑 앱은 통화(열기, 읽기, 쓰기)를 가로채고 추가 로컬 캐시를 제공합니다. 또한 AEM Assets 서버에 대한 원격 호출을 최적화된 AEM HTTP 요청으로 변환합니다. 다음 다이어그램은 AEM 데스크탑 앱 아키텍처를 보여 줍니다.

![AEM 데스크탑 앱 아키텍처](assets/arch_v1.png)

*그림:데스크탑 앱 아키텍처*

파일을 저장할 때 쓰기 시 추가 캐싱을 수행하면 먼저 파일이 로컬에 저장되므로 사용자가 네트워크 전송을 기다릴 필요가 없습니다. 그런 다음 사전 정의된 지연 시간(30초)이 지나면 파일이 백그라운드에서 AEM에 업로드된 후 자산이 AEM에 업로드됩니다. AEM 데스크탑 앱은 백그라운드 파일 업로드 상태를 모니터링하기 위한 UI를 제공합니다.

## AEM 데스크톱 앱 {#recommended-use-of-aem-desktop-app} 권장 사용

AEM 데스크탑 앱의 주요 기능은 다음과 같습니다.

* **데스크탑에서 AEM Assets 웹 UI에서 파일을 엽니다**. 웹 UI에서 데스크탑(Finder, 탐색기에서)에 자산을 표시하거나 데스크톱 응용 프로그램을 사용하여 자산을 열 수 있습니다.

* **체크아웃 및 체크인**. 자산을 편집하기 위해 체크 아웃할 수 있으며 AEM Assets에서 사용자에 대해 잠긴 것으로 표시됩니다. 편집 후 자산을 체크 인하여 잠금을 해제할 수 있습니다.

* **변경 내용을 파일에 저장합니다**. 네트워크 공유의 파일에 저장한 변경 내용은 AEM에 자동으로 업로드되고 새 버전이 만들어집니다.

* **연결된 에셋을 다른 문서에 배치할 수 있습니다**. Creative Cloud([!DNL Adobe Photoshop], [!DNL Adobe InDesign] 및 [!DNL Adobe Illustrator])와 같은 응용 프로그램에서는 외부 파일을 링크로 배치할 수 있습니다. 예를 들어 InDesign 문서에 이미지를 배치할 수 있습니다. 이 경우 네트워크 공유 마운트를 통해 배치하기 위해 AEM에서 자산을 검색하고 선택할 수 있습니다. 연결된 파일 가져오기는 MS Office와 같은 Adobe이 아닌 일부 앱에서도 작동합니다.

* **AEM의 참조 해상도입니다**. 가져온 파일과 링크가 있는 기본 파일이 모두 AEM에 저장되어 있으면 자산 참조에 대한 서버측 정보를 자동으로 제공할 수 있습니다.

* **데스크탑에서 에셋에 액세스합니다**. 마운트된 네트워크 공유에서 상황에 맞는 메뉴는 [!UICONTROL More Info] 대화 상자(더 큰 미리 보기, 키 메타데이터)와 AEM UI에서 자산을 여는 기능을 제공합니다.

* **대용량 계층 폴더를 일괄** 업로드합니다. AEM UI에서 만들기 > 폴더 업로드 옵션을 사용하여 자산을 업로드하는 경우 AEM 데스크톱 앱은 선택한 폴더 계층 구조를 백그라운드에서 AEM에 업로드합니다. 업로드 진행 상태는 데스크톱 앱의 전용 UI를 사용하여 모니터링할 수 있습니다.

## AEM 데스크톱 앱 {#inappropriate-use-of-aem-desktop-app}의 부적절한 사용

* 데스크탑에서 자산을 관리하기 위해 AEM 데스크탑 앱을 사용하지 마십시오. AEM 데스크탑 앱이 네트워크 드라이브를 대체하기 위해 구축되지 않았습니다. 대신 다음 기능을 사용하십시오.

   * 디지털 에셋 관리를 위한 AEM Assets 웹 UI(에셋, 메타데이터 및 복사 또는 이동 검색 또는 공유)

   * AEM 데스크탑 앱 [!UICONTROL Folder Upload]을(를) 사용하여 크고 계층적 폴더를 업로드합니다.

* AEM 데스크탑 앱을 AEM Assets용 &quot;데스크탑 동기화&quot; 클라이언트로 취급하지 마십시오. 여기서 AEM 데스크탑 앱의 주요 이점은 전체 저장소에 &quot;가상&quot; 액세스를 제공하고 데스크탑 동기화 애플리케이션은 일반적으로 한 사용자에 속한 자산만 동기화한다는 것입니다. AEM 데스크탑 앱은 일부 수준의 캐싱 및 백그라운드 업로드를 제공합니다.그러나 Adobe Creative Cloud 데스크탑 앱 또는 Microsoft OneDrive와 같은 일반적인 &quot;동기화&quot; 애플리케이션과 매우 다르게 작동합니다.

* AEM 데스크탑 앱 네트워크 드라이브를 사용하여 자산을 자주 저장하지 마십시오. 모든 저장 작업은 AEM Assets으로 전송됩니다. 따라서 마운트된 AEM Assets 저장소에서 직접 집중적인 편집 작업을 수행하는 것은 어렵습니다. 마운트된 저장소에서 바로 에셋을 편집하면 관련 없는 버전으로 에셋의 타임라인이 중단되고 서버에 추가 오버헤드가 추가됩니다.

* 한 AEM 인스턴스에서 다른 인스턴스로 대량의 데이터를 마이그레이션하는 경우에는 AEM 데스크탑 앱을 사용하지 마십시오. 자산 마이그레이션을 계획 및 실행하려면 [마이그레이션 안내서](https://experienceleague.adobe.com/docs/experience-manager-65/assets/administer/assets-migration-guide.html)를 참조하십시오. 반대로, 데스크톱 앱 [은 [!DNL Adobe Experience Manager]에서 처음으로 많은 수의 자산을 벌크 업로드를 지원합니다.](use-app-v1.md#bulkupload)

## 선택한 사용 사례용 Recommendations {#recommendations-for-selected-use-cases}

### 크리에이티브 사용자를 위한 에셋 액세스 {#access-to-assets-for-creative-users}

AEM 데스크탑 앱은 전체 DAM 저장소에 대한 가상 액세스를 제공하므로 데스크탑의 크리에이티브 사용자가 데스크탑에서 원하는 에셋을 찾아 액세스하는 것은 복잡할 수 있습니다. 이러한 모범 사례를 통해 고객을 간소화할 수 있습니다.

* AEM Assets 웹 UI의 공동 작업 기능을 사용하여 크리에이티브 사용자에게 적합한 에셋에 보다 직접 액세스할 수 있습니다. 폴더 또는 컬렉션 공유, 스마트 컬렉션 제공(저장된 검색) 또는 올바른 자산에 대한 포인터를 사용하여 알림을 전송하는 방법 중 일부가 이들 중 하나입니다. 그러면 크리에이티브 사용자는 웹 UI에서 데스크탑 액션을 사용하여 데스크탑에서 이러한 에셋에 빠르게 액세스할 수 있습니다.

* 필요한 에셋에만 액세스하거나 관심 있는 에셋에 대한 액세스를 기본적으로 제한하여 크리에이티브 사용자를 위해 DAM 저장소에 대한 보기를 간소화하기 위해 에셋에 대한 올바른 권한(액세스 제어)을 고려합니다.

   * 크리에이티브 사용자와 관련되지 않는 특정 영역은 사용자 그룹에 대해 거부될 수 있으며 해당 영역을 보기에서 제거할 수 있습니다(데스크톱에서도).

   * DAM의 대부분의 에셋은 최종적으로 확정적이며 변경 목적이 아님 - 크리에이티브 사용자를 위해 읽기 전용이어야 합니다.

   * 변경 또는 수정 작업이 필요한 에셋만 크리에이티브 사용자가 쓸 수 있도록 쓰여야 합니다. 일부 조직에서는 AEM 프로젝트 및 폴더를 사용하여 여전히 변경 사항이 있는 자산을 호스팅합니다.

### 자산 검색 중 {#searching-assets}

데스크탑에서 열려는 파일을 검색하려면 다음을 수행합니다.

* AEM Assets 웹 UI를 사용하여 자산을 찾습니다. AEM Assets의 강력한 검색 기능(검색 패싯, 저장된 검색)뿐만 아니라 올바른 에셋을 찾을 수 있는 추가 기능을 제공합니다. 상태(승인, 만료), 컬렉션, 작업, 알림 및 다른 사용자/그룹과 폴더/컬렉션 공유를 기반으로 자산을 검색하는 기능과 같은 추가 필터가 포함되어 있습니다.

* 자산을 찾은 후 AEM UI의 데스크톱 작업을 사용하여 데스크탑의 자산에 액세스합니다.

### AEM 데스크톱 앱 {#updating-assets-opened-using-aem-desktop-app}을(를) 사용하여 연 자산 업데이트

AEM Assets에서 로컬 네트워크 공유에 매핑되는 위치에서 직접 자산을 편집하는 경우, 에셋은 데스크탑에 저장할 때마다 AEM에 업로드됩니다. 또한 AEM은 버전을 만들고 변환을 생성합니다.

AEM에 저장된 자산에 업데이트가 필요한 경우:

* 승인 프로세스의 일부 수정 요청과 같이 **부 업데이트**&#x200B;의 경우:

   * 파일을 체크 아웃하고 데스크탑에서 엽니다.

   * 파일을 업데이트합니다.

   * 업데이트된 버전을 저장합니다. 자산이 업데이트되고 타임라인에 비교를 위한 원본 버전이 표시됩니다.

* 작은 크리에이티브 WIP 주기가 필요한 변경 요청과 같은 **주요 업데이트**&#x200B;의 경우:

   * 바탕 화면에서 적절한 폴더를 열려면 표시 옵션을 사용합니다.

   * 매핑된 AEM Assets 공유 외부의 WIP 폴더에 파일을 복사합니다(예: 파일을 Adobe Creative Cloud 데스크톱 앱과 동기화된 폴더에 복사).

   * 파일을 작업하고 간헐적으로 저장합니다. 변경 사항은 AEM Assets에 저장되지 않습니다.

   * 편집이 완료되면 AEM에서 매핑한 파일을 이동, 복사 또는 저장하여 새 버전으로 업로드합니다.

## 네트워크 성능 {#network-performance}

AEM 데스크탑 앱을 사용하는 사용자에게 좋은 환경은 데스크탑과 AEM 서버 간, 특히 자산 업로드 및 업데이트 시 적절한 성능을 위해 조정된 서버에 따라, 원활하고 안정된 네트워크 연결이 크게 좌우됩니다. 이러한 권장 사항은 조직의 네트워크/IT 팀을 위한 것입니다.

### 네트워크 고려 사항 {#network-considerations}

AEM Assets 네트워크 구성에 대한 우수 사례를 이해하려면 [AEM Assets 네트워크 고려 사항](https://experienceleague.adobe.com/docs/experience-manager-64/assets/administer/assets-migration-guide.html) 문서를 참조하십시오. 사용자를 위해 AEM 데스크탑 앱 경험을 최적화하는 데 도움이 되는 몇 가지 중요한 사항은 다음과 같습니다.

* **올바르게 구성된 Dispatcher를 사용합니다**. 추가 보안을 위해 AEM Dispatcher를 사용하고 디스패처 뒤에 있는 AEM에 대한 [AEM 데스크탑 앱 연결에 대해 구성되어 있는지 확인합니다.](install-configure-app-v1.md#connect-to-an-aem-instance-behind-a-dispatcher)

* **대역폭을 저장합니다**. Finder를 사용하여 마운트된 저장소를 검색할 때 Mac의 Finder에서 아이콘 미리 보기를 끄는 것이 좋습니다. 파인더가 각 파일에 미리 보기를 생성하도록 요청하고 데스크톱 앱이 자산을 로컬로 다운로드 및 캐시하도록 합니다. 대역폭을 저장하는 동안 데스크탑에 있는 사용자에 대한 사용자 경험이 감소하므로 자산 및/또는 제한된 대역폭이 있는 저장소를 사용하여 작업할 때 이 작업이 수행되어야 합니다.

>[!NOTE]
>
>아이콘 미리 보기를 해제하려면 Finder에서 [!UICONTROL View]으로 이동하여 [!UICONTROL View Options]을 선택한 다음 [!UICONTROL Show icon preview] 옵션을 선택 해제합니다. 현재 폴더에만 사용할 수 있습니다. 기본적으로 설정하려면 동일한 대화 상자에서 [!UICONTROL Use as default] 옵션을 클릭합니다.

### 서버 성능 최적화 {#optimizing-server-performance}

AEM Assets 서버를 성능에 맞게 최적화하는 방법을 이해하려면 [AEM Assets 성능 조정 안내서](https://experienceleague.adobe.com/docs/experience-manager-65/assets/administer/performance-tuning-guidelines.html)를 참조하십시오. AEM 데스크톱 응용 프로그램의 서버 성능에 대한 일부 중요한 측면은 자산 업로드를 위해 제대로 수행되도록 워크플로 구성을 최적화하는 것에 있습니다.

* **더 많은 성능 에셋 업로드**. [AEM 에셋 업데이트 워크플로 모델을 일시적인 ](https://experienceleague.adobe.com/docs/experience-manager-65/assets/administer/performance-tuning-guidelines.html)으로 구성합니다.

* **업로드에 대한 서버 CPU를 제한합니다**. 업로드가 모든 CPU를 소모하지 않도록 최대 병렬 워크플로우 작업 매개 변수가 올바르게 설정되어 있는지 확인합니다.
