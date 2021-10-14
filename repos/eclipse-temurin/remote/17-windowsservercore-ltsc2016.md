## `eclipse-temurin:17-windowsservercore-ltsc2016`

```console
$ docker pull eclipse-temurin@sha256:20b7cc5202748ec509cd3864ba57f7489396c5588462f50f4776c684781ef3c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.14393.4704; amd64

### `eclipse-temurin:17-windowsservercore-ltsc2016` - windows version 10.0.14393.4704; amd64

```console
$ docker pull eclipse-temurin@sha256:654348399c835448e518b2a72549e21b9cd14b1f90dce38256eac2c01e3aba75
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 GB (6628750966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e3e9701ab96f013ecb442d9a468155090e3dc26ee9f48a28fdda0f5ee248bc4`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 06 Oct 2021 21:16:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 13 Oct 2021 12:40:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Oct 2021 18:59:02 GMT
ENV JAVA_VERSION=jdk-17+35
# Wed, 13 Oct 2021 19:00:56 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17%2B35/OpenJDK17-jdk_x64_windows_hotspot_17_35.msi ...');     [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12 ; Invoke-WebRequest -Uri https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17%2B35/OpenJDK17-jdk_x64_windows_hotspot_17_35.msi -O 'openjdk.msi' ;     Write-Host ('Verifying sha256 (4a0350a9e3e0cf3bba9a57890bb0b223b7c47883169730f122100fc31d61d486) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '4a0350a9e3e0cf3bba9a57890bb0b223b7c47883169730f122100fc31d61d486') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-17' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 13 Oct 2021 19:02:11 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 13 Oct 2021 19:02:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0c776a8e8e3c02d360995b7fa26a3fd7c0928965795fac57b69ff07418ab07bf`  
		Size: 2.2 GB (2202780626 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6974b1bd85ba3f9ce16d86231eced43f720fed9c13411d37584dfe7193bcde60`  
		Last Modified: Wed, 13 Oct 2021 13:27:57 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:507b50cb230e4739993a1147cd6b10302df619133a162dbb7226533c8ff046ed`  
		Last Modified: Wed, 13 Oct 2021 19:43:10 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c14bbcd8245eb2fa566ddc78e69006db632c4d95351a4a0e2c44aac0541b6875`  
		Last Modified: Wed, 13 Oct 2021 19:43:40 GMT  
		Size: 352.1 MB (352108400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf4ef24556ec98a93248c3e47566a015211a99e03b42dd77f6e0a44f0301d8b`  
		Last Modified: Wed, 13 Oct 2021 19:43:15 GMT  
		Size: 3.9 MB (3871884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3301fb1a089bde0c91dc57582bf359110f5188127c672e482ca07aa79318dbb4`  
		Last Modified: Wed, 13 Oct 2021 19:43:10 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
