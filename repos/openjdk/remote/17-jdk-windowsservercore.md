## `openjdk:17-jdk-windowsservercore`

```console
$ docker pull openjdk@sha256:9b5e9de59974f824250899ddf8d56d256c05d14fbccfdb664ca498f7cf8994cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.469; amd64
	-	windows version 10.0.17763.2452; amd64

### `openjdk:17-jdk-windowsservercore` - windows version 10.0.20348.469; amd64

```console
$ docker pull openjdk@sha256:4aae3b637684d26cd3b989a2930f0e21bae5014c1e0c9789dc73def426f5ac82
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2391579088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ed079b3284996e9c9202f2650b1b3c84717d114fe23ff19f9832b177b28470d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Thu, 06 Jan 2022 03:56:33 GMT
RUN Install update ltsc2022-amd64
# Tue, 11 Jan 2022 18:59:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Jan 2022 05:09:49 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 12 Jan 2022 05:30:03 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 12 Jan 2022 05:30:24 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 12 Jan 2022 05:30:25 GMT
ENV JAVA_VERSION=17.0.1
# Wed, 12 Jan 2022 05:30:26 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk17.0.1/2a2082e5a09d4267845be086888add4f/12/GPL/openjdk-17.0.1_windows-x64_bin.zip
# Wed, 12 Jan 2022 05:30:28 GMT
ENV JAVA_SHA256=329900a6673b237b502bdcf77bc334da34bc91355c5fd2d457fc00f53fd71ef1
# Wed, 12 Jan 2022 05:31:26 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 12 Jan 2022 05:31:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:9b593686e27e7562a5b0696823307ffa822214cee8bd2eec1075eadad4cb9712`  
		Size: 956.0 MB (956001983 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:99e0b71ede60d3b2c5b9053bf27e47c0875590991eede49813d849cc660c7551`  
		Last Modified: Tue, 11 Jan 2022 19:32:06 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c42ce1d7b7857ac1eb8d4fbf9579f07cf6a89ed47f3a0979451365d92324f699`  
		Last Modified: Wed, 12 Jan 2022 22:55:59 GMT  
		Size: 644.8 KB (644784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf69350006ea949808daf3fc697a581e66d7b95921a83e53de6bc31d5db522a1`  
		Last Modified: Wed, 12 Jan 2022 23:05:55 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b8ebab832ceb215be7cb31f146c8bed89448602e10c0486ad91ee2fbae3cfb2`  
		Last Modified: Wed, 12 Jan 2022 23:05:56 GMT  
		Size: 551.6 KB (551577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56375712b7ab2fc8a30694df28154153a69cb31c2f49b16322820f0bcec56844`  
		Last Modified: Wed, 12 Jan 2022 23:05:53 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a57b91fd34c83efa97b67dc431cbf33b9f48a1bf51351f6c6452146baabb095`  
		Last Modified: Wed, 12 Jan 2022 23:05:53 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2921a0cb42a7fc65ce4fbb9abee7eb56cde82537b624975c5b5123d2ea3180a`  
		Last Modified: Wed, 12 Jan 2022 23:05:53 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08db1d3fa66870a3b0c82ab2ba0061e30e1600683a70dc92438aa015ca35c21a`  
		Last Modified: Wed, 12 Jan 2022 23:06:15 GMT  
		Size: 182.7 MB (182673242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de44def65b962c8c9485ce04756d87847564420d2bc4e60b6a60f465820db746`  
		Last Modified: Wed, 12 Jan 2022 23:05:53 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:17-jdk-windowsservercore` - windows version 10.0.17763.2452; amd64

```console
$ docker pull openjdk@sha256:2b2e69ec1047ac8f74cbcce6031c189e7b3edfc6e0be6794744defed1332c5b8
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2895316518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bee5571c4901206f1abf82d71c3209c468058e59e9ed19ee1cd8a75de7c950c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 07 Jan 2022 22:48:13 GMT
RUN Install update 1809-amd64
# Wed, 12 Jan 2022 05:11:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Jan 2022 05:12:35 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 12 Jan 2022 05:31:45 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 12 Jan 2022 05:32:43 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 12 Jan 2022 05:32:44 GMT
ENV JAVA_VERSION=17.0.1
# Wed, 12 Jan 2022 05:32:45 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk17.0.1/2a2082e5a09d4267845be086888add4f/12/GPL/openjdk-17.0.1_windows-x64_bin.zip
# Wed, 12 Jan 2022 05:32:46 GMT
ENV JAVA_SHA256=329900a6673b237b502bdcf77bc334da34bc91355c5fd2d457fc00f53fd71ef1
# Wed, 12 Jan 2022 05:34:33 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 12 Jan 2022 05:34:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:635f15ebd5b486e8a00bf217a0574a29550e5bbf08c1d021e1e308100b2e49b5`  
		Size: 993.9 MB (993898043 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3a70d5fd54e2005efbf590b48700ed40509210354a0d8f3f18c3b444a5325896`  
		Last Modified: Wed, 12 Jan 2022 06:20:33 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d74f00c66c11971de2e35204e3f42aca9ac77b3dba4dcd545130bea41c91fd27`  
		Last Modified: Wed, 12 Jan 2022 22:56:55 GMT  
		Size: 346.0 KB (345951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7014e99f571cfcd24c19fb5a487bf4afe1dcb811f528d65c21725f961e4eaa80`  
		Last Modified: Wed, 12 Jan 2022 23:06:47 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42895b59af59e02410c8ddc82959acf091e9ca80ef27db786446fed8b0603c69`  
		Last Modified: Wed, 12 Jan 2022 23:06:47 GMT  
		Size: 303.0 KB (302974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eb45d7171fe478528b968ba6e2868259a66583ca1ba4e4094d5337de6ab4dcc`  
		Last Modified: Wed, 12 Jan 2022 23:06:44 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d141cf6adf2eef0c732052d9b0c2633017ee86901aa2320d9d5433695a92263a`  
		Last Modified: Wed, 12 Jan 2022 23:06:44 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05d99b148200d6a1a2dd13c3a7c53d2ecfa4bd3e5185ba0875e569fbde4b335d`  
		Last Modified: Wed, 12 Jan 2022 23:06:44 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada38029f5d04ac6d939528896a5222e9fcffc48fb2675892788a98eb41bba55`  
		Last Modified: Wed, 12 Jan 2022 23:07:06 GMT  
		Size: 182.4 MB (182428223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b217a5d77b84271c20e2dca6c30b04613cb5eef4cb9fa22fce4c9271feeb4a52`  
		Last Modified: Wed, 12 Jan 2022 23:06:44 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
