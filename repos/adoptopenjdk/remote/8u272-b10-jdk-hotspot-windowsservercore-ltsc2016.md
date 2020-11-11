## `adoptopenjdk:8u272-b10-jdk-hotspot-windowsservercore-ltsc2016`

```console
$ docker pull adoptopenjdk@sha256:cf798dbdcc4546b9b1e02e9e91c45c9186c9e66fb58d7e35d50c20b000ad065c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4046; amd64

### `adoptopenjdk:8u272-b10-jdk-hotspot-windowsservercore-ltsc2016` - windows version 10.0.14393.4046; amd64

```console
$ docker pull adoptopenjdk@sha256:56290fac4242fdc444beffd768a5843ef1bf071940fac7c41881254b66ceb526
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 GB (5973051899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c2f5cd4aae109e97d80a8eb34ab8d95842eb64ee748a7a0ec7a51097463e1cf`
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
# Wed, 11 Nov 2020 18:49:09 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u272-b10/OpenJDK8U-jdk_x64_windows_hotspot_8u272b10.msi ...');     [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     wget https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u272-b10/OpenJDK8U-jdk_x64_windows_hotspot_8u272b10.msi -O 'openjdk.msi';     Write-Host ('Verifying sha256 (71b6ca8f866bf604e6d4fbe29884bbfd815ffcf1dd2dbbc82c8f33b9c0485c9d) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '71b6ca8f866bf604e6d4fbe29884bbfd815ffcf1dd2dbbc82c8f33b9c0485c9d') {             Write-Host 'FAILED!';             exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;     Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
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
	-	`sha256:d25d62c7a29632659ee8dbf3b74d944de63bdebde90f1644c1633a8583e0f9bb`  
		Last Modified: Wed, 11 Nov 2020 20:04:28 GMT  
		Size: 202.5 MB (202490799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
