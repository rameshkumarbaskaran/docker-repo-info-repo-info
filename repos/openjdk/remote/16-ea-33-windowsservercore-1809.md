## `openjdk:16-ea-33-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:d6bda7e49ef5400c82d8edd0a9bf6ddc5bd874da4e995cd33f160dbaa5940557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1697; amd64

### `openjdk:16-ea-33-windowsservercore-1809` - windows version 10.0.17763.1697; amd64

```console
$ docker pull openjdk@sha256:6e632178663e22738c4b170027c7be892b9dd193cfc77b0385f6ebeb475f8b95
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2630210509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dd83af993ec63bc4435f9545a7a2982aa774c5d25010e9b20a70720ca5ac180`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 08 Jan 2021 08:50:52 GMT
RUN Install update 1809-amd64
# Wed, 13 Jan 2021 13:13:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Jan 2021 19:49:01 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force
# Wed, 13 Jan 2021 19:58:29 GMT
ENV JAVA_HOME=C:\openjdk-16
# Wed, 13 Jan 2021 19:58:52 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Sat, 23 Jan 2021 01:20:58 GMT
ENV JAVA_VERSION=16-ea+33
# Sat, 23 Jan 2021 01:20:59 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk16/33/GPL/openjdk-16-ea+33_windows-x64_bin.zip
# Sat, 23 Jan 2021 01:21:00 GMT
ENV JAVA_SHA256=b1f3c41d34eb15946fe1fe5793ed38705a41d6b76612319913be9d677ad0b24c
# Sat, 23 Jan 2021 01:22:33 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Sat, 23 Jan 2021 01:22:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4dcc9a9b9e680514ef3fdfcc2ce08a3768f9e412703faa137f4a7c8297600052`  
		Size: 717.4 MB (717439216 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e00081a98bb2679c3c5f469e09d475980133a20987f9cae4cf4f7aedf59f9d8f`  
		Last Modified: Wed, 13 Jan 2021 13:17:19 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:095bdf2ec48c97c5c3f23fd49bb117d66d72f8b46f5707f3c1b77227c6ca013e`  
		Last Modified: Wed, 13 Jan 2021 21:11:37 GMT  
		Size: 9.4 MB (9362296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e10056d427e3b5e74ec86dfc8d857b8486abe1baf0ad334f69237291a4ef1d1f`  
		Last Modified: Wed, 13 Jan 2021 21:17:32 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74ef5af7a200bb8cd051f06886340e50cddbfcfcb4e7332e1796c7d0f851f04`  
		Last Modified: Wed, 13 Jan 2021 21:17:31 GMT  
		Size: 297.7 KB (297727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dc7eeeeb5d9dd4636a5f78441b904fbd772d19ee1bc4d25c7261366edb10179`  
		Last Modified: Sat, 23 Jan 2021 01:37:06 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5beffe642f7f8fe3deb8dbe15529177718dbf856dc813c7236992aaaf24748b0`  
		Last Modified: Sat, 23 Jan 2021 01:37:05 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afc267cfa8462debf1c2ff894fc2b3ac6464ca651ab0786cd65ec0221af128aa`  
		Last Modified: Sat, 23 Jan 2021 01:37:05 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e29ea452569e40f0824566175d62a67afe73cc0c74dffee96e81d7f648c91c5`  
		Last Modified: Sat, 23 Jan 2021 01:40:39 GMT  
		Size: 184.8 MB (184770657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d17436a69096d61e11782956af791a30c9ff8fc961fcf76949d2b0ffb5ea961`  
		Last Modified: Sat, 23 Jan 2021 01:37:12 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
