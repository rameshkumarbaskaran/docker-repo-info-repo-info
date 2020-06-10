## `openjdk:8u252-jre-windowsservercore`

```console
$ docker pull openjdk@sha256:f2b2aa27f98ee9641b68491d1c381fcbb58e19d135f93867c95167787a6faf59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1282; amd64
	-	windows version 10.0.14393.3750; amd64

### `openjdk:8u252-jre-windowsservercore` - windows version 10.0.17763.1282; amd64

```console
$ docker pull openjdk@sha256:050fc179c215dc3812f809c358a2e37c27133e6dbd1b98afac2cfae1f6e62893
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2336408060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fba6c7187e469055f6f04eb6503e6a42c90f10fc90bb4142879887bd0ea9d62`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Jun 2020 01:48:42 GMT
RUN Install update 1809-amd64
# Tue, 09 Jun 2020 22:33:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Jun 2020 23:04:41 GMT
ENV JAVA_HOME=C:\openjdk-8
# Tue, 09 Jun 2020 23:05:22 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Tue, 09 Jun 2020 23:05:23 GMT
ENV JAVA_VERSION=8u252
# Tue, 09 Jun 2020 23:12:02 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jre_
# Tue, 09 Jun 2020 23:12:03 GMT
ENV JAVA_URL_VERSION=8u252b09
# Tue, 09 Jun 2020 23:12:51 GMT
RUN $url = ('{0}x64_windows_{1}.zip' -f $env:JAVA_BASE_URL, $env:JAVA_URL_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'openjdk.zip'; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  java -version'; java -version; 		Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:666079ee04606f07f4a27dd98526f5049ef8fed93e347d8b4c447b0d5060c77d`  
		Size: 575.6 MB (575581379 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f841c6a0c622cd36b5b2688011a224ac3e8e96273758f4a2804f2f3f099f267d`  
		Last Modified: Tue, 09 Jun 2020 23:17:50 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b52332a6d13a4eceaf15230fbd96c1f7136ebbb1b447dbee2026fa966d16e5d5`  
		Last Modified: Tue, 09 Jun 2020 23:32:34 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57dd3b73be0c8bbdcab3e2ddbd39573c9fa7aa2e25a64801dd873a8d424d12fa`  
		Last Modified: Tue, 09 Jun 2020 23:32:34 GMT  
		Size: 4.8 MB (4762718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfbc99c9dcdf8401e437fd2bada9fbde4f01b912a801ccc7329e710a44dfd1d5`  
		Last Modified: Tue, 09 Jun 2020 23:32:32 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e60cf02843aae5a69c5fefd8f6c160a29398eb36b8c3eaa613ad63d55daa3a0c`  
		Last Modified: Tue, 09 Jun 2020 23:33:55 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e8164b11ced3c4d8458af0f9eecf57a8856f339875170f756258d43cb610f7e`  
		Last Modified: Tue, 09 Jun 2020 23:33:55 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b1b5a82a7924194553d78c5769dcb5202d706146c21838f005484556f39bd6f`  
		Last Modified: Tue, 09 Jun 2020 23:34:36 GMT  
		Size: 37.7 MB (37725315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:8u252-jre-windowsservercore` - windows version 10.0.14393.3750; amd64

```console
$ docker pull openjdk@sha256:0bfa96b35d8275d17768b0ad79220c0e352a8bafcf2e57cb9bc7dfef85a05d20
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5782199682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f89f2f734e5f27c73f557e17cf88facfa1963d581ec6c15b40558e286f4aa75`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 01 Jun 2020 18:53:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 09 Jun 2020 22:36:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Jun 2020 23:06:53 GMT
ENV JAVA_HOME=C:\openjdk-8
# Tue, 09 Jun 2020 23:08:17 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Tue, 09 Jun 2020 23:08:18 GMT
ENV JAVA_VERSION=8u252
# Tue, 09 Jun 2020 23:13:03 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jre_
# Tue, 09 Jun 2020 23:13:04 GMT
ENV JAVA_URL_VERSION=8u252b09
# Tue, 09 Jun 2020 23:14:52 GMT
RUN $url = ('{0}x64_windows_{1}.zip' -f $env:JAVA_BASE_URL, $env:JAVA_URL_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'openjdk.zip'; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  java -version'; java -version; 		Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:375fbabb84945635805b46a02a17ac15a3177bcaae7404cfab5f1ceb0460cb60`  
		Size: 1.7 GB (1664011795 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c938241e0507e1ada5f864325483d86fd08533a5a31e7cb6ec1357db9891b245`  
		Last Modified: Tue, 09 Jun 2020 23:18:33 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6efeab943acb379b8bd4d0dc4f19a541b7538946603e0267a1dab8dc1528783`  
		Last Modified: Tue, 09 Jun 2020 23:33:02 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d5ac5751f3659ba87911bad898574099b553cd1ce9b816ff347f04e6cee8c58`  
		Last Modified: Tue, 09 Jun 2020 23:33:01 GMT  
		Size: 5.4 MB (5386119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a117a4a0f0bd8cd0a3f93efe8ee96d4e1756e36d81c8294318a861f6d5042644`  
		Last Modified: Tue, 09 Jun 2020 23:32:59 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51648851eab2836bd893dfdb403b107273d3f5a9fc98c904fced18cc715ea2d0`  
		Last Modified: Tue, 09 Jun 2020 23:34:47 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65d539b1c52a475a11dfd7acde928f749ef956e21e8c4633c8804019a3836a36`  
		Last Modified: Tue, 09 Jun 2020 23:34:46 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52da5551c3ae414d8a3f0162a9d837fa6335f0df15752665bdbde456f3e86915`  
		Last Modified: Tue, 09 Jun 2020 23:34:54 GMT  
		Size: 42.8 MB (42810171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
