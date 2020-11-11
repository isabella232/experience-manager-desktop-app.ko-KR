---
title: Adobe Experience Manager 데스크탑 앱 문제 해결을 위한 모범 사례
description: 모범 사례 및 문제 해결을 따라 설치, 업그레이드, 구성 등과 관련된 가끔 발생하는 문제를 해결합니다.
uuid: ce98a3e7-5454-41be-aaaa-4252b3e0f8dd
contentOwner: AG
products: SG_EXPERIENCEMANAGER/6.5/ASSETS, SG_EXPERIENCEMANAGER/6.4/ASSETS, SG_EXPERIENCEMANAGER/6.3/ASSETS
discoiquuid: f5eb222a-6cdf-4ae3-9cf2-755c873f397c
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 200135fb96bbfcf9f72e857514bb9b71a88ed817
workflow-type: tm+mt
source-wordcount: '2228'
ht-degree: 0%

---


# Troubleshoot Adobe Experience Manager desktop app {#troubleshoot-v2}

Adobe Experience Manager(AEM) 데스크탑 앱은 원격 Experience Manager 배포의 DAM(Digital Asset Management) 저장소에 연결됩니다. 이 앱은 저장소 정보 및 검색 결과를 컴퓨터에서 가져오고, 파일 및 폴더를 다운로드 및 업로드하며, AEM Assets 사용자 인터페이스와 충돌을 관리하는 기능을 포함합니다.

앱 문제를 해결하고 모범 사례를 알아보고 제한 사항을 확인하십시오.

## Best practices {#best-practices-to-prevent-troubles}

몇 가지 일반적인 문제 및 문제 해결을 방지하려면 다음 우수 사례를 따르십시오.

* **데스크탑 앱의 작동 방식 이해**:애플리케이션 사용을 시작하기 전에 앱이 작동하는 방식을 알기 위해 잠시 시간을 할애하십시오. Experience Manager 웹 인터페이스와 데스크탑 간 연결, 저장소 매핑, 에셋 캐싱, 로컬에 저장, 백그라운드에서 업로드 등에 대해 자세히 알아보십시오. 사용 [방법](release-notes.md#how-app-works)보기

* **폴더 이름에 지원되지 않는 문자는 사용할 수 없습니다**.폴더를 만들거나 업로드할 때 공백과 잘못된 문자를 사용하지 마십시오. Experience Manager 자산에 폴더 [만들기에서 문자 목록을 참조하십시오](https://experienceleague.adobe.com/docs/experience-manager-65/assets/managing/manage-assets.html#creating-folders). 일부 Adobe Experience Manager 사용 사례는 폴더 이름에 지원되지 않는 문자로 인해 영향을 받을 수 있습니다.

* **충돌을 방지하는 모범 사례**:여러 에셋을 공동 작업할 때 발생할 수 있는 충돌을 방지하려면 편집 충돌 [을 방지하십시오](using.md#adv-workflow-collaborate-avoid-conflicts).

* **대용량 계층적 폴더에 대해 폴더 업로드 사용**:자산 웹 인터페이스나 다른 방법을 사용하는 대신 Experience Manager 데스크탑 앱을 사용하여 큰 폴더를 업로드합니다. 이 앱은 로깅 및 모니터링으로 자산을 백그라운드에서 업로드합니다. 자산 [일괄 업로드를 참조하십시오](using.md#bulk-upload-assets).

* **최신 버전**&#x200B;사용:최신 앱 버전을 사용하고, 새 앱 버전을 설치하거나 최신 Adobe Experience Manager 버전으로 업그레이드하기 전에 항상 호환성을 확인하십시오. See [release notes](release-notes.md).

* **동일한 드라이브 문자**&#x200B;사용:조직 전체에서 동일한 드라이브 문자를 사용하여 Adobe Experience Manager DAM에 매핑합니다. 다른 사용자가 배치한 자산을 보려면 경로가 동일해야 합니다. 동일한 드라이브 문자를 사용하면 DAM 에셋에 대한 경로를 일관되게 유지할 수 있습니다. 다른 사용자가 다른 드라이브 문자를 사용하더라도 에셋은 배치된 상태로 유지되며 제거되지 않습니다.

* **네트워크**:네트워크 성능은 데스크탑 앱 성능을 Experience Manager에 매우 중요합니다. 파일 전송 또는 벌크 작업에 대한 응답 속도가 느려지면 네트워크 트래픽이 많을 수 있는 기능이나 앱을 끕니다.

* **데스크탑 앱에 지원되지 않는 사용 사례**:자산의 마이그레이션에 앱을 사용하지 마십시오(계획 및 기타 도구 필요).대용량 DAM 작업(예: 대용량 폴더 이동, 대용량 업로드, 고급 메타데이터 검색을 사용한 파일 찾기);동기화 클라이언트로(디자인 원칙 및 사용 패턴은 Microsoft OneDrive 또는 Adobe Creative Cloud 데스크탑 동기화와 같은 인동기화 클라이언트와 다름)

* **시간 초과**:현재 데스크탑 앱에는 고정 시간 간격 이후 Experience Manager 서버와 데스크탑 앱 간의 연결을 연결하는 구성 가능한 시간 초과 값이 없습니다. 대용량 자산을 업로드할 때 잠시 후 연결이 시간 초과되면 업로드 시간 초과를 늘려 자산을 몇 번 업로드하기 위해 앱이 재시도합니다. 기본 시간 초과 설정을 변경하는 권장 방법은 없습니다.

## 문제 해결 방법 {#troubleshooting-prep}

데스크탑 앱 문제를 해결하려면 다음 정보를 참조하십시오. 또한 지원을 요청하려는 경우 Adobe 고객 지원 센터에 문제를 보다 효과적으로 전달할 수 있습니다.

### 로그 파일의 위치 {#check-log-files-v2}

[!DNL Experience Manager] 데스크탑 앱은 운영 체제에 따라 다음 위치에 로그 파일을 저장합니다.

Windows: `%LocalAppData%\Adobe\AssetsCompanion\Logs`

Mac: `~/Library/Logs/Adobe\ Experience\ Manager\ Desktop`

많은 자산을 업로드할 때 일부 파일이 업로드되지 않으면 실패한 업로드를 식별하는 파일을 참조하십시오 `backend.log` .

>[!NOTE]
>
>지원 요청이나 티켓 구입 시 Adobe 고객 지원 센터에 문의할 때 고객 지원 팀이 문제를 이해하는 데 도움이 되도록 로그 파일을 공유하라는 메시지가 나타납니다. 전체 `Logs` 폴더를 보관하고 고객 지원 센터 담당자와 공유합니다.

### 로그 파일의 세부 정보 수준 변경 {#level-of-details-in-log}

로그 파일의 세부 사항 수준을 변경하려면 다음을 수행하십시오.

1. 응용 프로그램이 실행되고 있지 않은지 확인합니다.

1. Windows 시스템의 경우:

   1. 명령 창을 엽니다.

   1. 다음 명령을 실행하여 데스크탑 [!DNL Adobe Experience Manager] 앱을 실행합니다.

   ```shell
   set AEM_DESKTOP_LOG_LEVEL=DEBUG&"C:\Program Files\Adobe\Adobe Experience Manager Desktop.exe
   ```

   Mac 시스템의 경우:

   1. 터미널 창을 엽니다.

   1. 다음 명령을 실행하여 데스크탑 [!DNL Adobe Experience Manager] 앱을 실행합니다.

   ```shell
   AEM_DESKTOP_LOG_LEVEL=DEBUG open /Applications/Adobe\ Experience\ Manager\ Desktop.app
   ```

유효한 로그 수준은 디버그, 정보, 경고 또는 오류입니다. 로그의 범위는 DEBUG에서 가장 높고 ERROR에서는 가장 낮습니다.

### 디버그 모드 활성화 {#enable-debug-mode}

문제를 해결하려면 디버그 모드를 활성화하고 로그에서 자세한 정보를 얻을 수 있습니다.

>[!NOTE]
>
>유효한 로그 수준은 디버그, 정보, 경고 또는 오류입니다. 로그의 범위는 DEBUG에서 가장 높고 ERROR에서는 가장 낮습니다.

Mac에서 디버그 모드에서 앱을 사용하려면:

1. 터미널 창 또는 명령 프롬프트를 엽니다.

1. 다음 명령을 실행하여 [!DNL Experience Manager] 데스크탑 앱을 실행합니다.

   `AEM_DESKTOP_LOG_LEVEL=DEBUG open /Applications/Adobe\ Experience\ Manager\ Desktop.app`.

Windows에서 디버그 모드를 활성화하려면:

1. 명령 창을 엽니다.

1. 다음 명령을 실행하여 데스크탑 [!DNL Experience Manager] 앱을 실행합니다.

`AEM_DESKTOP_LOG_LEVEL=DEBUG&"C:\Program Files\Adobe\Adobe Experience Manager Desktop.exe`.

### 캐시 지우기 {#clear-cache-v2}

다음 단계를 수행합니다.

1. 응용 프로그램을 시작하고 AEM 인스턴스를 연결합니다.

1. 오른쪽 상단 모서리의 줄임표를 클릭하고 선택하여 애플리케이션의 기본 설정을 엽니다 [!UICONTROL Preferences].

1. 항목을 표시하는 항목을 찾습니다 [!UICONTROL Current Cache Size]. 이 요소 옆에 있는 휴지통 아이콘을 클릭합니다.

캐시를 수동으로 지우려면 아래 단계를 수행하십시오.

>[!CAUTION]
>
>이것은 잠재적으로 파괴적인 수술이다. 업로드되지 않은 로컬 파일 변경 사항이 [!DNL Adobe Experience Manager]있는 경우 계속 진행하면 변경 내용이 손실됩니다.

응용 프로그램의 기본 설정에 있는 응용 프로그램의 캐시 디렉토리를 삭제하여 캐시를 지웁니다.

1. 애플리케이션을 시작합니다.

1. 오른쪽 상단 모서리의 줄임표를 선택하고 선택하여 애플리케이션의 기본 설정을 엽니다 [!UICONTROL Preferences].

1. 값을 [!UICONTROL Cache Directory] 확인합니다.

   이 디렉토리에는 인코딩된 끝점의 이름을 딴 하위 디렉토리가 [!DNL Adobe Experience Manager] 있습니다. 이름은 대상 [!DNL Adobe Experience Manager] URL의 인코딩 버전입니다. 예를 들어 응용 프로그램이 타깃팅하는 경우 디렉토리 이름 `localhost:4502` 이 됩니다 `localhost_4502`.

캐시를 지우려면 원하는 인코딩 끝점 [!DNL Adobe Experience Manager] 디렉터리를 삭제합니다. 또는 환경 설정에 지정된 전체 디렉토리를 삭제하면 애플리케이션에서 사용한 모든 인스턴스에 대한 캐시가 지워집니다.

데스크톱 [!DNL Adobe Experience Manager] 앱의 캐시를 지우려면 몇 가지 문제를 해결할 수 있는 임시 문제 해결 작업입니다. 앱 환경 설정에서 캐시를 지웁니다. 환경 설정 [설정을 참조하십시오](install-upgrade.md#set-preferences). 캐시 폴더의 기본 위치는 다음과 같습니다.

### 데스크탑 [!DNL Adobe Experience Manager] 앱 버전 이해 {#know-app-version-v2}

버전 번호를 보려면

1. 애플리케이션을 시작합니다.

1. 오른쪽 상단 모서리의 줄임표를 클릭하고 마우스 위로 마우스를 가져간 다음 [!UICONTROL Help]을 클릭합니다 [!UICONTROL About].

   버전 번호가 이 화면에 나와 있습니다.

### 배치된 자산을 볼 수 없음 {#placed-assets-missing}

사용자 또는 기타 크리에이티브 전문가가 지원 파일에 가져온 에셋을 볼 수 없는 경우(예: INDD 파일) 다음을 확인하십시오.

* 서버에 연결합니다. 네트워크 연결이 끊어지면 자산 다운로드가 중단될 수 있습니다.

* 파일 크기. 대용량 에셋을 다운로드하고 표시하는 데 시간이 오래 걸립니다.

* 일관된 문자 경험 제공 사용자나 다른 협력자가 AEM DAM을 다른 드라이브 문자로 매핑하는 동안 에셋을 배치하면 배치된 에셋이 표시되지 않습니다.

* 권한. 가져온 자산을 가져올 권한이 있는지 확인하려면 AEM 관리자에게 문의하십시오.

### 데스크톱 앱의 사용자 인터페이스에서 파일을 편집해도 [!DNL Adobe Experience Manager] 즉시 {#changes-on-da-not-visible-on-aem}

[!DNL Adobe Experience Manager] 데스크탑 앱은 모든 파일 편집 완료 시간을 사용자에게 알려줍니다. 파일의 크기와 복잡도에 따라 새로운 버전의 파일을 다시 전송하기까지 상당한 시간이 소요됩니다 [!DNL Adobe Experience Manager]. 파일 편집이 완료되고 자동으로 업로드되는 시기를 추측하는 대신, 응용 프로그램 디자인에서 파일을 주고 받는 횟수를 최소화해야 합니다. 사용자는 파일 변경 내용을 업로드하도록 선택하여 파일 [!DNL Adobe Experience Manager] 의 전송을 다시 시작하는 것이 좋습니다.

### macOS에서 업그레이드할 때 발생하는 문제 {#issues-when-upgrading-on-macos}

macOS에서 AEM 데스크탑 앱을 업그레이드할 때 가끔 문제가 발생할 수 있습니다. AEM 데스크탑 앱용 레거시 시스템 폴더에서 AEM 데스크톱 앱의 새 버전이 올바르게 로드되지 않기 때문입니다. 이 문제를 해결하려면 다음 폴더 및 파일을 수동으로 제거할 수 있습니다.

다음 단계를 실행하기 전에 macOS 응용 프로그램 폴더의 `Adobe Experience Manager Desktop` 응용 프로그램을 휴지통으로 드래그합니다. 그런 다음 터미널을 열고 다음 명령을 실행하고 메시지가 표시되면 암호를 입력합니다.

```shell
sudo rm -rf ~/Library/Application\ Support/com.adobe.aem.desktop
sudo rm -rf ~/Library/Preferences/com.adobe.aem.desktop.plist
sudo rm -rf ~/Library/Logs/Adobe\ Experience\ Manager\ Desktop

sudo find /var/folders -type d -name "com.adobe.aem.desktop" | xargs rm -rf
sudo find /var/folders -type d -name "com.adobe.aem.desktop.finderintegration-plugin" | xargs rm -rf
```

### 파일을 업로드할 수 없음 {#upload-fails}

AEM 6.5.1 이상에서 데스크탑 앱을 사용하는 경우 S3 또는 Azure 커넥터를 버전 1.10.4 이상으로 업그레이드하십시오. 이 업데이트는 [OAK-8599와 관련된 파일 업로드 실패 문제를 해결합니다](https://issues.apache.org/jira/browse/OAK-8599). 설치 [지침을 참조하십시오](install-upgrade.md#install-v2).

### [!DNL Experience Manager] 데스크탑 앱 연결 문제 {#connection-issues}

일반적인 연결 문제가 발생하는 경우 데스크톱 응용 프로그램의 기능에 대한 자세한 정보를 얻을 수 있는 몇 가지 방법이 [!DNL Experience Manager] 있습니다.

**요청 로그 확인**

[!DNL Experience Manager] 데스크탑 앱은 각 요청의 응답 코드와 함께 전송된 모든 요청을 전용 로그 파일에 기록합니다.

1. 응용 프로그램 `request.log` 의 로그 디렉토리에서 열어 이러한 요청을 확인합니다.

1. 로그의 각 줄은 요청이나 응답을 나타냅니다. 요청에는 `>` 문자가 뒤에 요청된 URL이 옵니다. 응답에는 `<` 문자 뒤에 응답 코드와 요청된 URL이 추가됩니다. 각 라인의 GUID를 사용하여 요청 및 응답을 일치시킬 수 있습니다.

**응용 프로그램의 포함된 브라우저가 로드한 요청 확인**

응용 프로그램 요청의 대부분은 요청 로그에 있습니다. 그러나 여기에 유용한 정보가 없으면 응용 프로그램의 임베디드 브라우저가 보낸 요청을 검토하는 것이 유용합니다.
이러한 요청을 보는 방법에 대한 자세한 내용은 [SAML 섹션을](#da-connection-issue-with-saml-aem) 참조하십시오.

#### SAML 로그인 인증이 작동하지 않음 {#da-connection-issue-with-saml-aem}

데스크탑 [!DNL Experience Manager] [!DNL Adobe Experience Manager] 앱이 SSO 활성화(SAML) 인스턴스에 연결되지 않은 경우 이 섹션을 참조하여 문제를 해결하십시오. SSO 프로세스는 다양하며 복잡하기도 하며 이러한 유형의 연결을 수용할 수 있도록 애플리케이션의 디자인이 효과적입니다. 그러나 일부 설정에 추가적인 문제 해결 작업이 필요합니다.

경우에 따라 SAML 프로세스가 원래 요청된 경로로 리디렉션되지 않거나 최종 리디렉션이 [!DNL Adobe Experience Manager] 데스크탑 앱에서 구성된 것과 다른 호스트로 리디렉션되는 경우가 있습니다. 이러한 경우가 아님을 확인하려면

1. 웹 브라우저를 엽니다.

1. 주소 표시줄에 URL `<AEM host>/content/dam.json` 을 입력합니다.

   예를 들어 대상 인스턴스 `<AEM host>` 로 [!DNL Adobe Experience Manager] 대체합니다 `http://localhost:4502/content/dam.json`.

1. 인스턴스에 [!DNL Adobe Experience Manager] 로그인합니다.

1. 로그인이 완료되면 주소 표시줄에서 브라우저의 현재 주소를 확인합니다. 처음에 입력한 URL과 정확하게 일치해야 합니다.

1. 또한 이전의 모든 내용이 `/content/dam.json` 데스크톱 앱 설정에 구성된 대상 [!DNL Adobe Experience Manager] [!DNL Adobe Experience Manager] 값과 일치하는지 확인하십시오.

**로그인 SAML 프로세스는 위의 단계에 따라 올바르게 작동하지만 사용자는 여전히 로그인할 수 없습니다**

로그인 프로세스를 표시하는 [!DNL Adobe Experience Manager] 데스크톱 앱 내의 창은 단순히 대상 [!DNL Adobe Experience Manager] 인스턴스의 웹 사용자 인터페이스를 표시하는 웹 브라우저입니다.

* Mac 버전에서는 [WebView를 사용합니다](https://developer.apple.com/documentation/webkit/webview).

* Windows 버전은 Chromium 기반 CefSharp를 [사용합니다](https://cefsharp.github.io/).

SAML 프로세스가 이러한 브라우저를 지원하는지 확인합니다.

문제를 더 해결하기 위해 브라우저가 로드하려고 하는 정확한 URL을 볼 수 있습니다. 이 정보를 보려면:

1. 디버그 모드에서 응용 프로그램을 시작하는 방법에 [따릅니다](#enable-debug-mode).

1. 로그인 시도를 재현합니다.

1. 애플리케이션의 [로그 디렉토리](#check-log-files-v2) 탐색

1. Windows의 경우:

   1. &quot;aemunowlog.txt&quot;를 엽니다.

   1. &quot;로그인 브라우저 주소가 다음으로 변경됨&quot;으로 시작하는 메시지를 검색합니다. 이러한 항목에는 애플리케이션이 로드한 URL도 포함되어 있습니다.

   Mac:

   1. `com.adobe.aem.desktop-nnnnnnnn-nnnnnn.log`가 **있는** 경우 n이 최신 파일 이름에 있는 숫자로 대체됩니다.

   1. &quot;로드된 프레임&quot;으로 시작하는 메시지를 검색합니다. 이러한 항목에는 애플리케이션이 로드한 URL도 포함되어 있습니다.


로드되고 있는 URL 시퀀스를 보면 SAML의 끝에서 문제를 해결하고 무엇이 잘못되었는지 확인하는 데 도움이 될 수 있습니다.

#### SSL 구성 문제 {#ssl-config-v2}

AEM 데스크톱 앱이 HTTP 통신에 사용하는 라이브러리는 엄격한 SSL 적용을 사용합니다. 경우에 따라 브라우저 사용에 성공하지만 AEM 데스크탑 앱을 사용하지 못할 수도 있습니다. SSL을 적절하게 구성하려면 Apache에 누락된 중간 인증서를 설치합니다. Apache [에서 중간 CA 인증서를 설치하는 방법을 참조하십시오](https://access.redhat.com/solutions/43575).


AEM Desktop에서 HTTP 통신에 사용하는 라이브러리는 엄격한 SSL 적용을 사용합니다. 따라서 [!DNL Adobe Experience Manager] 데스크탑 앱에서 브라우저를 통해 성공한 SSL 연결이 실패하는 인스턴스가 있을 수 있습니다. 이 기능은 SSL의 올바른 구성을 권장하고 보안을 강화하지만 응용 프로그램이 연결할 수 없을 때 좌절감을 줄 수 있습니다.

이 경우 도구를 사용하여 서버의 SSL 인증서를 분석하고 문제를 식별하여 수정할 수 있도록 하는 것이 좋습니다. URL을 제공할 때 서버 인증서를 검사하는 웹 사이트가 있습니다.

임시 측정은 데스크톱 앱에서 엄격한 SSL 적용을 비활성화할 수 [!DNL Adobe Experience Manager] 있습니다. SSL이 잘못 구성된 근본 원인을 숨겨서 보안을 낮추기 때문에 권장되는 장기 솔루션은 아닙니다. 엄격한 적용을 비활성화하려면

1. 원하는 편집기를 사용하여 다음 위치(운영 체제에 따라)에서 기본적으로 찾을 수 있는 애플리케이션의 JavaScript 구성 파일을 편집합니다.

   Mac: `/Applications/Adobe Experience Manager Desktop.app/Contents/Resources/javascript/lib-smb/config.json`

   Windows: `C:\Program Files (x86)\Adobe\Adobe Experience Manager Desktop\javascript\config.json`

1. 파일에서 다음 섹션을 찾습니다.

   ```shell
   ...
   "assetRepository": {
       "options": {
   ...
   ```

1. 다음과 같이 추가하여 섹션 `"strictSSL": false` 을 수정합니다.

   ```shell
   ...
   "assetRepository": {
       "options": {
           "strictSSL": false,
   ...
   ```

1. 파일을 저장하고 데스크탑 [!DNL Adobe Experience Manager] 앱을 다시 시작합니다.

### 앱이 응답하지 않음 {#unresponsive}

거의 애플리케이션이 응답하지 않거나 흰색 화면만 표시하거나 인터페이스 아래쪽에 오류가 표시되는 경우가 있습니다. 다음 순서대로 시도하십시오.

* 애플리케이션 인터페이스를 마우스 오른쪽 버튼으로 클릭하고 을 클릭합니다 **[!UICONTROL Refresh]**.
* 애플리케이션을 종료하고 다시 엽니다.

두 방법 모두에서 앱은 루트 DAM 폴더에서 시작됩니다.

### 데스크탑 앱에 대한 추가 도움말 [!DNL Experience Manager] 필요 {#additional-help}

다음 정보가 포함된 Jira 티켓을 만듭니다.

* 를 `DAM - Companion App` 사용하여 [!UICONTROL Component]작업하십시오.

* 문제를 재현하는 자세한 단계입니다 [!UICONTROL Description].

* 문제를 복제하는 동안 캡처한 DEBUG 수준 로그.

* Target AEM 버전.

* 운영 체제 버전.

* [!DNL Adobe Experience Manager] 데스크탑 앱 버전. 앱 버전을 확인하려면 데스크탑 앱 버전 [을 찾아보십시오](#know-app-version-v2).

>[!MORELIKETHIS]
>
>* [알려진 문제](release-notes.md#known-issues-v2)
>* [편집 충돌 방지](using.md#adv-workflow-collaborate-avoid-conflicts)

