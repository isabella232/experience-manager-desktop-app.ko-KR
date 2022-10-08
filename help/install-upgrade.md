---
title: 데스크탑 앱 설치 및 구성
description: 설치 및 구성 [!DNL Adobe Experience Manager] 데스크탑 앱 [!DNL Adobe Experience Manager Assets] 서버 및 로컬 파일 시스템에서 자산을 다운로드합니다.
feature: Desktop App,Release Information
exl-id: 422e51c1-c456-4151-bb43-4b3d29a58187
source-git-commit: 5b5970cec02d4a605bd7d826d1daa71fe228b0d9
workflow-type: tm+mt
source-wordcount: '1426'
ht-degree: 0%

---

# 설치 [!DNL Adobe Experience Manager] 데스크탑 앱 {#install-app-v2}

사용 [!DNL Adobe Experience Manager] 데스크탑 앱, 내 자산 [!DNL Experience Manager] 로컬 데스크탑에서 쉽게 사용할 수 있으며 모든 기본 데스크탑 애플리케이션에서 사용할 수 있습니다. 자산을 미리 보고 기본 데스크탑 응용 프로그램에서 열고 다른 문서에 배치하기 위해 Mac Finder 또는 Windows 탐색기에 표시하고 로컬로 변경할 수 있습니다. 변경 사항은 다시 [!DNL Experience Manager] 업로드하고 저장소에 새 버전이 만들어집니다.

이러한 통합을 통해 조직에서 다양한 역할을 수행할 수 있습니다.

* 자산을 중앙에서 관리 [!DNL Experience Manager Assets].

* 타사 애플리케이션 및 Adobe Creative Cloud을 포함한 모든 기본 데스크탑 애플리케이션에서 자산에 액세스합니다. 이렇게 하면 사용자는 브랜딩을 포함한 다양한 표준을 쉽게 준수할 수 있습니다.

를 사용하려면 [!DNL Experience Manager] 데스크탑 앱:

* 에서 [!DNL Experience Manager] 버전은에서 지원됩니다. [!DNL Experience Manager] 데스크탑 앱. 자세한 내용은 [시스템 요구 사항](release-notes.md).

* 애플리케이션을 다운로드하여 설치합니다. 자세한 내용은 [데스크탑 앱 설치](#install-v2) 아래의 제품에서 사용할 수 있습니다.

* 몇 개의 자산을 사용하여 연결을 테스트합니다. 자세한 내용은 [자산을 찾아보고 검색하는 방법](using.md#browse-search-preview-assets).

## 시스템 요구 사항, 사전 요구 사항 및 다운로드 링크 {#tech-specs-v2}

자세한 내용은 [[!DNL Experience Manager] 데스크탑 앱 릴리스 노트](release-notes.md).

## 이전 버전에서 업그레이드 {#upgrade-from-previous-version}

데스크탑 앱의 v1.x 사용자인 경우 이전 버전과 최신 앱 버전의 차이점과 유사점을 파악합니다. 자세한 내용은 [데스크탑 앱의 새로운 기능](introduction.md#whats-new-v2) 및 [앱 작동 방식](release-notes.md#how-app-works).

>[!NOTE]
>
>한 컴퓨터에 두 버전의 데스크탑 앱을 함께 사용할 수 없습니다. 버전을 설치하기 전에 다른 버전을 제거하십시오.

이전 버전의 앱에서 업그레이드하려면 다음 지침을 따르십시오.

1. 업그레이드하기 전에 모든 자산을 동기화하고 변경 사항을에 업로드하십시오 [!DNL Experience Manager]. 앱을 제거할 때 편집된 내용이 손실되지 않도록 하기 위한 것입니다.

1. 이전 버전의 앱을 제거합니다. 제거할 때 캐시를 지우려면 옵션을 선택합니다.

1. 시스템을 다시 시작합니다.

1. [다운로드](release-notes.md) 및 [설치](#install-v2) 최신 앱. 아래 지침을 따르십시오.

##  설치 {#install-v2}

데스크탑 앱을 설치하려면 다음 단계를 수행합니다. 기존 Adobe 제거 [!DNL Experience Manager] 최신 앱을 설치하기 전에 데스크탑 앱 v1.x를 사용하십시오. 자세한 내용은 위의 내용을 참조하십시오.

1. 에서 최신 설치 관리자를 다운로드합니다. [릴리스 노트](release-notes.md) 페이지.

1. 의 URL 및 자격 증명을 유지합니다 [!DNL Experience Manager] 배포가 간편합니다.

1. 다른 버전의 앱에서 업그레이드하는 경우 다음을 참조하십시오 [데스크탑 앱 업그레이드](#upgrade-from-previous-version).

1. 사용 중인 경우 이 단계를 건너뜁니다 [!DNL Experience Manager] 로서의 [!DNL Cloud Service], [!DNL Experience Manager] 6.4.4 이상 또는 [!DNL Experience Manager] 6.5.0 이상 에서 [!DNL Experience Manager] 설치 프로그램은 [릴리스 노트](release-notes.md). 필요한 경우 해당 파일을 다운로드합니다 [호환성 패키지](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/cq640/featurepack/adobe-asset-link-support) 을 사용하여 설치합니다. [!DNL Experience Manager] 패키지 관리자 [!DNL Experience Manager] 관리자 패키지를 설치하려면 다음을 참조하십시오 [패키지 작업 방법](https://experienceleague.adobe.com/docs/experience-manager-65/administering/contentmanagement/package-manager.html).

1. 설치 관리자 바이너리를 실행하고 화면 지침에 따라 설치합니다.

1. Windows에서는 설치 프로그램이 설치 여부를 `Visual Studio C++ Redistributable 2015`. 화면의 지침에 따라 설치합니다. 설치에 실패하면 수동으로 설치합니다. 설치 관리자를 [여기](https://www.microsoft.com/en-us/download/details.aspx?id=52685) 둘 다 설치합니다. `vc_redist.x64.exe` 및 `vc_redist.x86.exe` 파일. 다시 실행 [!DNL Experience Manager] 데스크탑 앱 설치 관리자.

1. 메시지가 표시되면 시스템을 다시 시작합니다. 데스크탑 앱을 실행하고 구성합니다.

1. 앱을 와 연결하려면 [!DNL Experience Manager] 리포지토리에서 앱 아이콘을 클릭하고 앱을 실행합니다. 의 주소를 입력합니다 [!DNL Experience Manager] 서버 형식 `https://[aem_server]:[port]/`.

   클릭 **[!UICONTROL Connect]** 자격 증명을 제공합니다.

   ![데스크탑 앱의 연결 화면과 입력 서버 주소](assets/connect_da2.png)

   *그림: 입력 서버 주소에 대한 연결 화면입니다.*

   선택 **[!UICONTROL Remember Connection]** 데스크탑 앱에 로그온할 때마다 연결 세부 사항을 입력하지 않도록 합니다.

   >[!CAUTION]
   >
   >주소 앞이나 뒤에 선행 또는 후행 공백이 없는지 확인합니다. [!DNL Experience Manager] server. 그렇지 않으면 앱에 연결할 수 없습니다 [!DNL Experience Manager] server.

1. 연결에 성공하면 [!DNL Experience Manager] DAM. 앱 내에서 폴더를 찾을 수 있습니다.

   ![로그인하면 앱에 DAM 콘텐츠가 표시됩니다](assets/firstview_da2.png)

   *그림: 애플리케이션은 로그인 후 DAM 컨텐츠를 표시합니다*

1. ([!DNL Experience Manager] 6.5.1 이상) [!DNL Experience Manager] 6.5.1 이상, S3 또는 Azure 커넥터를 버전 1.10.4 이상으로 업그레이드하십시오. 자세한 내용은 [Azure 커넥터](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/deploying/data-store-config.html#azure-data-store) 또는 [S3 커넥터](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/deploying/data-store-config.html#amazon-s-data-store).

   AMS(Adobe Managed Services) 고객은 Adobe 고객 지원 센터에 문의하십시오.

## 환경 설정 지정 {#set-preferences}

기본 설정을 변경하려면 ![추가 옵션 아이콘](assets/do-not-localize/more_options_da2.png) 및 **[!UICONTROL Preference]** ![환경 설정 아이콘](assets/do-not-localize/preferences_icon_da2.png). 에서 **[!UICONTROL Preferences]** 창에서 다음 값을 조정합니다.

* [!UICONTROL Launch application on login].

* [!UICONTROL Show window when application starts].

* **[!UICONTROL Cache Directory]**: 앱의 로컬 캐시 위치(로컬로 다운로드한 자산이 들어 있음).

* **[!UICONTROL Network Drive Letter]**: 에 매핑하는 데 사용되는 드라이브 문자입니다 [!DNL Experience Manager] DAM. 확실하지 않은 경우 변경하지 마십시오. 이 앱은 Windows의 모든 드라이브 문자를 매핑할 수 있습니다. 두 사용자가 서로 다른 드라이브 문자의 자산을 배치하면 서로 다른 문자로 배치된 자산을 볼 수 없습니다. 자산의 경로가 변경됩니다. 자산은 바이너리 파일(INDD)에 남아 있으며 제거되지 않습니다. 앱에는 사용 가능한 모든 드라이브 문자가 나열되며 기본적으로 일반적으로 사용 가능한 마지막 문자가 사용됩니다 `Z`.

* **[!UICONTROL Maximum Cache Size]**: 로컬로 다운로드된 자산을 저장하는 데 사용되는 GB의 하드 디스크에서 허용되는 캐시.

* **[!UICONTROL Current cache size]**: 로컬로 다운로드한 자산의 저장소 크기입니다. 이 정보는 앱을 사용하여 자산을 다운로드한 후에만 표시됩니다.

* **[!UICONTROL Automatically download linked assets]**: 지원되는 기본 Creative Cloud 앱에 배치된 자산을 원래 파일을 다운로드할 경우 자동으로 가져옵니다.

* **[!UICONTROL Maximum number of downloads]**: ![주의 아이콘](assets/do-not-localize/caution-icon.png) 주의해서 바꾸세요. 자산을 처음 다운로드할 때(표시, 열기, 편집, 다운로드 또는 유사한 옵션을 통해) 배치에 이 수보다 작은 경우에만 자산이 다운로드됩니다. 기본값은 50입니다. 확실하지 않은 경우 변경하지 마십시오. 값을 늘리면 대기 시간이 길어지고 값을 줄이면 필요한 자산이나 폴더를 한 번에 다운로드하지 못할 수 있습니다.

* **[!UICONTROL Use legacy conventions when creating nodes for assets and folders]**: ![주의 아이콘](assets/do-not-localize/caution-icon.png) 주의해서 바꾸세요. 이 설정을 사용하여 폴더를 업로드할 때 앱에서 v1.10 앱 동작을 에뮬레이션할 수 있습니다. v1.10에서 리포지토리에서 생성된 노드 이름은 사용자가 제공하는 폴더 이름의 공백 및 대소문자를 따릅니다. 그러나 앱의 v2.1에서는 폴더 이름에 있는 추가 공백이 대시로 변환됩니다. 예를 들어 업로드 `New Folder` 또는 `new   folder` 옵션이 선택되어 있지 않고 v2.1의 기본 동작이 유지되면 리포지토리에서 동일한 노드를 생성합니다. 이 옵션을 선택하면 위의 두 폴더에 대한 저장소에 다른 노드가 만들어지고 v1.10 앱의 동작과 일치합니다.

   v2.1의 기본 동작은 동일하게 유지됩니다. 즉, 폴더 이름의 여러 공백을 저장소 노드 이름의 대시로 바꾸고 소문자 노드 이름으로 변환합니다.

* **[!UICONTROL Upload Acceleration]**: ![주의 아이콘](assets/do-not-localize/caution-icon.png) 주의해서 바꾸세요. 자산을 업로드할 때 애플리케이션에서 동시 업로드를 사용하여 업로드 속도를 향상시킬 수 있습니다. 슬라이더를 오른쪽으로 이동하여 업로드의 동시성을 늘릴 수 있습니다. 맨 왼쪽에 있는 슬라이더는 동시 실행 없음(단일 스레드 업로드)을 의미하며 중간 위치는 10개의 동시 스레드에 해당하며 맨 오른쪽에 있는 최대 제한은 20개의 동시 스레드에 해당합니다. 더 높은 동시 시청 제한은 리소스를 많이 사용합니다.

사용할 수 없는 기본 설정을 업데이트하려면 [!DNL Experience Manager] server 및 update 기본 설정을 업데이트한 후 ![환경 설정 저장](assets/do-not-localize/save_preferences_da2.png).

![데스크탑 앱 환경 설정 및 설정](assets/preferences_da2.png)

*그림: 데스크탑 앱 환경 설정.*

### 프록시 지원 {#proxy-support}

[!DNL Experience Manager] 데스크탑 앱에서는 시스템의 사전 정의된 프록시를 사용하여 HTTPS를 통해 인터넷에 연결합니다. 추가 인증이 필요하지 않은 네트워크 프록시를 사용해야 앱을 연결할 수 있습니다.

Windows(인터넷 옵션 > LAN 설정)에 대한 프록시 서버 설정을 구성하거나 수정한 경우 [!DNL Experience Manager] 변경 사항을 적용할 데스크탑 앱입니다. 프록시 구성은 데스크탑 앱을 시작할 때 적용됩니다. 앱을 닫은 후 다시 실행하여 변경 사항을 적용합니다.

프록시에 인증이 필요한 경우 IT 팀이 [!DNL Experience Manager Assets] 애플리케이션 트래픽을 전달할 수 있도록 프록시 서버 설정의 URL입니다.

## 앱 제거 {#uninstall-the-app}

Windows에서 응용 프로그램을 제거하려면 다음 단계를 수행합니다.

1. 모든 변경 내용을 [!DNL Experience Manager] 편집 내용이 손실되지 않도록 합니다. 자세한 내용은 [자산 편집 및 업데이트된 자산 업로드 [!DNL Experience Manager]](using.md#edit-assets-upload-updated-assets). 로그오프 및 [!UICONTROL Exit] 앱.

1. 다른 OS 애플리케이션을 제거하려면 앱을 제거합니다. Windows에서 프로그램 추가 및 제거에서 제거합니다.

1. 캐시 및 로그를 제거하려면 필요한 확인란을 선택합니다.

   ![로그 및 캐시를 제거하려면 제거 대화 상자](assets/uninstall_da2.png)

1. 화면의 지시를 따르십시오. 완료되면 시스템을 다시 시작합니다.

Mac에서 애플리케이션을 제거하려면 다음 단계를 수행합니다.

1. 모든 변경 내용을 [!DNL Experience Manager] 편집 내용이 손실되지 않도록 합니다. 자세한 내용은 [자산 편집 및 업데이트된 자산 업로드 [!DNL Experience Manager]](using.md#edit-assets-upload-updated-assets). 로그오프 및 [!UICONTROL Exit] 앱.

1. 제거 `Adobe Experience Manager Desktop.app` 변환 전: `/Applications`.

또는 Mac에서 내부 애플리케이션 캐시를 지우고 앱을 제거하려면 터미널에서 다음 명령을 실행할 수 있습니다.

```shell
/Applications/Adobe Experience Manager Desktop/Contents/Resources/uninstall-osx/uninstall.sh
```
