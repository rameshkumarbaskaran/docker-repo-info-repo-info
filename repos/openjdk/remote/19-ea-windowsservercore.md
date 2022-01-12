## `openjdk:19-ea-windowsservercore`

```console
$ docker pull openjdk@sha256:722091c2e2a27c70aaa049671429327abbb6ca86f502bf5feb5572bfce64c668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.20348.469; amd64
	-	windows version 10.0.17763.2452; amd64
	-	windows version 10.0.14393.4886; amd64

### `openjdk:19-ea-windowsservercore` - windows version 10.0.20348.469; amd64

```console
$ docker pull openjdk@sha256:2e1562014fc4c3fed5559daa29936977f8c9e0664dc2423aef30990a61991c87
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2394270359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72c71647ba6bbe35385b926bac7e138520dffdf92baf9083a40d2f6f0beaf21b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Thu, 06 Jan 2022 03:56:33 GMT
RUN Install update ltsc2022-amd64
# Tue, 11 Jan 2022 18:59:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Jan 2022 05:09:49 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 12 Jan 2022 05:09:50 GMT
ENV JAVA_HOME=C:\openjdk-19
# Wed, 12 Jan 2022 05:10:09 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 12 Jan 2022 05:10:10 GMT
ENV JAVA_VERSION=19-ea+4
# Wed, 12 Jan 2022 05:10:11 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk19/4/GPL/openjdk-19-ea+4_windows-x64_bin.zip
# Wed, 12 Jan 2022 05:10:12 GMT
ENV JAVA_SHA256=d76667c6d142d73576ea27adc9849ccd7f116011bbb4f22c7f0a76635d3a2901
# Wed, 12 Jan 2022 05:11:10 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 12 Jan 2022 05:11:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:9b593686e27e7562a5b0696823307ffa822214cee8bd2eec1075eadad4cb9712`  
		Size: 956.0 MB (956001983 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:99e0b71ede60d3b2c5b9053bf27e47c0875590991eede49813d849cc660c7551`  
		Last Modified: Tue, 11 Jan 2022 19:32:06 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c42ce1d7b7857ac1eb8d4fbf9579f07cf6a89ed47f3a0979451365d92324f699`  
		Last Modified: Wed, 12 Jan 2022 22:55:59 GMT  
		Size: 644.8 KB (644784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3aff587b21f31d2c01622cca482ab4ce1034e72ec67fe0a67894e20119fc654`  
		Last Modified: Wed, 12 Jan 2022 22:55:58 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b01c57c266a512234c3cad7efd226645be4c579a3d14e556c78c5aa280c06f2`  
		Last Modified: Wed, 12 Jan 2022 22:55:59 GMT  
		Size: 551.5 KB (551450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39723ecca756aeb7ff1c172bc833a42ee65c24010d6c0395167e777158158831`  
		Last Modified: Wed, 12 Jan 2022 22:55:56 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46abaa599120b54bad069c2d33b1fbe0f45fc8b7c7306e6b66fd7dd47a12d14b`  
		Last Modified: Wed, 12 Jan 2022 22:55:56 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65afed6c38928bb44b52e033e7c96d1b575f302bb2f49f07669610c6078abca6`  
		Last Modified: Wed, 12 Jan 2022 22:55:55 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ba3e8fe055e2eca37b02993ae0385d6c878f868991687720ca48e8ad3e5ed0`  
		Last Modified: Wed, 12 Jan 2022 22:56:20 GMT  
		Size: 185.4 MB (185364683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3315ad1f1bac7627b5759f0aa8dabba315dabc90c6bbecbcf9bc09f539ad3b2e`  
		Last Modified: Wed, 12 Jan 2022 22:55:56 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:19-ea-windowsservercore` - windows version 10.0.17763.2452; amd64

```console
$ docker pull openjdk@sha256:a24fd523934bc40159400928c6cf9e20f416fb4e8003600117f85c59e7a2a467
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2898007981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0191d3c6481a7f15355c9786f47d27b2afa02c18dc4382591a346d183a611259`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 07 Jan 2022 22:48:13 GMT
RUN Install update 1809-amd64
# Wed, 12 Jan 2022 05:11:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Jan 2022 05:12:35 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 12 Jan 2022 05:12:36 GMT
ENV JAVA_HOME=C:\openjdk-19
# Wed, 12 Jan 2022 05:13:44 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 12 Jan 2022 05:13:45 GMT
ENV JAVA_VERSION=19-ea+4
# Wed, 12 Jan 2022 05:13:47 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk19/4/GPL/openjdk-19-ea+4_windows-x64_bin.zip
# Wed, 12 Jan 2022 05:13:48 GMT
ENV JAVA_SHA256=d76667c6d142d73576ea27adc9849ccd7f116011bbb4f22c7f0a76635d3a2901
# Wed, 12 Jan 2022 05:15:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 12 Jan 2022 05:15:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:635f15ebd5b486e8a00bf217a0574a29550e5bbf08c1d021e1e308100b2e49b5`  
		Size: 993.9 MB (993898043 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3a70d5fd54e2005efbf590b48700ed40509210354a0d8f3f18c3b444a5325896`  
		Last Modified: Wed, 12 Jan 2022 06:20:33 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d74f00c66c11971de2e35204e3f42aca9ac77b3dba4dcd545130bea41c91fd27`  
		Last Modified: Wed, 12 Jan 2022 22:56:55 GMT  
		Size: 346.0 KB (345951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327ffaefff991cf2fe273931958209ea8e54093032ace7748ca229ad6be7a66d`  
		Last Modified: Wed, 12 Jan 2022 22:56:54 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26fc100c3d9f2f8260f46a4a1aff08f3c8a0d9fd5f1ce2319b7d30e73018d3e`  
		Last Modified: Wed, 12 Jan 2022 22:56:54 GMT  
		Size: 302.7 KB (302659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59ceeff8dddf63e3e495cb34d9e16fe5b34fc5947f972cf05edf631d5c58c67`  
		Last Modified: Wed, 12 Jan 2022 22:56:51 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:274de986412e28424ad2eed344316ba3916ba1062ce47fd712e1fba489cbe7ad`  
		Last Modified: Wed, 12 Jan 2022 22:56:52 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44dc5334dfe8c1bb305700ad1e08d6cb780ba597b83fc4581195fda06909b853`  
		Last Modified: Wed, 12 Jan 2022 22:56:51 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87f2d0b75b36ecda928adcc18e2370d5cb36002f23936c010a7550410acc4d95`  
		Last Modified: Wed, 12 Jan 2022 22:57:14 GMT  
		Size: 185.1 MB (185120034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0292033a5384c759476361cc952ccde74b2772ef48b6bfa20f719e31668cabd8`  
		Last Modified: Wed, 12 Jan 2022 22:56:51 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:19-ea-windowsservercore` - windows version 10.0.14393.4886; amd64

```console
$ docker pull openjdk@sha256:b9f74e4947af75a7cf29985f4142a26bceaf9636aaa1104095c844466f979ff8
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 GB (6464019523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05a5e2337778d60653970e22ea03566ac1bd4a173f3a02b696fedd89d1e364f6`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Thu, 06 Jan 2022 14:33:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 11 Jan 2022 19:14:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Jan 2022 05:16:55 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 12 Jan 2022 05:16:56 GMT
ENV JAVA_HOME=C:\openjdk-19
# Wed, 12 Jan 2022 05:17:54 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 12 Jan 2022 05:17:55 GMT
ENV JAVA_VERSION=19-ea+4
# Wed, 12 Jan 2022 05:17:56 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk19/4/GPL/openjdk-19-ea+4_windows-x64_bin.zip
# Wed, 12 Jan 2022 05:17:57 GMT
ENV JAVA_SHA256=d76667c6d142d73576ea27adc9849ccd7f116011bbb4f22c7f0a76635d3a2901
# Wed, 12 Jan 2022 05:19:35 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 12 Jan 2022 05:19:38 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8428508ffd63b4af1ba690ec41e82a116f10ec6c3fb70962348f5448d42e5835`  
		Size: 2.2 GB (2208216859 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:9b5116c05ddf6ecb5a348f7628e3f3264afbb9909d86798316dbaff4a0e991a2`  
		Last Modified: Tue, 11 Jan 2022 19:35:13 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a804249f990290da306f883f1e85db00728eaab29aa4bd99a9833b830cb158`  
		Last Modified: Wed, 12 Jan 2022 22:57:37 GMT  
		Size: 340.9 KB (340850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1a166e2bba795aac696ff3563d536ae8b9e620a881ad8ef15daa5dec49611e4`  
		Last Modified: Wed, 12 Jan 2022 22:57:36 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b185a5b66ed7026042ee7bad546a5ee3bf4fab35305bb73da8f7fb352d5e8943`  
		Last Modified: Wed, 12 Jan 2022 22:57:37 GMT  
		Size: 333.9 KB (333850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071ecb23b8db1f19f7d0e651db8a2c61adf9e3b6d06b89ace44bce3951ebf511`  
		Last Modified: Wed, 12 Jan 2022 22:57:34 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea44292bff5c92988dd9b8db2c8e339c218af92aac22ae9298d2ba524a6a03e2`  
		Last Modified: Wed, 12 Jan 2022 22:57:34 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f9d025e445df9dcffd7253bdecc54d49aa30ab5710c7356ec0e8d0d22b934ce`  
		Last Modified: Wed, 12 Jan 2022 22:57:34 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6af6d1db9c5b6c3fdecf75b2fe5afd6dbbae0a27dbc1cd37ffcbce6a6568629`  
		Last Modified: Wed, 12 Jan 2022 23:01:02 GMT  
		Size: 185.1 MB (185133598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9fce3bbded9639d189763d8a003d63c853a84ee04730b08cb8dbaa9ca3a7b37`  
		Last Modified: Wed, 12 Jan 2022 22:57:34 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
