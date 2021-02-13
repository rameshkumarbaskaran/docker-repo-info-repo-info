## `openjdk:17-ea-jdk-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:deec70b0435bed66997b377d1e27084abdffe818da94ca02eaf9268a10c97121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1757; amd64

### `openjdk:17-ea-jdk-windowsservercore-1809` - windows version 10.0.17763.1757; amd64

```console
$ docker pull openjdk@sha256:7efb2058b19a74e0cc76d91e95953f7ce24570d9170e1e971535c5afcd83c165
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2634791066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05c0dc319b883755bdb9ff964dcb1d03851295528eacbf5302c965c17c75bff3`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Sat, 06 Feb 2021 05:03:14 GMT
RUN Install update 1809-amd64
# Wed, 10 Feb 2021 13:14:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Feb 2021 16:39:44 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 10 Feb 2021 16:39:45 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 10 Feb 2021 16:40:04 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 12 Feb 2021 23:15:15 GMT
ENV JAVA_VERSION=17-ea+9
# Fri, 12 Feb 2021 23:15:16 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk17/9/GPL/openjdk-17-ea+9_windows-x64_bin.zip
# Fri, 12 Feb 2021 23:15:17 GMT
ENV JAVA_SHA256=616961fd8286b02167951f1d802bbd9ec3448ea8b9e148c204f778741e73f22a
# Fri, 12 Feb 2021 23:16:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 12 Feb 2021 23:16:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:db4edcf0861ff3fdc41851a5a218965ecb2ab6cf4ec9448fb80cc4b6792fd46c`  
		Size: 720.9 MB (720933935 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:433d24156d44dde3b3c6c0094ba5824a315286ae537c68f272e464fc426510f6`  
		Last Modified: Wed, 10 Feb 2021 13:40:44 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9fdb3b9c58e6d398b7f6c8c351559fc536c4ad21618a63035a7223b88bd65f`  
		Last Modified: Wed, 10 Feb 2021 17:16:08 GMT  
		Size: 9.4 MB (9416675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f54c8c307aa58138a691da27e184aae054ccca2438544a5c65c7ebfc71b4d08`  
		Last Modified: Wed, 10 Feb 2021 17:16:05 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:162a0c2432ae95365715187c3e2691a5006fa137d82bc3e70d40e9fb49e11e06`  
		Last Modified: Wed, 10 Feb 2021 17:16:07 GMT  
		Size: 318.6 KB (318567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23638ebc36c7258e9936c309ea54c4153378ba51aae42fae05855f3ac396913b`  
		Last Modified: Fri, 12 Feb 2021 23:28:47 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55fd4c1d290982b9892a89c99ce2a9029ef28f6494d5bd77c66736b898dbb991`  
		Last Modified: Fri, 12 Feb 2021 23:28:47 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c458d1cde8ff848a9f1643f354ae636bb494719ba8ea03140090ebe9d523a7cc`  
		Last Modified: Fri, 12 Feb 2021 23:28:47 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:920249958751be821bf992d672bcaead122f069bd940f6b5b2591b0382729a11`  
		Last Modified: Fri, 12 Feb 2021 23:29:07 GMT  
		Size: 185.8 MB (185780706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9dfed17b926fd1dfe9886a3ca57b08852755c16be54d7a9a644f51ba9c42ac8`  
		Last Modified: Fri, 12 Feb 2021 23:28:47 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
