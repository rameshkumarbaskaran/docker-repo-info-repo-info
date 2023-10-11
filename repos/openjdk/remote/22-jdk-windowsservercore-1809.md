## `openjdk:22-jdk-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:65cb3cee460ffe4a0de93c5b1f99215a28f223224c4e4c92fd7b77edc6c840d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `openjdk:22-jdk-windowsservercore-1809` - windows version 10.0.17763.4974; amd64

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
