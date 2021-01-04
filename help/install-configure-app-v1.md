---
title: ' [!DNL Experience Manager] 데스크탑 앱 버전 1.x 설치 및 구성'
description: ' [!DNL Experience Manager] desktop app version 1.x to work with [!DNL Assets] 서버를 설치 및 구성하고 자산을 데스크탑에 드라이브로 마운트할 수 있도록 매핑합니다.'
translation-type: tm+mt
source-git-commit: a25c1fa13895ae9eb7268e3e01c83a5f0b9d7d1d
workflow-type: tm+mt
source-wordcount: '903'
ht-degree: 0%

---


# [!DNL Experience Manager] 데스크탑 앱 v1.x {#install-and-configure-aem-desktop-app} 설치 및 구성

[!DNL Experience Manager] 데스크탑 앱을 사용하면 [!DNL Experience Manager] 내의 에셋은 로컬 데스크탑에서 쉽게 액세스할 수 있으며 모든 데스크탑 애플리케이션에서 사용할 수 있습니다. 자산은 Mac Finder 또는 Windows 탐색기에서 쉽게 표시되며, 데스크톱 응용 프로그램에서 열렸으며 로컬로 변경될 수 있습니다. 업로드하고 저장소에 새 버전이 만들어질 때 변경 내용이 다시 [!DNL Experience Manager]에 저장됩니다.

이러한 통합을 통해 조직의 다양한 역할이 중앙에서 에셋을 관리하고 Creative Cloud 및 기타 애플리케이션에서 에셋을 액세스할 수 있으며 브랜딩을 비롯한 다양한 표준을 쉽게 준수할 수 있습니다.

[!DNL Experience Manager] 데스크탑 앱을 사용하려면

* [!DNL Experience Manager] 서버 버전이 [!DNL Experience Manager] 데스크탑 앱에서 지원되는지 확인하십시오. [호환성 매트릭스](release-notes-of-v1.md#compatibilitymatrix)를 참조하십시오.

* 애플리케이션을 다운로드하여 설치합니다.

* 몇 개의 에셋을 사용하여 연결을 테스트합니다. 자세한 내용은 [데스크톱에서 자산 액세스 및 열기](use-app-v1.md#openondesktop)를 참조하십시오.

## 시스템 요구 사항, 사전 요구 사항 및 다운로드 링크 {#system-requirements-prerequisites-and-download-links}

자세한 내용은 [[!DNL Experience Manager] 데스크탑 앱 릴리스 노트](release-notes-of-v1.md)를 참조하십시오.

## 앱을 설치하고 [!DNL Experience Manager] 서버 {#install-and-connect-aem-desktop-app-to-aem-server}에 연결

자세한 내용은 [설치 및 연결 [!DNL Experience Manager] desktop app to [!DNL Experience Manager] server](use-app-v1.md#installandconnect)을 참조하십시오.

>[!NOTE]
>
>한 번에 하나의 [!DNL Experience Manager] 데스크탑 앱 인스턴스만 설치하고 활성화할 수 있습니다.

## 파일 처리 {#file-handling}

데스크탑 앱으로 마운트된 네트워크 공유 위치에서 파일을 변경하면 파일이 두 단계로 해당 위치에 저장됩니다. 첫 번째 단계에서는 파일이 로컬에 저장됩니다. 사용자는 전송이 완료될 때까지 기다리지 않고 파일을 저장하고 파일을 계속 작업할 수 있습니다.

두 번째 단계에서는 데스크톱 앱이 사전 정의된 지연(예: 30초) 후에 업데이트된 파일을 [!DNL Experience Manager] 서버에 업로드합니다. 이 작업은 백그라운드에서 수행됩니다. 업로드 작업의 상태를 보려면 자산 상태 보기 옵션을 사용합니다.

1. 자산을 자산에 업로드합니다.

1. 도구 모음에서 [!DNL Experience Manager] 데스크탑 앱 아이콘을 클릭합니다.

1. 메뉴에서 자산 상태 보기 옵션을 선택합니다.

1. 대화 상자에서 업로드 작업의 상태를 검토합니다.

>[!NOTE]
>
>[!DNL Experience Manager] 데스크탑 앱은 최대 40GB의 에셋을 처리할 수 있습니다.

## 디스패처 {#connect-to-an-aem-instance-behind-a-dispatcher} 뒤에 있는 [!DNL Experience Manager] 인스턴스에 연결

자산 API의 복사 및 이동 메서드를 사용하려면 다음 추가 헤더를 [!DNL Experience Manager]에 전달해야 합니다.

* X-대상
* X-깊이
* X-덮어쓰기

[!DNL Experience Manager] 바탕 화면 [!DNL Experience Manager] 은 기본 포트를 포함하는 URL 사용에 연결합니다. 따라서 디스패처 구성의 `virtualhosts` 설정에는 기본 포트 번호가 포함되어야 합니다. `virtualhosts` 구성에 대한 자세한 내용은 [가상 호스트 식별](https://experienceleague.adobe.com/docs/experience-manager-dispatcher/using/configuring/dispatcher-configuration.html#identifying-virtual-hosts-virtualhosts)을 참조하십시오.

이러한 추가 헤더를 통과하도록 디스패처를 구성하는 방법에 대한 자세한 내용은 [HTTP 헤더](https://experienceleague.adobe.com/docs/experience-manager-dispatcher/using/configuring/dispatcher-configuration.html#specifying-the-http-headers-to-pass-through-clientheaders) 지정을 참조하십시오.

### 프록시 지원 {#proxy-support}

[!DNL Experience Manager] 데스크탑 앱은 시스템의 사전 정의된 프록시를 사용하여 HTTPS를 통해 인터넷에 연결합니다. 앱은 추가 인증이 필요하지 않은 네트워크 프록시를 사용해야만 연결할 수 있습니다.

Windows(인터넷 옵션 > LAN 설정)에 대한 프록시 서버 설정을 구성하거나 수정하는 경우 변경 사항을 적용하려면 [!DNL Experience Manager] 데스크탑 앱을 다시 시작하십시오.

>[!NOTE]
>
>프록시 구성은 데스크톱 앱을 시작할 때만 적용됩니다. 변경 사항이 적용되려면 앱을 닫고 다시 실행하십시오.

프록시에 인증이 필요한 경우 IT 팀이 프록시 서버 설정의 Experience Manager 자산 URL을 허용하여 응용 프로그램 트래픽을 전달할 수 있습니다.

## 자산 정보 대화 상자 사용자 지정 {#customize-the-asset-info-dialog}

다음 구성 요소 중 하나 또는 둘 다를 오버레이하여 [자산 정보] 대화 상자를 사용자 지정할 수 있습니다.

* `/libs/dam/gui/content/assets/moreinfo`의 Granite 사용자 인터페이스 페이지입니다.

* `/libs/dam/gui/components/admin/moreinfo`의 HTL `/css/javascript` 구성 요소입니다.

어떤 구성 요소가 오버레이되어 있는지 여부는 사용자 정의 특성에 따라 다릅니다. [자산 정보] 대화 상자의 일부로 표시되는 구성 요소를 변경하려면 [Granite 사용자 인터페이스] 페이지를 오버레이합니다. 대화 상자의 HTML, CSS 또는 JavaScript 내용을 변경하려면 HTL 구성 요소를 오버레이하십시오.

## 캐시 관리 {#manage-cache}

Windows의 경우 캐시는 `%LOCALAPPDATA%\Adobe\AssetsCompanion\Cache\`에 있으며, 여기서 은 데스크톱 앱에 구성된 [!DNL Experience Manager] 호스트의 인코딩 버전입니다. 예를 들어 `http://localhost:4502`은(는) `http%3A%2F%2Flocalhost%3A4502%2F`로 나타납니다.

Mac OS X에서 유사한 디렉토리는 `~/Library/Group Containers/group.com.adobe.aem.desktop/cache`입니다.

### 캐시 {#in-app-option-to-manage-cache} 관리 인앱 옵션

로컬 캐싱을 위해 사용할 수 있는 디스크 공간의 양을 제어할 수 있습니다. Assets 서버의 아티팩트가 보다 매끄러운 경험을 위해 로컬로 캐시됩니다. 요구 사항에 맞게 기본값을 변경할 수 있습니다. 또한 캐시를 지우면 모든 에셋을 새로 가져올 수 있습니다. 원하는 옵션을 설정하려면 응용 프로그램의 아이콘을 클릭하고 **[!UICONTROL Advanced]** > **[!UICONTROL Manage Cache]**&#x200B;을 클릭합니다. ****

>[!NOTE]
>
>캐시를 지우면 저장하지 않은 변경 사항이 유지됩니다. [!DNL Experience Manager] 서버에 체크 인되지 않은 모든 자산은 유지되며 삭제되지 않습니다.

### Windows {#change-location-of-cache-on-windows}에서 캐시 위치 변경

[!DNL Experience Manager] 데스크톱 앱에 대한 캐시의 기본 위치는 다음과 같습니다.

* Windows에서 `%LocalAppData%\Adobe\AssetsCompanion\Cache\EncodedAEMEndpoint`.

* Mac에서 `~/Library/Group/Containers/group.com.adobe.aem.desktop/cache/EncodedAEMEndpoint`.

`EncodedAEMEndpoint` 은 앱의 구성된  [!DNL Experience Manager] 끝점 URL입니다. 값은 [!DNL Experience Manager] 서버의 타깃팅 URL의 인코딩된 버전입니다. 예를 들어 응용 프로그램이 `http://localhost:4502`을(를) 대상으로 하는 경우 디렉토리 이름은 `http%3A%2F%2Flocalhost%3A4502`입니다. 이 예제의 캐시 디렉토리에 대한 Windows 경로는 `%LocalAppData%\Adobe\AssetsCompanion\Cache\http%3A%2F%2Flocalhost%3A4502`입니다.

응용 프로그램이 다른 폴더 또는 다른 드라이브를 가리키도록 지정하려면 응용 프로그램의 구성 파일을 편집합니다.

1. 앱의 설치 디렉터리로 이동합니다. Windows의 기본 위치는 `C:\Program Files (x86)\Adobe\Adobe Experience Manager Desktop`입니다.

1. 텍스트 편집기를 사용하여 Adobe Experience Manager Desktop.exe.config 파일을 편집합니다.

   이 파일에 대한 변경 내용을 저장하려면 관리자 권한이 필요합니다.

1. &quot;ProxyCacheRoot&quot; 문자열을 검색합니다. 값이 캐시 위치 `%LocalAppData%\Adobe\AssetsCompanion\Cache`으로 설정되어 있는 것을 확인할 수 있습니다. 이 값을 유효한 경로로 변경하십시오.

   >[!NOTE]
   >
   >앱은 *&lt;인코딩된 AEM 끝점>* 하위 디렉토리를 자동으로 만듭니다. 이 동작은 구성할 수 없습니다.

>[!MORELIKETHIS]
* [데스크탑  [!DNL Experience Manager] 앱](https://experienceleague.adobe.com/docs/experience-manager-learn/assets/creative-workflows/aem-desktop-app.html) 소개
* [데스크탑  [!DNL Experience Manager] 앱을](use-app-v1.md) 사용합니다.
* [데스크탑  [!DNL Experience Manager] 앱](troubleshoot-app-v1.md) 문제 해결

