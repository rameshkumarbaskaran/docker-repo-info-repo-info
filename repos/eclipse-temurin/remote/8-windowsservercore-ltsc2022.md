## `eclipse-temurin:8-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:2c4366f5c6bb8839369093ef2b3e8b55459234608ab782b7b1b3dd516ab41726
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.524; amd64

### `eclipse-temurin:8-windowsservercore-ltsc2022` - windows version 10.0.20348.524; amd64

```console
$ docker pull eclipse-temurin@sha256:6a775f5225c002a25f9b3cb40632a7e5c98f8174f6e0f1361fee1ce84a3ea533
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2405103077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9db257f5a98e8ae6c8ab5010474a5a817a1e3bddd2e407738bb12cf110c95812`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Tue, 01 Feb 2022 02:49:40 GMT
RUN Install update ltsc2022-amd64
# Wed, 09 Feb 2022 13:37:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Feb 2022 19:43:44 GMT
ENV JAVA_VERSION=jdk8u322-b06
# Wed, 09 Feb 2022 19:44:52 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_x64_windows_hotspot_8u322b06.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_x64_windows_hotspot_8u322b06.msi ;     Write-Host ('Verifying sha256 (e9337d5bba9b60a9d00a939fecb05718b2303023a587da6ae4862080714f9f0b) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'e9337d5bba9b60a9d00a939fecb05718b2303023a587da6ae4862080714f9f0b') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 09 Feb 2022 19:45:12 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac -version'; javac -version;     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:898469748ff68223ab87b654b29fb366c1f4f2b7cfad7a37426346ea16db8dfa`  
		Size: 963.2 MB (963225591 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7062696b7aef1ca33afdf32084a532f7e3151a844eb7cb2455bcc907e0f42a58`  
		Last Modified: Wed, 09 Feb 2022 14:28:27 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba7b901e4e6b6e91c80f180e35739299ac255bea90215aa01fa0150f31618d73`  
		Last Modified: Thu, 10 Feb 2022 20:32:40 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:046221b7ecea405949a67ddf54d23419d6ffd9db5365bfb501f0ca584a64a591`  
		Last Modified: Thu, 10 Feb 2022 20:32:57 GMT  
		Size: 189.6 MB (189627007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28c3a2890571e235ca5dc398334fc962c42bcdf4f2237cf42c83a660be6dfcb9`  
		Last Modified: Thu, 10 Feb 2022 20:32:40 GMT  
		Size: 548.6 KB (548594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
