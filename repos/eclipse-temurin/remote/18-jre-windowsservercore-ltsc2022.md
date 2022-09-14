## `eclipse-temurin:18-jre-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:8680b5ba02a4f6947edc0d5267aac4b82d6f799e0128fc43b583d35ff9145b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1006; amd64

### `eclipse-temurin:18-jre-windowsservercore-ltsc2022` - windows version 10.0.20348.1006; amd64

```console
$ docker pull eclipse-temurin@sha256:89081094738c37d46deab5cb9c0b7312aefaf9dd3b6357893a1bc6c58e38322a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2422019687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beb5602ecde02d6b3527e295bfee39d41b61eb4b1e3f57254f8d553181f73581`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Thu, 08 Sep 2022 20:30:55 GMT
RUN Install update 10.0.20348.1006
# Wed, 14 Sep 2022 12:09:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Sep 2022 16:26:32 GMT
ENV JAVA_VERSION=jdk-18.0.2.1+1
# Wed, 14 Sep 2022 16:34:34 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2.1%2B1/OpenJDK18U-jre_x64_windows_hotspot_18.0.2.1_1.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2.1%2B1/OpenJDK18U-jre_x64_windows_hotspot_18.0.2.1_1.msi ;     Write-Host ('Verifying sha256 (1e726c0ea2a8b25c2c75a8174df173dd54c98caa0235ef49d84a03292f152bfc) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '1e726c0ea2a8b25c2c75a8174df173dd54c98caa0235ef49d84a03292f152bfc') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-18' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 14 Sep 2022 16:34:55 GMT
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
	-	`sha256:26d5b521ee82dff3a1edca26df6b02fa9c803362e173a6a27332ce7aaf59c045`  
		Last Modified: Wed, 14 Sep 2022 16:54:24 GMT  
		Size: 1.4 KB (1355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9e5a9351e38dde5dee2f9ecdaee608d42b5713d9e857333aa27c5d88cccb4be`  
		Last Modified: Wed, 14 Sep 2022 16:56:36 GMT  
		Size: 74.5 MB (74530081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e08f57849c29d61c77e4a6a31758e9b0639c09985809c73b4d7cf7b7d77502c3`  
		Last Modified: Wed, 14 Sep 2022 16:56:26 GMT  
		Size: 537.2 KB (537247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
