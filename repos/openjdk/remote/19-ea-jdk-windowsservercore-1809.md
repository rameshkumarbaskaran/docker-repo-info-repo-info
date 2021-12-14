## `openjdk:19-ea-jdk-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:17999c1a169e390083f7df248b0eaeeb3947f0fbd8d178b3d506573009f09676
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2300; amd64

### `openjdk:19-ea-jdk-windowsservercore-1809` - windows version 10.0.17763.2300; amd64

```console
$ docker pull openjdk@sha256:8ba8dd3597ba5e3aaf56dfb847de89effb623958053e6aa0d580efd5a4f0b51d
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2891952633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f49a10516d1d79c7867cafa8fd699b971faf3ef0c5a9f51090ba4eb3a02fbcc`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Nov 2021 00:30:48 GMT
RUN Install update 1809-amd64
# Wed, 10 Nov 2021 01:42:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Nov 2021 20:25:40 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 14 Dec 2021 01:19:08 GMT
ENV JAVA_HOME=C:\openjdk-19
# Tue, 14 Dec 2021 01:20:09 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 14 Dec 2021 01:20:10 GMT
ENV JAVA_VERSION=19-ea+1
# Tue, 14 Dec 2021 01:20:11 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk19/1/GPL/openjdk-19-ea+1_windows-x64_bin.zip
# Tue, 14 Dec 2021 01:20:12 GMT
ENV JAVA_SHA256=2964c4ea8952f33b7d853c7e8c7a7535fc2b6ab560815bbd4befd0581708b944
# Tue, 14 Dec 2021 01:22:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 14 Dec 2021 01:22:02 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c1f4c7287c99b95fce227924349d1d139aceb37d97b555144bd5808935b6eab0`  
		Size: 987.8 MB (987788268 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b35c0957cca5902f3108e43a3c2c11250dc754ee0bb43900eb0719b4350f0bc2`  
		Last Modified: Wed, 10 Nov 2021 02:08:44 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db7f0affb9ccb091d200f0da9e1f9185ac51673de7fed0c7b6d5c33e7c906911`  
		Last Modified: Wed, 10 Nov 2021 21:07:09 GMT  
		Size: 358.8 KB (358799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562f1a5727d1dd40b5172bd6a2d027212ffd663762b40070df047af782a2305d`  
		Last Modified: Tue, 14 Dec 2021 01:33:20 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc5c70efa1fb33ce6999137950b2c7e0a74c5b609a4392ec720f47a6e868f313`  
		Last Modified: Tue, 14 Dec 2021 01:33:21 GMT  
		Size: 348.9 KB (348900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f8ee9760f24974387189a4a1727c5efac59c664c97988488b1cdea8d7832066`  
		Last Modified: Tue, 14 Dec 2021 01:33:18 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8db9d319530e9f813a9beebb315f07bf09e6b8f2f6c70d311de18d7ff1be0964`  
		Last Modified: Tue, 14 Dec 2021 01:33:18 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f9d269d05c178bf36d3009fa0bae32bbf7467502eb435ea0e24f9bba5c4ec46`  
		Last Modified: Tue, 14 Dec 2021 01:33:18 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e67049f65dbbd2717bdc3b19b0ed6fdbe67109e76da67d470f421cfd2acf92e8`  
		Last Modified: Tue, 14 Dec 2021 01:33:40 GMT  
		Size: 185.1 MB (185115369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6090ab12aee53f291cf7cb84ce85925526674f13bc96459a0460813ffd91945`  
		Last Modified: Tue, 14 Dec 2021 01:33:18 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
