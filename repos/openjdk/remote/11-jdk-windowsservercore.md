## `openjdk:11-jdk-windowsservercore`

```console
$ docker pull openjdk@sha256:c7600090da40f57b3d5d0b027239d1151bbb94408ba0032205064275a3a49e60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64
	-	windows version 10.0.14393.3568; amd64

### `openjdk:11-jdk-windowsservercore` - windows version 10.0.17763.1098; amd64

```console
$ docker pull openjdk@sha256:5ab7e3b53d152081bc25a5c532d51ae0be8b6b56c9466d4e6316b2d1af09a593
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2460207435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c027c57157f572ba78ab03c59ee3bc75bc2e38839d5a0c7d73892d80bbd06167`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 06 Mar 2020 11:12:29 GMT
RUN Install update 1809-amd64
# Wed, 11 Mar 2020 00:42:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Mar 2020 15:08:43 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 11 Mar 2020 15:09:18 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Wed, 11 Mar 2020 15:09:20 GMT
ENV JAVA_VERSION=11.0.6
# Wed, 11 Mar 2020 15:09:21 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.6%2B10/OpenJDK11U-jdk_
# Wed, 11 Mar 2020 15:09:23 GMT
ENV JAVA_URL_VERSION=11.0.6_10
# Wed, 11 Mar 2020 15:11:05 GMT
RUN $url = ('{0}x64_windows_{1}.zip' -f $env:JAVA_BASE_URL, $env:JAVA_URL_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'openjdk.zip'; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 11 Mar 2020 15:11:07 GMT
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
	-	`sha256:11e649eb43fd93a65966272d23e924d3d20051943dea83bf6ae74e4f656040cc`  
		Last Modified: Wed, 11 Mar 2020 15:30:39 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0017d785620d6ed4358420d77384c6b7e5b01d6cc53cb19703e6a4b8da8f9bb6`  
		Last Modified: Wed, 11 Mar 2020 15:30:41 GMT  
		Size: 4.7 MB (4655620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb6bd3e02742ce60f814bfcbb6d4719201983c9170cd28ec4e78081c858c8b4`  
		Last Modified: Wed, 11 Mar 2020 15:30:36 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:759747b28a7619de233681630a0bdb9cf134efb80a270eae7e8432657ed63f27`  
		Last Modified: Wed, 11 Mar 2020 15:30:36 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2818ef314a8783d0453c4c06072108211cd81a8ef73194af0d5672b7d93223a4`  
		Last Modified: Wed, 11 Mar 2020 15:30:36 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35e22e75839abcf39c145bab3b437a07409e649212474d1fee1098d747c12043`  
		Last Modified: Wed, 11 Mar 2020 15:34:04 GMT  
		Size: 190.2 MB (190208734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e23b5d3f1f875117aa59ac272b84326ea3f2a613572ba2db1d83b4412c8f002e`  
		Last Modified: Wed, 11 Mar 2020 15:30:36 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:11-jdk-windowsservercore` - windows version 10.0.14393.3568; amd64

```console
$ docker pull openjdk@sha256:d3d4caf900cd4476e634a97f44d6ca4339b412ee52b4f07585ad48a08cb2cd3c
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5929448215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbe294cb4d3af0485874a759b1f8a479e2de8ecc544568829cd7a125ee6483f6`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 10 Mar 2020 08:14:00 GMT
RUN Install update ltsc2016-amd64
# Fri, 13 Mar 2020 21:32:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 13 Mar 2020 21:50:27 GMT
ENV JAVA_HOME=C:\openjdk-11
# Fri, 13 Mar 2020 21:52:09 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Fri, 13 Mar 2020 21:52:11 GMT
ENV JAVA_VERSION=11.0.6
# Fri, 13 Mar 2020 21:52:13 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.6%2B10/OpenJDK11U-jdk_
# Fri, 13 Mar 2020 21:52:14 GMT
ENV JAVA_URL_VERSION=11.0.6_10
# Fri, 13 Mar 2020 21:54:54 GMT
RUN $url = ('{0}x64_windows_{1}.zip' -f $env:JAVA_BASE_URL, $env:JAVA_URL_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'openjdk.zip'; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 13 Mar 2020 21:54:56 GMT
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
	-	`sha256:3dbaaac138e78b27185297a03aab373e6110bc40cdc639c5587dd02e533ef0ee`  
		Last Modified: Fri, 13 Mar 2020 22:13:24 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2bf8401d8ac85cf0e422f5bb94b6182bd241ef3296d41292cf76d06f5beae2b`  
		Last Modified: Fri, 13 Mar 2020 22:13:25 GMT  
		Size: 5.4 MB (5381981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89aee932ba86551f0a3e61bd8cb22047aa6112cf8c3c64a364b8b6f1399e7d89`  
		Last Modified: Fri, 13 Mar 2020 22:13:18 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c71e9686a46d43a8cd968b64ba363ce5bbde651b2bc7cdadd39c2f7fc62ef089`  
		Last Modified: Fri, 13 Mar 2020 22:13:18 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9ab17f679c35db510cb853dfd5063d1485469e0c2ccdef5ab03cf202689e1c7`  
		Last Modified: Fri, 13 Mar 2020 22:13:19 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3f9a7bf0e13e543f1a055ef13e6e4c5510903dd499c3b3be6e0cb833c3e2f13`  
		Last Modified: Fri, 13 Mar 2020 22:13:46 GMT  
		Size: 195.3 MB (195298006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fd727e304825f4ba7e4d1372fa008a0dc9e947fe03a088d4b74381165bf2c42`  
		Last Modified: Fri, 13 Mar 2020 22:13:18 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
