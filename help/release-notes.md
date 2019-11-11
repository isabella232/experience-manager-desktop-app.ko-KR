---
title: AEM 데스크탑 앱 릴리스 노트
seo-title: AEM 데스크탑 앱 릴리스 노트
description: AEM 데스크탑 앱 v1.x에 대한 릴리스 세부 정보, 개선 사항, 새로운 기능, 호환성 및 다운로드 링크.
seo-description: AEM 데스크탑 앱 v1.x에 대한 릴리스 세부 정보, 개선 사항, 새로운 기능, 호환성 및 다운로드 링크.
uuid: b783c3f8-aa1e-4c05-b687-5894909769f5
contentOwner: asgupta
products: SG_EXPERIENCEMANAGER/6.3/ASSETS
discoiquuid: 3052549b-fe75-44fb-a55e-5cc612868f54
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: b74a3ff5c9a25ee1433dd661a1bce677271a5ebe

---


# AEM 데스크탑 앱 릴리스 노트 {#release-notes-v2}

| 제품 | AEM(Adobe Experience Manager) 데스크탑 앱 |
|---------------|--------------------------------------------------------------------|
| 앱 버전(개정) | 2.0 (2.0.0.4) |
| 지원되는 AEM 버전 | AEM 6.5, AEM 6.4, AEM 6.3(호환성 패키지 포함) |
| 유형 | 주요 릴리스 |
| 릴리스 날짜 | 2019년 8월 30일(Mac), 2019년 9월 9일 (Win) |
| URL 다운로드 | [MacOS 64비트](https://download.macromedia.com/aem-assets-companion-app/aem-desktop-osx-2.0.0.4.dmg),Windows [64비트](https://download.macromedia.com/aem-assets-companion-app/aem-desktop-win64-2.0.0.4.exe), [Windows 32비트](https://download.macromedia.com/aem-assets-companion-app/aem-desktop-win32-2.0.0.4.exe) |

## 시스템 요구 사항 및 사전 요구 사항 {#system-requirements-and-prerequisites-v2}

AEM 데스크탑 앱은 다음 운영 체제와 호환됩니다.

* Mac OS X 10.10 이상, 최신 버그 수정
* 최신 서비스 팩 및 버그 수정이 포함된 Windows 7 및 Windows 10

이 앱은 온프레미스 또는 Adobe Managed Services(AMS)에 배포되든 관계없이 다음 AEM 버전과 작동합니다.

* [AEM 6.5.0](https://helpx.adobe.com/experience-manager/6-5/release-notes.html) 이상
* [AEM 6.4.4](https://helpx.adobe.com/experience-manager/6-4/release-notes/sp-release-notes.html) 이상
* AEM 6.4.0 - 6.4.3( [호환성 패키지 포함)](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq640/featurepack/adobe-asset-link-support)
* AEM 6.3.3.1 이상 및 [호환성 패키지](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq640/featurepack/adobe-asset-link-support)
* AEM 6.3의 경우 [서비스 팩은 계획이](https://helpx.adobe.com/experience-manager/maintenance-releases-roadmap.html)없습니다. 최신 AEM 버전으로 업그레이드하는 것이 좋습니다.

로컬 컴퓨터에 설치하려는 앱 버전은 특정 Adobe Experience Manager 서버 버전/서버측 추가 구성 요소(서비스 팩, 핫픽스 또는 기능 팩)가 필요합니다. 도움이 필요하면 AEM 관리자에게 문의하십시오.

### 다양한 에셋 및 파일 유형 지원 {#support-for-file-types}

애플리케이션은 기본 작업에 대해 이진 파일을 나타내는 AEM에 저장된 자산을 지원합니다. 기본 데스크톱 응용 프로그램에서 파일을 여는 것은 Mac Preview 또는 Adobe Photoshop과 같은 특정 응용 프로그램에 대한 PNG 또는 JPG와 같은 특정 파일 유형의 운영 체제 연결에 따릅니다.

몇 가지 파일 유형은 바이너리에 연결된 에셋을 배치할 수 있도록 지원합니다. 데스크톱 앱을 사용하여 이진 파일을 열 때 자산이 AEM 저장소에 있는 경우 애플리케이션은 연결된 자산을 미리 다운로드합니다. 현재 지원되는 파일 유형은 다음과 같습니다.

* Adobe InDesign 파일(INDD 포맷)
* Adobe Illustrator 파일(AI 포맷)
* Adobe Photoshop 파일(PS 포맷)

이 기능은 위의 애플리케이션의 Adobe Creative Cloud 2018 및 Creative Cloud 2019 버전에서 지원됩니다. 앱은 휴리스틱한 최적 일치 방법을 사용하여 연결된 자산의 로컬 데스크톱 경로를 AEM 서버의 URL에 매핑합니다. 몇 가지 가정을 바탕으로 합니다.

* 기본 애플리케이션에 배치된 파일에 대한 경로는 전역 데스크톱 경로를 사용합니다("표시" 옵션과 함께 표시된 로컬 네트워크 공유에서 배치).
* 경로는 기본 앱으로 파일의 XMP 레코드에 저장됩니다
* AEM 파섹
* 경로는 AEM의 자산에 일치할 수 있습니다(즉, 배치된 파일도 일치하는 경로 아래의 AEM에 있음).

## 새로운 기능 및 향상된 기능 {#whats-new-added}

자세한 내용은 앱의 [새로운 기능을 참조하십시오](introduction.md#whats-new-v2).

## 설치 지침 {#installation-instructions-v2}

앱 설치 및 구성 방법에 대한 자세한 내용은 AEM [데스크탑 앱](install-upgrade.md)설치를 참조하십시오.

이전 AEM 데스크톱 앱에서 업그레이드하는 경우 이전 버전에서 [업그레이드 시](install-upgrade.md#upgrade-from-previous-version)나열된 전환 모범 사례를 따라야 합니다.

## 앱 작동 방식에 대한 중요 참고 사항 {#how-app-works}

응용 프로그램 및 응용 프로그램의 작동 방식에 대한 다음 내용을 이해하는 것이 중요합니다.

* 애플리케이션은 자산 이진을 AEM에서 AEM으로 전체 전송해야 하는 작업을 완벽하게 제어합니다(자산 열기, 편집, 업로드 변경 사항 및 업로드).
   * 데스크탑에서 에셋을 사용하여 작업하려면 개별, 폴더 또는 다중 선택을 통해 명시적으로 데스크탑을 열고 편집 또는 다운로드해야 합니다.
   * AEM에 업로드된 자산에 대한 로컬 변경 사항을 가져오려면 개별적으로 또는 다중 선택을 [!UICONTROL Upload Changes]통해 선택해야 합니다.
   * 애플리케이션은 데스크톱 및 AEM에서 자산을 동기화하는 '동기화 클라이언트'가 아닙니다.
   * 애플리케이션은 AEM 저장소를 가상 폴더 구조로 매핑하는 네트워크 공유를 제공하지 않습니다.
* 애플리케이션에서 표시되는 자산 목록은 AEM 자산 저장소의 상태를 기반으로 합니다. 로컬에서 다운로드한 다음 로컬 파일 또는 캐시 폴더에서 이름을 바꾼 모든 파일은 응용 프로그램에서 표시하거나 관리하지 않습니다.
* 앱에 예상 결과가 표시되지 않으면 상단 막대에서 새로 고침 아이콘을 클릭합니다.
* 작업을 사용할 때 표시되는 로컬 네트워크 공유는 로컬에서 사용할 수 있는 파일(및 폴더)만 표시합니다. [!UICONTROL Reveal File] [!UICONTROL Reveal File] 에셋을 [!UICONTROL Reveal Folder] 미리 다운로드하여 로컬 네트워크 공유에서 원하는 에셋을 찾을 수 있습니다.
* SMB(Mac) /WebDAV(Win) 로컬 네트워크 공유는 Adobe Creative Cloud 앱이 Creative Cloud 앱의 기본 파일에 연결/배치된 에셋 파일을 읽을 때 사용됩니다.

다음 다이어그램은 사용자 작업에 의해 시작된 것처럼 클라우드에서 로컬 파일 시스템으로 에셋과 파일의 흐름을 보여 줍니다.

![데스크탑 앱을 통해 AEM 서버에서 기본 데스크탑 앱으로의 자산 흐름](assets/do-not-localize/da20_flow_diagram.png)

## Known issues {#known-issues-v2}

**사용자 인터페이스 문제:**
* 때때로 데스크탑 앱의 인터페이스가 비어 있을 수 있습니다. 마우스 오른쪽 단추를 클릭하고 클릭하여 애플리케이션을 다시 [!UICONTROL Refresh] 로드합니다. 이러한 새로 고침은 앱의 상태를 재설정하고 DAM 저장소의 루트에 있는 시작 화면에서 시작합니다. <!-- CQ-4270267 -->
* 트랙패드나 마우스 휠이 없으면 폴더/검색 결과를 탐색하기 어렵습니다. 마우스 휠이 없는 마우스 장치에서는 스크롤 막대가 표시되지 않을 수 있습니다. <!-- CQ-4269947 -->
* 종종, 자산 업로드가 변경될 때 진행률 표시줄이 올바로 표시되지 않습니다.
* 필터를 적용하고 제거하여 로컬에서 편집한 모든 자산을 찾은 후 앱에서 사용자가 시작한 검색 결과 또는 폴더 보기로 이동하지 않습니다. 앱은 DAM 저장소의 루트 폴더를 표시합니다.
* 때때로 실행 중인 AEM 서버가 없는 URL에 연결하면 연결 화면이 응답하지 않습니다. 애플리케이션을 종료하고 다시 시작합니다.

**CRUD(만들기, 읽기, 업데이트 및 삭제) 문제:**
* 응용 프로그램에서 잘못된 문자가 있어도 파일을 업로드하려고 하면 서버측 업로드 오류가 발생할 수 있습니다. <!-- CQ-4273652 -->
* 댓글이 있는 자산에 대한 변경 사항을 업로드할 때 주석은 AEM의 자산에 저장되지만 버전 관리 주석으로 표시되지 않습니다(AEM 6.4.5, 6.5.1에서 해결됨). <!-- CQ-4268990 -->
* 사용자가 자산 전송을 취소할 수 없습니다. 의도하지 않은 큰 전송을 트리거한 경우 애플리케이션을 종료하고 다시 시작합니다. <!-- CQ-4278940 -->

**플랫폼 문제:**
* Windows에서는 편집한 것이 아닐 수도 있지만 자산을 연 [!UICONTROL Edited Locally] 후 자산의 상태가 즉시 변경될 수 있습니다. 을 [!UICONTROL Refresh] 클릭하여 업데이트합니다.

>[!MORELIKETHIS]
>
>* [AEM 6.5 설명서](https://helpx.adobe.com/support/experience-manager/6-5.html)
>* [AEM Assets 6.5 설명서](https://docs.adobe.com/content/help/en/experience-manager-64/assets/home.html)
>* [AEM 데스크탑 앱 사용](using.md)
>* [데스크탑 앱 설치 및 업그레이드](install-upgrade.md)
>* [모범 사례 및 문제 해결 팁](troubleshoot.md)

