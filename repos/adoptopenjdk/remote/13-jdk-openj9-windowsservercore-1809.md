## `adoptopenjdk:13-jdk-openj9-windowsservercore-1809`

```console
$ docker pull adoptopenjdk@sha256:36e4a73fbe4fed44ed3c502ba66cd4b75f35efd33d6254b2f06d177b1024fce0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.914; amd64

### `adoptopenjdk:13-jdk-openj9-windowsservercore-1809` - windows version 10.0.17763.914; amd64

```console
$ docker pull adoptopenjdk@sha256:72b073ca5eefb1a3a88c7943c223a1308af5a4eaf97af10db46cb3aa6d8dab2f
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2612718486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30ba7bb3bec961ad02b628d846c6d9df681b3f8b15a56264e4fdd190b37d868d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 29 Nov 2019 04:34:15 GMT
RUN Install update 1809-amd64
# Tue, 10 Dec 2019 21:34:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2019 21:48:39 GMT
ENV JAVA_VERSION=jdk-13.0.1+9_openj9-0.17.0
# Wed, 11 Dec 2019 21:51:30 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9_openj9-0.17.0/OpenJDK13U-jdk_x64_windows_openj9_13.0.1_9_openj9-0.17.0.msi ...');         [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;         wget https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9_openj9-0.17.0/OpenJDK13U-jdk_x64_windows_openj9_13.0.1_9_openj9-0.17.0.msi -O 'openjdk.msi';         Write-Host ('Verifying sha256 (bdcd3349615c7f6ab2102686d2ed1704b1e033bbbb227d278b9c280913af778f) ...');         if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'bdcd3349615c7f6ab2102686d2ed1704b1e033bbbb227d278b9c280913af778f') {                 Write-Host 'FAILED!';                 exit 1;         };                 New-Item -ItemType Directory -Path C:\temp | Out-Null;                 Write-Host 'Installing using MSI ...';         Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',         '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;         Write-Host 'Removing openjdk.msi ...';         Remove-Item openjdk.msi -Force;         Remove-Item -Path C:\temp -Recurse | Out-Null;
# Wed, 11 Dec 2019 21:51:32 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+UseContainerSupport -XX:+IdleTuningCompactOnIdle -XX:+IdleTuningGcOnIdle
# Wed, 11 Dec 2019 21:51:34 GMT
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
	-	`sha256:30102692d07344969de4b566b87942e49ca63e764a3f99125269fe2619180ae2`  
		Last Modified: Wed, 11 Dec 2019 22:40:33 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb1205dcfbe94a6d489c2a27624c999a18d574e02c228d5616d4e7220377901`  
		Last Modified: Wed, 11 Dec 2019 22:41:38 GMT  
		Size: 396.4 MB (396410376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d892192140ddbec4bba8354ea9b75700a227e2f5cbdd80918eaa3976f24e3332`  
		Last Modified: Wed, 11 Dec 2019 22:40:33 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c19f27928d421b3bf39c1f88f2fc2fc0fbf58808ef5d0d3c8d272f765c1b79`  
		Last Modified: Wed, 11 Dec 2019 22:40:33 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
