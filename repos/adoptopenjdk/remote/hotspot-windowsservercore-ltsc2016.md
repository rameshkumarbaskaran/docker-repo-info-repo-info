## `adoptopenjdk:hotspot-windowsservercore-ltsc2016`

```console
$ docker pull adoptopenjdk@sha256:e5b6cafd88355d7274980aaa112b1bb3de05837f3aff5d0540896017df2bdd75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3443; amd64

### `adoptopenjdk:hotspot-windowsservercore-ltsc2016` - windows version 10.0.14393.3443; amd64

```console
$ docker pull adoptopenjdk@sha256:9b6f495b9ba0a3a1113c40c8f513fba90b3d02c51b9d3cc70fa8ba5f76fb8d17
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 GB (6125339121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbc83d19d0c07529ea7b2df75139009f96aac54d8c53872d2e371b08d3b536b1`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Thu, 02 Jan 2020 15:48:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 14 Jan 2020 23:50:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Jan 2020 19:23:52 GMT
ENV JAVA_VERSION=jdk-13.0.1+9
# Wed, 15 Jan 2020 19:27:26 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_x64_windows_hotspot_13.0.1_9.msi ...');         [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;         wget https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_x64_windows_hotspot_13.0.1_9.msi -O 'openjdk.msi';         Write-Host ('Verifying sha256 (ccb52fac99f9d872d02fc5b82f33863138e9fbe08fef4c2e21ec8ec8c3eb2b44) ...');         if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'ccb52fac99f9d872d02fc5b82f33863138e9fbe08fef4c2e21ec8ec8c3eb2b44') {                 Write-Host 'FAILED!';                 exit 1;         };                 New-Item -ItemType Directory -Path C:\temp | Out-Null;                 Write-Host 'Installing using MSI ...';         Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',         '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;         Write-Host 'Removing openjdk.msi ...';         Remove-Item openjdk.msi -Force;         Remove-Item -Path C:\temp -Recurse | Out-Null;
# Wed, 15 Jan 2020 19:27:28 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:31f9df80631e7b5d379647ee7701ff50e009bd2c03b30a67a0a8e7bba4a26f94`  
		Size: 1.7 GB (1654613376 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f1c8c4c99f36cfcf87884a9382011e93fb05fa4002d8f4eca62a43e744db8e95`  
		Last Modified: Wed, 15 Jan 2020 01:46:47 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de6db5462e62638982657baff47e3a99b6c0cae00d3f6b652e448b7293edc8ae`  
		Last Modified: Wed, 15 Jan 2020 20:53:41 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab70e60e39afd2272f82ff593d0e469da387f276008aca4264d648a62fa1d535`  
		Last Modified: Wed, 15 Jan 2020 20:54:21 GMT  
		Size: 400.7 MB (400736266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17dd68ac15bbcabff2ab351d2b83aee87178b910a2058241712baabe175752ef`  
		Last Modified: Wed, 15 Jan 2020 20:53:41 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
