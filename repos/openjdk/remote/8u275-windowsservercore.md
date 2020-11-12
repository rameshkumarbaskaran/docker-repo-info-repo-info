## `openjdk:8u275-windowsservercore`

```console
$ docker pull openjdk@sha256:6473733e98862d753b97f6a95c910d2662a047c6d5b1dfa73afae2fff557d954
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1577; amd64
	-	windows version 10.0.14393.4046; amd64

### `openjdk:8u275-windowsservercore` - windows version 10.0.17763.1577; amd64

```console
$ docker pull openjdk@sha256:96c42ea0e7915503179c9271047487620de12b32566f2248583081829e8e8f1b
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2502945821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec3c2ed914432f6bd8cac71c5220bff276a42197baf482bf47bee396e3d32660`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 03 Nov 2020 03:11:34 GMT
RUN Install update 1809-amd64
# Wed, 11 Nov 2020 13:26:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Nov 2020 18:13:44 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 11 Nov 2020 18:14:22 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Thu, 12 Nov 2020 01:34:35 GMT
ENV JAVA_VERSION=8u275
# Thu, 12 Nov 2020 01:34:36 GMT
ENV JAVA_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u275-b01/OpenJDK8U-jdk_x64_windows_8u275b01.zip
# Thu, 12 Nov 2020 01:35:45 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac -version'; javac -version; 	Write-Host '  java -version'; java -version; 		Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:680bbdbacf1bcbace70de5087d02d31e9dd7a22feae59f746f54dab46c1d5bda`  
		Size: 669.7 MB (669696346 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:da5a67a9f3a363cb69c8104913a5a58c1c47e8f648a07d057fc28a5f98790e60`  
		Last Modified: Wed, 11 Nov 2020 13:37:50 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:961c113008286ec10d5b5ad6712c39a4f6893491652c16952e9ad9d6182a696d`  
		Last Modified: Wed, 11 Nov 2020 18:35:15 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4485491cb68a4d866c356a328fbcaa1122d7eb2ec55323238ff04c01659a1b49`  
		Last Modified: Wed, 11 Nov 2020 18:35:26 GMT  
		Size: 9.2 MB (9234346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8be0d7b941c4cc39629a0b0f78c4aa565c0b1a7798acbfc5ec0365e62d0ea4c`  
		Last Modified: Thu, 12 Nov 2020 01:57:14 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:800f5226f185597cf2b07ec974947bf1cf0a3b64148e0300b909ebc546f95256`  
		Last Modified: Thu, 12 Nov 2020 01:57:14 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:622d42176195a24fd67ebcab23c5ba37208296efcfe8ec6704d566e297c6d2fb`  
		Last Modified: Thu, 12 Nov 2020 01:57:26 GMT  
		Size: 105.7 MB (105677608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:8u275-windowsservercore` - windows version 10.0.14393.4046; amd64

```console
$ docker pull openjdk@sha256:cffc4d42166589d7a01bf417d3fab6050c674b243c598c28f610b10405f78715
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5891696225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fed3dfb24a15005d24bc6a3cade05cb7109a6e308d427a9ee4d4617af5c3dc3e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 28 Oct 2020 18:03:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Nov 2020 13:23:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Nov 2020 18:15:40 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 11 Nov 2020 18:16:53 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Thu, 12 Nov 2020 01:36:01 GMT
ENV JAVA_VERSION=8u275
# Thu, 12 Nov 2020 01:36:02 GMT
ENV JAVA_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u275-b01/OpenJDK8U-jdk_x64_windows_8u275b01.zip
# Thu, 12 Nov 2020 01:38:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac -version'; javac -version; 	Write-Host '  java -version'; java -version; 		Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4830fb08bc2df7ae80548c349b880c263ea87a7b93e13ecbc77c862b6e179558`  
		Size: 1.7 GB (1700572904 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:126d9a92c0cb7b68c56dec2dd5ba118de9dde3ec6368db734c5135fdf1528a33`  
		Last Modified: Wed, 11 Nov 2020 13:34:53 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:864d6ab6d378108050bf02ccd849c38e57d78de73c9a59d83a550d004548aefe`  
		Last Modified: Wed, 11 Nov 2020 18:37:37 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:699c3656ce68e9d61d5eddc7285fd7bd7cecaec9dbd0e3625290ecd2dfcf91d1`  
		Last Modified: Wed, 11 Nov 2020 18:37:40 GMT  
		Size: 10.1 MB (10080718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17338a5c062bee677d2a8a14e27c2dbeedb6b44519ba560b618b7f8c736bcdf4`  
		Last Modified: Thu, 12 Nov 2020 01:57:44 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5003c695350a716ace3683217cf93f8fa339894d1442b470224d2c732c6299c5`  
		Last Modified: Thu, 12 Nov 2020 01:57:43 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e257de2f426e288d3c3ba110698728e1af1c66ab31f5aac73d820b3a48461732`  
		Last Modified: Thu, 12 Nov 2020 01:57:56 GMT  
		Size: 111.1 MB (111052126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
