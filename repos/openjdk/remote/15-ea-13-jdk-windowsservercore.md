## `openjdk:15-ea-13-jdk-windowsservercore`

```console
$ docker pull openjdk@sha256:6b1ece34d59558be1cd7af83f629e175ab49723c0b97aa8f3b79b0ebf3e5f702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64
	-	windows version 10.0.14393.3506; amd64

### `openjdk:15-ea-13-jdk-windowsservercore` - windows version 10.0.17763.1098; amd64

```console
$ docker pull openjdk@sha256:ba11278bd12debe800422f13974db1a29b6df19ef514449ac27d44d102541d20
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2463913836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eba8bd16c88b53e3feb0a2a7bf7ee07d21841774a259647ed6fc515277f1e53c`
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
# Wed, 11 Mar 2020 14:53:46 GMT
ENV JAVA_VERSION=15-ea+13
# Wed, 11 Mar 2020 14:53:47 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk15/13/GPL/openjdk-15-ea+13_windows-x64_bin.zip
# Wed, 11 Mar 2020 14:53:48 GMT
ENV JAVA_SHA256=2b3f4cbe9268a82f740264ce81dd085d92d562f5519c50f87f0c785ab2d668b7
# Wed, 11 Mar 2020 14:55:57 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 11 Mar 2020 14:56:00 GMT
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
	-	`sha256:2c4a108e0a37456b31f9078d95216fe50b9058e4a3dbaee5df638b9d5a171e4c`  
		Last Modified: Wed, 11 Mar 2020 15:25:00 GMT  
		Size: 1.2 KB (1205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8258a235d7706cd95d13cbfed163c06841613749a23172e0c028f313032b1bbc`  
		Last Modified: Wed, 11 Mar 2020 15:25:01 GMT  
		Size: 1.2 KB (1217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55d30aa1c2b2994fc4367cf22f0c551e51e81255fb945a15a7cc33ab867b3329`  
		Last Modified: Wed, 11 Mar 2020 15:25:01 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c847286d076959399e9125360fccc988b291b8c3dad5418a7bf3beb58f65ff5b`  
		Last Modified: Wed, 11 Mar 2020 15:25:38 GMT  
		Size: 193.6 MB (193621741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e325c57c594d2c586b9c83d5acb8e68eb1b393ece54ea7ed8530b6c909beb103`  
		Last Modified: Wed, 11 Mar 2020 15:25:01 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:15-ea-13-jdk-windowsservercore` - windows version 10.0.14393.3506; amd64

```console
$ docker pull openjdk@sha256:3c3c1121e7acf589a5e9fff38d72b95a79afa0b02260d27d20eb45b542ace6fc
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5940972460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c54d811fd29c9ade149e281f38efe9fbc09fb0c218dfbe24a259e304cea5327c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 14 Feb 2020 21:42:00 GMT
RUN Install update ltsc2016-amd64
# Thu, 20 Feb 2020 01:48:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 20 Feb 2020 01:49:57 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force
# Thu, 20 Feb 2020 01:49:59 GMT
ENV JAVA_HOME=C:\openjdk-15
# Thu, 20 Feb 2020 01:51:47 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Fri, 06 Mar 2020 22:17:12 GMT
ENV JAVA_VERSION=15-ea+13
# Fri, 06 Mar 2020 22:17:13 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk15/13/GPL/openjdk-15-ea+13_windows-x64_bin.zip
# Fri, 06 Mar 2020 22:17:15 GMT
ENV JAVA_SHA256=2b3f4cbe9268a82f740264ce81dd085d92d562f5519c50f87f0c785ab2d668b7
# Fri, 06 Mar 2020 22:20:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 06 Mar 2020 22:20:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:846a2223e9e7a88a2a07d706553f144d380483d72fb9f0697c4fcd71773a8693`  
		Size: 1.7 GB (1657079102 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:72c4471958f7f0f07260f0f430bcffb0bc07811088c24cffba1439d250ea1ae3`  
		Last Modified: Thu, 20 Feb 2020 03:04:52 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f6eada8556f1688b8cc14a7529ed2bd5822b6570a73c142f15a023eda1563d9`  
		Last Modified: Thu, 20 Feb 2020 03:04:58 GMT  
		Size: 5.4 MB (5361808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7ce35a0aa37afd4baa3b9058c4be764cc458f70c6849a36a7aaa50e6707e6b2`  
		Last Modified: Thu, 20 Feb 2020 03:04:52 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bfc5a4ac5c33ba6e40369cbdb81f258c11758ec88b55da5560b114a6fc2ec2a`  
		Last Modified: Thu, 20 Feb 2020 03:04:55 GMT  
		Size: 5.3 MB (5341588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:988c6250d45a138f0fb0db7e36cce0792f0732b49f9a65393283bd8af5047a08`  
		Last Modified: Fri, 06 Mar 2020 22:30:26 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e3762ca2ef82f74a64c8a6067c72ef8a83685d1fd0c2fceecd0475c3d92046`  
		Last Modified: Fri, 06 Mar 2020 22:30:26 GMT  
		Size: 1.2 KB (1226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10a2acec192d9ff10338a76566e7fbcf0cbe6897157a5f9128c35af3510419f4`  
		Last Modified: Fri, 06 Mar 2020 22:30:26 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:003aae430b442b4ed730f7a965f758c126ae938d5b3f672fae458281858127c5`  
		Last Modified: Fri, 06 Mar 2020 22:31:07 GMT  
		Size: 203.2 MB (203196854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52423e3a07b55737ec2164ab8feb9aa22e9ec7815ad3e10d6a513077f82bf711`  
		Last Modified: Fri, 06 Mar 2020 22:30:26 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
