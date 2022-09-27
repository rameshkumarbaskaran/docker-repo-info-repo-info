## `eclipse-temurin:19_36-jre-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:8afd72169e8b2a75e904fa3cbcaa3e146c4b94382a21b038e3b5bb9d0bcc4146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1006; amd64
	-	windows version 10.0.17763.3406; amd64

### `eclipse-temurin:19_36-jre-windowsservercore` - windows version 10.0.20348.1006; amd64

```console
$ docker pull eclipse-temurin@sha256:34e097aff1ed981c84ba601cc3bb5130325422541567ec7688879329339b7387
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2425290722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4619956b0d3aa93854467698496e563286217e80a6a89403167e16dadadca4e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Thu, 08 Sep 2022 20:30:55 GMT
RUN Install update 10.0.20348.1006
# Wed, 14 Sep 2022 12:09:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 26 Sep 2022 23:16:50 GMT
ENV JAVA_VERSION=jdk-19+36
# Mon, 26 Sep 2022 23:24:01 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jre_x64_windows_hotspot_19_36.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jre_x64_windows_hotspot_19_36.msi ;     Write-Host ('Verifying sha256 (2fe3e0989b31551b65cd3d276f8435618aad7f4e3f2996a58c3b51f0de4ccf35) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '2fe3e0989b31551b65cd3d276f8435618aad7f4e3f2996a58c3b51f0de4ccf35') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-19' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Mon, 26 Sep 2022 23:24:22 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
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
	-	`sha256:b8752d5de0350b986ee99ca812024507c97656ab4071b82da530723ad4463415`  
		Last Modified: Mon, 26 Sep 2022 23:32:15 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:808efdf17f10ae8436de7e155c541411ecfd56505737dc70b205c7d087466509`  
		Last Modified: Mon, 26 Sep 2022 23:34:27 GMT  
		Size: 77.8 MB (77786662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:581b99a64f17d157730eea70d3cb7532be9c9d9b889532a467e1d568ce16c58a`  
		Last Modified: Mon, 26 Sep 2022 23:34:17 GMT  
		Size: 551.6 KB (551633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:19_36-jre-windowsservercore` - windows version 10.0.17763.3406; amd64

```console
$ docker pull eclipse-temurin@sha256:efeae336d08133be6f49c7fa84bc6929ff585664c9fd4058454433487f9fd076
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2784481382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f99610a7407c7c2196fb50d1777b2f3925af915a1d9c72b5d70430c611afa1c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Fri, 09 Sep 2022 22:43:02 GMT
RUN Install update 10.0.17763.3406
# Tue, 13 Sep 2022 18:21:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 26 Sep 2022 23:19:02 GMT
ENV JAVA_VERSION=jdk-19+36
# Mon, 26 Sep 2022 23:26:05 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jre_x64_windows_hotspot_19_36.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jre_x64_windows_hotspot_19_36.msi ;     Write-Host ('Verifying sha256 (2fe3e0989b31551b65cd3d276f8435618aad7f4e3f2996a58c3b51f0de4ccf35) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '2fe3e0989b31551b65cd3d276f8435618aad7f4e3f2996a58c3b51f0de4ccf35') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-19' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Mon, 26 Sep 2022 23:27:12 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
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
	-	`sha256:150d8a9324d7a4243398747bdc5cb7e68b57a6372fa9bce00aa78cee0f2c70a7`  
		Last Modified: Mon, 26 Sep 2022 23:33:01 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f17b1c79f0430edacbaa87a2af4e49a327be6b1966ffed46ed22c9642296fa4`  
		Last Modified: Mon, 26 Sep 2022 23:34:47 GMT  
		Size: 77.6 MB (77578266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9fbe26a9b9629d55d002f0dfdbc1b86fb7c841ded0f7ca3fb67f1dfb60a741b`  
		Last Modified: Mon, 26 Sep 2022 23:34:37 GMT  
		Size: 3.3 MB (3335598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
