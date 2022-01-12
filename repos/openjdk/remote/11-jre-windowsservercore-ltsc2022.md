## `openjdk:11-jre-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:4cc4745cfe679c83a8f396cbfc33f36c64cf4b2b0801cf6871a6a8c9bef76988
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.469; amd64

### `openjdk:11-jre-windowsservercore-ltsc2022` - windows version 10.0.20348.469; amd64

```console
$ docker pull openjdk@sha256:da29e82279be5aaab1553be14a6480b30c9efead81d6023bc507afe87f7919b9
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2248878421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb264efe4f1e1e5bf9a320ee715ea603c8cbcd0880871589dcf20cc0c526f401`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
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
# Wed, 12 Jan 2022 05:38:47 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 12 Jan 2022 05:39:08 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 12 Jan 2022 05:39:09 GMT
ENV JAVA_VERSION=11.0.13
# Wed, 12 Jan 2022 05:47:26 GMT
ENV JAVA_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_x64_windows_11.0.13_8.zip
# Wed, 12 Jan 2022 05:48:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
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
	-	`sha256:a7411817cd433c58455bba3bbb1cbe34398c0aab3b4975bf6e9ace2e3cd1406d`  
		Last Modified: Wed, 12 Jan 2022 23:12:23 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e45a967717a5e96a5851000141a69ca5bf8111f9cfbe506c5bcc3ecd757c4d`  
		Last Modified: Wed, 12 Jan 2022 23:12:22 GMT  
		Size: 551.6 KB (551580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9b1a91a5c28e77d60b97dbd305026b619ce5b6fc1bca2d6ccb79d558471e477`  
		Last Modified: Wed, 12 Jan 2022 23:12:21 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:273e16a784b1c3f8d58e5cf57f92f3f0ad74e010536ccc2e3ee3cf77c31fce3e`  
		Last Modified: Wed, 12 Jan 2022 23:15:18 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29366269b9f6fe518b42ee57ac0cb77772be1eb2c28ca763efd3cb9f97092eee`  
		Last Modified: Wed, 12 Jan 2022 23:15:27 GMT  
		Size: 40.0 MB (39975445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
