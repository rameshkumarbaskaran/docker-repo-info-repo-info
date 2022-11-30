## `openjdk:20-ea-25-windowsservercore`

```console
$ docker pull openjdk@sha256:9291f6c350764840866617709319ca375af5676b90e902bda33159ec4d0d43ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1249; amd64
	-	windows version 10.0.17763.3650; amd64

### `openjdk:20-ea-25-windowsservercore` - windows version 10.0.20348.1249; amd64

```console
$ docker pull openjdk@sha256:3df89eaefe724290cec7b3740b599920c56599c9f3d68e29ba4d0544bf822677
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2676414865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab6e3e484bc88a32c6be9a48241e7bd49eb5e821472baea938a0a8759a0e852e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Sat, 05 Nov 2022 07:49:25 GMT
RUN Install update 10.0.20348.1249
# Tue, 08 Nov 2022 18:28:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Nov 2022 17:20:09 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 09 Nov 2022 17:20:10 GMT
ENV JAVA_HOME=C:\openjdk-20
# Wed, 09 Nov 2022 17:20:37 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 30 Nov 2022 21:14:25 GMT
ENV JAVA_VERSION=20-ea+25
# Wed, 30 Nov 2022 21:14:27 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk20/25/GPL/openjdk-20-ea+25_windows-x64_bin.zip
# Wed, 30 Nov 2022 21:14:28 GMT
ENV JAVA_SHA256=df1ddb21754991ae2d94d337d63701b99322e13c3418a6a2d19fe33097cc76d6
# Wed, 30 Nov 2022 21:15:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 30 Nov 2022 21:15:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a4aee932fccc1ec8135f290aca03a7c93dcc2536fc84723813ef9b95f6fd13ea`  
		Last Modified: Wed, 18 May 2022 07:59:24 GMT  
		Size: 1.5 GB (1473997635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e276673195ed11807395b0da51ac20ef31c925ce955c29ad1bab54f14617c25b`  
		Last Modified: Tue, 08 Nov 2022 19:41:53 GMT  
		Size: 1.0 GB (1007770983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3becc14271944025e3fa6c2ef2689bdfbf09bfc54ec339115d3082df315898e4`  
		Last Modified: Tue, 08 Nov 2022 19:38:57 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f5ce72a05e01b629001eb0ff2b493ddf6cd8e3c7a836607dc83cfbbec299b3`  
		Last Modified: Wed, 09 Nov 2022 17:35:31 GMT  
		Size: 614.7 KB (614677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:766f89a2f9cf276bf435dc9be37e180dfcfc54b750ca8cca41b1e0673eb95abe`  
		Last Modified: Wed, 09 Nov 2022 17:35:30 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3329d7d902a4cde0c4f3848690267bd771e713ccee926c04fc723e62ad0105e8`  
		Last Modified: Wed, 09 Nov 2022 17:35:31 GMT  
		Size: 546.1 KB (546089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7f0cdf1ac4b1d7a6f023b9d4aea447a67c261103faeef91ee31fc08e9ca204`  
		Last Modified: Wed, 30 Nov 2022 21:21:44 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37f173048dda3b9a57055e0f9ea603ea32cbccaefa4ea13ac300b8977d081bdd`  
		Last Modified: Wed, 30 Nov 2022 21:21:44 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d35529e832cef08cb67620e93e0a08180a8354bfaed4bf790b9de83c77d58a3`  
		Last Modified: Wed, 30 Nov 2022 21:21:44 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:687700bc6c0f3b2c831d0cb6968d2ebfc9ebdedc226022f4c823586218d146ab`  
		Last Modified: Wed, 30 Nov 2022 21:22:05 GMT  
		Size: 193.5 MB (193476898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c4726862895f57064881ff1bc18228da34617e555fad0a4434b8aa30d1410a9`  
		Last Modified: Wed, 30 Nov 2022 21:21:44 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:20-ea-25-windowsservercore` - windows version 10.0.17763.3650; amd64

```console
$ docker pull openjdk@sha256:0c2141aada33f3bbbb80f7895c1c5b3f5234dcc9c1a01ca81d1f6a4a8f78bdb5
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (2972553846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c767c7fed9d09bf025fbca06303de7786ea386f1dcfc93177797cb066419f5b9`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 05 Nov 2022 18:29:26 GMT
RUN Install update 10.0.17763.3650
# Tue, 08 Nov 2022 18:31:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Nov 2022 17:23:18 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 09 Nov 2022 17:23:19 GMT
ENV JAVA_HOME=C:\openjdk-20
# Wed, 09 Nov 2022 17:24:31 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 30 Nov 2022 21:16:10 GMT
ENV JAVA_VERSION=20-ea+25
# Wed, 30 Nov 2022 21:16:11 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk20/25/GPL/openjdk-20-ea+25_windows-x64_bin.zip
# Wed, 30 Nov 2022 21:16:12 GMT
ENV JAVA_SHA256=df1ddb21754991ae2d94d337d63701b99322e13c3418a6a2d19fe33097cc76d6
# Wed, 30 Nov 2022 21:18:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 30 Nov 2022 21:18:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a48a3e4ae2de839d8e99bde16eb91d113fb2cf889bba472d0c4274851b5fb402`  
		Last Modified: Tue, 21 Jun 2022 18:30:17 GMT  
		Size: 1.9 GB (1924269350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26cc6e4f9eb1ae415a5ead6f884cac597bbd57efa6cd042c878d5b54c9d2091`  
		Last Modified: Tue, 08 Nov 2022 19:44:35 GMT  
		Size: 854.3 MB (854317461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f182832ad6ad5ea3d4b7320fd7bfea56fb9cf8413be904e52db6ed14c8d9e36f`  
		Last Modified: Tue, 08 Nov 2022 19:42:07 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c85372c7985a34aa1619da07364507356666af5e2f073a7a04b171c25354b4a`  
		Last Modified: Wed, 09 Nov 2022 17:36:18 GMT  
		Size: 364.8 KB (364807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2c5944c42080bba06b7004a16754ffff768c5ce0b7b3c895891f0f4efe6ef6`  
		Last Modified: Wed, 09 Nov 2022 17:36:17 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e29b6097f3b07473eb77be3c0d8c63285a498161914a045d403afd73a63e73`  
		Last Modified: Wed, 09 Nov 2022 17:36:18 GMT  
		Size: 321.6 KB (321605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36bec8f5193acd31771698e7552a7ed48ef151b47b7cec7f3cfb70af139e1606`  
		Last Modified: Wed, 30 Nov 2022 21:22:23 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f12daec212300bcec63a2c45697808940d28a853aa69f187074034cf0d819e4`  
		Last Modified: Wed, 30 Nov 2022 21:22:23 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f198a8d852e3b4c73a33a267bbd45fb5af5470268a722a0ab5c11b6bedbc338d`  
		Last Modified: Wed, 30 Nov 2022 21:22:24 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e156ae0f96607e963a388ec35fc819691d26580fe1db72c3fca25924c676dac2`  
		Last Modified: Wed, 30 Nov 2022 21:22:44 GMT  
		Size: 193.3 MB (193272202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9602846ce5948dad6a4eb710cb4fca7ca99bb66b12e2e410a5ec1eebb76ac1fe`  
		Last Modified: Wed, 30 Nov 2022 21:22:23 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
