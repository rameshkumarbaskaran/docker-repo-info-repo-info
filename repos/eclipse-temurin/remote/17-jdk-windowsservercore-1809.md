## `eclipse-temurin:17-jdk-windowsservercore-1809`

```console
$ docker pull eclipse-temurin@sha256:536494fad98885dcafe3cc4e56effdf179a53a084c08d464c321a2c01c42c521
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2183; amd64

### `eclipse-temurin:17-jdk-windowsservercore-1809` - windows version 10.0.17763.2183; amd64

```console
$ docker pull eclipse-temurin@sha256:a82784dae7d4d1aa931a17ba9148472efb57395b3c368cb74f7a461235644112
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (3042804057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50d2b943b9d173cc14dd17f03155a8dc2a7d681d888ebd65276c6d7f6f5e4cbc`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Sep 2021 04:08:33 GMT
RUN Install update 1809-amd64
# Wed, 15 Sep 2021 00:29:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 22 Sep 2021 19:15:34 GMT
ENV JAVA_VERSION=jdk-17+35
# Wed, 22 Sep 2021 19:17:30 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17%2B35/OpenJDK17-jdk_x64_windows_hotspot_17_35.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17%2B35/OpenJDK17-jdk_x64_windows_hotspot_17_35.msi ;     Write-Host ('Verifying sha256 (4a0350a9e3e0cf3bba9a57890bb0b223b7c47883169730f122100fc31d61d486) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '4a0350a9e3e0cf3bba9a57890bb0b223b7c47883169730f122100fc31d61d486') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-17' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 22 Sep 2021 19:18:48 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 22 Sep 2021 19:18:49 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a0ddf88812f10c7d6edc858aa9784ff5ca9de4a7bb631909c090090343abd059`  
		Size: 968.4 MB (968365008 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:92dd43eae724dbe7e9e517c7fded74c5920ae7eb160042055178ceadf1916505`  
		Last Modified: Wed, 15 Sep 2021 01:09:40 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c7bc84dd2ef854244ef9f7b1caee8d74639379e182ee9e4f3a6a2c184069654`  
		Last Modified: Wed, 22 Sep 2021 19:24:58 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:709113e5bf3e2809b5096023ece3c9e088bcef42c216e30e4098103056a70895`  
		Last Modified: Wed, 22 Sep 2021 19:25:29 GMT  
		Size: 352.2 MB (352199477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff708a91afddfce768ffad2f5a814cc77bf95b73106cbb6356db91f105eedc5e`  
		Last Modified: Wed, 22 Sep 2021 19:25:00 GMT  
		Size: 3.9 MB (3902550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09db3cb2244bb78aefea4c2a1996890b1471ea8d7d939d461b8416102600a4e9`  
		Last Modified: Wed, 22 Sep 2021 19:24:58 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
