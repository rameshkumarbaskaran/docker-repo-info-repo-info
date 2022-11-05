## `eclipse-temurin:8u352-b08-jre-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:a0f1676406976834057c908f8a0cc30593f053c760ed84d02fa3c9e5e44fc26e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1129; amd64

### `eclipse-temurin:8u352-b08-jre-windowsservercore-ltsc2022` - windows version 10.0.20348.1129; amd64

```console
$ docker pull eclipse-temurin@sha256:28e3f5188bceea5c68c97deaff37b7e979474587bfb1b0cca52929260fb248cf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2545707626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1fe9206d318c20a742823d22f07730176c8a8d18d3b4de59c406b9f8b2925cc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Fri, 07 Oct 2022 22:13:48 GMT
RUN Install update 10.0.20348.1129
# Tue, 11 Oct 2022 20:20:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 04 Nov 2022 23:15:21 GMT
ENV JAVA_VERSION=jdk8u352-b08
# Fri, 04 Nov 2022 23:22:37 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_x64_windows_hotspot_8u352b08.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_x64_windows_hotspot_8u352b08.msi ;     Write-Host ('Verifying sha256 (27bc5324a8d684e6afa286029c64e4d90e12d4f0b947093865b6c78ac83bd6ee) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '27bc5324a8d684e6afa286029c64e4d90e12d4f0b947093865b6c78ac83bd6ee') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Fri, 04 Nov 2022 23:23:02 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:a4aee932fccc1ec8135f290aca03a7c93dcc2536fc84723813ef9b95f6fd13ea`  
		Last Modified: Wed, 18 May 2022 07:59:24 GMT  
		Size: 1.5 GB (1473997635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08e9b54b31e104f64c9eb8a65ac0af5effd645bd00a77ea297b6015d28022a74`  
		Last Modified: Mon, 17 Oct 2022 21:39:11 GMT  
		Size: 1000.0 MB (1000028645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15e15cecc9c7498ee7335091ed603347777bb2f7810e8b701327779faaae1712`  
		Last Modified: Tue, 11 Oct 2022 20:34:44 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d81b95c2ffbe5c795ce214bddc7d3e6f8e9a11b5c1380432bb647c6ce27ad745`  
		Last Modified: Sat, 05 Nov 2022 00:20:43 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be30960615735335edf078e02772cdbf38ed401d91c250c062610c5c2f85dd9c`  
		Last Modified: Sat, 05 Nov 2022 00:22:26 GMT  
		Size: 71.1 MB (71127572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb715978db9fe00c6f6735cf37e1ffd44fbe37981b96f8c32021f9075a41b644`  
		Last Modified: Sat, 05 Nov 2022 00:22:17 GMT  
		Size: 551.0 KB (550968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
