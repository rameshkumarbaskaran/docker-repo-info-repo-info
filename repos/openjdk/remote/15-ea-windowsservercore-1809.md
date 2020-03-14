## `openjdk:15-ea-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:b424d338ea21f4f0530ec22e49132a78303bf4fbed8f70df2d96cbfb52e9ac61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `openjdk:15-ea-windowsservercore-1809` - windows version 10.0.17763.1098; amd64

```console
$ docker pull openjdk@sha256:603d6758a35cae0c31e1e9b1d9e0e5e9c5d81abf545dfa94c0eb913c11cbc213
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2463946274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f195f115122531d2e4757a66cf7450d66977f125c3a1e11f2def8b3aa78b4d87`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 06 Mar 2020 11:12:29 GMT
RUN Install update 1809-amd64
# Wed, 11 Mar 2020 00:42:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Mar 2020 14:53:20 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force
# Wed, 11 Mar 2020 14:53:21 GMT
ENV JAVA_HOME=C:\openjdk-15
# Wed, 11 Mar 2020 14:53:45 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Fri, 13 Mar 2020 21:30:33 GMT
ENV JAVA_VERSION=15-ea+14
# Fri, 13 Mar 2020 21:30:34 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk15/14/GPL/openjdk-15-ea+14_windows-x64_bin.zip
# Fri, 13 Mar 2020 21:30:35 GMT
ENV JAVA_SHA256=411989eacb4772fbec0f334fbb94ab162b5abb91fd3a677892c09c15083f1e01
# Fri, 13 Mar 2020 21:32:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 13 Mar 2020 21:32:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23645bd7ee0885911e1e2ab55ebcb36ce35795e1ceba9166ffd1b26dde18c3ee`  
		Size: 730.7 MB (730650958 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a7fab05ac5ad4b2f665ad71b5c08a81e82bff7ea2fdcbb66c14193d2dd268875`  
		Last Modified: Wed, 11 Mar 2020 01:16:21 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a4f86b1e9c271e3e0e37ceb96d7c9042f35b463aef0323a7ca7d3166be8163b`  
		Last Modified: Wed, 11 Mar 2020 15:25:11 GMT  
		Size: 4.7 MB (4659035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:252d80eee5b49917fa28f0aa282593137be5d7dd4c9fd863164226d8f099d9fa`  
		Last Modified: Wed, 11 Mar 2020 15:25:05 GMT  
		Size: 1.2 KB (1194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a29727e0a8d494510a0c0cad18a44647ecb6cf968e13fac178f7a42d802bb625`  
		Last Modified: Wed, 11 Mar 2020 15:25:07 GMT  
		Size: 289.6 KB (289584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8a5566847a7b1bee76ac1d82f01435d6ddc3c33db47e660cb4a7b7daf151a9`  
		Last Modified: Fri, 13 Mar 2020 22:08:34 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fb345f46c96b752b7af43bf2276665fcc321d13a3c666cccdbbd9ff4a2cbb14`  
		Last Modified: Fri, 13 Mar 2020 22:08:34 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3360376008a7f1e5551d931353941bcbb153f2e0486869dbe966a5c9a9c5dc62`  
		Last Modified: Fri, 13 Mar 2020 22:08:34 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c300d815f9d07abc656fe2220477d30f1fba70d8f6612f17b0ad1a87fe4ceec`  
		Last Modified: Fri, 13 Mar 2020 22:09:12 GMT  
		Size: 193.7 MB (193654530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5000631e76fb9742af50fe5fe6fc3744ea733d735530193348d422a0674a9274`  
		Last Modified: Fri, 13 Mar 2020 22:08:34 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
