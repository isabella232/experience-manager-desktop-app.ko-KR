---
title: 사용 [!DNL Experience Manager] 데스크탑 앱
description: 사용 [!DNL Adobe Experience Manager] 데스크탑 앱, [!DNL Adobe Experience Manager] DAM 자산은 Win 또는 Mac 데스크탑에서 바로 사용할 수 있으며 다른 애플리케이션에서 사용할 수 있습니다.
mini-toc-levels: 1
feature: Desktop App,Asset Management
exl-id: fa19d819-231a-4a01-bfd2-6bba6fec2f18
source-git-commit: ca04b64e1ebfee4b677fcc5ef84b0e8fd9950d17
workflow-type: tm+mt
source-wordcount: '4054'
ht-degree: 0%

---

# 사용 [!DNL Adobe Experience Manager] 데스크탑 앱 {#use-aem-desktop-app-v2}

를 사용하십시오 [!DNL Adobe Experience Manager] 데스크탑 앱으로 이동하여 [!DNL Adobe Experience Manager] 로컬 데스크탑의 DAM 저장소를 사용하고 모든 데스크탑 애플리케이션에서 이러한 자산을 사용합니다. 데스크탑 애플리케이션에서 자산을 열고 자산을 로컬로 편집할 수 있습니다. 변경 내용을 다시 업로드하십시오 [!DNL Experience Manager] 버전 제어를 사용하면 다른 사용자와 업데이트를 공유할 수 있습니다. 새 파일 및 폴더 계층 구조를 [!DNL Experience Manager], 폴더를 만들고 자산 또는 폴더를 [!DNL Experience Manager] DAM.

통합을 통해 조직에서 다양한 역할이 의 자산을 중앙에서 관리할 수 있습니다 [!DNL Experience Manager Assets] 및 를 사용하여 Windows 또는 Mac OS의 기본 애플리케이션에서 로컬 데스크탑의 자산에 액세스할 수 있습니다.

로그아웃한 후 또는 처음으로 애플리케이션을 열 때는 의 URL을 입력합니다 [!DNL Experience Manager] 서버 형식 `https://[aem-server-url]:[port]/`. 그런 다음 [!UICONTROL Connect] 선택 사항입니다. 앱에 서버를 연결하는 자격 증명을 제공합니다.

를 사용하여 수행하는 주요 작업 [!DNL Adobe Experience Manager] 데스크탑 앱은

![을 사용하여 수행할 수 있는 워크플로우 및 작업 [!DNL Experience Manager] 데스크탑 앱](assets/aem_desktop_app_usecases_v2.png "을 사용하여 수행할 수 있는 워크플로우 및 작업 [!DNL Adobe Experience Manager] 데스크탑 앱")
다운로드 [이](assets/aem_desktop_app_usecases_print.pdf) 인쇄용 PDF 파일.

## 데스크탑 앱 작동 방식 {#how-app-works2}

애플리케이션을 사용하기 전에 [앱 작동 방식](release-notes.md#how-app-works). 또한 다음 용어를 숙지하십시오.

* **[!UICONTROL Desktop Actions]**: Assets 웹 인터페이스에서 브라우저 내에서 자산 위치를 탐색하거나 체크 아웃하고 기본 데스크탑 애플리케이션에서 편집할 자산을 열 수 있습니다. 이러한 작업은 웹 인터페이스에서 사용할 수 있으며 데스크탑 앱 기능을 사용합니다. 자세한 내용은 [데스크톱 작업을 활성화하는 방법](using.md#desktopactions-v2).

* 파일 상태는 **[!UICONTROL Cloud Only]**: 이러한 자산은 로컬 시스템에서 다운로드되지 않으며 [!DNL Experience Manager] 서버만 해당.

* 파일 상태는 **[!UICONTROL Available locally]**: 자산은 그대로 다운로드되어 로컬 시스템에서 사용할 수 있습니다. 자산은 변경되지 않습니다.

* 파일 상태는 **[!UICONTROL Edited locally]**: 이러한 자산은 로컬에서 수정되며, 변경 내용은 업로드된 다음에 유지됩니다 [!DNL Experience Manager] server. 업로드하면 상태가 [!UICONTROL Available locally]. 자세한 내용은 [자산 편집](using.md#edit-assets-upload-updated-assets).

* 파일 상태는 **[!UICONTROL Editing conflict]**: 사용자와 다른 사용자가 자산을 동시에 수정하는 경우, 앱은 편집 충돌이 발생했음을 나타냅니다. 또한 앱에서는 변경 사항을 유지하거나 취소할 수 있는 옵션을 제공합니다. 자세한 내용은 [편집 충돌을 방지하는 방법](using.md#adv-workflow-collaborate-avoid-conflicts).

* 파일 상태는 **[!UICONTROL Modified remotely]**: 앱은 다운로드한 자산이 [!DNL Experience Manager] server. 또한 앱에서는 최신 버전을 다운로드하고 로컬 복사본을 업데이트하는 선택 사항을 제공합니다. 자세한 내용은 [편집 충돌을 방지하는 방법](using.md#adv-workflow-collaborate-avoid-conflicts).

* **[!UICONTROL Check-out]**: 파일을 편집하거나 파일을 편집하려면 상태를 전환하여 체크 아웃합니다. 앱의 자산에 잠금 아이콘을 추가하고 [!DNL Experience Manager] 웹 인터페이스. 잠금 아이콘은 다른 사용자에게 동일한 자산을 동시에 편집하면 편집 충돌이 발생하지 않도록 합니다.

* **[!UICONTROL Check-in]**: 편집 충돌을 일으키지 않고 다른 사용자가 편집할 수 있도록 자산을 안전한 것으로 표시합니다. 변경 사항을 업로드하면 잠금 아이콘이 자동으로 제거됩니다. 체크인 상태를 전환하면 변경 사항을 업로드하지 않고 수동으로 체크 인하지 않는 것이 좋지만 잠금 아이콘도 제거됩니다. 변경 사항을 취소한 경우 수동으로 체크 인을 전환합니다.

* **[!UICONTROL Open]** 작업: 자산을 열어 기본 애플리케이션에서 미리 보기하면 됩니다. 자산을 체크 아웃하지 않으므로 이 작업을 사용하여 자산을 편집하지 않는 것이 좋습니다. 이렇게 하면 자산을 편집할 수 있고 다른 사용자가 편집을 할 수 있어 편집 충돌이 발생합니다.

* **[!UICONTROL Edit]** 작업: 작업을 사용하여 이미지를 수정합니다. 클릭 [!UICONTROL Edit] 작업은 자동으로 자산을 체크 아웃하고 자산에 잠금 아이콘을 추가합니다. 편집 을 클릭한 후, 자산을 편집하지 않으려면 을 클릭합니다 [!UICONTROL Toggle check-in]. 에서 자산을 삭제, 이름 변경 또는 이동하려면 다음을 수행하십시오 [!DNL Experience Manager] DAM 폴더 계층 구조, [!DNL Experience Manager] 편집 작업이 아닌 웹 인터페이스 작업.

* **[!UICONTROL Download]** 작업: 로컬 시스템에 자산을 다운로드합니다. 지금 자산을 다운로드하고 나중에 편집할 수 있습니다. 오프라인으로 작업하고 나중에 변경 내용을 업로드합니다. 자산은 파일 시스템의 캐시 폴더에 다운로드됩니다.

* **[!UICONTROL Reveal File]** 또는 **[!UICONTROL Reveal Folder]** 작업: 자산이 로컬 캐시 폴더로 다운로드되는 동안 앱은 로컬 네트워크 드라이브를 모방하고 각 자산에 대한 로컬 경로를 제공합니다. 이 경로를 알아보려면 앱에서 적절한 표시 옵션을 사용하십시오. Creative Cloud 애플리케이션에 자산을 배치하는 데 필요한 작업을 표시합니다. 자세한 내용은 [자산 배치](using.md#place-assets-in-native-documents).

* **[!UICONTROL Open In Web]** 작업: 에서 자산을 보려면 [!DNL Experience Manager] 웹 인터페이스에서 엽니다. 다음에서 더 많은 워크플로우를 시작할 수 있습니다. [!DNL Experience Manager] 메타데이터 또는 자산 검색 업데이트와 같은 인터페이스.

* **[!UICONTROL Delete]** 작업: 에서 자산 삭제 [!DNL Experience Manager] DAM 저장소. 작업을 수행하면 Experience Manager 서버에서 자산의 원본 사본이 삭제됩니다. 로컬 자산에 대한 수정 사항만 취소하려면 다음을 참조하십시오 [변경 내용 삭제](using.md#edit-assets-upload-updated-assets).

* **[!UICONTROL Upload Changes]**: 데스크탑 앱에서는 명시적으로 업로드하는 경우에만 업데이트된 자산을 업로드합니다 [!DNL Experience Manager] server. 편집 내용을 저장하면 변경 사항이 로컬 시스템에만 저장됩니다. 업로드하면 자산이 자동으로 체크 인되고 잠금 아이콘이 제거됩니다. 자세한 내용은 [자산 편집](using.md#edit-assets-upload-updated-assets).

## 에서 데스크톱 작업 활성화 [!DNL Experience Manager] 웹 인터페이스 {#desktopactions-v2}

에서 [!DNL Assets] 브라우저의 사용자 인터페이스에서 자산 위치를 탐색하거나 체크 아웃하고 데스크탑 애플리케이션에서 편집할 자산을 열 수 있습니다. 이러한 옵션을 라고 합니다 [!UICONTROL Desktop Actions] 기본적으로 활성화되어 있지 않습니다. 활성화하려면 다음 단계를 수행하십시오.

1. 에서 [!DNL Assets] 콘솔에서 **[!UICONTROL User]** 아이콘 을 클릭하여 제품에서 사용할 수 있습니다.
1. 클릭 **[!UICONTROL My Preferences]** 를 **[!UICONTROL Preferences]** 대화 상자.

1. 에서 [!UICONTROL User Preferences] 대화 상자, 선택 **[!UICONTROL Show Desktop Actions For Assets]**&#x200B;를 클릭한 다음 **[!UICONTROL Accept]**.


   ![자산에 대한 데스크톱 작업 표시 를 선택하여 데스크톱 작업을 활성화합니다](assets/enable_desktop_actions.png)

   *그림: 선택 [!UICONTROL Show Desktop Actions For Assets] 데스크톱 작업을 활성화하려면*

## 자산 찾아보기, 검색 및 미리 보기 {#browse-search-preview-assets}

에서 사용할 수 있는 자산을 찾아보고, 검색하고, 미리 볼 수 있습니다 [!DNL Experience Manager] 리포지토리(모두 데스크탑 애플리케이션 내에서)입니다. 앱에서 다음 작업을 시도하십시오.

1. 모든 자산의 작은 축소판과 함께 폴더를 찾아 폴더에서 사용할 수 있는 자산의 몇 가지 기본 정보를 확인하십시오.

   ![DAM 파일 및 폴더 찾아보기](assets/browse_folder_da2.png "DAM 파일 및 폴더 찾아보기")

1. 자세한 정보와 개별 자산의 더 큰 축소판을 보려면 파일 이름을 클릭합니다.

   ![자산 및 작업의 더 큰 미리 보기 참조](assets/large_preview_actions_da2.png "자산 및 작업의 더 큰 미리 보기 참조")

1. 클릭 **[!UICONTROL Open]** 또는 **[!UICONTROL Edit]** 로컬에서 파일을 다운로드하고 각 기본 애플리케이션에서 보거나 편집할 수 있습니다.
1. 키워드를 사용하여 검색하여 [!DNL Experience Manager] 저장소. 사용 `?` 및 `*` 와일드카드로 사용할 수 있습니다. 이러한 와일드카드는 각각 단일 문자 또는 여러 문자를 대체합니다. 필요에 따라 결과를 필터링하고 정렬합니다.

   ![별표 와일드카드를 사용한 샘플 검색](assets/search_wildcard_da2.png "별표 와일드카드를 사용한 샘플 검색")

   ![별표 와일드카드를 사용한 다른 샘플 검색](assets/search_wildcard2_da2.png "별표 와일드카드의 다른 배치를 갖는 다른 샘플 검색")

>[!NOTE]
>
>앱은 자산의 제목이나 파일 이름뿐만 아니라 여러 메타데이터 필드에서 검색 기준을 일치시켜 자산을 표시합니다.

## 에셋 다운로드 {#download-assets}

로컬 파일 시스템에서 자산을 다운로드할 수 있습니다. 앱에서 자산을 가져옵니다. [!DNL Experience Manager] 서버와 로컬 파일 시스템에 동일한 복사본을 저장합니다.

클릭 ![추가 옵션 아이콘](assets/do-not-localize/more2_da2.png) 옵션을 선택하고 ![다운로드 아이콘](assets/do-not-localize/download_cloud_da2.png) 다운로드

![자산에 대한 다운로드 옵션](assets/download_option_da2.png "자산에 대한 다운로드 옵션")

>[!NOTE]
>
>대용량 파일 또는 여러 파일을 다운로드하거나 업로드할 때 자산 및 폴더에서 작업이 비활성화됩니다. 작업은 다운로드나 업로드가 완료되면 사용할 수 있습니다.

큐 크기가 크거나 일부 네트워크 문제가 발생하는 경우 여러 자산을 다운로드하면 성능이 저하될 수 있습니다. 또한 폴더를 다운로드할 때 자신도 모르게 다운로드할 많은 자산을 큐에 올릴 수 있습니다. 오랜 대기 시간을 방지하기 위해 앱에서는 한 번에 다운로드되는 자산 수를 제한합니다. 구성 방법을 알아보려면 [환경 설정 지정](install-upgrade.md#set-preferences). 이 제한보다 낮더라도, 때때로 앱은 분명히 큰 폴더를 다운로드하기 전에 확인을 시도할 수 있습니다.

![상대적으로 많은 수의 자산이 다운로드되었는지 앱에서 확인합니다](assets/download_confirmation_da2.png "상대적으로 많은 수의 자산이 다운로드되었는지 앱에서 확인합니다")

폴더를 선택하고 다운로드하면 이 애플리케이션은 의 폴더에 직접 저장된 자산만 다운로드합니다 [!DNL Experience Manager]. 하위 폴더에서 자산을 자동으로 다운로드하지 않습니다.

## 데스크탑에서 자산 열기 {#openondesktop-v2}

기본 애플리케이션에서 볼 원격 자산을 열 수 있습니다. 자산은 로컬 폴더에 다운로드되고 파일 형식과 관련된 기본 애플리케이션에서 실행됩니다. 기본 애플리케이션을 변경하여 Mac 또는 Windows에서 특정 파일 유형(확장)을 열 수 있습니다.

클릭 **[!UICONTROL Open]** 를 클릭합니다. 자산이 로컬로 다운로드되고 기본 애플리케이션에서 열립니다. 상태 표시줄에서 큰 자산의 다운로드 진행 및 전송 속도를 확인합니다.

<!-- ![Download progress bar for large-sized assets](assets/download_status_bar_da2.png "Download progress bar for large-sized assets")
-->

>[!NOTE]
>
>예상 변경 사항이 앱에 반영되지 않으면 새로 고침 아이콘을 클릭합니다 ![새로 고침 아이콘](assets/do-not-localize/refresh.png) 또는 앱 인터페이스를 마우스 오른쪽 버튼으로 클릭하고 **[!UICONTROL Refresh]**. 더 큰 다운로드나 업로드가 진행 중인 동안에는 작업을 사용할 수 없습니다.

자산의 로컬 다운로드 폴더를 열려면 ![추가 작업 아이콘](assets/do-not-localize/more2_da2.png) 을(를) 클릭합니다. ![표시 아이콘](assets/do-not-localize/reveal_action2_da2.png) **[!UICONTROL Reveal File]** 작업.

## 자산을 기본 문서에 사용하거나 배치합니다 {#place-assets-in-native-documents}

자산을 기본 문서에 배치할 때 Windows 탐색기 또는 Mac Finder의 파일에 액세스하는 경우가 있습니다. 로컬에서 다운로드한 파일의 파일 시스템 위치로 이동하려면 ![표시 아이콘](assets/do-not-localize/reveal_action2_da2.png) **[!UICONTROL Reveal File]** 선택 사항입니다.

![자산에 대한 파일 작업 표시](assets/revealfile_action_da2.png "자산에 대한 파일 작업 표시")

클릭 **[!UICONTROL Reveal File]**, 또는 **[!UICONTROL Reveal Folder]** 폴더에서 로컬 시스템에서 미리 선택된 파일이나 폴더로 Windows 탐색기 또는 Mac Finder를 엽니다. 이 옵션은 [!DNL Experience Manager] 로컬 파일 배치 또는 연결을 지원하는 기본 응용 프로그램의 파일입니다. Adobe InDesign에 파일을 배치하는 방법을 보려면 [그래픽 배치](https://helpx.adobe.com/indesign/using/placing-graphics.html).

다음 **[!UICONTROL Reveal File]** 작업은 로컬로 사용할 수 있는 자산만 표시하는 로컬 네트워크 공유를 엽니다. 이 공유에는 앱을 사용하여 표시하거나 다운로드하거나 열리거나 편집한 자산이 표시됩니다. 로컬 네트워크 공유에서 변경 내용을 업로드하지 않습니다 [!DNL Experience Manager]. 변경 사항을 업로드하려면 을 명시적으로 사용합니다 **[!UICONTROL Upload Changes]** 또는 **[!UICONTROL Upload]** 앱의 작업.

>[!NOTE]
>
>이전 버전과의 호환성을 위해 [!DNL Experience Manager] 데스크탑 앱 v1.x에서 표시되는 파일은 로컬 네트워크 공유에서 제공되며 로컬에서 사용할 수 있는 파일만 노출합니다. 나타난 파일의 데스크탑 경로는 앱 v1.x에서 만든 경로와 동일합니다.

>[!CAUTION]
>
>사용 안 함 **[!UICONTROL Reveal File]** 기본 애플리케이션에서 자산을 편집하는 옵션입니다. 대신, **[!UICONTROL Edit]** 작업. 자세한 내용은 [고급 워크플로우: 동일한 파일에 대한 공동 작업 및 편집 충돌 방지](#adv-workflow-collaborate-avoid-conflicts).

## 자산 편집 및 업데이트된 자산 업로드 [!DNL Experience Manager] {#edit-assets-upload-updated-assets}

변경 작업을 수행할 때 편집할 자산을 열고 업데이트된 자산을 Experience ManagerEM 서버에 업로드합니다. 다른 사용자의 편집과 충돌을 방지하려면 앱을 사용하여 편집 세션을 시작합니다. 편집을 시작하기 전에 자산에 잠금 아이콘이 없는지 확인합니다. 즉, 다른 사용자가 자산을 편집하지 않습니다.

자산을 편집하려면 자산을 검색하거나 자산의 위치로 이동합니다. 클릭 ![자세히 아이콘](assets/do-not-localize/more2_da2.png) 을(를) 클릭합니다. **[!UICONTROL Edit]**.

사용 **[!UICONTROL Toggle Check-out]** 다음 두 상황에서 다른 사용자의 편집과 충돌을 방지하기 위해 자산을 잠급니다.

* 자산을 먼저 체크 아웃하지 않고 편집을 시작했습니다(예: 자산을 열면 해당 자산).
* 곧 자산 편집을 시작할 계획이며 다른 사용자가 편집하지 않도록 합니다.

편집을 완료하면 앱에 **[!UICONTROL Edited Locally]** 변경된 자산의 상태입니다. 자산에 저장된 모든 변경 사항은 변경 사항을에 업로드할 때까지 로컬 전용입니다 [!DNL Experience Manager]. 개인 또는 일부 자산을 하나씩 업로드하려면 **[!UICONTROL Upload Changes]** 자산에 대한 옵션 사용. 에서 자산의 버전을 만듭니다 [!DNL Experience Manager]. 의 웹 인터페이스 사용 [!DNL Assets], 자산 내역은 [타임라인 보기](https://experienceleague.adobe.com/docs/experience-manager-65/assets/using/activity-stream.html).

![앱에서 변경 내용 업로드 옵션](assets/upload_changes_single1_da2.png "앱에서 변경 내용 업로드 옵션")

![자산의 큰 미리 보기를 볼 때 변경 내용 업로드 선택 사항](assets/upload_changes_single2_da2.png "자산의 큰 미리 보기를 볼 때 변경 내용 업로드 선택 사항")

공동 작업 편집에 대한 우수 사례가 필요하면 [고급 워크플로우: 동일한 파일에 대한 공동 작업 및 편집 충돌 방지](#adv-workflow-collaborate-avoid-conflicts).

다음과 같은 경우 로컬 자산에 대한 변경 및 편집 내용을 취소할 수 있습니다. 클릭 **[!UICONTROL Discard Changes]**.

* 로컬 변경 내용을 [!DNL Experience Manager].
* 일부 변경 사항을 저장한 후 원래 자산에서 변경 작업을 시작합니다.
* 더 이상 필요하지 않으므로 자산 편집을 중지합니다.

필요한 경우 체크 아웃을 전환합니다. 업데이트된 자산이 로컬 캐시 폴더에서 제거되고 편집하거나 열 때 다시 다운로드됩니다.

## 새 자산을 업로드하고 [!DNL Experience Manager] {#upload-and-add-new-assets-to-aem}

사용자는 DAM 저장소에 새 자산을 추가할 수 있습니다. 예를 들어, 사진 촬영에서 로 많은 수의 사진을 추가하려는 에이전시 사진사나 계약업체일 수 있습니다 [!DNL Experience Manager] 저장소. 새 컨텐츠를에 추가하려면 [!DNL Experience Manager], 선택 ![cloud에 업로드 옵션](assets/do-not-localize/upload_to_cloud_da2.png) 를 클릭합니다. 로컬 파일 시스템에서 자산 파일을 탐색하고 를 클릭합니다 **[!UICONTROL Select]**. 또는 자산을 업로드하려면 애플리케이션 인터페이스에서 파일 또는 폴더를 드래그합니다. Windows에서 자산을 앱 내의 폴더로 드래그하면 자산이 폴더에 업로드됩니다. 업로드하는 데 시간이 오래 걸리는 경우 앱에 진행률 표시줄이 표시됩니다.

<!-- ![Download progress bar for large-sized assets](assets/upload_status_da2.png "Download progress bar for large-sized assets")
-->

로컬 파일 시스템에서 폴더 또는 개별 파일을 업로드할 수 있습니다. 폴더의 계층은 업로드될 때 유지됩니다. 자산을 일괄 업로드하기 전에 다음을 참조하십시오 [일괄 업로드](#bulk-upload-assets).

지정된 세션에서 전송된 자산 목록을 보려면 를 클릭합니다 **[!UICONTROL View]** > **[!UICONTROL Assets transfers]**. 목록을 사용하면 현재 세션의 파일 전송을 보고 신속하게 확인할 수 있습니다.

![특정 세션의 전송된 자산 목록](assets/assets_transfered_da2.png "특정 세션의 전송된 자산 목록")

에서 업로드 동시성(가속)을 제어할 수 있습니다 **[!UICONTROL Preferences]** > **[!UICONTROL Upload acceleration]** 설정 일반적으로 더 많은 동시성은 더 빠른 업로드를 제공하지만 리소스를 많이 사용하므로 로컬 시스템의 처리 능력이 더 많이 소모될 수 있습니다. 느린 시스템이 발생하는 경우 낮은 동시성 값을 사용하여 업로드를 다시 시도합니다.

>[!NOTE]
>
>전송 목록은 영구적이지 않으며 앱을 종료하고 다시 여는 경우에는 사용할 수 없습니다.

### 자산 이름의 특수 문자 관리 {#special-characters-in-filename}

레거시 앱에서 저장소에서 생성된 노드 이름은 사용자가 제공하는 폴더 이름의 공백 및 대소문자를 유지합니다. 현재 애플리케이션에서 v1.10 앱의 노드 이름 지정 규칙을 에뮬레이션하려면 다음을 활성화합니다 [!UICONTROL Use legacy conventions when creating nodes for assets and folders] 에서 [!UICONTROL Preferences]. 자세한 내용은 [앱 환경 설정](/help/install-upgrade.md#set-preferences). 이 레거시 기본 설정은 기본적으로 비활성화됩니다.

>[!NOTE]
>
>이 앱은 다음 이름 지정 규칙을 사용하여 저장소의 노드 이름만 변경합니다. 이 앱에는 가 유지됩니다 `Title` 자산입니다.

<!-- TBD: Do NOT use this table.

| Where do characters occur | Characters | Legacy preference | Renaming convention | Example |
|---|---|---|---|---|
| In file name extension | `.` | Enabled or disabled | Retained as is | NA |
| File or folder name | `. / : [ ] | *` | Enabled or disabled | Replaced with a `-` (hyphen) | `myimage.jpg` remains as is and `my.image.jpg` changes to `my-image.jpg`. |
| Folder name | `% ; # , + ? ^ { } "` | Disabled | Replaced with a `-` (hyphen) | tbd |
| File name | `% # ? { } &` | Disabled | Replaced with a `-` (hyphen) | tbd |
| File name | Whitespaces | Enabled or disabled | Retained as is | NA |
| Folder name | Whitespaces | Disabled | Replaced with a `-` (hyphen) | tbd |
| File name | Uppercase characters | Disabled | Retained as is | tbd |
| Folder name | Uppercase characters | Disabled | Replaced with a `-` (hyphen) | tbd |
-->

| 문자 ‡ | 앱의 기존 환경 설정 | 파일 이름에서 발생하는 경우 | 폴더 이름에서 발생하는 경우 | 예 |
|---|---|---|---|---|
| `. / : [ ] | *` | 활성화 또는 비활성화 | 다음으로 대체됨 `-` (하이픈) A `.` 파일 이름 확장명의 (점)은 그대로 유지됩니다. | 다음으로 대체됨 `-` (하이픈) | `myimage.jpg` 는 다음과 같이 유지됩니다. `my.image.jpg` 변경 사항 `my-image.jpg`. |
| `% ; # , + ? ^ { } "` 및 공백 | ![아이콘 선택 취소](assets/do-not-localize/deselect-icon.png) 비활성화됨 | 공백은 유지됩니다. | 다음으로 대체됨 `-` (하이픈) | `My Folder.` 변경 사항 `my-folder-`. |
| `# % { } ? & .` | ![아이콘 선택 취소](assets/do-not-localize/deselect-icon.png) 비활성화됨 | 다음으로 대체됨 `-` (하이픈) | NA. | `#My New File.` 변경 사항 `-My New File-`. |
| 대문자 | ![아이콘 선택 취소](assets/do-not-localize/deselect-icon.png) 비활성화됨 | 케이스는 그대로 유지됩니다. | 소문자로 변경되었습니다. | `My New Folder` 변경 사항 `my-new-folder`. |
| 대문자 | ![선택 항목 아이콘](assets/do-not-localize/selection-checked-icon.png) 활성화됨 | 케이스는 그대로 유지됩니다. | 케이스는 그대로 유지됩니다. | 나. |

문자 ‡ 목록은 공백으로 구분된 목록입니다.

<!-- TBD: Check if the following is to be included in the footnote.

Do not use &#92;&#92; in the names of files and &#92;&#116; &#38; in the names of folders. 
-->


<!-- TBD: Securing the below presentation of the same content in a comment.

**File names**

| Characters | Replaced by |
|---|---|
| &#35; &#37; &#123; &#63; &#125; &#38; &#46; &#47; &#58; &#91; &#124; &#93; &#42; | hyphen (-) |
| whitespaces | whitespaces are retained |
| capital case | casing is retained |

>[!CAUTION]
>
>Avoid using &#92;&#92; in file names.

**Folder names**

| Characters | Replaced by |
|---|---|
| Characters | Replaced by |
| &#37; &#59; &#35; &#44; &#43; &#63; &#94; &#123; &#123; &#34; &#46; &#47; &#59; &#91; &#93; &#124; &#42; | hyphen (-) |
| whitespaces | hyphen (-) |
| capital case | lower case |

>[!CAUTION]
>
>Avoid using &#92;&#92; &#92;&#116; &#38; in folder names.

>[!NOTE]
>
>If you enable [!UICONTROL Use legacy conventions when creating nodes for assets and folders] in app [!UICONTROL Preferences], then the app emulates v1.10 app behavior when uploading folders. In v1.10, the node names created in the repository respect spaces and casing of the folder names provided by the user. For more information, see [app Preferences](/help/install-upgrade.md#set-preferences).

-->

## 여러 자산으로 작업 {#work-with-multiple-assets}

사용자는 한 번에 모든 편집 내용을 업로드하거나 몇 번의 클릭으로 중첩된 폴더를 업로드하는 등의 작업을 사용하여 여러 자산으로 쉽게 작업하고 관리할 수 있습니다.

### 큰 폴더 찾아보기 {#browse-large-folders}

많은 자산이 포함된 폴더로 작업할 경우 스크롤하여 더 많은 자산을 확인합니다. 키보드를 사용하여 스크롤하려면 Tab 키를 여러 번 눌러 맨 위에 있는 자산을 선택합니다. 강조 표시된 자산을 선택하여 언제 선택하는지 확인합니다. 이제 아래쪽 화살표 키를 사용하여 자산 목록을 이동합니다.

### 선택한 자산에 대한 빠른 작업 {#quick-actions-for-selected-assets}

몇 개의 자산의 축소판을 클릭하여 자산을 선택합니다. 모든 자산을 선택하려면 앱의 상단 표시줄에서 확인란을 클릭합니다. 선택한 모든 자산에 적용할 수 있는 작업 세트가 앱 하단에 있는 도구 모음에 표시됩니다.

![하단의 도구 모음에는 선택한 자산과 관련된 작업이 표시됩니다](assets/actions_bottom_toolbar1_da2.png "맨 아래에 있는 도구 모음에는 선택한 자산에 대한 일반적인 작업이 표시됩니다")

![선택 영역에 대한 일반적인 작업이 없을 때 도구 모음에 작업 없음](assets/actions_bottom_toolbar2_da2.png "선택 영역에 대한 일반적인 작업이 없을 때 도구 모음에 작업 없음")

하단의 도구 모음에서 사용할 수 있는 작업은 선택한 파일의 상태에 따라 달라집니다. 예를 들어 **[!UICONTROL Edited Locally]** 파일, **[!UICONTROL Upload Changes]** 아이콘. 혼합을 선택하는 경우 **[!UICONTROL Edited locally]** 및 **[!UICONTROL Cloud only]**, **[!UICONTROL Upload Changes]** 작업을 사용할 수 없습니다.

### 편집한 모든 이미지 찾기 {#find-all-edited-images}

응용 프로그램은 **[!UICONTROL Edited locally]**&#x200B;를 사용하면 로컬로 다운로드한 모든 파일( [!UICONTROL Open] 또는 [!UICONTROL Edit] 작업)을 수행한 다음 수정합니다. 앱을 사용하면 로컬로 편집한 모든 자산을 선택하고 몇 번의 클릭으로 변경 사항을 업로드할 수 있습니다. 이 보기에는 편집 충돌이 있는 로컬로 편집한 자산도 표시됩니다.

![로컬에서 편집한 모든 자산을 표시하도록 필터링합니다.](assets/edited_locally_filter_da2.png "로컬에서 편집한 모든 자산을 표시하도록 필터링합니다. 즉, 일괄 편집 업로드입니다.")

### 자산 일괄 업로드 {#bulk-upload-assets}

사진사나 광고 에이전시와 같은 사용자 또는 조직은 외부에서 수행한 더 큰 세트에서 사진 촬영, 수정 또는 선택과 같은 시나리오에서 다양한 로컬 자산을 만들 수 있습니다 [!DNL Experience Manager]. 이렇게 큰 로컬 폴더를 [!DNL Assets] 데스크탑 앱에서 바로 사용 폴더 계층은 보존되며 모든 중첩 하위 폴더와 포함된 자산이 업로드됩니다. 업로드된 자산은 동일한 서버의 다른 사용자도 즉시 사용할 수 있습니다. 자산이 백그라운드로 업로드되므로 작업이 웹 브라우저 세션에 연결되어 있지 않습니다.

![데스크탑에서 여러 로컬 폴더로 [!DNL Experience Manager]](assets/upload_local_folders_da2.png "데스크탑에서 Experience Manager으로 여러 로컬 폴더를 벌크 업로드")

업로드 후 예상 변경 사항이 앱에 반영되지 않으면 새로 고침 아이콘을 클릭합니다 ![새로 고침 아이콘](assets/do-not-localize/refresh.png).

>[!NOTE]
>
>업로드 기능을 사용하여 두 개 간에 자산을 마이그레이션하지 마십시오 [!DNL Experience Manager] 배포. 대신 를 참조하십시오. [마이그레이션 안내서](https://experienceleague.adobe.com/docs/experience-manager-65/assets/administer/assets-migration-guide.html).

### 전송된 자산 목록 {#list-of-transferred-assets}

지정된 세션에서 전송된 자산 목록을 보려면 를 참조하십시오 [자산 업로드 위치 [!DNL Experience Manager]](#upload-and-add-new-assets-to-aem).

## 고급 워크플로우: 시작 위치 [!DNL Assets] 웹 인터페이스 {#adv-workflow-start-from-aem-ui}

필요한 경우 Assets 웹 인터페이스에서 워크플로우를 시작합니다. 데스크탑 앱은 [!DNL Experience Manager] 데스크톱 작업을 사용하여 요청한 경우 인수할 수 있습니다.

웹 인터페이스에서 워크플로우를 시작하는 특별한 사례는 자산 검색입니다. 자산 사용자 인터페이스의 Omnisearch 표시줄에서는 고급 검색 환경을 제공합니다. 먼저 웹에서 원하는 자산을 찾은 다음 을 사용하여 앱에서 워크플로우를 시작할 수 있습니다 [!UICONTROL Desktop Actions]. 일부 샘플 사례에는 패싯을 사용하여 검색 결과 필터링, Adobe Stock에서 라이선스가 있는 특정 자산 찾기 또는 웹 인터페이스에서 보다 나은 검색을 위해 조직에서 구현한 사용자 지정 등이 있습니다.

데스크탑 앱 기능은 Assets 웹 인터페이스에서 다음 작업을 시도할 때 사용됩니다.

* 다음 [!UICONTROL Desktop Actions] 이렇게 하면 [!UICONTROL Open], [!UICONTROL Edit], 및 [!UICONTROL Reveal]
* [!UICONTROL Upload folder]
* [!UICONTROL Check-out] 또는 [!UICONTROL check-in]

예를 들어, 앱에서 체크 아웃된 자산에 사용할 수 있는 웹 인터페이스의 작업은 다음과 같습니다 [!UICONTROL Open], [!UICONTROL Reveal], 및 [!UICONTROL Check-in].

![의 데스크톱 작업 [!DNL Experience Manager] 웹 인터페이스](assets/assets_web_actions_da2.png "Experience Manager 웹 인터페이스의 데스크톱 작업")

>[!NOTE]
>
>브라우저는 다음에 대한 시작을 허용하라는 메시지를 표시할 수 있습니다 [!DNL Adobe Experience Manager] 데스크톱. 브라우저에서 앱으로 중단되지 않은 전송을 수행하려면 적절한 확인란을 선택하여 앱이 항상 이어지도록 하십시오.

웹 인터페이스를 사용하여 다음 정보나 워크플로우를 찾을 수 없습니다. 웹 인터페이스에서 로컬 변경 사항을 추적하지 않으며 다음을 알지 못하므로 데스크탑 앱을 사용하십시오.

* 로컬에서 편집한 파일입니다.
* 편집 충돌이 있는 파일과 이를 해결하는 방법입니다.
* 로컬 변경 내용을 업로드 [!DNL Experience Manager].
* 로컬에서 사용할 수 있는 파일의 다양한 상태입니다.

반대로, 데스크탑 앱에서 를 사용하여 웹 인터페이스에서 자산을 열 수 있습니다 **[!UICONTROL Open In Web]** 작업.

## 고급 워크플로우: 동일한 파일에 대한 공동 작업 및 편집 충돌 방지 {#adv-workflow-collaborate-avoid-conflicts}

공동 작업 환경에서는 여러 사용자가 버전 관리 충돌을 야기할 수 있는 동일한 자산 세트에서 작업할 수 있습니다. 충돌을 방지하려면 다음 우수 사례를 따르십시오.

* 을 클릭하여 자산을 편집하지 마십시오 [!UICONTROL Open]. 파일 시스템 폴더에서 을 열어 로컬에서 다운로드한 자산을 편집하지 마십시오. 다른 사용자는 자산이 편집되고 있음을 알지 못합니다.
* 자산을 편집하려면 항상 을(를) 클릭합니다 [!UICONTROL Edit]. 기본 애플리케이션에서 자산을 열고 자산에 잠금 아이콘을 추가하므로 다른 사용자는 해당 자산이 편집되고 있음을 알 수 있습니다.
* 클릭 [!UICONTROL Toggle Check-in] 실수로 클릭하여 편집을 시작하는 경우 [!UICONTROL Edit]. 이렇게 하면 자산에 잠금 아이콘이 추가됩니다. 나중에 자산을 편집하려고 하지만 다른 사람이 자산을 편집하지 않도록 하려면 [!UICONTROL Toggle Check-in] 자산을 잠그려면 다음을 수행하십시오.
* 자산을 편집하기 전에 다른 사용자가 자산을 편집하고 있지 않은지 확인하십시오. 자산에서 잠금 아이콘을 찾습니다.
* 편집 내용을 완료한 후 모든 변경 내용을 업로드한 다음, 자산을 체크 인합니다.

![편집 충돌 상태](assets/edits_conflicts_status_da2.png "편집 충돌 상태")

로컬로 다운로드한 자산이 [!DNL Experience Manager] 서버, 앱에 **[!UICONTROL Modified remotely]** 상태. 를 클릭하여 로컬 복사본을 제거하거나 로컬 복사본을 새로 고칠 수 있습니다 [!UICONTROL Remove] 또는 [!UICONTROL Update] 각각 사용할 수 있습니다. 대화 상자의 링크를 사용하면 자산의 두 버전을 모두 볼 수 있습니다.

![자산을 원격으로 수정할 때 충돌을 해결하는 옵션입니다](assets/modified_remotely_dialog_da2.png "자산을 원격으로 수정할 때 충돌을 해결하는 옵션입니다")

로컬에서 편집 중인 자산이 사용자의 지식 없이 서버에서 업데이트되는 경우 앱에 **[!UICONTROL Editing Conflict]** 상태. 한 세트의 변경 사항을 유지할 수 있습니다. 즉, 업데이트를 유지합니다. **[!UICONTROL Keep Mine]**)를 클릭하고 다른 사용자의 편집 또는 업데이트를 존중하며 사용자의 업데이트를 삭제합니다(**[!UICONTROL Overwrite Mine]**).

![편집 충돌을 해결하는 옵션](assets/editing_conflict_dialog_da2.png "편집 충돌을 해결하는 옵션")

## 고급 워크플로우: InDesign 파일에 자산 배치 및 연결 {#adv-workflow-place-assets-indesign}

사용 시 [!DNL Experience Manager] 데스크탑 앱에서 연결된 자산이 있는 파일을 열면 자산이 미리 다운로드되어 기본 애플리케이션에 표시됩니다. 이 워크플로우가 작동하려면 기본 애플리케이션에서 로컬 자산에 대한 링크 배치를 지원해야 합니다 [!DNL Experience Manager] 이진 파일에서 서버측 참조에 대한 이러한 링크 해결을 지원해야 합니다.

[!DNL Experience Manager] 데스크탑 앱에서는 Adobe InDesign, Adobe Illustrator 및 Adobe Photoshop 등 몇 가지 선별된 Adobe Creative Cloud 데스크탑 애플리케이션 및 파일 포맷으로 이 워크플로우를 지원합니다. 워크플로우를 통해 지원되는 Creative Cloud 파일을 사용하여 효율적으로 작업할 수 있습니다. 따라서 사용자 A가 InDesign 파일에 몇 개의 자산을 배치하고 [!DNL Experience Manager]로 지정하는 경우 자산이 파일의 일부가 아니지만 사용자 B는 InDesign 파일에 자산을 표시합니다. 자산은 사용자 B의 컴퓨터에서 로컬로 다운로드됩니다.

>[!NOTE]
>
>데스크탑 앱은 Windows의 모든 드라이브에 매핑할 수 있습니다. 그러나 원활한 작업을 위해 기본 드라이브 문자를 변경하지 마십시오. 동일한 조직의 사용자가 다른 드라이브 문자를 사용하는 경우 다른 사용자가 배치한 자산을 볼 수 없습니다. 경로가 변경되므로 배치된 자산을 가져오지 않습니다. 배치된 자산은 계속해서 이진 파일(INDD)에 배치되며 제거되지 않습니다.

이 워크플로우의 제한 사항을 알아보려면 [시스템 요구 사항 및 지원되는 버전](release-notes.md).

이미지 자산 및 InDesign으로 이 워크플로우를 사용하려면 다음 단계를 수행합니다.

1. 에 배치된 자산을 사용하여 INDD 파일을 바로 사용할 수 있도록 유지 [!DNL Experience Manager]. 이러한 INDD 파일을 만드는 방법을 알아보려면 [그래픽 배치](https://helpx.adobe.com/indesign/using/placing-graphics.html).
1. 데스크탑 앱 내에서 **[!UICONTROL Edit]** 에 배치된 자산이 있는 INDD 파일 [!DNL Experience Manager].
1. 앱은 InDesign 파일과 연결된 자산을 모두 다운로드합니다. InDesign이 문서를 열면 링크가 해결되고 자산이 다운로드되며 자산이 InDesign 문서에 표시됩니다.
1. InDesign 파일에 새 그래픽을 배치하려면 **[!UICONTROL Reveal File]** 작업 을 클릭합니다. 작업은 자산을 로컬로 다운로드하고 Windows 탐색기 또는 Mac Finder에서 로컬 네트워크 공유 위치를 엽니다.
1. 노출된 자산을 InDesign 문서에 배치합니다. 문서에 링크가 만들어집니다.
1. InDesign 문서에서 편집 내용을 완료하면 저장한 다음 [!DNL Experience Manager] 데스크탑 앱 사용.

## 고급 워크플로우: 로컬로 자산 다운로드 {#adv-workflow-download-assets-locally}

앱에서 자산을 다운로드합니다. [!DNL Experience Manager] 많은 시나리오에서 로컬에서 파일 시스템을 관리할 수 있습니다. 이 다운로드는 대역폭 및 디스크 공간을 소모합니다. 이 시나리오를 이해하면 다운로드가 완료될 때까지 대기시간을 최적화하는 데 도움이 됩니다.

온디맨드 앱 내에서 자산을 다운로드합니다. 자세한 내용은 [자산 다운로드](#download-assets).

를 사용하는 경우 [!UICONTROL Open] 기본 데스크탑 애플리케이션에서 자산을 여는 작업입니다. 이 자산은 로컬로 사용할 수 없는 경우 로컬로 다운로드됩니다. 자세한 내용은 [자산 열기](#openondesktop-v2).

앱 내에서 자산 또는 폴더의 위치를 표시하면 자산 또는 폴더가 먼저 로컬로 다운로드된 다음 로컬 네트워크 공유에서 시스템에서 열립니다. 자세한 내용은 [자산 열기](#openondesktop-v2).

를 사용하는 경우 [!UICONTROL Edit] 기본 데스크탑 애플리케이션에서 자산을 편집하는 작업. 로컬로 사용할 수 없는 경우 로컬로 자산이 다운로드됩니다. 자세한 내용은 [자산 편집 및 업데이트된 자산 업로드 [!DNL Experience Manager]](#edit-assets-upload-updated-assets).

앱이 설치되고 허용되면 사용 시 작업이 완료됩니다 [!UICONTROL Desktop Actions] 변환 전: [!DNL Experience Manager] 웹 인터페이스. 앱은 먼저 자산을 다운로드한 다음 작업을 완료합니다.
