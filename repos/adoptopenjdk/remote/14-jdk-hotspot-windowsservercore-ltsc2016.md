## `adoptopenjdk:14-jdk-hotspot-windowsservercore-ltsc2016`

```console
$ docker pull adoptopenjdk@sha256:09ca2cfb5c3eae834a4d6a75f38c954cb49b23c2faafa2885ea37f83c0296ff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3630; amd64

### `adoptopenjdk:14-jdk-hotspot-windowsservercore-ltsc2016` - windows version 10.0.14393.3630; amd64

```console
$ docker pull adoptopenjdk@sha256:5bb31ea24a852ec7632bc59a4d97ade4195649d22835cb6f614db98df047cc53
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 GB (6123163919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:816067b1e20d9a6ffded75e24e694e885b7eec6424262de2ea96849fd1d32373`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Apr 2020 17:30:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 14 Apr 2020 21:35:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 21 Apr 2020 19:26:24 GMT
ENV JAVA_VERSION=jdk-14.0.1+7
# Tue, 21 Apr 2020 19:29:46 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk14-binaries/releases/download/jdk-14.0.1%2B7/OpenJDK14U-jdk_x64_windows_hotspot_14.0.1_7.msi ...');         [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;         wget https://github.com/AdoptOpenJDK/openjdk14-binaries/releases/download/jdk-14.0.1%2B7/OpenJDK14U-jdk_x64_windows_hotspot_14.0.1_7.msi -O 'openjdk.msi';         Write-Host ('Verifying sha256 (57bba8e69023985ebe09e79cda85e171e2ec87a0c738d5018a836ee779fe52e9) ...');         if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '57bba8e69023985ebe09e79cda85e171e2ec87a0c738d5018a836ee779fe52e9') {                 Write-Host 'FAILED!';                 exit 1;         };                 New-Item -ItemType Directory -Path C:\temp | Out-Null;                 Write-Host 'Installing using MSI ...';         Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',         '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;         Write-Host 'Removing openjdk.msi ...';         Remove-Item openjdk.msi -Force;         Remove-Item -Path C:\temp -Recurse | Out-Null;
# Tue, 21 Apr 2020 19:29:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d0099407ec8ccaf0472e55152e38b262bdf0b2cf8dfd2e8afcc89d728ba3f5a0`  
		Size: 1.7 GB (1658081673 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7ac0134cee91589d04e97f11994235cce86faef5c581d15f2e143ecb90e92572`  
		Last Modified: Tue, 14 Apr 2020 22:16:36 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a60da3316fa78e6e1e207c1ea67262df7d2328a7949d91adb7e62dcb2c186e8c`  
		Last Modified: Tue, 21 Apr 2020 20:10:34 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37f314c6d0ef2fd4d3ae793792583a112f9a02aa4bfdd9ba7c80fcad86eb215`  
		Last Modified: Tue, 21 Apr 2020 20:11:29 GMT  
		Size: 395.1 MB (395092936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eb31ea3107309e040408435578453f767ffb7c8967346699beb99808f4d42da`  
		Last Modified: Tue, 21 Apr 2020 20:10:34 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
