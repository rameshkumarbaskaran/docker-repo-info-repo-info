## `adoptopenjdk:14-hotspot-windowsservercore`

```console
$ docker pull adoptopenjdk@sha256:95f50a69e15bad19169951f1d568d03cfa9a78f97ec4a57c08a7aa12f4a98223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3630; amd64
	-	windows version 10.0.17763.1158; amd64

### `adoptopenjdk:14-hotspot-windowsservercore` - windows version 10.0.14393.3630; amd64

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

### `adoptopenjdk:14-hotspot-windowsservercore` - windows version 10.0.17763.1158; amd64

```console
$ docker pull adoptopenjdk@sha256:396306b5189d630fbf9b9662a6045a7f00bc2fae16ef2115889260efb37811f6
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2660641557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:057d28269182ee9240784b795f1c2e0c03094079a4be4ba99eb254fa131047fe`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Apr 2020 03:38:38 GMT
RUN Install update 1809-amd64
# Tue, 14 Apr 2020 21:32:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 21 Apr 2020 19:30:06 GMT
ENV JAVA_VERSION=jdk-14.0.1+7
# Tue, 21 Apr 2020 20:02:59 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk14-binaries/releases/download/jdk-14.0.1%2B7/OpenJDK14U-jdk_x64_windows_hotspot_14.0.1_7.msi ...');         [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;         wget https://github.com/AdoptOpenJDK/openjdk14-binaries/releases/download/jdk-14.0.1%2B7/OpenJDK14U-jdk_x64_windows_hotspot_14.0.1_7.msi -O 'openjdk.msi';         Write-Host ('Verifying sha256 (57bba8e69023985ebe09e79cda85e171e2ec87a0c738d5018a836ee779fe52e9) ...');         if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '57bba8e69023985ebe09e79cda85e171e2ec87a0c738d5018a836ee779fe52e9') {                 Write-Host 'FAILED!';                 exit 1;         };                 New-Item -ItemType Directory -Path C:\temp | Out-Null;                 Write-Host 'Installing using MSI ...';         Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',         '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;         Write-Host 'Removing openjdk.msi ...';         Remove-Item openjdk.msi -Force;         Remove-Item -Path C:\temp -Recurse | Out-Null;
# Tue, 21 Apr 2020 20:03:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:eac6fba788c9781d6f989eb0932cb33bf72c2cce4eb234cc6decdcab89e183bc`  
		Size: 736.0 MB (736021953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:edc29de224149bd438350512f7a31a67edbd3fcafce757aa60620dc459c184ad`  
		Last Modified: Tue, 14 Apr 2020 22:15:56 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8c07ad24e08a50c4f9c87963650fa90fe57b43abb17e1824271c9067140a9f`  
		Last Modified: Tue, 21 Apr 2020 20:11:51 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab90788586d12196dc5980b678b2ad9c45826d8edb6d01e0519a3202a5efa75c`  
		Last Modified: Tue, 21 Apr 2020 20:12:41 GMT  
		Size: 389.9 MB (389930929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd96da8f4396023e639f090d8a6ad38e363f3e3be8d2d669fdbe9daa2ee498e0`  
		Last Modified: Tue, 21 Apr 2020 20:11:51 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
