## `adoptopenjdk:8u232-b09-jre-hotspot-windowsservercore-ltsc2016`

```console
$ docker pull adoptopenjdk@sha256:34c32cd90aa94f9c32aec446443922b229ced180e75e5979551d063ec46e5e79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3506; amd64

### `adoptopenjdk:8u232-b09-jre-hotspot-windowsservercore-ltsc2016` - windows version 10.0.14393.3506; amd64

```console
$ docker pull adoptopenjdk@sha256:8ddbd2fd1256bdb72158edec05bbd0e10cb48056c622595113241d8b59b60ab7
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5805595743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d59ba8c7c5b389f585cc3d11240fd7612f9b154e6fa7dafcecdaa7bf05b2852f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 14 Feb 2020 21:42:00 GMT
RUN Install update ltsc2016-amd64
# Thu, 20 Feb 2020 01:48:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 20 Feb 2020 10:38:19 GMT
ENV JAVA_VERSION=jdk8u232-b09
# Thu, 20 Feb 2020 10:46:31 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jre_x64_windows_hotspot_8u232b09.msi ...');         [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;         wget https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jre_x64_windows_hotspot_8u232b09.msi -O 'openjdk.msi';         Write-Host ('Verifying sha256 (5fe6d4d666f87168354da7ea1be99d74973b2d31bdbd225f45c30e67044887ba) ...');         if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '5fe6d4d666f87168354da7ea1be99d74973b2d31bdbd225f45c30e67044887ba') {                 Write-Host 'FAILED!';                 exit 1;         };                 New-Item -ItemType Directory -Path C:\temp | Out-Null;                 Write-Host 'Installing using MSI ...';         Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',         '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;         Write-Host 'Removing openjdk.msi ...';         Remove-Item openjdk.msi -Force;         Remove-Item -Path C:\temp -Recurse | Out-Null;
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:846a2223e9e7a88a2a07d706553f144d380483d72fb9f0697c4fcd71773a8693`  
		Size: 1.7 GB (1657079102 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:72c4471958f7f0f07260f0f430bcffb0bc07811088c24cffba1439d250ea1ae3`  
		Last Modified: Thu, 20 Feb 2020 03:04:52 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54a0e56ce74b3e43a89a657481038b04d3730997a2b3a55da4f191b001ffc14f`  
		Last Modified: Thu, 20 Feb 2020 11:45:21 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6192700473ee3f7fc906fd40c5b8a9d41b7dd8fffef62d68f353cdcd2c1b9fd1`  
		Last Modified: Thu, 20 Feb 2020 11:47:44 GMT  
		Size: 78.5 MB (78528339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
