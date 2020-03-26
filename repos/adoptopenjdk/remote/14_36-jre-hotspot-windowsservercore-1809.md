## `adoptopenjdk:14_36-jre-hotspot-windowsservercore-1809`

```console
$ docker pull adoptopenjdk@sha256:9080ae2441185d0f934b17ec6c3b2add7d1119a4306c037fe93552bd7d7d4a2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `adoptopenjdk:14_36-jre-hotspot-windowsservercore-1809` - windows version 10.0.17763.1098; amd64

```console
$ docker pull adoptopenjdk@sha256:779c946d8d77adf95c2deade2a9c5592f0577dfd607627ed2034ca55a4242907
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2363517058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:494f9b7100d6180b27a5ecb2677345d551eebeff72dbfcde990b95051b3af0b9`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 06 Mar 2020 11:12:29 GMT
RUN Install update 1809-amd64
# Wed, 11 Mar 2020 00:42:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 26 Mar 2020 18:19:38 GMT
ENV JAVA_VERSION=jdk-14+36
# Thu, 26 Mar 2020 18:26:26 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk14-binaries/releases/download/jdk-14%2B36/OpenJDK14U-jre_x64_windows_hotspot_14_36.msi ...');         [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;         wget https://github.com/AdoptOpenJDK/openjdk14-binaries/releases/download/jdk-14%2B36/OpenJDK14U-jre_x64_windows_hotspot_14_36.msi -O 'openjdk.msi';         Write-Host ('Verifying sha256 (b04050c65ace822ee515c84b0856abf87deb2ff8c0586e18066eafde744233ed) ...');         if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'b04050c65ace822ee515c84b0856abf87deb2ff8c0586e18066eafde744233ed') {                 Write-Host 'FAILED!';                 exit 1;         };                 New-Item -ItemType Directory -Path C:\temp | Out-Null;                 Write-Host 'Installing using MSI ...';         Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',         '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;         Write-Host 'Removing openjdk.msi ...';         Remove-Item openjdk.msi -Force;         Remove-Item -Path C:\temp -Recurse | Out-Null;
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23645bd7ee0885911e1e2ab55ebcb36ce35795e1ceba9166ffd1b26dde18c3ee`  
		Size: 730.7 MB (730650958 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a7fab05ac5ad4b2f665ad71b5c08a81e82bff7ea2fdcbb66c14193d2dd268875`  
		Last Modified: Wed, 11 Mar 2020 01:16:21 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b36e39a8621783ad973c7afd51d903915d6901177e86c2e25f796bce8694bba4`  
		Last Modified: Thu, 26 Mar 2020 18:42:32 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:762bf767f89ec6ad32927d4252619cb49c60ae8ed8c2c7b593d59eef309b196a`  
		Last Modified: Thu, 26 Mar 2020 18:44:19 GMT  
		Size: 98.2 MB (98178414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
