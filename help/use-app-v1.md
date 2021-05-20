---
title: ' [!DNL Experience Manager] 데스크탑 앱 버전 1.10을 사용하십시오.'
description: Adobe Experience Manager 데스크탑 앱 버전 1.10을 사용하고 데스크탑의 자산으로 작업을 최적화하는 방법을 알아봅니다.
feature: 데스크탑 앱,자산 관리
exl-id: 2fdc1c8d-b822-4cca-ad06-bd875a00aa6d
source-git-commit: 4616934e8923693106401da008e2510310d0742a
workflow-type: tm+mt
source-wordcount: '2377'
ht-degree: 0%

---

# [!DNL Experience Manager] 데스크탑 앱 v1.10 {#use-aem-desktop-app-v1x} 사용

앱을 사용하면 로컬 데스크탑에서 [!DNL Experience Manager] 내의 자산에 쉽게 액세스할 수 있으며 모든 데스크탑 애플리케이션에서 사용할 수 있습니다. 자산은 Mac Finder 또는 Windows Explorer에서 쉽게 표시되며, 데스크탑 애플리케이션에서 열고, 로컬로 변경할 수 있습니다. 변경 사항은 리포지토리에서 생성된 새 버전으로 다시 [!DNL Experience Manager]에 저장됩니다.

이러한 통합을 통해 조직에서 다양한 역할이 자산의 자산을 중앙에서 관리하고 Creative Cloud 및 기타 애플리케이션에서 액세스할 수 있지만 브랜딩을 포함한 다양한 표준을 쉽게 준수할 수 있습니다.

[!DNL Experience Manager] 데스크탑 앱 v1을 사용하여 수행하는 주요 작업은 다음과 같습니다.

1. [ [!DNL Experience Manager] 서버와 연결](#installandconnect)
1. [데스크탑에서 바로 자산 열기](#openondesktop)
1. [데스크탑에서 자산 편집 및 체크아웃](#workonassets)
1. [자산 및 폴더를 일괄 업로드](#bulkupload)

권장되는 여러 가지 작업 및 방법은 [앱 사용 우수 사례](best-practices-for-v1.md)를 참조하십시오. 앱 사용 시 문제가 발생하는 경우 [문제를 해결하는 방법 [!DNL Experience Manager] desktop](troubleshoot-app-v1.md)을 참조하십시오.

>[!NOTE]
>
>데스크탑 앱은 [!DNL Experience Manager] 6.1 릴리스에서 도입되었으며 [!DNL Experience Manager Assets Companion App]라고 했습니다.

## [!DNL Experience Manager] 크리에이티브 워크플로우의 데스크탑 앱 터치 포인트  {#aem-desktop-app-touch-points-in-the-creative-workflow}

[!DNL Experience Manager] 데스크탑 앱은  [!DNL Assets]와 함께 크리에이티브 워크플로우에 통합되고 다음과 같은 터치 포인트를 제공합니다.

![[!DNL Experience Manager] 데스크탑 앱 터치 포인트는 크리에이티브 워크플로우입니다](assets/aem_desktopapp_workflow.png)

[!DNL Experience Manager] 데스크탑 앱 터치 포인트는 크리에이티브 워크플로우입니다

## 앱을 설치하고 [!DNL Experience Manager] 서버에 연결합니다 {#installandconnect}

크리에이티브 자산을 만들거나 편집하려면 먼저 데스크탑 애플리케이션을 [!DNL Assets] 서버와 연결하여 저장소에서 자산을 다운로드하고 업로드하십시오. 다음 작업을 수행합니다.

1. [앱을 설치합니다](#installapp).
1. [기본 설정 ](#inapppref) 및 연결 세부 정보를 설정합니다.
1. [서버에  [!DNL Experience Manager] ](#connect) 연결하고 자산 저장소를 로컬 드라이브로 마운트합니다.
1. [데스크톱 작업 ](#desktopactions) 서버를  [!DNL Experience Manager] 사용하도록 설정합니다.

[!DNL Experience Manager] 데스크탑 앱에서는 HTTPS 연결을 사용하여  [!DNL Experience Manager] 서버에 연결하여 자산을 강력하고 안전하게 전송합니다.

>[!NOTE]
>
>설치 및 구성 단계의 일부 또는 전부에 대해 [!DNL Experience Manager] 관리자 또는 시스템 관리자의 도움이 필요할 수 있습니다.

### 응용 프로그램 설치 {#installapp}

[!DNL Experience Manager] 데스크탑 앱을 사용하려면 [!DNL Experience Manager] 서버 버전이 앱에서 지원되는지 확인하십시오. 운영 체제(Mac 또는 Windows)에 적합한 설치 파일(이진)을 다운로드하여 앱을 설치합니다.

네트워크 및 시스템 환경 설정에 따라 자세한 구성이 필요할 수 있습니다. 자세한 내용은 [설치 및 구성 [!DNL Experience Manager] 데스크탑 앱](install-configure-app-v1.md)을 참조하십시오.

1. [[!DNL Experience Manager] 데스크탑 앱 v1.10 다운로드 페이지](/help/release-notes-of-v1.md)로 이동하여 운영 체제에 적합한 바이너리를 다운로드합니다.
1. 다운로드한 설치 파일을 시작하고 화면의 지침에 따라 앱을 설치합니다.

   >[!NOTE]
   >
   >[!DNL Experience Manager] 데스크탑 앱의 인스턴스를 하나만 설치하고 한 번에 활성화할 수 있습니다.

### 인앱 옵션 및 환경 설정을 이해합니다 {#inapppref}

이 응용 프로그램에서는 [!DNL Experience Manager] 서버에 연결 및 연결을 끊고, 업로드 상태를 보고, 로컬 캐시를 관리하는 등의 작업을 수행할 수 있습니다. 기본 설정은 응용 프로그램의 일반적인 사용자에 대해 작동합니다. 설정을 조정하면 응용 프로그램에서 더 많은 내용을 가져오고 [!DNL Experience Manager] 서버와의 통합을 종료할 수 있습니다. 다양한 설정은 아래에 자세히 설명되어 있습니다.

**자산** 탐색저장소가 마운트된 로컬  [!DNL Assets] 드라이브를 엽니다. 즉, 로컬 시스템에서 사용 가능한 자산을 탐색합니다.

**자산** 상태 보기변경된 자산을 업로드하거나 새 자산을  [!DNL Assets] 저장소에 추가하면 애플리케이션이 자산을 백그라운드에서 업로드합니다. 특히 큰 크기의 자산에 대해 업로드가 완료될 때까지 기다리지 않고 백그라운드 업로드를 통해 원활한 작업을 수행할 수 있습니다. 로컬에 변경 사항을 저장하고 잊어버릴 수 있습니다. 응용 프로그램에서 사용 가능한 대역폭에 따라 이러한 자산을 서버로 전송하는 데 시간이 좀 걸립니다. 몇 가지 기본 정보와 함께 업로드 상태를 확인할 수 있습니다.

**** 옵션: 시스템이 시작될 때 응용 프로그램을 시작할 설정에 액세스하려면 데스크탑 앱 트레이의 옵션을 클릭합니다.앱을 실행할  [!DNL Experience Manager] 때 서버에 연결하려면그리고 마운트한 후 사용 가능한 로컬 드라이브 문자 [!DNL Assets] 를 변경합니다.

**고급 >** 캐시 관리로컬 캐싱에 사용할 수 있는 디스크 공간의 크기를 제어할 수 있습니다. [!DNL Assets] 서버의 가공물이 로컬에 캐시되므로 더 원활한 경험을 제공할 수 있습니다. 요구 사항에 맞게 기본값을 변경할 수 있습니다. 또한 캐시를 지우면 모든 자산을 새로 가져올 수도 있습니다. 캐시를 지우면 저장하지 않은 변경 사항이 유지됩니다. [!DNL Experience Manager] 서버에 체크 인되지 않은 자산은 모두 유지되며 삭제되지 않습니다.

### [!DNL Experience Manager] 서버에 연결 {#connect}

이 앱은 Mac 및 Windows에서 프록시 구성을 지원합니다. 앱이 시작될 때 구성을 읽습니다. 프록시 설정을 수정하는 경우 변경 사항을 적용하려면 앱을 다시 시작하십시오.

>[!NOTE]
>
>프록시 설정을 수정하는 경우 변경 사항이 적용되도록 앱을 다시 시작합니다. 그렇지 않으면 앱은 이전에 구성한 프록시 서버를 계속 사용합니다.

1. [!DNL Experience Manager] 데스크탑 앱을 시작합니다. [!DNL Experience Manager] 인스턴스를 앱에 매핑하려면 [!DNL Experience Manager] 서버를 `https://[aem-server-url]:[port]` 형식으로 지정합니다.

   ![Mac에서 인증 및  [!DNL Experience Manager] 서버 URL 제공](assets/aem_desktop_app_server_url.png)

1. 로그인 화면에서 인스턴스의 사용자 이름과 암호를 지정합니다. 대체 [!DNL Experience Manager] 인스턴스를 지정하려면 **[!UICONTROL Alternate Login URL]** 옵션을 선택합니다.

   ![ [!DNL Experience Manager]   [!DNL Experience Manager] 데스크탑 앱의 로그인 화면에서 서버 자격 증명을 제공합니다](assets/login_screen_v1.png)

### [!DNL Experience Manager] 웹 인터페이스에서 데스크톱 작업 활성화 {#desktopactions}

Assets 사용자 인터페이스 내에서 자산 위치를 탐색하거나 체크 아웃하고 데스크탑 애플리케이션에서 편집할 자산을 열 수 있습니다. 이러한 옵션을 데스크탑 작업이라고 하며 기본적으로 활성화되지 않습니다. 다음 단계에 따라 활성화하십시오.

1. Assets 인터페이스에서 도구 모음의 오른쪽 상단 모서리에 있는 사용자 아이콘을 클릭/탭합니다.
1. **[!UICONTROL My Preferences]** 을 클릭하여 **[!UICONTROL Preferences]** 대화 상자를 표시합니다.

   ![[!DNL Experience Manager] 사용자 환경 설정을 사용한 인터페이스](assets/aem_ui_user_preferences.png)

1. 사용자 환경 설정 대화 상자에서 **[!UICONTROL Show Desktop Actions For Assets]**&#x200B;을 선택합니다. 클릭 **[!UICONTROL Accept]**.

   ![데스크톱 작업 [!UICONTROL Show Desktop Actions For Assets] 을 활성화하려면 확인](assets/enable_desktop_actions.png)

   *그림:자산에 대한 데스크톱 작업 표시 를 선택하여 데스크톱 작업을 활성화합니다.*

## 데스크탑에서 자산 액세스 및 열기 {#openondesktop}

**열기**&#x200B;를 클릭하여 로컬 컴퓨터에서 자산을 열면 앱은 자산을 해당 내부 캐시에 다운로드합니다. 이 앱은 다운로드한 자산의 파일 유형과 연관된 기본 데스크탑 애플리케이션을 시작합니다.

Mac의 경우 컨텍스트 메뉴에서 **열기**&#x200B;를 선택하여 [!DNL Experience Manager] 데스크탑 앱을 통해 자산을 엽니다. Windows의 경우 컨텍스트 메뉴에서 웹에서 열기 를 선택하여 자산을 엽니다. 자산 상태 창에서 ![데스크탑에서 열기 아이콘](assets/do-not-localize/aemassets_icon_openondesktop.png)을 클릭/탭하여 자산을 엽니다.

INDD(Adobe InDesign) 파일의 경우 컨텍스트 메뉴에서 **[!UICONTROL Open]**&#x200B;을 선택합니다. 이 옵션을 클릭하면 앱이 연결된 자산을 로컬 파일 시스템에 다운로드한 다음 Adobe InDesign에서 INDD 파일을 엽니다. 이 방법을 사용하면 INDD 파일을 편집할 때 필요한 자산을 로컬에서 사용할 수 있습니다.

![ [!DNL Experience Manager] 데스크탑 앱을 사용하여 자산에 액세스하고 여는 컨텍스트 메뉴 옵션](assets/aem_desktopapp_mac_context_menu.png)

*그림: [!DNL Experience Manager] 데스크탑 앱을 사용하여 자산에 액세스하고 여는 컨텍스트 메뉴 옵션.*

>[!NOTE]
>
>Windows에서 [기본 Windows 7 설정](https://support.microsoft.com/en-us/kb/2668751)을 사용하면 [!DNL Experience Manager] 데스크탑 앱에서 50MB보다 큰 자산을 처리할 수 없습니다.

<!-- TBD: The above note is for Windows 7 which is not supported by the app anymore. Remove it later.
-->

>[!NOTE]
>
>Adobe에서는 Mac의 Finder 보기 옵션으로 이동하고 마운트된 [!DNL Assets] 폴더에 대해 **항목 정보 표시**, **항목 미리 보기 표시** 및 **미리 보기 열 표시** 옵션을 비활성화하는 것이 좋습니다. 성능이 향상됩니다.

### [!DNL Experience Manager] 인터페이스의 추가 옵션 {#additional-options-in-aem-assets}

[!DNL Assets] 저장소를 로컬 드라이브에 매핑하면 매핑된 자산 및 폴더에 대해 추가 아이콘과 폴더 업로드 기능이 표시되도록 할 수 있습니다.

1. [!DNL Assets] 인터페이스를 열고 폴더 또는 자산 위로 포인터를 가져가 카드 보기에서 빠른 작업으로 데스크탑 작업을 표시합니다.

   ![Assets UI에서 빠른 작업 메뉴를 열어 데스크탑 작업을 확인합니다](assets/desktop_actions_in_card_view.png)

   *그림:Assets UI에서 빠른 작업 메뉴를 열어 데스크탑 작업을 확인합니다.*

   이러한 데스크톱 작업은 자산을 선택한 후 또는 자산 페이지의 도구 모음에서 **데스크톱 작업** 옵션을 클릭할 때도 사용할 수 있습니다.

1. 특정 파일 확장자와 연결된 데스크탑 애플리케이션에서 자산을 열려면 **데스크탑에서 열기** 빠른 작업 ![바탕 화면에서 열기 아이콘](assets/do-not-localize/aemassets_icon_openondesktop.png)를 클릭합니다.

   또는 도구 모음의 **데스크톱 작업** 메뉴에서 **열기**&#x200B;를 선택합니다.

로컬 파일 시스템에서 특정 자산을 찾으려면 **표시** 빠른 작업 ![표시 아이콘](assets/do-not-localize/aemassets_reveal_icon.png)을 클릭합니다. 또는 도구 모음의 **데스크톱 작업** 메뉴에서 **표시**&#x200B;를 선택합니다.

## 자산 상태 {#understand-the-asset-statuses} 이해

| ![Windows 기본 앱 아이콘](assets/do-not-localize/win_default.png) | 앱이 서버에 연결되고 모든 자산이 동기화됩니다. |
--- |--- |
| ![Windows 사용 안 함 아이콘](assets/do-not-localize/win_disabled.png) | 앱이 시작되었지만 서버와 연결되어 있지 않습니다. 일부 자산의 동기화가 보류 중일 수 있습니다. |
| ![Windows 파일 동기화 아이콘](assets/do-not-localize/win_sync.png) | 자산이 동기화 중입니다. 파일을 업로드하거나 다운로드하는 중입니다. 자산 상태 창에서 정확한 상태를 보고 전송을 일시 중지할 수 있습니다. |
| ![Windows 다시 연결 아이콘](assets/do-not-localize/win_refresh.png) | 앱이 다시 연결하려고 합니다. 네트워크 문제로 인해 네트워크 연결이 끊어질 수 있습니다. |

## 자산 작업 {#workonassets}

### [!DNL Experience Manager] 웹 인터페이스에서 자산 확인 {#check-out-assets-from-the-aem-web-interface}

[!DNL Assets] 편집할 자산을 확인하고 변경을 완료한 후 다시 체크 인할 수 있습니다. 자산을 체크 아웃한 후에는 자산을 편집, 주석 달기, 게시, 이동 또는 삭제할 수만 있습니다. 자산을 체크 아웃하면 자산이 잠기고 다른 사용자가 이러한 작업을 수행하지 못하도록 합니다. 자산을 체크 아웃/체크 인하려면 자산에 대한 쓰기 액세스 권한이 필요합니다.

[!DNL Experience Manager] 웹 인터페이스에서 자산을 체크 아웃하는 방법에는 두 가지가 있습니다. 첫 번째 방법에 대한 자세한 내용은 자산 UI](https://experienceleague.adobe.com/docs/experience-manager-65/assets/managing/check-out-and-submit-assets.html)에서 파일 체크인 및 체크아웃 을 참조하십시오. [ [!DNL Experience Manager] 데스크탑 앱이 설치되었을 때 자산을 체크 아웃하고 여는 두 번째 방법은 다음 단계를 따르십시오.

1. [!DNL Assets] 인터페이스를 열고 폴더 또는 자산 위로 포인터를 가져가 카드 보기에서 빠른 작업으로 데스크탑 작업을 표시합니다.

   ![카드 보기의 속성 옵션](assets/desktop_actions_in_card_view.png)

   이러한 데스크탑 작업은 자산을 선택한 후 도구 모음에서 데스크탑 작업 아이콘을 클릭/탭하거나 자산 페이지의 도구 모음에서 를 선택할 때도 사용할 수 있습니다.

1. 자산을 열려면 데스크탑에서 열기 빠른 작업 ![데스크탑에서 열기 아이콘](assets/do-not-localize/aemassets_icon_openondesktop.png)을 클릭/탭합니다.

   또는 도구 모음의 [데스크톱 작업] 메뉴에서 [열기]를 선택합니다.

   >[!NOTE]
   >
   >방금 열었고 체크 아웃되지 않은 파일을 편집하는 경우 다른 사용자는 사용자가 자산을 업데이트하고 있음을 알 수 없습니다.

1. Adobe Creative Cloud 애플리케이션에서 편집할 자산을 열려면 데스크탑 빠른 편집 작업 ![데스크탑 편집 아이콘](assets/do-not-localize/aemassets_icon_editdesktop.png)을 클릭/탭합니다. 편집할 자산도 체크 아웃됩니다. 편집을 완료한 후 자산을 체크 인하여 [!DNL Assets]의 변경 사항을 업데이트합니다.

   또는 도구 모음의 [데스크톱 작업] 메뉴에서 [편집]을 선택합니다.

1. 메뉴 열기 옵션을 선택합니다. 선택한 자산이 미리 보기 모드로 열립니다.
1. 자산을 편집하려면 편집 옵션을 선택합니다. 자산이 편집 모드로 열립니다.

### Mac OS의 Finder에서 자산 확인 {#check-out-assets-on-mac}

이 앱을 사용하면 다른 사용자가 작업 중인 파일을 수정하지 못하도록 자산 파일을 체크 아웃할 수 있습니다.

1. Mac 컨텍스트 메뉴에서 AEM Assets 폴더 열기 옵션을 선택하여 Finder를 엽니다.

   ![ [!DNL Experience Manager] 데스크탑 앱을 사용하여 자산에 액세스하고 여는 컨텍스트 메뉴 옵션](assets/aem_desktopapp_mac_context_menu.png)

   *그림: [!DNL Experience Manager] 데스크탑 앱을 사용하여 자산에 액세스하고 여는 컨텍스트 메뉴 옵션.*

1. 체크 아웃할 자산으로 이동합니다.
1. 자산을 마우스 오른쪽 단추로 클릭하고 컨텍스트 메뉴에서 자산 추가 를 선택합니다.
1. 자산 정보 대화 상자에서 체크아웃 아이콘을 클릭/탭하여 자산을 확인합니다. 체크아웃 아이콘은 클릭/탭한 후 체크인 아이콘으로 전환됩니다.

   ![체크 아웃할 자산 찾아보기](assets/browse_assets_to_checkout.png)

1. 다른 사용자가 사용할 수 있도록 자산을 체크 인하려면 자산 정보 대화 상자에서 체크인 아이콘을 클릭/탭합니다.

### Windows {#check-out-assets-on-windows}에서 자산 확인

이 앱을 사용하면 다른 사용자가 작업 중인 파일을 수정하지 못하도록 자산 파일을 체크 아웃할 수 있습니다.

1. 컨텍스트 메뉴에서 자산 탐색을 선택하여 탐색기를 엽니다.
1. Explorer에서 체크 아웃할 자산의 위치로 이동합니다.
1. 자산을 마우스 오른쪽 단추로 클릭하고 컨텍스트 메뉴에서 웹에서 열기 를 선택합니다.
1. 자산 정보 대화 상자에서 체크아웃 아이콘을 클릭/탭합니다. 체크아웃 아이콘은 체크인 아이콘으로 전환합니다.

   ![체크아웃 아이콘 전환](assets/checkout_icon_toggles.png)

1. Explorer에서 자산을 검토합니다. 자산 ![자산 잠금 아이콘](assets/do-not-localize/aemassets_icon_lockcheckout.png)의 잠금 아이콘은 자산을 체크 아웃했음을 나타냅니다.

   >[!NOTE]
   >
   >약간의 지연 후에 잠금 아이콘이 나타날 수 있습니다. [!DNL Experience Manager] 데스크탑 앱에서 자산을 캐시하여 빠른 액세스를 제공하므로 잠긴 상태를 업데이트하는 데 몇 분 정도 걸릴 수 있습니다.

1. 다른 사용자가 사용할 수 있도록 자산을 체크 인하려면 **자산 정보** 대화 상자에서 체크인 아이콘을 클릭/탭합니다.

### Finder 또는 Explorer를 사용하여 자산을 확인하고 웹 인터페이스 {#check-in-an-asset-using-finder-or-explorer-and-using-web-interface}을 사용합니다.

자산 편집을 완료하면 데스크탑 애플리케이션에 자산을 저장합니다. 컨텍스트 메뉴에서 **추가 자산 정보**&#x200B;를 선택하고 체크 인을 클릭합니다.

자산이 [!DNL Experience Manager] 서버에 업로드됩니다. 시스템 트레이 아이콘에서 **자산 상태 보기**&#x200B;를 선택하여 업로드 상태를 확인할 수 있습니다. 또는 [!DNL Experience Manager] 웹 인터페이스에서 자산을 체크 인할 수 있습니다. 체크 아웃된 자산을 클릭하거나 선택합니다. 도구 모음에서 체크인 아이콘 ![체크인 아이콘](assets/do-not-localize/aemassets_icon_checkin.png)을 클릭합니다.

변경 사항이 로컬로 저장되면 자산이 자동으로 [!DNL Experience Manager]에 업로드됩니다. 이 체크 인을 사용하면 자산을 다른 [!DNL Experience Manager] 사용자가 편집할 수 있습니다.

### 자산 및 폴더를 [!DNL Experience Manager] 서버에 벌크 업로드 {#bulkupload}

[!DNL Experience Manager] 데스크탑 앱을 사용하면 로컬 파일 디렉토리의 자산이 들어 있는 전체 폴더를 [!DNL Assets](으)로 업로드할 수 있습니다. 이 방법으로 폴더 내의 모든 자산은 한 번에 하나씩 업로드하지 않고 일괄 업로드됩니다.

1. Assets UI의 도구 모음에서 **만들기**&#x200B;를 클릭/탭하고 메뉴에서 **폴더 업로드**&#x200B;를 선택합니다.
1. 업로드할 폴더를 찾아 선택합니다.
1. 확인 을 클릭/탭합니다. 자산 상태 대화 상자에 업로드 상태가 표시됩니다.

   ![자산 상태 창에서 업로드 상태를 참조하십시오](assets/aem_desktopapp_bulkupload_status.png)

   자산 상태 창에서 업로드 상태를 참조하십시오

   >[!NOTE]
   >
   >해당 아이콘을 클릭/탭하여 업로드를 수동으로 일시 중지하거나 취소할 수 있습니다.

1. 폴더 업로드 후 대화 상자를 닫고 자산 UI로 이동합니다. 업로드된 폴더는 웹 인터페이스에 표시됩니다.

Adobe은 로컬 파일 시스템에서 네트워크 공유 영역으로 많은 파일 또는 중첩된 폴더를 복사하여 붙여넣거나 드래그하지 않는 것이 좋습니다. 기술 제한 사항으로 인해 앱이 업로드 프로세스를 제어할 수 없고 성능이 좋지 않습니다.

또는 Finder 또는 Explorer에서 [!DNL Experience Manager]에 업로드할 파일/폴더를 선택하고 시스템 클립보드에 복사하고, 네트워크 공유 영역의 대상 폴더로 이동한 다음 [!DNL Experience Manager] 데스크탑 앱 컨텍스트 메뉴에서 **자산 붙여넣기**&#x200B;를 선택합니다. 이 방법으로 [!DNL Experience Manager] 데스크탑 앱에서는 [!DNL Experience Manager] 웹 인터페이스에서 사용할 수 있는 **폴더 업로드** 옵션과 유사하게 붙여넣은 자산을 업로드하기 시작합니다.

>[!MORELIKETHIS]
>
>* [데스크탑 앱 응용 프로그램 문제 해결 [!DNL Experience Manager] 을 참조하십시오](troubleshoot-app-v1.md)

