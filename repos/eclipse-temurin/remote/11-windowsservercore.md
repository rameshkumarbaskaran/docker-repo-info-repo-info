## `eclipse-temurin:11-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:df3f9c9a76c57e93e97229448d481638c39dc9e5374f500e7fe79f080799dca6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1006; amd64
	-	windows version 10.0.17763.3406; amd64

### `eclipse-temurin:11-windowsservercore` - windows version 10.0.20348.1006; amd64

```console
$ docker pull eclipse-temurin@sha256:a52d0349d55c9ea95b212e9e42e731a9cec00f3930ac4bf3f008a813834484e3
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2714312285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f8066d38982d7a343ad3ef723d5b6ad427454bf4dde4a55f3a99d9731897499`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Thu, 08 Sep 2022 20:30:55 GMT
RUN Install update 10.0.20348.1006
# Wed, 14 Sep 2022 12:09:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Sep 2022 16:07:55 GMT
ENV JAVA_VERSION=jdk-11.0.16.1+1
# Wed, 14 Sep 2022 16:08:55 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jdk_x64_windows_hotspot_11.0.16.1_1.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jdk_x64_windows_hotspot_11.0.16.1_1.msi ;     Write-Host ('Verifying sha256 (d528dbd30b066d9654e1c9a0ce54985ad6575efdf0de6bea32bb35589a9830e1) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'd528dbd30b066d9654e1c9a0ce54985ad6575efdf0de6bea32bb35589a9830e1') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 14 Sep 2022 16:09:15 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 14 Sep 2022 16:09:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4486102fd3820ed9527fa3e7bfefa8305c2f054e65b46dffe9675755e3d8f288`  
		Size: 910.1 MB (910085953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c5da8902b0918fe9bb0d466157622ccaf8209e4becbdd188ec41ecb563c068e6`  
		Last Modified: Wed, 14 Sep 2022 12:41:36 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4ff218aedfc55d388b85a1254e140efaf2579f3752ad0ba69d637cdbfb1d72e`  
		Last Modified: Wed, 14 Sep 2022 16:48:25 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5efa80b6a9a3e5cce3fb10b5d696d73fcd832499310745f9c8b6d0aa2e822e1`  
		Last Modified: Wed, 14 Sep 2022 16:48:55 GMT  
		Size: 366.8 MB (366820411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8ada15c48e87ae623f3e5aab3f86e7c31ab0d18f3607edec2d6593408262986`  
		Last Modified: Wed, 14 Sep 2022 16:48:25 GMT  
		Size: 538.0 KB (538040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00ecc2c921d9349f9393a9885d2d22f5985ce9be14df136e78e15e5d2927fc78`  
		Last Modified: Wed, 14 Sep 2022 16:48:25 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-windowsservercore` - windows version 10.0.17763.3406; amd64

```console
$ docker pull eclipse-temurin@sha256:f82a4436ab7e5094e6deb27e4922d75660e6a45a9bc089eaa33ba77032a2b03a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 GB (3070493292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbba0f5d03e8060e2955f7e986fea807292f9027aeb9b2f70c186faef3f5ab6b`
-	Default Command: `["jshell"]`
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
# Wed, 14 Sep 2022 16:10:58 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jdk_x64_windows_hotspot_11.0.16.1_1.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jdk_x64_windows_hotspot_11.0.16.1_1.msi ;     Write-Host ('Verifying sha256 (d528dbd30b066d9654e1c9a0ce54985ad6575efdf0de6bea32bb35589a9830e1) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'd528dbd30b066d9654e1c9a0ce54985ad6575efdf0de6bea32bb35589a9830e1') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 14 Sep 2022 16:11:55 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 14 Sep 2022 16:11:56 GMT
CMD ["jshell"]
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
	-	`sha256:f3f74e9f9dd79acc3a7a4fa40aca3f80d0467d96cc1b047c2206a179c9c3d5ab`  
		Last Modified: Wed, 14 Sep 2022 16:49:37 GMT  
		Size: 366.6 MB (366606206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7353a57bed0d479e6562f0d678e570df859e3c61635607412658183688ada893`  
		Last Modified: Wed, 14 Sep 2022 16:49:07 GMT  
		Size: 318.1 KB (318130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269b21e890411ba9bddaffa92a050c05aaf751afde9349870676bd129d90956b`  
		Last Modified: Wed, 14 Sep 2022 16:49:07 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
