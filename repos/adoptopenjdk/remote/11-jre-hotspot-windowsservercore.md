## `adoptopenjdk:11-jre-hotspot-windowsservercore`

```console
$ docker pull adoptopenjdk@sha256:fc68aeee26eb3758097434fec9460becd1b384508d5b36fd73e9c151611d7857
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3384; amd64
	-	windows version 10.0.17763.914; amd64
	-	windows version 10.0.17134.1184; amd64

### `adoptopenjdk:11-jre-hotspot-windowsservercore` - windows version 10.0.14393.3384; amd64

```console
$ docker pull adoptopenjdk@sha256:1705486d8657b0cfca223751ed478587084862fda6d7822382dc1f4ffa8852c5
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5799185004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3deb4120e6482cb7324a341fa7e63d86a5592a9ce6cfe98d261e5d8a05cd9a9f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 27 Nov 2019 14:43:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Dec 2019 00:35:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2019 20:33:36 GMT
ENV JAVA_VERSION=jdk-11.0.5+10
# Wed, 11 Dec 2019 20:45:46 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.5%2B10/OpenJDK11U-jre_x64_windows_hotspot_11.0.5_10.msi ...');         [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;         wget https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.5%2B10/OpenJDK11U-jre_x64_windows_hotspot_11.0.5_10.msi -O 'openjdk.msi';         Write-Host ('Verifying sha256 (3d06a2bde2bf9cad88bf151aa789528a87353a18c26f17cf259fa86439c9c417) ...');         if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '3d06a2bde2bf9cad88bf151aa789528a87353a18c26f17cf259fa86439c9c417') {                 Write-Host 'FAILED!';                 exit 1;         };                 New-Item -ItemType Directory -Path C:\temp | Out-Null;                 Write-Host 'Installing using MSI ...';         Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',         '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;         Write-Host 'Removing openjdk.msi ...';         Remove-Item openjdk.msi -Force;         Remove-Item -Path C:\temp -Recurse | Out-Null;
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:55d044e60c8959ce88aee467913bb11827c1ec057a2fd108a293e274dbd74f1d`  
		Size: 1.7 GB (1652717978 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:530e4240d4261ce165890648d1df6230dc4f9ce5df2e6cf9f0d5876694c3d4f0`  
		Last Modified: Wed, 11 Dec 2019 01:14:39 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73cdabb8bd4292a6e5eb846dd0b34a08d0aff7cc337d6e216c2c49086b684b52`  
		Last Modified: Wed, 11 Dec 2019 22:15:22 GMT  
		Size: 1.2 KB (1199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f014667f9203be19049e8b912123661e8482489b376817d233bd985f92a44df0`  
		Last Modified: Wed, 11 Dec 2019 22:19:09 GMT  
		Size: 76.5 MB (76478719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adoptopenjdk:11-jre-hotspot-windowsservercore` - windows version 10.0.17763.914; amd64

```console
$ docker pull adoptopenjdk@sha256:bf54176717759609fad92e554a86fb51794b8f2e31ad1087fc13c9f881822e24
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2292055954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:683256147282e55489730eb0bcef43a8d0d55316746f0135362c20372a44c862`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 29 Nov 2019 04:34:15 GMT
RUN Install update 1809-amd64
# Tue, 10 Dec 2019 21:34:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2019 20:37:25 GMT
ENV JAVA_VERSION=jdk-11.0.5+10
# Wed, 11 Dec 2019 20:47:28 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.5%2B10/OpenJDK11U-jre_x64_windows_hotspot_11.0.5_10.msi ...');         [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;         wget https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.5%2B10/OpenJDK11U-jre_x64_windows_hotspot_11.0.5_10.msi -O 'openjdk.msi';         Write-Host ('Verifying sha256 (3d06a2bde2bf9cad88bf151aa789528a87353a18c26f17cf259fa86439c9c417) ...');         if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '3d06a2bde2bf9cad88bf151aa789528a87353a18c26f17cf259fa86439c9c417') {                 Write-Host 'FAILED!';                 exit 1;         };                 New-Item -ItemType Directory -Path C:\temp | Out-Null;                 Write-Host 'Installing using MSI ...';         Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',         '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;         Write-Host 'Removing openjdk.msi ...';         Remove-Item openjdk.msi -Force;         Remove-Item -Path C:\temp -Recurse | Out-Null;
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
	-	`sha256:5755881a66d10243b0bb97116f643d3d33d876716d310d22f5503a3da26ea9b7`  
		Last Modified: Wed, 11 Dec 2019 22:16:36 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c42e1c859ba7517dd5841212efeb6beea3283f7a96bb877b0b2e819ee042cd2d`  
		Last Modified: Wed, 11 Dec 2019 22:19:44 GMT  
		Size: 75.8 MB (75750243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adoptopenjdk:11-jre-hotspot-windowsservercore` - windows version 10.0.17134.1184; amd64

```console
$ docker pull adoptopenjdk@sha256:79bdda5db0380e87a71d0297f4446f7b9a5182b21c1d0304c04888521d16f713
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2432614769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f704b9c8261a51d1fdcb0808370bf194ca8880eb144ebe98f261cd659df450b8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 12 Apr 2018 09:20:54 GMT
RUN Apply image 1803-RTM-amd64
# Wed, 04 Dec 2019 15:21:18 GMT
RUN Install update 1803-amd64
# Wed, 11 Dec 2019 20:25:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2019 20:40:29 GMT
ENV JAVA_VERSION=jdk-11.0.5+10
# Wed, 11 Dec 2019 20:49:19 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.5%2B10/OpenJDK11U-jre_x64_windows_hotspot_11.0.5_10.msi ...');         [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;         wget https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.5%2B10/OpenJDK11U-jre_x64_windows_hotspot_11.0.5_10.msi -O 'openjdk.msi';         Write-Host ('Verifying sha256 (3d06a2bde2bf9cad88bf151aa789528a87353a18c26f17cf259fa86439c9c417) ...');         if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '3d06a2bde2bf9cad88bf151aa789528a87353a18c26f17cf259fa86439c9c417') {                 Write-Host 'FAILED!';                 exit 1;         };                 New-Item -ItemType Directory -Path C:\temp | Out-Null;                 Write-Host 'Installing using MSI ...';         Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',         '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;         Write-Host 'Removing openjdk.msi ...';         Remove-Item openjdk.msi -Force;         Remove-Item -Path C:\temp -Recurse | Out-Null;
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
	-	`sha256:8910e7a0ae7cd57d5a29fc540a4121f7d98a0c670b11c2f9fca893ab1a6d1ed7`  
		Last Modified: Wed, 11 Dec 2019 22:17:46 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56b25d0d0df0fd417e5a1e02d9059df1d96bd661e0168a1ef135498364d68179`  
		Last Modified: Wed, 11 Dec 2019 22:20:21 GMT  
		Size: 76.1 MB (76050605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
