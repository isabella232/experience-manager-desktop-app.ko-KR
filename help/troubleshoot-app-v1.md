---
title: AEM 데스크톱 앱 버전 1.x 문제 해결
seo-title: AEM 데스크탑 앱 문제 해결
description: 설치, 업그레이드, 구성 등과 관련된 가끔 발생하는 문제를 해결하려면 AEM 데스크탑 앱 버전 1.x 문제를 해결하십시오.
seo-description: 설치, 업그레이드, 구성 등과 관련된 가끔 발생하는 문제를 해결하려면 AEM 데스크탑 앱 버전 1.x 문제를 해결하십시오.
uuid: ce98a3e7-5454-41be-aaaa-4252b3e0f8dd
contentOwner: asgupta
products: SG_EXPERIENCEMANAGER/6.3/ASSETS
discoiquuid: f5eb222a-6cdf-4ae3-9cf2-755c873f397c
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 7ce29042aff6d4caea0e7b8a56673d4bfed03a45

---


# AEM 데스크탑 앱 v1.x 문제 해결 {#troubleshoot-aem-desktop-app}

설치, 업그레이드, 구성 등과 관련된 가끔 발생하는 문제를 해결하려면 AEM 데스크탑 앱 문제를 해결하십시오.

AEM(Adobe Experience Manager) 데스크탑 앱에는 AEM 자산 저장소를 데스크탑에서 네트워크 공유(Mac OS에서 SMB 공유)로 매핑하는 데 도움이 되는 유틸리티가 포함되어 있습니다. 네트워크 공유는 원격 소스를 컴퓨터의 로컬 파일 시스템에 속한 것처럼 처리할 수 있는 운영 체제 기술입니다. 데스크톱 앱의 경우 원격 AEM 인스턴스의 DAM 파섹 저장소 구조가 원격 파일 소스로 타깃팅됩니다. 다음 다이어그램은 데스크탑 앱 토폴로지에 대해 설명합니다.

![데스크탑 앱 다이어그램](assets/aem-desktopapp-architecture.png)

이 아키텍처를 사용하여 데스크톱 앱은 마운트된 네트워크 공유에 대한 파일 시스템 호출(열기, 닫기, 읽기, 쓰기 등)을 가로채서 AEM 서버에 대한 기본 AEM HTTP 호출로 변환합니다. 파일은 로컬에 캐시됩니다. 자세한 내용은 AEM [데스크톱 앱 v1.x](use-app-v1.md)사용을 참조하십시오.

## 데스크탑 앱 구성 요소 개요 {#desktop-nbsp-app-component-overview}

데스크탑 앱에는 다음 구성 요소가 포함되어 있습니다.

* **데스크탑 애플리케이션**:DAM을 원격 파일 시스템으로 마운트/마운트 해제하고 로컬로 마운트된 네트워크 공유와 연결된 원격 AEM 인스턴스 간의 파일 시스템 호출을 변환할 수 있습니다.
* **운영 체제 WebDAV/SMB 클라이언트**:Windows 탐색기/Finder와 데스크탑 앱 간의 통신을 처리합니다. 파일이 검색, 작성, 수정, 삭제, 이동 또는 복사되면 운영 체제(OS) WebDAV/SMB 클라이언트는 이 작업을 데스크탑 앱으로 전달합니다. 통신을 수신한 데스크톱 앱은 이를 기본 AEM 원격 API 호출로 변환합니다. 예를 들어, 사용자가 마운트된 디렉토리에 파일을 만드는 경우 WebDAV/SMB 클라이언트가 요청을 시작하면 데스크탑 앱이 DAM에서 파일을 생성하는 HTTP 요청으로 변환됩니다. WebDAV/SMB 클라이언트는 OS에 내장된 구성 요소입니다. 데스크탑 앱, AEM 또는 Adobe와 어떠한 방식으로든 연계되지 않습니다.
* **Adobe Experience Manager 인스턴스**:AEM Assets DAM 저장소에 저장된 자산에 대한 액세스를 제공합니다. 또한, 탑재된 네트워크 공유와 상호 작용하는 로컬 데스크톱 응용 프로그램을 대신하여 데스크톱 응용 프로그램에서 요청한 작업을 수행합니다. 대상 AEM 인스턴스는 AEM 버전 6.1 이상을 실행해야 합니다. 이전 AEM 버전을 실행하는 AEM 인스턴스에는 완전히 작동하도록 추가 기능 팩과 핫픽스가 설치되어 있어야 할 수 있습니다.

## AEM 데스크톱 앱에 대한 사용 사례 {#intended-use-cases-for-aem-desktop-app}

AEM 데스크탑 앱은 네트워크 공유 기술을 사용하여 원격 AEM 리포지토리를 로컬 데스크탑에 매핑합니다. 그러나 사용자가 로컬 데스크탑에서 직접 디지털 에셋 관리 작업을 수행하는 네트워크 공유 에셋을 대체하는 것이 아닙니다. 여기에는 여러 파일을 이동하거나 복사하거나, 큰 폴더 구조를 Finder/탐색기에서 직접 AEM 자산 네트워크 공유로 드래그하는 작업이 포함됩니다.

AEM 데스크톱 앱은 AEM Assets Touch UI와 로컬 데스크톱 간에 DAM 자산을 액세스(열기)하고 편집(저장)하는 편리한 방법을 제공합니다. AEM 자산 서버의 자산을 데스크톱 기반 워크플로우와 연결합니다.

다음 사용 예는 AEM Desktop을 어떻게 사용해야 하는지를 보여줍니다.

* 사용자가 AEM에 로그인하고 웹 UI를 사용하여 자산을 찾습니다.
* 사용자는 AEM 웹 UI의 데스크톱 작업 기능을 사용하여 필요에 따라 데스크탑에서 자산을 열고, 표시하거나 편집합니다.
* AEM Desktop은 자산의 파일 유형에 대한 기본 편집기에서 자산을 엽니다.
* 사용자가 자산을 변경합니다.
* 파일이 수정되면 사용자는 AEM Desktop의 백그라운드 동기화 상태 창을 사용하여 파일의 동기화 상태를 볼 수 있습니다.
* 사용자는 AEM Desktop의 컨텍스트 메뉴를 사용하여 자산을 체크 인/체크 아웃하거나 DAM 사용자 인터페이스로 돌아갑니다.
* 파일 변경 작업을 완료한 후 사용자는 AEM 웹 UI로 돌아갑니다

이 사례만이 아닙니다. 하지만 AEM Desktop이 자산을 로컬로 액세스/편집할 수 있는 편리한 메커니즘인 방법을 설명합니다. DAM 웹 UI는 더 나은 환경을 제공하므로 가능한 한 많이 사용하는 것이 좋습니다. Adobe는 고객 요구 사항을 보다 유연하게 충족할 수 있습니다.

## 제한 사항 {#limitations}

WebDAV/SMB1 네트워크 공유 기능을 사용하면 탐색기/파인더 창에서 편리하게 파일을 작업할 수 있습니다. 그러나 탐색기/Finder 및 AEM은 특정 제한 사항이 있는 네트워크 연결을 통해 통신합니다. 예를 들어 1GB 파일을 마운트된 WebDAV/SMB 디렉토리에 복사하는 데 걸리는 시간은 웹 브라우저를 사용하여 웹 사이트에 1GB 파일을 업로드하는 데 필요한 시간과 거의 동일합니다. 실제로 이전의 경우 WebDAV/SMB 프로토콜과 OS의 WebDAV/SMB 클라이언트(특히 Mac OS X)의 비효율성 때문에 지속 시간이 더 길어질 수 있습니다.

마운트된 디렉토리에서 수행할 수 있는 작업 유형에는 제한이 있습니다. 일반적으로 큰 파일을 편집하는 경우 특히 지연/대기 시간이 높거나 대역폭 사용량이 낮은 네트워크 연결을 통해 대용량 파일을 작업하는 것이 어려울 수 있습니다.

Adobe에서는 마운트된 디렉토리에서 특정 유형의 파일을 효율적으로 직접 편집할 수 있도록 클라이언트에 커밋하기 전에 일부 사용 사례 테스트를 수행하는 것이 좋습니다.

AEM Desktop은 다음을 포함하나 이에 국한되지 않고 집중적인 파일 시스템 조작을 수행하는 데 적합하지 않습니다.

* 파일 및 디렉토리 이동 또는 복사
* AEM에 많은 자산 추가
* 폴더 검색을 제외한 파일 시스템을 통해 파일 검색 및 열기
* 파일 아카이브 압축 또는 압축 해제

운영 체제의 제한 사항으로 인해 Windows의 파일 크기는 4,294,967,295바이트(약 4.29GB)로 제한됩니다. 네트워크 공유의 파일 크기를 정의하는 레지스트리 설정 때문입니다. 레지스트리 설정의 값은 참조된 번호와 같은 최대 크기의 DWORD입니다.

## AEM을 사용한 캐싱 및 통신 {#caching-and-communication-with-aem}

AEM 데스크톱 앱은 최종 사용자 경험을 개선하기 위해 내부 캐싱 및 백그라운드 업로드 기능을 제공합니다. 큰 파일을 저장하면 로컬에 저장되어 작업을 계속할 수 있습니다. 이후(현재 30초) 파일은 백그라운드에서 AEM 서버로 전송됩니다.

Creative Cloud 데스크톱 또는 기타 파일 동기화 솔루션과 달리 AEM 데스크탑 앱은 전체 데스크탑 동기화 클라이언트가 아닙니다. 이러한 이유는 전체 동기화를 위해 매우 큰(수백 GB 또는 테라바이트)의 전체 AEM 자산 저장소에 대한 액세스를 제공하기 때문입니다.

캐싱은 네트워크/스토리지 오버헤드를 사용자와 관련된 자산 하위 집합으로 제한할 수 있습니다.

다음은 AEM 데스크톱 응용 프로그램에서 캐시를 수행하는 방법입니다.

* Finder에서 폴더를 열고 파일의 축소판/미리 보기가 표시되거나 응용 프로그램에서 파일을 열면 데스크톱 응용 프로그램이 파일 바이너리를 캐시합니다.
* Finder 또는 다른 데스크탑 애플리케이션을 통해 파일을 저장할 때 파일이 먼저 로컬에 저장되고(캐시됨) 운영 체제에 알림이 표시됩니다. 그러면 파일이 백그라운드에서 서버에 업로드하기 위해 큐에 올라가 네트워크를 통해 업로드됩니다. 네트워크 오류가 발생하는 경우 데스크톱 응용 프로그램에서 전체 파일 업로드를 최대 3번 재시도합니다. 3회 재시도 후 업로드하지 못한 경우 파일이 충돌하는 파일로 표시되고 백그라운드 업로드 대기열 상태 창을 통해 상태가 표시됩니다. 데스크톱 앱이 더 이상 파일을 업데이트하지 않습니다. 연결을 복원한 후 파일을 업데이트하고 다시 업로드해야 합니다

모든 작업은 로컬로 캐시되지 않습니다. 다음은 로컬 캐싱 없이 AEM Server로 즉시 전송됩니다.

* 만들기, 삭제 등과 같은 폴더의 모든 작업
* 버전 1.4에 도입된 폴더 업로드 기능은 로컬에 파일을 캐시하지 않고 로컬 폴더 계층 구조를 업로드합니다.

## 개별 작업 {#individual-operations}

개별 사용자에 대해 하위 최적화 성능을 해결하는 경우 먼저 제한 사항을 [검토하십시오](https://helpx.adobe.com/experience-manager/desktop-app/troubleshooting-desktop-app.html#limitations). 이후 섹션에는 개별 사용자에 대한 성능 향상을 위한 제안이 포함됩니다.

## 대역폭 권장 사항 {#bandwidth-recommendations}

개별 사용자가 사용할 수 있는 대역폭은 WebDAV/SMB 클라이언트의 성능에 중요한 역할을 합니다.

Adobe에서는 개별 사용자의 업로드 속도가 10Mbps에 가까울 것을 권장합니다. 무선 연결의 경우 대역폭을 여러 사용자 간에 공유하는 경우가 많습니다. 여러 사용자가 네트워크 대역폭을 사용하는 작업을 동시에 수행하는 경우 성능이 더 저하될 수 있습니다. 이러한 문제를 방지하려면 유선 연결을 사용하십시오.

## Windows 전용 구성 {#windows-specific-configurations}

Windows에서 AEM을 실행하는 경우 WebDAV 클라이언트의 성능을 향상하도록 Windows를 구성할 수 있습니다. 자세한 내용은 https://support.microsoft.com/en-us/kb/2445570을 [참조하십시오](https://support.microsoft.com/en-us/kb/2445570).

Windows 7에서 IE 설정을 수정하면 WebDAV의 성능이 향상될 수 있습니다. 자세한 내용은 http://oddballupdate.com/2009/12/fix-slow-webdav-performance-in-windows-7/을 [참조하십시오](http://oddballupdate.com/2009/12/fix-slow-webdav-performance-in-windows-7/).

## 동시 작업 {#concurrent-operations}

로컬로 파일과 상호 작용하는 경우 AEM Desktop은 AEM에서 최신 버전의 파일을 사용할 수 있는지 여부를 확인합니다. 새 버전을 사용할 수 있는 경우 응용 프로그램은 로컬 캐시에 파일의 새 복사본을 다운로드합니다. 그러나 AEM Desktop은 로컬에 캐시된 파일을 수정한 경우 덮어쓰지 않습니다. 이 기능을 사용하면 실수로 작업을 덮어쓰지 않습니다.

동일한 파일이 로컬과 AEM에서 모두 수정되면 로컬에서 수정된 버전이 AEM의 버전을 덮어씁니다. 이 경우 이전 버전은 자산의 타임라인에서 사용할 수 있습니다. 두 버전을 모두 확인하고 충돌을 해결할 수 있습니다.

로컬 파일이 서버에서 사용할 수 있는 버전과 일치하지 않는 경우 배경 업로드 상태 대화 상자에서 충돌 사실을 알려줍니다. 문제를 해결하려면 충돌하는 파일을 열고 저장합니다. 파일을 저장하면 AEM Desktop이 최신 로컬 변경 사항을 AEM에 동기화합니다. 타임라인에서 이전 버전의 에셋을 보고 충돌을 해결할 수 있습니다.

여러 사용자가 동일한 AEM 인스턴스를 타깃팅하는 별도의 마운트된 디렉토리에서 작업하려고 할 때 추가적인 요소를 고려해야 합니다. 특히 다음 요소가 중요합니다.

* 사용자의 원래 네트워크에서 사용할 수 있는 대역폭
* 원래 네트워크의 방화벽 또는 프록시 등의 네트워크 구성
* 대상 AEM 인스턴스의 네트워크에서 사용할 수 있는 대역폭 크기
* 대상 AEM 인스턴스 앞에 디스패처가 있는지 여부
* 대상 AEM 인스턴스의 현재 로드

## 추가 AEM 구성 {#additional-aem-configurations}

여러 사용자가 동시에 작업할 때 WebDAV/SMB 성능이 크게 저하되는 경우 AEM에서 몇 가지 사항을 구성하여 성능을 향상시킬 수 있습니다.

## 일시적인 에셋 업데이트 워크플로우 {#update-asset-transient-workflows}

DAM 자산 업데이트 워크플로우에 대해 일시적인 워크플로우를 활성화하여 AEM 측에서 성능을 향상시킬 수 있습니다. 임시 워크플로우를 활성화하면 AEM에서 자산을 만들거나 수정할 때 자산을 업데이트하는 데 필요한 처리 능력이 줄어듭니다.

1. 구성할 AEM `/miscadmin` 인스턴스에서 탐색합니다(예: `http://[Server]:[Port]/miscadmin`).
1. 탐색 트리에서 도구 &gt; **워크플로우** &gt; **모델** &gt; **** 댐 ****&#x200B;를 확장합니다.
1. DAM 자산 **업데이트를 두 번 클릭합니다**.
1. 부동 도구 패널에서 페이지 **탭으로** 전환한 다음 페이지 속성을 **클릭합니다**.
1. 임시 **워크플로우** 확인란을 선택하고 확인을 **클릭합니다**.

### Granite Transient 워크플로 큐 조정 {#adjust-granite-transient-workflow-queue}

AEM 성능을 개선하기 위한 또 다른 방법은 [MOCK] Another method to configure the value of the maximum parallel jobs for the Granite Workflow Queue job. 권장 값은 서버에서 사용할 수 있는 CPU의 약 절반입니다. 값을 조정하려면 다음 단계를 수행하십시오.

1. 구성할 AEM *인스턴스의* /system <http://&lt;Server&gt;:&lt;Port&gt;/system/console/configMgr>/console/configMgr로 이동합니다(예:).
1. QueueConfiguration **을**&#x200B;검색하고 Granite Temporary Workflow Queue **작업을 찾을 때까지 각 작업을 클릭하여** 엽니다. 옆에 있는 편집 아이콘을 클릭합니다.
1. [최대 **병렬 작업** ] 값을 변경하고 [저장]을 **클릭합니다**.

## AWS 구성 {#aws-configuration}

네트워크 대역폭 제한으로 인해 여러 사용자가 동시에 작업할 때 WebDAV/SMB의 성능이 저하될 수 있습니다. WebDAV/SMB의 성능을 개선하기 위해 AWS에서 실행되는 대상 AEM 인스턴스에 대한 AWS 인스턴스의 크기를 늘리는 것이 좋습니다.

이 측정은 특히 서버에서 사용할 수 있는 네트워크 대역폭의 양을 증가시킵니다. 다음은 자세한 사항입니다.

* AWS 인스턴스 전용 네트워크 대역폭의 양은 인스턴스 크기가 증가하면 증가합니다. 각 인스턴스 크기에 사용할 수 있는 대역폭에 대한 자세한 내용은 AWS [설명서를](https://aws.amazon.com/ec2/instance-types/)참조하십시오.
* 대규모 클라이언트에 대한 문제 해결 시 Adobe는 AEM 인스턴스의 크기를 c4.8xlarge로 구성했는데, 주로 제공된 전용 대역폭 4000Mbps에 해당합니다.
* AEM 인스턴스 앞에 디스패처가 있는 경우 적절한 크기인지 확인하십시오. AEM 인스턴스에서 4000Mbps를 제공하지만 디스패처가 500Mbps만 제공하는 경우 유효 대역폭은 500Mbps입니다. 디스패처가 네트워크 병목 현상을 만들기 때문입니다.

## 체크 아웃된 파일 제한 {#checked-out-file-limitations}

Explorer/Finder를 통해 체크 아웃된 파일과 상호 작용할 수 있는 방법에는 몇 가지 알려진 제한 사항이 있습니다. 파일을 체크 아웃한 경우 해당 파일을 체크 아웃한 사용자를 제외한 모든 사람이 파일을 읽기 전용으로 설정해야 합니다. AEM에서 WebDAV/SMB1 프로토콜을 구현하면 이 규칙이 적용됩니다. 그러나 OS WebDAV/SMB 클라이언트는 체크 아웃된 파일과 상호 작용하지 않는 경우가 많습니다. 일부 항목은 아래에 설명되어 있습니다.

### 일반 {#general}

체크 아웃된 파일에 기록할 때 잠금은 AEM의 WebDAV 구현 내에서만 적용됩니다. 따라서 이 잠금은 데스크톱 앱과 같은 WebDAV를 사용하는 클라이언트에만 적용됩니다. 잠금은 AEM의 웹 인터페이스를 통해 적용되지 않습니다. AEM 인터페이스는 체크 아웃된 자산에 대한 카드 보기에 잠금 아이콘만 표시합니다. 아이콘은 외형이며 AEM의 동작에는 영향을 주지 않습니다.

일반적으로 WebDAV 클라이언트는 예상대로 작동하지는 않습니다. 추가 문제가 있을 수 있습니다. 하지만 AEM에서 자산을 새로 고치거나 확인하는 것은 자산이 수정되지 않고 있는지 확인하는 건전한 방법입니다. 이러한 동작은 Adobe의 제어권이 아닌 OS WebDAV 클라이언트의 일반적인 방식입니다.

### Windows {#windows}

Windows의 파일 탐색기에서 파일이 사라지므로 파일을 성공적으로 삭제할 수 있습니다. 그러나 디렉토리를 새로 고치고 AEM 자산을 체크 인하면 파일이 여전히 있는 것으로 표시됩니다. 또한 파일을 편집할 수 있는 것으로 나타납니다(경고 대화 상자나 오류 메시지가 표시되지 않음). 그러나 파일을 다시 열거나 AEM 자산을 체크 인하면 파일이 변경되지 않았음을 알 수 있습니다.

#### Mac OS X {#mac-os-x}

파일을 교체하면 경고나 오류가 표시되지 않지만 AEM에서 자산을 확인해도 변경되지 않은 상태로 남아 있습니다. AEM에서 자산을 새로 고치거나 확인하여 수정 중이 아닌지 확인합니다.

## 데스크탑 앱 아이콘 문제 해결(Mac OS X) {#troubleshooting-desktop-app-icon-issues-mac-os-x}

데스크탑 앱을 설치하면 메뉴 모음에 데스크탑 앱 메뉴 아이콘이 표시됩니다. 아이콘이 나타나지 않으면 다음 단계를 수행하여 문제를 해결하십시오.

1. 운영 체제 터미널 창을 엽니다.
1. 명령 프롬프트에 다음 명령을 입력한 다음 Enter 키를 누릅니다.

   ```shell
    cd ../Library/Caches.
   ```

1. 다음 명령을 입력하고 Enter 키를 누릅니다.

   ```shell
   rm -r com.adobe.aem.assetscompanion 
   ```

1. 다음 명령을 입력하고 Enter 키를 누릅니다.

   ```shell
   cd ~/Library/Preferences
   ```

1. 다음 명령을 입력하고 Enter 키를 누릅니다.

   ```shell
   rm com.adobe.aem.assetscompanion.plist
   ```

1. 다음 명령을 입력하고 Enter 키를 누릅니다.

   ```shell
   rm ~/Library/Group\ Containers/group.com.adobe.aem.desktop/*
   ```

1. 시스템을 다시 시작합니다.

AEM Desktop은 지정된 파일을 세 번 동기화하려고 시도합니다. 세 번째 시도 후 파일이 동기화되지 않는 경우 AEM Desktop은 파일이 충돌하는 것으로 간주하고 백그라운드 업로드 상태 창을 통해 알려줍니다. 충돌 상태는 최신 변경 사항을 여전히 로컬에서 사용할 수 있지만 AEM에 동기화되지 않음을 나타냅니다. AEM 데스크톱 앱이 더 이상 동기화를 시도하지 않습니다.

이 문제를 해결하는 가장 간단한 방법은 충돌하는 파일을 열고 다시 저장하는 것입니다. AEM Desktop이 추가로 세 번 동기화를 시도하도록 합니다. 파일을 동기화하지 못한 경우 아래 섹션을 참조하십시오.

## AEM 데스크톱 캐시 지우기 {#clearing-aem-desktop-cache}

AEM Desktop의 캐시를 지우는 것은 여러 AEM Desktop 문제를 해결할 수 있는 예비 문제 해결 작업입니다.

다음 위치에서 응용 프로그램의 캐시 디렉토리를 삭제하여 캐시를 지울 수 있습니다.Windows:%LocalAppData%\Adobe\AssetsCompanion\Cache\

Mac:~/Library/Group/Containers/group.com.adobe.aem.desktop/cache/

하지만 AEM Desktop의 구성된 AEM 끝점에 따라 위치가 변경될 수 있습니다. 값은 타깃팅된 URL의 인코딩 버전입니다. 예를 들어 응용 프로그램이 타깃팅하는 경우 디렉토리 `http://localhost:4502`이름은 `http%3A%2F%2Flocalhost%3A4502%2F`입니다.

캐시를 지우려면 &lt;인코딩된 AEM 끝점&gt; 디렉터리를 삭제합니다.

>[!NOTE]
>
>AEM 데스크톱 캐시를 지우면 AEM에 동기화되지 않은 로컬 파일 변경 내용이 손실됩니다.

>[!NOTE]
>
>AEM 데스크톱 앱 버전 1.5부터 데스크톱 앱 UI에 캐시를 지우는 옵션이 있습니다.

## AEM 데스크톱 버전 찾기 {#finding-the-aem-desktop-version}

AEM 데스크톱 버전을 확인하는 절차는 Windows 및 Mac OS에서 모두 동일합니다.

AEM Desktop 아이콘을 클릭한 다음 정보를 **선택합니다**. 버전 번호가 화면에 표시됩니다.

## macOS에서 AEM 데스크탑 앱 업그레이드 {#upgrading-aem-desktop-app-on-macos}

macOS에서 AEM 데스크탑 앱을 업그레이드할 때 가끔 문제가 발생할 수 있습니다. 이는 AEM 데스크톱 앱용 레거시 시스템 폴더에서 AEM Desktop의 새 버전이 제대로 로드되지 못했기 때문입니다. 이 문제를 해결하려면 다음 폴더 및 파일을 수동으로 제거할 수 있습니다.

아래 단계를 실행하기 전에 macOS 애플리케이션 폴더의 "Adobe Experience Manager Desktop" 애플리케이션을 휴지통으로 드래그합니다. 그런 다음 Terminal을 열고 다음 명령을 실행하여 메시지가 표시되면 암호를 입력합니다.

```shell
sudo rm -rf ~/Library/Application\ Support/com.adobe.aem.desktop
sudo rm -rf ~/Library/Preferences/com.adobe.aem.desktop.plist
sudo rm -rf ~/Library/Logs/Adobe\ Experience\ Manager\ Desktop

sudo find /var/folders -type d -name "com.adobe.aem.desktop" | xargs rm -rf
sudo find /var/folders -type d -name "com.adobe.aem.desktop.finderintegration-plugin" | xargs rm -rf
```

## 다른 사람이 체크 아웃한 파일 저장 {#saving-a-file-checked-out-by-others}

운영 체제의 기술적 제한으로 인해 사용자가 다른 사람이 체크 아웃한 파일을 덮어쓸 때 일관된 경험을 할 수 없습니다. 이 환경은 체크 아웃된 파일을 편집하는 데 사용되는 애플리케이션에 따라 다릅니다. 경우에 따라 디스크 쓰기 실패를 나타내는 오류 메시지가 표시되거나 관련되지 않은 것처럼 보이거나 일반 오류가 표시됩니다. 다른 경우에는 오류 메시지가 표시되지 않고 작업이 성공한 것 같습니다.

이 경우 파일을 닫았다가 다시 열면 내용이 변경되지 않을 수 있습니다. 그러나 일부 응용 프로그램은 파일 백업을 저장할 수 있으므로 변경 내용을 적용할 수 있습니다.

체크 인 시 동작에 관계없이 파일이 변경되지 않습니다. 다른 버전의 파일이 표시되더라도 변경 내용이 AEM에 동기화되지 않습니다.

## 파일 이동 문제 해결 {#troubleshooting-problems-around-moving-files}

서버 API를 사용하려면 이동 및 복사 작업을 위해 추가 헤더, X-Destination, X-Depth 및 X-Overwrite가 필요합니다. 디스패처는 기본적으로 이러한 헤더를 전달하지 않으므로 이러한 작업이 실패합니다. 자세한 내용은 디스패처의 AEM [에 연결을 참조하십시오](install-configure-app-v1.md#connect-to-an-aem-instance-behind-a-dispatcher).

## AEM Desktop 연결 문제 해결 {#troubleshooting-aem-desktop-connection-issues}

### SAML 리디렉션 문제 {#saml-redirect-issue}

AEM Desktop에서 SSO 활성화(SAML) AEM 인스턴스에 연결하는 문제가 발생하는 가장 일반적인 이유는 SAML 프로세스가 원래 요청된 경로로 다시 리디렉션되지 않기 때문입니다. 또는 AEM 데스크탑에서 구성되지 않은 호스트로 연결이 리디렉션될 수 있습니다. 다음 단계를 수행하여 로그인 프로세스를 확인합니다.

1. 웹 브라우저를 엽니다.
1. 주소 표시줄에서 URL을 지정합니다 `/content/dam.json`.
1. 예를 들어 URL을 대상 AEM 인스턴스로 바꿉니다 `http://localhost:4502/content/dam.json`.
1. AEM에 로그온합니다.
1. 로그인한 후 주소 표시줄에서 브라우저의 현재 주소를 확인합니다. 처음 입력한 URL과 일치해야 합니다.
1. AEM Desktop에 구성된 대상 AEM 값과 앞의 모든 항목이 일치하는지 `/content/dam.json` 확인합니다.

### SSL 구성 문제 {#ssl-configuration-issue}

AEM 데스크톱 앱에서 HTTP 통신에 사용하는 라이브러리는 엄격한 SSL 적용을 사용합니다. 때때로 브라우저 사용에 성공하지만 AEM 데스크톱 앱을 사용하지 못할 수 있습니다. SSL을 적절히 구성하려면 Apache에 누락된 중간 인증서를 설치합니다. Apache [에서 중간 CA 인증서를 설치하는 방법을 참조하십시오](https://access.redhat.com/solutions/43575).

## 디스패처와 함께 AEM Desktop 사용 {#using-aem-desktop-with-dispatcher}

AEM Desktop은 AEM Dispatcher 뒤에서 AEM 배포와 함께 작동하며, 이는 AEM 서버에 대한 기본 및 권장 구성입니다. AEM 작성 환경 앞의 AEM 디스패처는 일반적으로 DAM 자산 캐싱을 생략하도록 구성됩니다. 따라서 디스패처는 AEM Desktop 관점으로부터 추가 캐싱을 제공하지 않습니다. 디스패처 구성이 AEM Desktop에서 작동하도록 조정되었는지 확인합니다. 자세한 내용은 디스패처 [뒤에서 AEM에 연결을 참조하십시오](install-configure-app-v1.md#connect-to-an-aem-instance-behind-a-dispatcher).

## 로그 파일 확인 {#checking-for-log-files}

운영 체제에 따라 다음 위치에서 AEM Desktop용 로그 파일을 찾을 수 있습니다.

* Windows: `%LocalAppData%\Adobe\AssetsCompanion\Logs`
* Mac: `~/Library/Logs/Adobe\ Experience\ Manager\ Desktop`