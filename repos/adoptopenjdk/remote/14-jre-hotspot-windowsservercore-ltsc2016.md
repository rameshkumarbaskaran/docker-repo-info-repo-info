## `adoptopenjdk:14-jre-hotspot-windowsservercore-ltsc2016`

```console
$ docker pull adoptopenjdk@sha256:4602fc4d56341389cc61901898a51302d5e3873c89fd8fa6c650d4dfee905cda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3568; amd64

### `adoptopenjdk:14-jre-hotspot-windowsservercore-ltsc2016` - windows version 10.0.14393.3568; amd64

```console
$ docker pull adoptopenjdk@sha256:b75d65048b99de254b20774941f6aeec5cf23a233410c93906346d677f11a464
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5827593790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ad8ff29e4454df160f924c00a1c76ae3de95f0c4125a489a95cf53ec50d3131`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
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
# Thu, 26 Mar 2020 18:24:48 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk14-binaries/releases/download/jdk-14%2B36/OpenJDK14U-jre_x64_windows_hotspot_14_36.msi ...');         [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;         wget https://github.com/AdoptOpenJDK/openjdk14-binaries/releases/download/jdk-14%2B36/OpenJDK14U-jre_x64_windows_hotspot_14_36.msi -O 'openjdk.msi';         Write-Host ('Verifying sha256 (b04050c65ace822ee515c84b0856abf87deb2ff8c0586e18066eafde744233ed) ...');         if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'b04050c65ace822ee515c84b0856abf87deb2ff8c0586e18066eafde744233ed') {                 Write-Host 'FAILED!';                 exit 1;         };                 New-Item -ItemType Directory -Path C:\temp | Out-Null;                 Write-Host 'Installing using MSI ...';         Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',         '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;         Write-Host 'Removing openjdk.msi ...';         Remove-Item openjdk.msi -Force;         Remove-Item -Path C:\temp -Recurse | Out-Null;
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
	-	`sha256:47d91ca15692bbf4742867848d3c8e94ad815d3f43790fb3ee7b9c31d0f52477`  
		Last Modified: Thu, 26 Mar 2020 18:43:48 GMT  
		Size: 98.8 MB (98830458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
