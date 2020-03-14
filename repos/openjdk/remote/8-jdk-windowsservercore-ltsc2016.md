## `openjdk:8-jdk-windowsservercore-ltsc2016`

```console
$ docker pull openjdk@sha256:c4f47b5090a3ee0cf95c8ec5b77d376f315afc38b6d0168a66b2490da922872e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3568; amd64

### `openjdk:8-jdk-windowsservercore-ltsc2016` - windows version 10.0.14393.3568; amd64

```console
$ docker pull openjdk@sha256:75afabe7d2a5ab2d893ecd2fcc185620e05442cd135bda7aea40a9f6f437f978
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5839017631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6d5742f46cc611087137cf9930e33052fbe06a264f44ecef4743c4adbb68f80`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 10 Mar 2020 08:14:00 GMT
RUN Install update ltsc2016-amd64
# Fri, 13 Mar 2020 21:32:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 13 Mar 2020 21:57:55 GMT
ENV JAVA_HOME=C:\openjdk-8
# Fri, 13 Mar 2020 21:59:15 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Fri, 13 Mar 2020 21:59:17 GMT
ENV JAVA_VERSION=8u242
# Fri, 13 Mar 2020 21:59:19 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u242-b08/OpenJDK8U-jdk_
# Fri, 13 Mar 2020 21:59:20 GMT
ENV JAVA_URL_VERSION=8u242b08
# Fri, 13 Mar 2020 22:01:45 GMT
RUN $url = ('{0}x64_windows_{1}.zip' -f $env:JAVA_BASE_URL, $env:JAVA_URL_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'openjdk.zip'; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac -version'; javac -version; 	Write-Host '  java -version'; java -version; 		Write-Host 'Complete.'
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
	-	`sha256:3914fd59d83a115b2171e327c8d29e0f9623505b1452d20fdefa58d20c160d57`  
		Last Modified: Fri, 13 Mar 2020 22:14:46 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2578df19454647b32e930bddcfe60fa43fd7c0d03803bb428f24d791655a41f7`  
		Last Modified: Fri, 13 Mar 2020 22:14:45 GMT  
		Size: 5.4 MB (5378404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:129cab9706a9294ee544e4992668ac6ecb3d7a8626ef633db19d93e28f773875`  
		Last Modified: Fri, 13 Mar 2020 22:14:42 GMT  
		Size: 1.2 KB (1218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae19d100f0bea65fc5f1170908046a1eccd745e161b95c0571d1e262b6d7d0e8`  
		Last Modified: Fri, 13 Mar 2020 22:14:43 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc92fa77c4b265e23ea090dc08a11e1cdd097e9249fd7d89283382bc83abf77f`  
		Last Modified: Fri, 13 Mar 2020 22:14:42 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edbe41fb6e1179ffc2c643112c8043f1082c723d7a9754c4e1227ff4dbefdb2f`  
		Last Modified: Fri, 13 Mar 2020 22:15:03 GMT  
		Size: 104.9 MB (104872182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
