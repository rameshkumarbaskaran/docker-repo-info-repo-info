## `openjdk:22-ea-jdk-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:5bb03cad2166f549ae87dc9a65b23bbd2ea52f50264df035fb14c6d6a6197fb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4737; amd64

### `openjdk:22-ea-jdk-windowsservercore-1809` - windows version 10.0.17763.4737; amd64

```console
$ docker pull openjdk@sha256:cc86bb74d99f9b3cc7c9419c5350616c465882e9a181892567019ea1f4ce4fa1
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2195814054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86fc04c3034edb951405896940b1840a92110436fffdb8540952393a158a0943`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 02 Aug 2023 09:07:15 GMT
RUN Install update 10.0.17763.4737
# Wed, 09 Aug 2023 23:36:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 10 Aug 2023 02:39:19 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Thu, 10 Aug 2023 02:39:21 GMT
ENV JAVA_HOME=C:\openjdk-22
# Thu, 10 Aug 2023 02:40:19 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Thu, 10 Aug 2023 02:40:20 GMT
ENV JAVA_VERSION=22-ea+9
# Thu, 10 Aug 2023 02:40:21 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk22/9/GPL/openjdk-22-ea+9_windows-x64_bin.zip
# Thu, 10 Aug 2023 02:40:22 GMT
ENV JAVA_SHA256=86de3956f3cf843d68c473831181e873e8f4ad3aad53db980302ee94bc62ae5e
# Thu, 10 Aug 2023 02:41:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Thu, 10 Aug 2023 02:41:59 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95f433aa7d90194e65f6b08a599b3ee12292e124d47c204107baedfd71054c1`  
		Last Modified: Tue, 08 Aug 2023 18:31:16 GMT  
		Size: 345.3 MB (345334986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03d23fbbd4f650b6f60106a3cc28d711efce2f97cfb80b67e2dec305e011aa3`  
		Last Modified: Thu, 10 Aug 2023 00:19:47 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82556c0499019c0d63fc48880317518db1b5694401f0d8420ea2c4961effcee4`  
		Last Modified: Thu, 10 Aug 2023 02:49:35 GMT  
		Size: 250.9 KB (250879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a5d5ec7e3c127f5942ff38f7f912fe583a70ebd26a2f23b08ec931d3ac747f0`  
		Last Modified: Thu, 10 Aug 2023 02:49:35 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e0adf33ca81bc87626c3e4e8e94d469cc903ac1e4cf98961cbf569e7f7662fd`  
		Last Modified: Thu, 10 Aug 2023 02:49:35 GMT  
		Size: 246.9 KB (246857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7846b4db53846f619a9b70f4ac44a3d5b5defacad2c9096639412c7454479057`  
		Last Modified: Thu, 10 Aug 2023 02:49:33 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632b04cff43e33eb9f81892288a706d90c7292ef6f584b18bc608c88e2f4b6e7`  
		Last Modified: Thu, 10 Aug 2023 02:49:33 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018dc86b650d934d9e0d01de5e5f6be314c0d83ba176add513d332a978e41f1f`  
		Last Modified: Thu, 10 Aug 2023 02:49:33 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d85b9606c168ccee72ff8b1bb3bc5ebbac73a235a88e8402219fb748e343a9b9`  
		Last Modified: Thu, 10 Aug 2023 02:49:54 GMT  
		Size: 199.4 MB (199352498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12e6f70b4b17801b42be80c0d01f447cf21cb170d0b74558153535017d1a15b8`  
		Last Modified: Thu, 10 Aug 2023 02:49:33 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
