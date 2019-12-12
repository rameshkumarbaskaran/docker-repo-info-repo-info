## `adoptopenjdk:8-openj9-windowsservercore-1803`

```console
$ docker pull adoptopenjdk@sha256:e4010bc74643f2b5b07b68d9c2b8ffd3aacea3b66a46f94e6aac17adc322c3f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17134.1184; amd64

### `adoptopenjdk:8-openj9-windowsservercore-1803` - windows version 10.0.17134.1184; amd64

```console
$ docker pull adoptopenjdk@sha256:49fab510bf1acbc8b7b24ee3cc604d472a439d855e832545eb6428b66fa1a46d
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2579987174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dea01125dd9d8bfd3a71e48c6c07d26e2227f12f7bd1fe88f3860a176a8c719`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 12 Apr 2018 09:20:54 GMT
RUN Apply image 1803-RTM-amd64
# Wed, 04 Dec 2019 15:21:18 GMT
RUN Install update 1803-amd64
# Wed, 11 Dec 2019 20:25:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2019 21:19:09 GMT
ENV JAVA_VERSION=jdk8u232-b09_openj9-0.17.0
# Wed, 11 Dec 2019 21:21:43 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09_openj9-0.17.0/OpenJDK8U-jdk_x64_windows_openj9_8u232b09_openj9-0.17.0.msi ...');         [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;         wget https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09_openj9-0.17.0/OpenJDK8U-jdk_x64_windows_openj9_8u232b09_openj9-0.17.0.msi -O 'openjdk.msi';         Write-Host ('Verifying sha256 (c0c64822a4b657f2ac2b2185a7113070d57380153d2e1d6c20e04aa33cb295ae) ...');         if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'c0c64822a4b657f2ac2b2185a7113070d57380153d2e1d6c20e04aa33cb295ae') {                 Write-Host 'FAILED!';                 exit 1;         };                 New-Item -ItemType Directory -Path C:\temp | Out-Null;                 Write-Host 'Installing using MSI ...';         Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',         '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;         Write-Host 'Removing openjdk.msi ...';         Remove-Item openjdk.msi -Force;         Remove-Item -Path C:\temp -Recurse | Out-Null;
# Wed, 11 Dec 2019 21:21:45 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+UseContainerSupport -XX:+IdleTuningCompactOnIdle -XX:+IdleTuningGcOnIdle
```

-	Layers:
	-	`sha256:d9e8b01179bfc94a5bdb1810fbd76b999aa52016001ace2d3a4c4bc7065a9601`  
		Last Modified: Tue, 18 Sep 2018 22:43:55 GMT  
		Size: 1.7 GB (1659688273 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d117323cd539488e5ef3bef575a41fa714d83119b0da1896607d96ec2a5e3b52`  
		Size: 696.9 MB (696873564 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:76b68c2d6c99fac63a7998081753df26697a83f71d1138943905bde6cb959583`  
		Last Modified: Wed, 11 Dec 2019 22:12:46 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83b2b390540a91a8eb8dc86cc503cd1f4668031d778b9af0daf237db7f7f4224`  
		Last Modified: Wed, 11 Dec 2019 22:29:07 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a43f44f679b7587e442734499e8bc735cf0e29c4e07ab1c84e2d8c8f821ea79`  
		Last Modified: Wed, 11 Dec 2019 22:29:34 GMT  
		Size: 223.4 MB (223421870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a957a98bea6042e7cae371cc087be6befa79c74053f1e879c30f18505f4f79f7`  
		Last Modified: Wed, 11 Dec 2019 22:29:07 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
