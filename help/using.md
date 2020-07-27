---
title: Adobe Experience Manager 데스크탑 앱 사용
description: Win 또는 Mac 데스크탑에서 바로 Adobe Experience Manager DAM 에셋을 사용하여 Adobe Experience Manager 데스크탑 앱을 설치하고 사용하는 방법에 대해 학습합니다. 모범 사례 및 문제 해결 정보를 확인하십시오.
uuid: 55057617-89de-43cd-8419-1252a42ab2fb
contentOwner: AG
products: SG_EXPERIENCEMANAGER/6.3/ASSETS
discoiquuid: 39d7bcad-d7b0-4978-a790-4cb68b8a7d6a
mini-toc-levels: 1
translation-type: tm+mt
source-git-commit: 27cc0ba26622016ce82b758fb0607652176f6992
workflow-type: tm+mt
source-wordcount: '3995'
ht-degree: 0%

---


# Use Adobe Experience Manager desktop app {#use-aem-desktop-app-v2}

Adobe Experience Manager(AEM) 데스크탑 앱을 사용하여 로컬 데스크탑에서 Adobe Experience Manager DAM 자산에 손쉽게 액세스하고 모든 데스크탑 애플리케이션에서 이러한 자산을 사용할 수 있습니다. 데스크톱 응용 프로그램에서 자산을 열고 자산을 로컬로 편집할 수 있습니다. 변경 내용을 버전 제어를 통해 Experience Manager으로 다시 업로드하여 다른 사용자와 업데이트를 공유할 수 있습니다. Experience Manager DAM에서 새 파일 및 폴더 계층을 Experience Manager에 업로드하고, 폴더를 만들고, 자산 또는 폴더를 삭제할 수도 있습니다.

통합을 통해 조직의 다양한 역할이 Experience Manager 에셋에서 중앙에서 자산을 관리하고 Windows 또는 Mac OS의 기본 애플리케이션에서 로컬 데스크탑에 있는 에셋에 액세스할 수 있습니다.

로그아웃한 후 또는 처음으로 응용 프로그램을 열 때는 Experience Manager 서버의 URL을 제공합니다. [연결]을 클릭합니다. 응용 프로그램을 서버와 연결하려면 자격 증명을 제공하십시오.

Experience Manager 데스크탑 앱을 사용하는 주요 작업은 다음과 같습니다.

![데스크탑 앱 [!DNL Experience Manager] 을 사용하여 수행할 수 있는 워크플로우 및](assets/aem_desktop_app_usecases_v2.png "작업 Adobe Experience Manager 데스크탑 앱")을 사용하여 수행할 수 [있는 작업 이](assets/aem_desktop_app_usecases_print.pdf) 인쇄용 PDF 파일 다운로드

## 데스크탑 앱 작동 방식 {#how-app-works2}

애플리케이션 사용을 시작하기 전에 앱의 작동 [방식을 이해해야 합니다](release-notes.md#how-app-works). 또한 다음 용어를 숙지하십시오.

* **[!UICONTROL Desktop Actions]**: 자산 웹 인터페이스에서 브라우저 내에서 자산 위치를 탐색하거나 체크 아웃하고 기본 데스크탑 애플리케이션에서 편집할 자산을 열 수 있습니다. 이러한 작업은 웹 인터페이스에서 사용할 수 있으며 데스크탑 앱 기능을 사용합니다. 데스크톱 작업 [을 활성화하는 방법을 참조하십시오](using.md#desktopactions-v2).

* 파일 상태 **[!UICONTROL Cloud Only]**: 이러한 자산은 로컬 컴퓨터에서 다운로드되지 않으며 Experience Manager 서버에서만 사용할 수 있습니다.

* 파일 상태 **[!UICONTROL Available locally]**: 에셋은 다운로드되고 있는 그대로 로컬 시스템에서 사용할 수 있습니다. 자산은 변경되지 않습니다.

* 파일 상태 **[!UICONTROL Edited locally]**: 이러한 자산은 로컬에서 수정되며 변경 내용은 Experience Manager 서버에 업로드된 상태로 유지됩니다. 업로드하면 상태가 로 변경됩니다 [!UICONTROL Available locally]. 자산 [편집을 참조하십시오](using.md#edit-assets-upload-updated-assets).

* 파일 상태 **[!UICONTROL Editing conflict]**: 사용자와 다른 사용자가 자산을 동시에 수정하는 경우 앱은 편집 충돌이 발생했음을 나타냅니다. 또한 이 앱은 변경 사항을 유지하거나 취소할 수 있는 옵션도 제공합니다. 편집 충돌을 방지하는 [방법을 확인하십시오](using.md#adv-workflow-collaborate-avoid-conflicts).

* 파일 상태 **[!UICONTROL Modified remotely]**: 앱은 다운로드한 자산이 Experience Manager 서버에서 변경되었는지 여부를 나타냅니다. 또한 앱은 최신 버전을 다운로드하고 로컬 복사본을 업데이트하는 옵션도 제공합니다. 편집 충돌을 방지하는 [방법을 확인하십시오](using.md#adv-workflow-collaborate-avoid-conflicts).

* **[!UICONTROL Check-out]**: 파일을 편집하거나 파일을 편집하려면 상태를 전환하여 체크 아웃합니다. 앱과 AEM 웹 인터페이스의 자산에 잠금 아이콘이 추가됩니다. 잠금 아이콘은 편집 충돌이 발생할 때 동일한 자산을 동시에 편집하지 않도록 다른 사용자에게 알립니다.

* **[!UICONTROL Check-in]**: 편집 충돌을 발생시키지 않고 다른 사용자가 편집할 수 있도록 에셋을 안전한 것으로 표시합니다. 변경 내용을 업로드하면 잠금 아이콘이 자동으로 제거됩니다. 체크 인 상태를 전환하면 변경 사항을 업로드하지 않고 수동으로 체크 인하지 않는 것이 좋지만 잠금 아이콘이 제거됩니다. 변경 내용을 취소한 경우 체크 인을 수동으로 전환합니다.

* **[!UICONTROL Open]** action: 기본 애플리케이션에서 자산을 열어 미리 보면 됩니다. 자산을 체크 아웃하지 않고 다른 사용자가 편집을 하면 편집 충돌이 발생하므로 이 작업을 사용하여 자산을 편집하는 것이 좋습니다.

* **[!UICONTROL Edit]** action: 동작을 사용하여 이미지를 수정합니다. 작업을 클릭하면 자동으로 자산이 체크 아웃되고 자산에 잠금 아이콘이 추가됩니다. [!UICONTROL Edit] 편집을 클릭한 후 자산을 편집하지 않으려면 을 클릭합니다 [!UICONTROL Toggle check-in]. AEM DAM 폴더 계층 구조에서 자산을 삭제하거나 이름을 바꾸거나 이동하려면 편집 작업이 아닌 AEM 웹 인터페이스 작업을 사용하십시오.

* **[!UICONTROL Download]** action: 로컬 컴퓨터에 자산을 다운로드합니다. 지금 자산을 다운로드하고 나중에 편집할 수 있습니다. 오프라인으로 작업하고 나중에 변경 내용을 업로드합니다. 에셋이 파일 시스템의 캐시 폴더에 다운로드됩니다.

* **[!UICONTROL Reveal File]** 또는 작업: **[!UICONTROL Reveal Folder]** 자산이 로컬 캐시 폴더에 다운로드되는 동안 앱은 로컬 네트워크 드라이브를 흉내내고 각 자산에 대한 로컬 경로를 제공합니다. 이 경로를 알려면 앱에서 적절한 표시 옵션을 사용하십시오. Creative Cloud 애플리케이션에 에셋을 배치하려면 표시 작업이 필요합니다. 자산 [가져오기를 참조하십시오](using.md#place-assets-in-native-documents).

* **[!UICONTROL Open In Web]** action: AEM 웹 인터페이스에서 자산을 보려면 웹에서 엽니다. 메타데이터 또는 자산 검색과 같은 AEM 인터페이스에서 더 많은 워크플로우를 시작할 수 있습니다.

* **[!UICONTROL Delete]** action: AEM DAM 저장소에서 자산을 삭제합니다. AEM 서버에서 자산의 원본 사본이 삭제됩니다. 로컬 자산의 수정 내용만 [취소하려면 변경 내용 취소를 참조하십시오](using.md#edit-assets-upload-updated-assets).

* **[!UICONTROL Upload Changes]**: 데스크톱 앱은 AEM 서버에 명시적으로 업로드할 때만 업데이트된 자산을 업로드합니다. 편집 내용을 저장할 때 변경 내용은 로컬 컴퓨터에만 저장됩니다. 업로드하면 자산이 자동으로 체크 인되고 잠금 아이콘이 제거됩니다. 자산 [편집을 참조하십시오](using.md#edit-assets-upload-updated-assets).

## AEM 웹 인터페이스에서 데스크톱 작업 활성화 {#desktopactions-v2}

브라우저의 자산 사용자 인터페이스 내에서 자산 위치를 탐색하거나 체크 아웃하고 자산을 열어 데스크탑 애플리케이션에서 편집할 수 있습니다. 이러한 옵션은 호출되며 [!UICONTROL Desktop Actions] 기본적으로 활성화되지 않습니다. 활성화하려면 다음 단계를 수행합니다.

1. 자산 콘솔의 도구 모음에서 **[!UICONTROL User]** 아이콘을 클릭/탭합니다.
1. 을 클릭/탭하여 대화 상자 **[!UICONTROL My Preferences]** 를 **[!UICONTROL Preferences]** 표시합니다.
1. 사용자 환경 설정 대화 상자에서 을 선택합니다 **[!UICONTROL Show Desktop Actions For Assets]**. 클릭/탭 **[!UICONTROL Accept]**.

   ![데스크톱 작업을 활성화하려면 자산에 대한 데스크톱 작업 표시를 선택합니다.](assets/chlimage_1-3.png)

   데스크탑 작업 [!UICONTROL Show Desktop Actions For Assets] 을 활성화하려면 확인

## 에셋 검색, 미리 보기 {#browse-search-preview-assets}

데스크톱 응용 프로그램 내에서 AEM 저장소에서 사용 가능한 자산을 찾아보고, 검색하고, 미리 볼 수 있습니다. 앱에서 다음 작업을 시도하십시오.

1. 폴더를 검색하여 모든 에셋의 작은 축소판과 함께 폴더에서 사용 가능한 에셋의 몇 가지 기본 정보를 볼 수 있습니다.

   ![DAM 파일 및 폴더](assets/browse_folder_da2.png "검색DAM 파일 및 폴더 찾아보기")

1. 자세한 정보와 개별 자산의 큰 축소판을 보려면 파일 이름을 클릭합니다.

   ![자산 및 작업의 더 큰 미리](assets/large_preview_actions_da2.png "보기자산 및 작업의 더 큰 미리 보기 보기")

1. 또는 **[!UICONTROL Open]** **[!UICONTROL Edit]** 를 클릭하여 로컬로 파일을 다운로드하고 기본 애플리케이션에서 보거나 편집할 수 있습니다.
1. 키워드를 사용하여 검색하여 AEM 저장소에서 관련 자산을 찾습니다. 와일드카드로 `?` 및 를 `*` 사용합니다. 이러한 와일드카드는 단일 문자 또는 여러 문자로 각각 대체됩니다. 필요에 따라 결과를 필터링하고 정렬합니다.

   ![별표 와일드카드를 사용한 샘플](assets/search_wildcard_da2.png "검색별표 와일드카드를 사용한 샘플 검색")

   ![별표 와일드카드를 사용하는 다른 샘플 검색](assets/search_wildcard2_da2.png "별표 와일드카드가 다른 위치를 갖는 다른 샘플 검색")

>[!NOTE]
>
>앱은 자산의 제목이나 파일 이름뿐만 아니라 여러 메타데이터 필드에서 검색 기준을 일치시켜 자산을 표시합니다.

## 자산 다운로드 {#download-assets}

로컬 파일 시스템에서 에셋을 다운로드할 수 있습니다. 앱이 AEM 서버의 자산을 가져오고 로컬 파일 시스템에 동일한 사본을 저장합니다.

옵션을 보려면 ![추가 옵션 아이콘](assets/do-not-localize/more2_da2.png) 을 클릭하고 ![다운로드 아이콘](assets/do-not-localize/download_cloud_da2.png) 을 클릭하여 다운로드합니다.

![자산 다운로드 옵션](assets/download_option_da2.png "자산에 대한 다운로드 옵션")

>[!NOTE]
>
>대용량 파일 또는 여러 파일을 다운로드하거나 업로드할 때, 응용 프로그램은 자산 및 폴더에 대한 작업을 끕니다. 다운로드 또는 업로드가 완료되면 작업을 사용할 수 있습니다.

큐 크기가 크거나 네트워크 문제가 발생하는 경우 여러 에셋을 다운로드하면 성능이 저하될 수 있습니다. 또한 폴더를 다운로드할 때 많은 에셋을 모르고 대기열에 보관할 수 있습니다. 장시간 대기 시간을 피하기 위해 앱은 한 번에 다운로드한 자산의 수를 제한합니다. 구성 방법을 알려면 환경 설정 [설정을 참조하십시오](install-upgrade.md#set-preferences). 이 제한보다 낮더라도, 앱이 때로 큰 폴더를 다운로드하기 전에 확인을 요구할 수 있습니다.

![앱이 상대적으로 많은 수의](assets/download_confirmation_da2.png "에셋 다운로드를 확인앱은 상대적으로 많은 수의 에셋을 다운로드했음을 확인합니다")

폴더를 선택하고 다운로드한 경우 애플리케이션은 AEM의 폴더에 직접 저장된 자산만 다운로드합니다. 하위 폴더에서 자산을 자동으로 다운로드하지 않습니다.

## 데스크탑에서 에셋 열기 {#openondesktop-v2}

기본 응용 프로그램에서 볼 원격 자산을 열 수 있습니다. 에셋이 로컬 폴더로 다운로드되고 파일 형식과 관련된 기본 애플리케이션에서 실행됩니다. 기본 애플리케이션을 Mac 또는 Windows에서 특정 파일 유형(익스텐션)으로 변경할 수 있습니다.

자산 메뉴 **[!UICONTROL Open]** 에서 을 클릭합니다. 자산이 로컬로 다운로드되고 기본 응용 프로그램에서 열립니다. 상태 표시줄에서 대용량 에셋의 다운로드 진행 및 전송 속도를 확인합니다.

<!-- ![Download progress bar for large-sized assets](assets/download_status_bar_da2.png "Download progress bar for large-sized assets")
-->

>[!NOTE]
>
>예상 변경 사항이 앱에 반영되지 않은 경우 새로 고침 아이콘 ![새로 고침 아이콘을](assets/do-not-localize/refresh.png) 클릭하거나 앱 인터페이스에서 마우스 오른쪽 버튼을 클릭하고 을 클릭합니다 **[!UICONTROL Refresh]**. 더 큰 다운로드 또는 업로드가 진행 중이면 작업을 사용할 수 없습니다.

자산의 로컬 다운로드 폴더를 열려면 ![추가 작업 아이콘](assets/do-not-localize/more2_da2.png) 을 클릭하고 ![표시 아이콘](assets/do-not-localize/reveal_action2_da2.png) 동작을 클릭합니다 **[!UICONTROL Reveal File]** .

## 기본 문서에 에셋 사용 또는 배치 {#place-assets-in-native-documents}

에셋을 기본 문서에 가져올 때 Windows 탐색기 또는 Mac Finder에서 파일에 액세스하는 경우가 있습니다. 로컬로 다운로드한 파일의 파일 시스템 위치로 이동하려면 [표시] 아이콘 ![옵션을 사용합니다](assets/do-not-localize/reveal_action2_da2.png) **[!UICONTROL Reveal File]** .

![자산에 대한 파일 작업](assets/revealfile_action_da2.png "표시자산에 대한 파일 표시 작업")

로컬 컴퓨터 **[!UICONTROL Reveal File]**&#x200B;에서 파일 또는 폴더를 미리 선택한 상태로 Windows 탐색기 또는 Mac Finder를 열려면 을 클릭하거나 **[!UICONTROL Reveal Folder]** 폴더를 클릭하십시오. 이 옵션은 로컬 파일 배치 또는 연결을 지원하는 기본 애플리케이션에 AEM 파일을 배치하는 데 유용합니다. Adobe InDesign에서 파일을 가져오는 방법을 보려면 그래픽 [가져오기를 참조하십시오](https://helpx.adobe.com/indesign/using/placing-graphics.html).

작업은 로컬로 사용할 수 있는 자산만 표시하는 로컬 네트워크 공유를 **[!UICONTROL Reveal File]** 엽니다. 즉, 앱을 사용하여 표시하거나, 다운로드하거나, 열거나 편집한 자산을 표시합니다. 로컬 네트워크 공유에서는 AEM에 대한 변경 사항을 업로드하지 않습니다. 변경 내용을 업로드하려면 앱에서 명시적으로 **[!UICONTROL Upload Changes]** 또는 작업 **[!UICONTROL Upload]** 을 사용하십시오.

>[!NOTE]
>
>AEM 데스크톱 앱 v1.x와의 이전 호환성을 위해, 표시되는 파일은 로컬 네트워크 공유에서 제공되므로 로컬에서 사용할 수 있는 파일만 노출됩니다. 표시되는 파일의 데스크탑 경로는 앱 v1.x에서 만든 경로와 동일합니다.

>[!CAUTION]
>
>기본 응용 프로그램에서 자산을 편집할 때 **[!UICONTROL Reveal File]** 옵션을 사용하지 마십시오. 대신 동작을 **[!UICONTROL Edit]** 사용하십시오. 자세한 내용은 [고급 워크플로우를 참조하십시오. 동일한 파일에서 공동 작업하고 편집 충돌을 방지할 수 있습니다](#adv-workflow-collaborate-avoid-conflicts).

## 자산 편집 및 업데이트된 에셋 업로드 {#edit-assets-upload-updated-assets}

변경할 때 편집할 자산을 열고 업데이트된 자산을 AEM 서버에 업로드합니다. 다른 사용자의 편집과 충돌을 방지하려면 앱을 사용하여 편집 세션을 시작합니다. 편집을 시작하기 전에, 자산에 잠금 아이콘이 설정되어 있지 않은지, 즉 다른 사용자가 자산을 편집하고 있지 않은지 확인하십시오.

자산을 편집하려면 자산을 검색하거나 자산의 위치로 이동합니다. 자세히 아이콘 ![을](assets/do-not-localize/more2_da2.png) 클릭하고 을 클릭합니다 **[!UICONTROL Edit]**.

다음 두 상황 **[!UICONTROL Toggle Check-out]** 에서 다른 사용자의 편집과 충돌을 방지하기 위해 자산을 잠그는 데 사용합니다.

* 자산을 먼저 확인하지 않고 편집을 시작했습니다(즉, 열기만 하면).
* 에셋 편집을 곧 시작할 계획이며 다른 사람이 편집하기를 원하지 않습니다.

편집을 완료하면 앱이 변경된 에셋의 **[!UICONTROL Edited Locally]** 상태를 표시합니다. 자산에 저장된 모든 변경 사항은 AEM에 변경 사항을 업로드할 때까지 로컬만 적용됩니다. 개인 또는 일부 자산을 하나씩 업로드하려면 자산의 옵션 **[!UICONTROL Upload Changes]** 에서 을 클릭합니다. AEM에 자산의 버전이 만들어집니다. AEM Assets의 웹 인터페이스를 사용하면 [타임라인 보기에서 자산 내역을 볼 수 있습니다](https://docs.adobe.com/content/help/en/experience-manager-65/assets/using/activity-stream.html).

![앱의 변경 내용 업로드 옵션](assets/upload_changes_single1_da2.png "앱의 변경 내용 업로드")

![자산의 대규모 미리 보기를 볼 때 변경 내용 업로드](assets/upload_changes_single2_da2.png "옵션자산의 큰 미리 보기를 볼 때 변경 내용 업로드")

공동 작업 편집에 대한 우수 사례를 보려면 [고급 워크플로우를 참조하십시오. 동일한 파일에서 공동 작업하고 편집 충돌을 방지할 수 있습니다](#adv-workflow-collaborate-avoid-conflicts).

다음 경우 로컬 자산에 대한 변경 사항 및 편집 내용을 취소할 수 있습니다. 클릭 **[!UICONTROL Discard Changes]**.

* AEM에서 로컬 변경 사항을 저장하지 않으려면
* 일부 변경 사항을 저장한 후 원래 에셋을 변경하기 시작합니다.
* 더 이상 필요하지 않으므로 에셋 편집을 중지합니다.

필요한 경우 체크 아웃을 전환합니다. 업데이트된 자산이 로컬 캐시 폴더에서 제거되고 편집 또는 열 때 다시 다운로드됩니다.

## AEM에 새 자산 업로드 및 추가 {#upload-and-add-new-assets-to-aem}

사용자는 DAM 저장소에 새 자산을 추가할 수 있습니다. 예를 들어 사진 촬영에서 AEM 저장소에 많은 수의 사진을 추가하려는 에이전시 사진 작가 또는 계약업체일 수 있습니다. AEM에 새 콘텐츠를 추가하려면 앱 상단 ![에서 클라우드에 업로드 아이콘](assets/do-not-localize/upload_to_cloud_da2.png) 을 클릭합니다. 로컬 파일 시스템에서 자산 파일을 탐색하고 을 클릭합니다 **[!UICONTROL Select]**. 앱이 자산을 업로드하기 시작하고 자산을 업로드하는 데 시간이 더 걸리는 경우 하단에 진행률 표시줄을 표시합니다. 폴더를 만들거나 업로드할 때 공백과 잘못된 문자를 사용하지 마십시오. AEM Assets에서 폴더 [만들기에서 문자 목록을 참조하십시오](https://docs.adobe.com/content/help/en/experience-manager-65/assets/managing/managing-assets-touch-ui.html#Creatingfolders).

<!-- ![Download progress bar for large-sized assets](assets/upload_status_da2.png "Download progress bar for large-sized assets")
-->

로컬 파일 시스템에서 폴더 또는 개별 파일을 업로드할 수 있습니다. 폴더의 계층은 업로드될 때 유지됩니다. 자산을 일괄 업로드하기 전에 벌크 [업로드를 참조하십시오](#bulk-upload-assets).

지정된 세션에서 전송된 자산 목록을 보려면 **[!UICONTROL View]** > 을 클릭합니다 **[!UICONTROL Assets transfers]**. 목록을 사용하면 현재 세션의 파일 전송을 보고 신속하게 확인할 수 있습니다.

![특정 세션의 전송된 자산](assets/assets_transfered_da2.png "목록특정 세션의 전송된 자산 목록")

> 설정에서 업로드 동시 실행(가속)을 제어할 수 **[!UICONTROL Preferences]** **[!UICONTROL Upload acceleration]** 있습니다. 더 많은 동시 사용은 일반적으로 더 빠른 업로드를 제공하지만, 리소스를 많이 사용하므로 로컬 시스템의 처리 능력이 더 많이 소모될 수 있습니다. 느린 시스템을 사용하는 경우 낮은 동시 시청 값을 사용하여 다시 업로드합니다.

>[!NOTE]
>
>전송 목록은 지속적이지 않으며 앱을 종료하고 다시 열면 사용할 수 없습니다.

>[!NOTE]
>
>파일이 업로드되지 않고 AEM 6.5.1 이상 배포에 연결하는 경우 이 [문제 해결 정보를 참조하십시오](troubleshoot.md#upload-fails).

## 여러 에셋을 사용한 작업 {#work-with-multiple-assets}

사용자는 이동 중에 모든 편집 내용을 업로드하거나 몇 번의 클릭으로 중첩된 폴더를 업로드하는 등의 작업을 통해 여러 에셋을 간편하게 작업하고 관리할 수 있습니다.

### 큰 폴더 찾아보기 {#browse-large-folders}

많은 에셋이 포함된 폴더로 작업할 때 스크롤하여 더 많은 에셋을 봅니다. 키보드를 사용하여 스크롤하려면 Tab 키를 몇 번 눌러 위쪽에서 자산을 선택합니다. 강조 표시된 에셋을 선택하면 해당 에셋이 선택되는지 확인할 수 있습니다. 이제 아래쪽 화살표 키를 사용하여 자산 목록을 이동합니다.

### 선택한 자산에 대한 빠른 작업 {#quick-actions-for-selected-assets}

몇 가지 자산의 축소판을 클릭하여 자산을 선택합니다. 모든 자산을 선택하려면 앱의 상단 표시줄에 있는 확인란을 클릭합니다. 선택한 모든 자산에 적용되는 작업 세트가 앱 하단의 도구 모음에 함께 표시됩니다.

![아래쪽의 도구 모음에는 선택한 자산과 관련된](assets/actions_bottom_toolbar1_da2.png "작업이 표시하단의 도구 모음에는 선택한 자산에 대한 일반적인 작업이 표시됩니다")

![선택 항목에 대한 일반적인 작업이 없는 경우 도구](assets/actions_bottom_toolbar2_da2.png "모음에 작업 없음선택 영역에 대한 일반적인 작업이 없는 경우 도구 모음에 작업 없음")

아래쪽의 도구 모음에서 사용할 수 있는 작업은 선택한 파일의 상태에 따라 달라집니다. 예를 들어 **[!UICONTROL Edited Locally]** 파일만 선택하면 아이콘이 **[!UICONTROL Upload Changes]** 표시됩니다. 및 조합을 선택하는 경우 작업 **[!UICONTROL Edited locally]** 을 사용할 **[!UICONTROL Cloud only]**&#x200B;수 **[!UICONTROL Upload Changes]** 없습니다.

### 편집한 모든 이미지 찾기 {#find-all-edited-images}

응용 프로그램은 로컬로(또는 작업 **[!UICONTROL Edited locally]**&#x200B;을 통해) 다운로드한 다음 수정한 모든 파일에 빠르게 액세스할 수 있도록 하는 보기( [!UICONTROL Open] 또는 [!UICONTROL Edit] 보기)를 제공합니다. 이 앱을 사용하면 로컬에서 편집한 모든 에셋을 선택하고 몇 번의 클릭만으로 변경 내용을 업로드할 수 있습니다. 이 보기에는 편집과 충돌이 있는 로컬에서 편집된 에셋도 표시됩니다.

![로컬에서 편집한 모든](assets/edited_locally_filter_da2.png "자산 보기 필터로컬에서 편집한 모든 자산 보기&#40;편집 내용의 일괄 업로드&#41;")

### 자산 일괄 업로드 {#bulk-upload-assets}

사진 작가 또는 크리에이티브 에이전시와 같은 사용자 또는 조직은 AEM 외부에서 수행한 더 큰 세트에서 사진 촬영, 수정, 선택 등 다양한 로컬 자산을 만들 수 있습니다. 이러한 대규모 로컬 폴더를 데스크탑 앱에서 바로 AEM Assets에 업로드할 수 있습니다. 폴더 계층은 보존되고 모든 중첩 하위 폴더 및 포함된 자산이 업로드됩니다. 업로드된 에셋은 동일한 서버의 다른 사용자도 즉시 사용할 수 있습니다. 자산이 백그라운드에서 업로드되므로 작업은 웹 브라우저 세션에 연결되어 있지 않습니다.

![데스크탑에서 여러 로컬 폴더를 AEMB에 일괄](assets/upload_local_folders_da2.png "업로드데스크탑에서 여러 로컬 폴더를 AEM으로 업로드합니다.")

업로드 후 예상 변경 사항이 앱에 반영되지 않으면 새로 고침 아이콘 새로 고침 아이콘 ![을 클릭합니다](assets/do-not-localize/refresh.png).

>[!NOTE]
>
>두 AEM 배포 간에 자산을 마이그레이션하는 데 업로드 기능을 사용하지 마십시오. 대신 [마이그레이션 안내서를 참조하십시오](https://docs.adobe.com/content/help/en/experience-manager-65/assets/administer/assets-migration-guide.html).

### 전송된 자산 목록 {#list-of-transferred-assets}

지정된 세션에서 전송된 자산 목록을 보려면 AEM에 [자산 업로드를 참조하십시오](#upload-and-add-new-assets-to-aem).

## 고급 워크플로우: AEM Assets 웹 인터페이스에서 시작 {#adv-workflow-start-from-aem-ui}

필요한 경우 AEM Assets 웹 인터페이스에서 워크플로우를 시작합니다. 데스크탑 앱은 AEM과 통합되므로 데스크탑 동작을 사용하여 요청할 때 인계받을 수 있습니다.

웹 인터페이스에서 워크플로우를 시작하는 특별한 경우는 자산 검색입니다. 자산 사용자 인터페이스의 Omnisearch 막대는 고급 검색 환경을 제공합니다. 먼저 웹에서 원하는 자산을 찾은 다음 앱에서 워크플로우를 시작할 수 있습니다. [!UICONTROL Desktop Actions] 일부 샘플 사례에는 패싯을 사용하여 검색 결과 필터링, Adobe Stock에서 라이선스가 부여된 특정 에셋 찾기 또는 웹 인터페이스에서 보다 나은 검색 결과를 얻을 수 있도록 조직에서 구현한 사용자 지정 등이 있습니다.

데스크톱 앱 기능은 자산 웹 인터페이스에서 다음 작업을 시도할 때 사용됩니다.

* The [!UICONTROL Desktop Actions] that allows [!UICONTROL Open], [!UICONTROL Edit], and [!UICONTROL Reveal]
* [!UICONTROL Upload folder]
* [!UICONTROL Check-out] 또는 [!UICONTROL check-in]

예를 들어 앱에서 체크 아웃된 자산에 대해 사용할 수 있는 웹 인터페이스의 작업은 [!UICONTROL Open]및 [!UICONTROL Reveal]입니다 [!UICONTROL Check-in].

![AEM 웹](assets/assets_web_actions_da2.png "인터페이스의 데스크톱 작업AEM 웹 인터페이스의 데스크톱 작업")

>[!NOTE]
>
>브라우저가 사용자에게 Adobe Experience Manager 데스크톱 시작을 허용할지 여부를 묻는 메시지를 표시할 수 있습니다. 브라우저에서 앱으로 중단 없이 전송하려면 해당 확인란을 선택하여 항상 앱을 인계받을 수 있습니다.

다음 정보나 워크플로우는 웹 인터페이스를 사용하여 찾을 수 없습니다. 웹 인터페이스가 로컬 변경 사항을 추적하지 않고 다음을 알지 못하므로 데스크탑 앱을 사용하십시오.

* 로컬에서 편집한 파일
* 편집 충돌이 있는 파일과 이를 해결하는 방법
* AEM에 로컬 변경 사항을 업로드합니다.
* 로컬에서 사용 가능한 파일의 다양한 상태

반대로, 작업을 사용하여 데스크탑 앱부터 시작되는 웹 인터페이스에서 자산을 열 수 **[!UICONTROL Open In Web]** 있습니다.

## 고급 워크플로우: 동일한 파일 공동 작업 및 편집 충돌 방지 {#adv-workflow-collaborate-avoid-conflicts}

공동 작업 환경에서 여러 사용자가 동일한 에셋 세트를 사용하여 버전 간 충돌을 발생시킬 수 있습니다. 충돌을 방지하려면 다음 우수 사례를 따르십시오.

* 클릭하여 자산을 편집하지 마십시오 [!UICONTROL Open]. 파일 시스템 폴더에서 열어 로컬로 다운로드한 에셋을 편집하지 마십시오. 다른 사용자는 에셋이 편집 중임을 알지 못합니다.
* 자산을 편집하려면 항상 클릭합니다 [!UICONTROL Edit]. 기본 애플리케이션에서 자산을 열고 자산에 잠금 아이콘을 추가하므로 다른 사용자는 에셋이 편집되고 있음을 알 수 있습니다.
* 클릭하지 [!UICONTROL Toggle Check-in] 않고 실수로 편집을 시작한 경우 을 클릭합니다 [!UICONTROL Edit]. 자산에 잠금 아이콘이 추가됩니다. 나중에 에셋을 편집할 계획이지만 다른 사람이 에셋을 편집하지 않도록 하려는 경우에도 에셋을 [!UICONTROL Toggle Check-in] 잠그려면 을 클릭합니다.
* 자산을 편집하기 전에 다른 사용자가 해당 자산을 편집하지 않는지 확인하십시오. 자산에서 잠금 아이콘을 찾습니다.
* 편집을 완료한 후 모든 변경 내용을 업로드한 다음 자산을 체크 인합니다.

![편집 충돌 상태편집](assets/edits_conflicts_status_da2.png "충돌 상태")

로컬로 다운로드한 자산이 AEM 서버에서 업데이트되는 경우 앱에 **[!UICONTROL Modified remotely]** 상태가 표시됩니다. 로컬 복사본을 제거하거나 로컬 복사본을 새로 고칠 수 있습니다. 이 경우 [!UICONTROL Remove] 또는 [!UICONTROL Update] 각각 을 클릭합니다. 대화 상자의 링크를 통해 두 버전의 자산을 볼 수 있습니다.

![에셋이 원격으로](assets/modified_remotely_dialog_da2.png "수정되는 경우 충돌을 해결하는 옵션에셋이 원격으로 수정되는 경우 충돌을 해결하는 옵션")

로컬로 편집하고 있는 자산이 사용자의 지식 없이도 서버에서 업데이트되는 경우 앱에 **[!UICONTROL Editing Conflict]** 상태가 표시됩니다. 업데이트(클릭)를 유지하고 다른 사용자의 편집 내용을 삭제하거나 다른 사용자의 업데이트를 존중하여 자신의 변경 사항( **[!UICONTROL Keep Mine]****[!UICONTROL Overwrite Mine]**)을 삭제할 수 있습니다.

![편집 충돌 해결](assets/editing_conflict_dialog_da2.png "옵션편집 충돌 해결 옵션")

## 고급 워크플로우: InDesign 파일에서 에셋 가져오기 및 연결 {#adv-workflow-place-assets-indesign}

AEM 데스크톱 앱을 사용하여 연결된 자산이 있는 파일을 열면 자산이 미리 다운로드되어 기본 응용 프로그램에 표시됩니다. 이 워크플로우가 제대로 작동하려면 기본 애플리케이션에서 로컬 자산에 대한 링크 가져오기를 지원해야 하며 AEM에서는 바이너리 파일의 서버측 참조에 대한 이러한 링크 해결을 지원해야 합니다.

AEM 데스크탑 앱은 일부 Adobe Creative Cloud 데스크탑 애플리케이션 및 파일 포맷(Adobe InDesign, Adobe Illustrator 및 Adobe Photoshop)과 함께 이 워크플로우를 지원합니다. 워크플로우를 통해 지원되는 Creative Cloud 파일을 사용하여 효율적으로 작업할 수 있습니다. 따라서 사용자 A가 InDesign 파일에 몇 개의 자산을 배치하고 AEM에 체크 인하면, 자산이 파일의 일부가 아닌 경우에도 사용자 B가 InDesign 파일의 자산을 확인합니다. 자산은 사용자 B의 컴퓨터에서 로컬로 다운로드됩니다.

>[!NOTE]
>
>데스크탑 앱은 Windows의 모든 드라이브에 매핑할 수 있습니다. 그러나 원활한 작업을 위해 기본 드라이브 문자를 변경하지 마십시오. 동일한 조직의 사용자가 다른 드라이브 문자를 사용하는 경우 다른 사용자가 설치한 에셋을 볼 수 없습니다. 배치된 에셋은 경로 변경으로 가져오는 것이 아닙니다. 배치된 자산은 계속 바이너리 파일(예: INDD)에 배치되며 제거되지 않습니다.

이 워크플로우의 제한 사항에 대해서는 [시스템 요구 사항 및 지원되는 버전을 참조하십시오](release-notes.md#system-requirements-and-prerequisites-v2).

이미지 에셋 및 InDesign에서 이 워크플로우를 사용하려면 다음 단계를 따르십시오.

1. AEM에 배치된 에셋이 있는 INDD 파일을 간편하게 사용할 수 있습니다. 이러한 INDD 파일을 만드는 방법을 알아보려면 그래픽 [가져오기를 참조하십시오](https://helpx.adobe.com/indesign/using/placing-graphics.html).
1. 데스크톱 앱 **[!UICONTROL Edit]** 내에서 AEM에 배치된 자산이 있는 INDD 파일입니다.
1. 앱은 InDesign 파일과 연결된 에셋을 모두 다운로드합니다. InDesign에서 문서를 열면 링크가 해결되고 에셋이 다운로드되며 에셋이 InDesign 문서에 표시됩니다.
1. InDesign 파일에 새 그래픽을 배치하려면 자산에서 **[!UICONTROL Reveal File]** 액션을 사용합니다. 이렇게 하면 에셋이 로컬로 다운로드되고 Windows 탐색기 또는 Mac Finder에서 로컬 네트워크 공유 위치가 열립니다.
1. InDesign 문서에 공개된 에셋을 배치합니다. 그러면 문서에 링크가 만들어집니다.
1. InDesign 문서에서 편집을 완료하면 저장한 다음 데스크탑 앱을 사용하여 AEM에 업로드합니다.

## 고급 워크플로우: 로컬로 에셋 다운로드 {#adv-workflow-download-assets-locally}

앱은 다양한 시나리오에서 파일 시스템의 로컬로 AEM 서버에서 자산을 다운로드합니다. 다운로드는 대역폭 및 디스크 공간을 사용합니다. 이 시나리오를 이해하면 다운로드를 완료하기 위한 대기 시간을 최적화할 수 있습니다.

On-Demand 앱 내에서 자산을 다운로드합니다. 자산 [다운로드를 참조하십시오](#download-assets).

동작을 사용하여 기본 데스크톱 응용 프로그램에서 자산을 열면, 아직 로컬로 사용할 수 없는 경우 자산이 로컬로 다운로드됩니다. [!UICONTROL Open] 자산 [열기를 참조하십시오](#openondesktop-v2).

앱 내에서 자산 또는 폴더의 위치를 표시하면, 먼저 자산 또는 폴더가 로컬에서 다운로드된 후 로컬 네트워크 공유의 시스템에서 열립니다. 자산 [열기를 참조하십시오](#openondesktop-v2).

동작을 사용하여 기본 데스크톱 응용 프로그램에서 자산을 편집하는 경우, 아직 로컬에서 사용할 수 없는 경우 자산이 로컬로 다운로드됩니다. [!UICONTROL Edit] 자산 [편집 및 업데이트된 자산 업로드를 참조하십시오](#edit-assets-upload-updated-assets).

앱이 설치되고 허용되면 AEM 웹 인터페이스에서 사용할 때 작업이 완료됩니다 [!UICONTROL Desktop Actions] . 앱이 자산을 먼저 다운로드한 다음 작업을 완료합니다.
