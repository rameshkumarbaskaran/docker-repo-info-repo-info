## `openjdk:18-ea-jdk-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:d3197232ece804b9bda9e829a5bd26081dbc88b36011ce1a4bb788adefe1fe65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2114; amd64

### `openjdk:18-ea-jdk-windowsservercore-1809` - windows version 10.0.17763.2114; amd64

```console
$ docker pull openjdk@sha256:8e5d98e6488bf89685c62cec60260ac64673b290998f231dc86417fab0526b21
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2869652496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c70bca6b9cdd518cb78692021e25160c5557da1afc3da09cf994d987459dc442`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 05 Aug 2021 19:44:34 GMT
RUN Install update 1809-amd64
# Wed, 11 Aug 2021 12:16:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Aug 2021 17:21:43 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 11 Aug 2021 17:21:46 GMT
ENV JAVA_HOME=C:\openjdk-18
# Wed, 11 Aug 2021 17:22:48 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 13 Aug 2021 18:14:35 GMT
ENV JAVA_VERSION=18-ea+10
# Fri, 13 Aug 2021 18:14:37 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk18/10/GPL/openjdk-18-ea+10_windows-x64_bin.zip
# Fri, 13 Aug 2021 18:14:39 GMT
ENV JAVA_SHA256=ebb61201944bef5edd2faa880c947aef2e21db417e501d39e01f2cf473245a02
# Fri, 13 Aug 2021 18:16:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 13 Aug 2021 18:16:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c67ded6868b61d392a0c096f911563fd6bc0bc3ed4fe401d077b3718a1b0cdaf`  
		Size: 967.7 MB (967665054 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f5be68d5dab08a1dcc52a6ee52dd4901e4d6a384f0df3a12cba3d53649f7c602`  
		Last Modified: Wed, 11 Aug 2021 13:29:37 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a93339de9664b8795350d24edfc9da5614b2c1711961e94e1cb0ca7cf7fae74a`  
		Last Modified: Wed, 11 Aug 2021 18:16:44 GMT  
		Size: 360.5 KB (360455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c74e3eb523942e0a9d7759e2b01e97ab8666b3f5e3de6d2bc3f0af7ba05a733`  
		Last Modified: Wed, 11 Aug 2021 18:16:43 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f02991b19a6d7da3867281c2401153bfb9a7890b6a53aa493ae4839fa4dcbf97`  
		Last Modified: Wed, 11 Aug 2021 18:16:43 GMT  
		Size: 317.3 KB (317277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41973bd74cd9d9ea8523561fcc96f46b838cecd729052b1fb22bed136bc21b30`  
		Last Modified: Fri, 13 Aug 2021 18:23:57 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6528e3e5bb7ce8bed37faee3e0821e521824ca6d53bbb0e42868bc74798d0280`  
		Last Modified: Fri, 13 Aug 2021 18:23:57 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cfb56eb8fc906539dccd215ce9bd17336c413afcd32d48202c2d9e7504ade6b`  
		Last Modified: Fri, 13 Aug 2021 18:23:57 GMT  
		Size: 1.4 KB (1448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d3b477d76c08e87a529fccdc192715269617c5b893c3bbeb32f8825afe57d4`  
		Last Modified: Fri, 13 Aug 2021 18:24:16 GMT  
		Size: 183.0 MB (182968284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60728b7e1cfb16e2d9ab70cba9bbec1cd416a694c7eb5b37b752cc7da3cd4f0b`  
		Last Modified: Fri, 13 Aug 2021 18:23:57 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
