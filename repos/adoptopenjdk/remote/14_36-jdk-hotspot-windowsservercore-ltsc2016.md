## `adoptopenjdk:14_36-jdk-hotspot-windowsservercore-ltsc2016`

```console
$ docker pull adoptopenjdk@sha256:9b46b2037eca5c1ddd7a36ce930403020ee2d7575699912141d437f1ba3b7f09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3568; amd64

### `adoptopenjdk:14_36-jdk-hotspot-windowsservercore-ltsc2016` - windows version 10.0.14393.3568; amd64

```console
$ docker pull adoptopenjdk@sha256:d0bcf9b411a6ccc6678c88c26d049d994ba0ee57ba9b0d6e481f1bc57e6afbad
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 GB (6134942245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfd300b75cdbd382647fece6c40aefcd90b598332bfee83c3bfd312330922b40`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 10 Mar 2020 08:14:00 GMT
RUN Install update ltsc2016-amd64
# Fri, 13 Mar 2020 21:32:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 26 Mar 2020 18:15:40 GMT
ENV JAVA_VERSION=jdk-14+36
# Thu, 26 Mar 2020 18:19:19 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk14-binaries/releases/download/jdk-14%2B36/OpenJDK14U-jdk_x64_windows_hotspot_14_36.msi ...');         [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;         wget https://github.com/AdoptOpenJDK/openjdk14-binaries/releases/download/jdk-14%2B36/OpenJDK14U-jdk_x64_windows_hotspot_14_36.msi -O 'openjdk.msi';         Write-Host ('Verifying sha256 (f33ff09ade466ce4a50a6cba9f88b6a1596f8259bf2802215be113cd455208c3) ...');         if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'f33ff09ade466ce4a50a6cba9f88b6a1596f8259bf2802215be113cd455208c3') {                 Write-Host 'FAILED!';                 exit 1;         };                 New-Item -ItemType Directory -Path C:\temp | Out-Null;                 Write-Host 'Installing using MSI ...';         Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',         '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;         Write-Host 'Removing openjdk.msi ...';         Remove-Item openjdk.msi -Force;         Remove-Item -Path C:\temp -Recurse | Out-Null;
# Thu, 26 Mar 2020 18:19:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a5d20b7a2294a0d2631f74f49fc34574484a692913559546ef0bceae789fd7a8`  
		Size: 1.7 GB (1658775203 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f08cc5bf7287bc1d8f72edfe2439c99210e433230a22fc73264fcf1685850ed2`  
		Last Modified: Fri, 13 Mar 2020 22:09:47 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bafdaf15fdfb37f3f1bad87c80f8f4879a6e5a95c2a072fbf67bde76dc4a2a90`  
		Last Modified: Thu, 26 Mar 2020 18:41:07 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ce5544682915a616df7006904b4c932e1a38d0ee27aec6eececd5952ff8c831`  
		Last Modified: Thu, 26 Mar 2020 18:42:10 GMT  
		Size: 406.2 MB (406177770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd6d690a561b781f90e7ab8c009eaa1a17a557ee0dbaaf9f66f768383fe3237a`  
		Last Modified: Thu, 26 Mar 2020 18:41:07 GMT  
		Size: 1.1 KB (1143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
