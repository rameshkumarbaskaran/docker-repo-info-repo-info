## `adoptopenjdk:11-jre-hotspot-windowsservercore-1803`

```console
$ docker pull adoptopenjdk@sha256:969dac30e45e912024ff19bfc4ac7626544e738ac76ec8b84ad3e3af89c6a437
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17134.1246; amd64

### `adoptopenjdk:11-jre-hotspot-windowsservercore-1803` - windows version 10.0.17134.1246; amd64

```console
$ docker pull adoptopenjdk@sha256:0af05126ebcb9d87b618f7fd5a752a1bb16f617b56e7f3e36ea53d726356520e
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2434989889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75db2ab64c6284a898c7db037a6ef10f7624970340c1e04c8c3a183a1b082185`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 12 Apr 2018 09:20:54 GMT
RUN Apply image 1803-RTM-amd64
# Wed, 08 Jan 2020 15:30:02 GMT
RUN Install update 1803-amd64
# Wed, 15 Jan 2020 18:58:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Jan 2020 19:14:32 GMT
ENV JAVA_VERSION=jdk-11.0.5+10
# Wed, 15 Jan 2020 19:23:26 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.5%2B10/OpenJDK11U-jre_x64_windows_hotspot_11.0.5_10.msi ...');         [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;         wget https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.5%2B10/OpenJDK11U-jre_x64_windows_hotspot_11.0.5_10.msi -O 'openjdk.msi';         Write-Host ('Verifying sha256 (3d06a2bde2bf9cad88bf151aa789528a87353a18c26f17cf259fa86439c9c417) ...');         if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '3d06a2bde2bf9cad88bf151aa789528a87353a18c26f17cf259fa86439c9c417') {                 Write-Host 'FAILED!';                 exit 1;         };                 New-Item -ItemType Directory -Path C:\temp | Out-Null;                 Write-Host 'Installing using MSI ...';         Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',         '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;         Write-Host 'Removing openjdk.msi ...';         Remove-Item openjdk.msi -Force;         Remove-Item -Path C:\temp -Recurse | Out-Null;
```

-	Layers:
	-	`sha256:d9e8b01179bfc94a5bdb1810fbd76b999aa52016001ace2d3a4c4bc7065a9601`  
		Last Modified: Tue, 18 Sep 2018 22:43:55 GMT  
		Size: 1.7 GB (1659688273 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:270ec3ad3fc7d52c0dd086b32f7751131c799e25cdcd4686cc33cbf2b607c34e`  
		Size: 699.2 MB (699246147 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4b8ccd780af5210d26057ebca3a11489d01a7a0151f175a60af96d3719ce8bc9`  
		Last Modified: Wed, 15 Jan 2020 20:45:08 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98c10173f75e43b342c7fb6d7e73a144d844d5669ef82d3d819453243a554553`  
		Last Modified: Wed, 15 Jan 2020 20:50:23 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b37b81b38f7c293319775df508a9c16a6d1006bd264eb3c87eb0eb4f1793bb87`  
		Last Modified: Wed, 15 Jan 2020 20:53:16 GMT  
		Size: 76.1 MB (76053075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
