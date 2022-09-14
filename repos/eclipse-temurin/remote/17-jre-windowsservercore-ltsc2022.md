## `eclipse-temurin:17-jre-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:7a14c4cbe508e3b645c2553d6dbebd5c26460317cfc1cdb5601ebf4d530b107f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1006; amd64

### `eclipse-temurin:17-jre-windowsservercore-ltsc2022` - windows version 10.0.20348.1006; amd64

```console
$ docker pull eclipse-temurin@sha256:d90bb0caf2e94962200dc42662b72b1ee8f1b5899fef18300c4853ab770ba0f7
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2422168450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ca0e80023cf462af1d942e0f02805837dc2a9397fca243cae0ae92120f14b87`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Thu, 08 Sep 2022 20:30:55 GMT
RUN Install update 10.0.20348.1006
# Wed, 14 Sep 2022 12:09:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Sep 2022 16:17:03 GMT
ENV JAVA_VERSION=jdk-17.0.4.1+1
# Wed, 14 Sep 2022 16:22:58 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jre_x64_windows_hotspot_17.0.4.1_1.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jre_x64_windows_hotspot_17.0.4.1_1.msi ;     Write-Host ('Verifying sha256 (f9b8c41b3cf1cf3bf4d0ad8eee1d2e49678696afad4e595ad023668cbab8b664) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'f9b8c41b3cf1cf3bf4d0ad8eee1d2e49678696afad4e595ad023668cbab8b664') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-17' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 14 Sep 2022 16:23:18 GMT
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
	-	`sha256:31e7a87ae7360db7cb4dd9d22f1aba9b0877b8d927223283282ef075702a3bef`  
		Last Modified: Wed, 14 Sep 2022 16:51:19 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83f570ea80b2ac46211b120f7082fcfe1d62ace0f67e49f241c36b1abae26b89`  
		Last Modified: Wed, 14 Sep 2022 16:53:37 GMT  
		Size: 74.7 MB (74677419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a82ff587a3e0569f58621f4a18664dd1194e304f8ea3b84772b3b7c7414c5164`  
		Last Modified: Wed, 14 Sep 2022 16:53:24 GMT  
		Size: 538.7 KB (538726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
