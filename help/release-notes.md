---
title: '[!DNL Adobe Experience Manager] 데스크탑 앱 릴리스 노트'
description: ' [!DNL Adobe Experience Manager] 데스크탑 앱에 대한 릴리스 세부 정보, 향상된 기능, 새로운 기능, 호환성 및 다운로드 링크.'
mini-toc-levels: 1
feature: 데스크탑 앱, 릴리스 정보
exl-id: e058e7a2-fcc8-4ad1-899e-20695db6bc72
source-git-commit: ac533db59b2a5c64243b762f4b77b3148c4f1867
workflow-type: tm+mt
source-wordcount: '1523'
ht-degree: 26%

---

# [!DNL Adobe Experience Manager] 데스크탑 앱 릴리스 노트  {#release-notes-v2}

최신 데스크탑 앱 버전 2.1(2.1.2.0)의 릴리스 정보는 아래에 나와 있습니다. 릴리스 날짜는 2021년 3월 26일입니다. 개선 사항이 있는 부 릴리스입니다.

지원되는 **버전**&#x200B;은 다음과 같습니다.[!DNL Experience Manager]

* [!DNL Experience Manager] 로서의  [!DNL Cloud Service]. [릴리스 노트](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/home.html?lang=ko-KR)를 참조하십시오.
* [!DNL Experience Manager] Adobe Managed Services(AMS) 또는 On-Premise에서 6.5.0 이상 [서비스 팩 릴리스 노트](https://experienceleague.adobe.com/docs/experience-manager-65/release-notes/service-pack/sp-release-notes.html?lang=ko-KR)를 참조하십시오.
* [!DNL Experience Manager] Adobe Managed Services(AMS) 또는 On-Premise에서 6.4.4 이상 [서비스 팩 릴리스 노트](https://experienceleague.adobe.com/docs/experience-manager-64/release-notes/sp-release-notes.html?lang=ko-KR)를 참조하십시오.
* [!DNL Experience Manager] 6.4.0 - 6.4.3( [호환성 ](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/cq640/featurepack/adobe-asset-link-support) 패키지가 Adobe Managed Services(AMS) 또는 On-Premise에 설치됨)
* [!DNL Experience Manager] 6.3(호환성 패키지 포함)
* [!DNL Experience Manager] 6.3.3.1 이상( [호환성 패키지 설치 ](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq640/featurepack/adobe-asset-link-support) ) 데스크탑 앱은 [!DNL Experience Manager] 6.3.3.0 또는 이전 버전에서 지원되지 않습니다.

[!DNL Adobe Experience Manager] 데스크탑 앱은 다음  **운영 체제에서 사용할 수 있습니다**.

* macOS X 10.14 이상(최신 버그 수정 포함) [Apple Siliconicon이 ](https://support.apple.com/en-us/HT211814) 있는 Mac 컴퓨터는 아직 지원되지 않습니다.
* Windows 10(최신 서비스 팩 및 버그 수정 포함)

지원되는 OS의 **다운로드 URL**&#x200B;은 다음과 같습니다.

| 운영 체제 | [!DNL Experience Manager]로서의 [!DNL Cloud Service]  | [!DNL Experience Manager] 6.x |
|---|---|---|
| macOS 64비트 | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-2.1.2.0.dmg) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-2.1.2.0.dmg) |
| Windows 64비트 | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win64-2.1.2.0.exe) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win64-2.1.2.0.exe) |
| Windows 32비트 | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win32-2.1.2.0.exe) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win32-2.1.2.0.exe) |

>[!NOTE]
>
>Windows 7은 더 이상 지원되지 않습니다. [Windows 7](https://support.microsoft.com/en-us/help/4057281/windows-7-support-ended-on-january-14-2020)의 EOL에 대한 문서를 참조하십시오.

<!-- The version of the app you plan to install on your local machine requires a specific [!DNL Adobe Experience Manager] server version/additional server-side components (service packs, hot fixes, or feature packs). Contact your [!DNL Experience Manager] administrator for help.
-->

## 다른 자산 및 파일 유형 {#support-for-file-types} 지원

기본 작업용 이진 파일을 나타내는 [!DNL Experience Manager]에 저장된 자산을 애플리케이션에서 지원합니다. 기본 데스크탑 애플리케이션에서 열리는 파일은 운영 체제에서 특정 애플리케이션(예: Mac Preview 또는 Adobe Photoshop)에 연결된 특정 파일 유형(예: PNG 또는 JPG)에 따라 다릅니다.

몇 가지 파일 유형은 연결된 자산을 바이너리에 배치하는 것을 지원합니다. 데스크탑 앱을 사용하여 이진 파일을 열 때 자산이 [!DNL Experience Manager] 저장소에 있는 경우 연결된 자산을 애플리케이션에서 미리 다운로드합니다. 현재 지원되는 파일 유형은 다음과 같습니다.

* [!DNL Adobe InDesign] 파일(INDD 형식)
* [!DNL Adobe Illustrator] 파일(AI 형식)
* [!DNL Adobe Photoshop] 파일(PS 형식)

이 기능은 위의 애플리케이션의 [!DNL Adobe Creative Cloud] 2018 및 [!DNL Adobe Creative Cloud] 2019 버전에서 지원됩니다. 앱에서는 가장 일치하는 방식을 추론하여 연결된 자산의 로컬 데스크탑 경로를 [!DNL Experience Manager] 서버의 URL에 매핑합니다. 몇 가지 가정을 이용합니다.

* 기본 애플리케이션에 배치된 파일까지 경로에는 글로벌 데스크탑 경로( [!UICONTROL Reveal] 옵션과 함께 표시된 로컬 네트워크 공유에서 배치됨)가 사용됩니다.

* 경로는 기본 앱에서 파일의 XMP 레코드에 저장합니다.

* [!DNL Experience Manager] 자산의 메타데이터 레코드까지 경로로 XMP 레코드를 추출했습니다.

* 경로가 [!DNL Experience Manager]의 자산에 일치할 수 있습니다. 즉, 배치된 파일도 경로가 일치하는 [!DNL Experience Manager]에 있습니다.

## 새로운 기능, 개선 사항 및 버그 수정 {#what-is-new}

자세한 내용은 [v2.0의 새로운 기능](introduction.md#whats-new-v2)을 참조하십시오.

**앱 v2.1.2.0에서 업데이트**

* [!UICONTROL Clear Cookies]에 대한 새 옵션이 응용 프로그램의 기본 메뉴에 추가됩니다. 따라서 서버에서 다른 서버로 연결을 변경하는 등 잠재적인 로그인 문제가 발생합니다. ](/help/troubleshoot.md#cannot-login-cookies-issue)에 연결하기 전에 [쿠키 지우기 를 참조하십시오.

**앱 v2.1.1.0에서 업데이트**

* 고급 설정을 사용하여 폴더를 업로드할 때 앱에서 v1.10 앱 동작을 에뮬레이션할 수 있습니다. v1.10에서 리포지토리에서 생성된 노드 이름은 사용자가 제공하는 폴더 이름의 공백 및 대소문자를 따릅니다. v2.1의 기본 동작은 동일하게 유지됩니다. 즉, 폴더 이름에 있는 여러 공백을 저장소 노드 이름의 하이픈으로 바꾸고 소문자 노드 이름으로 변환합니다. [앱 환경 설정](/help/install-upgrade.md#set-preferences)을 참조하십시오.

**앱 v2.1.0.0에서 업데이트**

* 이제 자산을 업로드하기 위해 Windows 탐색기 또는 Mac Finder에서 직접 애플리케이션 인터페이스의 파일 또는 폴더를 드래그할 수 있습니다. 이 기능은 애플리케이션에서 이전에 사용할 수 있었던 업로드 옵션 외에도 작동합니다.<!-- CQ-4309527 -->

**앱 v2.0.3에서 업데이트**

현재 버전에서 해결된 버그는 다음과 같습니다.

* [!DNL Adobe Experience Manager] 6.5.5.0에서 DAM 저장소에 액세스하려고 하는 Windows의 앱 사용자에 대한 로그인 문제를 해결했습니다.

**앱 v2.0.2의 업데이트**

버그 수정 및 업데이트는 다음과 같습니다.

* 이제 업로드 성능을 향상시키기 위해 업로드 가속 설정을 사용할 수 있습니다. 이 설정을 켜면 더 많은 로컬 CPU 스레드를 사용하여 앱을 더 빨리 업로드하고 리소스를 많이 사용합니다.

* 파일 이름 또는 특정 GB18030 문자가 포함된 경로가 수정될 때 자산 업로드가 발생합니다.<!-- CQ-4283494 -->

* 검색 결과에서 다른 정렬 유형으로 전환한 후 관련성별로 정렬 옵션을 사용할 수 있습니다.<!-- CQ-4286874 -->

* 이제 데스크탑 앱에 명시적으로 새로 고칠 필요 없이 하위 폴더가 나열됩니다.<!-- CQ-4285711 -->

* (Windows) 일부 Windows 시스템에서 사용할 수 없는 앱 인터페이스 문제가 해결되었습니다. 인터페이스 요소가 &#39;이동됨&#39; 사이드로의 클릭 영역으로 왜곡되어 표시되므로 사용자가 앱 인터페이스를 클릭할 수 없습니다.<!-- CQ-4280785 -->

**앱 v2.0.1의 업데이트**

버그 수정 및 업데이트는 다음과 같습니다.

* `%APPDATA%` 경로와 일치하도록 `%Temp%` 디렉터리를 구성하는 옵션을 허용합니다.<!-- CQ-4282665 -->

* 사용자가 Okta SAML 인증을 통해 [!DNL Experience Manager] 작성자에 로그인할 수 있도록 허용합니다.<!-- CQ-4278134 -->

## 설치 지침 {#installation-instructions-v2}

앱을 설치하고 구성하는 방법은 [ [!DNL Experience Manager]  데스크탑 앱 설치를 참조하십시오](install-upgrade.md).

이전 [!DNL Experience Manager] 데스크탑 앱에서 업그레이드하는 경우 [이전 버전에서 업그레이드](install-upgrade.md#upgrade-from-previous-version)에 나열된 전환 우수 사례를 따라야 합니다.

## 앱 작동 방식에 대한 중요한 참고 사항 {#how-app-works}

애플리케이션 및 애플리케이션 작동 방식에 대한 다음 내용을 알고 있어야 합니다.

* 자산 바이너리 전체를 [!DNL Experience Manager](열기, 편집, 변경 내용 업로드 및 자산 업로드)과 서로 전송해야 하는 작업에 대한 모든 권한을 애플리케이션에서 제공합니다.

   * 데스크탑의 자산으로 작업하려면 개별적으로, 폴더로 또는 다중 선택을 통해 열기, 편집 또는 데스크탑으로 다운로드를 명시적으로 수행해야 합니다.

   * [!DNL Experience Manager]에 업로드된 자산에 로컬 변경 내용을 가져오려면 개별적으로 또는 다중 선택을 통해 [!UICONTROL Upload Changes] 을 선택해야 합니다.

   * 애플리케이션이 데스크탑과 [!DNL Experience Manager]에서 자산을 동기화하는 &#39;동기화 클라이언트&#39;가 아닙니다.

   * 응용 프로그램에서 [!DNL Experience Manager] 저장소를 가상 폴더 구조로 매핑하는 네트워크 공유를 제공하지 않습니다.

* 애플리케이션에서 표시하는 자산 목록은 Assets 저장소의 상태에 따라 다릅니다. 로컬에서 다운로드한 다음 로컬 파일 또는 캐시 폴더에서 이름을 변경한 파일은 애플리케이션에서 표시하거나 관리하지 않습니다.

* 예상한 결과가 앱에서 표시되지 않으면 상단 표시줄의 새로 고침 아이콘을 클릭합니다.

* [!UICONTROL Reveal File] 작업을 사용할 때 표시되는 로컬 네트워크 공유에는 로컬에서 사용할 수 있는 파일(및 폴더)만 표시됩니다. 로컬 네트워크 공유에 표시되는 적합한 자산을 가져올 수 있도록 [!UICONTROL Reveal File] 및 [!UICONTROL Reveal Folder]에서 자산을 미리 다운로드합니다.

* SMB(Mac)/WebDAV(Windows) 로컬 네트워크 공유는 Creative Cloud 앱의 기본 파일에 연결/배치된 자산 파일을 Adobe Creative Cloud 앱에서 읽을 때 사용됩니다.

다음 다이어그램은 사용자 작업에서 시작된 자산과 파일의 클라우드와 로컬 파일 시스템 간 흐름을 보여줍니다.

![[!DNL Experience Manager]데스크탑 앱을 통한 서버부터 기본 데스크탑 앱까지 자산 흐름](assets/da20_flow_diagram.png)

## 알려진 문제 {#known-issues-v2}

**사용자 인터페이스 문제:**

* 데스크탑 앱의 인터페이스가 비어 있는 경우가 가끔 있습니다. 마우스 오른쪽 단추를 클릭하고 [!UICONTROL Refresh] 을 클릭하여 응용 프로그램을 다시 로드합니다. 새로 고침 후 DAM 저장소의 루트에서 시작합니다. 자산의 업데이트 또는 상태는 유지됩니다.<!-- CQ-4270267 -->

* 트랙 패드 또는 마우스 포인터를 사용하지 않으면 폴더/검색 결과를 탐색하기 어렵습니다. 마우스 장치에 마우스 휠이 없으면 스크롤 막대가 표시되지 않을 수 있습니다.<!-- CQ-4269947 -->

* 자산 업로드가 변경될 때 진행률 표시줄이 제대로 표시되지 않는 경우가 가끔 있습니다.

* 필터를 적용하고 제거하여 로컬에서 편집한 모든 자산을 찾으면 사용자가 시작한 검색 결과 또는 폴더 보기로 앱에서 이동하지 않습니다. DAM 저장소의 루트 폴더를 앱에서 표시합니다.

* 실행 중인 [!DNL Experience Manager] 서버가 없는 URL에 연결하면 연결 화면이 응답하지 않는 경우가 가끔 있습니다. 애플리케이션을 종료하고 다시 시작합니다.

**CRUD(만들기, 읽기, 업데이트 및 삭제) 문제:**

* 잘못된 문자가 있어도 애플리케이션에서 파일 업로드를 시도하면 서버측 업로드가 실패할 수 있습니다. <!-- CQ-4273652 -->

* 변경 내용을 주석과 함께 자산에 업로드할 때 주석이 자산과 함께 [!DNL Experience Manager]에 저장되지만 버전 관리 주석으로 표시되지 않습니다. 이 문제는 [!DNL Experience Manager] 6.4.5 및 [!DNL Experience Manager] 6.5.1에서 해결되었습니다. Adobe은 최신 서비스 팩을 설치하는 것이 좋습니다.<!-- CQ-4268990 -->

* 사용자가 자산 전송을 취소할 수 없습니다. 의도하지 않은 대용량 전송을 트리거한 경우 애플리케이션을 종료하고 다시 시작합니다. <!-- CQ-4278940 -->

**플랫폼 문제:**

* 자산을 열면 해당 자산을 편집하지 않았더라도 [!UICONTROL Edited Locally] 상태로 즉시 변경되는 경우가 가끔 있습니다. [!UICONTROL Refresh] 아이콘을 클릭하여 업데이트합니다.

>[!MORELIKETHIS]
>
>* [[!DNL Experience Manager] as a [!DNL Cloud Service] 설명서](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/landing/home.html)
>* [[!DNL Experience Manager] as a [!DNL Cloud Service] [!DNL Assets] 설명서](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/home.html)
>* [데스크탑 앱을 사용하는 방법 [!DNL Experience Manager] 데스크탑](using.md)
* [데스크탑 앱 설치 및 업그레이드](install-upgrade.md)
* [우수 사례 및 문제 해결 팁](troubleshoot.md)

