## `eclipse-temurin:8u352-b08-jdk-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:408792b8dfe8e9ed3fb0f66de7db36b0cce4bc894c1f34cf99b468f5363ea9d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1129; amd64

### `eclipse-temurin:8u352-b08-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.1129; amd64

```console
$ docker pull eclipse-temurin@sha256:cfa646541d2b673dc3b9e25b17b854d62544226cb383fdb466235146407df292
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2664324567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdfe0998373fffdf2245ed659e60217d4c2ab7616be3b556ed5b3ae56fe80670`
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
# Fri, 04 Nov 2022 23:16:35 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_x64_windows_hotspot_8u352b08.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_x64_windows_hotspot_8u352b08.msi ;     Write-Host ('Verifying sha256 (c3f2ee62970bae81aa163e155faab8498638962a0a480aa01620d3122ad902ee) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'c3f2ee62970bae81aa163e155faab8498638962a0a480aa01620d3122ad902ee') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Fri, 04 Nov 2022 23:17:05 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac -version'; javac -version;     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
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
	-	`sha256:f7379d5aa4590fa96cccde051446c588110784f4dcaf90914e8d119c3fc5a22d`  
		Last Modified: Sat, 05 Nov 2022 00:21:02 GMT  
		Size: 189.7 MB (189744999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e528e03d98963fb7505b55682340696a39f85f365e0cfc2c4ac15ca8424309`  
		Last Modified: Sat, 05 Nov 2022 00:20:44 GMT  
		Size: 550.5 KB (550482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
