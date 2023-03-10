## `openjdk:21-ea-jdk-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:077e6499ad62c4b4f1a83e1d87c18c45f63190c782a119602a4c5710b83a8eb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4010; amd64

### `openjdk:21-ea-jdk-windowsservercore-1809` - windows version 10.0.17763.4010; amd64

```console
$ docker pull openjdk@sha256:5aededb27235917fc599e466e21ff145576d1c785442a13244cd79f49d88adb8
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2158576456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82d65c6bd2c60ad11829d8403661d7c4a2fbd0320f19cbf79f8c52b40bb2921e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Tue, 07 Feb 2023 10:44:53 GMT
RUN Install update 10.0.17763.4010
# Wed, 15 Feb 2023 22:41:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Feb 2023 02:17:23 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Thu, 16 Feb 2023 02:17:24 GMT
ENV JAVA_HOME=C:\openjdk-21
# Thu, 16 Feb 2023 02:18:29 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Thu, 09 Mar 2023 23:17:14 GMT
ENV JAVA_VERSION=21-ea+13
# Thu, 09 Mar 2023 23:17:15 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk21/13/GPL/openjdk-21-ea+13_windows-x64_bin.zip
# Thu, 09 Mar 2023 23:17:16 GMT
ENV JAVA_SHA256=243e8681ce473d4c13a7aed22eb2109685da552776c021b415457445426cf659
# Thu, 09 Mar 2023 23:19:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Thu, 09 Mar 2023 23:19:28 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f77c707e813c8220ab3c92b6eb7b445ee0b1a485686ff62014ae32c17d2b1b6`  
		Last Modified: Thu, 16 Feb 2023 00:29:31 GMT  
		Size: 255.0 MB (255014079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a5753d4956d637f7e88bedf0b91260e724500d9fa9b91c0a9ed419263659a9a`  
		Last Modified: Thu, 16 Feb 2023 00:28:25 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98437cec399b6656d20521928c292ca8c2e4c0c737b7cb970de037167fc8db6f`  
		Last Modified: Thu, 16 Feb 2023 02:28:35 GMT  
		Size: 515.3 KB (515330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a0fdacfc64d4626f9464e954281e2675812980cad460d5989807088ab5d22d6`  
		Last Modified: Thu, 16 Feb 2023 02:28:35 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63aceb75603170d702778c30ea615042a578e11438c4f8e572720a1a81963ec`  
		Last Modified: Thu, 16 Feb 2023 02:28:35 GMT  
		Size: 333.4 KB (333385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dd386b38305cf1ddee52a5664b0b44e0d00528b98fd86a898e78c32455ecfb8`  
		Last Modified: Thu, 09 Mar 2023 23:22:43 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13a3185fd74c69ce4e82f8807706d413e99505f732fb693bad226b91c2ae7ee9`  
		Last Modified: Thu, 09 Mar 2023 23:22:43 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60b54b654fd3e0eebac97cf135310bf484e447eea2b766bfd4e79a74ab6b3f32`  
		Last Modified: Thu, 09 Mar 2023 23:22:43 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:210ad572e4bb5b7ca547d22bf702bda54d9e0a96048b3e7e0b8dad1bf2ada56c`  
		Last Modified: Thu, 09 Mar 2023 23:23:04 GMT  
		Size: 194.8 MB (194761321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9a1e978ec60275c131350c9ad94b2468a00397a0d8164e47ce654a28bec78ed`  
		Last Modified: Thu, 09 Mar 2023 23:22:43 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
