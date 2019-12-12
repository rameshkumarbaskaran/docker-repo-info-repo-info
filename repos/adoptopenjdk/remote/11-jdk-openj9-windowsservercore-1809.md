## `adoptopenjdk:11-jdk-openj9-windowsservercore-1809`

```console
$ docker pull adoptopenjdk@sha256:8c41c01baa5228420dde5f91d8290585d45aef68c5e706913ef91e861397016c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.914; amd64

### `adoptopenjdk:11-jdk-openj9-windowsservercore-1809` - windows version 10.0.17763.914; amd64

```console
$ docker pull adoptopenjdk@sha256:a1bb3fec5a8692954db24f0ac88f798fab49b7ac978374743486003fb30ec378
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2601689670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09120a204b29a4d0aa1230ab9a5ffd3202d0a90bc61826db76e26e46f06911a0`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 29 Nov 2019 04:34:15 GMT
RUN Install update 1809-amd64
# Tue, 10 Dec 2019 21:34:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2019 21:32:14 GMT
ENV JAVA_VERSION=jdk-11.0.5+10_openj9-0.17.0
# Wed, 11 Dec 2019 21:35:16 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.5%2B10_openj9-0.17.0/OpenJDK11U-jdk_x64_windows_openj9_11.0.5_10_openj9-0.17.0.msi ...');         [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;         wget https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.5%2B10_openj9-0.17.0/OpenJDK11U-jdk_x64_windows_openj9_11.0.5_10_openj9-0.17.0.msi -O 'openjdk.msi';         Write-Host ('Verifying sha256 (434de0c634d08b1e1490c616f33fa9f002e8d8d40c3d4c8bf09dca0a44f5d710) ...');         if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '434de0c634d08b1e1490c616f33fa9f002e8d8d40c3d4c8bf09dca0a44f5d710') {                 Write-Host 'FAILED!';                 exit 1;         };                 New-Item -ItemType Directory -Path C:\temp | Out-Null;                 Write-Host 'Installing using MSI ...';         Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',         '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;         Write-Host 'Removing openjdk.msi ...';         Remove-Item openjdk.msi -Force;         Remove-Item -Path C:\temp -Recurse | Out-Null;
# Wed, 11 Dec 2019 21:35:18 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+UseContainerSupport -XX:+IdleTuningCompactOnIdle -XX:+IdleTuningGcOnIdle
# Wed, 11 Dec 2019 21:35:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:faf31ee0aa3d3c60a38dd03c7554d632065cef50eab052ef1444590786249d07`  
		Size: 681.6 MB (681618026 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e147f14e0d6a9cbd5261162dea8f3aac7a34db5d9f6a587a9aac6b88722a2da4`  
		Last Modified: Tue, 10 Dec 2019 22:07:34 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8631bbc4bb3e5bee1414faacf34032c7bf59c67d85ed6f6aacf4ec6a6072b6db`  
		Last Modified: Wed, 11 Dec 2019 22:33:54 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8889da5ad26bfadf4e8e5cc64aa83d51f17db7a6934ccd39345d84c881952307`  
		Last Modified: Wed, 11 Dec 2019 22:35:13 GMT  
		Size: 385.4 MB (385381500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7958a595bbbba5a11da6a77bee8a8ad5c02a9630483ed8de6f54843369c5f1f`  
		Last Modified: Wed, 11 Dec 2019 22:33:53 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bdc70e2ab87b6f10064e2c43e6d423904f11466074b66136bcad7a7e91e4b94`  
		Last Modified: Wed, 11 Dec 2019 22:33:54 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
