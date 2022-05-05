## `eclipse-temurin:8u332-b09-jre-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:20c8ee177adee5401e7a5d8a0298b689deb9fa4d2935c33ee670b60ff6057fb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.643; amd64

### `eclipse-temurin:8u332-b09-jre-windowsservercore-ltsc2022` - windows version 10.0.20348.643; amd64

```console
$ docker pull eclipse-temurin@sha256:9e83bdfa9d680543e8cc2fec8eee8d5adcb64936cc31dc2272efa23e3ce632d1
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2298478514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e962c21c9127c83ddee1518e7fff3ad756a7eaeab2386c98d7a3af168a5f5dd1`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Sun, 03 Apr 2022 05:50:25 GMT
RUN Install update ltsc2022-amd64
# Wed, 13 Apr 2022 02:27:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 05 May 2022 18:16:10 GMT
ENV JAVA_VERSION=jdk8u332-b09
# Thu, 05 May 2022 18:23:17 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_x64_windows_hotspot_8u332b09.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_x64_windows_hotspot_8u332b09.msi ;     Write-Host ('Verifying sha256 (c724d3ba94f24f6ecddc6dc7367acaa4ca5b0eda828627302b8e8589dddf66c8) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'c724d3ba94f24f6ecddc6dc7367acaa4ca5b0eda828627302b8e8589dddf66c8') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 05 May 2022 18:23:43 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:dccd9e4d14d3d5a6e93f87350b903e117368ada32d711986f779b5a3ef8657cc`  
		Size: 975.3 MB (975255801 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1ab01d498c34190a1e49e15239442a41312c6ea5904e18f186f84f90f11fc422`  
		Last Modified: Wed, 13 Apr 2022 03:13:51 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f8c57151eb30020e9959c4cb9b41666c020982d1e607217114a03c25ecd432`  
		Last Modified: Thu, 05 May 2022 21:20:22 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1dc96b678df9d6f2db74f1242e02137bca23323a4ce854e460b139aef274205`  
		Last Modified: Thu, 05 May 2022 21:23:16 GMT  
		Size: 70.9 MB (70943976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b12cfef26fdd788960bd75bff6987ba5336bbe19d55ef07395aa9a0a06b5d587`  
		Last Modified: Thu, 05 May 2022 21:21:58 GMT  
		Size: 576.8 KB (576837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
