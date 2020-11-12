## `openjdk:11-jdk-windowsservercore-ltsc2016`

```console
$ docker pull openjdk@sha256:1e081f8391adbfc6ccd0639ffa31e059d727d3a3ce770c48d14af002397a682a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4046; amd64

### `openjdk:11-jdk-windowsservercore-ltsc2016` - windows version 10.0.14393.4046; amd64

```console
$ docker pull openjdk@sha256:618ad2c6131653534c05a1db81a801dec9f73c7427ae4f949540004385ead810
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 GB (5981360711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6532e3437ed3c3d91ca491f876bd58c2e81ce8e482aa47858b774f6441c8ef5`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 28 Oct 2020 18:03:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Nov 2020 13:23:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Nov 2020 18:05:05 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 11 Nov 2020 18:06:20 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Thu, 12 Nov 2020 01:27:19 GMT
ENV JAVA_VERSION=11.0.9.1
# Thu, 12 Nov 2020 01:27:20 GMT
ENV JAVA_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.9.1%2B1/OpenJDK11U-jdk_x64_windows_11.0.9.1_1.zip
# Thu, 12 Nov 2020 01:29:47 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Thu, 12 Nov 2020 01:29:49 GMT
CMD ["jshell"]
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
	-	`sha256:40be1fb26a8773b8a3f641f7c3725588991d90ca4f0a50882c02545abe56278f`  
		Last Modified: Wed, 11 Nov 2020 18:31:35 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44de1279f62435080fd4e85f046c6470cd3785563ac42771ade9bec484f0b312`  
		Last Modified: Wed, 11 Nov 2020 18:31:34 GMT  
		Size: 10.1 MB (10079557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac2a2807012820ea28ae6d2d6425305fd549fba3b4b09985d6434503b4ccf8c`  
		Last Modified: Thu, 12 Nov 2020 01:51:45 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e72fe945c020ed4cd94e553cae93193dea26b22c47f769d73733e637fb2c1860`  
		Last Modified: Thu, 12 Nov 2020 01:51:44 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd71b42e374ea2cc7c02a7d4689bdc6ac90d8198b4a9d0da90a23f5284806591`  
		Last Modified: Thu, 12 Nov 2020 01:52:04 GMT  
		Size: 200.7 MB (200716760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5a39c9d244663f4a1128ff64392f3368cac85b2da7534b3257d6a2d54b87d05`  
		Last Modified: Thu, 12 Nov 2020 01:51:45 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
