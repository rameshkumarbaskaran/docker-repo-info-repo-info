## `eclipse-temurin:11-windowsservercore-1809`

```console
$ docker pull eclipse-temurin@sha256:cdb22618b4a4a59a1b7adb44ea5be43d0060e4136ff757a4886ab8a1c8136f75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4737; amd64

### `eclipse-temurin:11-windowsservercore-1809` - windows version 10.0.17763.4737; amd64

```console
$ docker pull eclipse-temurin@sha256:7c3e8b2ce576fcd2663e61b6981e98012063882218f25109ffe89c84ba554842
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2363636857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a25f7a46f1b4c5255bb9aa9c1fc3e0898281f5b2f6e2b5ef5769bc2710705cae`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 02 Aug 2023 09:07:15 GMT
RUN Install update 10.0.17763.4737
# Wed, 09 Aug 2023 23:36:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 31 Aug 2023 20:17:22 GMT
ENV JAVA_VERSION=jdk-11.0.20.1+1
# Thu, 31 Aug 2023 20:19:06 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jdk_x64_windows_hotspot_11.0.20.1_1.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jdk_x64_windows_hotspot_11.0.20.1_1.msi ;     Write-Host ('Verifying sha256 (51785957427c5f34581930fbb224a44550f70d1c5ecb6f05ab27432e6a1f9a75) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '51785957427c5f34581930fbb224a44550f70d1c5ecb6f05ab27432e6a1f9a75') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 31 Aug 2023 20:20:05 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Thu, 31 Aug 2023 20:20:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95f433aa7d90194e65f6b08a599b3ee12292e124d47c204107baedfd71054c1`  
		Last Modified: Tue, 08 Aug 2023 18:31:16 GMT  
		Size: 345.3 MB (345334986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03d23fbbd4f650b6f60106a3cc28d711efce2f97cfb80b67e2dec305e011aa3`  
		Last Modified: Thu, 10 Aug 2023 00:19:47 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07f504e4e741de21d212954d1da593b5baa3249d5351e3bd0b201fee8cd36f67`  
		Last Modified: Thu, 31 Aug 2023 20:41:14 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2da0b58474e69a07881c80fd8137e38b1a0afa458c38462bf8bfaa646b42610d`  
		Last Modified: Thu, 31 Aug 2023 20:41:41 GMT  
		Size: 367.5 MB (367453010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a0c9c3edd81eab104f3e8dd0787328f715e7b081f428a44dd925588cc0c00cd`  
		Last Modified: Thu, 31 Aug 2023 20:41:15 GMT  
		Size: 224.2 KB (224243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f492b23b28a96b475aac90605904021e77682f5cc1df681599983ab1c633ed12`  
		Last Modified: Thu, 31 Aug 2023 20:41:14 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
