---
title: '데스크톱 응용 프로그램에 대한 우수 사례 및 문제 해결 [!DNL Adobe Experience Manager] '
description: 모범 사례 및 문제 해결을 따라 설치, 업그레이드, 구성 등과 관련하여 가끔 발생하는 문제를 해결합니다.
exl-id: f388e4ac-907d-4093-ba6f-86ecdafeb015
translation-type: tm+mt
source-git-commit: b893ad24d360ed382cab50771413219ea7bda09e
workflow-type: tm+mt
source-wordcount: '2261'
ht-degree: 0%

---

# [!DNL Adobe Experience Manager] 데스크톱 앱 {#troubleshoot-v2} 문제 해결

[!DNL Adobe Experience Manager] 데스크탑 앱은 배포의  [!DNL Experience Manager] DAM(Digital Asset Management) 저장소에 연결됩니다. 이 앱은 시스템에 저장소 정보 및 검색 결과를 가져오고, 파일 및 폴더를 다운로드 및 업로드하며, 자산 사용자 인터페이스와 충돌을 관리하는 기능을 포함합니다.

앱 문제를 해결하고 모범 사례에 대해 알아보고 제한 사항을 확인하십시오.

## 우수 사례 {#best-practices-to-prevent-troubles}

몇 가지 일반적인 문제 및 문제 해결을 방지하려면 다음 우수 사례를 따르십시오.

* **데스크탑 앱의 작동** 방식 이해:애플리케이션을 사용하기 전에 앱이 작동하는 방식을 알기 위해 잠시 시간을 할애하십시오. [!DNL Experience Manager] 웹 인터페이스와 데스크탑 간 연결, 저장소 매핑, 에셋 캐싱, 로컬에 저장, 백그라운드에서 업로드 등에 대해 알아보십시오. [작동 방식](release-notes.md#how-app-works)을 참조하십시오.

* **폴더 이름에 지원되지 않는 문자를 사용하지 마십시오**.폴더를 만들거나 업로드할 때 공백과 잘못된 문자를 사용하지 마십시오.  [!DNL Experience Manager Assets]](https://experienceleague.adobe.com/docs/experience-manager-65/assets/managing/manage-assets.html#creating-folders)에서 폴더 만들기에 있는 문자 목록을 참조하십시오. [ 일부 [!DNL Experience Manager] 사용 사례는 폴더 이름에 지원되지 않는 문자로 인해 영향을 받을 수 있습니다.

* **충돌을 방지하기 위한 우수 사례**:여러 에셋에서 공동 작업할 때 발생할 수 있는 충돌을 방지하려면 편집 충돌 [을 방지하십시오](using.md#adv-workflow-collaborate-avoid-conflicts).

* **대용량 계층적 폴더에 대해 폴더 업로드 사용**:자산 웹 인터페이스나 다른 방법을 사용하는 대신  [!DNL Experience Manager] 데스크탑 앱을 사용하여 큰 폴더를 업로드합니다. 앱은 로깅 및 모니터링을 통해 백그라운드에서 자산을 업로드합니다. [자산 일괄 업로드](using.md#bulk-upload-assets)를 참조하십시오.

* **최신 버전** 사용:최신 앱 버전을 사용하고 새 앱 버전을 설치하거나 최신 버전으로 업그레이드하기 전에 항상 호환성을  [!DNL Experience Manager] 확인하십시오. [릴리스 노트](release-notes.md)를 참조하십시오.

* **동일한 드라이브 문자** 사용:조직 전체에서 동일한 드라이브 문자를 사용하여  [!DNL Experience Manager] DAM에 매핑합니다. 다른 사용자가 배치한 자산을 보려면 경로가 동일해야 합니다. 동일한 드라이브 문자를 사용하면 DAM 자산에 대한 경로를 일관되게 유지할 수 있습니다. 다른 사용자가 다른 드라이브 문자를 사용하더라도 에셋은 배치된 상태로 유지되며 제거되지 않습니다.

* **네트워크**:네트워크 성능은  [!DNL Experience Manager] 데스크탑 앱 성능에 매우 중요합니다. 파일 전송 또는 벌크 작업에 대한 응답이 느려지면 네트워크 트래픽이 많을 수 있는 기능이나 앱을 끕니다.

* **데스크탑 앱에 지원되지 않는 사용 사례**:자산의 마이그레이션에 앱을 사용하지 마십시오(계획 및 기타 도구가 필요함).대량의 DAM 작업(큰 폴더 이동, 큰 업로드, 고급 메타데이터 검색을 사용한 파일 찾기 등);동기화 클라이언트로 사용하십시오(디자인 원칙 및 사용 패턴은 Microsoft OneDrive 또는 Adobe Creative Cloud 데스크탑 동기화와 같은 in-sync 클라이언트와 다름).

* **시간 초과**:현재, 데스크톱 앱에는 고정 시간 간격 이후 서버와 데스크톱 앱 간의 연결을  [!DNL Experience Manager] 연결하는 구성 가능한 시간 초과 값이 없습니다. 큰 자산을 업로드할 때 잠시 후 연결이 시간 초과되면 업로드 시간 초과를 증가시켜 앱이 자산을 몇 번 업로드하도록 다시 시도합니다. 기본 시간 초과 설정을 변경하는 권장 방법은 없습니다.

## {#troubleshooting-prep} 문제 해결 방법

데스크탑 앱 문제를 해결하려면 다음 정보를 참조하십시오. 또한 지원을 요청하려는 경우 Adobe 고객 지원 센터에 문제를 보다 효과적으로 전달할 수 있습니다.

### 로그 파일 위치 {#check-log-files-v2}

[!DNL Experience Manager] 데스크톱 앱은 운영 체제에 따라 다음 위치에 로그 파일을 저장합니다.

Windows: `%LocalAppData%\Adobe\AssetsCompanion\Logs`

Mac의 경우:`~/Library/Logs/Adobe\ Experience\ Manager\ Desktop`

많은 자산을 업로드할 때, 일부 파일이 업로드되지 못할 경우, 실패한 업로드를 식별하려면 `backend.log` 파일을 참조하십시오.

>[!NOTE]
>
>지원 요청이나 티켓 구입 시 Adobe 고객 지원 센터에서 작업할 때 고객 지원 센터 팀이 문제를 이해하는 데 도움이 되도록 로그 파일을 공유하라는 요청을 받을 수 있습니다. 전체 `Logs` 폴더를 보관하고 고객 지원 센터 담당자와 공유합니다.

### 로그 파일 {#level-of-details-in-log}의 세부 정보 수준 변경

로그 파일의 세부 정보 수준을 변경하려면 다음을 수행합니다.

1. 응용 프로그램이 실행되고 있지 않은지 확인합니다.

1. Windows 시스템의 경우:

   1. 명령 창을 엽니다.

   1. 다음 명령을 실행하여 [!DNL Adobe Experience Manager] 데스크탑 앱을 시작합니다.

   ```shell
   set AEM_DESKTOP_LOG_LEVEL=DEBUG&"C:\Program Files\Adobe\Adobe Experience Manager Desktop.exe
   ```

   Mac 시스템의 경우:

   1. 터미널 창을 엽니다.

   1. 다음 명령을 실행하여 [!DNL Adobe Experience Manager] 데스크탑 앱을 시작합니다.

   ```shell
   AEM_DESKTOP_LOG_LEVEL=DEBUG open /Applications/Adobe\ Experience\ Manager\ Desktop.app
   ```

유효한 로그 수준은 디버그, 정보, 경고 또는 오류입니다. 로그 범위는 DEBUG에서 가장 높고 ERROR에서는 가장 낮습니다.

### 디버그 모드 {#enable-debug-mode} 사용

문제를 해결하려면 디버그 모드를 활성화하고 로그에서 자세한 정보를 볼 수 있습니다.

>[!NOTE]
>
>유효한 로그 수준은 디버그, 정보, 경고 또는 오류입니다. 로그 범위는 DEBUG에서 가장 높고 ERROR에서는 가장 낮습니다.

Mac에서 디버그 모드에서 앱을 사용하려면:

1. 터미널 창 또는 명령 프롬프트를 엽니다.

1. 다음 명령을 실행하여 [!DNL Experience Manager] 데스크탑 앱을 실행합니다.

   `AEM_DESKTOP_LOG_LEVEL=DEBUG open /Applications/Adobe\ Experience\ Manager\ Desktop.app`.

Windows에서 디버그 모드를 활성화하려면:

1. 명령 창을 엽니다.

1. 다음 명령을 실행하여 [!DNL Experience Manager] 데스크탑 앱을 시작합니다.

`AEM_DESKTOP_LOG_LEVEL=DEBUG&"C:\Program Files\Adobe\Adobe Experience Manager Desktop.exe`.

### [!DNL Adobe Experience Manager] 데스크탑 앱 버전 {#know-app-version-v2} 알아보기

버전 번호를 보려면:

1. 애플리케이션을 시작합니다.

1. 오른쪽 위 모서리의 줄임표를 클릭하고 [!UICONTROL Help] 위로 마우스를 가져간 다음 [!UICONTROL About] 을 클릭합니다.

   버전 번호가 이 화면에 나열됩니다.

### 캐시 지우기 {#clear-cache-v2}

다음 단계를 수행합니다.

1. 응용 프로그램을 시작하고 [!DNL Experience Manager] 인스턴스를 연결합니다.

1. 오른쪽 위 모서리의 줄임표를 클릭하고 [!UICONTROL Preferences]을 선택하여 응용 프로그램의 기본 설정을 엽니다.

1. [!UICONTROL Current Cache Size]을(를) 표시하는 항목을 찾습니다. 이 요소 옆에 있는 휴지통 아이콘을 클릭합니다.

캐시를 수동으로 지우려면 아래 단계를 수행하십시오.

>[!CAUTION]
>
>이것은 잠재적으로 파괴되는 작업입니다. [!DNL Adobe Experience Manager]에 업로드되지 않은 로컬 파일 변경 내용이 있는 경우 계속 진행하면 해당 변경 내용이 손실됩니다.

응용 프로그램의 환경 설정에 있는 응용 프로그램의 캐시 디렉토리를 삭제하여 캐시를 지웁니다.

1. 애플리케이션을 시작합니다.

1. 오른쪽 위 모서리의 줄임표를 선택하고 [!UICONTROL Preferences]을 선택하여 응용 프로그램의 기본 설정을 엽니다.

1. [!UICONTROL Cache Directory] 값을 확인합니다.

   이 디렉토리에는 인코딩된 [!DNL Adobe Experience Manager] 끝점의 이름을 가진 하위 디렉토리가 있습니다. 이름은 대상 [!DNL Adobe Experience Manager] URL의 인코딩 버전입니다. 예를 들어 응용 프로그램이 `localhost:4502`을(를) 대상으로 하는 경우 디렉토리 이름은 `localhost_4502`이 됩니다.

캐시를 지우려면 원하는 인코딩된 [!DNL Adobe Experience Manager] 끝점 디렉터리를 삭제합니다. 또는 환경 설정에 지정된 전체 디렉토리를 삭제하면 애플리케이션에서 사용한 모든 인스턴스에 대한 캐시가 지워집니다.

데스크톱 앱의 캐시를 지우려면 몇 가지 문제를 해결할 수 있는 사전 문제 해결 작업입니다. [!DNL Adobe Experience Manager] 앱 환경 설정에서 캐시를 지웁니다. [환경 설정](install-upgrade.md#set-preferences) 설정을 참조하십시오. 캐시 폴더의 기본 위치는 다음과 같습니다.

## 가져온 자산 {#placed-assets-missing}을(를) 볼 수 없습니다.

사용자 또는 다른 크리에이티브 전문가가 지원 파일에 가져온 에셋(예: INDD 파일)이 표시되지 않으면 다음을 확인하십시오.

* 서버에 연결합니다. 네트워크 연결이 끊어지면 자산 다운로드가 중단될 수 있습니다.

* 파일 크기. 대용량 에셋을 다운로드하고 표시하는 데 시간이 오래 걸립니다.

* 문자 일관성 향상 사용자나 다른 협력자가 [!DNL Experience Manager] DAM을 다른 드라이브 문자로 매핑하는 동안 에셋을 배치했다면 가져온 에셋이 표시되지 않습니다.

* 권한. 가져온 자산을 가져올 권한이 있는지 확인하려면 [!DNL Experience Manager] 관리자에게 문의하십시오.

### 데스크톱 앱 사용자 인터페이스에서 파일을 편집해도 [!DNL Adobe Experience Manager] 즉시 {#changes-on-da-not-visible-on-aem}에 반영되지 않습니다.

[!DNL Adobe Experience Manager] 데스크탑 앱은 모든 파일 편집 완료 시간을 사용자가 결정합니다. 파일의 크기와 복잡도에 따라 새 버전의 파일을 다시 [!DNL Adobe Experience Manager]으로 전송하는 데 상당한 시간이 소요됩니다. 응용 프로그램 디자인에서는 파일 편집이 완료되고 자동으로 업로드되는 시기를 추측하지 않고 파일을 주고 받는 횟수를 최소화합니다. 파일의 변경 내용을 업로드하도록 선택하여 사용자가 파일 전송을 다시 [!DNL Adobe Experience Manager]으로 시작하는 것이 좋습니다.

### macOS {#issues-when-upgrading-on-macos}에서 업그레이드할 때 발생하는 문제

macOS에서 [!DNL Experience Manager] 데스크탑 앱을 업그레이드할 때 간혹 문제가 발생할 수 있습니다. 이는 [!DNL Experience Manager] 데스크톱 앱에 대한 레거시 시스템 폴더 때문에 새 버전의 [!DNL Experience Manager] 데스크톱 앱이 올바로 로드되지 않습니다. 이 문제를 해결하려면 다음 폴더 및 파일을 수동으로 제거할 수 있습니다.

다음 단계를 실행하기 전에 macOS 응용 프로그램 폴더의 `Adobe Experience Manager Desktop` 응용 프로그램을 휴지통으로 드래그합니다. 그런 다음 터미널을 열고 다음 명령을 실행하고 메시지가 표시되면 암호를 입력합니다.

```shell
sudo rm -rf ~/Library/Application\ Support/com.adobe.aem.desktop
sudo rm -rf ~/Library/Preferences/com.adobe.aem.desktop.plist
sudo rm -rf ~/Library/Logs/Adobe\ Experience\ Manager\ Desktop

sudo find /var/folders -type d -name "com.adobe.aem.desktop" | xargs rm -rf
sudo find /var/folders -type d -name "com.adobe.aem.desktop.finderintegration-plugin" | xargs rm -rf
```

## {#upload-fails} 파일을 업로드할 수 없습니다.

[!DNL Experience Manager] 6.5.1 이상 버전의 데스크톱 앱을 사용하는 경우 S3 또는 Azure 커넥터를 버전 1.10.4 이상으로 업그레이드하십시오. 이 업데이트는 [OAK-8599](https://issues.apache.org/jira/browse/OAK-8599)과 관련된 파일 업로드 실패 문제를 해결합니다. [설치 지침](install-upgrade.md#install-v2)을 참조하십시오.

## [!DNL Experience Manager] 데스크탑 앱 연결 문제  {#connection-issues}

일반적인 연결 문제가 발생하는 경우 데스크톱 응용 프로그램에서 수행하는 작업에 대한 자세한 정보를 얻을 수 있는 몇 가지 방법이 있습니다.[!DNL Experience Manager]

**요청 로그 확인**

[!DNL Experience Manager] 데스크탑 앱은 각 요청의 응답 코드와 함께 전송된 모든 요청을 전용 로그 파일에 기록합니다.

1. 이러한 요청을 보려면 응용 프로그램의 로그 디렉터리에 `request.log`을(를) 엽니다.

1. 로그의 각 라인은 요청이나 응답을 나타냅니다. 요청에는 `>` 문자가 뒤에 요청된 URL이 옵니다. 응답에는 `<` 문자 뒤에 응답 코드와 요청된 URL이 옵니다. 요청과 응답은 각 라인의 GUID를 사용하여 일치할 수 있습니다.

**응용 프로그램의 포함된 브라우저에서 로드한 요청 확인**

응용 프로그램 요청의 대부분은 요청 로그에 있습니다. 그러나 여기에 유용한 정보가 없는 경우 응용 프로그램의 포함된 브라우저가 보낸 요청을 확인하는 데 유용합니다.
이러한 요청을 보는 방법에 대한 자세한 내용은 [SAML 섹션](#da-connection-issue-with-saml-aem)을 참조하십시오.

### {#da-connection-issue-with-saml-aem}이(가) 작동하지 않는 SAML 로그인 인증

[!DNL Experience Manager] 데스크탑 앱이 SSO 지원(SAML) 배포에 연결할 수  [!DNL Adobe Experience Manager] 없습니다. 응용 프로그램의 디자인이 SSO 연결 및 프로세스의 변형과 복잡성을 수용하려고 시도합니다. 그러나 설치 시 추가 문제 해결이 필요할 수 있습니다.

경우에 따라 SAML 프로세스가 원래 요청된 경로로 다시 리디렉션되지 않거나 최종 리디렉션은 [!DNL Adobe Experience Manager] 데스크탑 앱에서 구성된 것과 다른 호스트로 리디렉션됩니다. 이러한 경우가 아님을 확인하려면

1. 웹 브라우저를 엽니다. `https://[aem_server]:[port]/content/dam.json` URL에 액세스합니다.

1. [!DNL Adobe Experience Manager] 배포에 로그인합니다.

1. 로그인이 완료되면 주소 표시줄에서 브라우저의 현재 주소를 확인합니다. 처음에 입력한 URL과 정확하게 일치해야 합니다.

1. 또한 `/content/dam.json` 이전의 모든 내용이 [!DNL Adobe Experience Manager] 데스크톱 앱 설정에 구성된 대상 [!DNL Adobe Experience Manager] 값과 일치하는지 확인합니다.

**로그인 SAML 프로세스는 위의 단계에 따라 올바르게 작동하지만 사용자는 계속 로그인할 수 없습니다.**

로그인 프로세스를 표시하는 [!DNL Adobe Experience Manager] 데스크톱 앱 내의 창은 단순히 대상 [!DNL Adobe Experience Manager] 인스턴스의 웹 사용자 인터페이스를 표시하는 웹 브라우저입니다.

* Mac 버전은 [WebView](https://developer.apple.com/documentation/webkit/webview)를 사용합니다.

* Windows 버전은 Chromium 기반 [CefSharp](https://cefsharp.github.io/)을 사용합니다.

SAML 프로세스가 이러한 브라우저를 지원하는지 확인합니다.

문제를 추가로 해결하기 위해 브라우저가 로드를 시도하는 정확한 URL을 볼 수 있습니다. 이 정보를 보려면:

1. [디버그 모드](#enable-debug-mode)에서 응용 프로그램을 시작하는 방법에 따릅니다.

1. 로그인 시도를 재현합니다.

1. 응용 프로그램의 [로그 디렉토리](#check-log-files-v2)로 이동합니다.

1. Windows의 경우:

   1. &quot;aemunconrolog.txt&quot;를 엽니다.

   1. &quot;로그인 브라우저 주소가 다음으로 변경됨&quot;으로 시작하는 메시지를 검색합니다. 이러한 항목에는 응용 프로그램이 로드한 URL도 포함되어 있습니다.

   Mac의 경우:

   1. `com.adobe.aem.desktop-nnnnnnnn-nnnnnn.log`가  **** 있는 경우 최신 파일 이름에 있는 숫자 중 하나로 대체됩니다.

   1. &quot;로드된 프레임&quot;으로 시작하는 메시지를 검색합니다. 이러한 항목에는 응용 프로그램이 로드한 URL도 포함되어 있습니다.


로드되는 URL 시퀀스를 보면 SAML의 끝에서 문제를 해결하는 데 도움이 되어 잘못된 점을 파악할 수 있습니다.

### SSL 구성 문제 {#ssl-config-v2}

엄격한 SSL 적용을 활용하는 HTTP 통신에 대해 [!DNL Experience Manager] 데스크톱 앱이 사용하는 라이브러리입니다. 때때로 브라우저 사용에 성공하지만 [!DNL Experience Manager] 데스크탑 앱을 사용하지 못할 수도 있습니다. SSL을 적절히 구성하려면 Apache에서 누락된 중간 인증서를 설치합니다. Apache](https://access.redhat.com/solutions/43575)에서 중간 CA 인증서를 설치하는 방법을 참조하십시오.[

HTTP 통신을 위해 [!DNL Experience Manager] 데스크톱 앱이 사용하는 라이브러리는 엄격한 SSL 적용을 사용합니다. 따라서 브라우저 간 SSL 연결에 [!DNL Adobe Experience Manager] 데스크탑 앱이 실패할 수 있습니다. 이 기능은 SSL의 올바른 구성을 권장하고 보안을 강화하지만 응용 프로그램이 연결할 수 없을 때 좌절감을 줄 수 있습니다.

이 경우 도구를 사용하여 서버의 SSL 인증서를 분석하고 문제를 식별하여 문제를 수정할 수 있는 것이 좋습니다. URL 제공에 대한 서버 인증서를 검사하는 웹 사이트가 있습니다.

임시 측정은 [!DNL Adobe Experience Manager] 데스크톱 앱에서 엄격한 SSL 적용을 비활성화할 수 있습니다. SSL이 잘못 구성된 근본 원인을 숨겨 보안을 강화하므로 이는 권장되지 않는 장기 솔루션입니다. 엄격한 적용을 비활성화하려면 다음을 수행하십시오.

1. 원하는 편집기를 사용하여 다음 위치(운영 체제에 따라 다름)에 있는 응용 프로그램의 JavaScript 구성 파일을 편집합니다.

   Mac의 경우:`/Applications/Adobe Experience Manager Desktop.app/Contents/Resources/javascript/lib-smb/config.json`

   Windows: `C:\Program Files (x86)\Adobe\Adobe Experience Manager Desktop\javascript\config.json`

1. 파일에서 다음 섹션을 찾습니다.

   ```shell
   ...
   "assetRepository": {
       "options": {
   ...
   ```

1. 다음과 같이 `"strictSSL": false`을(를) 추가하여 섹션을 수정합니다.

   ```shell
   ...
   "assetRepository": {
       "options": {
           "strictSSL": false,
   ...
   ```

1. 파일을 저장하고 [!DNL Adobe Experience Manager] 데스크탑 앱을 다시 시작합니다.

### 다른 서버 {#cannot-login-cookies-issue}로 전환할 때 로그인 문제

[!DNL Experience Manager] 서버를 사용한 후 다른 서버에 대한 연결을 변경하려고 하면 로그인 문제가 발생할 수 있습니다. 기존 쿠키가 새로운 인증에 방해가 되기 때문입니다. [!UICONTROL Clear Cookies]에 대한 주 메뉴의 옵션이 도움이 됩니다. 앱의 현재 세션에서 로그아웃한 다음 연결을 진행하기 전에 [!UICONTROL Clear Cookies]을 선택합니다.

![서버 전환 시 쿠키 지우기](assets/main_menu_logout_da2.png)

## 앱이 응답하지 않음 {#unresponsive}

거의 응용 프로그램이 응답하지 않거나, 흰색 화면만 표시하거나, 인터페이스 아래쪽에 아무 옵션도 없는 오류를 표시하는 경우가 있습니다. 순서대로 다음을 시도해 보십시오.

* 응용 프로그램 인터페이스를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Refresh]**&#x200B;을 클릭합니다.
* 애플리케이션을 종료하고 다시 엽니다.

두 방법 모두에서 앱은 루트 DAM 폴더에서 시작됩니다.

## 만료된 자산 {#hide-expired-assets} 숨기기

[!DNL Experience Manager] 사용자 인터페이스 내에서 자산을 검색할 때 만료된 자산이 표시되지 않습니다. 데스크탑 앱 및 에셋 링크에서 에셋을 검색할 때 만료된 에셋을 보고, 검색하고, 가져오는 것을 방지하기 위해 관리자는 다음 구성을 수행할 수 있습니다. 구성은 관리자 권한에 관계없이 모든 사용자에 대해 작동합니다.

* [만료된 자산을 숨기도록 Experience Manager 6.5의 구성](https://experienceleague.adobe.com/docs/experience-manager-65/assets/managing/manage-assets.html#hide-expired-assets-via-acp-api).
* [만료된 자산을 숨기기 위한 Cloud Service의 구성입니다](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/manage-digital-assets.html#hide-expired-assets-via-acp-api).

<!--
### Need additional help with [!DNL Experience Manager] desktop app {#additional-help}

Create Jira ticket with the following information:

* Use `DAM - Companion App` as the [!UICONTROL Component].

* Detailed steps to reproduce the issue in [!UICONTROL Description].

* DEBUG level logs that were captured while reproducing the issue.

* Target Experience Manager version.

* Operating system version.

* [!DNL Adobe Experience Manager] desktop app version. To know your app version, see [finding the desktop app version](#know-app-version-v2).
-->

>[!MORELIKETHIS]
>
>* [알려진 문제](release-notes.md#known-issues-v2)
>* [편집 충돌 방지](using.md#adv-workflow-collaborate-avoid-conflicts)

