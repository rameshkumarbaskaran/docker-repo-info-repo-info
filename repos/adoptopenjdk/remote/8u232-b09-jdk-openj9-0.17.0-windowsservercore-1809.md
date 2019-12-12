## `adoptopenjdk:8u232-b09-jdk-openj9-0.17.0-windowsservercore-1809`

```console
$ docker pull adoptopenjdk@sha256:11e1b2f5626849ffb19b106bbcd570cd8758472ba419a2e9dfbdd029eb339dce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.914; amd64

### `adoptopenjdk:8u232-b09-jdk-openj9-0.17.0-windowsservercore-1809` - windows version 10.0.17763.914; amd64

```console
$ docker pull adoptopenjdk@sha256:219c2ccf8108d71d0e64b767ce965cf02d261eee474aea68818264df025ae8ad
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2439429187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4b742a646f08a124b35d595be0a36b738480a47ad87773cbe68ae7242ef5f32`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 29 Nov 2019 04:34:15 GMT
RUN Install update 1809-amd64
# Tue, 10 Dec 2019 21:34:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2019 21:16:36 GMT
ENV JAVA_VERSION=jdk8u232-b09_openj9-0.17.0
# Wed, 11 Dec 2019 21:18:53 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09_openj9-0.17.0/OpenJDK8U-jdk_x64_windows_openj9_8u232b09_openj9-0.17.0.msi ...');         [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;         wget https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09_openj9-0.17.0/OpenJDK8U-jdk_x64_windows_openj9_8u232b09_openj9-0.17.0.msi -O 'openjdk.msi';         Write-Host ('Verifying sha256 (c0c64822a4b657f2ac2b2185a7113070d57380153d2e1d6c20e04aa33cb295ae) ...');         if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'c0c64822a4b657f2ac2b2185a7113070d57380153d2e1d6c20e04aa33cb295ae') {                 Write-Host 'FAILED!';                 exit 1;         };                 New-Item -ItemType Directory -Path C:\temp | Out-Null;                 Write-Host 'Installing using MSI ...';         Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',         '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;         Write-Host 'Removing openjdk.msi ...';         Remove-Item openjdk.msi -Force;         Remove-Item -Path C:\temp -Recurse | Out-Null;
# Wed, 11 Dec 2019 21:18:55 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+UseContainerSupport -XX:+IdleTuningCompactOnIdle -XX:+IdleTuningGcOnIdle
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
	-	`sha256:dc8a458b25dccd8f456aca6e7bc87bdc8fabb7cb5e131f60f3a7cb9b0ea18a00`  
		Last Modified: Wed, 11 Dec 2019 22:28:05 GMT  
		Size: 1.2 KB (1215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e548cd12d0be87c33743e2e69dac106e0e61bc0d348bdf902d84547a44902acc`  
		Last Modified: Wed, 11 Dec 2019 22:28:37 GMT  
		Size: 223.1 MB (223122229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f6bb72a1d9cba8f0989b6ab8f83ddb0aefb21f63e35b844d930e0927cd6d56e`  
		Last Modified: Wed, 11 Dec 2019 22:28:05 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
