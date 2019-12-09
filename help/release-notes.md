---
title: AEM 데스크탑 앱 릴리스 노트
description: AEM 데스크탑 앱용 릴리스 세부 정보, 개선 사항, 새로운 기능, 호환성 및 다운로드 링크.
uuid: b783c3f8-aa1e-4c05-b687-5894909769f5
contentOwner: AG
products: SG_EXPERIENCEMANAGER/6.3/ASSETS
discoiquuid: 3052549b-fe75-44fb-a55e-5cc612868f54
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: ad5337c8e1697d0a37d3020d25802dc1d732f320

---


# AEM 데스크탑 앱 릴리스 노트 {#release-notes-v2}

| 제품 | AEM(Adobe Experience Manager) 데스크탑 앱 |
|---------------|--------------------------------------------------------------------|
| 앱 버전(개정) | 2.0(2.0.0.4) |
| 지원되는 AEM 버전 | AEM 6.5, AEM 6.4, AEM 6.3(호환성 패키지 포함) |
| 유형 | 주요 릴리스 |
| 릴리스 날짜 | 2019년 8월 30일(Mac), 2019년 9월 9일(Windows) |
| 다운로드 URL | [MacOS 64비트](https://download.macromedia.com/aem-assets-companion-app/aem-desktop-osx-2.0.0.4.dmg), [Windows 64비트](https://download.macromedia.com/aem-assets-companion-app/aem-desktop-win64-2.0.0.4.exe), [Windows 32비트](https://download.macromedia.com/aem-assets-companion-app/aem-desktop-win32-2.0.0.4.exe) |

## 시스템 요구 사항 및 사전 요구 사항 {#system-requirements-and-prerequisites-v2}

AEM 데스크탑 앱은 다음 운영 체제와 호환됩니다.

* Mac OS X 10.10 이상(최신 버그 수정 포함)
* Windows 7 및 Windows 10(최신 서비스 팩 및 버그 수정 포함)

이 앱은 배포 위치가 온-프레미스이거나 AMS(Adobe Managed Services)이거나 관계없이 다음 AEM 버전과 연동합니다.

* [AEM 6.5.0](https://helpx.adobe.com/experience-manager/6-5/release-notes.html) 이상
* [AEM 6.4.4](https://helpx.adobe.com/experience-manager/6-4/release-notes/sp-release-notes.html) 이상
* AEM 6.4.0 - 6.4.3([호환성 패키지](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq640/featurepack/adobe-asset-link-support) 포함)
* AEM 6.3.3.1 이상([호환성 패키지](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq640/featurepack/adobe-asset-link-support) 포함)
* AEM 6.3의 경우 [계획된 서비스 팩](https://helpx.adobe.com/experience-manager/maintenance-releases-roadmap.html)이 없습니다. 이후 AEM 버전으로 업그레이드하는 것이 좋습니다.

앱 버전을 로컬 컴퓨터에 설치하려면 특정 Adobe Experience Manager 서버 버전/서버측 추가 구성 요소(서비스 팩, 핫픽스 또는 기능 팩)가 필요합니다. 도움말은 AEM 관리자에게 문의하십시오.

### 다양한 자산 및 파일 유형 지원 {#support-for-file-types}

기본 작업용 이진 파일을 나타내는 AEM에 저장된 자산을 애플리케이션에서 지원합니다. 기본 데스크탑 애플리케이션에서 열리는 파일은 운영 체제에서 특정 애플리케이션(예: Mac Preview 또는 Adobe Photoshop)에 연결된 특정 파일 유형(예: PNG 또는 JPG)에 따라 다릅니다.

몇 가지 파일 유형은 연결된 자산을 바이너리에 배치하는 것을 지원합니다. 데스크탑 앱을 사용하여 이진 파일을 열 때 자산이 AEM 저장소에 있는 경우 연결된 자산을 애플리케이션에서 미리 다운로드합니다. 현재 지원되는 파일 유형은 다음과 같습니다.

* Adobe InDesign 파일(INDD 형식)
* Adobe Illustrator 파일(AI 형식)
* Adobe Photoshop 파일(PS 형식)

위의 애플리케이션의 Adobe Creative Cloud 2018 및 Creative Cloud 2019 버전에서 기능이 지원됩니다. 앱에서는 가장 일치하는 방식을 추론하여 연결된 자산의 로컬 데스크탑 경로를 AEM 서버의 URL에 매핑합니다. 몇 가지 가정을 이용합니다.

* 기본 애플리케이션에 배치된 파일까지 경로에는 글로벌 데스크탑 경로 사용("표시" 옵션이 표시된 로컬 네트워크 공유에서 배치됨)
* 경로는 기본 앱에서 파일의 XMP 레코드에 저장합니다.
* AEM에서는 자산의 메타데이터 레코드까지 경로로 XMP 레코드를 추출했음
* 경로가 AEM의 자산에 일치할 수 있음(즉, 배치된 파일이 경로가 일치하는 AEM에도 있음)

## 새로운 기능 및 향상된 기능 {#whats-new-added}

자세한 내용은 [앱의 새로운 기능](introduction.md#whats-new-v2)을 참조하십시오.

## 설치 지침 {#installation-instructions-v2}

앱을 설치하고 구성하는 방법은 [AEM 데스크탑 앱 설치](install-upgrade.md)를 참조하십시오.

이전 AEM 데스크탑 앱에서 업그레이드하는 경우 [이전 버전에서 업그레이드](install-upgrade.md#upgrade-from-previous-version)에 나열된 전환 우수 사례를 따라야 합니다.

## 앱 작동 방식에 대한 중요한 참고 사항 {#how-app-works}

애플리케이션 및 애플리케이션 작동 방식에 대한 다음 내용을 알고 있어야 합니다.

* 자산 바이너리 전체를 AEM과 서로 전송해야 하는 작업에 대한 모든 권한을 애플리케이션에서 제공합니다(열기, 편집, 변경 내용 업로드 및 자산 업로드).
   * 데스크탑의 자산으로 작업하려면 개별적으로, 폴더로 또는 다중 선택을 통해 열기, 편집 또는 데스크탑으로 다운로드를 명시적으로 수행해야 합니다.
   * AEM에 업로드된 자산에 로컬 변경 내용을 가져오려면[!UICONTROL Upload Changes] 개별적으로 또는 다중 선택을 통해 선택해야 합니다.
   * 애플리케이션이 데스크탑과 AEM 전체에서 자산을 동기화하는 '동기화 클라이언트'가 아닙니다.
   * AEM 저장소를 가상 폴더 구조로 매핑하는 네트워크 공유를 애플리케이션에서 제공하지 않습니다.
* 애플리케이션에서 표시하는 자산 목록은 AEM Assets 저장소의 상태에 따라 다릅니다. 로컬에서 다운로드한 다음 로컬 파일 또는 캐시 폴더에서 이름을 변경한 파일은 애플리케이션에서 표시하거나 관리하지 않습니다.
* 예상한 결과가 앱에서 표시되지 않으면 상단 표시줄의 새로 고침 아이콘을 클릭합니다.
* [!UICONTROL Reveal File] 작업을 사용할 때 표시되는 로컬 네트워크 공유에는 로컬에서 사용할 수 있는 파일(및 폴더)만 표시됩니다. 로컬 네트워크 공유에 표시되는 적합한 자산을 가져올 수 있도록 [!UICONTROL Reveal File] 및 [!UICONTROL Reveal Folder]에서 자산을 미리 다운로드합니다.
* SMB(Mac)/WebDAV(Windows) 로컬 네트워크 공유는 Creative Cloud 앱의 기본 파일에 연결/배치된 자산 파일을 Adobe Creative Cloud 앱에서 읽을 때 사용됩니다.

다음 다이어그램은 사용자 작업에서 시작된 자산과 파일의 클라우드와 로컬 파일 시스템 간 흐름을 보여줍니다.

![데스크탑 앱을 통한 AEM 서버부터 기본 데스크탑 앱까지 자산 흐름](assets/da20_flow_diagram.png)

## 알려진 문제 {#known-issues-v2}

**사용자 인터페이스 문제:**
* 때때로 데스크탑 앱의 인터페이스는 비어 있을 수 있습니다. Right-click and click [!UICONTROL Refresh] to re-load the application. 새로 고친 후에는 DAM 저장소의 루트에서 시작합니다. 자산의 업데이트 또는 상태가 유지됩니다. <!-- CQ-4270267 -->
* 트랙 패드나 마우스 포인터 없이 폴더/검색 결과를 탐색하기 어렵습니다. The scroll-bar might not appear with mouse devices without mouse wheel. <!-- CQ-4269947 -->
* 자산 업로드가 변경될 때 진행률 표시줄이 제대로 표시되지 않는 경우가 가끔 있습니다.
* 필터를 적용하고 제거하여 로컬에서 편집한 모든 자산을 찾으면 사용자가 시작한 검색 결과 또는 폴더 보기로 앱에서 이동하지 않습니다. DAM 저장소의 루트 폴더를 앱에서 표시합니다.
* 실행 중인 AEM 서버가 없는 URL에 연결하면 연결 화면이 응답하지 않는 경우가 가끔 있습니다. 애플리케이션을 종료하고 다시 시작합니다.

**CRUD(만들기, 읽기, 업데이트 및 삭제) 문제:**
* 잘못된 문자가 있어도 애플리케이션에서 파일 업로드를 시도하면 서버측 업로드가 실패할 수 있습니다. <!-- CQ-4273652 -->
* 댓글이 있는 자산에 변경 사항을 업로드하면 댓글은 AEM의 자산에 저장되지만 버전 관리 주석으로 표시되지 않습니다. 이 문제는 AEM 6.4.5 및 AEM 6.5.1에서 해결되었습니다.최신 서비스 팩을 설치하는 것이 좋습니다. <!-- CQ-4268990 -->
* 사용자가 자산 전송을 취소할 수 없습니다. 의도하지 않은 대용량 전송을 트리거한 경우 애플리케이션을 종료하고 다시 시작합니다. <!-- CQ-4278940 -->

**플랫폼 문제:**
* 자산을 열면 해당 자산을 편집하지 않았더라도 [!UICONTROL Edited Locally] 상태로 즉시 변경되는 경우가 가끔 있습니다. [!UICONTROL Refresh] 아이콘을 클릭하여 업데이트합니다.

>[!MORELIKETHIS]
>
>* [AEM 6.5 설명서](https://helpx.adobe.com/support/experience-manager/6-5.html)
>* [AEM Assets 6.5 설명서](https://docs.adobe.com/content/help/en/experience-manager-64/assets/home.html)
>* [AEM 데스크탑 앱 사용](using.md)
>* [데스크탑 앱 설치 및 업그레이드](install-upgrade.md)
>* [우수 사례 및 문제 해결 팁](troubleshoot.md)

