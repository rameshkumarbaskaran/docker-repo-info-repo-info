## `openjdk:8-jdk-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:28933d667cd0a8c31df533be1bdd533d21fde301997b6903ebcc0a8f608aa810
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1697; amd64

### `openjdk:8-jdk-windowsservercore-1809` - windows version 10.0.17763.1697; amd64

```console
$ docker pull openjdk@sha256:70e86bc22a9c11d794e7fa2f77f3b36f56c66a545f4f346aa765d60565c28fe6
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2550867357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe68b178d6f847b6c3a3ef8257d282cb7ffcc93f321e126c19340c33bcf0c76c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 08 Jan 2021 08:50:52 GMT
RUN Install update 1809-amd64
# Wed, 13 Jan 2021 13:13:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Jan 2021 20:55:59 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 13 Jan 2021 20:56:41 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Thu, 21 Jan 2021 02:24:40 GMT
ENV JAVA_VERSION=8u282
# Thu, 21 Jan 2021 02:24:41 GMT
ENV JAVA_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u282-b08/OpenJDK8U-jdk_x64_windows_8u282b08.zip
# Thu, 21 Jan 2021 02:25:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac -version'; javac -version; 	Write-Host '  java -version'; java -version; 		Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4dcc9a9b9e680514ef3fdfcc2ce08a3768f9e412703faa137f4a7c8297600052`  
		Size: 717.4 MB (717439216 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e00081a98bb2679c3c5f469e09d475980133a20987f9cae4cf4f7aedf59f9d8f`  
		Last Modified: Wed, 13 Jan 2021 13:17:19 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1014559aa8330920e2a61da1c7cc26b15e9fe552eb1d26ec9bbb38f190014347`  
		Last Modified: Wed, 13 Jan 2021 21:37:46 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:055aa085f13458ec1beb7302362f1caac423112886af03fcdc8814f1984e00bb`  
		Last Modified: Wed, 13 Jan 2021 21:37:50 GMT  
		Size: 9.4 MB (9361116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c7892dd711fed914d99e12f4e78e4f6be8e09c862e4e682e2ce4a421af6705b`  
		Last Modified: Thu, 21 Jan 2021 02:43:15 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d30a4fd69cc2b37abeb29c52a1f65f79dae683f5954bd03c04e8880e53fee8ef`  
		Last Modified: Thu, 21 Jan 2021 02:43:15 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeb90b62313be86f1abf3b1894598c18c9fc2cbf8f2e6c0a7b6990c44e2aa9f3`  
		Last Modified: Thu, 21 Jan 2021 02:43:29 GMT  
		Size: 105.7 MB (105729072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
