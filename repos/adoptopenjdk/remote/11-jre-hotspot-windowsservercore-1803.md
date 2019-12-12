## `adoptopenjdk:11-jre-hotspot-windowsservercore-1803`

```console
$ docker pull adoptopenjdk@sha256:a9dfe1635088e433ec0935b657a4ad7354d31ae9d3a4301f0fee53e19763bd3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17134.1184; amd64

### `adoptopenjdk:11-jre-hotspot-windowsservercore-1803` - windows version 10.0.17134.1184; amd64

```console
$ docker pull adoptopenjdk@sha256:79bdda5db0380e87a71d0297f4446f7b9a5182b21c1d0304c04888521d16f713
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2432614769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f704b9c8261a51d1fdcb0808370bf194ca8880eb144ebe98f261cd659df450b8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 12 Apr 2018 09:20:54 GMT
RUN Apply image 1803-RTM-amd64
# Wed, 04 Dec 2019 15:21:18 GMT
RUN Install update 1803-amd64
# Wed, 11 Dec 2019 20:25:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2019 20:40:29 GMT
ENV JAVA_VERSION=jdk-11.0.5+10
# Wed, 11 Dec 2019 20:49:19 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.5%2B10/OpenJDK11U-jre_x64_windows_hotspot_11.0.5_10.msi ...');         [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;         wget https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.5%2B10/OpenJDK11U-jre_x64_windows_hotspot_11.0.5_10.msi -O 'openjdk.msi';         Write-Host ('Verifying sha256 (3d06a2bde2bf9cad88bf151aa789528a87353a18c26f17cf259fa86439c9c417) ...');         if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '3d06a2bde2bf9cad88bf151aa789528a87353a18c26f17cf259fa86439c9c417') {                 Write-Host 'FAILED!';                 exit 1;         };                 New-Item -ItemType Directory -Path C:\temp | Out-Null;                 Write-Host 'Installing using MSI ...';         Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',         '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;         Write-Host 'Removing openjdk.msi ...';         Remove-Item openjdk.msi -Force;         Remove-Item -Path C:\temp -Recurse | Out-Null;
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
	-	`sha256:8910e7a0ae7cd57d5a29fc540a4121f7d98a0c670b11c2f9fca893ab1a6d1ed7`  
		Last Modified: Wed, 11 Dec 2019 22:17:46 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56b25d0d0df0fd417e5a1e02d9059df1d96bd661e0168a1ef135498364d68179`  
		Last Modified: Wed, 11 Dec 2019 22:20:21 GMT  
		Size: 76.1 MB (76050605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
