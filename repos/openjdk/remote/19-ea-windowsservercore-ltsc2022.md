## `openjdk:19-ea-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:643540bef5e1fa62cfe688053dab2bb8987541fb296beb4f58e33c77f17690ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.524; amd64

### `openjdk:19-ea-windowsservercore-ltsc2022` - windows version 10.0.20348.524; amd64

```console
$ docker pull openjdk@sha256:e9989bd46c5a994d508258d2a07a2ccfad6071d2075eeb0737849a13851e783a
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2404417314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bb99eb22ff1a615498dca5a947cbb20a0b43be6813a665e2586bed910e99fa5`
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
# Fri, 04 Mar 2022 23:14:50 GMT
ENV JAVA_VERSION=19-ea+12
# Fri, 04 Mar 2022 23:14:51 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk19/12/GPL/openjdk-19-ea+12_windows-x64_bin.zip
# Fri, 04 Mar 2022 23:14:52 GMT
ENV JAVA_SHA256=13424e479ad28976926b63a14d003733a80cea14b863e28be122b782cdda29aa
# Fri, 04 Mar 2022 23:15:45 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 04 Mar 2022 23:15:47 GMT
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
	-	`sha256:aeb9c2c64743067196633d5b461fa4cec3cdf445805f761ab80e50302ea1c0c6`  
		Last Modified: Fri, 04 Mar 2022 23:23:20 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f5df876ba90559a405b352754937f636ccff8d0a382e63aa7f050596f63485c`  
		Last Modified: Fri, 04 Mar 2022 23:23:20 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec628ff8b75e41d580ba3166feca77f7961a9f8b5e4896a4bf168df454f33021`  
		Last Modified: Fri, 04 Mar 2022 23:23:20 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67873529a58125a774a90762948caed7a337917ec150aaa4beeef90a25f34f18`  
		Last Modified: Fri, 04 Mar 2022 23:23:41 GMT  
		Size: 188.3 MB (188335195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:369786ee233579337dc001c16376790bbb7ede12ae1de3c219625eb3a373c2b5`  
		Last Modified: Fri, 04 Mar 2022 23:23:20 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
