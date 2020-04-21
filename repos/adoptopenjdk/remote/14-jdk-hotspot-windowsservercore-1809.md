## `adoptopenjdk:14-jdk-hotspot-windowsservercore-1809`

```console
$ docker pull adoptopenjdk@sha256:4ffb3c22af4d1f28b39e4d480c37695ebf8703bdc537e11789619b5e103a2422
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1158; amd64

### `adoptopenjdk:14-jdk-hotspot-windowsservercore-1809` - windows version 10.0.17763.1158; amd64

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
