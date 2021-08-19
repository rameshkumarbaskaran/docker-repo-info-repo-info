## `eclipse-temurin:8-jre`

```console
$ docker pull eclipse-temurin@sha256:8b50fc756a7122ceffb378740cd04166f48c01673d76208f86bdbe0ddab1e820
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	windows version 10.0.17763.2114; amd64
	-	windows version 10.0.14393.4583; amd64

### `eclipse-temurin:8-jre` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:259019760a21d85abf527a6874821069a49ad3fed6ede263d32536787d592b9c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.3 MB (86312650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad64d8568d4727abe7bed54f223bd130023b2ba7412e0d64fe1d56485a6b3b86`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:59:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 19 Aug 2021 20:21:59 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Aug 2021 20:22:00 GMT
ENV JAVA_VERSION=jdk8u302-b08
# Thu, 19 Aug 2021 20:22:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='a74e63657ad04151a8f95202071d2895f1cc9295c910ad3c361ff1cc27395107';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_x64_linux_hotspot_8u302b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 19 Aug 2021 20:22:04 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Aug 2021 20:22:05 GMT
RUN echo Verifying install ...     && echo   java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07835b17b92ab861c8965cceb50fb949c78dfadc034faaead298983cc494906f`  
		Last Modified: Thu, 19 Aug 2021 20:23:41 GMT  
		Size: 16.0 MB (16032608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41d6d46cb5dafc99d7cddddf2bd3e51092da5d10027b018b6d1f64f5a45d1de7`  
		Last Modified: Thu, 19 Aug 2021 20:23:43 GMT  
		Size: 41.7 MB (41711938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:272c4372a00c532a7f86afdb1a365b2dc393c4eb7b0b83eac6b6d91c1a68249c`  
		Last Modified: Thu, 19 Aug 2021 20:23:37 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-jre` - windows version 10.0.17763.2114; amd64

```console
$ docker pull eclipse-temurin@sha256:b48c8596379632eb0d7326e05715750e2c65d4d1bd511666f6e51fe69dff6a93
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2756965689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6134357607772d8358e333f99a678216379e649232eec2418e5110535551f389`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 05 Aug 2021 19:44:34 GMT
RUN Install update 1809-amd64
# Wed, 11 Aug 2021 12:16:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 13 Aug 2021 21:32:38 GMT
ENV JAVA_VERSION=jdk8u302-b08
# Thu, 19 Aug 2021 20:16:23 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_x64_windows_hotspot_8u302b08.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_x64_windows_hotspot_8u302b08.msi ;     Write-Host ('Verifying sha256 (34e5eea737dfaca57ec5162e6fece5259f403fa419c7bcab572e9cdd2bcf8dd1) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '34e5eea737dfaca57ec5162e6fece5259f403fa419c7bcab572e9cdd2bcf8dd1') {             Write-Host 'FAILED!';             exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {             Write-Host 'FAILED installing MSI!' ;             exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 19 Aug 2021 20:17:54 GMT
RUN Write-Host 'Verifying install ...';     Write-Host '  java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c67ded6868b61d392a0c096f911563fd6bc0bc3ed4fe401d077b3718a1b0cdaf`  
		Size: 967.7 MB (967665054 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f5be68d5dab08a1dcc52a6ee52dd4901e4d6a384f0df3a12cba3d53649f7c602`  
		Last Modified: Wed, 11 Aug 2021 13:29:37 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4366f6dcb586d60ea7d0031a2dcac52b65aff56b1029ade45a73aa1df80b279`  
		Last Modified: Fri, 13 Aug 2021 22:00:10 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d41e89342d74afcd4485007252993c065ea8445afb3e5818bb9867e21de6601`  
		Last Modified: Thu, 19 Aug 2021 20:25:49 GMT  
		Size: 70.6 MB (70621145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f28e23fd65d57423793eaf946468fd91cdd77e4492ebf84297e04fa667c479c`  
		Last Modified: Thu, 19 Aug 2021 20:24:27 GMT  
		Size: 343.7 KB (343749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-jre` - windows version 10.0.14393.4583; amd64

```console
$ docker pull eclipse-temurin@sha256:b1b3be103a39c8ebfd577c947820a0608a3943cad44401a7c2407a06b1f97ed2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6341807673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:884b9a193a0b99e3f48380bea9f70f6d7b7ed9d46d3486ec9c530044aedbdd3c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Sun, 01 Aug 2021 08:52:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Aug 2021 12:51:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 13 Aug 2021 21:36:03 GMT
ENV JAVA_VERSION=jdk8u302-b08
# Thu, 19 Aug 2021 20:20:14 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_x64_windows_hotspot_8u302b08.msi ...');     [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12 ; Invoke-WebRequest -Uri https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_x64_windows_hotspot_8u302b08.msi -O 'openjdk.msi' ;     Write-Host ('Verifying sha256 (34e5eea737dfaca57ec5162e6fece5259f403fa419c7bcab572e9cdd2bcf8dd1) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '34e5eea737dfaca57ec5162e6fece5259f403fa419c7bcab572e9cdd2bcf8dd1') {             Write-Host 'FAILED!';             exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {             Write-Host 'FAILED installing MSI!' ;             exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 19 Aug 2021 20:21:57 GMT
RUN Write-Host 'Verifying install ...';     Write-Host '  java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c427f892fe74603ae09d4e49b25f8f7046f957054034dc9f462e0e88d7bffaa5`  
		Size: 2.2 GB (2200980134 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2d4b5c087d85e7fbeffd8b282ecd862da1fb7ff00c37657c5712888936292097`  
		Last Modified: Wed, 11 Aug 2021 13:30:26 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:482fe77a1b07de2e3de2d4afb544f5d4e94c199a6882f435600f2884c30be901`  
		Last Modified: Fri, 13 Aug 2021 22:00:39 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:665c822e6ce5a88b8719e4854a21652071a8c78119e3edc3510487ee57443e4f`  
		Last Modified: Thu, 19 Aug 2021 20:26:08 GMT  
		Size: 70.5 MB (70525959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:666b04b3f42ef2dd7b8458619ae9de3bb152ba5bedd0054cce312e4268ee26e8`  
		Last Modified: Thu, 19 Aug 2021 20:25:59 GMT  
		Size: 312.9 KB (312874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
