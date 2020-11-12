## `openjdk:8-jre-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:2cdb5253daad01841fa32212d6a9c997fefd5663b1c3a685b640845612b6e40b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1577; amd64

### `openjdk:8-jre-windowsservercore-1809` - windows version 10.0.17763.1577; amd64

```console
$ docker pull openjdk@sha256:454a0881d85220bb74d33e2e6e5c937ddb8f649fe13682f7dae7d39599b0b68e
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2440185913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03ecd3e5cf449013495ebff0cdcbd4e54e54daa06a20babf3ab846add2e0b4ed`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 03 Nov 2020 03:11:34 GMT
RUN Install update 1809-amd64
# Wed, 11 Nov 2020 13:26:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Nov 2020 18:13:44 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 11 Nov 2020 18:14:22 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Thu, 12 Nov 2020 01:34:35 GMT
ENV JAVA_VERSION=8u275
# Thu, 12 Nov 2020 01:39:04 GMT
ENV JAVA_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u275-b01/OpenJDK8U-jre_x64_windows_8u275b01.zip
# Thu, 12 Nov 2020 01:39:47 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  java -version'; java -version; 		Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:680bbdbacf1bcbace70de5087d02d31e9dd7a22feae59f746f54dab46c1d5bda`  
		Size: 669.7 MB (669696346 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:da5a67a9f3a363cb69c8104913a5a58c1c47e8f648a07d057fc28a5f98790e60`  
		Last Modified: Wed, 11 Nov 2020 13:37:50 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:961c113008286ec10d5b5ad6712c39a4f6893491652c16952e9ad9d6182a696d`  
		Last Modified: Wed, 11 Nov 2020 18:35:15 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4485491cb68a4d866c356a328fbcaa1122d7eb2ec55323238ff04c01659a1b49`  
		Last Modified: Wed, 11 Nov 2020 18:35:26 GMT  
		Size: 9.2 MB (9234346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8be0d7b941c4cc39629a0b0f78c4aa565c0b1a7798acbfc5ec0365e62d0ea4c`  
		Last Modified: Thu, 12 Nov 2020 01:57:14 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f2c2156462c26adf9e5c781bce4bce636ac93cdd145e00d79dafb5ca633e195`  
		Last Modified: Thu, 12 Nov 2020 02:00:25 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:140202478dc068edf29123898b136ea9b4633ef2c40268f842e48a5ce283b886`  
		Last Modified: Thu, 12 Nov 2020 02:00:31 GMT  
		Size: 42.9 MB (42917707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
