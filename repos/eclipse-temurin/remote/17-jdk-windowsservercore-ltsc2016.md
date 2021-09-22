## `eclipse-temurin:17-jdk-windowsservercore-ltsc2016`

```console
$ docker pull eclipse-temurin@sha256:51b4965615441bf8e9d4eef4efc2089ed4a4b3f0532fffe7ba4f9326708fb6d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.14393.4651; amd64

### `eclipse-temurin:17-jdk-windowsservercore-ltsc2016` - windows version 10.0.14393.4651; amd64

```console
$ docker pull eclipse-temurin@sha256:6924b3cac13f1ac82af6e1c40e25b5cde82c8a82a9fd2c6965e5ef67d75e62a5
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 GB (6627329938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e6fc83bd90649092deac8e4f8399da9ddfe35a4bab8fd44e34bcf411b0a885d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 13 Sep 2021 01:03:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Sep 2021 00:34:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 22 Sep 2021 19:19:00 GMT
ENV JAVA_VERSION=jdk-17+35
# Wed, 22 Sep 2021 19:20:47 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17%2B35/OpenJDK17-jdk_x64_windows_hotspot_17_35.msi ...');     [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12 ; Invoke-WebRequest -Uri https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17%2B35/OpenJDK17-jdk_x64_windows_hotspot_17_35.msi -O 'openjdk.msi' ;     Write-Host ('Verifying sha256 (4a0350a9e3e0cf3bba9a57890bb0b223b7c47883169730f122100fc31d61d486) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '4a0350a9e3e0cf3bba9a57890bb0b223b7c47883169730f122100fc31d61d486') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-17' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 22 Sep 2021 19:22:04 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 22 Sep 2021 19:22:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e9b8281bf21e46c781fb54e4f15f5728e2c44dea4219c9e6deeb732f1d909d3b`  
		Size: 2.2 GB (2201342322 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8721f004192f15fe71b8626ef3f3e34cbf2cfe1d15a63b6b544ab946162ef707`  
		Last Modified: Wed, 15 Sep 2021 01:10:18 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f49d9944f0ee26658bd3b061f70175331db2d135498f135b51e2d56bc91296f0`  
		Last Modified: Wed, 22 Sep 2021 19:25:42 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfe1184e431040d16efe337b3e1c033ffd44b3e31e8c40cf3280dd67725cc262`  
		Last Modified: Wed, 22 Sep 2021 19:26:11 GMT  
		Size: 352.1 MB (352119229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c0068fbe946985173169c879030f09738015917ae0723f10296e944cde09ec9`  
		Last Modified: Wed, 22 Sep 2021 19:25:43 GMT  
		Size: 3.9 MB (3878599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85d22dcfef501c6b259fb677722a930d25a48b97a0eba137de4b785c00ae0221`  
		Last Modified: Wed, 22 Sep 2021 19:25:42 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
