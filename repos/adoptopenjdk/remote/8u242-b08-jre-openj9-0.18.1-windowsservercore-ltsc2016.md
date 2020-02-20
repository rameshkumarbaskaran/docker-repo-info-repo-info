## `adoptopenjdk:8u242-b08-jre-openj9-0.18.1-windowsservercore-ltsc2016`

```console
$ docker pull adoptopenjdk@sha256:cc9a5427b4696f9dcea893a6f4a16d0293bbaf267e6d2560a8fbda2011689154
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3506; amd64

### `adoptopenjdk:8u242-b08-jre-openj9-0.18.1-windowsservercore-ltsc2016` - windows version 10.0.14393.3506; amd64

```console
$ docker pull adoptopenjdk@sha256:7fedecbd314d2ed82c4df6e22243a4a10534a9c9273d6271da435382e0f01c6c
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5820247979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:168678d29c49c65cc5f301c368801060e248170046bd744fe78d14dc39a59027`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 14 Feb 2020 21:42:00 GMT
RUN Install update ltsc2016-amd64
# Thu, 20 Feb 2020 01:48:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 20 Feb 2020 11:11:11 GMT
ENV JAVA_VERSION=jdk8u242-b08_openj9-0.18.1
# Thu, 20 Feb 2020 11:19:09 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u242-b08_openj9-0.18.1/OpenJDK8U-jre_x64_windows_openj9_8u242b08_openj9-0.18.1.msi ...');         [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;         wget https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u242-b08_openj9-0.18.1/OpenJDK8U-jre_x64_windows_openj9_8u242b08_openj9-0.18.1.msi -O 'openjdk.msi';         Write-Host ('Verifying sha256 (a8aa18b79dc2fddc9563951f975cfbf6490c8ccfc92cbda924ac7b9ed9454bf5) ...');         if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'a8aa18b79dc2fddc9563951f975cfbf6490c8ccfc92cbda924ac7b9ed9454bf5') {                 Write-Host 'FAILED!';                 exit 1;         };                 New-Item -ItemType Directory -Path C:\temp | Out-Null;                 Write-Host 'Installing using MSI ...';         Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',         '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;         Write-Host 'Removing openjdk.msi ...';         Remove-Item openjdk.msi -Force;         Remove-Item -Path C:\temp -Recurse | Out-Null;
# Thu, 20 Feb 2020 11:19:11 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+UseContainerSupport -XX:+IdleTuningCompactOnIdle -XX:+IdleTuningGcOnIdle
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
	-	`sha256:b981f375364895ed9d514cf4624f03c7719eddd3aff20ea24e55f91d10550790`  
		Last Modified: Thu, 20 Feb 2020 12:03:11 GMT  
		Size: 1.2 KB (1203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ad6dd18182710ea6c27b38fe4aa120541bddb9517509a412a9efc37a4aeed6`  
		Last Modified: Thu, 20 Feb 2020 12:06:03 GMT  
		Size: 93.2 MB (93179429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc0a068a07934d5ee42fca6b73ebaab9ce23db2e780825a70a0ab7bf130b74d1`  
		Last Modified: Thu, 20 Feb 2020 12:05:49 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
