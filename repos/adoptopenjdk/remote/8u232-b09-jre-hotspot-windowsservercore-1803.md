## `adoptopenjdk:8u232-b09-jre-hotspot-windowsservercore-1803`

```console
$ docker pull adoptopenjdk@sha256:090ead56bf5d403980bee3b5b4ac401948ecb8ab69c09fe1ba63bfd56732d126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17134.1184; amd64

### `adoptopenjdk:8u232-b09-jre-hotspot-windowsservercore-1803` - windows version 10.0.17134.1184; amd64

```console
$ docker pull adoptopenjdk@sha256:ab99fd429452da742a42996eccd023150cb2054966e42285930d91855af48f90
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2434629330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ec24e9c2bdb3042e41f608c055049f462b9f54e8ad548d8582e793b0402db49`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 12 Apr 2018 09:20:54 GMT
RUN Apply image 1803-RTM-amd64
# Wed, 04 Dec 2019 15:21:18 GMT
RUN Install update 1803-amd64
# Wed, 11 Dec 2019 20:25:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2019 20:31:47 GMT
ENV JAVA_VERSION=jdk8u222-b10
# Wed, 11 Dec 2019 20:33:23 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u222-b10/OpenJDK8U-jre_x64_windows_hotspot_8u222b10.msi ...');         [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;         wget https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u222-b10/OpenJDK8U-jre_x64_windows_hotspot_8u222b10.msi -O 'openjdk.msi';         Write-Host ('Verifying sha256 (54a97f9065c3c741c0d816425bcfc31a69042001bdfd30f8b16b9369441a61b6) ...');         if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '54a97f9065c3c741c0d816425bcfc31a69042001bdfd30f8b16b9369441a61b6') {                 Write-Host 'FAILED!';                 exit 1;         };                 New-Item -ItemType Directory -Path C:\temp | Out-Null;                 Write-Host 'Installing using MSI ...';         Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',         '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;         Write-Host 'Removing openjdk.msi ...';         Remove-Item openjdk.msi -Force;         Remove-Item -Path C:\temp -Recurse | Out-Null;
```

-	Layers:
	-	`sha256:d9e8b01179bfc94a5bdb1810fbd76b999aa52016001ace2d3a4c4bc7065a9601`  
		Last Modified: Tue, 18 Sep 2018 22:43:55 GMT  
		Size: 1.7 GB (1659688273 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d117323cd539488e5ef3bef575a41fa714d83119b0da1896607d96ec2a5e3b52`  
		Size: 696.9 MB (696873564 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:76b68c2d6c99fac63a7998081753df26697a83f71d1138943905bde6cb959583`  
		Last Modified: Wed, 11 Dec 2019 22:12:46 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:807040455b650682c3dbdc54384503afd98cb2c8950ac1977c20391484a6549e`  
		Last Modified: Wed, 11 Dec 2019 22:14:47 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d00da31c982053d477312d442dcbedd9afff258fec71472532e4f799d9f98683`  
		Last Modified: Wed, 11 Dec 2019 22:14:58 GMT  
		Size: 78.1 MB (78065140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
