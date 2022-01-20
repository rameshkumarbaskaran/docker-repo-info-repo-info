## `openjdk:19-ea-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:843149ee3b68ff0c19ecaf496c7f06250bcf80319448514050bf88a4b64d19ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.473; amd64

### `openjdk:19-ea-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.473; amd64

```console
$ docker pull openjdk@sha256:fbf5ff63e65002c3994fd6c1c7ee078d817b39d873e8f784a95d6fd58a3cdbc6
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2394012649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b46d851e5ff1352747083fec25a4fd89a5ebeac200fec1cd4a0af800b24056e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Sun, 16 Jan 2022 05:17:24 GMT
RUN Install update ltsc2022-amd64
# Wed, 19 Jan 2022 22:21:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 19 Jan 2022 22:23:11 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 19 Jan 2022 22:23:13 GMT
ENV JAVA_HOME=C:\openjdk-19
# Wed, 19 Jan 2022 22:23:50 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 19 Jan 2022 22:23:51 GMT
ENV JAVA_VERSION=19-ea+5
# Wed, 19 Jan 2022 22:23:52 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk19/5/GPL/openjdk-19-ea+5_windows-x64_bin.zip
# Wed, 19 Jan 2022 22:23:54 GMT
ENV JAVA_SHA256=f26cae210cb484a48c086f2207018482162d2dd793fb69cc5575dc575159ee1c
# Wed, 19 Jan 2022 22:25:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 19 Jan 2022 22:25:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0e02c12b1310e6c76c29fcd6f81905400fdb6a01caac9dc825939ad004baffef`  
		Size: 955.8 MB (955800778 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2e1f45a873642f0aab3474828d75469362741244e7c714068ac1afe056102cd6`  
		Last Modified: Thu, 20 Jan 2022 00:40:19 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa436893917b4b24f7020ae30c97fa33ab983d9c24e6fd7534d56f8b19bf786f`  
		Last Modified: Thu, 20 Jan 2022 02:19:54 GMT  
		Size: 601.2 KB (601200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:039cc436f8de7b22962fef11f63ff7fb05b1dad02d0b04d62c514a24ef045cf9`  
		Last Modified: Thu, 20 Jan 2022 02:19:54 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:880009a6e2005dbfbbe934f1896114d21a0e91c8bdaffaee2d5349c8e9de467f`  
		Last Modified: Thu, 20 Jan 2022 02:19:54 GMT  
		Size: 506.3 KB (506304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6476e989f4ef1c0105bcbfdb2e49a2f9a8e2c38c7965632f12874d53f966a3ac`  
		Last Modified: Thu, 20 Jan 2022 02:19:51 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70e9e6382144fac92b0302de50ef80abed74492f950559f445c07fb619328fa5`  
		Last Modified: Thu, 20 Jan 2022 02:19:51 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d1ae9e8e1f91816db321b537dae2215fafc5c28edad901672074520af94d9bb`  
		Last Modified: Thu, 20 Jan 2022 02:19:51 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d459a2a2f0391e238a8490c233e0cecf0215497acbf0e2b113235bc36a47934`  
		Last Modified: Thu, 20 Jan 2022 02:20:13 GMT  
		Size: 185.4 MB (185396804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f67526579a95197c298e3d91e454074a2bf71e07bc9b281dcbb6c6f9345b112`  
		Last Modified: Thu, 20 Jan 2022 02:19:51 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
