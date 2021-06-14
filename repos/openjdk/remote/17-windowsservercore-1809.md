## `openjdk:17-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:d020b67567215d700884538bc8dcd76eb25b2f8fef409663594af72633a49794
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1999; amd64

### `openjdk:17-windowsservercore-1809` - windows version 10.0.17763.1999; amd64

```console
$ docker pull openjdk@sha256:0a57821dd7508f9b5666b5ac4e505da3475e4edbb5541bda47e56c0f0229a727
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2824736490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:178a4c49b166e1d490d65cdf5c4c58bfa27b1b7cd1c7122ceb00a1187c1a0412`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Sun, 06 Jun 2021 04:28:43 GMT
RUN Install update 1809-amd64
# Wed, 09 Jun 2021 12:10:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Jun 2021 16:45:14 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 09 Jun 2021 16:45:17 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 09 Jun 2021 16:45:47 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 14 Jun 2021 21:24:46 GMT
ENV JAVA_VERSION=17-ea+26
# Mon, 14 Jun 2021 21:24:49 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk17/26/GPL/openjdk-17-ea+26_windows-x64_bin.zip
# Mon, 14 Jun 2021 21:24:51 GMT
ENV JAVA_SHA256=257291da8017cdf411d0380de8c9cf3fa93925d5381f546ffc8fd81ae84e2eee
# Mon, 14 Jun 2021 21:25:57 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 14 Jun 2021 21:26:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:639bb6bb2beb4cfdcacb9f0844344448fe26494665d5fe78a494419f86fbb18f`  
		Size: 923.3 MB (923252167 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7863ef96846d497ea06fe442ea13dcecaf5c248ce238c69800475281a4fa848e`  
		Last Modified: Wed, 09 Jun 2021 12:20:41 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc4f84ebe44976489de74231891a3bceaf046cdaf5d963f8d9785d418863bfd7`  
		Last Modified: Wed, 09 Jun 2021 17:24:02 GMT  
		Size: 352.1 KB (352057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:580f726be9e9223f5fbe72ec77a450134c84e6501882795e77ae88e34b87949a`  
		Last Modified: Wed, 09 Jun 2021 17:24:01 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6098af536049b2e7b8c27707faac52e3ac75b37f3ba29e5543ea2f149e8ce501`  
		Last Modified: Wed, 09 Jun 2021 17:24:01 GMT  
		Size: 310.1 KB (310100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:966e81c6b5de37bf0a644beca421057502e2463509996f4c0b27be959f9735ba`  
		Last Modified: Mon, 14 Jun 2021 21:42:47 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2948d65f889effcaa053505bdd9f8e8ca682d3cb9e37a4e8d3fcaae3c8b0c3ac`  
		Last Modified: Mon, 14 Jun 2021 21:42:47 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc601d3ecdd0902a3f20c9447d47bed355004c1a3d12ce820bc4b67e66daa09`  
		Last Modified: Mon, 14 Jun 2021 21:42:47 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf48c719447747c4d46cecc82758d9f83db70ed7d6b081001c0e1bcc2ec0fa3`  
		Last Modified: Mon, 14 Jun 2021 21:46:06 GMT  
		Size: 182.5 MB (182480804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f11430f5874943f64056194df73ca88e5385a044c7f6a3c6f0ce295bc9702484`  
		Last Modified: Mon, 14 Jun 2021 21:42:47 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
