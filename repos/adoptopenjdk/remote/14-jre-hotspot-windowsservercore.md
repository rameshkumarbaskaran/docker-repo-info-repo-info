## `adoptopenjdk:14-jre-hotspot-windowsservercore`

```console
$ docker pull adoptopenjdk@sha256:d0538083149f4b97d2ef44d64af87296fef2e45fc900b4eefee67018ed760458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3568; amd64
	-	windows version 10.0.17763.1098; amd64

### `adoptopenjdk:14-jre-hotspot-windowsservercore` - windows version 10.0.14393.3568; amd64

```console
$ docker pull adoptopenjdk@sha256:b75d65048b99de254b20774941f6aeec5cf23a233410c93906346d677f11a464
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5827593790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ad8ff29e4454df160f924c00a1c76ae3de95f0c4125a489a95cf53ec50d3131`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 10 Mar 2020 08:14:00 GMT
RUN Install update ltsc2016-amd64
# Fri, 13 Mar 2020 21:32:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 26 Mar 2020 18:15:40 GMT
ENV JAVA_VERSION=jdk-14+36
# Thu, 26 Mar 2020 18:24:48 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk14-binaries/releases/download/jdk-14%2B36/OpenJDK14U-jre_x64_windows_hotspot_14_36.msi ...');         [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;         wget https://github.com/AdoptOpenJDK/openjdk14-binaries/releases/download/jdk-14%2B36/OpenJDK14U-jre_x64_windows_hotspot_14_36.msi -O 'openjdk.msi';         Write-Host ('Verifying sha256 (b04050c65ace822ee515c84b0856abf87deb2ff8c0586e18066eafde744233ed) ...');         if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'b04050c65ace822ee515c84b0856abf87deb2ff8c0586e18066eafde744233ed') {                 Write-Host 'FAILED!';                 exit 1;         };                 New-Item -ItemType Directory -Path C:\temp | Out-Null;                 Write-Host 'Installing using MSI ...';         Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',         '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;         Write-Host 'Removing openjdk.msi ...';         Remove-Item openjdk.msi -Force;         Remove-Item -Path C:\temp -Recurse | Out-Null;
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
	-	`sha256:bafdaf15fdfb37f3f1bad87c80f8f4879a6e5a95c2a072fbf67bde76dc4a2a90`  
		Last Modified: Thu, 26 Mar 2020 18:41:07 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47d91ca15692bbf4742867848d3c8e94ad815d3f43790fb3ee7b9c31d0f52477`  
		Last Modified: Thu, 26 Mar 2020 18:43:48 GMT  
		Size: 98.8 MB (98830458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adoptopenjdk:14-jre-hotspot-windowsservercore` - windows version 10.0.17763.1098; amd64

```console
$ docker pull adoptopenjdk@sha256:779c946d8d77adf95c2deade2a9c5592f0577dfd607627ed2034ca55a4242907
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2363517058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:494f9b7100d6180b27a5ecb2677345d551eebeff72dbfcde990b95051b3af0b9`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 06 Mar 2020 11:12:29 GMT
RUN Install update 1809-amd64
# Wed, 11 Mar 2020 00:42:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 26 Mar 2020 18:19:38 GMT
ENV JAVA_VERSION=jdk-14+36
# Thu, 26 Mar 2020 18:26:26 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk14-binaries/releases/download/jdk-14%2B36/OpenJDK14U-jre_x64_windows_hotspot_14_36.msi ...');         [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;         wget https://github.com/AdoptOpenJDK/openjdk14-binaries/releases/download/jdk-14%2B36/OpenJDK14U-jre_x64_windows_hotspot_14_36.msi -O 'openjdk.msi';         Write-Host ('Verifying sha256 (b04050c65ace822ee515c84b0856abf87deb2ff8c0586e18066eafde744233ed) ...');         if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'b04050c65ace822ee515c84b0856abf87deb2ff8c0586e18066eafde744233ed') {                 Write-Host 'FAILED!';                 exit 1;         };                 New-Item -ItemType Directory -Path C:\temp | Out-Null;                 Write-Host 'Installing using MSI ...';         Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',         '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;         Write-Host 'Removing openjdk.msi ...';         Remove-Item openjdk.msi -Force;         Remove-Item -Path C:\temp -Recurse | Out-Null;
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23645bd7ee0885911e1e2ab55ebcb36ce35795e1ceba9166ffd1b26dde18c3ee`  
		Size: 730.7 MB (730650958 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a7fab05ac5ad4b2f665ad71b5c08a81e82bff7ea2fdcbb66c14193d2dd268875`  
		Last Modified: Wed, 11 Mar 2020 01:16:21 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b36e39a8621783ad973c7afd51d903915d6901177e86c2e25f796bce8694bba4`  
		Last Modified: Thu, 26 Mar 2020 18:42:32 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:762bf767f89ec6ad32927d4252619cb49c60ae8ed8c2c7b593d59eef309b196a`  
		Last Modified: Thu, 26 Mar 2020 18:44:19 GMT  
		Size: 98.2 MB (98178414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
