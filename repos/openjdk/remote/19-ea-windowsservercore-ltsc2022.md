## `openjdk:19-ea-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:ce3c2519590c252171059cd106978fc830b8f072a462ade1b565e8f432e63b7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.524; amd64

### `openjdk:19-ea-windowsservercore-ltsc2022` - windows version 10.0.20348.524; amd64

```console
$ docker pull openjdk@sha256:7078b06dae4c85356419f98141ebeed5a36a1c2d566fe94695895dbffcb47102
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2401627252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:140d4ffd99199e328d7ad84c182f84dd1610c94ce8403c6e1179372aa3662970`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Tue, 01 Feb 2022 02:49:40 GMT
RUN Install update ltsc2022-amd64
# Wed, 09 Feb 2022 13:37:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Feb 2022 18:40:17 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 09 Feb 2022 18:40:18 GMT
ENV JAVA_HOME=C:\openjdk-19
# Wed, 09 Feb 2022 18:40:37 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 21 Feb 2022 18:15:52 GMT
ENV JAVA_VERSION=19-ea+10
# Mon, 21 Feb 2022 18:15:53 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk19/10/GPL/openjdk-19-ea+10_windows-x64_bin.zip
# Mon, 21 Feb 2022 18:15:54 GMT
ENV JAVA_SHA256=8b23bdf0ea67df0996ec5adb192319e5cbf205be6d9750bf1a2050fedd1e7d1f
# Mon, 21 Feb 2022 18:16:47 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 21 Feb 2022 18:16:49 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:898469748ff68223ab87b654b29fb366c1f4f2b7cfad7a37426346ea16db8dfa`  
		Size: 963.2 MB (963225591 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7062696b7aef1ca33afdf32084a532f7e3151a844eb7cb2455bcc907e0f42a58`  
		Last Modified: Wed, 09 Feb 2022 14:28:27 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16fc5298c05f3e14d89c86be0ac333bd8cfa150ada3565e9f2736c19d8cac25b`  
		Last Modified: Wed, 09 Feb 2022 19:16:25 GMT  
		Size: 616.4 KB (616433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21971a484cbb6138250125b67d62f83b05a4770a5da18e51e7b3ac8e5743e725`  
		Last Modified: Wed, 09 Feb 2022 19:16:24 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0be28f1a2b136367cb8f8044ec174a09f9976e0f389c7fe25cd4e12f2e59b5a`  
		Last Modified: Wed, 09 Feb 2022 19:16:25 GMT  
		Size: 532.5 KB (532549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e7bba71359c096711083a080b0e02cbfdcbc87b1388a3d8f31bfa692f879d64`  
		Last Modified: Mon, 21 Feb 2022 19:20:44 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b7bc01e38f2ff2287838d6ce45071cfd115fd25af05fe4f1df9173b701585f0`  
		Last Modified: Mon, 21 Feb 2022 19:20:44 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bab58cf2c013e9cca680e813141f39bb4fcb82e970f9df4a13f0db58522f53c`  
		Last Modified: Mon, 21 Feb 2022 19:20:44 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05018027bc11da085c9a1779967f22b3abff18d41b58a6c4bea0c6bb6f70fcf`  
		Last Modified: Mon, 21 Feb 2022 19:21:06 GMT  
		Size: 185.5 MB (185545579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f04ea330a10cc8d9ef8f9a0c2338456ae904b4e6b9d2c516215077781d54f3`  
		Last Modified: Mon, 21 Feb 2022 19:20:44 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
