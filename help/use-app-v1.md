---
title: ' [!DNL Experience Manager] 데스크톱 앱 버전 1.10을 사용합니다.'
description: Adobe Experience Manager 데스크톱 앱 버전 1.10을 사용하고 데스크탑에 있는 에셋으로 작업을 최적화하는 방법을 알아봅니다.
feature: Desktop App,Asset Management
exl-id: 2fdc1c8d-b822-4cca-ad06-bd875a00aa6d
translation-type: tm+mt
source-git-commit: 4616934e8923693106401da008e2510310d0742a
workflow-type: tm+mt
source-wordcount: '2377'
ht-degree: 0%

---

# [!DNL Experience Manager] 데스크탑 앱 v1.10 {#use-aem-desktop-app-v1x} 사용

앱을 사용하면 [!DNL Experience Manager] 내의 에셋은 로컬 데스크탑에서 쉽게 액세스할 수 있으며 모든 데스크탑 애플리케이션에서 사용할 수 있습니다. 자산은 Mac Finder 또는 Windows 탐색기에서 쉽게 표시되며, 데스크톱 응용 프로그램에서 열리며 로컬에서 변경될 수 있습니다. 변경 사항은 저장소에 새로 만든 버전으로 [!DNL Experience Manager]에 다시 저장됩니다.

이러한 통합을 통해 조직의 다양한 역할이 중앙에서 에셋을 관리하고 Creative Cloud 및 기타 애플리케이션에서 에셋을 액세스할 수 있으며 브랜딩을 비롯한 다양한 표준을 쉽게 준수할 수 있습니다.

[!DNL Experience Manager] 데스크탑 앱 v1을 사용하여 수행하는 주요 작업은 다음과 같습니다.

1. [서버와  [!DNL Experience Manager] 연결](#installandconnect)
1. [데스크탑에서 바로 에셋 열기](#openondesktop)
1. [데스크탑에서 에셋 편집 및 체크 아웃](#workonassets)
1. [자산 및 폴더 일괄 업로드](#bulkupload)

권장되는 다양한 방법과 그렇지 않은 방법은 앱](best-practices-for-v1.md) 사용에 대한 [우수 사례를 참조하십시오. 앱 사용 시 문제가 발생하는 경우 [문제 해결 [!DNL Experience Manager] desktop](troubleshoot-app-v1.md) 방법을 참조하십시오.

>[!NOTE]
>
>데스크탑 앱은 [!DNL Experience Manager] 6.1 릴리스에서 도입되었으며 [!DNL Experience Manager Assets Companion App]이라고 합니다.

## [!DNL Experience Manager] 크리에이티브 워크플로우의 데스크탑 앱 터치 포인트  {#aem-desktop-app-touch-points-in-the-creative-workflow}

[!DNL Experience Manager] 데스크탑 앱은 크리에이티브 워크플로우 [!DNL Assets]와 통합되어 있고 다음과 같은 터치 포인트를 제공합니다.

![[!DNL Experience Manager] 데스크탑 앱 터치 - 크리에이티브 워크플로우](assets/aem_desktopapp_workflow.png)

[!DNL Experience Manager] 데스크탑 앱 터치 - 크리에이티브 워크플로우

## 앱을 설치하고 [!DNL Experience Manager] 서버 {#installandconnect}에 연결

크리에이티브 에셋을 만들거나 편집하려면 먼저 데스크톱 응용 프로그램을 [!DNL Assets] 서버와 연결하여 저장소에 에셋을 다운로드하고 업로드합니다. 다음 작업을 수행합니다.

1. [앱을 설치합니다](#installapp).
1. [환경 설정 ](#inapppref) 및 연결 세부 사항을 설정합니다.
1. [서버에  [!DNL Experience Manager] ](#connect) 연결하고 에셋 저장소를 로컬 드라이브로 마운트합니다.
1. [데스크탑 ](#desktopactions) 동작  [!DNL Experience Manager] 서버를 활성화합니다.

[!DNL Experience Manager] 데스크탑 앱은 HTTPS 연결을 사용하여 서버에 연결하여  [!DNL Experience Manager] 안전하고 안정적으로 에셋을 전송합니다.

>[!NOTE]
>
>설치 및 구성 단계의 일부 또는 전체를 보려면 [!DNL Experience Manager] 관리자 또는 시스템 관리자의 도움이 필요할 수 있습니다.

### 응용 프로그램 {#installapp} 설치

[!DNL Experience Manager] 데스크탑 앱을 사용하려면 [!DNL Experience Manager] 서버 버전이 앱에서 지원되는지 확인하십시오. 운영 체제(Mac 또는 Windows)에 적합한 설치 파일(바이너리)을 다운로드하고 앱을 설치합니다.

네트워크 및 시스템 환경 설정에 따라 자세한 구성이 필요할 수 있습니다. 자세한 내용은 [설치 및 구성 [!DNL Experience Manager] 데스크탑 앱](install-configure-app-v1.md)을 참조하십시오.

1. [[!DNL Experience Manager] 데스크탑 앱 v1.10 다운로드 페이지](/help/release-notes-of-v1.md)로 이동하여 운영 체제에 적합한 바이너리를 다운로드합니다.
1. 다운로드한 설치 파일을 실행하고 화면의 지침에 따라 앱을 설치합니다.

   >[!NOTE]
   >
   >한 번에 하나의 [!DNL Experience Manager] 데스크탑 앱 인스턴스만 설치하고 활성화할 수 있습니다.

### 인앱 옵션 및 환경 설정 {#inapppref} 이해

응용 프로그램에서는 [!DNL Experience Manager] 서버에 연결 및 연결을 해제하고, 업로드 상태를 보고, 로컬 캐시를 관리하는 등의 설정을 허용합니다. 기본 설정은 응용 프로그램의 일반 사용자에게 작동합니다. 설정을 수정하여 응용 프로그램에서 더 많은 정보를 얻고 [!DNL Experience Manager] 서버와의 통합에서 벗어날 수 있습니다. 다양한 설정에 대해서는 아래에 자세히 설명합니다.

**자산** 탐색저장소가 마운트된 로컬  [!DNL Assets] 드라이브를 엽니다. 즉, 로컬 시스템에서 사용 가능한 에셋을 살펴보십시오.

**자산** 상태 보기변경된 자산을 업로드하거나 새 자산을  [!DNL Assets] 저장소에 추가하면 애플리케이션이 백그라운드에서 자산을 업로드합니다. 백그라운드 업로드를 사용하면 업로드가 끝날 때까지 기다릴 필요 없이, 특히 크기가 큰 자산에 대해 매끄러운 작업을 수행할 수 있습니다. 변경 내용을 로컬에 저장하고 잊어버릴 수 있습니다. 사용 가능한 대역폭에 따라 응용 프로그램에서 이러한 에셋을 서버로 보내는 데 시간이 다소 소요됩니다. 몇 가지 기본 정보와 함께 업로드 상태를 확인할 수 있습니다.

**옵션** 시스템 시작 시 응용 프로그램을 시작하는 설정에 액세스하려면 데스크탑 앱 트레이의 옵션을 클릭합니다.앱을 실행할  [!DNL Experience Manager] 때 서버에 연결하는 방법;를 클릭하여 마운트한 후 사용할 수 있는 로컬 드라이브 문자 [!DNL Assets] 를 변경합니다.

**고급 >** 캐시 관리로컬 캐싱에 사용할 수 있는 디스크 공간의 양을 제어할 수 있습니다. [!DNL Assets] 서버의 아티팩트가 보다 원활한 경험을 위해 로컬에 캐시됩니다. 요구 사항에 맞게 기본값을 변경할 수 있습니다. 또한 캐시를 지우면 모든 에셋을 새로 가져올 수 있습니다. 캐시를 지우면 저장하지 않은 변경 사항이 유지됩니다. [!DNL Experience Manager] 서버에 체크 인되지 않은 모든 자산은 유지되며 삭제되지 않습니다.

### [!DNL Experience Manager] 서버 {#connect}에 연결

앱은 Mac 및 Windows에서 프록시 구성을 지원합니다. 앱이 시작될 때 구성을 읽습니다. 프록시 설정을 수정하는 경우 변경 사항이 적용되도록 앱을 다시 시작합니다.

>[!NOTE]
>
>프록시 설정을 수정하는 경우 변경 사항이 적용되도록 앱을 다시 시작합니다. 그렇지 않으면 앱이 이전에 구성한 프록시 서버를 계속 사용합니다.

1. [!DNL Experience Manager] 데스크탑 앱을 실행합니다. [!DNL Experience Manager] 인스턴스를 앱과 매핑하려면 `https://[aem-server-url]:[port]` 형식으로 [!DNL Experience Manager] 서버를 지정합니다.

   ![Mac에서 인증 및  [!DNL Experience Manager] 서버 URL 제공](assets/aem_desktop_app_server_url.png)

1. 로그인 화면에서 인스턴스의 사용자 이름과 암호를 지정합니다. 대체 [!DNL Experience Manager] 인스턴스를 지정하려면 **[!UICONTROL Alternate Login URL]** 옵션을 선택합니다.

   ![ [!DNL Experience Manager] 데스크탑 앱 [!DNL Experience Manager] 의 로그인 화면에서 서버 자격 증명 제공](assets/login_screen_v1.png)

### [!DNL Experience Manager] 웹 인터페이스 {#desktopactions}에서 데스크톱 작업 활성화

자산 사용자 인터페이스 내에서 자산 위치를 탐색하거나 체크 아웃하고 데스크톱 응용 프로그램에서 편집할 자산을 열 수 있습니다. 이러한 옵션은 데스크톱 작업이라고 하며 기본적으로 활성화되지 않습니다. 다음 단계에 따라 활성화합니다.

1. 자산 인터페이스에서 도구 모음의 오른쪽 상단에 있는 사용자 아이콘을 클릭/탭합니다.
1. **[!UICONTROL My Preferences]**&#x200B;을 클릭하여 **[!UICONTROL Preferences]** 대화 상자를 표시합니다.

   ![[!DNL Experience Manager] 사용자 환경 설정을 사용한 인터페이스](assets/aem_ui_user_preferences.png)

1. [사용자 환경 설정] 대화 상자에서 **[!UICONTROL Show Desktop Actions For Assets]**&#x200B;을 선택합니다. 클릭 **[!UICONTROL Accept]**.

   ![데스크톱  [!UICONTROL Show Desktop Actions For Assets] 작업을 활성화하려면 확인](assets/enable_desktop_actions.png)

   *그림:데스크톱 작업을 활성화하려면 자산에 대한 데스크톱 작업 표시를 선택합니다.*

## 데스크탑에서 자산 액세스 및 열기 {#openondesktop}

**열기**&#x200B;를 클릭하여 로컬 컴퓨터에서 자산을 열면 앱이 자산을 내부 캐시에 다운로드합니다. 앱은 다운로드한 자산의 파일 형식과 관련된 기본 데스크톱 응용 프로그램을 실행합니다.

Mac의 경우 컨텍스트 메뉴에서 **열기**&#x200B;를 선택하여 [!DNL Experience Manager] 데스크탑 앱을 통해 자산을 엽니다. Windows의 경우 컨텍스트 메뉴에서 웹에서 열기를 선택하여 자산을 엽니다. 자산 상태 창에서 ![데스크탑에서 열기 아이콘](assets/do-not-localize/aemassets_icon_openondesktop.png)을 클릭/탭하여 자산을 엽니다.

Adobe InDesign(INDD) 파일의 경우 컨텍스트 메뉴에서 **[!UICONTROL Open]**&#x200B;을 선택합니다. 이 옵션을 클릭하면 앱이 연결된 에셋을 로컬 파일 시스템에 다운로드한 다음 Adobe InDesign에서 INDD 파일을 엽니다. 이 방법을 사용하면 INDD 파일을 편집할 때 필요한 에셋을 로컬에서 사용할 수 있습니다.

![ [!DNL Experience Manager] 데스크탑 앱을 사용하여 자산에 액세스하고 여는 컨텍스트 메뉴 옵션](assets/aem_desktopapp_mac_context_menu.png)

*그림:컨텍스트 메뉴 옵션을 사용하여  [!DNL Experience Manager] 데스크톱 앱을 사용하여 자산에 액세스하고 열 수 있습니다.*

>[!NOTE]
>
>Windows의 경우 [기본 Windows 7 설정](https://support.microsoft.com/en-us/kb/2668751) 데스크톱 앱이 50MB보다 큰 자산을 처리하지 못하게 합니다.[!DNL Experience Manager]

<!-- TBD: The above note is for Windows 7 which is not supported by the app anymore. Remove it later.
-->

>[!NOTE]
>
>Mac의 [Finder 보기 옵션]으로 이동하고 마운트된 [!DNL Assets] 폴더에 대해 **항목 정보 표시**, **항목 미리 보기 표시** 및 **미리 보기 열 표시** 옵션을 비활성화하는 것이 좋습니다. 성능이 개선됩니다.

### [!DNL Experience Manager] 인터페이스 {#additional-options-in-aem-assets}의 추가 옵션

[!DNL Assets] 리포지토리를 로컬 드라이브에 매핑한 후 매핑된 자산 및 폴더에 대해 추가 아이콘과 폴더 업로드 기능을 사용하여 표시할 수 있습니다.

1. [!DNL Assets] 인터페이스를 열고 포인터를 폴더 또는 자산 위로 가져가면 데스크톱 작업이 카드 보기에서 빠른 작업으로 표시됩니다.

   ![자산 UI에서 빠른 작업 메뉴를 열어 데스크톱 작업을 봅니다.](assets/desktop_actions_in_card_view.png)

   *그림:자산 UI에서 빠른 작업 메뉴를 열어 데스크톱 작업을 봅니다.*

   이러한 데스크톱 작업은 자산을 선택한 후 또는 자산 페이지의 도구 모음에서 **데스크톱 작업** 옵션을 클릭할 때도 사용할 수 있습니다.

1. 특정 파일 확장명과 연결된 데스크톱 응용 프로그램에서 자산을 열려면 **바탕 화면에서 열기** 빠른 작업 ![바탕 화면에서 열기 아이콘](assets/do-not-localize/aemassets_icon_openondesktop.png)을 클릭합니다.

   또는 도구 모음의 **데스크톱 작업** 메뉴에서 **열기**&#x200B;를 선택합니다.

로컬 파일 시스템에서 특정 자산을 찾으려면 **표시** 빠른 작업 ![표시 아이콘](assets/do-not-localize/aemassets_reveal_icon.png)을 클릭합니다. 또는 도구 모음의 **데스크톱 작업** 메뉴에서 **표시**&#x200B;를 선택합니다.

## 자산 상태 {#understand-the-asset-statuses} 이해

| ![Windows 기본 앱 아이콘](assets/do-not-localize/win_default.png) | 앱이 서버에 연결되고 모든 자산이 동기화됩니다. |
--- |--- |
| ![Windows 비활성화 아이콘](assets/do-not-localize/win_disabled.png) | 앱이 실행되었지만 서버와 연결되지 않았습니다. 일부 자산은 동기화를 보류 중일 수 있습니다. |
| ![Windows 파일 동기화 아이콘](assets/do-not-localize/win_sync.png) | 자산을 동기화하는 중입니다. 파일이 업로드되거나 다운로드되고 있습니다. 정확한 상태를 보고 자산 상태 창에서 전송을 일시 중지할 수 있습니다. |
| ![Windows 다시 연결 아이콘](assets/do-not-localize/win_refresh.png) | 앱이 다시 연결하려고 합니다. 네트워크 문제로 인해 연결을 끊을 수 있습니다. |

## 에셋 작업 {#workonassets}

### [!DNL Experience Manager] 웹 인터페이스 {#check-out-assets-from-the-aem-web-interface}에서 자산 확인

[!DNL Assets] 편집할 에셋을 확인하고 변경을 완료한 후 다시 로그인할 수 있습니다. 자산을 체크 아웃한 후에는 에셋을 편집, 주석 추가, 게시, 이동 또는 삭제할 수만 있습니다. 자산을 체크 아웃하면 자산이 잠기고 다른 사용자가 이러한 작업을 수행할 수 없습니다. 자산을 체크 아웃/체크 인하려면 자산에 대해 쓰기 액세스 권한이 필요합니다.

[!DNL Experience Manager] 웹 인터페이스에서 자산을 체크 아웃하는 방법은 두 가지가 있습니다. 첫 번째 방법에 대한 자세한 내용은 자산 UI](https://experienceleague.adobe.com/docs/experience-manager-65/assets/managing/check-out-and-submit-assets.html)에서 [체크 인 및 체크 아웃 파일을 참조하십시오. [!DNL Experience Manager] 데스크탑 앱이 설치될 때 자산을 체크 아웃하고 여는 두 번째 방법은 다음 단계를 수행합니다.

1. [!DNL Assets] 인터페이스를 열고 포인터를 폴더 또는 자산 위로 가져가면 데스크톱 작업이 카드 보기에서 빠른 작업으로 표시됩니다.

   ![카드 보기의 속성 옵션](assets/desktop_actions_in_card_view.png)

   이러한 데스크톱 작업은 자산을 선택한 후 도구 모음에서 데스크톱 작업 아이콘을 클릭/탭하거나 자산 페이지의 도구 모음에서 사용할 수도 있습니다.

1. 자산을 열려면 데스크탑에서 열기 빠른 작업 ![데스크탑에서 열기 아이콘](assets/do-not-localize/aemassets_icon_openondesktop.png)을 클릭/탭합니다.

   또는 도구 모음의 [데스크톱 작업] 메뉴에서 [열기]를 선택합니다.

   >[!NOTE]
   >
   >방금 열었지만 체크 아웃되지 않은 파일을 편집하면 다른 사용자는 자신이 에셋을 업데이트하고 있음을 알 수 없습니다.

1. Adobe Creative Cloud 응용 프로그램에서 편집할 에셋을 열려면 데스크탑 편집 빠른 작업 ![데스크탑 편집 아이콘](assets/do-not-localize/aemassets_icon_editdesktop.png)을 클릭/탭합니다. 편집할 에셋도 체크 아웃됩니다. 편집을 마친 후 자산을 체크 인하여 [!DNL Assets]의 변경 내용을 업데이트합니다.

   또는 도구 모음의 [데스크톱 작업] 메뉴에서 [편집]을 선택합니다.

1. [열기] 메뉴 옵션을 선택합니다. 선택한 자산이 미리 보기 모드에서 열립니다.
1. 자산을 편집하려면 편집 옵션을 선택합니다. 자산은 편집 모드에서 열립니다.

### Mac OS {#check-out-assets-on-mac}의 Finder에서 자산 확인

이 앱을 사용하면 다른 사용자가 작업 중인 파일을 수정하지 못하도록 에셋 파일을 체크 아웃할 수 있습니다.

1. Mac 컨텍스트 메뉴에서 AEM Assets 폴더 열기 옵션을 선택하여 Finder를 엽니다.

   ![ [!DNL Experience Manager] 데스크탑 앱을 사용하여 자산에 액세스하고 여는 컨텍스트 메뉴 옵션](assets/aem_desktopapp_mac_context_menu.png)

   *그림:컨텍스트 메뉴 옵션을 사용하여  [!DNL Experience Manager] 데스크톱 앱을 사용하여 자산에 액세스하고 열 수 있습니다.*

1. 체크 아웃할 자산으로 이동합니다.
1. 자산을 마우스 오른쪽 단추로 클릭하고 컨텍스트 메뉴에서 추가 자산 정보를 선택합니다.
1. 자산 정보 대화 상자에서 체크아웃 아이콘을 클릭/탭하여 자산을 확인합니다. 체크아웃 아이콘을 클릭/탭하면 체크 인 아이콘으로 전환됩니다.

   ![체크아웃할 에셋 찾아보기](assets/browse_assets_to_checkout.png)

1. 다른 사용자가 사용할 수 있도록 자산을 체크 인하려면 [자산 정보] 대화 상자에서 체크 인 아이콘을 클릭/탭합니다.

### Windows {#check-out-assets-on-windows}에서 자산 확인

이 앱을 사용하면 다른 사용자가 작업 중인 파일을 수정하지 못하도록 에셋 파일을 체크 아웃할 수 있습니다.

1. 컨텍스트 메뉴에서 자산 탐색을 선택하여 탐색기를 엽니다.
1. 탐색기에서 체크 아웃할 자산의 위치로 이동합니다.
1. 자산을 마우스 오른쪽 단추로 클릭하고 컨텍스트 메뉴에서 웹에서 열기를 선택합니다.
1. 자산 정보 대화 상자에서 체크아웃 아이콘을 클릭/탭합니다. 체크 아웃 아이콘은 체크 인 아이콘으로 전환됩니다.

   ![체크아웃 아이콘 전환](assets/checkout_icon_toggles.png)

1. 탐색기에서 자산을 검토합니다. 자산 ![자산 잠금 아이콘](assets/do-not-localize/aemassets_icon_lockcheckout.png)의 잠금 아이콘은 자산을 체크 아웃했음을 나타냅니다.

   >[!NOTE]
   >
   >약간의 지연 후에 잠금 아이콘이 나타날 수 있습니다. [!DNL Experience Manager] 데스크톱 앱은 빠른 액세스를 위해 자산을 캐시하므로 잠긴 상태를 업데이트하는 데 몇 분 정도 걸릴 수 있습니다.

1. 다른 사용자가 사용할 수 있도록 자산을 체크 인하려면 **자산 정보** 대화 상자에서 체크 인 아이콘을 클릭/탭합니다.

### Finder 또는 탐색기를 사용하여 자산을 체크 인하고 웹 인터페이스 {#check-in-an-asset-using-finder-or-explorer-and-using-web-interface} 사용

자산 편집을 마쳤으면 데스크톱 응용 프로그램에 자산을 저장합니다. 컨텍스트 메뉴에서 **추가 자산 정보**&#x200B;를 선택하고 체크 인을 클릭합니다.

에셋이 [!DNL Experience Manager] 서버에 업로드됩니다. 선택적으로 시스템 트레이 아이콘에서 **자산 상태 보기**&#x200B;를 선택하여 업로드 상태를 확인할 수 있습니다. 또는 [!DNL Experience Manager] 웹 인터페이스에서 자산을 체크 인할 수 있습니다. 체크 아웃된 자산을 클릭하거나 선택합니다. 도구 모음에서 체크 인 아이콘 ![체크 인 아이콘](assets/do-not-localize/aemassets_icon_checkin.png)을 클릭합니다.

변경 내용이 로컬에 저장된 후 에셋이 자동으로 [!DNL Experience Manager]에 업로드됩니다. 체크 인을 사용하면 에셋을 다른 [!DNL Experience Manager] 사용자가 편집할 수 있습니다.

### 자산 및 폴더를 [!DNL Experience Manager] 서버 {#bulkupload}에 일괄 업로드

[!DNL Experience Manager] 데스크탑 앱을 사용하면 로컬 파일 디렉토리의 에셋이 포함된 전체 폴더를 [!DNL Assets]에 업로드할 수 있습니다. 이렇게 하면 한 번에 하나씩 업로드하지 않아도 폴더 내의 모든 에셋이 일괄 업로드됩니다.

1. 자산 UI의 도구 모음에서 **만들기**&#x200B;를 클릭/탭하고 메뉴에서 **폴더 업로드**&#x200B;를 선택합니다.
1. 업로드할 폴더를 찾아 선택합니다.
1. 확인을 클릭/탭합니다. 자산 상태 대화 상자에 업로드 상태가 표시됩니다.

   ![자산 상태 창에서 업로드 상태 보기](assets/aem_desktopapp_bulkupload_status.png)

   자산 상태 창에서 업로드 상태 보기

   >[!NOTE]
   >
   >해당 아이콘을 클릭/탭하여 업로드를 수동으로 일시 중지하거나 취소할 수 있습니다.

1. 폴더 업로드 후 대화 상자를 닫고 자산 UI로 이동합니다. 업로드된 폴더가 웹 인터페이스에 표시됩니다.

Adobe에서는 로컬 파일 시스템에서 네트워크 공유 영역으로 많은 수의 파일이나 중첩된 폴더를 복사하여 붙여넣거나 드래그하는 것이 좋습니다. 기술적 제한으로 인해 앱이 업로드 프로세스를 제어할 수 없고 성능이 좋지 않습니다.

또는 Finder 또는 탐색기에서 [!DNL Experience Manager]에 업로드할 파일/폴더를 선택하고, 시스템 클립보드로 복사하고, 네트워크 공유 영역의 대상 폴더로 이동하고 [!DNL Experience Manager] 데스크탑 앱 컨텍스트 메뉴에서 **자산 붙여넣기**&#x200B;를 선택합니다. 이렇게 하면 [!DNL Experience Manager] 데스크탑 앱이 [!DNL Experience Manager] 웹 인터페이스에서 사용할 수 있는 **폴더 업로드** 옵션과 유사한 붙여넣은 에셋을 업로드하기 시작합니다.

>[!MORELIKETHIS]
>
>* [데스크탑  [!DNL Experience Manager] 앱 애플리케이션 문제 해결](troubleshoot-app-v1.md)

