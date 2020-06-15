---
title: AEM 데스크톱 앱 버전 1.x 설치 및 구성
description: AEM Assets 서버와 연동되도록 AEM 데스크톱 앱 버전 1.x를 설치 및 구성하고 자산을 데스크탑에 드라이브로 매핑합니다.
uuid: 79bc9de9-5708-41f9-ac43-68c1fd2a2129
contentOwner: AG
products: SG_EXPERIENCEMANAGER/6.3/ASSETS
discoiquuid: f6365302-1690-4719-9b8c-035719422740
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 0049a67503e476ac03f039942c3849509a085c5b
workflow-type: tm+mt
source-wordcount: '992'
ht-degree: 1%

---


# AEM 데스크톱 앱 v1.x 설치 및 구성 {#install-and-configure-aem-desktop-app}

AEM 데스크톱 앱을 사용하면 AEM 내의 에셋은 로컬 데스크탑에서 쉽게 액세스할 수 있으며 모든 데스크탑 애플리케이션에서 사용할 수 있습니다. 자산은 Mac Finder 또는 Windows 탐색기에서 쉽게 표시되며, 데스크톱 응용 프로그램에서 열리고 로컬에서 변경될 수 있습니다. 업로드하면 변경 사항이 AEM에 다시 저장되고 저장소에 새 버전이 만들어집니다.

이러한 통합을 통해 조직의 다양한 역할이 AEM Assets에서 중앙에서 자산을 관리하고 Creative Cloud 및 기타 애플리케이션에서 이러한 에셋을 이용할 수 있으며 브랜딩을 비롯한 다양한 표준을 손쉽게 준수할 수 있습니다.

AEM 데스크톱 앱을 사용하려면

* AEM 서버 버전이 AEM 데스크탑 앱에서 지원되는지 확인합니다. 호환성 [매트릭스를 참조하십시오](release-notes-of-v1.md#compatibilitymatrix).
* 애플리케이션을 다운로드하여 설치합니다.
* 몇 개의 에셋을 사용하여 연결을 테스트합니다. 데스크탑에서 [자산 액세스 및 열기를 참조하십시오](use-app-v1.md#openondesktop).

## 시스템 요구 사항, 사전 요구 사항 및 다운로드 링크 {#system-requirements-prerequisites-and-download-links}

자세한 내용은 [AEM 데스크탑 앱 릴리스 노트를 참조하십시오](release-notes-of-v1.md).

## AEM 데스크탑 앱 설치 및 AEM 서버에 연결 {#install-and-connect-aem-desktop-app-to-aem-server}

자세한 내용은 AEM [데스크톱 앱 설치 및 AEM 서버에 연결을 참조하십시오](use-app-v1.md#installandconnect).

>[!NOTE]
>
>한 번에 하나의 AEM 데스크탑 앱 인스턴스만 설치하고 활성화할 수 있습니다.

## 파일 처리 {#file-handling}

데스크탑 앱으로 마운트된 네트워크 공유 위치에서 파일을 변경하면 파일이 두 단계로 해당 위치에 저장됩니다. 첫 번째 단계에서는 파일이 로컬에 저장됩니다. 사용자는 전송 완료를 기다리지 않고 파일을 저장하고 파일을 계속 작업할 수 있습니다.

두 번째 단계에서는 데스크톱 앱이 사전 정의된 지연(예: 30초) 후에 업데이트된 파일을 AEM 서버에 업로드합니다. 이 작업은 백그라운드에서 수행됩니다. 업로드 작업의 상태를 보려면 자산 상태 보기 옵션을 사용합니다.

1. 자산을 AEM Assets에 업로드합니다.
1. 도구 모음에서 AEM 데스크톱 앱 아이콘을 클릭/탭합니다.
1. 메뉴에서 자산 상태 보기 옵션을 선택합니다.
1. 대화 상자에서 업로드 작업의 상태를 검토하십시오.

>[!NOTE]
>
>AEM 데스크탑 앱은 최대 40GB의 자산을 처리할 수 있습니다.

## 디스패처 뒤의 AEM 인스턴스에 연결 {#connect-to-an-aem-instance-behind-a-dispatcher}

자산 API의 복사 및 이동 메서드는 AEM에 다음과 같은 추가 헤더를 전달해야 합니다.

* X-대상
* X-깊이
* X-덮어쓰기

AEM Desktop은 기본 포트를 포함하는 URL을 사용하여 AEM에 연결합니다. 따라서 발송자 구성의 `virtualhosts` 설정에는 기본 포트 번호가 포함되어야 합니다. 구성에 대한 자세한 내용은 `virtualhosts` 가상 호스트 [식별을 참조하십시오](https://docs.adobe.com/content/help/en/experience-manager-dispatcher/using/configuring/dispatcher-configuration.html#identifying-virtual-hosts-virtualhosts).

발송자가 이러한 추가 헤더를 통과하도록 구성하는 방법에 대한 자세한 내용은 HTTP 헤더 [지정을 참조하십시오](https://docs.adobe.com/content/help/en/experience-manager-dispatcher/using/configuring/dispatcher-configuration.html#specifying-the-http-headers-to-pass-through-clientheaders).

### 프록시 지원 {#proxy-support}

AEM 데스크톱 앱은 시스템의 사전 정의된 프록시를 사용하여 HTTPS를 통해 인터넷에 연결합니다. 이 앱은 추가 인증이 필요 없는 네트워크 프록시를 통해서만 연결할 수 있습니다.

Windows(인터넷 옵션 > LAN 설정)에 대한 프록시 서버 설정을 구성하거나 수정하는 경우 변경 사항이 적용되도록 AEM 데스크톱 앱을 다시 시작하십시오.

>[!NOTE]
>
>프록시 구성은 데스크톱 앱을 시작할 때만 적용됩니다. 변경 사항이 적용되려면 앱을 닫고 다시 실행하십시오.

프록시에 인증이 필요한 경우 IT 팀이 프록시 서버 설정의 Experience Manager 자산 URL을 허용하여 응용 프로그램 트래픽을 전달할 수 있습니다.

## 자산 정보 대화 상자 사용자 지정 {#customize-the-asset-info-dialog}

다음 구성 요소 중 하나 또는 모두를 오버레이하여 [자산 정보] 대화 상자를 사용자 지정할 수 있습니다.

* [MOCK] The Granite user interface page at `/libs/dam/gui/content/assets/moreinfo`
* HTL 구성 `/css/javascript` 요소 `/libs/dam/gui/components/admin/moreinfo`

겹쳐진 구성 요소는 사용자 정의 특성에 따라 다릅니다. 자산 정보 대화 상자의 일부로 표시되는 구성 요소를 변경하려면 [화강암 사용자 인터페이스] 페이지를 오버레이합니다. 대화 상자의 HTML/CSS/Javascript 내용을 변경하려면 HTL 구성 요소를 오버레이하십시오.

## 캐시 관리 {#manage-cache}

Windows에서 캐시는 데스크톱 앱 `%LOCALAPPDATA%\Adobe\AssetsCompanion\Cache\`에 구성된 AEM 호스트의 인코딩 버전입니다. 예를 들어, 으로 `http://localhost:4502` 나타납니다 `http%3A%2F%2Flocalhost%3A4502%2F`.

Mac OS X의 경우 유사한 디렉토리가 있습니다 `~/Library/Group Containers/group.com.adobe.aem.desktop/cache`.

### 캐시 관리를 위한 인앱 옵션 {#in-app-option-to-manage-cache}

로컬 캐싱 용도로 사용할 수 있는 디스크 공간의 양을 제어할 수 있습니다. AEM Assets 서버의 아티팩트는 보다 원활한 경험을 위해 로컬에 캐시됩니다. 요구 사항에 맞게 기본값을 변경할 수 있습니다. 또한 캐시를 지우면 모든 자산을 새로 가져올 수 있습니다. 원하는 옵션을 설정하려면 응용 프로그램 아이콘을 클릭하고 **[!UICONTROL Advanced]** > **[!UICONTROL Manage Cache]**&#x200B;를 클릭합니다. ***

>[!NOTE]
>
>캐시를 지우면 저장하지 않은 변경 사항이 유지됩니다. AEM 서버에 체크 인되지 않은 모든 자산은 유지되며 삭제되지 않습니다.

### Windows에서 캐시 위치 변경 {#change-location-of-cache-on-windows}

AEM 데스크톱 앱에 대한 캐시의 기본 위치는 다음과 같습니다.

* Windows: `%LocalAppData%\Adobe\AssetsCompanion\Cache\EncodedAEMEndpoint`
* Mac: `~/Library/Group/Containers/group.com.adobe.aem.desktop/cache/EncodedAEMEndpoint`

`EncodedAEMEndpoint` 은(는) AEM 데스크톱 앱의 구성된 AEM 끝점 URL입니다. 값은 AEM 서버의 타깃팅 URL의 인코딩된 버전입니다. 예를 들어 응용 프로그램이 타깃팅하는 경우 디렉토리 이름 `http://localhost:4502`은 입니다 `http%3A%2F%2Flocalhost%3A4502`. 이 예제의 캐시 디렉터리에 대한 Windows 경로는 %LocalAppData%\Adobe\AssetsCompanion\Cache\http%3A%2F%2Flocalhost%3A4502입니다.

응용 프로그램이 다른 폴더 또는 다른 드라이브를 가리키도록 지정하려면 응용 프로그램의 구성 파일을 편집합니다.

1. 앱의 설치 디렉토리로 이동합니다. Windows의 기본 위치는 입니다 `C:\Program Files (x86)\Adobe\Adobe Experience Manager Desktop`.
1. 텍스트 편집기를 사용하여 Adobe Experience Manager Desktop.exe.config 파일을 편집합니다.

   이 파일에 대한 변경 사항을 저장하려면 관리자 권한이 필요합니다.

1. &quot;ProxyCacheRoot&quot; 문자열을 검색합니다. 값이 캐시 위치 &quot;%LocalAppData%\Adobe\AssetsCompanion\Cache&quot;으로 설정되어 있는 것이 보입니다. 이 값을 유효한 경로로 변경하기만 하면 됩니다.

   >[!NOTE]
   >
   >앱은 자동으로 *&lt;인코딩된 AEM Endpoint>* 하위 디렉토리를 만듭니다. 이 동작을 구성할 수 없습니다.

>[!MORELIKETHIS]
* [AEM 데스크탑 앱 소개](https://helpx.adobe.com/customer-care-office-hours/aem/desktop-app.html)
* [AEM 데스크탑 앱 사용](use-app-v1.md)
* [AEM 데스크탑 앱의 체크 인/체크 아웃 이해](https://docs.adobe.com/content/help/en/experience-manager-learn/assets/collaboration/checkin-checkout-technical-video-understand.html)
* [AEM Assets에서 데스크탑 앱 사용](https://docs.adobe.com/content/help/en/experience-manager-learn/assets/collaboration/checkin-checkout-technical-video-understand.html)
* [AEM 데스크탑 앱 문제 해결](troubleshoot-app-v1.md)

