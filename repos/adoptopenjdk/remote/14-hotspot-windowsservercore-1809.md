## `adoptopenjdk:14-hotspot-windowsservercore-1809`

```console
$ docker pull adoptopenjdk@sha256:da2897e7da9f7ac457985d03252cc7d91595f414765972a34691f6fd06261070
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `adoptopenjdk:14-hotspot-windowsservercore-1809` - windows version 10.0.17763.1098; amd64

```console
$ docker pull adoptopenjdk@sha256:483176ea1258427a6aaf57967c8d22888a06f0d2bd1d0003f9e79e09a72d7c55
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2666354205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87f4516066cfd3175bc27654433b55793c599f8b11bb27851cca2a7a913a847f`
-	Default Command: `["jshell"]`
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
# Thu, 26 Mar 2020 18:22:20 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk14-binaries/releases/download/jdk-14%2B36/OpenJDK14U-jdk_x64_windows_hotspot_14_36.msi ...');         [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;         wget https://github.com/AdoptOpenJDK/openjdk14-binaries/releases/download/jdk-14%2B36/OpenJDK14U-jdk_x64_windows_hotspot_14_36.msi -O 'openjdk.msi';         Write-Host ('Verifying sha256 (f33ff09ade466ce4a50a6cba9f88b6a1596f8259bf2802215be113cd455208c3) ...');         if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'f33ff09ade466ce4a50a6cba9f88b6a1596f8259bf2802215be113cd455208c3') {                 Write-Host 'FAILED!';                 exit 1;         };                 New-Item -ItemType Directory -Path C:\temp | Out-Null;                 Write-Host 'Installing using MSI ...';         Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',         '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;         Write-Host 'Removing openjdk.msi ...';         Remove-Item openjdk.msi -Force;         Remove-Item -Path C:\temp -Recurse | Out-Null;
# Thu, 26 Mar 2020 18:22:22 GMT
CMD ["jshell"]
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
	-	`sha256:d60f0644abfcbc4abbda61652ace99dcda434d4c6d7e601bf5dfe6e082beb748`  
		Last Modified: Thu, 26 Mar 2020 18:43:19 GMT  
		Size: 401.0 MB (401014407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22c640a484e125548d3c771520f80d3280300c81108527d9f8ca6339b77f3820`  
		Last Modified: Thu, 26 Mar 2020 18:42:32 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
