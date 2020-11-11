## `adoptopenjdk:11-jdk-hotspot-windowsservercore`

```console
$ docker pull adoptopenjdk@sha256:0430d38c47fcb5a535948a3b13f0e89e15f452ab986a993d04610a1d968220f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1577; amd64
	-	windows version 10.0.14393.4046; amd64

### `adoptopenjdk:11-jdk-hotspot-windowsservercore` - windows version 10.0.17763.1577; amd64

```console
$ docker pull adoptopenjdk@sha256:d0b106e7aa98798032f03d42c13dd5a510854492713dd0cd87952738c163c1e0
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2760367239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:197cf84766456a5f5910e274f72a701460bab56d60134cbbcc73a8c5e9abe55d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 03 Nov 2020 03:11:34 GMT
RUN Install update 1809-amd64
# Wed, 11 Nov 2020 13:26:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Nov 2020 18:53:04 GMT
ENV JAVA_VERSION=jdk-11.0.9+11
# Wed, 11 Nov 2020 18:55:29 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.9%2B11.1/OpenJDK11U-jdk_x64_windows_hotspot_11.0.9_11.msi ...');     [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     wget https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.9%2B11.1/OpenJDK11U-jdk_x64_windows_hotspot_11.0.9_11.msi -O 'openjdk.msi';     Write-Host ('Verifying sha256 (631fcb658a7431d8f01f9c10e1eaf0e8c74ae609fa1aa9a0cf27c2305ab3431d) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '631fcb658a7431d8f01f9c10e1eaf0e8c74ae609fa1aa9a0cf27c2305ab3431d') {             Write-Host 'FAILED!';             exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;     Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 11 Nov 2020 18:55:30 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:680bbdbacf1bcbace70de5087d02d31e9dd7a22feae59f746f54dab46c1d5bda`  
		Size: 669.7 MB (669696346 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:da5a67a9f3a363cb69c8104913a5a58c1c47e8f648a07d057fc28a5f98790e60`  
		Last Modified: Wed, 11 Nov 2020 13:37:50 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88d4fcb4aeb45ca5a2ac84c6a0bf153768eaec7e1df6ae4ae91782127283946d`  
		Last Modified: Wed, 11 Nov 2020 20:05:29 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6901bf9d04c3a4b9622d42a6f9ed70f2127cbb480b07fa7852ca0d86d6ebafc5`  
		Last Modified: Wed, 11 Nov 2020 20:06:04 GMT  
		Size: 372.3 MB (372334554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e834fcc2317a2bffd78506ecb0ddb4beef6e0ca11ec22244d8cabd196dc744bf`  
		Last Modified: Wed, 11 Nov 2020 20:05:28 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adoptopenjdk:11-jdk-hotspot-windowsservercore` - windows version 10.0.14393.4046; amd64

```console
$ docker pull adoptopenjdk@sha256:d5abb49c50ca1ddfb57016e6fbf9276466dfc46628e4846c4402501542c063d0
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 GB (6143685883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f98506c3966c934a2e66b944f5fdcfbef1dcad06ee1ab978c8e60196bb183f0`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 28 Oct 2020 18:03:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Nov 2020 13:23:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Nov 2020 18:55:46 GMT
ENV JAVA_VERSION=jdk-11.0.9+11
# Wed, 11 Nov 2020 18:58:53 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.9%2B11.1/OpenJDK11U-jdk_x64_windows_hotspot_11.0.9_11.msi ...');     [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     wget https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.9%2B11.1/OpenJDK11U-jdk_x64_windows_hotspot_11.0.9_11.msi -O 'openjdk.msi';     Write-Host ('Verifying sha256 (631fcb658a7431d8f01f9c10e1eaf0e8c74ae609fa1aa9a0cf27c2305ab3431d) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '631fcb658a7431d8f01f9c10e1eaf0e8c74ae609fa1aa9a0cf27c2305ab3431d') {             Write-Host 'FAILED!';             exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;     Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 11 Nov 2020 18:58:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4830fb08bc2df7ae80548c349b880c263ea87a7b93e13ecbc77c862b6e179558`  
		Size: 1.7 GB (1700572904 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:126d9a92c0cb7b68c56dec2dd5ba118de9dde3ec6368db734c5135fdf1528a33`  
		Last Modified: Wed, 11 Nov 2020 13:34:53 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47efa4ea66519325e506a5f51e1fcdc42b785982583e939f1c4883eb11964b2b`  
		Last Modified: Wed, 11 Nov 2020 20:06:19 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:378e1eec3bf696d5a14a5d7a32ccd1e6848b336acac223d03365fc2d81a7bb45`  
		Last Modified: Wed, 11 Nov 2020 20:06:48 GMT  
		Size: 373.1 MB (373123623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2f20dc759765519bfb52216c2762ad3aab2ecdde3783ed8be5ee0758edf599e`  
		Last Modified: Wed, 11 Nov 2020 20:06:19 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
