## `adoptopenjdk:8-jdk-hotspot-windowsservercore-1809`

```console
$ docker pull adoptopenjdk@sha256:8718d482197dcecc0c9aad7954e1c50a6b292f014b8f67a0b6e5727e65dbbac9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1577; amd64

### `adoptopenjdk:8-jdk-hotspot-windowsservercore-1809` - windows version 10.0.17763.1577; amd64

```console
$ docker pull adoptopenjdk@sha256:baf1c04cf8e4ea5c3766ede3c896e1b4a69e79fe0673c4efa329d3e94391357c
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2589726384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbe0457ba5ac3e950599c600bffa3ee7a646dcec70657f7ee1ac2ed3c2a4b7db`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 03 Nov 2020 03:11:34 GMT
RUN Install update 1809-amd64
# Wed, 11 Nov 2020 13:26:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Nov 2020 18:44:50 GMT
ENV JAVA_VERSION=jdk8u272-b10
# Wed, 11 Nov 2020 18:46:35 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u272-b10/OpenJDK8U-jdk_x64_windows_hotspot_8u272b10.msi ...');     [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     wget https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u272-b10/OpenJDK8U-jdk_x64_windows_hotspot_8u272b10.msi -O 'openjdk.msi';     Write-Host ('Verifying sha256 (71b6ca8f866bf604e6d4fbe29884bbfd815ffcf1dd2dbbc82c8f33b9c0485c9d) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '71b6ca8f866bf604e6d4fbe29884bbfd815ffcf1dd2dbbc82c8f33b9c0485c9d') {             Write-Host 'FAILED!';             exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;     Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:680bbdbacf1bcbace70de5087d02d31e9dd7a22feae59f746f54dab46c1d5bda`  
		Size: 669.7 MB (669696346 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:da5a67a9f3a363cb69c8104913a5a58c1c47e8f648a07d057fc28a5f98790e60`  
		Last Modified: Wed, 11 Nov 2020 13:37:50 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef73a4345aed026e9c6a9dc0f40dd69bb0a5f30efa5e4198da6acf16d477fa49`  
		Last Modified: Wed, 11 Nov 2020 20:03:36 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f9a9b62f151bf61d383544a0a083198ca30aa53d013eb99ddceaf19e6c3ad3c`  
		Last Modified: Wed, 11 Nov 2020 20:03:54 GMT  
		Size: 201.7 MB (201694819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
