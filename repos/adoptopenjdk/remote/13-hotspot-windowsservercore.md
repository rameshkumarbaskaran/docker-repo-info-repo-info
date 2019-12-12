## `adoptopenjdk:13-hotspot-windowsservercore`

```console
$ docker pull adoptopenjdk@sha256:460d9d148c45406895ed80de0b663efb19e6aab6d046ef406aa0e9b13c5cde56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3384; amd64
	-	windows version 10.0.17763.914; amd64
	-	windows version 10.0.17134.1184; amd64

### `adoptopenjdk:13-hotspot-windowsservercore` - windows version 10.0.14393.3384; amd64

```console
$ docker pull adoptopenjdk@sha256:895cf89f4fe7adcb2cea7ba17c5fd7514592539124b2bad98f072ab3258112b4
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 GB (6123377446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ad9f72cc84414dca3db9d32c77449bf9c1d21321d54fc1109dc4365b0d035a4`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 27 Nov 2019 14:43:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Dec 2019 00:35:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2019 20:49:45 GMT
ENV JAVA_VERSION=jdk-13.0.1+9
# Wed, 11 Dec 2019 20:53:14 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_x64_windows_hotspot_13.0.1_9.msi ...');         [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;         wget https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_x64_windows_hotspot_13.0.1_9.msi -O 'openjdk.msi';         Write-Host ('Verifying sha256 (ccb52fac99f9d872d02fc5b82f33863138e9fbe08fef4c2e21ec8ec8c3eb2b44) ...');         if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'ccb52fac99f9d872d02fc5b82f33863138e9fbe08fef4c2e21ec8ec8c3eb2b44') {                 Write-Host 'FAILED!';                 exit 1;         };                 New-Item -ItemType Directory -Path C:\temp | Out-Null;                 Write-Host 'Installing using MSI ...';         Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',         '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;         Write-Host 'Removing openjdk.msi ...';         Remove-Item openjdk.msi -Force;         Remove-Item -Path C:\temp -Recurse | Out-Null;
# Wed, 11 Dec 2019 20:53:16 GMT
CMD ["jshell"]
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
	-	`sha256:e7713ca0ff94e9d7e89e29d2f10394c0bdc4f26f5fc4626d0f81d45f22cd1c73`  
		Last Modified: Wed, 11 Dec 2019 22:20:43 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c60b225489bae39f303a8be7472814fb7394eec02351524fd0536170d234485`  
		Last Modified: Wed, 11 Dec 2019 22:21:28 GMT  
		Size: 400.7 MB (400670040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5adbe5796db55bdedba5ff66c324938614f822ee8526e8ec02ad212c9ec86484`  
		Last Modified: Wed, 11 Dec 2019 22:20:43 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adoptopenjdk:13-hotspot-windowsservercore` - windows version 10.0.17763.914; amd64

```console
$ docker pull adoptopenjdk@sha256:cb445410bceea93623e17013816a647a0c10abc4df3ec1d326e1b53f2ed8e560
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2611776758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:355ecab2a1ad82236a114b241b8ce8e0c6802ba745b3b35d93ed6acd3e0d837a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 29 Nov 2019 04:34:15 GMT
RUN Install update 1809-amd64
# Tue, 10 Dec 2019 21:34:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2019 20:53:35 GMT
ENV JAVA_VERSION=jdk-13.0.1+9
# Wed, 11 Dec 2019 20:56:27 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_x64_windows_hotspot_13.0.1_9.msi ...');         [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;         wget https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_x64_windows_hotspot_13.0.1_9.msi -O 'openjdk.msi';         Write-Host ('Verifying sha256 (ccb52fac99f9d872d02fc5b82f33863138e9fbe08fef4c2e21ec8ec8c3eb2b44) ...');         if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'ccb52fac99f9d872d02fc5b82f33863138e9fbe08fef4c2e21ec8ec8c3eb2b44') {                 Write-Host 'FAILED!';                 exit 1;         };                 New-Item -ItemType Directory -Path C:\temp | Out-Null;                 Write-Host 'Installing using MSI ...';         Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',         '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;         Write-Host 'Removing openjdk.msi ...';         Remove-Item openjdk.msi -Force;         Remove-Item -Path C:\temp -Recurse | Out-Null;
# Wed, 11 Dec 2019 20:56:29 GMT
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
	-	`sha256:3aadf355f3e249b7fd4b7f036269d9763cc3273bf6dd7477afea1338cf815725`  
		Last Modified: Wed, 11 Dec 2019 22:22:06 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56b3bea8fe51ca71f8ed6db5168c39e63c5dfcbc8d1eb7d92f7743bf7bb83330`  
		Last Modified: Wed, 11 Dec 2019 22:22:58 GMT  
		Size: 395.5 MB (395469810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cd74cfa57705332d030a10df2748e91c1d16b473d6ca9dcdf0a10c4ead5cfaa`  
		Last Modified: Wed, 11 Dec 2019 22:22:05 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adoptopenjdk:13-hotspot-windowsservercore` - windows version 10.0.17134.1184; amd64

```console
$ docker pull adoptopenjdk@sha256:49a62202343581e3f259b4d27cff50d85e2616869da1cc2415c3b33903600374
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2752334259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb3990140ace5a98054a997be377f25d3aeb46d412f6d6a459dd8a07b9169427`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 12 Apr 2018 09:20:54 GMT
RUN Apply image 1803-RTM-amd64
# Wed, 04 Dec 2019 15:21:18 GMT
RUN Install update 1803-amd64
# Wed, 11 Dec 2019 20:25:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2019 20:56:54 GMT
ENV JAVA_VERSION=jdk-13.0.1+9
# Wed, 11 Dec 2019 21:00:04 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_x64_windows_hotspot_13.0.1_9.msi ...');         [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;         wget https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_x64_windows_hotspot_13.0.1_9.msi -O 'openjdk.msi';         Write-Host ('Verifying sha256 (ccb52fac99f9d872d02fc5b82f33863138e9fbe08fef4c2e21ec8ec8c3eb2b44) ...');         if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'ccb52fac99f9d872d02fc5b82f33863138e9fbe08fef4c2e21ec8ec8c3eb2b44') {                 Write-Host 'FAILED!';                 exit 1;         };                 New-Item -ItemType Directory -Path C:\temp | Out-Null;                 Write-Host 'Installing using MSI ...';         Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',         '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;         Write-Host 'Removing openjdk.msi ...';         Remove-Item openjdk.msi -Force;         Remove-Item -Path C:\temp -Recurse | Out-Null;
# Wed, 11 Dec 2019 21:00:05 GMT
CMD ["jshell"]
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
	-	`sha256:557616f300af2276f1eaca5d8ef5ad6b386a31622f1629b52a790256f52cd956`  
		Last Modified: Wed, 11 Dec 2019 22:23:38 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:017cac186c823a2fee16bc426c1e78c81fed2a333bd5d889ae71dcd0a48b5313`  
		Last Modified: Wed, 11 Dec 2019 22:24:36 GMT  
		Size: 395.8 MB (395768897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fc13508ff23fc0220c71b3a06ec4b6d914cf93a43f42521b327ac4908cd0e53`  
		Last Modified: Wed, 11 Dec 2019 22:23:37 GMT  
		Size: 1.2 KB (1201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
