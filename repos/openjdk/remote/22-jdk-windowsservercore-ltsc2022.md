## `openjdk:22-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:a2dbc3504005ec8f2c89729cd9a45b71dd9d851704c6c67953a6ca387bd3c384
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2159; amd64

### `openjdk:22-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.2159; amd64

```console
$ docker pull openjdk@sha256:d3fac28959c9ed527e5f96ffdc06dd9ce47c512a15a108bb35b80e78f5faa81a
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2087800245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2ce61782ad7b910138459ac52c8b5e48a5bf1c82a1e885f16ecd068f5ce4b01`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 02 Dec 2023 12:42:56 GMT
RUN Install update 10.0.20348.2159
# Tue, 09 Jan 2024 00:54:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Jan 2024 00:55:16 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 09 Jan 2024 00:55:17 GMT
ENV JAVA_HOME=C:\openjdk-22
# Tue, 09 Jan 2024 00:55:23 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 09 Jan 2024 00:55:23 GMT
ENV JAVA_VERSION=22-ea+30
# Tue, 09 Jan 2024 00:55:24 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk22/30/GPL/openjdk-22-ea+30_windows-x64_bin.zip
# Tue, 09 Jan 2024 00:55:25 GMT
ENV JAVA_SHA256=3714f6cd54b27fcae643df9a1c2a10ae44a9ded4e6a4ede6866067717b70e01c
# Tue, 09 Jan 2024 00:55:53 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 09 Jan 2024 00:55:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7839fc47f6e056f9e09a214230f8b7115e69419dbc74acbbb1ad6bc0caa28862`  
		Last Modified: Tue, 12 Dec 2023 18:27:40 GMT  
		Size: 500.7 MB (500674814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458ab00caee60771ea8c674514e615c7575c64dee2a0a534ae75674177b1caa3`  
		Last Modified: Tue, 09 Jan 2024 00:56:02 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b94547f49fabaa19545b609426995242d8cf1b07079fad489e27f315312030ec`  
		Last Modified: Tue, 09 Jan 2024 00:56:03 GMT  
		Size: 505.5 KB (505483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5136171e045010e6628a8997bd470e50c5a30c76cb3a621c3d9c830081f87f94`  
		Last Modified: Tue, 09 Jan 2024 00:56:02 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e32821195f0915e9812c8559e8c554a1fd9effb4b12049cf2c3271b4cd7bbe73`  
		Last Modified: Tue, 09 Jan 2024 00:56:02 GMT  
		Size: 322.5 KB (322489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82592292596c1e31217633c00391fb4402dbe168b4af12b7f0dda2ee0c443ba4`  
		Last Modified: Tue, 09 Jan 2024 00:56:00 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0fb5735af049ce5a7e582ce101e8e9eda65e7c67a4b7fcdf9330f9f328b89c0`  
		Last Modified: Tue, 09 Jan 2024 00:56:00 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b525fdf57359d43f166c410cd0e97fe47d92a827f10b894b89fc3696d19e16f1`  
		Last Modified: Tue, 09 Jan 2024 00:56:00 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69025915d38220673ab055606c081f25ccd25df4ad7902b8ab83887337a6461c`  
		Last Modified: Tue, 09 Jan 2024 00:56:10 GMT  
		Size: 197.7 MB (197690912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0ec68ddbd1182fdffe4767bde59148e8dd8955dac8474527752eb1fdda300a`  
		Last Modified: Tue, 09 Jan 2024 00:56:00 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
