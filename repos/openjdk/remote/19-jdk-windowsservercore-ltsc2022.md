## `openjdk:19-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:ed907b9debf74a16c365ec1bf95df22bfa5585de65810dcbe983236d9e705af9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.350; amd64

### `openjdk:19-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.350; amd64

```console
$ docker pull openjdk@sha256:da6505385755d01c0b138749f8468e247022a0e70bbc77af740023b4870cd5a1
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2371091215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea71b10f47c8859670098feefc24e199eac64c30b9f9706aa25f6cee2a7821e2`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Wed, 03 Nov 2021 08:36:33 GMT
RUN Install update ltsc2022-amd64
# Wed, 10 Nov 2021 01:38:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Nov 2021 20:23:23 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 14 Dec 2021 01:17:41 GMT
ENV JAVA_HOME=C:\openjdk-19
# Tue, 14 Dec 2021 01:18:05 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 14 Dec 2021 01:18:06 GMT
ENV JAVA_VERSION=19-ea+1
# Tue, 14 Dec 2021 01:18:07 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk19/1/GPL/openjdk-19-ea+1_windows-x64_bin.zip
# Tue, 14 Dec 2021 01:18:08 GMT
ENV JAVA_SHA256=2964c4ea8952f33b7d853c7e8c7a7535fc2b6ab560815bbd4befd0581708b944
# Tue, 14 Dec 2021 01:18:57 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 14 Dec 2021 01:18:59 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a0eb404f1860fa8786ad09d1d9fe9fd580115f83cd38623bc4eb0c46abdaa0a3`  
		Size: 932.9 MB (932907933 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:27ded59d7006d9d7bffa7c253cd04a900a5d6b0d47b84d0edd624d12fd64cdc9`  
		Last Modified: Wed, 10 Nov 2021 02:07:39 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbc4afb60e31b5cebc49ca0785c802982ffcb26a35cbf45cb86cfacf57f997ea`  
		Last Modified: Wed, 10 Nov 2021 21:03:27 GMT  
		Size: 616.5 KB (616541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2745077586923de46911fd1f185c702ade6653b6ded1010d3f22f20ea65b67ea`  
		Last Modified: Tue, 14 Dec 2021 01:32:39 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bca060a561d6e0b81f8d52bdffa7471df8335ee474e6b8bde603f499272a6c65`  
		Last Modified: Tue, 14 Dec 2021 01:32:39 GMT  
		Size: 545.8 KB (545752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2fe60a41df8e15fc527bf0cdcc25be4a51793c2ca64a49ab16b333733a749c4`  
		Last Modified: Tue, 14 Dec 2021 01:32:36 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99f83dc373482ff26488add728ea27dc9979a199f925bae767fdbcab2c075885`  
		Last Modified: Tue, 14 Dec 2021 01:32:36 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3172b558aff8fbb3eb84b9324ee617436d96f36ee9b1af0b5881f8875f660a7`  
		Last Modified: Tue, 14 Dec 2021 01:32:36 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73a8beded1d8d5e49933907237987580c3e080f2578ab8432defe50b83efaabf`  
		Last Modified: Tue, 14 Dec 2021 01:32:58 GMT  
		Size: 185.3 MB (185313956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b76005fb30ae0c44d36f45525414b4aba8485accc94bbd778405813f0d8fe49a`  
		Last Modified: Tue, 14 Dec 2021 01:32:36 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
