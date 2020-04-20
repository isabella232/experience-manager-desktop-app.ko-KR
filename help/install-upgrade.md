---
title: Adobe Experience Manager 데스크탑 앱 설치 및 구성
description: Adobe Experience Manager Assets 서버와 연동되고 로컬 파일 시스템에서 에셋을 다운로드할 수 있도록 Adobe Experience Manager 데스크탑 앱을 설치하고 구성합니다.
uuid: 79bc9de9-5708-41f9-ac43-68c1fd2a2129
contentOwner: AG
products: SG_EXPERIENCEMANAGER/6.3/ASSETS
discoiquuid: f6365302-1690-4719-9b8c-035719422740
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 0301538b5cc00a187709b484bed8f0ca7b799f03

---


# Install Adobe Experience Manager desktop app {#install-app-v2}

Adobe Experience Manager 데스크탑 앱을 사용하면 Experience Manager의 에셋을 로컬 데스크탑에서 손쉽게 이용할 수 있으며 모든 기본 데스크탑 애플리케이션에서 사용할 수 있습니다. 에셋을 미리 보거나 기본 데스크탑 애플리케이션에서 열 수 있으며, Mac Finder 또는 Windows 탐색기에서 다른 문서에 삽입할 수 있고, 로컬에서 변경할 수 있습니다. 이렇게 하면 업로드 시 변경 사항이 Experience Manager에 다시 저장되고 저장소에 새 버전이 생성됩니다.

이러한 통합을 통해 조직의 다양한 역할이

* Adobe Experience Manager Assets에서 중앙에서 자산 관리
* 타사 애플리케이션 및 Adobe Creative Cloud를 비롯한 모든 기본 데스크탑 애플리케이션에서 에셋을 이용할 수 있습니다. 이렇게 하면 브랜딩을 비롯한 다양한 표준을 손쉽게 준수할 수 있습니다.

Experience Manager 데스크탑 앱을 사용하려면

* Experience Manager 데스크톱 앱이 Experience Manager 버전을 지원하는지 확인하십시오. 아래 [시스템 요구 사항을](release-notes.md#system-requirements-and-prerequisites-v2) 참조하십시오.
* 애플리케이션을 다운로드하여 설치합니다. 아래 데스크탑 앱 [](#install-v2) 설치를 참조하십시오.
* 몇 개의 자산을 사용하여 연결을 테스트합니다. 자산을 [검색하고 찾아보는](using.md#browse-search-preview-assets)방법을 참조하십시오.

## 시스템 요구 사항, 사전 요구 사항 및 다운로드 링크 {#tech-specs-v2}

자세한 내용은 Experience Manager [데스크탑 앱 릴리스 노트를](release-notes.md)참조하십시오.

## Upgrade from a previous version {#upgrade-from-previous-version}

데스크탑 앱의 v1.x 사용자는 이전 버전과 최신 버전의 차이점과 유사점을 파악합니다. 데스크탑 앱의 [새로운 기능](introduction.md#whats-new-v2) 및 앱 [작동 방식 보기](release-notes.md#how-app-works)

>[!NOTE]
>
>한 컴퓨터에 두 버전의 데스크탑 앱을 함께 사용할 수 없습니다. 버전을 설치하기 전에 다른 버전을 제거합니다.

이전 버전의 앱에서 업그레이드하려면 다음 지침을 따르십시오.

1. 업그레이드하기 전에 모든 자산을 동기화하고 변경 내용을 Experience Manager에 업로드하십시오. 이는 앱을 제거할 때 편집된 내용이 손실되지 않도록 하기 위한 것입니다.
1. 이전 버전의 앱을 제거합니다. 제거할 때 캐시 지우기 옵션을 선택합니다.
1. 시스템을 다시 시작합니다.
1. [최신 앱을 다운로드하여](release-notes.md) [설치합니다](#install-v2) . 아래 지침을 따르십시오.

##  설치 {#install-v2}

데스크탑 앱을 설치하려면 다음 단계를 따르십시오. 최신 앱을 설치하기 전에 기존 Adobe Experience Manager 데스크탑 앱 v1.x를 제거합니다. 자세한 내용은 상기를 참조하십시오.

1. 릴리스 [정보](release-notes.md) 페이지에서 최신 설치 프로그램을 다운로드합니다.
1. Adobe Experience Manager 배포의 URL과 자격 증명을 간편하게 이용하세요.
1. 다른 버전의 앱에서 업그레이드하는 경우 데스크탑 앱 [](#upgrade-from-previous-version)업그레이드를 참조하십시오.
1. Experience Manager를 클라우드 서비스, Experience Manager 6.4.4 이상 또는 Experience Manager 6.5.0 이상으로 사용하는 경우 이 단계를 건너뛸 수 있습니다. Experience Manager 설정이 [릴리스 노트에](release-notes.md)언급된 호환성 요구 사항을 충족하는지 확인하십시오. 필요한 경우 해당 [호환성 패키지를](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq640/featurepack/adobe-asset-link-support) 다운로드하고 Experience Manager 패키지 관리자를 Experience Manager 관리자로 사용하여 설치합니다. 패키지를 설치하려면 패키지 [작업 방법을 참조하십시오](https://helpx.adobe.com/experience-manager/6-5/sites/administering/using/package-manager.html).
1. 설치 프로그램 바이너리를 실행하고 화면에 표시되는 지침에 따라 설치합니다.
1. Windows의 경우 설치 프로그램이 설치하라는 메시지가 표시될 수 `Visual Studio C++ Redistributable 2015`있습니다. 화면의 지침에 따라 설치합니다. 설치에 실패하면 수동으로 설치합니다. [여기에서](https://www.microsoft.com/en-us/download/details.aspx?id=52685) 설치 프로그램을 다운로드하고 `vc_redist.x64.exe` `vc_redist.x86.exe` 파일과 파일을 모두 설치합니다. AEM 데스크톱 앱 설치 관리자를 다시 실행합니다.
1. 메시지가 표시되면 컴퓨터를 다시 시작합니다. 데스크탑 앱을 실행하고 구성합니다.
1. 앱을 AEM 저장소에 연결하려면 트레이에서 앱 아이콘을 클릭하여 앱을 실행합니다. AEM 인스턴스의 주소를 제공합니다. 을 클릭하고 자격 증명을 **[!UICONTROL Connect]** 제공합니다.

   ![데스크탑 앱의 연결 화면입력 서버](assets/connect_da2.png "주소에 대한 연결 화면")

   >[!C채움]
   >
   >AEM 서버의 주소 앞 또는 뒤에 선행 또는 후행 공백이 없는지 확인합니다. 그렇지 않으면 앱이 AEM 서버에 연결할 수 없습니다.

1. 연결이 성공하면 AEM DAM의 루트 폴더에서 사용할 수 있는 폴더 및 자산 목록을 볼 수 있습니다. 앱 내에서 폴더를 검색할 수 있습니다.

   ![로그인하면 앱에 DAM](assets/firstview_da2.png "콘텐츠가 표시됩니다 로그인하면 앱에 DAM 콘텐츠가 표시됩니다")

1. (Experience Manager 6.5.1 이상) Experience Manager 6.5.1 이상 버전의 데스크탑 앱을 사용하는 경우 S3 또는 Azure 커넥터를 버전 1.10.4 이상으로 업그레이드하십시오. Azure [커넥터](https://helpx.adobe.com/experience-manager/6-5/sites/deploying/using/data-store-config.html#AzureDataStore) 또는 [S3 커넥터를](https://helpx.adobe.com/experience-manager/6-5/sites/deploying/using/data-store-config.html#AmazonS3DataStore)참조하십시오.

   AMS(Adobe Managed Services) 고객은 Adobe 고객 지원 센터에 문의하십시오.

## 환경 설정 {#set-preferences}

환경 설정을 변경하려면 추가 옵션 ![아이콘](assets/do-not-localize/more_options_da2.png) 및 **[!UICONTROL Preference]** 환경 설정 아이콘을 ![클릭합니다](assets/do-not-localize/preferences_icon_da2.png). 창에서 **[!UICONTROL Preferences]** 다음 값을 조정합니다.

* [!UICONTROL Launch application on login].
* [!UICONTROL Show window when application starts].
* **[!UICONTROL Cache Directory]**:앱의 로컬 캐시 위치(로컬에서 다운로드한 에셋이 포함).
* **[!UICONTROL Network Drive Letter]**:AEM DAM에 매핑하는 데 사용되는 드라이브 문자입니다. 확실하지 않으면 변경하지 마십시오. 이 앱은 Windows의 모든 드라이브 문자로 매핑할 수 있습니다. 두 사용자가 서로 다른 드라이브 글자의 에셋을 배치하면 서로 배치된 에셋이 표시되지 않습니다. 자산의 경로가 변경됩니다. 자산은 바이너리 파일(예: INDD)에 그대로 유지되며 제거되지 않습니다. 앱은 사용 가능한 모든 드라이브 문자를 나열하고 기본적으로 일반적으로 사용 가능한 마지막 문자를 사용합니다 `Z`.
* **[!UICONTROL Maximum Cache Size]**:로컬로 다운로드된 에셋을 저장하는 데 사용되는 하드 디스크의 캐시(GB)가 허용됩니다.
* **[!UICONTROL Current cache size]**:로컬에서 다운로드한 자산의 저장소 크기입니다. 이 정보는 앱을 사용하여 자산을 다운로드한 후에만 표시됩니다.
* **[!UICONTROL Automatically download linked assets]**:지원되는 기본 Creative Cloud 앱에 배치된 에셋은 원본 파일을 다운로드하는 경우 자동으로 반입됩니다.
* **[!UICONTROL Maximum number of downloads]**:자산을 처음 다운로드할 때(표시, 열기, 편집, 다운로드 또는 유사한 옵션을 통해) 일괄 처리에 이 수보다 작은 금액이 들어 있는 경우에만 자산이 다운로드됩니다. 기본값은 50입니다. 확실하지 않은 경우 변경하지 마십시오. 값을 늘리면 대기 시간이 길어지고 값을 줄이면 필요한 자산이나 폴더를 한 번에 다운로드할 수 없습니다.
* **[!UICONTROL Upload Acceleration]**:자산을 업로드할 때 애플리케이션에서 동시 업로드를 사용하여 업로드 속도를 향상시킬 수 있습니다. 슬라이더를 오른쪽으로 이동하여 업로드의 동시 사용을 늘릴 수 있습니다. 맨 왼쪽의 슬라이더는 동시 실행 없음(단일 스레드 업로드)을 의미하고, 중간 위치는 동시 스레드 10개에 해당하며, 맨 오른쪽의 최대 제한은 동시 스레드 20개에 해당합니다. 동시 시청 제한이 높을수록 로컬 컴퓨터의 프로세서 리소스가 더 많이 소모됩니다.

사용할 수 없는 기본 설정을 업데이트하려면 AEM 서버에서 로그아웃하십시오. 환경 설정을 업데이트한 후 환경 ![설정](assets/do-not-localize/save_preferences_da2.png) 저장을 클릭하여 변경 사항을 저장합니다.

![AEM 데스크탑 앱 환경 설정 및](assets/preferences_da2.png "설정데스크탑 앱 환경 설정")

## 앱 제거 {#uninstall-the-app}

Windows에서 응용 프로그램을 제거하려면 다음 단계를 수행합니다.

1. 모든 변경 내용을 AEM에 업로드하여 편집 내용이 손실되지 않도록 합니다. 자산 [편집 및 업데이트된 자산 업로드를 참조하십시오](using.md#edit-assets-upload-updated-assets). 로그오프와 [!UICONTROL Exit] 앱
1. 다른 모든 OS 애플리케이션을 제거할 때 앱을 제거합니다. Windows의 프로그램 추가 및 제거에서 제거합니다.
1. 캐시와 로그를 제거하려면 필요한 확인란을 선택합니다.
   ![제거 대화 상자를 사용하여 로그 및](assets/uninstall_da2.png "캐시 제거로그 및 캐시를 제거하는 제거 대화 상자")
1. 화면에 표시되는 지침을 따릅니다. 완료되면 시스템을 다시 시작합니다.

Mac에서 애플리케이션을 제거하려면 다음 단계를 따르십시오.

1. 모든 변경 내용을 AEM에 업로드하여 편집 내용이 손실되지 않도록 합니다. 자산 [편집 및 업데이트된 자산 업로드를 참조하십시오](using.md#edit-assets-upload-updated-assets). 로그오프와 [!UICONTROL Exit] 앱
1. 에서 을 `Adobe Experience Manager Desktop.app` 제거합니다 `/Applications`.

또는 Mac에서 내부 애플리케이션 캐시를 정리하고 앱을 제거하려면 터미널에서 다음 명령을 실행할 수 있습니다.
`/Applications/Adobe Experience Manager Desktop/Contents/Resources/uninstall-osx/uninstall.sh`
