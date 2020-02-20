## `openjdk:11-jdk-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:998b3d74ed69f252e6526c7d5d488c8580925056791c6febf0c68b49a543874b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1040; amd64

### `openjdk:11-jdk-windowsservercore-1809` - windows version 10.0.17763.1040; amd64

```console
$ docker pull openjdk@sha256:b70b17a39f532c6b2636b1aca198f1ed8fed047fc5a1256171fcabfb7e40ae1e
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2425289638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18275362a21b93d384262575697ab7b789a3ac0e0a0f142474696ac8b21e8378`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 17 Feb 2020 06:57:13 GMT
RUN Install update 1809-amd64
# Thu, 20 Feb 2020 01:13:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 20 Feb 2020 02:35:40 GMT
ENV JAVA_HOME=C:\openjdk-11
# Thu, 20 Feb 2020 02:36:27 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Thu, 20 Feb 2020 02:36:29 GMT
ENV JAVA_VERSION=11.0.6
# Thu, 20 Feb 2020 02:36:31 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.6%2B10/OpenJDK11U-jdk_
# Thu, 20 Feb 2020 02:36:32 GMT
ENV JAVA_URL_VERSION=11.0.6_10
# Thu, 20 Feb 2020 02:38:17 GMT
RUN $url = ('{0}x64_windows_{1}.zip' -f $env:JAVA_BASE_URL, $env:JAVA_URL_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'openjdk.zip'; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Thu, 20 Feb 2020 02:38:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b5405b7580792436b60c664b5fa766ea57f5a60c1d9a8c522cf53e99e4813355`  
		Size: 695.8 MB (695818606 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2061e035d6ba931d9f00238104b970d3410f4ef0d9603b4f074c7052858e01e3`  
		Last Modified: Thu, 20 Feb 2020 03:03:21 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75452a63f3763e8ebf9d1cee8f65d83d8f7730026911a26c3697a19b816d04de`  
		Last Modified: Thu, 20 Feb 2020 03:21:28 GMT  
		Size: 1.2 KB (1203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f62aa5027d31ad22ec9323cabddb76989151f954e9a798fba622abb5fd93bcf`  
		Last Modified: Thu, 20 Feb 2020 03:21:28 GMT  
		Size: 4.6 MB (4565818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d16722bd5f07ca46cbe905e9ce786b49708cc2ebfbaa87325f401fa8512ea30e`  
		Last Modified: Thu, 20 Feb 2020 03:21:24 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d904fa3e233cd05839921abb6d3e83ca0e1733e21e7356fd57448b740ccc225`  
		Last Modified: Thu, 20 Feb 2020 03:21:23 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:671d0a672dd4a82d53918f69d007935872b7d367f5836eb6532a8ca9d98698f2`  
		Last Modified: Thu, 20 Feb 2020 03:21:24 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bdc8fc6dfb2cd07b347b83fedafb2d3ea3e4e558863bddc5512c0f5a3f51c47`  
		Last Modified: Thu, 20 Feb 2020 03:24:41 GMT  
		Size: 190.2 MB (190212815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a83b9e4d89bb8d97c6a0af751fca8a3b72a0203b5603b7586b36e0b5aa92c65`  
		Last Modified: Thu, 20 Feb 2020 03:21:24 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
