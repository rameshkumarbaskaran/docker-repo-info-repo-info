## `openjdk:19-windowsservercore-ltsc2016`

```console
$ docker pull openjdk@sha256:d33f192b1a72b17ccc7aebb329bb0e96274adfede651b6267bc64a75fee72d85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.14393.4825; amd64

### `openjdk:19-windowsservercore-ltsc2016` - windows version 10.0.14393.4825; amd64

```console
$ docker pull openjdk@sha256:bd168d30936e1d90bfcdd3c7613a45b439c04c46d8bf830bf2b8da977b41f7ba
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 GB (6460495478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:929bd24df10911641c6167c530855e8f893ea6175e079ab1b49681e6cc340630`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 08 Dec 2021 08:38:00 GMT
RUN Install update ltsc2016-amd64
# Sat, 18 Dec 2021 00:22:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 18 Dec 2021 06:59:56 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Sat, 18 Dec 2021 06:59:58 GMT
ENV JAVA_HOME=C:\openjdk-19
# Sat, 18 Dec 2021 07:01:04 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 27 Dec 2021 19:03:35 GMT
ENV JAVA_VERSION=19-ea+3
# Mon, 27 Dec 2021 19:03:36 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk19/3/GPL/openjdk-19-ea+3_windows-x64_bin.zip
# Mon, 27 Dec 2021 19:03:37 GMT
ENV JAVA_SHA256=f36c3877bce15485798362efa5043564eda9265027dfb7b42a219fa5659ecda3
# Mon, 27 Dec 2021 19:05:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 27 Dec 2021 19:05:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2d026d646213ccf73d9f0584941d108253d62e73df2a74e070776884b7b0242b`  
		Size: 2.2 GB (2204728802 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7756a7a3024dbbb7cabda3151e8f8461ae808ae2ad3857f0c9235c5908ff7695`  
		Last Modified: Sat, 18 Dec 2021 01:22:26 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f88306d11f630889687486bb566861161592f87bc40ac9850fce316e5b7780`  
		Last Modified: Sat, 18 Dec 2021 10:55:53 GMT  
		Size: 335.8 KB (335827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:156b98596a6a205c44cb60ec59ad014ee89440f058f3461f521ffc899670dc95`  
		Last Modified: Sat, 18 Dec 2021 10:55:53 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52478147df3d18fbcb95a25b68742ff25cdb15025a1d754d61d54486c9151339`  
		Last Modified: Sat, 18 Dec 2021 10:55:53 GMT  
		Size: 329.4 KB (329409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:699ba066a89da3636f9f02637973f5c39d8360bde81a064b8b394d22ef059afd`  
		Last Modified: Mon, 27 Dec 2021 20:22:34 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e097e7dbc349aa35b784b37ca72ffa42a57b0b5abb2b7a50c9d08b34963ba5e`  
		Last Modified: Mon, 27 Dec 2021 20:22:34 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f5d79ab6adc5753acbee7f04c2a1cf08803bddde9f2bcb9762188b262f8efa1`  
		Last Modified: Mon, 27 Dec 2021 20:22:34 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c937be2e7a816fa747caa5d9a0eb73f3593ad7aea97a7982b287df50de56a368`  
		Last Modified: Mon, 27 Dec 2021 20:25:51 GMT  
		Size: 185.1 MB (185107033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5a0e3c56868ab16447c718131e63ed616a222d5f3cc4cc64bc507871623ca9e`  
		Last Modified: Mon, 27 Dec 2021 20:22:34 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
