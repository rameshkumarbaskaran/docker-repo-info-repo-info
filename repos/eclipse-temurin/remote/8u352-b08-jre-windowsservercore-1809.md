## `eclipse-temurin:8u352-b08-jre-windowsservercore-1809`

```console
$ docker pull eclipse-temurin@sha256:9342ee21c82b56e6d78b04c6b90e53ae5b42576af6e313761213bba20c4e12ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3532; amd64

### `eclipse-temurin:8u352-b08-jre-windowsservercore-1809` - windows version 10.0.17763.3532; amd64

```console
$ docker pull eclipse-temurin@sha256:f05056004ec89fe085d222f86f1c694d895db2fb2695d8ca6dd6cc7c6912bd78
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2844731311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:893cdfe074b842a5d9f90599d029c9646a6f0297f5615c9f2b0c3e9c04fc10c5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 08 Oct 2022 01:55:32 GMT
RUN Install update 10.0.17763.3532
# Tue, 11 Oct 2022 20:24:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 04 Nov 2022 23:17:23 GMT
ENV JAVA_VERSION=jdk8u352-b08
# Fri, 04 Nov 2022 23:24:28 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_x64_windows_hotspot_8u352b08.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_x64_windows_hotspot_8u352b08.msi ;     Write-Host ('Verifying sha256 (27bc5324a8d684e6afa286029c64e4d90e12d4f0b947093865b6c78ac83bd6ee) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '27bc5324a8d684e6afa286029c64e4d90e12d4f0b947093865b6c78ac83bd6ee') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Fri, 04 Nov 2022 23:25:38 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
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
	-	`sha256:542e9ed642e031882fd5750fac94359d6043aa15f690370244314639fec89897`  
		Last Modified: Sat, 05 Nov 2022 00:21:18 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:548ee9675649e858674c7357a8416fcbd814d7cb128448068c9173ee4bdca9ec`  
		Last Modified: Sat, 05 Nov 2022 00:22:46 GMT  
		Size: 70.9 MB (70897078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eae0c38f26fcfc19641c69575afc6a1e26324804a39dc968097cdd572eaeb4b`  
		Last Modified: Sat, 05 Nov 2022 00:22:38 GMT  
		Size: 333.0 KB (333046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
