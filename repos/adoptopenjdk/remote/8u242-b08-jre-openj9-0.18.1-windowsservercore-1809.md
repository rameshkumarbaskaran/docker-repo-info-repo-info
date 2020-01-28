## `adoptopenjdk:8u242-b08-jre-openj9-0.18.1-windowsservercore-1809`

```console
$ docker pull adoptopenjdk@sha256:93e486057c8c6c3670024cb2522022a5fdbc8912e9a92cd205e1322b948178be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.973; amd64

### `adoptopenjdk:8u242-b08-jre-openj9-0.18.1-windowsservercore-1809` - windows version 10.0.17763.973; amd64

```console
$ docker pull adoptopenjdk@sha256:47d14c6aa485fcc24a0aed3dcca25f6723f98cd0f19be1d38e55a65d24d13c5d
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2309853711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:177ef52abda351c2f96b30f0eaf3ba90f40f8b28261e5969bf3225b1c7a27029`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Sat, 11 Jan 2020 05:23:25 GMT
RUN Install update 1809-amd64
# Tue, 14 Jan 2020 23:46:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 28 Jan 2020 00:47:05 GMT
ENV JAVA_VERSION=jdk8u242-b08_openj9-0.18.1
# Tue, 28 Jan 2020 00:53:04 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u242-b08_openj9-0.18.1/OpenJDK8U-jre_x64_windows_openj9_8u242b08_openj9-0.18.1.msi ...');         [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;         wget https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u242-b08_openj9-0.18.1/OpenJDK8U-jre_x64_windows_openj9_8u242b08_openj9-0.18.1.msi -O 'openjdk.msi';         Write-Host ('Verifying sha256 (a8aa18b79dc2fddc9563951f975cfbf6490c8ccfc92cbda924ac7b9ed9454bf5) ...');         if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'a8aa18b79dc2fddc9563951f975cfbf6490c8ccfc92cbda924ac7b9ed9454bf5') {                 Write-Host 'FAILED!';                 exit 1;         };                 New-Item -ItemType Directory -Path C:\temp | Out-Null;                 Write-Host 'Installing using MSI ...';         Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',         '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;         Write-Host 'Removing openjdk.msi ...';         Remove-Item openjdk.msi -Force;         Remove-Item -Path C:\temp -Recurse | Out-Null;
# Tue, 28 Jan 2020 00:53:08 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+UseContainerSupport -XX:+IdleTuningCompactOnIdle -XX:+IdleTuningGcOnIdle
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:edbd72df76b46e904108d2f61a63c295b3e3d8092dbd5a03bbeb2fb4d34a3e55`  
		Size: 682.7 MB (682725872 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e9d323e253cb21832421dda4ec57dbd597bd4f934e62c162b9dec8b96e06e818`  
		Last Modified: Wed, 15 Jan 2020 01:45:20 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a10b9c8a0d2d742474d6b77a79300231bf976a0bc1b00b08c8762db8a8a52f0`  
		Last Modified: Tue, 28 Jan 2020 01:27:20 GMT  
		Size: 1.2 KB (1203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87fa61465e96fa2dff0b1b8143d95d28302e45d8971690c6332cea78d1c89a41`  
		Last Modified: Tue, 28 Jan 2020 01:29:19 GMT  
		Size: 92.4 MB (92438943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3bccef0da1a313e2ae9c72ee270a93455cc08554f53d74633d70c12177cfbdb`  
		Last Modified: Tue, 28 Jan 2020 01:29:04 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
