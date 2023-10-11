## `openjdk:22-ea-windowsservercore`

```console
$ docker pull openjdk@sha256:c10c7d3ca2ebdfc9400fc8051c172b2e29e2437bc5e42f207aeada4942bb8241
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2031; amd64
	-	windows version 10.0.17763.4974; amd64

### `openjdk:22-ea-windowsservercore` - windows version 10.0.20348.2031; amd64

```console
$ docker pull openjdk@sha256:991314469b2d2f9825bf70026ad4175f6396df6f76d098d8d516d3b284fb7671
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2059939042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30757eeed416aceb1ff6c735f465644a2f5430fb2f3cefb97804fda2fcba1290`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 06 Oct 2023 21:59:31 GMT
RUN Install update 10.0.20348.2031
# Wed, 11 Oct 2023 01:35:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Oct 2023 03:48:56 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 11 Oct 2023 03:48:57 GMT
ENV JAVA_HOME=C:\openjdk-22
# Wed, 11 Oct 2023 03:49:19 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 11 Oct 2023 03:49:20 GMT
ENV JAVA_VERSION=22-ea+18
# Wed, 11 Oct 2023 03:49:21 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk22/18/GPL/openjdk-22-ea+18_windows-x64_bin.zip
# Wed, 11 Oct 2023 03:49:22 GMT
ENV JAVA_SHA256=9514da1d60086946d1324cfabda5280213d7243eec44e2268bbbf02248d910ff
# Wed, 11 Oct 2023 03:50:16 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 11 Oct 2023 03:50:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d2471a50c8ec3ea61c16dd871f7b9167bf779faad2b6e5a6f72a18b88b846b`  
		Last Modified: Tue, 10 Oct 2023 17:55:23 GMT  
		Size: 471.2 MB (471244358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a73b90f34f44bbbb354af4f3d4cc6cde597d2f5183641e139f7ca8b76ec3bb9`  
		Last Modified: Wed, 11 Oct 2023 02:45:06 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71221770428be33fb112dc7596eb2857d0a894b9444c8ac1e070fb2713cf0cef`  
		Last Modified: Wed, 11 Oct 2023 03:55:46 GMT  
		Size: 438.1 KB (438050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d7edf8e3cbf42462ac6609acad01b5456938cdcc07b096dfebda103810e262f`  
		Last Modified: Wed, 11 Oct 2023 03:55:45 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:935ab285e7bf5c8a65c15bf37e24c811dc80f14c18753ee554d67b2924e05265`  
		Last Modified: Wed, 11 Oct 2023 03:55:45 GMT  
		Size: 251.8 KB (251804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d0f4a5f34128cebe88f66eb9aef17fdb03d7e3a0ea425588af06878193bbe0`  
		Last Modified: Wed, 11 Oct 2023 03:55:43 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b858b7766040991e6f6e14bfbc07bc24fb859edbaef91148c600ce53c122e879`  
		Last Modified: Wed, 11 Oct 2023 03:55:43 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9b2936d7b070f8c3b5b6e0fafa8e7a7a96ed02c2cfc9e5cb545249c2372fa41`  
		Last Modified: Wed, 11 Oct 2023 03:55:43 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edbc95ebf5a4de8c90268e183e77c2c9262cfefd39dde940a6f93f6ee98cbba1`  
		Last Modified: Wed, 11 Oct 2023 03:56:03 GMT  
		Size: 199.4 MB (199397674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33442e6f6d8be6eaf94c6d16407a118914be5c8ce247bf0f81691a63e25db3a5`  
		Last Modified: Wed, 11 Oct 2023 03:55:43 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:22-ea-windowsservercore` - windows version 10.0.17763.4974; amd64

```console
$ docker pull openjdk@sha256:c581a3712578bed9f8fcb785c4e09d00e47f36019e8caaeaecdd0386e48f7b4b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2231765580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d46afd818ec7e1b3b37dad3917f5edaf71a037206b243790fc9ef0cfecc6f85`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 02 Oct 2023 08:29:38 GMT
RUN Install update 10.0.17763.4974
# Wed, 11 Oct 2023 01:36:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Oct 2023 03:51:39 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 11 Oct 2023 03:51:40 GMT
ENV JAVA_HOME=C:\openjdk-22
# Wed, 11 Oct 2023 03:52:38 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 11 Oct 2023 03:52:39 GMT
ENV JAVA_VERSION=22-ea+18
# Wed, 11 Oct 2023 03:52:39 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk22/18/GPL/openjdk-22-ea+18_windows-x64_bin.zip
# Wed, 11 Oct 2023 03:52:40 GMT
ENV JAVA_SHA256=9514da1d60086946d1324cfabda5280213d7243eec44e2268bbbf02248d910ff
# Wed, 11 Oct 2023 03:54:08 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 11 Oct 2023 03:54:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af2bcb37edaec1dd87fc4a6f7c9129ca37bf1f91b65eb365ba9d4c70473beea`  
		Last Modified: Tue, 10 Oct 2023 17:51:10 GMT  
		Size: 381.0 MB (380970130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0814e4a0bb8c615854a85a2b60cd043cfd20ad5a5d755acab1b30b18e4bfad3c`  
		Last Modified: Wed, 11 Oct 2023 02:46:41 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f783cb3f1b4d13355b852dedee9d6d4d1970fb4493dc1642d1b2a2f2e81e868b`  
		Last Modified: Wed, 11 Oct 2023 03:56:26 GMT  
		Size: 460.2 KB (460193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130ee22501b1f092f84a96a93216a4e26e770e6728f3298841b909959eed064c`  
		Last Modified: Wed, 11 Oct 2023 03:56:26 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d71937d13c516a2428fe61543786cb08bd8e9b4ddf3d0bd80582d9e54be7950`  
		Last Modified: Wed, 11 Oct 2023 03:56:26 GMT  
		Size: 278.1 KB (278058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe0c910e051fc6b8e4ac2b6326f18c4046de68d605dc30c70942f7c96bc74a10`  
		Last Modified: Wed, 11 Oct 2023 03:56:24 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c1e64a7f4fea60370a4f42e2616abd9b20e3011fa64560d6b6ec4ce3d65aae3`  
		Last Modified: Wed, 11 Oct 2023 03:56:24 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98eac83b7e2bf9e22ab86fef3b170e05afccc1396c5a295ed06c1224f8462f50`  
		Last Modified: Wed, 11 Oct 2023 03:56:24 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d500489d6a1900e98a63a7d951be285726ee0f7fb8016ca631cc1fae6967168b`  
		Last Modified: Wed, 11 Oct 2023 03:56:43 GMT  
		Size: 199.4 MB (199429055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c53ff2c052e6b00481ebf465139d7c4580202bf68a094e610423a0c1b3d6355`  
		Last Modified: Wed, 11 Oct 2023 03:56:24 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
