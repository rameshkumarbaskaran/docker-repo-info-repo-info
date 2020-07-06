## `openjdk:15-ea-jdk-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:07f70abc75ba39a1b48473ae8b0cbb25f28703befca07a55c91b761c39fee0a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1282; amd64

### `openjdk:15-ea-jdk-windowsservercore-1809` - windows version 10.0.17763.1282; amd64

```console
$ docker pull openjdk@sha256:b2879bdd8fef948fe3cd3addf22b5f1347da938572eb8ae4fd8bff68ac547e25
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2490639590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86928d25c9f06da64debd4f463908b3b312fdf05ee9a3abe3c4894c231979cc9`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Jun 2020 01:48:42 GMT
RUN Install update 1809-amd64
# Tue, 09 Jun 2020 22:33:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Jun 2020 22:34:11 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force
# Tue, 09 Jun 2020 22:34:12 GMT
ENV JAVA_HOME=C:\openjdk-15
# Tue, 09 Jun 2020 22:34:39 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Mon, 06 Jul 2020 20:23:02 GMT
ENV JAVA_VERSION=15-ea+30
# Mon, 06 Jul 2020 20:23:03 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk15/30/GPL/openjdk-15-ea+30_windows-x64_bin.zip
# Mon, 06 Jul 2020 20:23:04 GMT
ENV JAVA_SHA256=9ca949d409fa964df8513f554cdaacb5efe6f135aabdc8476b753b31fe90f5f5
# Mon, 06 Jul 2020 20:55:16 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 06 Jul 2020 20:55:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:666079ee04606f07f4a27dd98526f5049ef8fed93e347d8b4c447b0d5060c77d`  
		Size: 575.6 MB (575581379 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f841c6a0c622cd36b5b2688011a224ac3e8e96273758f4a2804f2f3f099f267d`  
		Last Modified: Tue, 09 Jun 2020 23:17:50 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03d8ec06304524cdb2b900879af7ed2db71d5e36e5f2306b46859250255390d`  
		Last Modified: Tue, 09 Jun 2020 23:17:51 GMT  
		Size: 4.8 MB (4765053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29e91effeb439b76990fcc94732e86884df9c268d3125e7baeda527ddb3bb6d5`  
		Last Modified: Tue, 09 Jun 2020 23:17:50 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13d559d86d0b9a731bed7f5c7bfd949bba5687f2ad8da359606bfcb75a14161a`  
		Last Modified: Tue, 09 Jun 2020 23:17:49 GMT  
		Size: 289.8 KB (289776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e877d75020411833c0b1d9ed26ba8e67fda2dd201a658ea93266cd5a860663e4`  
		Last Modified: Mon, 06 Jul 2020 21:06:02 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e164b42679e32be279118a27faa4ed0cdb078ff2ea36b603716f9fca1dbdb1ac`  
		Last Modified: Mon, 06 Jul 2020 21:06:02 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:693c79b44335e8a782f9af7b48d6ecb81441c63d08bf6ddae81ca914a384d0fb`  
		Last Modified: Mon, 06 Jul 2020 21:06:02 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:939f6d699bda96542280d7f532ca80647f207f6b7ff3ee66191e15b2ace94196`  
		Last Modified: Mon, 06 Jul 2020 21:06:23 GMT  
		Size: 191.7 MB (191663632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54c9dd26ea28312dfff8bb3013ea1d6accfda36c61817341a0f0b05d37a3cfb5`  
		Last Modified: Mon, 06 Jul 2020 21:06:03 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
