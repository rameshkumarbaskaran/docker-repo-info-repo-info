## `openjdk:21-ea-26-windowsservercore`

```console
$ docker pull openjdk@sha256:659feaaf107ac12de16c146275bd48015393a714b85611329ed283dbe4a20e78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1787; amd64
	-	windows version 10.0.17763.4499; amd64

### `openjdk:21-ea-26-windowsservercore` - windows version 10.0.20348.1787; amd64

```console
$ docker pull openjdk@sha256:626b7dc74f2a7c619656eb52c917f24591257e5f13b8aefe7d891ca993f3d677
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1587386970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4b1aec85c6b4d787afc3ab8e363ac50f1b509d4f1ca8c26839efd533066c8a7`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 14 Jun 2023 17:38:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Jun 2023 20:24:17 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 14 Jun 2023 20:28:58 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 14 Jun 2023 20:29:22 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 14 Jun 2023 20:29:23 GMT
ENV JAVA_VERSION=21-ea+26
# Wed, 14 Jun 2023 20:29:24 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk21/26/GPL/openjdk-21-ea+26_windows-x64_bin.zip
# Wed, 14 Jun 2023 20:29:25 GMT
ENV JAVA_SHA256=1dc7aa62631ee8f9e91346529b41bb40764c9f0dd9192b24e52a1c19ce3cda65
# Wed, 14 Jun 2023 20:30:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 14 Jun 2023 20:30:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0972ddd233121a2afd2cf1a3eaec49d595cfe6b3ebe19ef3dd492d99784c370f`  
		Last Modified: Wed, 14 Jun 2023 18:17:55 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ecf7cfdecc4064a3b0d43346d08171233c7f384d58889a6b8710f45b5c57a9`  
		Last Modified: Wed, 14 Jun 2023 20:33:59 GMT  
		Size: 318.3 KB (318286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ebbdd7b332be16a3a5df77e0a2c4d72833fdacc6a2cab0bd336093650ded15a`  
		Last Modified: Wed, 14 Jun 2023 20:35:53 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a57ea6f3fe157301ffb86456c425db57163025371e05b4c02e81c1d7e25d56`  
		Last Modified: Wed, 14 Jun 2023 20:35:53 GMT  
		Size: 263.4 KB (263355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d6b362712f23c5b8b9ba70d1625a461acb37cfc62b54583f9d0b6a5b2a8d303`  
		Last Modified: Wed, 14 Jun 2023 20:35:51 GMT  
		Size: 1.4 KB (1385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5601443477475989b8d62fb36bf7227f6476869f40de947e4a5f04d1514ff0ff`  
		Last Modified: Wed, 14 Jun 2023 20:35:51 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:415265825b6f23060c315897e1f437838eb480564f101e0df41b056a8ba37158`  
		Last Modified: Wed, 14 Jun 2023 20:35:51 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ebee822b7494d4b7a13dea4f869c8d318ab5d2a278f75763c028e8a636d8860`  
		Last Modified: Wed, 14 Jun 2023 20:36:11 GMT  
		Size: 198.2 MB (198198383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c647721252a14f943856288064be6caa12dddb668cba75eb42875ff402f8f87`  
		Last Modified: Wed, 14 Jun 2023 20:35:51 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:21-ea-26-windowsservercore` - windows version 10.0.17763.4499; amd64

```console
$ docker pull openjdk@sha256:4d8dca55384e11b26827ca16f8fb5baef46a692f36adabc68a0e54abc11a1d60
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1849401235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:482e29c2b9b71b4799c3f46596ceb4a378a6ca998f8ab09585c20388ba87fa65`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 14 Jun 2023 17:39:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Jun 2023 20:26:18 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 14 Jun 2023 20:30:26 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 14 Jun 2023 20:30:53 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 14 Jun 2023 20:30:54 GMT
ENV JAVA_VERSION=21-ea+26
# Wed, 14 Jun 2023 20:30:55 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk21/26/GPL/openjdk-21-ea+26_windows-x64_bin.zip
# Wed, 14 Jun 2023 20:30:55 GMT
ENV JAVA_SHA256=1dc7aa62631ee8f9e91346529b41bb40764c9f0dd9192b24e52a1c19ce3cda65
# Wed, 14 Jun 2023 20:31:53 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 14 Jun 2023 20:31:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b712a9a082fd391beaa9ca7c8e6c3fda37b0ad8d29cc4663173ed973b961d342`  
		Last Modified: Wed, 14 Jun 2023 18:21:55 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1119c9dd4674cbb889b8cd01bbadf4652797b89d882f89be398f7da1beb24c70`  
		Last Modified: Wed, 14 Jun 2023 20:34:37 GMT  
		Size: 305.5 KB (305458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caf3365db6b1a5459442fd3a01aed321cab7afcea801751a10a37b6254119aed`  
		Last Modified: Wed, 14 Jun 2023 20:36:31 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:290d337ba15ee034e320e3aab54554a46b97bd5b2abd5b4eabcb81b98112a665`  
		Last Modified: Wed, 14 Jun 2023 20:36:31 GMT  
		Size: 257.3 KB (257292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e76bbe8068ce7883ff4f0d8c9074c3c8583b3a558550b38a85e3ba0662457fa`  
		Last Modified: Wed, 14 Jun 2023 20:36:29 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad799f6a869c57ea122f9753d423ce3bd981cfe43bc97602c8a4a664b50a31c1`  
		Last Modified: Wed, 14 Jun 2023 20:36:29 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad716b54b493d9f05458b6455d8eefdcc244742209c54548f7dd4e29db7bd052`  
		Last Modified: Wed, 14 Jun 2023 20:36:29 GMT  
		Size: 1.4 KB (1447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:905f5e971f82f438b9819c08a6e1371bcfba94a77945fab6d29dec7fd38c1d48`  
		Last Modified: Wed, 14 Jun 2023 20:36:49 GMT  
		Size: 198.2 MB (198209633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d81749d739d8a77afdab5d406ec60a801383b8ceec7438a691dd6880878dcff5`  
		Last Modified: Wed, 14 Jun 2023 20:36:29 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
