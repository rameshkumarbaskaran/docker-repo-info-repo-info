## `eclipse-temurin:11-jre-windowsservercore-1809`

```console
$ docker pull eclipse-temurin@sha256:780a19c794089b397aa3a30025a9508987dd347cd389f89f32464f039a0b320b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3406; amd64

### `eclipse-temurin:11-jre-windowsservercore-1809` - windows version 10.0.17763.3406; amd64

```console
$ docker pull eclipse-temurin@sha256:24472a99124dbce833a61513fde67a3cc7e05c9a5b114b76b27f53938d884503
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2777860428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:455c73a0d55ad002eb1a348e83280ac9fe739986241aeb019896eb58e218a52c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Fri, 09 Sep 2022 22:43:02 GMT
RUN Install update 10.0.17763.3406
# Tue, 13 Sep 2022 18:21:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Sep 2022 16:09:22 GMT
ENV JAVA_VERSION=jdk-11.0.16.1+1
# Wed, 14 Sep 2022 16:15:24 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_x64_windows_hotspot_11.0.16.1_1.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_x64_windows_hotspot_11.0.16.1_1.msi ;     Write-Host ('Verifying sha256 (2e69a0b9b90fbf95dc28878dce5657be9aa7cfec5a475e696553d3f84c18b2c0) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '2e69a0b9b90fbf95dc28878dce5657be9aa7cfec5a475e696553d3f84c18b2c0') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 14 Sep 2022 16:16:22 GMT
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
	-	`sha256:0412e481dacd6ab88366d32cd6dfa3f4dd29c9287ccd8283db8c08e7d82dc8c2`  
		Last Modified: Wed, 14 Sep 2022 16:49:07 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e8d8b0fd1bcdd919bee18ab2d1c11aa8db9448ab6e46bbe985850aac71ffac`  
		Last Modified: Wed, 14 Sep 2022 16:50:51 GMT  
		Size: 74.0 MB (73974164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01d18d67a0e4bc8e0451799bdc374ce391e6fa747dd36d9dfd573cf94fc056c4`  
		Last Modified: Wed, 14 Sep 2022 16:50:40 GMT  
		Size: 318.7 KB (318714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
