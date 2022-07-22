## `openjdk:19-ea-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:9e8a322a1487fa543e117b66b0cd0727a9cf65bf4b254dc8a602afd4574f1842
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.825; amd64

### `openjdk:19-ea-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.825; amd64

```console
$ docker pull openjdk@sha256:b9aa957f586bc97844b1f373fe46ee5f4fc50b8751fc902483b3732f709a5775
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2493195709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef04daaec79cca2daa81daafc0cf257dc56a7d8850947a8503d56ab20143a4ac`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Mon, 04 Jul 2022 17:46:55 GMT
RUN Install update 10.0.20348.825
# Tue, 12 Jul 2022 19:25:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Jul 2022 15:47:47 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 13 Jul 2022 15:53:28 GMT
ENV JAVA_HOME=C:\openjdk-19
# Wed, 13 Jul 2022 15:53:49 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Thu, 21 Jul 2022 23:19:03 GMT
ENV JAVA_VERSION=19-ea+32
# Thu, 21 Jul 2022 23:19:03 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk19/32/GPL/openjdk-19-ea+32_windows-x64_bin.zip
# Thu, 21 Jul 2022 23:19:04 GMT
ENV JAVA_SHA256=6c2cc12281a7dc05988631d3587e335ebc01322d312fd71114482d24a5ba2b63
# Thu, 21 Jul 2022 23:19:52 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Thu, 21 Jul 2022 23:19:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e1a27cb9d4615dec325f2cbabac4ca1f65413bdbb8b440cc961df032993a9b81`  
		Size: 863.4 MB (863367943 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6452cb934201756f0ed9fb5e0cbea54a22a66412cb696ff30a1923d456e28bcf`  
		Last Modified: Tue, 12 Jul 2022 20:20:48 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f6a9bb0f902c90ab99dd7b3c8634f73649b052868aa5272230088be93b0be1f`  
		Last Modified: Mon, 18 Jul 2022 21:21:07 GMT  
		Size: 655.6 KB (655645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd66eccfd01aee1696d4c33d4a0c1b49827e90518a13fde80169d46f2171f64`  
		Last Modified: Mon, 18 Jul 2022 21:23:16 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92a625d17ec9ae423e7fd6a2cd3d934b06c1a4872336d21f5021622a34e145e1`  
		Last Modified: Mon, 18 Jul 2022 21:23:16 GMT  
		Size: 555.8 KB (555849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29ee7df30cfdac39d28aeb1ca0a5ae3896c81d6ecf436719311f77398ea3f2a4`  
		Last Modified: Thu, 21 Jul 2022 23:29:02 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb0cdf9403fb0299b12d7d9e4d327126897d7489638c08b4570cd95963271c6`  
		Last Modified: Thu, 21 Jul 2022 23:29:02 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:376240edb7641a4d16745dd31793de3ec451f0fbfdd6dd6497e582ecda5296cd`  
		Last Modified: Thu, 21 Jul 2022 23:29:02 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c2c5ed799cbe9a5c45d1b30b70440c237e76862f669530a063ad88347ab1b5`  
		Last Modified: Thu, 21 Jul 2022 23:29:22 GMT  
		Size: 191.7 MB (191744145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f177135457481f0d7c86d729725ad66d4b0465fb89e79ce2fa756f5032e92a`  
		Last Modified: Thu, 21 Jul 2022 23:29:03 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
