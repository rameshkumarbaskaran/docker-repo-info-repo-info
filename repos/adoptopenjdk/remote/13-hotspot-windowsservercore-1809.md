## `adoptopenjdk:13-hotspot-windowsservercore-1809`

```console
$ docker pull adoptopenjdk@sha256:e5f77166f800651fa5c1b03d59520abb6233ce35f7d2ae3cc25f7504b2bc668d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.914; amd64

### `adoptopenjdk:13-hotspot-windowsservercore-1809` - windows version 10.0.17763.914; amd64

```console
$ docker pull adoptopenjdk@sha256:cb445410bceea93623e17013816a647a0c10abc4df3ec1d326e1b53f2ed8e560
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2611776758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:355ecab2a1ad82236a114b241b8ce8e0c6802ba745b3b35d93ed6acd3e0d837a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 29 Nov 2019 04:34:15 GMT
RUN Install update 1809-amd64
# Tue, 10 Dec 2019 21:34:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2019 20:53:35 GMT
ENV JAVA_VERSION=jdk-13.0.1+9
# Wed, 11 Dec 2019 20:56:27 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_x64_windows_hotspot_13.0.1_9.msi ...');         [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;         wget https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_x64_windows_hotspot_13.0.1_9.msi -O 'openjdk.msi';         Write-Host ('Verifying sha256 (ccb52fac99f9d872d02fc5b82f33863138e9fbe08fef4c2e21ec8ec8c3eb2b44) ...');         if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'ccb52fac99f9d872d02fc5b82f33863138e9fbe08fef4c2e21ec8ec8c3eb2b44') {                 Write-Host 'FAILED!';                 exit 1;         };                 New-Item -ItemType Directory -Path C:\temp | Out-Null;                 Write-Host 'Installing using MSI ...';         Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',         '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;         Write-Host 'Removing openjdk.msi ...';         Remove-Item openjdk.msi -Force;         Remove-Item -Path C:\temp -Recurse | Out-Null;
# Wed, 11 Dec 2019 20:56:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:faf31ee0aa3d3c60a38dd03c7554d632065cef50eab052ef1444590786249d07`  
		Size: 681.6 MB (681618026 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e147f14e0d6a9cbd5261162dea8f3aac7a34db5d9f6a587a9aac6b88722a2da4`  
		Last Modified: Tue, 10 Dec 2019 22:07:34 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aadf355f3e249b7fd4b7f036269d9763cc3273bf6dd7477afea1338cf815725`  
		Last Modified: Wed, 11 Dec 2019 22:22:06 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56b3bea8fe51ca71f8ed6db5168c39e63c5dfcbc8d1eb7d92f7743bf7bb83330`  
		Last Modified: Wed, 11 Dec 2019 22:22:58 GMT  
		Size: 395.5 MB (395469810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cd74cfa57705332d030a10df2748e91c1d16b473d6ca9dcdf0a10c4ead5cfaa`  
		Last Modified: Wed, 11 Dec 2019 22:22:05 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
