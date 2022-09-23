## `openjdk:20-ea-jdk-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:c0179a9a3b911dd576677d72a6b8241087cfbc797d253bc88e4a7b7321c95a1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3406; amd64

### `openjdk:20-ea-jdk-windowsservercore-1809` - windows version 10.0.17763.3406; amd64

```console
$ docker pull openjdk@sha256:5c53956a954dca1ca47f884d082677e88dc870443499bcb1858e7a9e076aed67
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2896435677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:525eecf37f31ff4236467182c3bef5a858e58d5943f071ef63a66ff4c85d99ad`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Fri, 09 Sep 2022 22:43:02 GMT
RUN Install update 10.0.17763.3406
# Tue, 13 Sep 2022 18:21:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Sep 2022 17:06:13 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 14 Sep 2022 17:06:14 GMT
ENV JAVA_HOME=C:\openjdk-20
# Wed, 14 Sep 2022 17:07:14 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 23 Sep 2022 00:34:44 GMT
ENV JAVA_VERSION=20-ea+16
# Fri, 23 Sep 2022 00:34:45 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk20/16/GPL/openjdk-20-ea+16_windows-x64_bin.zip
# Fri, 23 Sep 2022 00:34:46 GMT
ENV JAVA_SHA256=665cdc1485e5c1a63c6e90ea867f085376180321c8b2c576aa9c92ae05f0c9a9
# Fri, 23 Sep 2022 00:36:25 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 23 Sep 2022 00:36:26 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:cee64bf279e2ca8e924884a10ecb98bfa79c7f0cc8d25e73039b9aeb940815b6`  
		Size: 826.4 MB (826398623 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2bc395c8c47e61e593d2e905e0e051d40e7d25e4aeac7dbe08d3ec57acd0e68f`  
		Last Modified: Tue, 13 Sep 2022 18:25:24 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58648929570c8439cbc01e98ebc75618cbe96e946d332763402b53d89cc5639b`  
		Last Modified: Wed, 14 Sep 2022 17:22:14 GMT  
		Size: 349.5 KB (349457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f69dd72d8573f685284949ad83177bf75e72c3d8275d35aa6b4d21f5a480f2b9`  
		Last Modified: Wed, 14 Sep 2022 17:22:14 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59bfc5f723418de82847d7f0e86272a0dc2ec14263a42be94649cbc3d219420b`  
		Last Modified: Wed, 14 Sep 2022 17:22:14 GMT  
		Size: 311.8 KB (311834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a2a5b177fa5ffb8fa2b39b604af627ffe18a555e3e6b3d9828163c299cbbd1e`  
		Last Modified: Fri, 23 Sep 2022 00:39:41 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c128c61bbbbcf029bafb52a61c3be83a3537e53a409d544bd74197fa804e37bc`  
		Last Modified: Fri, 23 Sep 2022 00:39:41 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:353566d8b89bbbe3a6376c324a3edcee5cfcbcb8179c544773f6bee3b2cbf799`  
		Last Modified: Fri, 23 Sep 2022 00:39:41 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95c90286ec5d82155bcd14e43e5e8870837980cee8e2183f832363bbefe9f98a`  
		Last Modified: Fri, 23 Sep 2022 00:39:59 GMT  
		Size: 192.2 MB (192201187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c158264f676c35071ba7c53818d1c60728650c923bbe0b4e99c1d598492dd2b0`  
		Last Modified: Fri, 23 Sep 2022 00:39:41 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
