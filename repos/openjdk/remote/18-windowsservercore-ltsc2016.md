## `openjdk:18-windowsservercore-ltsc2016`

```console
$ docker pull openjdk@sha256:7f673fb145678b77d05e0a7ae9cff80a795f713cf5e1f4d8604c63dc8cb4f9ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4467; amd64

### `openjdk:18-windowsservercore-ltsc2016` - windows version 10.0.14393.4467; amd64

```console
$ docker pull openjdk@sha256:ba26699441ec2781faf5e55206c211f986e9afbf7f4e754825e676192f941611
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 GB (6454155731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bae36771cc08aaaeaeb5559fbd82c89de0143bb74ece5e6c6ada61c0e27f75e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Sun, 06 Jun 2021 15:37:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 09 Jun 2021 12:41:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Jun 2021 16:48:43 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 14 Jun 2021 21:17:21 GMT
ENV JAVA_HOME=C:\openjdk-18
# Mon, 14 Jun 2021 21:18:50 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 22 Jun 2021 21:19:15 GMT
ENV JAVA_VERSION=18-ea+2
# Tue, 22 Jun 2021 21:19:18 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk18/2/GPL/openjdk-18-ea+2_windows-x64_bin.zip
# Tue, 22 Jun 2021 21:19:20 GMT
ENV JAVA_SHA256=4f7a1b71a31a48a04127d3ef3d6838e2316e77a9f70e5aa291b5deeb7f6f2181
# Tue, 22 Jun 2021 21:21:40 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 22 Jun 2021 21:21:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2f52abeee6d6f4a925ad418b5e6200d4fca9bf92834ffc918b8bbaccd34251db`  
		Size: 2.2 GB (2195741359 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c82e82e95dbad4ccc260b42e03767eb07222e2f00ec57a69b3c87b17da1d2fd3`  
		Last Modified: Wed, 09 Jun 2021 13:04:25 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:030344af2a85aa48f4c1eb2866fe22830344ab5752d72cb3dec80e7234b68523`  
		Last Modified: Wed, 09 Jun 2021 17:24:45 GMT  
		Size: 343.9 KB (343868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ef266ecd06b083d74179f9d3e3d91c9ad296f394dc2c59fa7dab6646ad2c199`  
		Last Modified: Mon, 14 Jun 2021 21:38:19 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff084f0476eb537ee80cec72e601223378ca547aade81fd1195ce0a97c65e82e`  
		Last Modified: Mon, 14 Jun 2021 21:38:20 GMT  
		Size: 315.6 KB (315577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f50fa0e24a8e0fde4fceea4e765855cffbbec67e46a31923cb4c6539a94b953`  
		Last Modified: Tue, 22 Jun 2021 21:33:18 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7687c1b05720170040653ac19c083b0338152318684c9b72929c78ef9e5a07c1`  
		Last Modified: Tue, 22 Jun 2021 21:33:18 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65df17e81a9f9c2a0137d4709f99a441bec8350d216b776f624dccdfa2cfefd1`  
		Last Modified: Tue, 22 Jun 2021 21:33:18 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0427a5440c8708f0206e5d5b75e1416a7cf70a15a3d9845b79e31962134fb3b4`  
		Last Modified: Tue, 22 Jun 2021 21:37:02 GMT  
		Size: 187.8 MB (187760543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33984550d3187f46c837875b7f62ab08daa7b6aee7989ea4e2e75d1f1e5ca44c`  
		Last Modified: Tue, 22 Jun 2021 21:33:18 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
