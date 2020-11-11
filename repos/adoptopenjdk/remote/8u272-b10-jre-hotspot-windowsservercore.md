## `adoptopenjdk:8u272-b10-jre-hotspot-windowsservercore`

```console
$ docker pull adoptopenjdk@sha256:f06480dde07ff036012989b63ec97272673b2899ea48bd280a0cf9dc7fd4f32a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1577; amd64
	-	windows version 10.0.14393.4046; amd64

### `adoptopenjdk:8u272-b10-jre-hotspot-windowsservercore` - windows version 10.0.17763.1577; amd64

```console
$ docker pull adoptopenjdk@sha256:b03afcba9457c9f40bb17c0726d855f96d08de780f9aadfd2acb8cc48248c13e
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2471398540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec8170ee009aa8ce2a1ba426124a20ac6e3e9528984a565327c8b1b450f5d8b4`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 03 Nov 2020 03:11:34 GMT
RUN Install update 1809-amd64
# Wed, 11 Nov 2020 13:26:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Nov 2020 18:44:50 GMT
ENV JAVA_VERSION=jdk8u272-b10
# Wed, 11 Nov 2020 18:50:41 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u272-b10/OpenJDK8U-jre_x64_windows_hotspot_8u272b10.msi ...');     [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     wget https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u272-b10/OpenJDK8U-jre_x64_windows_hotspot_8u272b10.msi -O 'openjdk.msi';     Write-Host ('Verifying sha256 (0352a5764514a9fa375d9ec9a487f7e0e1352e1b33988994f6393405a8506974) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '0352a5764514a9fa375d9ec9a487f7e0e1352e1b33988994f6393405a8506974') {             Write-Host 'FAILED!';             exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;     Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
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
	-	`sha256:ef73a4345aed026e9c6a9dc0f40dd69bb0a5f30efa5e4198da6acf16d477fa49`  
		Last Modified: Wed, 11 Nov 2020 20:03:36 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb080197ee9a911ac6081b043945f6ac81a3e64fbf45fa6570f5930b85c53023`  
		Last Modified: Wed, 11 Nov 2020 20:04:52 GMT  
		Size: 83.4 MB (83366975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adoptopenjdk:8u272-b10-jre-hotspot-windowsservercore` - windows version 10.0.14393.4046; amd64

```console
$ docker pull adoptopenjdk@sha256:a89298f0af56a0cb52c00e6320a68303bc42bce9fd17b8d92950e259091d3630
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5854716495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40df4535d0db286f2d696328b19b11bb7fc0c54511158e37b9f9e15f6d044ddf`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 28 Oct 2020 18:03:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Nov 2020 13:23:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Nov 2020 18:46:46 GMT
ENV JAVA_VERSION=jdk8u272-b10
# Wed, 11 Nov 2020 18:52:45 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u272-b10/OpenJDK8U-jre_x64_windows_hotspot_8u272b10.msi ...');     [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     wget https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u272-b10/OpenJDK8U-jre_x64_windows_hotspot_8u272b10.msi -O 'openjdk.msi';     Write-Host ('Verifying sha256 (0352a5764514a9fa375d9ec9a487f7e0e1352e1b33988994f6393405a8506974) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '0352a5764514a9fa375d9ec9a487f7e0e1352e1b33988994f6393405a8506974') {             Write-Host 'FAILED!';             exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;     Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
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
	-	`sha256:52009880b4428eefa285cb6348f5de2b3f83b2b00022d397f700306e449a800d`  
		Last Modified: Wed, 11 Nov 2020 20:04:10 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7169aa3627492204b96bb7e766b90eb9ccf96b372837ab3b79735c067158d28d`  
		Last Modified: Wed, 11 Nov 2020 20:05:16 GMT  
		Size: 84.2 MB (84155395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
