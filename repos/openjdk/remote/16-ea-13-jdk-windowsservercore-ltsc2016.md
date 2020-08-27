## `openjdk:16-ea-13-jdk-windowsservercore-ltsc2016`

```console
$ docker pull openjdk@sha256:de48f66d6592a8604188f125762f76474578fa847940ab8679cf773282118c44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3866; amd64

### `openjdk:16-ea-13-jdk-windowsservercore-ltsc2016` - windows version 10.0.14393.3866; amd64

```console
$ docker pull openjdk@sha256:a3c1c2968af0c82782979591adbb442c9dfee633daac1b0bd84c72c018800f8f
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 GB (5955447308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1baa1b7421dd0a720dc687b79962065bf2980903719ef12ce52cc8b8db8a12d0`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 05 Aug 2020 13:27:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 11 Aug 2020 20:31:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Aug 2020 15:24:16 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force
# Wed, 12 Aug 2020 15:24:17 GMT
ENV JAVA_HOME=C:\openjdk-16
# Wed, 12 Aug 2020 15:25:29 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Thu, 27 Aug 2020 22:16:13 GMT
ENV JAVA_VERSION=16-ea+13
# Thu, 27 Aug 2020 22:16:14 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk16/13/GPL/openjdk-16-ea+13_windows-x64_bin.zip
# Thu, 27 Aug 2020 22:16:14 GMT
ENV JAVA_SHA256=054db7127dd6aaf511122fb635ed2d0c77aab20ce9cfe6c6c0b0a89910d354bc
# Thu, 27 Aug 2020 22:18:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Thu, 27 Aug 2020 22:18:38 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b2151f69990007e1df0a2a0a68997c72a9ce7546d653d17a482a51cc3323c047`  
		Size: 1.7 GB (1668161535 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:32838d9637dc39d4acee78700b0f93d6c8c9d2db755f12c8009c1b51687d3fbd`  
		Last Modified: Tue, 11 Aug 2020 20:54:28 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:138271f8777367b1ff54a3d43137d564baa693e3e0b71305261b35b9720e7779`  
		Last Modified: Wed, 12 Aug 2020 16:09:25 GMT  
		Size: 9.9 MB (9868368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34771dfe42ef423846ebfe01aab83001e3cc7208753079693787f39ae976a049`  
		Last Modified: Wed, 12 Aug 2020 16:09:20 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25894be8edb605a7d00928789801b5eaa84815ceb02fd359924f3252fffeae0d`  
		Last Modified: Wed, 12 Aug 2020 16:09:24 GMT  
		Size: 5.3 MB (5344121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98fb6b2fd331b1812a8b9fcbd0e7eb8aef12c17242325cd3aa066e538b4fb056`  
		Last Modified: Thu, 27 Aug 2020 22:24:41 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12eb4c1d1c3b25aaf8672bc7128490bface0408986c0c9cbff2f1a76a6dcee17`  
		Last Modified: Thu, 27 Aug 2020 22:24:41 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef63a0facbb497f1453bb5a98f15ac80db0ee465b3cd1984d21edaba47eaee60`  
		Last Modified: Thu, 27 Aug 2020 22:24:41 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3dde91683703007fdd80a1c07ed5abe1b2838179c78ca7eac21d8103f8c2a14`  
		Last Modified: Thu, 27 Aug 2020 22:25:03 GMT  
		Size: 202.1 MB (202080489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a1f87a3bfdc86b68410abd9c9f8fa40e264841a37781b05bb2c1e94571e4427`  
		Last Modified: Thu, 27 Aug 2020 22:24:41 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
