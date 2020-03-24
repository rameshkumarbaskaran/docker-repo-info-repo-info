## `openjdk:15-windowsservercore`

```console
$ docker pull openjdk@sha256:620d585ecfa97c4be2e186c7ee2b9c05ad8d04aa6900571bc77fdc7a0e749c4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64
	-	windows version 10.0.14393.3568; amd64

### `openjdk:15-windowsservercore` - windows version 10.0.17763.1098; amd64

```console
$ docker pull openjdk@sha256:6e63fdefe8006c445f9ada187052b4ad2f05d71b556b65db4ca896e96902fa2c
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2463933221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aa2281ddc5c4e07d3bd8e180711d90e28eb62c184a8ddd626e8e9ecc690ba4c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 06 Mar 2020 11:12:29 GMT
RUN Install update 1809-amd64
# Wed, 11 Mar 2020 00:42:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Mar 2020 14:53:20 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force
# Wed, 11 Mar 2020 14:53:21 GMT
ENV JAVA_HOME=C:\openjdk-15
# Wed, 11 Mar 2020 14:53:45 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Mon, 23 Mar 2020 21:14:33 GMT
ENV JAVA_VERSION=15-ea+15
# Mon, 23 Mar 2020 21:14:34 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk15/15/GPL/openjdk-15-ea+15_windows-x64_bin.zip
# Mon, 23 Mar 2020 21:14:35 GMT
ENV JAVA_SHA256=8f8ea4db0028dc5f911e8949707baf9b77400756ceccc04fdb2eefc2c7f828d9
# Mon, 23 Mar 2020 21:16:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 23 Mar 2020 21:16:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23645bd7ee0885911e1e2ab55ebcb36ce35795e1ceba9166ffd1b26dde18c3ee`  
		Size: 730.7 MB (730650958 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a7fab05ac5ad4b2f665ad71b5c08a81e82bff7ea2fdcbb66c14193d2dd268875`  
		Last Modified: Wed, 11 Mar 2020 01:16:21 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a4f86b1e9c271e3e0e37ceb96d7c9042f35b463aef0323a7ca7d3166be8163b`  
		Last Modified: Wed, 11 Mar 2020 15:25:11 GMT  
		Size: 4.7 MB (4659035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:252d80eee5b49917fa28f0aa282593137be5d7dd4c9fd863164226d8f099d9fa`  
		Last Modified: Wed, 11 Mar 2020 15:25:05 GMT  
		Size: 1.2 KB (1194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a29727e0a8d494510a0c0cad18a44647ecb6cf968e13fac178f7a42d802bb625`  
		Last Modified: Wed, 11 Mar 2020 15:25:07 GMT  
		Size: 289.6 KB (289584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37c6ecb3dfb192782797e684147e045ddf8c7c7ed74492cb8128168f8b174622`  
		Last Modified: Mon, 23 Mar 2020 21:24:34 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9dd9228a03096a3fe8abc1155ca6fb4f95cf2e662be54e7ad91459f0f39ef65`  
		Last Modified: Mon, 23 Mar 2020 21:24:34 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25baeaa77715a076f7d421bed6d6978223332ebe4ad6e2024060c579b8ed4321`  
		Last Modified: Mon, 23 Mar 2020 21:24:34 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8239de7a7c14d556fb4e77ce151d6e36a788ef3fbcea5ca958046e7b77c526c4`  
		Last Modified: Mon, 23 Mar 2020 21:27:41 GMT  
		Size: 193.6 MB (193641388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:675ff99756160a9c9ae134fc2f9a342914db2936940a8fa03e25804aac87f67a`  
		Last Modified: Mon, 23 Mar 2020 21:24:34 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:15-windowsservercore` - windows version 10.0.14393.3568; amd64

```console
$ docker pull openjdk@sha256:9fefa1a38103f636f1bb8c61615f53b4823f2ba2edf02fc785c579e962455810
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5942703059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f69a2f0beb90b6162b9fe2a091e87cd066951d878dde385bc896f0eedeb65c5a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 10 Mar 2020 08:14:00 GMT
RUN Install update ltsc2016-amd64
# Fri, 13 Mar 2020 21:32:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 13 Mar 2020 21:34:16 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force
# Fri, 13 Mar 2020 21:34:18 GMT
ENV JAVA_HOME=C:\openjdk-15
# Fri, 13 Mar 2020 21:35:43 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Mon, 23 Mar 2020 21:16:45 GMT
ENV JAVA_VERSION=15-ea+15
# Mon, 23 Mar 2020 21:16:46 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk15/15/GPL/openjdk-15-ea+15_windows-x64_bin.zip
# Mon, 23 Mar 2020 21:16:47 GMT
ENV JAVA_SHA256=8f8ea4db0028dc5f911e8949707baf9b77400756ceccc04fdb2eefc2c7f828d9
# Mon, 23 Mar 2020 21:19:44 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 23 Mar 2020 21:19:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a5d20b7a2294a0d2631f74f49fc34574484a692913559546ef0bceae789fd7a8`  
		Size: 1.7 GB (1658775203 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f08cc5bf7287bc1d8f72edfe2439c99210e433230a22fc73264fcf1685850ed2`  
		Last Modified: Fri, 13 Mar 2020 22:09:47 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25aa1b0ee68c69a66d5b4e6cdfd989815b485cf3988dd548e162f4772304f990`  
		Last Modified: Fri, 13 Mar 2020 22:09:51 GMT  
		Size: 5.4 MB (5380002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2edec803117173fae9526bf71d284db81781cff2f4e22fcf4cfabda2cf59f17a`  
		Last Modified: Fri, 13 Mar 2020 22:09:42 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adaa5169033250eb57d65694775263fcc1ccf51cd49794ba272552675d61c9bb`  
		Last Modified: Fri, 13 Mar 2020 22:09:48 GMT  
		Size: 5.4 MB (5357722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1581310560e9a2f626271bce100d7902d0bf7b09664a32ee6ec034dd2ba8c27a`  
		Last Modified: Mon, 23 Mar 2020 21:28:01 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a00777ea702c103770c2058cb8ee564d026ed15df12afb341b5c8fa7752b6fe`  
		Last Modified: Mon, 23 Mar 2020 21:28:00 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89922d9c6c46b47b03428055fdcf15d99132cff3578b8a97ad97e598d716ecae`  
		Last Modified: Mon, 23 Mar 2020 21:28:00 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e916440d819f22762cbb48a01aff50d7444d30080c10acd170822586c15675`  
		Last Modified: Mon, 23 Mar 2020 21:28:37 GMT  
		Size: 203.2 MB (203197449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa0b3da5676d6013f7c6b9158175437d8ef9828bad7d430eb6bbca3136d5b21`  
		Last Modified: Mon, 23 Mar 2020 21:28:00 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
