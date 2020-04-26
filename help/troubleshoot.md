---
title: Adobe Experience Manager 데스크탑 앱 모범 사례 및 문제 해결
description: 모범 사례 및 문제 해결을 통해 설치, 업그레이드, 구성 등과 관련된 가끔 발생하는 문제를 해결할 수 있습니다.
uuid: ce98a3e7-5454-41be-aaaa-4252b3e0f8dd
contentOwner: AG
products: SG_EXPERIENCEMANAGER/6.3/ASSETS
discoiquuid: f5eb222a-6cdf-4ae3-9cf2-755c873f397c
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: b92e47456f9e16c24eac43d1c5fef9a582f143b5

---


# Troubleshoot Adobe Experience Manager desktop app {#troubleshoot-v2}

AEM(Adobe Experience Manager) 데스크탑 앱은 원격 Experience Manager 배포의 DAM 파섹 저장소에 연결됩니다. 앱은 컴퓨터에서 저장소 정보와 검색 결과를 가져오고, 파일 및 폴더를 다운로드 및 업로드하며, AEM Assets 사용자 인터페이스와 충돌을 관리하는 기능을 포함합니다.

앱의 문제를 해결하고, 모범 사례에 대해 알아보고, 제한 사항을 살펴보십시오.

## Best practices {#best-practices-to-prevent-troubles}

몇 가지 일반적인 문제 및 문제 해결을 방지하려면 다음 우수 사례를 따르십시오.

* **데스크탑 앱의 작동**&#x200B;방식 이해:애플리케이션을 사용하기 전에 앱이 어떻게 작동하는지 알기 위해 몇 분 동안 시간을 할애할 수 있습니다. 웹 UI와 데스크탑 간의 연결, 저장소 매핑, 자산 캐싱, 로컬에 저장 및 백그라운드에서 업로드에 대해 알아봅니다. 작동 [방식](release-notes.md#how-app-works)보기

* **폴더 이름에**&#x200B;지원되지 않는 문자를 사용하지 마십시오.폴더를 만들거나 업로드할 때 공백과 잘못된 문자를 사용하지 마십시오. Experience Manager 자산에서 폴더 [만들기에서 문자 목록을 참조하십시오](https://docs.adobe.com/content/help/en/experience-manager-65/assets/managing/managing-assets-touch-ui.html#Creatingfolders). 일부 Adobe Experience Manager 사용 사례는 폴더 이름에 지원되지 않는 문자로 인해 영향을 받을 수 있습니다.

* **충돌을**&#x200B;방지하기 위한 모범 사례:여러 자산에서 공동 작업할 때 발생할 수 있는 충돌을 방지하려면 편집 충돌을 [방지하십시오](using.md#adv-workflow-collaborate-avoid-conflicts).

* **대용량 계층적 폴더에**&#x200B;폴더 업로드 사용:Assets 웹 인터페이스나 다른 방법을 사용하는 대신 Experience Manager 데스크탑 앱을 사용하여 큰 폴더를 업로드하십시오. 앱은 로깅 및 모니터링으로 자산을 백그라운드에서 업로드합니다. 자산 [일괄 업로드를](using.md#bulk-upload-assets)참조하십시오.

* **최신 버전**&#x200B;사용:최신 앱 버전을 사용하고 항상 호환성을 확인한 후 새 앱 버전을 설치하거나 최신 Adobe Experience Manager 버전으로 업그레이드하십시오. See [release notes](release-notes.md).

* **동일한 드라이브 문자**&#x200B;사용:조직 전체에서 동일한 드라이브 문자를 사용하여 Adobe Experience Manager DAM에 매핑할 수 있습니다. 다른 사용자가 배치한 자산을 보려면 경로가 동일해야 합니다. 동일한 드라이브 문자를 사용하면 DAM 에셋에 대한 경로를 일관되게 유지할 수 있습니다. 다른 사용자가 다른 드라이브 문자를 사용하더라도 에셋은 배치된 상태로 유지되며 제거되지 않습니다.

* **네트워크**:네트워크 성능은 Experience Manager 데스크탑 앱의 성능에 매우 중요합니다. 파일 전송 또는 벌크 작업에 대한 응답 속도가 느려지면 네트워크 트래픽이 많을 수 있는 기능이나 앱을 끕니다.

* **데스크톱 앱에**&#x200B;지원되지 않는 사용 사례:자산의 마이그레이션에 앱을 사용하지 마십시오(계획 및 기타 도구 필요).대량의 DAM 작업(큰 폴더 이동, 대용량 업로드, 고급 메타데이터 검색을 사용하여 파일 찾기 등)동기화 클라이언트로(디자인 원칙 및 사용 패턴은 Microsoft OneDrive 또는 Adobe Creative Cloud 데스크탑 동기화와 같은 동기화 클라이언트와 다름)

* **시간 초과**:현재 데스크톱 앱에는 고정 시간 간격 이후 Experience Manager 서버와 데스크톱 앱 간의 연결을 해제하는 구성 가능한 시간 초과 값이 없습니다. 대용량 자산을 업로드할 때 잠시 후 연결이 시간 초과되면 업로드 시간 초과를 증가시켜 앱이 자산을 몇 번 업로드하기 위해 다시 시도합니다. 기본 시간 초과 설정을 변경하는 권장 방법은 없습니다.

## 문제 해결 방법 {#troubleshooting-prep}

데스크탑 앱 문제를 해결하려면 다음 정보를 참조하십시오. 또한 지원을 요청하는 경우 Adobe 고객 지원 센터에 문제를 보다 효과적으로 전달할 수 있습니다.

### 디버그 모드 활성화 {#enable-debug-mode}

문제를 해결하려면 디버그 모드를 활성화하고 로그에서 자세한 정보를 얻을 수 있습니다. Mac의 디버그 모드에서 앱을 사용하려면 터미널 또는 명령 프롬프트에서 다음 명령줄 옵션을 사용합니다. `AEM_DESKTOP_LOG_LEVEL=DEBUG open /Applications/Adobe\ Experience\ Manager\ Desktop.app`Adobe

Windows에서 디버그 모드를 활성화하려면 다음 단계를 수행합니다.

1. 데스크탑 앱 설치 폴더에서 `Adobe Experience Manager Desktop.exe.config` 파일을 찾습니다. 기본적으로 폴더는 `C:\Program Files\Adobe\Adobe Experience Manager Desktop`입니다. 파일을 저장하고 닫습니다.

1. 파일의 `<level value="INFO"/>` 끝 부분을 찾습니다. 값을 ( `DEBUG`즉,)으로 변경합니다 `<level value="DEBUG"/>`.

1. 데스크탑 앱 설치 폴더에서 `logging.json` 파일을 찾습니다. 기본적으로 폴더는 `C:\Program Files\Adobe\Adobe Experience Manager Desktop\javascript\`입니다.

1. 파일에서 매개 변수의 모든 인스턴스를 `logging.json` `level` 찾습니다. 값을 에서 `info` 로 `debug`변경합니다. 파일을 저장하고 닫습니다.

1. 앱 환경 설정에서 지정한 위치에 있는 캐시된 디렉터리를 지웁니다.

1. 데스크탑 앱을 다시 시작합니다.

<!-- The Windows command doesn't work for now.
* On Windows: `SET AEM_DESKTOP_LOG_LEVEL=DEBUG & "C:\Program Files\Adobe\Adobe Experience Manager Desktop\Adobe Experience Manager Desktop.exe"`
-->

### 로그 파일의 위치 {#check-log-files-v2}

다음 위치에서 AEM 데스크탑 앱용 로그 파일을 찾을 수 있습니다. 많은 자산을 업로드할 때 일부 파일이 업로드되지 않는 경우 파일을 참조하여 실패한 업로드를 확인합니다 `backend.log` .

* Windows의 경로: `%LocalAppData%\Adobe\AssetsCompanion\Logs`

* Mac의 경로: `~/Library/Logs/Adobe\ Experience\ Manager\ Desktop`

>[!NOTE]
>
>지원 요청/티켓을 통해 Adobe 고객 지원 센터에 문의할 때 고객 지원 팀에서 문제를 이해하는 데 도움이 되도록 로그 파일을 공유하라는 메시지가 표시될 수 있습니다. 전체 `Logs` 폴더를 보관하고 고객 지원 센터 담당자에게 공유합니다.

### 캐시 지우기 {#clear-cache-v2}

AEM 데스크톱 앱의 캐시를 지우는 것은 몇 가지 문제를 해결할 수 있는 예비 문제 해결 작업입니다. 앱 환경 설정에서 캐시를 지웁니다. 환경 설정 [설정을](install-upgrade.md#set-preferences)참조하십시오. 캐시 폴더의 기본 위치는 다음과 같습니다.

* Windows: `%LocalAppData%\Adobe\AssetsCompanion\Cache\`

* Mac: `~/Library/Group/Containers/group.com.adobe.aem.desktop/cache/`

그러나 AEM 데스크탑의 구성된 AEM 끝점에 따라 위치가 변경될 수 있습니다. 값은 타깃팅된 URL의 인코딩 버전입니다. 예를 들어 응용 프로그램이 타깃팅하는 경우 디렉토리 `http://localhost:4502`이름은 `http%3A%2F%2Flocalhost%3A4502%2F`입니다. 캐시를 지우려면 해당 폴더를 삭제합니다. 디스크 공간이 부족할 때 여유 디스크 공간이 확보되기 때문에 캐시를 지워야 합니다.

>[!CAUTION]
>
>AEM 데스크톱 캐시를 지우는 경우 AEM 서버에 동기화되지 않은 로컬 자산 수정은 절대 손실됩니다.

### AEM 데스크탑 앱 버전 이해 {#know-app-version-v2}

앱 ![메뉴를](assets/do-not-localize/more_options_da2.png) 클릭하여 앱의 메뉴를 열고 **[!UICONTROL Help]** > **[!UICONTROL About]**&#x200B;을 클릭합니다.

## 가져온 자산을 볼 수 없음 {#placed-assets-missing}

사용자 또는 기타 크리에이티브 전문가가 지원 파일에 배치한 에셋을 볼 수 없는 경우(예: INDD 파일) 다음을 확인하십시오.

* 서버에 연결합니다. 완벽한 네트워크 연결을 통해 에셋 다운로드를 중지할 수 있습니다.
* 파일 크기. 대용량 에셋을 다운로드하고 표시하는 데 시간이 오래 걸립니다.
* 글자의 일관성 향상 사용자나 다른 협력자가 AEM DAM을 다른 드라이브 문자로 매핑하는 동안 에셋을 배치했다면 가져온 에셋이 표시되지 않습니다.
* 권한. 가져온 자산을 가져올 권한이 있는지 확인하려면 AEM 관리자에게 문의하십시오.

## macOS에서 업그레이드할 때 발생하는 문제 {#issues-when-upgrading-on-macos}

macOS에서 AEM 데스크탑 앱을 업그레이드할 때 가끔 문제가 발생할 수 있습니다. 이는 AEM 데스크톱 앱용 레거시 시스템 폴더에서 AEM 데스크톱 앱의 새 버전이 제대로 로드되지 못했기 때문입니다. 이 문제를 해결하려면 다음 폴더 및 파일을 수동으로 제거할 수 있습니다.

다음 단계를 실행하기 전에 macOS 응용 프로그램 폴더의 `Adobe Experience Manager Desktop` 응용 프로그램을 휴지통으로 드래그합니다. 그런 다음 터미널을 열고 다음 명령을 실행하고 메시지가 표시되면 암호를 입력합니다.

```shell
sudo rm -rf ~/Library/Application\ Support/com.adobe.aem.desktop
sudo rm -rf ~/Library/Preferences/com.adobe.aem.desktop.plist
sudo rm -rf ~/Library/Logs/Adobe\ Experience\ Manager\ Desktop

sudo find /var/folders -type d -name "com.adobe.aem.desktop" | xargs rm -rf
sudo find /var/folders -type d -name "com.adobe.aem.desktop.finderintegration-plugin" | xargs rm -rf
```

## 파일을 업로드할 수 없음 {#upload-fails}

AEM 6.5.1 이상 버전의 데스크탑 앱을 사용하는 경우 S3 또는 Azure 커넥터를 버전 1.10.4 이상으로 업그레이드하십시오. 이 업데이트는 OAK-8599와 관련된 파일 [업로드 실패 문제를 해결합니다](https://issues.apache.org/jira/browse/OAK-8599). 설치 지침을 [참조하십시오](install-upgrade.md#install-v2).

## SSL 구성 문제 {#ssl-config-v2}

AEM 데스크톱 앱에서 HTTP 통신에 사용하는 라이브러리는 엄격한 SSL 적용을 사용합니다. 때때로 브라우저 사용에 성공하지만 AEM 데스크톱 앱을 사용하지 못할 수 있습니다. SSL을 적절히 구성하려면 Apache에 누락된 중간 인증서를 설치합니다. Apache [에서 중간 CA 인증서를 설치하는 방법을 참조하십시오](https://access.redhat.com/solutions/43575).

## 앱이 응답하지 않음 {#unresponsive}

거의 응용 프로그램이 응답하지 않거나 흰색 화면만 표시하거나 인터페이스 아래쪽에 오류가 표시되는 경우는 없습니다. 순서대로 다음 작업을 시도하십시오.

1. 애플리케이션 인터페이스를 마우스 오른쪽 버튼으로 클릭한 다음 을 **[!UICONTROL Refresh]**&#x200B;클릭합니다.
1. 애플리케이션을 종료하고 다시 시작합니다.

두 방법 모두에서 앱은 루트 DAM 폴더에서 시작됩니다.

>[!MORELIKETHIS]
>
>* [알려진 문제](release-notes.md#known-issues-v2)
>* [편집 충돌 방지](using.md#adv-workflow-collaborate-avoid-conflicts)