## `openjdk:21-ea-windowsservercore`

```console
$ docker pull openjdk@sha256:5b728a909d20dd334c7a8c41dba1d91eb1ddf0853222ac2d881ea2ca137ec86c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1607; amd64
	-	windows version 10.0.17763.4131; amd64

### `openjdk:21-ea-windowsservercore` - windows version 10.0.20348.1607; amd64

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

### `openjdk:21-ea-windowsservercore` - windows version 10.0.17763.4131; amd64

```console
$ docker pull openjdk@sha256:1d114dee182fb721e841d8e1214c752f27719cc4310b151b28ec2ceb87331f90
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2209040204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:709b7e4cea81710026bc2fd24fc1e3fd9550e7e1b6d13b302e2aafc66bd51546`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Sat, 11 Mar 2023 10:37:22 GMT
RUN Install update 10.0.17763.4131
# Thu, 16 Mar 2023 00:41:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Mar 2023 04:17:49 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Thu, 16 Mar 2023 04:17:50 GMT
ENV JAVA_HOME=C:\openjdk-21
# Thu, 16 Mar 2023 04:19:13 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Thu, 16 Mar 2023 04:19:15 GMT
ENV JAVA_VERSION=21-ea+13
# Thu, 16 Mar 2023 04:19:17 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk21/13/GPL/openjdk-21-ea+13_windows-x64_bin.zip
# Thu, 16 Mar 2023 04:19:19 GMT
ENV JAVA_SHA256=243e8681ce473d4c13a7aed22eb2109685da552776c021b415457445426cf659
# Thu, 16 Mar 2023 04:21:10 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Thu, 16 Mar 2023 04:21:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a92048040b3b13af10f8287baabaddbb2759dfc77b1fb43f89b38b3275467f93`  
		Last Modified: Thu, 16 Mar 2023 01:42:29 GMT  
		Size: 305.6 MB (305565048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec8e4e0836091bdd33e8adb56d1e13b8096550727a20534e2a2ab9298c86fa09`  
		Last Modified: Thu, 16 Mar 2023 01:41:16 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6954ad7da48d4dd7acf8132bc41996dfcd7f157b30b2ca35ec4814ffc26a94d3`  
		Last Modified: Thu, 16 Mar 2023 04:31:25 GMT  
		Size: 480.4 KB (480436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8087e24b23846aed99e303ff6d5268f444daecd74c150fb70198dabc16487141`  
		Last Modified: Thu, 16 Mar 2023 04:31:25 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2836db1b10d5ae1b6c026b5fc8f9667c86fafa8854926472e99f786aea1aaf7f`  
		Last Modified: Thu, 16 Mar 2023 04:31:25 GMT  
		Size: 309.7 KB (309740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffbd7ea47105215573da90b3bafe7dd19a846735b3a7c1436e279d3b015eb3b1`  
		Last Modified: Thu, 16 Mar 2023 04:31:22 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5251add5ebfb1c096c2162a9207db660c9d8c0c9207445751468f32ff3a1909`  
		Last Modified: Thu, 16 Mar 2023 04:31:22 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e7e227675dc8b1909d3ec222acf56f387729ef8f47c5f2c79710e9e9b6a846c`  
		Last Modified: Thu, 16 Mar 2023 04:31:22 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1fc5408285b06502fd58d03edea27af559ef0ab1d0b2b8acbaf408631fa5c7b`  
		Last Modified: Thu, 16 Mar 2023 04:31:46 GMT  
		Size: 194.7 MB (194732573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8aa9be5ff1c8c819d49da8f40ddd42792061c6a41a22fafc4e4861778e439d3`  
		Last Modified: Thu, 16 Mar 2023 04:31:22 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
