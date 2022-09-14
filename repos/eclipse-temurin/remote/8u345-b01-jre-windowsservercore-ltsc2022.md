## `eclipse-temurin:8u345-b01-jre-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:916f9c6152d0632981d9f72dce93757d65a96ac2c7a7fc96cf20c37914d14423
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1006; amd64

### `eclipse-temurin:8u345-b01-jre-windowsservercore-ltsc2022` - windows version 10.0.20348.1006; amd64

```console
$ docker pull eclipse-temurin@sha256:12e9cd27e3492efcfb43c227d5d82a6487b6e339c391f76a8179b7e5bea4ff91
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2418691772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae8effb033ce9334ab4af40246ddbe41ca9081a84be09a900a2c9e32eac4d418`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Thu, 08 Sep 2022 20:30:55 GMT
RUN Install update 10.0.20348.1006
# Wed, 14 Sep 2022 12:09:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Sep 2022 15:58:35 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Wed, 14 Sep 2022 16:04:27 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_x64_windows_hotspot_8u345b01.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_x64_windows_hotspot_8u345b01.msi ;     Write-Host ('Verifying sha256 (30253824132f22de22fef11242fc9cd7a183b5e09757bb57ad1d82c03d852a3c) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '30253824132f22de22fef11242fc9cd7a183b5e09757bb57ad1d82c03d852a3c') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 14 Sep 2022 16:04:49 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4486102fd3820ed9527fa3e7bfefa8305c2f054e65b46dffe9675755e3d8f288`  
		Size: 910.1 MB (910085953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c5da8902b0918fe9bb0d466157622ccaf8209e4becbdd188ec41ecb563c068e6`  
		Last Modified: Wed, 14 Sep 2022 12:41:36 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a01ab8db53a5453998abd5ddd4d7f2c5af26995f59fb92fd627164cc9eeaecdb`  
		Last Modified: Wed, 14 Sep 2022 16:46:10 GMT  
		Size: 1.5 KB (1454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ec1a27733c36e7da4db1b0a51e4443b48cf507dcb7d6d4993c28ac7565381bd`  
		Last Modified: Wed, 14 Sep 2022 16:47:42 GMT  
		Size: 71.2 MB (71201089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e74809aaf209907dbb472ba05f668591fc483286e2a6539cadfcd73a3c253b`  
		Last Modified: Wed, 14 Sep 2022 16:47:34 GMT  
		Size: 538.2 KB (538225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
