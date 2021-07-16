## `openjdk:17-ea-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:eba62f104a67eacb022c27f16426b0ebad493b1f36c0302923290e3d3af662fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2061; amd64

### `openjdk:17-ea-windowsservercore-1809` - windows version 10.0.17763.2061; amd64

```console
$ docker pull openjdk@sha256:b9982a8855ac04e9ca96430fc2ba33afc865ce88e4b7f020e755631c1f84adcb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2868574620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:defcd2409b7a69eb676dc83c124439c5abebe403fd1adc25b81393f87ee54617`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 06 Jul 2021 20:34:18 GMT
RUN Install update 1809-amd64
# Wed, 14 Jul 2021 02:41:59 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Jul 2021 02:43:11 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 14 Jul 2021 02:55:40 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 14 Jul 2021 02:56:53 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Thu, 15 Jul 2021 22:20:06 GMT
ENV JAVA_VERSION=17-ea+31
# Thu, 15 Jul 2021 22:20:08 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk17/31/GPL/openjdk-17-ea+31_windows-x64_bin.zip
# Thu, 15 Jul 2021 22:20:10 GMT
ENV JAVA_SHA256=b46f818241d7d1a01192b061500a905e0ee1ccc2b0e41baa0c85ffd5c557002a
# Thu, 15 Jul 2021 22:21:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Thu, 15 Jul 2021 22:21:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f143c6fed32d477c35b660b2e108ea62e3593c03e44bd9ced208ce52b26b0841`  
		Size: 967.1 MB (967113907 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:dd3b24b55401566ea01a5005138a23766b6b6408c2276b7ebd097da01de80897`  
		Last Modified: Wed, 14 Jul 2021 03:38:04 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60588ed228454a5b9a3ebf90d5ae7109392676a95ebab716cf7bd486f4e257ae`  
		Last Modified: Wed, 14 Jul 2021 03:38:04 GMT  
		Size: 365.3 KB (365286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1803aa8cded0dbe983dc584b95721731baff32adc0a819e4331756bd0a7a9b38`  
		Last Modified: Wed, 14 Jul 2021 03:46:10 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12e8b66d878091e45d7ce5b9c5fa1033aabd86bc416035f11a6852c31fb4ff1c`  
		Last Modified: Wed, 14 Jul 2021 03:46:11 GMT  
		Size: 323.7 KB (323703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6de6405871bc39966da2d5d80b5e4bbd1eb7035a2b211b9ebe17d472fd5db2`  
		Last Modified: Thu, 15 Jul 2021 22:37:37 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4815db0be0fa875ae32293c8ef8b8d4bd76fef63f9d0acd1cc914c3ff819831`  
		Last Modified: Thu, 15 Jul 2021 22:37:37 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc8c1ced3644381271bb33c08c8011f7e69a95388dfa5c4e6f176a1bd89069f`  
		Last Modified: Thu, 15 Jul 2021 22:37:37 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ec8fcd11bd677bbae2786c93406bc75a1fbe89fbf85f2f422df49d0c7cd916f`  
		Last Modified: Thu, 15 Jul 2021 22:37:58 GMT  
		Size: 182.4 MB (182430320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf6b5d870816277974641e49c36b67502e2fd1be2de9494bd9ea882fdcd4286a`  
		Last Modified: Thu, 15 Jul 2021 22:37:37 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
