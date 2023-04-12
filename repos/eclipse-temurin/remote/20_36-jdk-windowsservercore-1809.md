## `eclipse-temurin:20_36-jdk-windowsservercore-1809`

```console
$ docker pull eclipse-temurin@sha256:e76094da9bcade4b2c259089363a22d53fec107b6f9f00c74d8107808456447d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4252; amd64

### `eclipse-temurin:20_36-jdk-windowsservercore-1809` - windows version 10.0.17763.4252; amd64

```console
$ docker pull eclipse-temurin@sha256:9b56feec90636eefd620a38568714e23dfe073f7d108d36d925eb598352771da
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2444981477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1210e4b78873bcb6a890f203b83f286793e1141c0eb4e2640e542d8f331e83e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Wed, 05 Apr 2023 00:41:54 GMT
RUN Install update 10.0.17763.4252
# Tue, 11 Apr 2023 23:40:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Apr 2023 01:32:59 GMT
ENV JAVA_VERSION=jdk-20+36
# Wed, 12 Apr 2023 01:34:52 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin20-binaries/releases/download/jdk-20%2B36/OpenJDK20U-jdk_x64_windows_hotspot_20_36.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin20-binaries/releases/download/jdk-20%2B36/OpenJDK20U-jdk_x64_windows_hotspot_20_36.msi ;     Write-Host ('Verifying sha256 (d4e41a6fce8f86dabb0422231f4723579021479eb9331cd9d07fb01c4126a022) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'd4e41a6fce8f86dabb0422231f4723579021479eb9331cd9d07fb01c4126a022') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-20' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 12 Apr 2023 01:36:10 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 12 Apr 2023 01:36:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9094c39c4b36a86359abb3da9e9d0d9c69b6930e9c7b308120310d43d63f693`  
		Last Modified: Wed, 12 Apr 2023 00:52:10 GMT  
		Size: 363.3 MB (363347289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9103f1e2cdefe8f16dae9619b88e38aa659abb17276d2362d435ad0721d3bf41`  
		Last Modified: Wed, 12 Apr 2023 00:50:55 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf58737ada6ceb6ccecf61ac725e911958369f4e22c3246ea140a32ec2727d5a`  
		Last Modified: Wed, 12 Apr 2023 09:43:18 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b352ffecfe246b34443af7eabc5e9c67ba02bc9993165f1c3030d65d2489b14`  
		Last Modified: Wed, 12 Apr 2023 09:43:53 GMT  
		Size: 369.7 MB (369666411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2006773ee17fb2d6f237b905d6f33cb222f7222139f6646bfe5842e824cc983`  
		Last Modified: Wed, 12 Apr 2023 09:43:20 GMT  
		Size: 4.0 MB (4019698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d649b08b4556c9f1210ced47fd491164df86492168363a485fc6830197bb205f`  
		Last Modified: Wed, 12 Apr 2023 09:43:18 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
