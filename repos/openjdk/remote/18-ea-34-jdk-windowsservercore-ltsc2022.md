## `openjdk:18-ea-34-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:0a97c7bed674046b7dfba752395737f8dde737fc139633a338b99105f7026718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.473; amd64

### `openjdk:18-ea-34-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.473; amd64

```console
$ docker pull openjdk@sha256:cf2452890b33ab344d84a1923e74efb4b825a34e0732ecaeac8511dac5774e79
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2393132018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdbc7801a5317a7041f0dd43240eef535f89ce1a3e761eb85ab39b15cd2040c6`
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
# Wed, 19 Jan 2022 22:26:59 GMT
ENV JAVA_HOME=C:\openjdk-18
# Wed, 19 Jan 2022 22:27:23 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 08 Feb 2022 02:21:17 GMT
ENV JAVA_VERSION=18-ea+34
# Tue, 08 Feb 2022 02:21:19 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk18/34/GPL/openjdk-18-ea+34_windows-x64_bin.zip
# Tue, 08 Feb 2022 02:21:20 GMT
ENV JAVA_SHA256=116c696ad08d6eee42a25ff414aedc31b9b6b88e237b03896da9ce2f1f144475
# Tue, 08 Feb 2022 02:22:29 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 08 Feb 2022 02:22:31 GMT
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
	-	`sha256:31f4f7a6e8580cb99cf7700636561b27369c4cc2c337a7823ed587aa14afa075`  
		Last Modified: Thu, 20 Jan 2022 02:22:12 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0288f53b75cf04d49e5801c8951aaf24ab2f100a947b6cc053c29402beb2df46`  
		Last Modified: Thu, 20 Jan 2022 02:22:10 GMT  
		Size: 506.4 KB (506430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ae876a00381c19f8c6be40733b02ee8c3f61c0753f4e2c5a6ace4f290acadf`  
		Last Modified: Tue, 08 Feb 2022 03:31:57 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:effac9efc7baf623c6b0aaa94c579bc715cb43e29a0c1a070ad348fa354fda4a`  
		Last Modified: Tue, 08 Feb 2022 03:31:58 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:226cc478ed1b73e10ff80bb177c87051d39ce285375707feff51358c9e4b6dab`  
		Last Modified: Tue, 08 Feb 2022 03:31:57 GMT  
		Size: 1.5 KB (1451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f7c2794d49ed138ee5b277723e049cd776d9e0932d0f7dda12b7b11f2360f4f`  
		Last Modified: Tue, 08 Feb 2022 03:35:10 GMT  
		Size: 184.5 MB (184516042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f30034bd9b894bcbc05249f3571260154ead75dc73f64ec2070ed7bfe25baea`  
		Last Modified: Tue, 08 Feb 2022 03:31:57 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
