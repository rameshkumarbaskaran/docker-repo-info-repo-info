## `openjdk:14-ea-32-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:554b6b16e6ddffb0571ca90b47ad22f5a1c65ae297fc5ae14e5cefea77e11c00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.973; amd64

### `openjdk:14-ea-32-windowsservercore-1809` - windows version 10.0.17763.973; amd64

```console
$ docker pull openjdk@sha256:fe5a0bfe7b35c227cfa118d9c1958a4564d3bb26a79b8af190c8fa38026d8f51
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2416432986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6ba1929fdd3c756f512bcdd6db68c1089cc520cf6d7ad112f8910ccb799bccb`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Sat, 11 Jan 2020 05:23:25 GMT
RUN Install update 1809-amd64
# Tue, 14 Jan 2020 23:46:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2020 23:47:06 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force
# Tue, 14 Jan 2020 23:58:14 GMT
ENV JAVA_HOME=C:\openjdk-14
# Tue, 14 Jan 2020 23:58:37 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Sat, 18 Jan 2020 00:23:53 GMT
ENV JAVA_VERSION=14-ea+32
# Sat, 18 Jan 2020 00:23:54 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk14/32/GPL/openjdk-14-ea+32_windows-x64_bin.zip
# Sat, 18 Jan 2020 00:23:55 GMT
ENV JAVA_SHA256=78b427c850c1245fb056a26b40e7edbd9cea01ec5aad8d70bfc2e53a540f7860
# Sat, 18 Jan 2020 00:25:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Sat, 18 Jan 2020 00:25:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:edbd72df76b46e904108d2f61a63c295b3e3d8092dbd5a03bbeb2fb4d34a3e55`  
		Size: 682.7 MB (682725872 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e9d323e253cb21832421dda4ec57dbd597bd4f934e62c162b9dec8b96e06e818`  
		Last Modified: Wed, 15 Jan 2020 01:45:20 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fe8a4080f0d1077681de059bc8597064c929d967b370eac061cacf38283adfe`  
		Last Modified: Wed, 15 Jan 2020 01:45:23 GMT  
		Size: 4.5 MB (4547614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a55aa49d97e830f6b3c864cafda1aceff84ee42dab37ddded91a28efb13412be`  
		Last Modified: Wed, 15 Jan 2020 01:55:29 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa48874f549ecadb376734cb21f5139d255704082fc0a269d8667613fa7013c8`  
		Last Modified: Wed, 15 Jan 2020 01:55:29 GMT  
		Size: 289.5 KB (289491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670c65cbd76937c66392714a2f289a14317708f3c069ec9c76ebaac38d619364`  
		Last Modified: Sat, 18 Jan 2020 00:41:51 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5d2a0837090730c3a4b566546caea9abeac5dcb63b73fbda4e823a29df4d801`  
		Last Modified: Sat, 18 Jan 2020 00:41:51 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8154c05198216d27934bf08a79927e8f2575d9535b2997cc3db860ad3295788`  
		Last Modified: Sat, 18 Jan 2020 00:41:51 GMT  
		Size: 1.2 KB (1199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6a0bdcb5ddce8da57c59fbabdc0abf42a91d83f3694fc1bcc5b157b1d3d7c53`  
		Last Modified: Sat, 18 Jan 2020 00:42:20 GMT  
		Size: 194.2 MB (194177532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf60aea71c0b66cd47766ae70c4933d3e07de5825aa9536ccd5153dfa4115b7`  
		Last Modified: Sat, 18 Jan 2020 00:41:51 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
