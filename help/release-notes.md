---
title: Adobe Experience Manager 데스크탑 앱 릴리스 노트
description: 릴리스 세부 사항, 개선 사항, 새로운 기능, 호환성 및 Adobe Experience Manager 데스크탑 앱용 다운로드 링크.
uuid: b783c3f8-aa1e-4c05-b687-5894909769f5
contentOwner: AG
products: SG_EXPERIENCEMANAGER/6.3/ASSETS
discoiquuid: 3052549b-fe75-44fb-a55e-5cc612868f54
index: y
internal: n
snippet: y
mini-toc-levels: 1
translation-type: tm+mt
source-git-commit: 91de08ba317de97a1d1900dc2351efcb4d6cf95f
workflow-type: tm+mt
source-wordcount: '1364'
ht-degree: 45%

---


# Adobe Experience Manager 데스크탑 앱 릴리스 노트 {#release-notes-v2}

| 제품 | Adobe Experience Manager 데스크탑 앱 |
|--- |--- |
| 앱 버전(개정) | 2.0 (2.0.3.2) |
| 지원되는 AEM 버전 | AEM의 Cloud ServiceAEM 6.5;AEM 6.4;AEM 6.3(호환성 패키지 포함) |
| 유형 | 부 릴리스 |
| 릴리스 날짜 | 2020년 8월 27일 (Mac 및 Win) |
| 다운로드 URL | [macOS 64비트](https://download.macromedia.com/aem-assets-companion-app/aem-desktop-osx-2.0.3.2.dmg); [Windows 64비트](https://download.macromedia.com/aem-assets-companion-app/aem-desktop-win64-2.0.3.2.exe); [Windows 32비트](https://download.macromedia.com/aem-assets-companion-app/aem-desktop-win32-2.0.3.2.exe) |

## 시스템 요구 사항 및 사전 요구 사항 {#system-requirements-and-prerequisites-v2}

Adobe Experience Manager 데스크탑 앱은 다음 운영 체제와 호환됩니다.

* Mac OS X 10.14 이상, 최신 버그 수정

* 최신 서비스 팩 및 버그 수정이 포함된 Windows 10

>[!NOTE]
>
>Windows 7은 더 이상 공급업체에서 지원하지 않습니다(https://support.microsoft.com/en-us/help/4057281/windows-7-support-ended-on-january-14-2020).

이 앱은 Cloud Service, AMS(Adobe Managed Services) 또는 온프레미스 중 어떤 Experience Manager 버전으로 배포되었든 다음 버전에서 작동합니다.

* [클라우드 서비스로서의 Experience Manager](https://docs.adobe.com/content/help/ko-KR/experience-manager-cloud-service/release-notes/home.html).

* [Experience Manager 6.5.0](https://docs.adobe.com/content/help/en/experience-manager-65/release-notes/release-notes.html) 이상

* [Experience Manager 6.4.4](https://docs.adobe.com/content/help/en/experience-manager-64/release-notes/release-notes.html) 이상

* Experience Manager 6.4.0 - 6.4.3( [호환성 패키지 포함)](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/cq640/featurepack/adobe-asset-link-support).

>[!NOTE]
>
>Experience Manager 6.3에 대한 데스크탑 앱 지원은 더 이상 필요하지 않습니다. Adobe은 최신 및 지원되는 Adobe Experience Manager 버전으로 업그레이드할 것을 권장합니다.
>Experience Manager 6.3.3.1 이상 버전은 [호환성 패키지를 설치한 후 데스크탑 앱에서 작동합니다](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq640/featurepack/adobe-asset-link-support). Experience Manager 6.3에는 [서비스 팩이 계획이 없으므로 이러한 패키지를 사용할 수 없습니다](https://helpx.adobe.com/kr/experience-manager/maintenance-releases-roadmap.html).

앱 버전을 로컬 컴퓨터에 설치하려면 특정 Adobe Experience Manager 서버 버전/서버측 추가 구성 요소(서비스 팩, 핫픽스 또는 기능 팩)가 필요합니다. Adobe Experience Manager 관리자에게 도움을 요청하십시오.

### Support for different assets and file types {#support-for-file-types}

이 응용 프로그램은 기본 작업을 위해 이진 파일을 나타내는 Adobe Experience Manager에 저장된 에셋을 지원합니다. 기본 데스크탑 애플리케이션에서 열리는 파일은 운영 체제에서 특정 애플리케이션(예: Mac Preview 또는 Adobe Photoshop)에 연결된 특정 파일 유형(예: PNG 또는 JPG)에 따라 다릅니다.

몇 가지 파일 유형은 연결된 자산을 바이너리에 배치하는 것을 지원합니다. 데스크톱 앱을 사용하여 이진 파일을 열 때 자산이 Experience Manager 저장소에 있는 경우 응용 프로그램은 연결된 자산을 미리 다운로드합니다. 현재 지원되는 파일 유형은 다음과 같습니다.

* [!DNL Adobe InDesign] 파일(INDD 형식)
* [!DNL Adobe Illustrator] 파일(AI 포맷)
* [!DNL Adobe Photoshop] 파일(PS 형식)

이 기능은 위의 애플리케이션의 Adobe Creative Cloud 2018 및 Adobe Creative Cloud 2019 버전에서 지원됩니다. 앱은 이성적인 최상의 일치 방법을 사용하여 연결된 자산의 로컬 데스크탑 경로를 Experience Manager 서버의 URL에 매핑합니다. 몇 가지 가정을 이용합니다.

* Paths to placed files in the native application use a global desktop path (placed from the local network share shown with [!UICONTROL Reveal] option).

* 경로는 기본 앱을 통해 파일의 XMP 기록에 저장됩니다.

* Experience Manager이 자산의 메타데이터 레코드 경로를 사용하여 XMP 레코드를 추출했습니다.

* 경로는 Experience Manager의 에셋과 일치할 수 있습니다. 즉, 배치된 파일도 일치하는 경로 아래 Experience Manager에 있습니다.

## 새로운 기능 및 향상된 기능 {#whats-new-added}

To know the details, see [What&#39;s new in v2.0](introduction.md#whats-new-v2).

**앱 v2.0.3의 업데이트**

현재 버전에서 수정된 버그:

* 앱을 사용하여 6.5.5.0 인스턴스에서 DAM 저장소에 액세스하려고 하는 Windows 사용자가 [!DNL Adobe Experience Manager] 직면한 로그인 문제를 수정했습니다.

**앱 v2.0.2의 업데이트**

버그 수정 및 업데이트는 다음과 같습니다.

* 업로드 성능을 향상시키려면 업로드 가속도가 증가합니다 [!UICONTROL Preferences]. 이 설정이 켜지면 앱은 더 많은 로컬 CPU 스레드를 사용하고 리소스를 많이 사용합니다.

* 파일 이름 또는 경로에 특정 GB18030자가 포함될 때 자산 업로드 문제가 해결되었습니다. <!-- CQ-4283494 -->

* 검색 결과에서 다른 정렬 유형으로 전환한 후 연관성 기준 정렬 옵션을 사용할 수 있습니다. <!-- CQ-4286874 -->

* 이제 데스크탑 앱은 명시적으로 새로 고칠 필요 없이 하위 폴더를 나열합니다. <!-- CQ-4285711 -->

* (Windows) 일부 Windows 컴퓨터에서 사용할 수 없는 앱 인터페이스 문제를 해결했습니다. 인터페이스 요소 &#39;이동됨&#39;의 클릭 영역에 맞게 변형된 앱 인터페이스를 클릭할 수 없습니다. <!-- CQ-4280785 -->

**앱 v2.0.1의 업데이트**

버그 수정 및 업데이트는 다음과 같습니다.

* 경로 일치로 `%Temp%` 디렉토리를 구성하는 옵션을 `%APPDATA%` 허용합니다. <!-- CQ-4282665 -->

* 사용자가 Okta SAML 인증을 통해 AEM 작성자에 로그인하도록 허용 <!-- CQ-4278134 -->

## 설치 지침 {#installation-instructions-v2}

To know how to install and configure the app, see [Install Experience Manager desktop app](install-upgrade.md).

If you are upgrading from a previous Experience Manager desktop app, you must follow these best practices for transitioning that are listed at [upgrade from previous version](install-upgrade.md#upgrade-from-previous-version).

## 앱 작동 방식에 대한 중요한 참고 사항 {#how-app-works}

애플리케이션 및 애플리케이션 작동 방식에 대한 다음 내용을 알고 있어야 합니다.

* 자산 바이너리 전체를 AEM과 서로 전송해야 하는 작업에 대한 모든 권한을 애플리케이션에서 제공합니다(열기, 편집, 변경 내용 업로드 및 자산 업로드).

   * 데스크탑의 자산으로 작업하려면 개별적으로, 폴더로 또는 다중 선택을 통해 열기, 편집 또는 데스크탑으로 다운로드를 명시적으로 수행해야 합니다.

   * AEM에 업로드된 자산에 로컬 변경 내용을 가져오려면[!UICONTROL Upload Changes] 개별적으로 또는 다중 선택을 통해 선택해야 합니다.

   * 애플리케이션이 데스크탑과 AEM 전체에서 자산을 동기화하는 &#39;동기화 클라이언트&#39;가 아닙니다.

   * AEM 저장소를 가상 폴더 구조로 매핑하는 네트워크 공유를 애플리케이션에서 제공하지 않습니다.

* 애플리케이션에서 표시하는 자산 목록은 AEM Assets 저장소의 상태에 따라 다릅니다. 로컬에서 다운로드한 다음 로컬 파일 또는 캐시 폴더에서 이름을 변경한 파일은 애플리케이션에서 표시하거나 관리하지 않습니다.

* 예상한 결과가 앱에서 표시되지 않으면 상단 표시줄의 새로 고침 아이콘을 클릭합니다.

* [!UICONTROL Reveal File] 작업을 사용할 때 표시되는 로컬 네트워크 공유에는 로컬에서 사용할 수 있는 파일(및 폴더)만 표시됩니다. 로컬 네트워크 공유에 표시되는 적합한 자산을 가져올 수 있도록 [!UICONTROL Reveal File] 및 [!UICONTROL Reveal Folder]에서 자산을 미리 다운로드합니다.

* SMB(Mac)/WebDAV(Windows) 로컬 네트워크 공유는 Creative Cloud 앱의 기본 파일에 연결/배치된 자산 파일을 Adobe Creative Cloud 앱에서 읽을 때 사용됩니다.

다음 다이어그램은 사용자 작업에서 시작된 자산과 파일의 클라우드와 로컬 파일 시스템 간 흐름을 보여줍니다.

![데스크탑 앱을 통한 AEM 서버부터 기본 데스크탑 앱까지 자산 흐름](assets/da20_flow_diagram.png)

## 알려진 문제 {#known-issues-v2}

**사용자 인터페이스 문제:**

* 때때로 데스크탑 앱의 인터페이스는 비어 있을 수 있습니다. Right-click and click [!UICONTROL Refresh] to re-load the application. 새로 고친 후에는 DAM 저장소의 루트에서 시작합니다. 자산의 업데이트 또는 상태는 유지됩니다. <!-- CQ-4270267 -->

* 트랙 패드나 마우스 포인터를 사용하지 않으면 폴더/검색 결과를 탐색하기가 어렵습니다. The scroll-bar might not appear with mouse devices without mouse wheel. <!-- CQ-4269947 -->

* 자산 업로드가 변경될 때 진행률 표시줄이 제대로 표시되지 않는 경우가 가끔 있습니다.

* 필터를 적용하고 제거하여 로컬에서 편집한 모든 자산을 찾으면 사용자가 시작한 검색 결과 또는 폴더 보기로 앱에서 이동하지 않습니다. DAM 저장소의 루트 폴더를 앱에서 표시합니다.

* 실행 중인 AEM 서버가 없는 URL에 연결하면 연결 화면이 응답하지 않는 경우가 가끔 있습니다. 애플리케이션을 종료하고 다시 시작합니다.

**CRUD(만들기, 읽기, 업데이트 및 삭제) 문제:**

* 잘못된 문자가 있어도 애플리케이션에서 파일 업로드를 시도하면 서버측 업로드가 실패할 수 있습니다. <!-- CQ-4273652 -->

* 댓글이 있는 자산에 변경 사항을 업로드하면 댓글은 AEM의 자산에 저장되지만 버전 관리 주석으로는 보이지 않습니다. 이 문제는 AEM 6.4.5 및 AEM 6.5.1에서 해결되었습니다. Adobe은 최신 서비스 팩을 설치하는 것이 좋습니다. <!-- CQ-4268990 -->

* 사용자가 자산 전송을 취소할 수 없습니다. 의도하지 않은 대용량 전송을 트리거한 경우 애플리케이션을 종료하고 다시 시작합니다. <!-- CQ-4278940 -->

**플랫폼 문제:**

* 자산을 열면 해당 자산을 편집하지 않았더라도 [!UICONTROL Edited Locally] 상태로 즉시 변경되는 경우가 가끔 있습니다. [!UICONTROL Refresh] 아이콘을 클릭하여 업데이트합니다.

>[!MORELIKETHIS]
>
>* [AEM(Cloud Service 설명서)](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html)
>* [AEM(Cloud Service 에셋 설명서)](https://docs.adobe.com/content/help/ko-KR/experience-manager-cloud-service/assets/home.html)
>* [Experience Manager 데스크탑 앱 사용 방법](using.md)
>* [데스크탑 앱 설치 및 업그레이드](install-upgrade.md)
>* [우수 사례 및 문제 해결 팁](troubleshoot.md)

