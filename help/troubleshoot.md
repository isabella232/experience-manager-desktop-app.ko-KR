---
title: '데스크탑 앱 및 문제 해결 우수 사례 [!DNL Adobe Experience Manager] '
description: 모범 사례 및 문제 해결을 따라 설치, 업그레이드, 구성 등과 관련된 간혹 문제가 해결됩니다.
exl-id: f388e4ac-907d-4093-ba6f-86ecdafeb015
source-git-commit: 2c846fb9cd82691f6439e93429dffcca8127ba68
workflow-type: tm+mt
source-wordcount: '2260'
ht-degree: 0%

---

# [!DNL Adobe Experience Manager] 데스크탑 앱 문제 해결 {#troubleshoot-v2}

[!DNL Adobe Experience Manager] 데스크탑 앱은 배포 [!DNL Experience Manager] 의 DAM(Digital Asset Management) 저장소에 연결됩니다. 이 앱은 컴퓨터에서 저장소 정보 및 검색 결과를 가져오고, 파일 및 폴더를 다운로드 및 업로드하며, Assets 사용자 인터페이스와 충돌을 관리하는 기능을 포함합니다.

앱 문제 해결, 모범 사례 학습 및 제한 사항을 확인하려면 를 참조하십시오.

## 우수 사례 {#best-practices-to-prevent-troubles}

몇 가지 일반적인 문제와 문제 해결을 방지하려면 다음 우수 사례를 따르십시오.

* **데스크탑 앱 작동 방식 이해**: 애플리케이션 사용을 시작하기 전에 앱이 작동하는 방식을 알아 보려면 잠시 시간을 할애하십시오. [!DNL Experience Manager] 웹 인터페이스와 데스크탑 간 연결, 저장소 매핑, 자산 캐싱, 로컬로 저장 및 백그라운드에서 업로드에 대해 알아봅니다. [작동 방식](release-notes.md#how-app-works)을 참조하십시오.

* **폴더 이름에 지원되지 않는 문자를 사용하지 마십시오**. 폴더를 만들거나 업로드할 때 공백 및 잘못된 문자를 사용하지 마십시오. [폴더 만들기 [!DNL Experience Manager Assets]](https://experienceleague.adobe.com/docs/experience-manager-65/assets/managing/manage-assets.html#creating-folders)에서 문자 목록을 참조하십시오. 일부 [!DNL Experience Manager] 사용 사례는 폴더 이름에 지원되지 않는 문자가 영향을 받을 수 있습니다.

* **충돌을 방지하기 위한 우수 사례**: 여러 자산을 공동 작업할 때 발생할 수 있는 충돌을 방지하려면  [편집 충돌 방지](using.md#adv-workflow-collaborate-avoid-conflicts)를 참조하십시오.

* **크고 계층적인 폴더에 대해 폴더 업로드 사용**: Assets 웹 인터페이스나 다른 방법을 사용하는 대신  [!DNL Experience Manager] 데스크탑 앱을 사용하여 큰 폴더를 업로드합니다. 이 앱에서는 로깅 및 모니터링을 사용하여 자산을 백그라운드에서 업로드합니다. [자산 일괄 업로드](using.md#bulk-upload-assets)를 참조하십시오.

* **최신 버전 사용**: 새 앱 버전을 설치하기 전에 또는 최신 버전으로 업그레이드하기 전에 최신 앱 버전을 사용하고 항상 호환성을  [!DNL Experience Manager] 확인하십시오. [릴리스 노트](release-notes.md)를 참조하십시오.

* **같은 드라이브 문자 사용**: 조직에 있는 동일한 드라이브 문자를 사용하여 DAM에  [!DNL Experience Manager] 매핑합니다. 다른 사용자가 배치한 자산을 보려면 경로가 동일해야 합니다. 동일한 드라이브 문자를 사용하면 DAM 자산의 경로를 일관되게 확인할 수 있습니다. 다른 사용자가 다른 드라이브 문자를 사용하더라도 자산이 배치된 상태로 유지되며 제거되지 않습니다.

* **네트워크** 주의: 네트워크 성능은  [!DNL Experience Manager] 데스크탑 앱 성능에 매우 중요합니다. 파일 전송 또는 대량 작업에 대한 응답 속도가 느려지면 네트워크 트래픽이 많을 수 있는 기능을 끄십시오.

* **데스크탑 앱에 대해 지원되지 않는 사용 사례**: 자산의 마이그레이션에 앱을 사용하지 마십시오(계획 및 기타 도구가 필요). 대량의 DAM 작업(대용량 폴더 이동, 대용량 업로드, 고급 메타데이터 검색을 사용하여 파일 찾기 등) 동기화 클라이언트로(디자인 원칙 및 사용 패턴은 Microsoft OneDrive 또는 Adobe Creative Cloud 데스크탑 동기처럼 동기화 중인 클라이언트와 다릅니다.)

* **시간 제한**: 현재 데스크탑 앱에는 고정된 시간 간격 후 서버 [!DNL Experience Manager] 와 데스크탑 앱 간의 연결을 해제하는 구성 가능한 시간 초과 값이 없습니다. 큰 자산을 업로드할 때 잠시 후에 연결이 시간 초과되면 업로드 시간 제한을 높여 자산을 몇 번 다시 업로드합니다. 기본 시간 초과 설정을 변경하는 권장 방법은 없습니다.

## 문제 해결 방법 {#troubleshooting-prep}

데스크탑 앱 문제를 해결하려면 다음 정보를 참조하십시오. 또한 지원을 원하는 경우 고객 지원 Adobe에 문제를 더 잘 전달할 수 있도록 준비합니다.

### 로그 파일 위치 {#check-log-files-v2}

[!DNL Experience Manager] 데스크탑 앱은 운영 체제에 따라 다음 위치에 로그 파일을 저장합니다.

Windows: `%LocalAppData%\Adobe\AssetsCompanion\Logs`

Mac에서: `~/Library/Logs/Adobe\ Experience\ Manager\ Desktop`

많은 자산을 업로드할 때 일부 파일을 업로드하지 못하면 `backend.log` 파일을 참조하여 실패한 업로드를 식별하십시오.

>[!NOTE]
>
>지원 요청 또는 티켓에서 Adobe 고객 지원 팀과 작업할 때 고객 지원 팀에서 문제를 이해하는 데 도움이 되도록 로그 파일을 공유하도록 요청할 수 있습니다. 전체 `Logs` 폴더를 보관하고 고객 지원 담당자와 공유합니다.

### 로그 파일의 세부 정보 수준 변경 {#level-of-details-in-log}

로그 파일의 세부 정보 수준을 변경하려면

1. 애플리케이션이 실행되고 있지 않은지 확인합니다.

1. Windows 시스템의 경우:

   1. 명령 창을 엽니다.

   1. 다음 명령을 실행하여 [!DNL Adobe Experience Manager] 데스크탑 앱을 시작합니다.

   ```shell
   set AEM_DESKTOP_LOG_LEVEL=DEBUG&"C:\Program Files\Adobe\Adobe Experience Manager Desktop.exe
   ```

   Mac 시스템에서:

   1. 터미널 창을 엽니다.

   1. 다음 명령을 실행하여 [!DNL Adobe Experience Manager] 데스크탑 앱을 시작합니다.

   ```shell
   AEM_DESKTOP_LOG_LEVEL=DEBUG open /Applications/Adobe\ Experience\ Manager\ Desktop.app
   ```

유효한 로그 수준은 DEBUG, INFO, WARN 또는 ERROR입니다. 로그 부위는 DEBUG에서 가장 높으며 ERROR에서는 가장 낮습니다.

### 디버그 모드 활성화 {#enable-debug-mode}

문제를 해결하려면 디버그 모드를 활성화하고 로그에 자세한 정보를 가져올 수 있습니다.

>[!NOTE]
>
>유효한 로그 수준은 DEBUG, INFO, WARN 또는 오류입니다. 로그 부위는 DEBUG에서 가장 높으며 ERROR에서는 가장 낮습니다.

Mac에서 디버그 모드에서 앱을 사용하려면 다음을 수행하십시오.

1. 터미널 창이나 명령 프롬프트를 엽니다.

1. 다음 명령을 실행하여 [!DNL Experience Manager] 데스크탑 앱을 시작합니다.

   `AEM_DESKTOP_LOG_LEVEL=DEBUG open /Applications/Adobe\ Experience\ Manager\ Desktop.app`.

Windows에서 디버그 모드를 활성화하려면

1. 명령 창을 엽니다.

1. 다음 명령을 실행하여 [!DNL Experience Manager] 데스크탑 앱을 시작합니다.

`AEM_DESKTOP_LOG_LEVEL=DEBUG&"C:\Program Files\Adobe\Adobe Experience Manager Desktop.exe`.

### [!DNL Adobe Experience Manager] 데스크탑 앱 버전을 알아봅니다 {#know-app-version-v2}

버전 번호를 보려면 다음을 수행하십시오.

1. 애플리케이션을 시작합니다.

1. 오른쪽 위 모서리의 줄임표를 클릭하고 [!UICONTROL Help] 위로 마우스를 이동한 다음 [!UICONTROL About] 를 클릭합니다.

   버전 번호는 이 화면에 나열됩니다.

### 캐시 지우기 {#clear-cache-v2}

다음 단계를 수행합니다.

1. 응용 프로그램을 시작하고 [!DNL Experience Manager] 인스턴스를 연결합니다.

1. 오른쪽 상단 모서리의 줄임표를 클릭하고 [!UICONTROL Preferences] 을 선택하여 응용 프로그램의 기본 설정을 엽니다.

1. [!UICONTROL Current Cache Size]을 표시하는 항목을 찾습니다. 이 요소 옆에 있는 휴지통 아이콘을 클릭합니다.

캐시를 수동으로 지우려면 아래 단계를 수행하십시오.

>[!CAUTION]
>
>이것은 잠재적으로 파괴적인 동작입니다. [!DNL Adobe Experience Manager]에 업로드되지 않은 로컬 파일 변경 내용이 있는 경우 계속 진행하면 해당 변경 내용이 손실됩니다.

응용 프로그램의 기본 설정에 있는 응용 프로그램의 캐시 디렉토리를 삭제하여 캐시가 지워집니다.

1. 애플리케이션을 시작합니다.

1. 오른쪽 상단 모서리에서 줄임표를 선택하고 [!UICONTROL Preferences] 을 선택하여 응용 프로그램의 기본 설정을 엽니다.

1. [!UICONTROL Cache Directory] 값을 확인합니다.

   이 디렉토리에는 인코딩된 [!DNL Adobe Experience Manager] 끝점 다음에 이름이 지정된 하위 디렉토리가 있습니다. 이름은 타깃팅된 [!DNL Adobe Experience Manager] URL의 인코딩된 버전입니다. 예를 들어 애플리케이션이 `localhost:4502`을(를) 타겟팅하는 경우 디렉토리 이름은 `localhost_4502`이 됩니다.

캐시를 지우려면 원하는 인코딩 [!DNL Adobe Experience Manager] 끝점 디렉터리를 삭제합니다. 또는 기본 설정에 지정된 전체 디렉토리를 삭제하면 애플리케이션에서 사용한 모든 인스턴스에 대한 캐시가 지워집니다.

데스크톱 앱의 캐시를 지우려면 몇 가지 문제를 해결할 수 있는 사전 문제 해결 작업입니다. [!DNL Adobe Experience Manager] 앱 환경 설정에서 캐시를 지웁니다. [환경 설정 지정](install-upgrade.md#set-preferences)을 참조하십시오. 캐시 폴더의 기본 위치는 다음과 같습니다.

## 배치된 자산을 볼 수 없음 {#placed-assets-missing}

본인 또는 다른 크리에이티브 전문가가 지원 파일(예: INDD 파일)에 배치한 자산을 볼 수 없는 경우 다음을 확인하십시오.

* 서버에 연결합니다. 전체 네트워크 연결로 자산 다운로드가 중단될 수 있습니다.

* 파일 크기입니다. 큰 자산을 다운로드하여 표시하는 데 시간이 오래 걸립니다.

* 드라이브 문자 일관성 사용자나 다른 공동 작업자가 [!DNL Experience Manager] DAM을 다른 드라이브 문자로 매핑하는 동안 자산을 배치했다면 배치된 자산이 표시되지 않습니다.

* 권한. 배치된 자산을 가져올 수 있는 권한이 있는지 확인하려면 [!DNL Experience Manager] 관리자에게 문의하십시오.

### 데스크탑 앱의 사용자 인터페이스에 있는 파일에 대한 편집 내용은 [!DNL Adobe Experience Manager]에 즉시 반영되지 않습니다 {#changes-on-da-not-visible-on-aem}

[!DNL Adobe Experience Manager] 데스크탑 앱에서는 파일의 모든 편집 작업이 완료되는 시점을 사용자가 결정합니다. 파일의 크기와 복잡성에 따라 새 버전의 파일을 다시 [!DNL Adobe Experience Manager]으로 전송하는 데 상당한 시간이 소요됩니다. 응용 프로그램의 설계에서는 파일 편집이 완료되고 자동으로 업로드되는 시기를 예측하는 대신 파일을 앞뒤로 전송하는 횟수를 최소화해야 합니다. 파일의 변경 내용을 업로드하도록 선택하여 사용자가 파일을 다시 [!DNL Adobe Experience Manager]으로 전송하는 것을 시작하는 것이 좋습니다.

### macOS에서 업그레이드할 때 발생하는 문제 {#issues-when-upgrading-on-macos}

macOS에서 [!DNL Experience Manager] 데스크탑 앱을 업그레이드할 때 간혹 문제가 발생할 수 있습니다. 이 문제는 [!DNL Experience Manager] 데스크탑 앱의 기존 시스템 폴더가 있기 때문에 새 버전의 [!DNL Experience Manager] 데스크탑 앱이 올바르게 로드되지 않습니다. 이 문제를 해결하려면 다음 폴더와 파일을 수동으로 제거할 수 있습니다.

다음 단계를 실행하기 전에, macOS 애플리케이션 폴더의 `Adobe Experience Manager Desktop` 애플리케이션을 휴지통으로 드래그합니다. 그런 다음 터미널을 열고 다음 명령을 실행하고 메시지가 표시되면 암호를 입력합니다.

```shell
sudo rm -rf ~/Library/Application\ Support/com.adobe.aem.desktop
sudo rm -rf ~/Library/Preferences/com.adobe.aem.desktop.plist
sudo rm -rf ~/Library/Logs/Adobe\ Experience\ Manager\ Desktop

sudo find /var/folders -type d -name "com.adobe.aem.desktop" | xargs rm -rf
sudo find /var/folders -type d -name "com.adobe.aem.desktop.finderintegration-plugin" | xargs rm -rf
```

## 파일을 업로드할 수 없습니다. {#upload-fails}

[!DNL Experience Manager] 6.5.1 이상에서 데스크탑 앱을 사용하는 경우 S3 또는 Azure 커넥터를 버전 1.10.4 이상으로 업그레이드하십시오. 이 변수는 [OAK-8599](https://issues.apache.org/jira/browse/OAK-8599)과 관련된 파일 업로드 실패 문제를 해결합니다. [설치 지침](install-upgrade.md#install-v2)을 참조하십시오.

## [!DNL Experience Manager] 데스크탑 앱 연결 문제 {#connection-issues}

일반 연결 문제가 발생하는 경우 [!DNL Experience Manager] 데스크탑 앱에서 수행하는 작업에 대한 자세한 정보를 얻는 몇 가지 방법이 있습니다.

**요청 로그를 확인합니다**

[!DNL Experience Manager] 데스크톱 앱은 보내는 모든 요청을 각 요청의 응답 코드와 함께 전용 로그 파일에 기록합니다.

1. 응용 프로그램의 로그 디렉토리에서 `request.log` 을 열어 이러한 요청을 확인합니다.

1. 로그의 각 행은 요청이나 응답을 나타냅니다. 요청에는 `>` 문자 뒤에 요청한 URL이 옵니다. 응답에는 `<` 문자 뒤에 응답 코드와 요청한 URL이 옵니다. 요청과 응답은 각 라인의 GUID를 사용하여 일치할 수 있습니다.

**응용 프로그램의 포함된 브라우저에서 로드한 요청을 확인합니다**

대부분의 응용 프로그램 요청은 요청 로그에 있습니다. 그러나 여기에 유용한 정보가 없다면 애플리케이션의 포함 브라우저에서 보낸 요청을 확인하는 것이 유용할 수 있습니다.
이러한 요청을 보는 방법에 대한 지침은 [SAML 섹션](#da-connection-issue-with-saml-aem)을 참조하십시오.

### SAML 로그인 인증이 작동하지 않음 {#da-connection-issue-with-saml-aem}

[!DNL Experience Manager] 데스크탑 앱은 SSO 사용(SAML) 배포에 연결할 수  [!DNL Adobe Experience Manager] 없습니다. 애플리케이션의 설계는 SSO 연결 및 프로세스의 변형과 복잡성을 수용하려고 합니다. 하지만, 설정에 추가 문제 해결 필요 가 있을 수 있습니다.

경우에 따라 SAML 프로세스가 원래 요청된 경로로 리디렉션되지 않거나 최종 리디렉션은 [!DNL Adobe Experience Manager] 데스크탑 앱에 구성된 경로와 다른 호스트로 리디렉션됩니다. 이 경우가 아닌지 확인하려면:

1. 웹 브라우저를 엽니다. `https://[aem_server]:[port]/content/dam.json` URL에 액세스합니다.

1. [!DNL Adobe Experience Manager] 배포에 로그인합니다.

1. 로그인이 완료되면 주소 표시줄에서 브라우저의 현재 주소를 확인합니다. 처음 입력한 URL과 정확히 일치해야 합니다.

1. 또한 `/content/dam.json` 앞의 모든 내용이 [!DNL Adobe Experience Manager] 데스크탑 앱의 설정에 구성된 target [!DNL Adobe Experience Manager] 값과 일치하는지 확인합니다.

**로그인 SAML 프로세스는 위의 단계에 따라 올바르게 작동하지만 사용자는 계속 로그인할 수 없습니다**

로그인 프로세스를 표시하는 [!DNL Adobe Experience Manager] 데스크탑 앱 내의 창은 단순히 대상 [!DNL Adobe Experience Manager] 인스턴스의 웹 사용자 인터페이스를 표시하는 웹 브라우저입니다.

* Mac 버전은 [WebView](https://developer.apple.com/documentation/webkit/webview)를 사용합니다.

* Windows 버전은 Chromium 기반 [CefSharp](https://cefsharp.github.io/)을 사용합니다.

SAML 프로세스가 이러한 브라우저를 지원하는지 확인합니다.

추가 문제를 해결하기 위해 브라우저가 로드하려고 하는 정확한 URL을 볼 수 있습니다. 다음 정보를 보려면 다음을 수행하십시오.

1. [디버그 모드](#enable-debug-mode)에서 응용 프로그램을 시작하는 지침을 따르십시오.

1. 로그인 시도를 재현합니다.

1. 응용 프로그램의 [로그 디렉토리](#check-log-files-v2)로 이동합니다.

1. Windows의 경우:

   1. &quot;aemcomavrolog.txt&quot;를 엽니다.

   1. &quot;로그인 브라우저 주소가 다음으로 변경됨&quot;으로 시작하는 메시지를 검색합니다. 이러한 항목에는 애플리케이션이 로드되는 URL도 포함되어 있습니다.

   Mac의 경우:

   1. `com.adobe.aem.desktop-nnnnnnnn-nnnnnn.log`여기서  **** 은 최신 파일 이름에 있는 숫자로 대체됩니다.

   1. &quot;로드된 프레임&quot;으로 시작하는 메시지를 검색합니다. 이러한 항목에는 애플리케이션이 로드되는 URL도 포함되어 있습니다.


로드되는 URL 시퀀스를 보면 SAML의 끝에서 문제를 해결하여 무엇이 잘못되었는지 확인하는 데 도움이 될 수 있습니다.

### SSL 구성 문제 {#ssl-config-v2}

[!DNL Experience Manager] 데스크탑 앱에서 HTTP 통신에 사용하는 라이브러리는 엄격한 SSL 적용을 사용합니다. 때때로 브라우저를 사용하여 연결이 성공하지만 [!DNL Experience Manager] 데스크탑 앱을 사용하는 데 실패합니다. SSL을 적절하게 구성하려면 Apache에서 누락된 중간 인증서를 설치합니다. Apache](https://access.redhat.com/solutions/43575)에서 중간 CA 인증서를 설치하는 방법 을 참조하십시오.[

[!DNL Experience Manager] 데스크탑 앱에서 HTTP 통신에 사용하는 라이브러리는 엄격한 SSL 적용을 활용합니다. 따라서 [!DNL Adobe Experience Manager] 데스크탑 앱에서 브라우저를 통해 성공한 SSL 연결이 실패하는 인스턴스가 있을 수 있습니다. 이는 SSL을 올바르게 구성하도록 유도하고 보안을 강화하므로 좋지만 응용 프로그램이 연결할 수 없을 때 좌절할 수 있습니다.

이 경우 권장되는 접근 방법은 도구를 사용하여 서버의 SSL 인증서를 분석하고 문제를 식별하여 수정할 수 있는 것입니다. URL 제공 시 서버의 인증서를 검사하는 웹 사이트가 있습니다.

임시 조치로서, [!DNL Adobe Experience Manager] 데스크탑 앱에서 엄격한 SSL 적용을 비활성화할 수 있습니다. 잘못 구성된 SSL의 근본 원인을 숨겨서 보안을 감소하므로 이것은 권장되는 장기 솔루션이 아닙니다. 엄격한 적용을 사용하지 않도록 설정하려면 다음을 수행하십시오.

1. 선택한 편집기를 사용하여 응용 프로그램의 JavaScript 구성 파일을 편집합니다. 이 파일은 기본적으로 운영 체제에 따라 다음 위치에 있습니다.

   Mac에서: `/Applications/Adobe Experience Manager Desktop.app/Contents/Resources/javascript/lib-smb/config.json`

   Windows: `C:\Program Files (x86)\Adobe\Adobe Experience Manager Desktop\javascript\config.json`

1. 파일에서 다음 섹션을 찾습니다.

   ```shell
   ...
   "assetRepository": {
       "options": {
   ...
   ```

1. 다음과 같이 `"strictSSL": false`을 추가하여 섹션을 수정합니다.

   ```shell
   ...
   "assetRepository": {
       "options": {
           "strictSSL": false,
   ...
   ```

1. 파일을 저장하고 [!DNL Adobe Experience Manager] 데스크탑 앱을 다시 시작합니다.

### 다른 서버로 전환할 때 로그인 문제 {#cannot-login-cookies-issue}

[!DNL Experience Manager] 서버를 사용한 후에 다른 서버로 연결을 변경하려고 하면 로그인 문제가 발생할 수 있습니다. 새 인증을 방해하는 오래된 쿠키 때문입니다. 주 메뉴의 [!UICONTROL Clear Cookies] 옵션이 도움이 됩니다. 앱의 현재 세션에서 로그아웃하고 [!UICONTROL Clear Cookies] 을 선택하고 연결을 계속 진행합니다.

![서버 전환 시 쿠키 지우기](assets/main_menu_logout_da2.png)

## 앱이 응답하지 않습니다 {#unresponsive}

거의 응용 프로그램이 응답하지 않거나, 흰색 화면만 표시하거나, 인터페이스의 옵션 없이 인터페이스 하단에 오류를 표시할 수 있습니다. 다음 순서로 수행합니다.

* 애플리케이션 인터페이스를 마우스 오른쪽 버튼으로 클릭하고 **[!UICONTROL Refresh]** 를 클릭합니다.
* 애플리케이션을 종료하고 다시 엽니다.

두 방법 모두에서 앱은 루트 DAM 폴더에서 시작됩니다.

## 만료된 자산 숨기기 {#hide-expired-assets}

[!DNL Experience Manager] 사용자 인터페이스 내에서 자산을 검색할 때 만료된 자산이 표시되지 않습니다. 데스크탑 앱 및 자산 링크에서 자산을 검색할 때 만료된 자산을 보고, 검색하고, 가져올 수 없도록 관리자는 다음 구성을 수행할 수 있습니다. 구성은 관리자 권한에 관계없이 모든 사용자에 대해 작동합니다.

* [만료된 자산을 숨기도록 Experience Manager 6.5에서 구성](https://experienceleague.adobe.com/docs/experience-manager-65/assets/managing/manage-assets.html#hide-expired-assets-via-acp-api).
* [만료된 자산을 숨기도록 Experience Manager as a Cloud Service에서 구성](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/manage-digital-assets.html#hide-expired-assets-via-acp-api).

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

