## `eclipse-temurin:11-jdk-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:f4440e4377f121a3ec0c320a6708d607d5ed92895be477a50e8cc21cf6c36d18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.524; amd64
	-	windows version 10.0.17763.2565; amd64

### `eclipse-temurin:11-jdk-windowsservercore` - windows version 10.0.20348.524; amd64

```console
$ docker pull eclipse-temurin@sha256:636066e9ae78c26340e0c2cf1ee020875776bfc3ec2b0d60f39cb16bb7ba8ff8
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2581717161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daeb1a48d63e74d6aad26eef44e145c8e4de1a47d049550b59a8849710c834d0`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Tue, 01 Feb 2022 02:49:40 GMT
RUN Install update ltsc2022-amd64
# Wed, 09 Feb 2022 13:37:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 10 Feb 2022 20:16:34 GMT
ENV JAVA_VERSION=jdk-11.0.14.1+1
# Thu, 10 Feb 2022 20:18:16 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_x64_windows_hotspot_11.0.14.1_1.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_x64_windows_hotspot_11.0.14.1_1.msi ;     Write-Host ('Verifying sha256 (afa6379e9b4bab0bdbf40a1051a219414d8c8fcb2c095e1552d23505293a577e) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'afa6379e9b4bab0bdbf40a1051a219414d8c8fcb2c095e1552d23505293a577e') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 10 Feb 2022 20:18:39 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Thu, 10 Feb 2022 20:18:40 GMT
CMD ["jshell"]
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
	-	`sha256:0dbd4a5d54ec2938ad933b2dc5df0f090cec8d90f477f2e3951b8d34e93748cb`  
		Last Modified: Thu, 10 Feb 2022 20:39:12 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f89d1c803aef76ea6a2451f9699840772b7bc1da9c156a208afd7857226796e1`  
		Last Modified: Thu, 10 Feb 2022 20:45:56 GMT  
		Size: 366.2 MB (366240015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2ff9934b62a32d1f11910083f3aab333a38dff0d42e1196d3fca1ffee73f5bb`  
		Last Modified: Thu, 10 Feb 2022 20:39:13 GMT  
		Size: 548.5 KB (548488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ad058629eec062788006e7ac5b60189ff068843467064fd5367b2c4d9a05ce9`  
		Last Modified: Thu, 10 Feb 2022 20:39:12 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jdk-windowsservercore` - windows version 10.0.17763.2565; amd64

```console
$ docker pull eclipse-temurin@sha256:53c7379e2d9d8f18d4f2e576887df97364cdee5d880a37f38739ace7458dd94d
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 GB (3080087035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fe708061959b00b6713a0d35dc7123d78a74a384e33eaf2b02c56bee9ba2ac2`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 02 Feb 2022 19:28:56 GMT
RUN Install update 1809-amd64
# Wed, 09 Feb 2022 13:09:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 10 Feb 2022 20:18:47 GMT
ENV JAVA_VERSION=jdk-11.0.14.1+1
# Thu, 10 Feb 2022 20:20:59 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_x64_windows_hotspot_11.0.14.1_1.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_x64_windows_hotspot_11.0.14.1_1.msi ;     Write-Host ('Verifying sha256 (afa6379e9b4bab0bdbf40a1051a219414d8c8fcb2c095e1552d23505293a577e) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'afa6379e9b4bab0bdbf40a1051a219414d8c8fcb2c095e1552d23505293a577e') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 10 Feb 2022 20:21:59 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Thu, 10 Feb 2022 20:22:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1bd78008c728d8f9e56dc2093e6eb55f0f0b1aa96e5d0c7ccc830c5f60876cdf`  
		Size: 995.4 MB (995381853 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f0c1566a9285d9465334dc923e9d6fd93a51b3ef6cb8497efcacbcf64e3b93fc`  
		Last Modified: Wed, 09 Feb 2022 13:26:13 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc27bdddb8879204876f5a95dbc73c22b95baab525c7b3ed1d06350acee9468c`  
		Last Modified: Thu, 10 Feb 2022 20:46:09 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ca1ba9d6707a06fbfe037765b81fbe5940039ccf27aa3d30114eca5adfe3ed4`  
		Last Modified: Thu, 10 Feb 2022 20:46:52 GMT  
		Size: 366.0 MB (366027665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dd561584f5caf1bd23631efc13c99d9cd3f2bac89a202b5baaa4fe7cca1f169`  
		Last Modified: Thu, 10 Feb 2022 20:46:09 GMT  
		Size: 340.5 KB (340479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b14f39924e89ea6c9de6aaa6490868abefc1d7bd68658373a6300a94c676eb87`  
		Last Modified: Thu, 10 Feb 2022 20:46:09 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
