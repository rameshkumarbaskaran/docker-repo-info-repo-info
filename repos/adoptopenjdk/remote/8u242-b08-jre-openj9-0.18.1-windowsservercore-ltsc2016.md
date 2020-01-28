## `adoptopenjdk:8u242-b08-jre-openj9-0.18.1-windowsservercore-ltsc2016`

```console
$ docker pull adoptopenjdk@sha256:07a143348ab24fa9cd74fe2af1ad4324d129c796f09aa56622fcd4baf0a6134e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3443; amd64

### `adoptopenjdk:8u242-b08-jre-openj9-0.18.1-windowsservercore-ltsc2016` - windows version 10.0.14393.3443; amd64

```console
$ docker pull adoptopenjdk@sha256:69b5adab9b315193dffc2aaf121043babb075e8cf7d23a34e07260692727c739
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5817805662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb0c0e32d6f6a2d91902172dbf98cd1c8affd615d2efc3dc18dfef208bab9874`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Thu, 02 Jan 2020 15:48:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 14 Jan 2020 23:50:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 28 Jan 2020 00:44:01 GMT
ENV JAVA_VERSION=jdk8u242-b08_openj9-0.18.1
# Tue, 28 Jan 2020 00:51:28 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u242-b08_openj9-0.18.1/OpenJDK8U-jre_x64_windows_openj9_8u242b08_openj9-0.18.1.msi ...');         [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;         wget https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u242-b08_openj9-0.18.1/OpenJDK8U-jre_x64_windows_openj9_8u242b08_openj9-0.18.1.msi -O 'openjdk.msi';         Write-Host ('Verifying sha256 (a8aa18b79dc2fddc9563951f975cfbf6490c8ccfc92cbda924ac7b9ed9454bf5) ...');         if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'a8aa18b79dc2fddc9563951f975cfbf6490c8ccfc92cbda924ac7b9ed9454bf5') {                 Write-Host 'FAILED!';                 exit 1;         };                 New-Item -ItemType Directory -Path C:\temp | Out-Null;                 Write-Host 'Installing using MSI ...';         Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',         '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;         Write-Host 'Removing openjdk.msi ...';         Remove-Item openjdk.msi -Force;         Remove-Item -Path C:\temp -Recurse | Out-Null;
# Tue, 28 Jan 2020 00:51:30 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+UseContainerSupport -XX:+IdleTuningCompactOnIdle -XX:+IdleTuningGcOnIdle
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:31f9df80631e7b5d379647ee7701ff50e009bd2c03b30a67a0a8e7bba4a26f94`  
		Size: 1.7 GB (1654613376 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f1c8c4c99f36cfcf87884a9382011e93fb05fa4002d8f4eca62a43e744db8e95`  
		Last Modified: Wed, 15 Jan 2020 01:46:47 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3323651339113d8d34ce6b152e9af71bf42429e00437d21461a5a3e6a635f933`  
		Last Modified: Tue, 28 Jan 2020 01:26:18 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc24f57032654fc19b75de5b119db3b8f59cc65eb01eb4dd6131390f5d743f46`  
		Last Modified: Tue, 28 Jan 2020 01:28:28 GMT  
		Size: 93.2 MB (93202820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff195db232255c892d55cb58a54f1470ec0b45f14dcbe1e404ecc698aae03822`  
		Last Modified: Tue, 28 Jan 2020 01:28:15 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
