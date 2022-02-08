## `openjdk:19-ea-jdk-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:f407d22a42aea707c80f444bfc0a157f18e567f2c3bcb6a65414dcc5d0e29b57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2458; amd64

### `openjdk:19-ea-jdk-windowsservercore-1809` - windows version 10.0.17763.2458; amd64

```console
$ docker pull openjdk@sha256:cacead43cc807629b0e5ea15cb5a1b0a74837914d5014284df724d1ede89a834
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2899295796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d37073ef28e2daad42e78124740f491af4d8f68d57bf54cbeaebae8f6aa255da`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 18 Jan 2022 01:52:23 GMT
RUN Install update 1809-amd64
# Wed, 19 Jan 2022 23:21:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 19 Jan 2022 23:23:41 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 19 Jan 2022 23:23:42 GMT
ENV JAVA_HOME=C:\openjdk-19
# Wed, 19 Jan 2022 23:24:43 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 08 Feb 2022 02:17:44 GMT
ENV JAVA_VERSION=19-ea+8
# Tue, 08 Feb 2022 02:17:45 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk19/8/GPL/openjdk-19-ea+8_windows-x64_bin.zip
# Tue, 08 Feb 2022 02:17:46 GMT
ENV JAVA_SHA256=eba519024733a2420e4c45145f4995121a1612f2dc875c1d37b0b87b69d563c2
# Tue, 08 Feb 2022 02:19:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 08 Feb 2022 02:19:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:567fd00846e9a9f44eea5925b497356dda00fe89b8335d2a3b2a8b9d84b0bb69`  
		Size: 995.0 MB (994988595 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba7b1090ce9545f6aac90d390785f6c5e3846304cb7596289dfc36c169d7b1da`  
		Last Modified: Thu, 20 Jan 2022 00:40:41 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98c73c8d54eeae51e9c93499966b4413ea63f218bdf175bed7b7d83c76e6d58`  
		Last Modified: Thu, 20 Jan 2022 02:20:37 GMT  
		Size: 357.3 KB (357347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64554bb59fd3345200ae4e79426f465295d19e9d1be31e0f5a60f5ddc13af5b2`  
		Last Modified: Thu, 20 Jan 2022 02:20:37 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec53942b6c9dd8e8c55c8a2268d1a09a715d75e3edcf063826fa7462dcdb7c2`  
		Last Modified: Thu, 20 Jan 2022 02:20:37 GMT  
		Size: 310.5 KB (310471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb93382399dbf19897266c16425c40ec4bef7b27f3687373cb3221e8ae0d2c13`  
		Last Modified: Tue, 08 Feb 2022 03:24:42 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0825b2736c6f8d9e43eabd301cf7658b87ba942d59cf0352d35aa753b43bb8f7`  
		Last Modified: Tue, 08 Feb 2022 03:24:42 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da30a4a85393397b050a1f427f830ea9c9af09508b82c05fde395ac3358e76a5`  
		Last Modified: Tue, 08 Feb 2022 03:24:42 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6f5a55378c92d153ee53021f7a1ad85250278a448407d8777e0b901cb768162`  
		Last Modified: Tue, 08 Feb 2022 03:27:56 GMT  
		Size: 185.3 MB (185297980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eeba1d031806eed5264fb70e38b9ed8eddbe6d21f13fa6f872e84994abb4118`  
		Last Modified: Tue, 08 Feb 2022 03:24:42 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
