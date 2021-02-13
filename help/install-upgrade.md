---
title: 데스크탑 앱 설치 및 구성
description: '서버를 설치 및 구성하고 로컬 파일 시스템에 자산을 다운로드합니다. [!DNL Adobe Experience Manager] desktop app to work with [!DNL Adobe Experience Manager Assets] '
translation-type: tm+mt
source-git-commit: cc4ce762ad1d7f4c5a54ab6bac9d1a872e3d18c9
workflow-type: tm+mt
source-wordcount: '1162'
ht-degree: 1%

---


# [!DNL Adobe Experience Manager] 데스크탑 앱 {#install-app-v2} 설치

[!DNL Adobe Experience Manager] 데스크탑 앱을 사용하면 [!DNL Experience Manager] 내의 에셋을 로컬 데스크탑에서 쉽게 사용할 수 있으며 모든 기본 데스크탑 애플리케이션에서 사용할 수 있습니다. 에셋은 미리 보거나 기본 데스크톱 응용 프로그램에서 열 수 있으며 다른 문서에 배치하기 위해 Mac Finder 또는 Windows 탐색기에 표시되며 로컬에서 변경할 수 있습니다. 업로드하면 변경 내용이 다시 [!DNL Experience Manager]에 저장되고 저장소에 새 버전이 만들어집니다.

이러한 통합을 통해 조직의 다양한 역할이

* [!DNL Experience Manager Assets]에서 중앙에서 자산을 관리합니다.

* 제3자 응용 프로그램 및 Adobe Creative Cloud을 비롯한 모든 기본 데스크탑 응용 프로그램의 에셋에 액세스합니다. 이렇게 하면 브랜딩을 비롯한 다양한 표준을 쉽게 준수할 수 있습니다.

[!DNL Experience Manager] 데스크탑 앱을 사용하려면

* [!DNL Experience Manager] 버전이 [!DNL Experience Manager] 데스크탑 앱에서 지원되는지 확인하십시오. 아래의 [시스템 요구 사항](release-notes.md#system-requirements-and-prerequisites-v2)을 참조하십시오.

* 애플리케이션을 다운로드하여 설치합니다. 아래의 [데스크탑 앱 설치](#install-v2)를 참조하십시오.

* 몇 개의 에셋을 사용하여 연결을 테스트합니다. [자산 검색 및 검색 방법](using.md#browse-search-preview-assets)을 참조하십시오.

## 시스템 요구 사항, 사전 요구 사항 및 다운로드 링크 {#tech-specs-v2}

자세한 내용은 [[!DNL Experience Manager] 데스크탑 앱 릴리스 노트](release-notes.md)를 참조하십시오.

## 이전 버전 {#upgrade-from-previous-version}에서 업그레이드

데스크탑 앱의 v1.x 사용자는 이전 버전과 최신 버전의 앱 간의 차이점과 유사점을 파악합니다. 데스크톱 앱](introduction.md#whats-new-v2) 및 [앱의 작동 방식](release-notes.md#how-app-works)을 참조하십시오.[

>[!NOTE]
>
>한 컴퓨터에 두 버전의 데스크탑 앱을 함께 사용할 수 없습니다. 버전을 설치하기 전에 다른 버전을 제거합니다.

이전 버전의 앱에서 업그레이드하려면 다음 지침을 따르십시오.

1. 업그레이드하기 전에 모든 자산을 동기화하고 변경 내용을 [!DNL Experience Manager]에 업로드합니다. 이는 앱을 제거할 때 편집된 내용이 손실되지 않도록 하기 위한 것입니다.

1. 이전 버전의 앱을 제거합니다. 제거할 때 캐시를 지우려면 옵션을 선택합니다.

1. 컴퓨터를 다시 시작합니다.

1. [](release-notes.md) 최신 앱 [](#install-v2) 을 다운로드하여 설치합니다. 아래 지침을 따르십시오.

##  설치 {#install-v2}

데스크탑 앱을 설치하려면 다음 단계를 따르십시오. 최신 앱을 설치하기 전에 기존 Adobe [!DNL Experience Manager] 데스크탑 앱 v1.x를 제거합니다. 자세한 내용은 상기를 참조하십시오.

1. [릴리스 노트](release-notes.md) 페이지에서 최신 설치 프로그램을 다운로드합니다.

1. [!DNL Experience Manager] 배포의 URL 및 자격 증명을 바로 사용할 수 있도록 보관하십시오.

1. 다른 버전의 앱에서 업그레이드하는 경우 [데스크탑 앱 업그레이드](#upgrade-from-previous-version)를 참조하십시오.

1. [!DNL Experience Manager]을(를) [!DNL Cloud Service], [!DNL Experience Manager] 6.4.4 이상 또는 [!DNL Experience Manager] 6.5.0 이상으로 사용하는 경우 이 단계를 건너뜁니다. [!DNL Experience Manager] 설정이 [릴리스 노트](release-notes.md)에 명시된 호환성 요구 사항을 충족하는지 확인합니다. 필요한 경우 해당 [호환성 패키지](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq640/featurepack/adobe-asset-link-support)을 다운로드하고 [!DNL Experience Manager] 패키지 관리자를 [!DNL Experience Manager] 관리자로 사용하여 설치합니다. 패키지를 설치하려면 [패키지 사용 방법](https://experienceleague.adobe.com/docs/experience-manager-65/administering/contentmanagement/package-manager.html)을 참조하십시오.

1. 설치 프로그램 바이너리를 실행하고 화면의 지침에 따라 설치합니다.

1. Windows의 경우 설치 관리자가 `Visual Studio C++ Redistributable 2015`을(를) 설치하라는 메시지를 표시할 수 있습니다. 화면의 지침에 따라 설치합니다. 설치에 실패하면 수동으로 설치합니다. [여기](https://www.microsoft.com/en-us/download/details.aspx?id=52685)에서 설치 프로그램을 다운로드하고 `vc_redist.x64.exe` 파일과 `vc_redist.x86.exe` 파일을 모두 설치합니다. [!DNL Experience Manager] 데스크탑 앱 설치 관리자를 다시 실행합니다.

1. 메시지가 표시되면 컴퓨터를 다시 시작합니다. 데스크탑 앱을 실행하고 구성합니다.

1. 앱을 [!DNL Experience Manager] 리포지토리와 연결하려면 트레이에서 앱 아이콘을 클릭하고 앱을 실행합니다. [!DNL Experience Manager] 서버 주소를 `https://[aem_server]:[port]/` 형식으로 제공합니다.

   **[!UICONTROL Connect]**&#x200B;을 클릭하고 자격 증명을 제공합니다.

   ![데스크탑 앱의 연결 화면을 입력 서버 주소에 연결](assets/connect_da2.png)

   *그림:입력 서버 주소에 대한 연결 화면입니다.*

   >[!CAUTION]
   >
   >[!DNL Experience Manager] 서버 주소 앞이나 뒤에 선행 또는 후행 공백이 없는지 확인합니다. 그렇지 않으면 앱이 [!DNL Experience Manager] 서버에 연결할 수 없습니다.

1. 성공적으로 연결되면 [!DNL Experience Manager] DAM의 루트 폴더에서 사용할 수 있는 폴더 및 자산 목록을 볼 수 있습니다. 앱 내에서 폴더를 찾아볼 수 있습니다.

   ![로그인하면 앱이 DAM 콘텐츠를 표시합니다.](assets/firstview_da2.png)

   *그림:응용 프로그램에 로그인 후 DAM 내용이 표시됩니다.*

1. ([!DNL Experience Manager] 6.5.1 이상) [!DNL Experience Manager] 6.5.1 이상 버전의 데스크탑 앱을 사용하는 경우 S3 또는 Azure 커넥터를 버전 1.10.4 이상으로 업그레이드하십시오. [Azure 커넥터](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/deploying/data-store-config.html#azure-data-store) 또는 [S3 커넥터](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/deploying/data-store-config.html#amazon-s-data-store)을 참조하십시오.

   AMS(Adobe Managed Services) 고객의 경우 Adobe 고객 지원 센터에 문의하십시오.

## 환경 설정 {#set-preferences} 설정

환경 설정을 변경하려면 ![추가 옵션 아이콘](assets/do-not-localize/more_options_da2.png) 및 **[!UICONTROL Preference]** ![환경 설정 아이콘](assets/do-not-localize/preferences_icon_da2.png)을 클릭합니다. **[!UICONTROL Preferences]** 창에서 다음 값을 조정합니다.

* [!UICONTROL Launch application on login].

* [!UICONTROL Show window when application starts].

* **[!UICONTROL Cache Directory]**:앱의 로컬 캐시 위치(로컬로 다운로드한 에셋이 포함되어 있음).

* **[!UICONTROL Network Drive Letter]**:DAM에 매핑하는 데 사용되는 드라이브  [!DNL Experience Manager] 문자입니다. 확실하지 않으면 변경하지 마십시오. 이 앱은 Windows의 모든 드라이브 문자로 매핑할 수 있습니다. 두 사용자가 서로 다른 드라이브 글자에서 에셋을 배치하면 서로 배치된 에셋이 표시되지 않습니다. 자산의 경로가 변경됩니다. 자산은 바이너리 파일(INDD)에 그대로 유지되며 제거되지 않습니다. 앱은 사용 가능한 모든 드라이브 문자를 나열하고 기본적으로 마지막으로 사용 가능한 문자(일반적으로 `Z`)를 사용합니다.

* **[!UICONTROL Maximum Cache Size]**:로컬에서 다운로드한 에셋을 저장하는 데 사용되는 하드 디스크의 캐시(GB)가 허용됩니다.

* **[!UICONTROL Current cache size]**:로컬로 다운로드한 자산의 저장소 크기입니다. 이 정보는 자산을 앱을 사용하여 다운로드한 후에만 표시됩니다.

* **[!UICONTROL Automatically download linked assets]**:지원되는 기본 Creative Cloud 앱에 있는 에셋은 원본 파일을 다운로드한 경우 자동으로 가져옵니다.

* **[!UICONTROL Maximum number of downloads]**:자산을 처음 다운로드할 때(표시, 열기, 편집, 다운로드 또는 유사한 옵션을 통해), 일괄 처리에서 이 수보다 작은 경우에만 자산이 다운로드됩니다. 기본값은 50입니다. 확실하지 않은 경우 변경하지 마십시오. 값을 늘리면 대기 시간이 길어지고 값을 줄이면 필요한 자산이나 폴더를 한 번에 다운로드할 수 없습니다.

* **[!UICONTROL Upload Acceleration]**:자산을 업로드할 때 애플리케이션에서 동시 업로드를 사용하여 업로드 속도를 향상시킬 수 있습니다. 슬라이더를 오른쪽으로 이동하여 업로드의 동시 사용을 늘릴 수 있습니다. 맨 왼쪽에 있는 슬라이더는 동시 실행 없음(단일 스레드 업로드)을 의미하고, 중간 위치는 동시 스레드 10개에 해당하며, 맨 오른쪽에 있는 최대 제한은 20개의 동시 스레드에 해당합니다. 동시 시청 제한이 클수록 로컬 컴퓨터의 프로세서가 더 많은 리소스를 사용해야 합니다.

사용할 수 없는 환경 설정을 업데이트하려면 [!DNL Experience Manager] 서버에서 로그아웃하십시오. 환경 설정을 업데이트한 후 ![환경 설정 저장](assets/do-not-localize/save_preferences_da2.png)을 클릭하여 변경 내용을 저장합니다.

![데스크탑 앱 환경 설정 및 설정](assets/preferences_da2.png)

*그림:데스크탑 앱 환경 설정.*

## 앱 {#uninstall-the-app} 제거

Windows에서 응용 프로그램을 제거하려면 다음 단계를 수행합니다.

1. 모든 변경 내용을 [!DNL Experience Manager]에 업로드하여 편집 내용이 손실되지 않도록 합니다. [자산 편집 및 업데이트된 자산을  [!DNL Experience Manager]](using.md#edit-assets-upload-updated-assets)에 업로드를 참조하십시오. 로그오프하고 [!UICONTROL Exit] 앱을 실행합니다.

1. 다른 OS 응용 프로그램을 제거할 때 앱을 제거합니다. Windows의 프로그램 추가 및 제거에서 제거합니다.

1. 캐시와 로그를 제거하려면 필요한 확인란을 선택합니다.

   ![로그 및 캐시를 제거하기 위한 제거 대화 상자](assets/uninstall_da2.png)

1. 화면의 지침을 따릅니다. 완료되면 컴퓨터를 다시 시작합니다.

Mac에서 응용 프로그램을 제거하려면 다음 단계를 수행합니다.

1. 모든 변경 내용을 [!DNL Experience Manager]에 업로드하여 편집 내용이 손실되지 않도록 합니다. [자산 편집 및 업데이트된 자산을  [!DNL Experience Manager]](using.md#edit-assets-upload-updated-assets)에 업로드를 참조하십시오. 로그오프하고 [!UICONTROL Exit] 앱을 실행합니다.

1. `/Applications`에서 `Adobe Experience Manager Desktop.app`을(를) 제거합니다.

또는 Mac에서 내부 응용 프로그램 캐시를 정리하고 앱을 제거하려면 터미널에서 다음 명령을 실행할 수 있습니다.

```shell
/Applications/Adobe Experience Manager Desktop/Contents/Resources/uninstall-osx/uninstall.sh
```
