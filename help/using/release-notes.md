---
title: "[!DNL Adobe Experience Manager] 데스크탑 앱 릴리스 노트"
description: 의 릴리스 세부 정보, 향상된 기능, 새로운 기능, 호환성 및 다운로드 링크 [!DNL Adobe Experience Manager] 데스크탑 앱입니다.
mini-toc-levels: 1
feature: Desktop App,Release Information
exl-id: e058e7a2-fcc8-4ad1-899e-20695db6bc72
source-git-commit: 0f366e07b9d220cf04286b24e4bb45ce0b385e5c
workflow-type: tm+mt
source-wordcount: '2624'
ht-degree: 14%

---

# [!DNL Adobe Experience Manager] 데스크탑 앱 릴리스 노트 {#release-notes-v2}

최신 데스크탑 앱 버전 2.3.0의 릴리스 정보는 다음과 같습니다. 릴리스 날짜는 2023년 7월 14일입니다.

최신 버전의 데스크탑 앱에는 다음과 같은 버그 수정 및 개선 사항이 포함되어 있습니다.

* IMS 로그인에 대한 지원이 추가되었습니다. IMS 통합을 사용하면 데스크탑 앱에서 액세스 토큰 새로 고침을 자동으로 수행하여 사용자가 최대 14일 동안 로그인 상태를 유지할 수 있습니다.

* 기업 프록시 및 웹 필터링에 대한 지원이 개선되었습니다.


다음 **지원됨 [!DNL Experience Manager] 버전** 은(는)

* [!DNL Experience Manager] as a [!DNL Cloud Service]. 다음을 참조하십시오 [릴리스 정보](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/home.html?lang=ko-KR).
* [!DNL Experience Manager] 6.5.0 이상(Adobe Managed Services(AMS) 또는 온프레미스) 다음을 참조하십시오 [서비스 팩 릴리스 노트](https://experienceleague.adobe.com/docs/experience-manager-65/release-notes/service-pack/sp-release-notes.html?lang=ko-KR).

[!DNL Adobe Experience Manager] 다음에서 데스크탑 앱을 사용할 수 있습니다. **운영 체제**:

* macOS X 10.14 이상(최신 버그 수정 포함)
* 최신 서비스 팩 및 버그 수정 사항이 포함된 Windows 10.

다음 **다운로드 URL** 지원되는 OS의 경우

| 운영 체제 | [!DNL Experience Manager] as a [!DNL Cloud Service] | [!DNL Experience Manager] 6.x |
|---|---|---|
| macOS (v2.3.0) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-x64-2.3.0.dmg) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-x64-2.3.0.dmg) |
| macOS Apple 실리콘(M1)(v2.3.0) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-arm64-2.3.0.dmg) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-arm64-2.3.0.dmg) |
| Windows 64비트(v2.3.0) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win-x64-2.3.0.exe) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win-x64-2.3.0.exe) |
| macOS (v2.2.2) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-x64-2.2.2.dmg) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-x64-2.2.2.dmg) |
| macOS Apple 실리콘(M1)(v2.2.2) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-arm64-2.2.2.dmg) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-arm64-2.2.2.dmg) |
| Windows 64비트(v2.2.2) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win-x64-2.2.2.exe) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win-x64-2.2.2.exe) |
| macOS (v2.2.1) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-x64-2.2.1.dmg) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-x64-2.2.1.dmg) |
| macOS Apple 실리콘(M1)(v2.2.1) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-arm64-2.2.1.dmg) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-arm64-2.2.1.dmg) |
| Windows 64비트(v2.2.1) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win-x64-2.2.1.exe) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win-x64-2.2.1.exe) |
| macOS (v2.2.0) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-x64-2.2.0.dmg) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-x64-2.2.0.dmg) |
| macOS Apple 실리콘(M1)(v2.2.0) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-arm64-2.2.0.dmg) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-arm64-2.2.0.dmg) |
| Windows 64비트(v2.2.0) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win-x64-2.2.0.exe) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win-x64-2.2.0.exe) |
| macOS (v2.1.5.0) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-2.1.5.0.dmg) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-2.1.5.0.dmg) |
| Windows 64비트(v2.1.5.0) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win64-2.1.5.0.exe) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win64-2.1.5.0.exe) |
| Windows 32비트(v2.1.5.0) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win32-2.1.5.0.exe) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win32-2.1.5.0.exe) |
| macOS (v2.1.4.0) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-2.1.4.0.dmg) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-2.1.4.0.dmg) |
| Windows 64비트(v2.1.4.0) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win64-2.1.4.0.exe) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win64-2.1.4.0.exe) |
| Windows 32비트(v2.1.4.0) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win32-2.1.4.0.exe) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win32-2.1.4.0.exe) |
| macOS (v2.1.3.4) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-2.1.3.4.dmg) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-2.1.3.4.dmg) |
| Windows 64비트(v2.1.3.4) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win64-2.1.3.4.exe) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win64-2.1.3.4.exe) |
| Windows 32비트(v2.1.3.1) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win32-2.1.3.1.exe) | [다운로드 링크](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win32-2.1.3.1.exe) |

>[!NOTE]
>
>Windows 7은 더 이상 지원되지 않습니다. 다음을 참조하십시오 [windows 7의 EOL에 대한 문서](https://support.microsoft.com/en-us/help/4057281/windows-7-support-ended-on-january-14-2020).

## 다양한 에셋 및 파일 유형 지원 {#support-for-file-types}

애플리케이션은에 저장된 자산을 지원합니다. [!DNL Experience Manager] 기본 작업용 이진 파일을 나타냅니다. 기본 데스크탑 애플리케이션에서 열리는 파일은 운영 체제에서 특정 애플리케이션(예: Mac Preview 또는 Adobe Photoshop)에 연결된 특정 파일 유형(예: PNG 또는 JPG)에 따라 다릅니다.

몇 가지 파일 유형은 연결된 자산을 바이너리에 배치하는 것을 지원합니다. 자산이 다음에 있는 경우 연결된 자산을 애플리케이션에서 미리 다운로드합니다. [!DNL Experience Manager] 데스크탑 앱을 사용하여 이진 파일을 열 때의 저장소입니다. 현재 지원되는 파일 유형은 다음과 같습니다.

* [!DNL Adobe InDesign] 파일(INDD 형식)
* [!DNL Adobe Illustrator] 파일(AI 형식)
* [!DNL Adobe Photoshop] 파일(PS 형식)

이 기능은 을 통해 지원됩니다. [!DNL Adobe Creative Cloud] 2018년 [!DNL Adobe Creative Cloud] 위의 애플리케이션의 2019 버전입니다. 앱에서는 가장 일치하는 방식을 추론하여 연결된 자산의 로컬 데스크탑 경로를 의 URL에 매핑합니다. [!DNL Experience Manager] 서버입니다. 몇 가지 가정을 이용합니다.

* 기본 애플리케이션에 배치된 파일로의 경로는 글로벌 데스크탑 경로를 사용합니다(표시된 로컬 네트워크 공유에서 배치됨). [!UICONTROL Reveal] 선택 사항).

* 경로는 기본 앱에서 파일의 XMP 레코드에 저장합니다.

* [!DNL Experience Manager] 은(는) 에셋의 메타데이터 레코드 경로가 포함된 XMP 레코드를 추출했습니다.

* 경로는 의 에셋에 일치시킬 수 있습니다. [!DNL Experience Manager]즉, 배치된 파일은에 있습니다 [!DNL Experience Manager] 를 입력합니다.

## 새로운 기능, 개선 사항 및 버그 수정 {#what-is-new}

자세한 내용은 다음을 참조하십시오. [v2.0의 새로운 기능](introduction.md#whats-new-v2).

**앱 v2.2.2의 업데이트**

* [Windows만 해당] 데스크탑 앱은 2.2.0 및 2.2.1 릴리스 버전을 설치한 후 빈 화면을 표시합니다.

**앱 v2.2.1의 업데이트**

* 을 클릭하면 데스크탑 앱에 세션 시간 초과 오류 메시지가 표시됩니다. **[!UICONTROL Sign In]**.

* macOS에서 데스크탑 앱 v2.2.0에 액세스하는 동안 문제가 발생합니다.

* 을 클릭하여 자산을 정렬할 때 데스크탑 앱에 오류 메시지가 표시됩니다. **[!UICONTROL Edited Locally]**.

**앱 v2.2.0의 업데이트**

* Apple Silicon(M1) 지원

* 데스크탑 앱에 로그온하는 동안 연결 문자열을 기억하는 기능.

**앱 v2.1.5.0의 업데이트**

* 중국어 문자가 포함된 폴더에 있는 파일을 업로드할 때 데스크탑 앱이 응답하지 않습니다(ASSETS-9237).

* 데스크탑 앱은 파일 이름의 점을 대시로 바꿉니다(ASSETS-10955).

**앱 v2.1.4.0의 업데이트**

애플리케이션의 새 버전은 버그 수정을 제공합니다.

**앱 v2.1.3.4의 업데이트**

애플리케이션의 새 버전은 버그 수정을 제공합니다.

**앱 v2.1.3.3의 업데이트**

애플리케이션의 새 버전은 버그 수정을 제공합니다.

**앱 v2.1.3.2의 업데이트**

이 버전의 애플리케이션은 버그 수정을 제공합니다.

**앱 v2.1.3.1의 업데이트**

이 버전에서 수정된 버그는 다음과 같습니다.

* 큰 에셋의 경우에도 에셋 업로드 및 다운로드 속도가 개선되었습니다. 이 릴리스에서는에서 에셋이 업로드되는 문제가 해결되었습니다. [!DNL desktop app] 매우 큰 파일이 업로드되면 때로 오류가 발생합니다.

**앱 v2.1.2.0에서 업데이트**

* 에 대한 새로운 옵션 [!UICONTROL Clear Cookies] 는 애플리케이션의 메인 메뉴에 추가됩니다. 서버에서 다른 서버로 연결을 변경하는 등의 잠재적 로그인 문제를 해결하는 데 도움이 됩니다. 다음을 참조하십시오 [연결하기 전에 쿠키 지우기](/help/using/troubleshoot.md#cannot-login-cookies-issue).

* 선택한 경우 앱에서 폴더 및 파일을 업로드하여 해당 노드 이름이에서 생성되도록 하는 옵션이 추가됩니다. [!DNL Adobe Experience Manager] 로컬 파일 및 폴더 이름과 동일합니다.

  이 동작은 데스크탑 앱 버전 1의 기본 동작과 유사합니다. 반면 현재 버전에서는 옵션이 활성화되지 않은 경우 및 문자를 공백으로 둡니다 `% ; # , + ? ^ { } "` 폴더 이름에서 는 폴더 경로에서 대시로 대체됩니다. 또한 폴더 경로에서 대문자 문자는 소문자로 변환됩니다. 그러나 파일 이름에서는 `# % { } ? &` 대시로 대체되지만 공백과 대/소문자는 그대로 유지됩니다. 자세한 내용은, [앱 환경 설정](/help/using/install-upgrade.md#set-preferences) 및 [새 에셋 업로드 및 추가](/help/using/using.md#upload-and-add-new-assets-to-aem).

**앱 v2.1.1.0에서 업데이트**

* 고급 설정을 사용하면 폴더를 업로드할 때 앱에서 v1.10 앱 동작을 에뮬레이션할 수 있습니다. v1.10에서 리포지토리에서 만든 노드 이름은 사용자가 제공한 폴더 이름의 공백과 대/소문자를 따릅니다. v2.1의 기본 동작은 계속 동일하게 유지됩니다. 즉, 폴더 이름의 여러 공백을 저장소 노드 이름에서 하이픈으로 바꾸고, 소문자 노드 이름으로 변환합니다. 다음을 참조하십시오 [앱 환경 설정](/help/using/install-upgrade.md#set-preferences).

**앱 v2.1.0.0에서 업데이트**

* 이제 에셋을 업로드하기 위해 Windows 탐색기 또는 Mac Finder에서 직접 애플리케이션 인터페이스의 파일 또는 폴더를 드래그할 수 있습니다. 애플리케이션에서 사용할 수 있는 업로드 옵션과 함께 작동합니다. 다음을 참조하십시오 [에셋 업로드](/help/using/using.md#upload-and-add-new-assets-to-aem) <!-- CQ-4309527 -->

**앱 v2.0.3에서 업데이트**

이 버전에서 수정된 버그는 다음과 같습니다.

* 의 DAM 저장소에 액세스하려고 하는 Windows의 앱 사용자에 대한 로그인 문제를 해결했습니다. [!DNL Adobe Experience Manager] 6.5.5.0.

**앱 v2.0.2의 업데이트**

버그 수정 및 업데이트:

* 업로드 가속화 설정을 사용하여 업로드 성능을 높일 수 있습니다. 이 설정을 켜면 앱이 더 많은 로컬 CPU 스레드를 사용하여 더 빠르게 업로드되고 더 많은 리소스를 사용합니다.

* 파일 이름 또는 특정 GB18030 문자가 포함된 경로가 수정되면 에셋이 업로드됩니다. <!-- CQ-4283494 -->

* 관련성을 기준으로 정렬 옵션은 검색 결과에서 다른 정렬 유형으로 전환한 후 사용할 수 있습니다. <!-- CQ-4286874 -->

* 이제 데스크탑 앱은 명시적으로 새로 고칠 필요 없이 하위 폴더를 나열합니다. <!-- CQ-4285711 -->

* (Windows) 일부 Windows 컴퓨터에서 앱 인터페이스를 사용할 수 없는 드문 문제를 해결했습니다. 인터페이스 요소가 &#39;이동됨&#39; 옆으로 클릭 영역이 왜곡되어 표시되므로 앱 인터페이스를 클릭할 수 없습니다. <!-- CQ-4280785 -->

**앱 v2.0.1의 업데이트**

버그 수정 및 업데이트:

* 옵션 구성 허용 `%Temp%` 일치시킬 디렉터리 `%APPDATA%` 경로. <!-- CQ-4282665 -->

* 사용자 로그인 허용 [!DNL Experience Manager] Okta SAML 인증을 통해 작성됩니다. <!-- CQ-4278134 -->

## 설치 지침 {#installation-instructions-v2}

앱을 설치하고 구성하는 방법은 [ [!DNL Experience Manager]  데스크탑 앱 설치를 참조하십시오](install-upgrade.md).

이전 버전에서 업그레이드하는 경우 [!DNL Experience Manager] 데스크탑 앱에서는 다음 목록에 있는 전환 우수 사례를 따라야 합니다. [이전 버전에서 업그레이드](install-upgrade.md#upgrade-from-previous-version).

## 앱 작동 방식에 대한 중요한 참고 사항 {#how-app-works}

애플리케이션 및 애플리케이션 작동 방식에 대한 다음 내용을 알고 있어야 합니다.

* 이 응용 프로그램에서는 에셋 바이너리를 및 로 완전히 전송해야 하는 작업을 완벽하게 제어할 수 있습니다 [!DNL Experience Manager] (열기, 편집, 변경 내용 업로드 및 에셋 업로드).

   * 데스크탑에서 자산으로 작업하려면 개별적으로, 폴더로 또는 다중 선택을 통해 열기, 편집 또는 데스크탑으로 다운로드를 명시적으로 수행해야 합니다.

   * 업로드된 에셋에 대한 로컬 변경 내용을 가져오려면 [!DNL Experience Manager], 다음을 선택해야 합니다. [!UICONTROL Upload Changes], 개별적으로 또는 다중 선택을 통해

   * 응용 프로그램이 데스크톱 및 전체에서 자산을 동기화하는 &#39;동기화 클라이언트&#39;가 아닙니다 [!DNL Experience Manager].

   * 응용 프로그램에서 다음을 매핑하는 네트워크 공유를 제공하지 않습니다. [!DNL Experience Manager] 가상 폴더 구조로서의 저장소.

* 애플리케이션에서 표시하는 자산 목록은 Assets 저장소의 상태에 따라 다릅니다. 로컬에서 다운로드한 다음 로컬 파일 또는 캐시 폴더에서 이름을 변경한 파일은 애플리케이션에서 표시하거나 관리하지 않습니다.

* 예상한 결과가 앱에서 표시되지 않으면 상단 표시줄의 새로 고침 아이콘을 클릭합니다.

* [!UICONTROL Reveal File] 작업을 사용할 때 표시되는 로컬 네트워크 공유에는 로컬에서 사용할 수 있는 파일(및 폴더)만 표시됩니다. 로컬 네트워크 공유에 표시되는 적합한 자산을 가져올 수 있도록 [!UICONTROL Reveal File] 및 [!UICONTROL Reveal Folder]에서 자산을 미리 다운로드합니다.

* SMB(Mac)/WebDAV(Windows) 로컬 네트워크 공유는 Creative Cloud 앱의 기본 파일에 연결/배치된 자산 파일을 Adobe Creative Cloud 앱에서 읽을 때 사용됩니다.

다음 다이어그램은 사용자 작업에서 시작된 자산과 파일의 클라우드와 로컬 파일 시스템 간 흐름을 보여줍니다.

![[!DNL Experience Manager]데스크탑 앱을 통한 서버부터 기본 데스크탑 앱까지 자산 흐름](assets/da20_flow_diagram.png)

## 알려진 문제 {#known-issues-v2}

**사용자 인터페이스 문제:**

* 데스크탑 앱의 인터페이스가 비어 있는 경우가 가끔 있습니다. 마우스 오른쪽 단추 클릭 및 클릭 [!UICONTROL Refresh] 응용 프로그램을 다시 로드합니다. 새로 고친 후에는 DAM 저장소의 루트에서 시작합니다. 에셋의 또는 상태에 대한 업데이트가 유지됩니다. <!-- CQ-4270267 -->

* 트랙 패드나 마우스 포인터가 없으면 폴더/검색 결과를 탐색하기 어렵습니다. 마우스 장치에 마우스 휠이 없으면 스크롤 막대가 표시되지 않을 수 있습니다. <!-- CQ-4269947 -->

* 자산 업로드가 변경될 때 진행률 표시줄이 제대로 표시되지 않는 경우가 가끔 있습니다.

* 필터를 적용하고 제거하여 로컬에서 편집한 모든 자산을 찾으면 사용자가 시작한 검색 결과 또는 폴더 보기로 앱에서 이동하지 않습니다. DAM 저장소의 루트 폴더를 앱에서 표시합니다.

* 이 없는 URL에 연결하는 경우 [!DNL Experience Manager] 서버가 실행 중이면 connect(연결) 화면이 응답하지 않습니다. 애플리케이션을 종료하고 다시 시작합니다.

**CRUD(만들기, 읽기, 업데이트 및 삭제) 문제:**

* 주석이 있는 에셋에 변경 사항을 업로드할 때 주석은 에셋과 함께 저장됩니다. [!DNL Experience Manager] 그러나 버전 관리 주석으로 표시되지 않습니다. 이 문제는에서 해결되었습니다. [!DNL Experience Manager] 6.4.5 및 [!DNL Experience Manager] Adobe 6.5.1. 최신 서비스 팩을 설치하는 것이 좋습니다. <!-- CQ-4268990 -->

* 사용자가 자산 전송을 취소할 수 없습니다. 의도하지 않은 대용량 전송을 트리거한 경우 애플리케이션을 종료하고 다시 시작합니다. <!-- CQ-4278940 -->

**플랫폼 문제:**

* 자산을 열면 해당 자산을 편집하지 않았더라도 [!UICONTROL Edited Locally] 상태로 즉시 변경되는 경우가 가끔 있습니다. [!UICONTROL Refresh] 아이콘을 클릭하여 업데이트합니다.

>[!MORELIKETHIS]
>
>* [[!DNL Experience Manager] as a [!DNL Cloud Service] 설명서](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/landing/home.html?lang=ko-KR)
>* [[!DNL Experience Manager] as a [!DNL Cloud Service] [!DNL Assets] 설명서](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/home.html?lang=ko-KR)
>* [사용 방법 [!DNL Experience Manager] 데스크탑 앱](using.md)
>* [데스크탑 앱 설치 및 업그레이드](install-upgrade.md)
>* [우수 사례 및 문제 해결 팁](troubleshoot.md)
