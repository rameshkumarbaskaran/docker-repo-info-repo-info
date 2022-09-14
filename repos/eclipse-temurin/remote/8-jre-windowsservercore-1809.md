## `eclipse-temurin:8-jre-windowsservercore-1809`

```console
$ docker pull eclipse-temurin@sha256:886278fe1c17a06e1721dc1804e3241d9df27206d50da346caaa20ea01651a4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3406; amd64

### `eclipse-temurin:8-jre-windowsservercore-1809` - windows version 10.0.17763.3406; amd64

```console
$ docker pull eclipse-temurin@sha256:5c56eab2ef5153cf767be716c892bcfd394097506639a1e61f5b1adae3d9c99b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2774869446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d520f4e1aa2d3bbc2cc6cf90e44f020109c29d390a201262bb0c820a939c29c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Fri, 09 Sep 2022 22:43:02 GMT
RUN Install update 10.0.17763.3406
# Tue, 13 Sep 2022 18:21:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Sep 2022 16:00:03 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Wed, 14 Sep 2022 16:06:18 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_x64_windows_hotspot_8u345b01.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_x64_windows_hotspot_8u345b01.msi ;     Write-Host ('Verifying sha256 (30253824132f22de22fef11242fc9cd7a183b5e09757bb57ad1d82c03d852a3c) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '30253824132f22de22fef11242fc9cd7a183b5e09757bb57ad1d82c03d852a3c') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 14 Sep 2022 16:07:21 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:cee64bf279e2ca8e924884a10ecb98bfa79c7f0cc8d25e73039b9aeb940815b6`  
		Size: 826.4 MB (826398623 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2bc395c8c47e61e593d2e905e0e051d40e7d25e4aeac7dbe08d3ec57acd0e68f`  
		Last Modified: Tue, 13 Sep 2022 18:25:24 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eb60d65564d0ac5040e222e0d050e314bd45ead06a1c32f2bcdc11434c03e57`  
		Last Modified: Wed, 14 Sep 2022 16:46:40 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc66993d08153a3e6120a271d2a9b5517ec0e0b3e27fc9dfb97e443d72920aa5`  
		Last Modified: Wed, 14 Sep 2022 16:48:00 GMT  
		Size: 71.0 MB (70982708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c343e6bb391016034f59961d4bb1db0a2deacbd3b6aaaac30beab12530258fb`  
		Last Modified: Wed, 14 Sep 2022 16:47:51 GMT  
		Size: 319.2 KB (319174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
