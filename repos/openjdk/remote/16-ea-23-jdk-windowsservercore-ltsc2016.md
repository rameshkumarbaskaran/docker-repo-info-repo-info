## `openjdk:16-ea-23-jdk-windowsservercore-ltsc2016`

```console
$ docker pull openjdk@sha256:9fba3fa302a2daedba9e48f1661783d599936c6716734f419061ae79407406fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3986; amd64

### `openjdk:16-ea-23-jdk-windowsservercore-ltsc2016` - windows version 10.0.14393.3986; amd64

```console
$ docker pull openjdk@sha256:331dba7dcf7b7fef87ebce0652f867f9d1ca2f14511e16e719a03ef90f99edb6
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5945235544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ad5383e0db6e45711d6cc8224a0eae66ee9556de1dab1fd9a0e2c5a309defe`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 02 Oct 2020 17:07:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Oct 2020 12:31:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Oct 2020 17:42:04 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force
# Wed, 14 Oct 2020 17:42:05 GMT
ENV JAVA_HOME=C:\openjdk-16
# Wed, 14 Oct 2020 17:43:23 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Fri, 06 Nov 2020 18:17:45 GMT
ENV JAVA_VERSION=16-ea+23
# Fri, 06 Nov 2020 18:17:46 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk16/23/GPL/openjdk-16-ea+23_windows-x64_bin.zip
# Fri, 06 Nov 2020 18:17:46 GMT
ENV JAVA_SHA256=43cfcadc298b570dd697c74e67886ebcaad569357e4c38d24e5d0ebaded77fb6
# Fri, 06 Nov 2020 18:20:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 06 Nov 2020 18:20:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:17a32268498b2feefa5457f0423ac15473596d514e48c694ef54d740a9a5067d`  
		Size: 1.7 GB (1671365753 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e300a13db0fbbf48a676ace9db3b0de292c825dfa01e6d82979d96ebc23d3675`  
		Last Modified: Wed, 14 Oct 2020 12:51:34 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e48f75bae068c25f8a226647b58c0be2010ed0c8cd6921bdc70e67addcbf5a03`  
		Last Modified: Wed, 14 Oct 2020 18:30:55 GMT  
		Size: 9.9 MB (9914428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:380be8c20c0be6ed94b2345de72a72dc8fa948cfb66f819ea06dbad3715e9431`  
		Last Modified: Wed, 14 Oct 2020 18:30:50 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2abbe75cd492fbd42e73733a282a661cb8caf898389b66479838c9d6a12bf93`  
		Last Modified: Wed, 14 Oct 2020 18:30:53 GMT  
		Size: 5.4 MB (5376495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e5f0fffa2690527bd85c7fbb0c815638bb7873903ccfcafde360f582cb13dfc`  
		Last Modified: Fri, 06 Nov 2020 18:26:17 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22714c20a67b41d8750a5bddf614b8d53b1e1a19e19515fa2010ca4b13858c3f`  
		Last Modified: Fri, 06 Nov 2020 18:26:17 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a8dd500e0376dede3c23d86a22312c0503a680ec7a5598310868d55d3dd4ef1`  
		Last Modified: Fri, 06 Nov 2020 18:26:16 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aee5a08177ec4b48f8931873a361bb177947351d7d7ea99f9f95a8abd2276ae`  
		Last Modified: Fri, 06 Nov 2020 18:26:38 GMT  
		Size: 188.6 MB (188586064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81749c96cc6c7b5eb1516b0dcbad71a2b604a42480fe9dccae7bde2a2e801855`  
		Last Modified: Fri, 06 Nov 2020 18:26:17 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
