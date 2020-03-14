## `openjdk:11-jre-windowsservercore-ltsc2016`

```console
$ docker pull openjdk@sha256:04e99f22f8f161b534ea3e1a41b94a93dd703e94b9146fc37aa821ed27a87171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3568; amd64

### `openjdk:11-jre-windowsservercore-ltsc2016` - windows version 10.0.14393.3568; amd64

```console
$ docker pull openjdk@sha256:1e98b72975c8e2dc1439dd4c757540cc023cd14a6869d2bf6d9f73a9798da7ba
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5778629274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0561e14e1e5b07fdb40e93303cda403cffe3ed645ed2ed19f78943feabc896fa`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
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
# Fri, 13 Mar 2020 21:55:27 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.6%2B10/OpenJDK11U-jre_
# Fri, 13 Mar 2020 21:55:28 GMT
ENV JAVA_URL_VERSION=11.0.6_10
# Fri, 13 Mar 2020 21:57:30 GMT
RUN $url = ('{0}x64_windows_{1}.zip' -f $env:JAVA_BASE_URL, $env:JAVA_URL_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'openjdk.zip'; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
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
	-	`sha256:56943e6a96620ea935c499c0a2cd4c43ab6864f8bff8ab2c11747e4177a9ebc9`  
		Last Modified: Fri, 13 Mar 2020 22:14:12 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab7f9810f4e7555b67c639e96abe73c0b6952d73dc73bb3a7302275bec6326d7`  
		Last Modified: Fri, 13 Mar 2020 22:14:12 GMT  
		Size: 1.2 KB (1217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de83d68036a4b3060bcb0b2bdf1bf487ab13f27699d2e7bde1e09d411ebf8a41`  
		Last Modified: Fri, 13 Mar 2020 22:14:25 GMT  
		Size: 44.5 MB (44480261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
