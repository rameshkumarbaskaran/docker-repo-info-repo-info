## `openjdk:21-ea-13-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:506d444e8c825793935834e5f3e175249038ae1ac35c3588d4c06f9b8062bbaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1607; amd64

### `openjdk:21-ea-13-windowsservercore-ltsc2022` - windows version 10.0.20348.1607; amd64

```console
$ docker pull openjdk@sha256:438087a5091e0f2723974dcebeb9d8b27f32c42556a5701e61e8a85e0025b38a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1910182675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee13099e1bbc2899029e5993fe8d1506f9e569c91d15b217b17a577ad6c27deb`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Fri, 10 Mar 2023 06:37:36 GMT
RUN Install update 10.0.20348.1607
# Thu, 16 Mar 2023 00:38:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Mar 2023 04:14:25 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Thu, 16 Mar 2023 04:14:26 GMT
ENV JAVA_HOME=C:\openjdk-21
# Thu, 16 Mar 2023 04:14:53 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Thu, 16 Mar 2023 04:14:55 GMT
ENV JAVA_VERSION=21-ea+13
# Thu, 16 Mar 2023 04:14:56 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk21/13/GPL/openjdk-21-ea+13_windows-x64_bin.zip
# Thu, 16 Mar 2023 04:14:57 GMT
ENV JAVA_SHA256=243e8681ce473d4c13a7aed22eb2109685da552776c021b415457445426cf659
# Thu, 16 Mar 2023 04:16:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Thu, 16 Mar 2023 04:16:02 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c921d7eac594f5e3ce3ef10adb8fd0f71bdbb713c4854336b995d25f89c44d42`  
		Last Modified: Thu, 16 Mar 2023 01:41:04 GMT  
		Size: 327.9 MB (327911088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bca4593035ae0e8d1b6e6eb1b053fddc6a6824b28f45f99de726d752d2c0f72`  
		Last Modified: Thu, 16 Mar 2023 01:39:50 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9232261c30bc22ec57212f386e8fea077a0775299f58234bfec01a611d98144`  
		Last Modified: Thu, 16 Mar 2023 04:30:43 GMT  
		Size: 736.0 KB (736009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:545d4a9e39b1cc7dac0d42fb0a331c120f1bfed624e7850e1faa4eb99110ce01`  
		Last Modified: Thu, 16 Mar 2023 04:30:43 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8063d1ae112267a681a9e7feb4d398e107825072b3fd2b95b3bad2efc8571978`  
		Last Modified: Thu, 16 Mar 2023 04:30:43 GMT  
		Size: 538.0 KB (538004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f09bdc56459352322c826ed14553f9e359f6ed98ba0111830b199661b4786f0`  
		Last Modified: Thu, 16 Mar 2023 04:30:41 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c404ff4f032997386c9524934ca9b6f7c6d644f78fefb6500d89e1973c5af01c`  
		Last Modified: Thu, 16 Mar 2023 04:30:41 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dc9fd43ba88a587127f177e6f6043e4c31ef4630982d7ac067f8f38959f9c8c`  
		Last Modified: Thu, 16 Mar 2023 04:30:41 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a91583104a6da61febe99b0badaf9ec6ce89423975fb57d78883f94baf0a73df`  
		Last Modified: Thu, 16 Mar 2023 04:31:04 GMT  
		Size: 195.0 MB (194960068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae756af42aac2b30d3ca07b0ad1383dc83c952dcce26b4326883e81f4415a42`  
		Last Modified: Thu, 16 Mar 2023 04:30:41 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
