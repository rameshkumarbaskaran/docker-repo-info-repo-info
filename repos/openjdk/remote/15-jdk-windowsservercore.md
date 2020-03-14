## `openjdk:15-jdk-windowsservercore`

```console
$ docker pull openjdk@sha256:99087212e033e682e8bffb09275feb4a939aec402b2b6bb103445e54dd758388
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64
	-	windows version 10.0.14393.3568; amd64

### `openjdk:15-jdk-windowsservercore` - windows version 10.0.17763.1098; amd64

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

### `openjdk:15-jdk-windowsservercore` - windows version 10.0.14393.3568; amd64

```console
$ docker pull openjdk@sha256:396ef6b02e2e121478b805f4ad085e95405aa8c73fc46b8c0381d7e773ff9629
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5938208091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0fd455f7a863c1f36857b008a4a64ab14fd215072ccfb3e1cd9ccdd499489d6`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 10 Mar 2020 08:14:00 GMT
RUN Install update ltsc2016-amd64
# Fri, 13 Mar 2020 21:32:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 13 Mar 2020 21:34:16 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force
# Fri, 13 Mar 2020 21:34:18 GMT
ENV JAVA_HOME=C:\openjdk-15
# Fri, 13 Mar 2020 21:35:43 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Fri, 13 Mar 2020 21:35:44 GMT
ENV JAVA_VERSION=15-ea+14
# Fri, 13 Mar 2020 21:35:46 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk15/14/GPL/openjdk-15-ea+14_windows-x64_bin.zip
# Fri, 13 Mar 2020 21:35:47 GMT
ENV JAVA_SHA256=411989eacb4772fbec0f334fbb94ab162b5abb91fd3a677892c09c15083f1e01
# Fri, 13 Mar 2020 21:38:37 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 13 Mar 2020 21:38:40 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a5d20b7a2294a0d2631f74f49fc34574484a692913559546ef0bceae789fd7a8`  
		Size: 1.7 GB (1658775203 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f08cc5bf7287bc1d8f72edfe2439c99210e433230a22fc73264fcf1685850ed2`  
		Last Modified: Fri, 13 Mar 2020 22:09:47 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25aa1b0ee68c69a66d5b4e6cdfd989815b485cf3988dd548e162f4772304f990`  
		Last Modified: Fri, 13 Mar 2020 22:09:51 GMT  
		Size: 5.4 MB (5380002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2edec803117173fae9526bf71d284db81781cff2f4e22fcf4cfabda2cf59f17a`  
		Last Modified: Fri, 13 Mar 2020 22:09:42 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adaa5169033250eb57d65694775263fcc1ccf51cd49794ba272552675d61c9bb`  
		Last Modified: Fri, 13 Mar 2020 22:09:48 GMT  
		Size: 5.4 MB (5357722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cff841a6c1efb673d21977bddbc31030dbf54877e0d6f6f3323e159005866497`  
		Last Modified: Fri, 13 Mar 2020 22:09:36 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fcbff29a9d05d1cb09450305cbc2de5dfc7ecbb454edd933d02e652e4de28b0`  
		Last Modified: Fri, 13 Mar 2020 22:09:36 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f843c8b4dec3125c31a706c0731ceaa7633d13388998402f1caa22daa34dfd84`  
		Last Modified: Fri, 13 Mar 2020 22:09:36 GMT  
		Size: 1.2 KB (1215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0411487b67f5c4349ebd073f7bd47e878c33e9e3bda756383ba0bb1846b4909a`  
		Last Modified: Fri, 13 Mar 2020 22:10:24 GMT  
		Size: 198.7 MB (198702200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a428392c53e1de3f13623aa7179a8f62bbdfcded1c6b6ac682a148e0c3667756`  
		Last Modified: Fri, 13 Mar 2020 22:09:36 GMT  
		Size: 1.2 KB (1198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
