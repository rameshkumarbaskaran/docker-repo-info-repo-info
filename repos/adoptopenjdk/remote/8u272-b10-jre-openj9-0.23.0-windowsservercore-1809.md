## `adoptopenjdk:8u272-b10-jre-openj9-0.23.0-windowsservercore-1809`

```console
$ docker pull adoptopenjdk@sha256:4e8052d8b5e625849d83dc27bbfed77014ceb345f582b2b9d6bfab13fb6f9af7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1577; amd64

### `adoptopenjdk:8u272-b10-jre-openj9-0.23.0-windowsservercore-1809` - windows version 10.0.17763.1577; amd64

```console
$ docker pull adoptopenjdk@sha256:0f66e102fb1e71bfee4716668bfdb1434e08176282a18ee1368497563517c0d5
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2485241343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65f1dc9014c28feb2a61a326bf059c7d85fdd78f895d9a4f3477325ebce1fc18`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 03 Nov 2020 03:11:34 GMT
RUN Install update 1809-amd64
# Wed, 11 Nov 2020 13:26:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Nov 2020 19:22:44 GMT
ENV JAVA_VERSION=jdk8u272-b10_openj9-0.23.0
# Wed, 11 Nov 2020 19:28:58 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u272-b10_openj9-0.23.0/OpenJDK8U-jre_x64_windows_openj9_8u272b10_openj9-0.23.0.msi ...');     [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     wget https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u272-b10_openj9-0.23.0/OpenJDK8U-jre_x64_windows_openj9_8u272b10_openj9-0.23.0.msi -O 'openjdk.msi';     Write-Host ('Verifying sha256 (7a0021f86d6a8f100e6d139e0f5e4c40b8af75809dc82b58b44dbcc479663355) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '7a0021f86d6a8f100e6d139e0f5e4c40b8af75809dc82b58b44dbcc479663355') {             Write-Host 'FAILED!';             exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;     Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 11 Nov 2020 19:28:59 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle
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
	-	`sha256:09d62c618e6da6c9f75458406ac1996ecbb3792fbaca635f5cb1d1386a08725f`  
		Last Modified: Wed, 11 Nov 2020 20:14:07 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7485bdd3a34db65f1a5772c07922156b3e00b3541577dcf2e28f42451cdc4779`  
		Last Modified: Wed, 11 Nov 2020 20:15:30 GMT  
		Size: 97.2 MB (97208617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809fff1c21ef064010c02ebbf44e54f4916b55fbd57e236b247bcd82778e55d1`  
		Last Modified: Wed, 11 Nov 2020 20:15:17 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
