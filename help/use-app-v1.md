---
title: 데스크탑 [!DNL Experience Manager] 앱 버전 1.x 사용
description: Adobe Experience Manager 데스크탑 앱 버전 1.x를 사용하고 데스크탑에서 에셋으로 작업을 최적화하는 방법을 살펴보십시오.
contentOwner: AG
translation-type: tm+mt
source-git-commit: 2893fc1f8aad02e1436a1a281a320e6837487220
workflow-type: tm+mt
source-wordcount: '2379'
ht-degree: 0%

---


# 데스크탑 [!DNL Experience Manager] 앱 v1.x 사용 {#use-aem-desktop-app-v1x}

Using the App, the assets within [!DNL Experience Manager] are easily accessible on your local desktop and can be used in any desktop applications. 에셋은 Mac Finder 또는 Windows 탐색기에서 쉽게 표시되며, 데스크탑 애플리케이션에서 열었으며 로컬에서 변경될 수 있습니다. 변경 사항은 저장소에 새로 만든 버전으로 다시 [!DNL Experience Manager] 저장됩니다.

이러한 통합을 통해 조직의 다양한 역할이 중앙에서 자산을 관리하고 Creative Cloud 및 기타 애플리케이션에서 자산에 액세스할 수 있으며 브랜딩을 비롯한 다양한 표준을 쉽게 준수할 수 있습니다.

데스크톱 앱 v1을 사용하는 [!DNL Experience Manager] 주요 작업은 다음과 같습니다.

1. [서버와 [!DNL Experience Manager] 연결](#installandconnect)
1. [데스크탑에서 바로 에셋 열기](#openondesktop)
1. [데스크탑에서 에셋 편집 및 체크 아웃](#workonassets)
1. [자산 및 폴더 일괄 업로드](#bulkupload)

권장되는 다양한 방법과 그렇지 않은 방법은 앱 사용 [모범 사례를 참조하십시오](best-practices-for-v1.md). 앱 사용 시 문제가 발생하는 경우 데스크톱 문제 해결 방법을 [ [!DNL Experience Manager] 참조하십시오](troubleshoot-app-v1.md).

>[!NOTE]
>
>[!DNL Experience Manager] 데스크탑 앱은 [!DNL Experience Manager] 6.1 릴리스에서 도입되었으며 [!DNL Experience Manager Assets Companion App]호출됩니다.

## [!DNL Experience Manager] 크리에이티브 워크플로우의 데스크탑 앱 터치 포인트 {#aem-desktop-app-touch-points-in-the-creative-workflow}

[!DNL Experience Manager] 데스크탑 앱과 함께 크리에이티브 워크플로우 [!DNL Assets]에 통합되고 다음과 같은 터치 포인트를 제공합니다.

![[!DNL Experience Manager] 데스크탑 앱 터치 포인트 크리에이티브 워크플로우](assets/aem_desktopapp_workflow.png)

[!DNL Experience Manager] 데스크탑 앱 터치 포인트 크리에이티브 워크플로우

## 앱 설치 및 [!DNL Experience Manager] 서버 연결 {#installandconnect}

크리에이티브 에셋을 만들거나 편집하려면 먼저 데스크탑 응용 프로그램을 [!DNL Assets] 서버와 연결하여 저장소에서 에셋을 다운로드하고 업로드합니다. 다음 작업을 수행합니다.

1. [앱을 설치합니다](#installapp).
1. [환경 설정](#inapppref) 및 연결 세부 사항을 설정합니다.
1. [서버 [!DNL Experience Manager] 에](#connect) 연결하고 에셋 저장소를 로컬 드라이브로 마운트합니다.
1. [서버에서 데스크톱 작업을](#desktopactions) 활성화합니다 [!DNL Experience Manager] .

[!DNL Experience Manager] 데스크탑 앱은 HTTPS 연결을 사용하여 에셋을 빠르고 안전하게 전송하기 위해 [!DNL Experience Manager] 서버에 연결합니다.

>[!NOTE]
>
>설치 및 구성 단계의 일부 또는 전체를 위해서는 관리자 또는 시스템 관리자의 도움이 필요할 수 [!DNL Experience Manager] 있습니다.

### 응용 프로그램 설치 {#installapp}

데스크탑 [!DNL Experience Manager] 앱을 사용하려면 앱에서 [!DNL Experience Manager] 서버 버전이 지원되는지 확인하십시오. 운영 체제(Mac 또는 Windows)에 적합한 설치 파일(바이너리)을 다운로드하고 앱을 설치합니다.

네트워크 및 시스템 환경 설정에 따라 자세한 구성이 필요할 수 있습니다. 자세한 내용은 [데스크톱 앱 [!DNL Experience Manager] 설치 및 구성을](install-configure-app-v1.md) 참조하십시오.

1. 데스크탑 [[!DNL Experience Manager] 앱 다운로드 페이지로](https://helpx.adobe.com/experience-manager/kb/download-companion-app.html) 이동하여 운영 체제에 적합한 바이너리를 다운로드합니다.
1. 다운로드한 설치 파일을 실행하고 화면의 지침에 따라 앱을 설치합니다.

   >[!NOTE]
   >
   >하나의 [!DNL Experience Manager] 데스크탑 앱 인스턴스만 설치하고 한 번에 활성화할 수 있습니다.

### 인앱 옵션 및 환경 설정 이해 {#inapppref}

이 응용 프로그램에서는 설정이 연결 및 서버와의 연결을 끊고, 업로드 상태를 보고, 로컬 캐시를 관리하는 등의 작업을 수행할 수 있습니다. [!DNL Experience Manager] 기본 설정은 응용 프로그램의 일반 사용자에 대해 작동합니다. 설정을 수정하여 응용 프로그램에서 더 많은 작업을 수행하고 [!DNL Experience Manager] 서버와의 통합에서 벗어날 수 있습니다. 다양한 설정은 아래에 자세히 설명되어 있습니다.

**자산 탐색** 저장소가 마운트된 로컬 드라이브를 [!DNL Assets] 엽니다. 즉, 로컬 시스템에서 사용 가능한 에셋을 살펴보십시오.

**자산 상태** 보기 변경된 자산이 업로드되거나 새 자산이 [!DNL Assets] 저장소에 추가되면 애플리케이션이 백그라운드에서 자산을 업로드합니다. 배경 업로드를 사용하면 업로드가 완료될 때까지 기다릴 필요 없이, 특히 크기가 큰 자산에 대해 원활한 작업을 수행할 수 있습니다. 변경 사항을 로컬에 저장할 수 있으며 잊어버릴 수도 있습니다. 사용 가능한 대역폭에 따라 응용 프로그램에서 이러한 에셋을 서버로 전송하는 데 시간이 걸립니다. 몇 가지 기본 정보와 함께 업로드 상태를 확인할 수 있습니다.

**옵션** 시스템 시작 시 응용 프로그램을 시작하는 설정에 액세스하려면 데스크탑 앱 트레이의 옵션을 클릭합니다.앱을 실행할 때 [!DNL Experience Manager] 서버에 연결하는 방법;를 클릭하여 마운트한 후 사용할 수 있는 로컬 드라이브 문자 [!DNL Assets] 를 변경합니다.

**고급 > 캐시** 관리 로컬 캐싱 용도로 사용할 수 있는 디스크 공간의 양을 제어할 수 있습니다. 서버의 아티팩트는 [!DNL Assets] 보다 원활한 경험을 위해 로컬에 캐시됩니다. 요구 사항에 맞게 기본값을 변경할 수 있습니다. 또한 캐시를 지우면 모든 자산을 새로 가져올 수 있습니다. 캐시를 지우면 저장하지 않은 변경 사항이 유지됩니다. 서버에 체크 인되지 않은 모든 자산은 [!DNL Experience Manager] 유지되며 삭제되지 않습니다.

### 서버에 [!DNL Experience Manager] 연결 {#connect}

이 앱은 Mac 및 Windows에서 프록시 구성을 지원합니다. 앱이 시작되면 구성이 읽혀집니다. 프록시 설정을 수정하는 경우 변경 사항을 적용하려면 앱을 다시 시작하십시오.

>[!NOTE]
>
>프록시 설정을 수정하는 경우 변경 사항이 적용되도록 앱을 다시 시작합니다. 그렇지 않으면 앱이 이전에 구성한 프록시 서버를 계속 사용합니다.

1. 데스크탑 [!DNL Experience Manager] 앱을 실행합니다. 인스턴스를 [!DNL Experience Manager] 앱과 매핑하려면 [!DNL Experience Manager] 서버를 형식으로 지정합니다 `https://[aem-server-url]:[port]`.

   ![Mac에서 인증 및 [!DNL Experience Manager] 서버 URL 제공](assets/aem_desktop_app_server_url.png)

1. 로그인 화면에서 인스턴스의 사용자 이름과 암호를 지정합니다. 대체 [!DNL Experience Manager] 인스턴스를 지정하려면 옵션을 **[!UICONTROL Alternate Login URL]** 선택합니다.

   ![데스크톱 앱의 로그인 화면에서 [!DNL Experience Manager] 서버 자격 증명을 [!DNL Experience Manager] 제공합니다.](assets/login_screen_v1.png)

### 웹 인터페이스에서 데스크탑 작업 [!DNL Experience Manager] 활성화 {#desktopactions}

자산 사용자 인터페이스 내에서 자산 위치 또는 체크 아웃을 살펴보고 데스크톱 응용 프로그램에서 편집할 자산을 열 수 있습니다. 이러한 옵션은 데스크톱 작업이라고 하며 기본적으로 활성화되지 않습니다. 다음 단계에 따라 활성화합니다.

1. 자산 인터페이스에서 도구 모음의 오른쪽 상단에 있는 사용자 아이콘을 클릭/탭합니다.
1. 을 **[!UICONTROL My Preferences]** 클릭하여 대화 상자를 **[!UICONTROL Preferences]** 표시합니다.

   ![[!DNL Experience Manager] 사용자 환경 설정 인터페이스](assets/aem_ui_user_preferences.png)

1. 사용자 환경 설정 대화 상자에서 을 선택합니다 **[!UICONTROL Show Desktop Actions For Assets]**. 클릭 **[!UICONTROL Accept]**.

   ![데스크탑 작업 [!UICONTROL Show Desktop Actions For Assets] 을 활성화하려면 확인](assets/enable_desktop_actions.png)

   *그림:데스크톱 작업을 활성화하려면 자산에 대한 데스크톱 작업 표시를 선택합니다.*

## 데스크탑에서 에셋 액세스 및 열기 {#openondesktop}

[ **열기** ]를 클릭하여 로컬 컴퓨터에서 자산을 열면 앱이 자산을 내부 캐시에 다운로드합니다. 앱은 다운로드한 자산의 파일 형식과 관련된 기본 데스크톱 응용 프로그램을 실행합니다.

Mac의 경우 **컨텍스트** 메뉴에서 열기를 선택하여 [!DNL Experience Manager] 데스크탑 앱을 통해 자산을 엽니다. Windows의 경우 컨텍스트 메뉴에서 웹에서 열기를 선택하여 자산을 엽니다. 자산 상태 창에서 ![데스크탑에서 열기를 클릭/탭하여 자산을 엽니다](assets/do-not-localize/aemassets_icon_openondesktop.png) .

Adobe InDesign(INDD) 파일의 경우 컨텍스트 메뉴 **[!UICONTROL Open]** 에서 선택합니다. 이 옵션을 클릭하면 앱이 로컬 파일 시스템에 연결된 에셋을 다운로드한 다음 Adobe InDesign에서 INDD 파일을 엽니다. 이 방법을 사용하면 INDD 파일을 편집할 때 필요한 자산을 로컬에서 사용할 수 있습니다.

![데스크탑 앱을 사용하여 자산에 액세스하고 열기 위한 컨텍스트 메뉴 옵션 [!DNL Experience Manager]](assets/aem_desktopapp_mac_context_menu.png)

*그림:데스크탑 앱을 사용하여 자산에 액세스하고 여는 컨텍스트 메뉴 옵션 [!DNL Experience Manager]*

>[!NOTE]
>
>Windows에서 [기본 Windows 7 설정은](https://support.microsoft.com/en-us/kb/2668751) 데스크톱 앱이 50MB보다 큰 자산을 처리하지 [!DNL Experience Manager] 못하게 합니다.

>[!NOTE]
>
>Adobe은 Mac의 Finder 보기 옵션으로 이동하고 마운트된 **폴더에 대한 옵션**&#x200B;항목 정보 표시 **, 항목 미리 보기**&#x200B;표시 **및 미리 보기 열** 표시 [!DNL Assets] 를 비활성화하는 것이좋습니다. 성능이 개선됩니다.

### 추가 [!DNL Experience Manager] 인터페이스 옵션 {#additional-options-in-aem-assets}

리포지토리를 로컬 드라이브에 매핑한 후 매핑된 자산 및 폴더에 대해 추가 아이콘 및 폴더 업로드 기능이 표시되도록 설정할 수 있습니다. [!DNL Assets]

1. 인터페이스를 열고 폴더 또는 자산 위에 포인터를 두면 카드 보기에서 빠른 작업으로 데스크톱 작업을 표시할 수 있습니다. [!DNL Assets]

   ![자산 UI에서 빠른 작업 메뉴를 열고 데스크톱 작업을 봅니다](assets/desktop_actions_in_card_view.png)

   *그림:자산 UI에서 빠른 작업 메뉴를 열고 데스크톱 작업을 봅니다.*

   이러한 데스크톱 작업은 자산을 선택한 후 도구 모음에서 **데스크톱 작업** 옵션을 클릭하거나 자산 페이지의 도구 모음에서 사용할 수도 있습니다.

1. 특정 파일 확장자와 연결된 데스크톱 응용 프로그램에서 자산을 열려면 데스크탑에서 **열기 빠른 작업** 바탕 화면에서 ![열기 아이콘을 클릭합니다](assets/do-not-localize/aemassets_icon_openondesktop.png).

   또는 도구 모음 **의** [ **데스크톱 작업** ] 메뉴에서 [열기]를선택합니다.

로컬 파일 시스템에서 특정 자산을 찾으려면 빠른 작업 **표시** 아이콘 ![표시를 클릭합니다](assets/do-not-localize/aemassets_reveal_icon.png). 또는 도구 모음 **의** [ **데스크톱 작업** ] 메뉴에서 [표시]를 선택합니다.

## 자산 상태 이해 {#understand-the-asset-statuses}

| ![Windows 기본 앱 아이콘](assets/do-not-localize/win_default.png) | 앱이 서버에 연결되고 모든 자산이 동기화됩니다. |
--- |--- |
| ![Windows 사용 안 함 아이콘](assets/do-not-localize/win_disabled.png) | 앱이 실행되었지만 서버와 연결되지 않았습니다. 일부 자산의 동기화가 보류 중일 수 있습니다. |
| ![Windows 파일 동기화 아이콘](assets/do-not-localize/win_sync.png) | 자산이 동기화 중입니다. 파일이 업로드되거나 다운로드되고 있습니다. 정확한 상태를 보고 자산 상태 창에서 전송을 일시 중지할 수 있습니다. |
| ![Windows 재연결 아이콘](assets/do-not-localize/win_refresh.png) | 앱이 다시 연결하려고 합니다. 네트워크 문제로 인해 연결이 끊어질 수 있습니다. |

## 에셋에서 작업 {#workonassets}

### 웹 인터페이스에서 자산 확인 [!DNL Experience Manager] {#check-out-assets-from-the-aem-web-interface}

[!DNL Assets] 편집할 에셋을 확인하고 변경을 완료한 후 다시 체크 인할 수 있습니다. 자산을 체크 아웃한 후, 자신만 자산을 편집, 주석 달기, 게시, 이동 또는 삭제할 수 있습니다. 자산을 체크 아웃하면 자산이 잠기고 다른 사용자가 이러한 작업을 수행할 수 없습니다. 자산을 체크 아웃/체크 인하려면 자산에 대해 쓰기 액세스 권한이 필요합니다.

두 가지 방법으로 [!DNL Experience Manager] 웹 인터페이스에서 자산을 확인할 수 있습니다. 첫 번째 방법에 대한 자세한 내용은 자산 UI에서 [파일 체크 인 및 체크 아웃을 참조하십시오](https://experienceleague.adobe.com/docs/experience-manager-65/assets/managing/check-out-and-submit-assets.html). 데스크톱 앱이 설치될 때 자산을 체크 아웃하고 여는 두 번째 방법은 다음 단계를 [!DNL Experience Manager] 따르십시오.

1. 인터페이스를 열고 폴더 또는 자산 위에 포인터를 두면 카드 보기에서 빠른 작업으로 데스크톱 작업을 표시할 수 있습니다. [!DNL Assets]

   ![카드 보기의 속성 옵션](assets/desktop_actions_in_card_view.png)

   이러한 데스크톱 작업은 자산을 선택한 후 도구 모음에서 데스크톱 작업 아이콘을 클릭/탭하거나 자산 페이지의 도구 모음에서 사용할 수도 있습니다.

1. 자산을 열려면 데스크탑에서 열기 빠른 작업 데스크탑에서 열기 아이콘 ![을 클릭/탭합니다](assets/do-not-localize/aemassets_icon_openondesktop.png).

   또는 도구 모음의 [데스크탑 작업] 메뉴에서 [열기]를 선택합니다.

   >[!NOTE]
   >
   >방금 열었지만 체크 아웃되지 않은 파일을 편집해도 다른 사용자는 사용자가 에셋을 업데이트하는지 알 수 없습니다.

1. Adobe Creative Cloud 애플리케이션에서 편집할 에셋을 열려면 데스크탑 빠른 작업 편집 데스크탑 ![편집 아이콘을 클릭/탭합니다](assets/do-not-localize/aemassets_icon_editdesktop.png). 또한 편집할 에셋을 확인합니다. 편집을 마친 후 자산을 체크 인하여 변경 내용을 업데이트하십시오 [!DNL Assets].

   또는 도구 모음의 [데스크톱 작업] 메뉴에서 [편집]을 선택합니다.

1. [열기] 메뉴 옵션을 선택합니다. 선택한 자산이 미리 보기 모드로 열립니다.
1. 자산을 편집하려면 편집 옵션을 선택합니다. 자산은 편집 모드에서 열립니다.

### Mac OS에서 Finder에서 자산 확인 {#check-out-assets-on-mac}

이 앱을 사용하면 다른 사용자가 작업 중인 파일을 수정하지 못하도록 자산 파일을 체크 아웃할 수 있습니다.

1. Mac 컨텍스트 메뉴에서 AEM Assets 폴더 열기 옵션을 선택하여 Finder를 엽니다.

   ![데스크탑 앱을 사용하여 자산에 액세스하고 열기 위한 컨텍스트 메뉴 옵션 [!DNL Experience Manager]](assets/aem_desktopapp_mac_context_menu.png)

   *그림:데스크탑 앱을 사용하여 자산에 액세스하고 여는 컨텍스트 메뉴 옵션 [!DNL Experience Manager]*

1. 체크 아웃할 자산으로 이동합니다.
1. 자산을 마우스 오른쪽 단추로 클릭하고 컨텍스트 메뉴에서 추가 자산 정보를 선택합니다.
1. 자산 정보 대화 상자에서 체크아웃 아이콘을 클릭/탭하여 자산을 확인합니다. 체크 아웃 아이콘을 클릭/탭하면 체크 인 아이콘으로 전환됩니다.

   ![체크아웃할 자산 찾아보기](assets/browse_assets_to_checkout.png)

1. 다른 사용자가 사용할 수 있도록 자산을 체크 인하려면 자산 정보 대화 상자에서 체크 인 아이콘을 클릭/탭합니다.

### Windows에서 자산 확인 {#check-out-assets-on-windows}

이 앱을 사용하면 다른 사용자가 작업 중인 파일을 수정하지 못하도록 자산 파일을 체크 아웃할 수 있습니다.

1. 컨텍스트 메뉴에서 자산 탐색을 선택하여 탐색기를 엽니다.
1. 탐색기에서 체크 아웃할 자산의 위치로 이동합니다.
1. 자산을 마우스 오른쪽 단추로 클릭하고 컨텍스트 메뉴에서 웹에서 열기를 선택합니다.
1. 자산 정보 대화 상자에서 체크아웃 아이콘을 클릭/탭합니다. 체크아웃 아이콘은 체크 인 아이콘으로 전환됩니다.

   ![체크아웃 아이콘이 전환합니다](assets/checkout_icon_toggles.png)

1. 탐색기에서 자산을 검토합니다. 자산 잠금 아이콘의 ![잠금](assets/do-not-localize/aemassets_icon_lockcheckout.png) 아이콘은 자산을 체크 아웃했음을 나타냅니다.

   >[!NOTE]
   >
   >약간의 지연 후에 잠금 아이콘이 나타날 수 있습니다. [!DNL Experience Manager] 데스크탑 앱은 에셋을 캐시하여 빠른 액세스를 제공하므로 잠긴 상태를 업데이트하는 데 몇 분 정도 걸릴 수 있습니다.

1. 다른 사용자가 사용할 수 있도록 자산을 체크 인하려면 [자산 정보] 대화 상자에서 **체크 인 아이콘을 클릭/탭합니다** .

### Finder 또는 탐색기를 사용하여 자산 체크 인 및 웹 인터페이스 사용 {#check-in-an-asset-using-finder-or-explorer-and-using-web-interface}

에셋 편집이 끝나면 데스크탑 애플리케이션에 에셋을 저장합니다. 컨텍스트 메뉴에서 **추가 자산 정보를** 선택하고 체크 인을 클릭합니다.

에셋이 [!DNL Experience Manager] 서버에 업로드됩니다. 시스템 트레이 아이콘에서 자산 상태 **보기를 선택하여** 업로드 상태를 확인할 수 있습니다(선택 사항). 또는 [!DNL Experience Manager] 웹 인터페이스에서 자산을 체크 인할 수 있습니다. 체크 아웃된 자산을 클릭하거나 선택합니다. 도구 모음에서 체크 인 아이콘 ![체크 인 아이콘을 클릭합니다](assets/do-not-localize/aemassets_icon_checkin.png).

자산이 로컬에 저장된 후 [!DNL Experience Manager] 자동으로 업로드됩니다. 이 체크 인은 자산을 다른 [!DNL Experience Manager] 사용자가 편집할 수 있도록 합니다.

### 서버에 자산 및 폴더 일괄 [!DNL Experience Manager] 업로드 {#bulkupload}

데스크탑 [!DNL Experience Manager] 앱을 사용하면 로컬 파일 디렉토리에서 에셋이 포함된 전체 폴더를 업로드할 수 있습니다 [!DNL Assets]. 이렇게 하면 한 번에 하나씩 업로드하지 않아도 폴더 내의 모든 에셋이 일괄 업로드됩니다.

1. 자산 UI의 도구 모음에서 **만들기를** 클릭/탭하고 메뉴에서 **폴더** 업로드를 선택합니다.
1. 업로드할 폴더를 찾아 선택합니다.
1. 확인을 클릭/탭합니다. [자산 상태] 대화 상자에 업로드 상태가 표시됩니다.

   ![자산 상태 창에서 업로드 상태 보기](assets/aem_desktopapp_bulkupload_status.png)

   자산 상태 창에서 업로드 상태 보기

   >[!NOTE]
   >
   >해당 아이콘을 클릭/탭하여 업로드를 수동으로 일시 중지하거나 취소할 수 있습니다.

1. 폴더 업로드 후 대화 상자를 닫고 자산 UI로 이동합니다. 업로드된 폴더가 웹 인터페이스에 표시됩니다.

Adobe에서는 로컬 파일 시스템에서 네트워크 공유 영역으로 많은 파일 또는 중첩된 폴더를 복사하여 붙여넣거나 드래그하는 것이 좋습니다. 기술적 제한으로 인해 앱에서 업로드 프로세스를 제어할 수 없고 성능이 좋지 않습니다.

또는 Finder 또는 탐색기 [!DNL Experience Manager] 에서 업로드할 파일/폴더를 선택하고, 시스템 클립보드로 복사하고, 네트워크 공유 영역의 대상 폴더로 이동하고, [!DNL Experience Manager] 데스크탑 앱 컨텍스트 메뉴에서 자산 **붙여넣기를 선택합니다**. 이렇게 하면 [!DNL Experience Manager] 데스크톱 앱이 **웹 인터페이스에서 사용할 수 있는 폴더** 업로드 [!DNL Experience Manager] 옵션과 유사한 붙여넣은 자산을 업로드하기 시작합니다.

>[!MORELIKETHIS]
>
>* [데스크탑 [!DNL Experience Manager] 앱 애플리케이션 문제 해결](troubleshoot-app-v1.md)

