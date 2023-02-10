## `openjdk:20-ea-35-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:0fd18e0e53da8f4247a11070b5d29869d7e91fd795cc38762d7af4dc99687dc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1487; amd64

### `openjdk:20-ea-35-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.1487; amd64

```console
$ docker pull openjdk@sha256:4bbea1c1b4fde4862e7479595cade1588119b62353a51db3278cafdf26f3ce09
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1580869005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e9802037bfcae647eebe147a34e58d2a1ea69e27f40f5348bc9b97cf842eac3`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Thu, 12 Jan 2023 01:40:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Jan 2023 05:07:34 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Thu, 12 Jan 2023 05:12:21 GMT
ENV JAVA_HOME=C:\openjdk-20
# Thu, 12 Jan 2023 05:12:42 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 10 Feb 2023 02:31:58 GMT
ENV JAVA_VERSION=20-ea+35
# Fri, 10 Feb 2023 02:31:59 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk20/35/GPL/openjdk-20-ea+35_windows-x64_bin.zip
# Fri, 10 Feb 2023 02:32:00 GMT
ENV JAVA_SHA256=8108ccc7d3f76d5cfc4a799d30970bdb046ae906e871c70a37f86399624cad89
# Fri, 10 Feb 2023 02:33:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 10 Feb 2023 02:33:07 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa41f3a43cc9e40e953b9cfe1530c27eed49cf79cdae96e9dfc39b04a1b75ecf`  
		Last Modified: Thu, 12 Jan 2023 02:29:45 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aa8e5b91e3c425a756945d0dec251c1595992592fd0dcf4df0ec0a7962717eb`  
		Last Modified: Thu, 12 Jan 2023 05:22:24 GMT  
		Size: 614.6 KB (614563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e473ae08f0a0a264ab6f873890549b89c65b8bdb708438338c229d6bb80f4084`  
		Last Modified: Thu, 12 Jan 2023 05:24:23 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c6f6e1b656f7612da0ef96aa76c88ddb66ccc536e23899b449c43784f4ba0bd`  
		Last Modified: Thu, 12 Jan 2023 05:24:23 GMT  
		Size: 552.6 KB (552562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59211941694fabf035a5983699198b6a942068ff12e2d6337cb92ae067771f39`  
		Last Modified: Fri, 10 Feb 2023 08:21:35 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:028263bf980db9bf8c9bc292a9d3898f58839ae7d7b4e03f7a31a858eaf8b439`  
		Last Modified: Fri, 10 Feb 2023 08:21:35 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f63ee4f6a20d09452f999c511462951af39d88b3528dca133ec1f50d27da3c7`  
		Last Modified: Fri, 10 Feb 2023 08:21:35 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9b2f5996c3a8fbe56b03513df7034ddd986f176e54ea0d47a5c85c754b2ccee`  
		Last Modified: Fri, 10 Feb 2023 08:21:59 GMT  
		Size: 193.7 MB (193664337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e92828611d3e94b84351fc9e4067c99ced79dd3736b23f7a30b97b2955eec9b`  
		Last Modified: Fri, 10 Feb 2023 08:21:35 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
