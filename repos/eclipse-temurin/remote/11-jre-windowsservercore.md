## `eclipse-temurin:11-jre-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:5376507e7ff008531e74f201311d74b4256a2d32900a36a4f370ffe6b456e4ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1129; amd64
	-	windows version 10.0.17763.3532; amd64

### `eclipse-temurin:11-jre-windowsservercore` - windows version 10.0.20348.1129; amd64

```console
$ docker pull eclipse-temurin@sha256:7bc8819203b684d50ea80547c35922a1fc9cfe440ba588ee6fba57217812ad3e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2548749441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83eddc93f32afc1d7e9021613508f36a01cba28ff5cdaeddad11b7df8ee0873b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Fri, 07 Oct 2022 22:13:48 GMT
RUN Install update 10.0.20348.1129
# Tue, 11 Oct 2022 20:20:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 04 Nov 2022 23:26:21 GMT
ENV JAVA_VERSION=jdk-11.0.17+8
# Fri, 04 Nov 2022 23:33:35 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_x64_windows_hotspot_11.0.17_8.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_x64_windows_hotspot_11.0.17_8.msi ;     Write-Host ('Verifying sha256 (25153859aec9104b91f34207d4d6f6e7ceb21d78bebf4c6a3409fb850fd203f8) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '25153859aec9104b91f34207d4d6f6e7ceb21d78bebf4c6a3409fb850fd203f8') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Fri, 04 Nov 2022 23:33:58 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
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
	-	`sha256:7db28e0cc457cf52d9f27e3543616589c24204640facf15d6fc8e3a671cd6d71`  
		Last Modified: Sat, 05 Nov 2022 00:23:14 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91bfd88d40c62e2f7dd06356ad62609c0c6bd01189f7ada1c649ce13496b7040`  
		Last Modified: Sat, 05 Nov 2022 00:25:38 GMT  
		Size: 74.2 MB (74168839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da1a59da1cfc3bfa3e8c8d89771891c707a8e70019e133b0914d91cbd19fd6df`  
		Last Modified: Sat, 05 Nov 2022 00:25:24 GMT  
		Size: 551.6 KB (551600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jre-windowsservercore` - windows version 10.0.17763.3532; amd64

```console
$ docker pull eclipse-temurin@sha256:cf2f5fc9055d35cc520165fc2b383b01e0970c5046dd01222740f405e6e9f279
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2847775088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dafaf228e2c18ea23a1385b6abf487257a1686c3f8850d09559bc0b0d708fd6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 08 Oct 2022 01:55:32 GMT
RUN Install update 10.0.17763.3532
# Tue, 11 Oct 2022 20:24:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 04 Nov 2022 23:28:37 GMT
ENV JAVA_VERSION=jdk-11.0.17+8
# Fri, 04 Nov 2022 23:35:40 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_x64_windows_hotspot_11.0.17_8.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_x64_windows_hotspot_11.0.17_8.msi ;     Write-Host ('Verifying sha256 (25153859aec9104b91f34207d4d6f6e7ceb21d78bebf4c6a3409fb850fd203f8) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '25153859aec9104b91f34207d4d6f6e7ceb21d78bebf4c6a3409fb850fd203f8') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Fri, 04 Nov 2022 23:36:55 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:a48a3e4ae2de839d8e99bde16eb91d113fb2cf889bba472d0c4274851b5fb402`  
		Last Modified: Tue, 21 Jun 2022 18:30:17 GMT  
		Size: 1.9 GB (1924269350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6193ab94a0498ba6454e2a35e189837b37a2eb01403e8b62654bdc28a4569c`  
		Last Modified: Mon, 17 Oct 2022 21:52:22 GMT  
		Size: 849.2 MB (849228999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c70f9828a2aec7ea0624298c8cc6f0bcb5f21b439f4e96304b8b47c8bf15ef8d`  
		Last Modified: Tue, 11 Oct 2022 20:35:04 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beb4fff7a5cc48f7e12070441abebddf92469e7c9da8921a239065ac03201a76`  
		Last Modified: Sat, 05 Nov 2022 00:24:05 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed9f1148ca23b1e28ec1c35c493613367126524acd3113a2288d5561fc1d191c`  
		Last Modified: Sat, 05 Nov 2022 00:26:04 GMT  
		Size: 73.9 MB (73938049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:700d7b8aba43daa98df2b9489c725e5ab577724073751950335248c104345f9a`  
		Last Modified: Sat, 05 Nov 2022 00:25:50 GMT  
		Size: 335.8 KB (335848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
