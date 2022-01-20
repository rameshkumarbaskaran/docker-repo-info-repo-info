## `openjdk:17-jdk-windowsservercore`

```console
$ docker pull openjdk@sha256:b7c781a55d539fbf84f4328381247805c2b4a1a48578616252a54a2f7b41a42c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.473; amd64
	-	windows version 10.0.17763.2458; amd64

### `openjdk:17-jdk-windowsservercore` - windows version 10.0.20348.473; amd64

```console
$ docker pull openjdk@sha256:7ba7c200003aae389704e228c259fa4aa68076d24dcf0dcb4bbee1850e964ae5
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2391730192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cb459a0fb41f54e484742f238474baec35501d3a5ec788445a688ed769a4c66`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Sun, 16 Jan 2022 05:17:24 GMT
RUN Install update ltsc2022-amd64
# Wed, 19 Jan 2022 22:21:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 19 Jan 2022 22:23:11 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 19 Jan 2022 22:30:05 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 19 Jan 2022 22:30:28 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 19 Jan 2022 22:30:29 GMT
ENV JAVA_VERSION=17.0.2
# Wed, 19 Jan 2022 22:30:30 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk17.0.2/dfd4a8d0985749f896bed50d7138ee7f/8/GPL/openjdk-17.0.2_windows-x64_bin.zip
# Wed, 19 Jan 2022 22:30:32 GMT
ENV JAVA_SHA256=b2208206bda47f2e0c971a39e057a5ec32c40b503d71e486790cb728d926b615
# Wed, 19 Jan 2022 22:31:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 19 Jan 2022 22:31:40 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0e02c12b1310e6c76c29fcd6f81905400fdb6a01caac9dc825939ad004baffef`  
		Size: 955.8 MB (955800778 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2e1f45a873642f0aab3474828d75469362741244e7c714068ac1afe056102cd6`  
		Last Modified: Thu, 20 Jan 2022 00:40:19 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa436893917b4b24f7020ae30c97fa33ab983d9c24e6fd7534d56f8b19bf786f`  
		Last Modified: Thu, 20 Jan 2022 02:19:54 GMT  
		Size: 601.2 KB (601200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3d38fb151b453ed72a7d16734e7d91a3a2bfb6b622dd458c3ff46f3be644c64`  
		Last Modified: Thu, 20 Jan 2022 02:27:13 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51a39f82d9b57a2deb5ae7adf74626e2eb6d5e5ec51662ffa4c3e1641aead0d7`  
		Last Modified: Thu, 20 Jan 2022 02:27:14 GMT  
		Size: 506.2 KB (506238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6862eb1691094e7d22cb113ee1cd2cfa85b15b65e8d4fb14c89d91a990752800`  
		Last Modified: Thu, 20 Jan 2022 02:27:11 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f49d2ad697832e8023b553711150c496d3e0be21b9a23d29b33bf3ebb7c00cd`  
		Last Modified: Thu, 20 Jan 2022 02:27:11 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f96d5aad430dd800e432ec7af090cf949db1e4d032a5b30f7c73917ae584ae1`  
		Last Modified: Thu, 20 Jan 2022 02:27:11 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d3ad0678d1925aa712117c89d1e9b9f65d1399e3b6eeb2a42537f978d4a6cd`  
		Last Modified: Thu, 20 Jan 2022 02:27:31 GMT  
		Size: 183.1 MB (183114447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52c1e6d63f0a00fd3c7c398ad05c72547358687848437d0dc91a746ceb5b317b`  
		Last Modified: Thu, 20 Jan 2022 02:27:11 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:17-jdk-windowsservercore` - windows version 10.0.17763.2458; amd64

```console
$ docker pull openjdk@sha256:2b47f15fb580c0bac2fa6633531b47b8689ecb346b6e77942064e761e3d9a6d4
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2896920845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d84bb4e90ce2297df2e20a9060ee0daee6d44ca42c3b19f3139defdff8335ff`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 18 Jan 2022 01:52:23 GMT
RUN Install update 1809-amd64
# Wed, 19 Jan 2022 23:21:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 19 Jan 2022 23:23:41 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 19 Jan 2022 23:30:40 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 19 Jan 2022 23:31:45 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 19 Jan 2022 23:31:46 GMT
ENV JAVA_VERSION=17.0.2
# Wed, 19 Jan 2022 23:31:47 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk17.0.2/dfd4a8d0985749f896bed50d7138ee7f/8/GPL/openjdk-17.0.2_windows-x64_bin.zip
# Wed, 19 Jan 2022 23:31:48 GMT
ENV JAVA_SHA256=b2208206bda47f2e0c971a39e057a5ec32c40b503d71e486790cb728d926b615
# Wed, 19 Jan 2022 23:33:33 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 19 Jan 2022 23:33:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:567fd00846e9a9f44eea5925b497356dda00fe89b8335d2a3b2a8b9d84b0bb69`  
		Size: 995.0 MB (994988595 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba7b1090ce9545f6aac90d390785f6c5e3846304cb7596289dfc36c169d7b1da`  
		Last Modified: Thu, 20 Jan 2022 00:40:41 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98c73c8d54eeae51e9c93499966b4413ea63f218bdf175bed7b7d83c76e6d58`  
		Last Modified: Thu, 20 Jan 2022 02:20:37 GMT  
		Size: 357.3 KB (357347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c663ce98e3a5b030262b038827cbdf4e5010bee8b412efff8591d8ac731e475`  
		Last Modified: Thu, 20 Jan 2022 02:27:59 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8013a01b5339df4046472ce3c58fbb4604827be136c9fe26686a567e91033f25`  
		Last Modified: Thu, 20 Jan 2022 02:27:59 GMT  
		Size: 310.8 KB (310830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc9cbed329d34b94e0c3fb656fe8edbab80d5ac585c8081e830794283127ef90`  
		Last Modified: Thu, 20 Jan 2022 02:27:56 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:783d4af08d78b8ec5912c14b980ce54830073932e2aa9b2b21aa40113c5e116f`  
		Last Modified: Thu, 20 Jan 2022 02:27:56 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66edb0b13bccbc5568a9d2a2a1843f6f41e4c556378543bf83fdf1228a2776b5`  
		Last Modified: Thu, 20 Jan 2022 02:27:56 GMT  
		Size: 1.4 KB (1385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d6fffdad4f88bd160f47b1dce7b1298b776ef626cc6f5c609e5418cdab23d5e`  
		Last Modified: Thu, 20 Jan 2022 02:31:09 GMT  
		Size: 182.9 MB (182922697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fea6086b2d9b422a232d207aaa0ef6a42727380dc51c95016e6157f3c51ed84`  
		Last Modified: Thu, 20 Jan 2022 02:27:57 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
