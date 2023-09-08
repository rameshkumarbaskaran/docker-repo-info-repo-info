## `openjdk:22-windowsservercore`

```console
$ docker pull openjdk@sha256:c6f4102e2aef57dda25bfd3ca59a80620643cbadfebd14b8720a71254d9778bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1906; amd64
	-	windows version 10.0.17763.4737; amd64

### `openjdk:22-windowsservercore` - windows version 10.0.20348.1906; amd64

```console
$ docker pull openjdk@sha256:3b2a7c95f953dc7e6606aab9865559b35d89b98e29644aee5c389c2c1cf45213
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1997373928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a92d8cbffc8ad6d500cfdd7635ccc68b7eadc28c387ac9b9608f463385ccc5f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 03 Aug 2023 10:01:10 GMT
RUN Install update 10.0.20348.1906
# Wed, 09 Aug 2023 23:35:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 10 Aug 2023 02:36:45 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Thu, 10 Aug 2023 02:36:46 GMT
ENV JAVA_HOME=C:\openjdk-22
# Thu, 10 Aug 2023 02:37:04 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 08 Sep 2023 19:34:04 GMT
ENV JAVA_VERSION=22-ea+14
# Fri, 08 Sep 2023 19:34:05 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk22/14/GPL/openjdk-22-ea+14_windows-x64_bin.zip
# Fri, 08 Sep 2023 19:34:06 GMT
ENV JAVA_SHA256=5a35fb7df33acaa4b3c14709a44966425b87a11c401c62e341d0fd8496cc11a8
# Fri, 08 Sep 2023 19:35:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 08 Sep 2023 19:35:03 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22a441455ace20af58f01367d769afc2b25c3db3e4a7aee67a634d14826f6f19`  
		Last Modified: Tue, 08 Aug 2023 18:20:41 GMT  
		Size: 408.8 MB (408765102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a53d0f5bc5dd4cb7976f788ee32f7195b84c7964cb22bc38a49eb55673629149`  
		Last Modified: Thu, 10 Aug 2023 00:18:32 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a18930eb7350c60f06351657db53550ff8c064f9f63673a2955eb64b696ffbd`  
		Last Modified: Thu, 10 Aug 2023 02:48:56 GMT  
		Size: 452.7 KB (452708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c00de06770671fea1af1d4340401ecedf3ab6e36133f76fd965e626275a3ef6`  
		Last Modified: Thu, 10 Aug 2023 02:48:56 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d260a183baa6941016ec79f387e49673760fd96dd3bae427fc4233c651e2046`  
		Last Modified: Thu, 10 Aug 2023 02:48:56 GMT  
		Size: 262.5 KB (262490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd71ea24262331e485899b45446ecea780534abc2d4bbec0e6dee47b9f78b06f`  
		Last Modified: Fri, 08 Sep 2023 19:39:01 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:902b729054f448b11b8b90878067a052928c71d8a020466b8404bc89aa29e44d`  
		Last Modified: Fri, 08 Sep 2023 19:39:01 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8092e25ff8095a7334965ba94241cd664e90e44fcae9bb4072c604cbe3dd13b`  
		Last Modified: Fri, 08 Sep 2023 19:39:01 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6218dc532877355508e38f38bd81bb3c76317d6c921bfd585619e80968ce200`  
		Last Modified: Fri, 08 Sep 2023 19:39:21 GMT  
		Size: 199.3 MB (199286494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b7d68875bbc0c35fa5c459d7fcb15bc2fe90f5f0d78c5fc5db6b285b96f128c`  
		Last Modified: Fri, 08 Sep 2023 19:39:01 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:22-windowsservercore` - windows version 10.0.17763.4737; amd64

```console
$ docker pull openjdk@sha256:17d5e5ade0d94afa7cf54ff445714b0d4a5175adba80b3eee10ec3a1713356ea
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2195899070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dfa8e3c38f08f7f31dd4028abef96e7ad4666b645849f615d13e9747cd42285`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 02 Aug 2023 09:07:15 GMT
RUN Install update 10.0.17763.4737
# Wed, 09 Aug 2023 23:36:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 10 Aug 2023 02:39:19 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Thu, 10 Aug 2023 02:39:21 GMT
ENV JAVA_HOME=C:\openjdk-22
# Thu, 10 Aug 2023 02:40:19 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 08 Sep 2023 19:35:18 GMT
ENV JAVA_VERSION=22-ea+14
# Fri, 08 Sep 2023 19:35:19 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk22/14/GPL/openjdk-22-ea+14_windows-x64_bin.zip
# Fri, 08 Sep 2023 19:35:20 GMT
ENV JAVA_SHA256=5a35fb7df33acaa4b3c14709a44966425b87a11c401c62e341d0fd8496cc11a8
# Fri, 08 Sep 2023 19:37:01 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 08 Sep 2023 19:37:02 GMT
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
	-	`sha256:82556c0499019c0d63fc48880317518db1b5694401f0d8420ea2c4961effcee4`  
		Last Modified: Thu, 10 Aug 2023 02:49:35 GMT  
		Size: 250.9 KB (250879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a5d5ec7e3c127f5942ff38f7f912fe583a70ebd26a2f23b08ec931d3ac747f0`  
		Last Modified: Thu, 10 Aug 2023 02:49:35 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e0adf33ca81bc87626c3e4e8e94d469cc903ac1e4cf98961cbf569e7f7662fd`  
		Last Modified: Thu, 10 Aug 2023 02:49:35 GMT  
		Size: 246.9 KB (246857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:417dd46bfffaea549d73a6c5885e74432cd563339c62e87dcb5ef769a9f00283`  
		Last Modified: Fri, 08 Sep 2023 19:39:41 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a44a772c8f038a12fc28f6f73794b4acf2552b88ed429bbbf5bb321ca552942`  
		Last Modified: Fri, 08 Sep 2023 19:39:41 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40bf6fee0aca502ea396cb95a48748ea8088d9fc6f81d3b0b4b5d56b2372f1f5`  
		Last Modified: Fri, 08 Sep 2023 19:39:41 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ee6cdc1a82051a06af3302e8a3d28a3c03f63eabd39dcfc22d45a9361c14b6`  
		Last Modified: Fri, 08 Sep 2023 19:40:02 GMT  
		Size: 199.4 MB (199437496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd78113b1b217285550765d08df7250f9c034996c3aab94bc2c5042208fbff9`  
		Last Modified: Fri, 08 Sep 2023 19:39:41 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
