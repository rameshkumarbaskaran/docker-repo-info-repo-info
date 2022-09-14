## `eclipse-temurin:18-jdk-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:7574237d0bc94d0028ff6841f7a3d0f23c031e8b8a6fdfbd9e83571b5a5c6802
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1006; amd64
	-	windows version 10.0.17763.3406; amd64

### `eclipse-temurin:18-jdk-windowsservercore` - windows version 10.0.20348.1006; amd64

```console
$ docker pull eclipse-temurin@sha256:f672fd373500d6fb07b0594b582b8fa5baf9304712a8b50467d301edc6090716
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2702598867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5af9fd782b486c8d6aad4d29558aad938d7526167be8e2439ae7243ec70c7dbf`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Thu, 08 Sep 2022 20:30:55 GMT
RUN Install update 10.0.20348.1006
# Wed, 14 Sep 2022 12:09:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Sep 2022 16:26:32 GMT
ENV JAVA_VERSION=jdk-18.0.2.1+1
# Wed, 14 Sep 2022 16:27:32 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2.1%2B1/OpenJDK18U-jdk_x64_windows_hotspot_18.0.2.1_1.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2.1%2B1/OpenJDK18U-jdk_x64_windows_hotspot_18.0.2.1_1.msi ;     Write-Host ('Verifying sha256 (e766c2d6100e70786ff0bb154054dd64bb45ea14ffc995544bbced98eb1c8703) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'e766c2d6100e70786ff0bb154054dd64bb45ea14ffc995544bbced98eb1c8703') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-18' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 14 Sep 2022 16:27:54 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 14 Sep 2022 16:27:55 GMT
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
	-	`sha256:26d5b521ee82dff3a1edca26df6b02fa9c803362e173a6a27332ce7aaf59c045`  
		Last Modified: Wed, 14 Sep 2022 16:54:24 GMT  
		Size: 1.4 KB (1355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71d83c4017b3e13876ab187c57feb0ce3bd424fb5f1a840f40df7c0da02ffe3f`  
		Last Modified: Wed, 14 Sep 2022 16:54:55 GMT  
		Size: 355.1 MB (355106606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b478dfe80bd2f270c30e3e3b3e1734eb8cccc518dc788cd86e8c55b7e02c274`  
		Last Modified: Wed, 14 Sep 2022 16:54:25 GMT  
		Size: 538.5 KB (538481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8b199fcf17c721a9beeb533f86317aed7256799dfa73402fa4dc21c1461c07a`  
		Last Modified: Wed, 14 Sep 2022 16:54:24 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:18-jdk-windowsservercore` - windows version 10.0.17763.3406; amd64

```console
$ docker pull eclipse-temurin@sha256:4358376272d3e72bb7a70d9d2e87fde3e182dbd32d9c2a62d3ab215d5a18e94c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 GB (3062253452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:535ff2c5b91399a7458f32c9874cf1be1cf20bed5acc43d9ca35db806764725e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Fri, 09 Sep 2022 22:43:02 GMT
RUN Install update 10.0.17763.3406
# Tue, 13 Sep 2022 18:21:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Sep 2022 16:28:15 GMT
ENV JAVA_VERSION=jdk-18.0.2.1+1
# Wed, 14 Sep 2022 16:31:50 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2.1%2B1/OpenJDK18U-jdk_x64_windows_hotspot_18.0.2.1_1.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2.1%2B1/OpenJDK18U-jdk_x64_windows_hotspot_18.0.2.1_1.msi ;     Write-Host ('Verifying sha256 (e766c2d6100e70786ff0bb154054dd64bb45ea14ffc995544bbced98eb1c8703) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'e766c2d6100e70786ff0bb154054dd64bb45ea14ffc995544bbced98eb1c8703') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-18' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 14 Sep 2022 16:32:51 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 14 Sep 2022 16:32:52 GMT
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
	-	`sha256:85a1bcd319e0d0b53c51f704f4020596a76b923e111317f26a7c9ceb586b8ce0`  
		Last Modified: Wed, 14 Sep 2022 16:55:08 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d833234d2579ae5c3d9494e167113bc79200a69d9d8724416a2cb31d24becd`  
		Last Modified: Wed, 14 Sep 2022 16:55:40 GMT  
		Size: 354.9 MB (354896078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eccd8582907bf8f5ab267219b6e432f828e9aec00ea89eb6e218b513eddb3b2`  
		Last Modified: Wed, 14 Sep 2022 16:55:09 GMT  
		Size: 3.8 MB (3788427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62086099bd9beb04922e4edfa4367776ed3f95ca640e82c250744ee8fe566ce8`  
		Last Modified: Wed, 14 Sep 2022 16:55:08 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
