## `adoptopenjdk:8u242-b08-jre-hotspot-windowsservercore-ltsc2016`

```console
$ docker pull adoptopenjdk@sha256:9186f655b5c80300d89ef6d1b3d7e86420f62e6ef2e300acab22a8e2fc582769
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3506; amd64

### `adoptopenjdk:8u242-b08-jre-hotspot-windowsservercore-ltsc2016` - windows version 10.0.14393.3506; amd64

```console
$ docker pull adoptopenjdk@sha256:939f5231e692f49252a1c3d2328458d28ad0ac8aa360c31da164358d2ef52025
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5805661495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:410e42efa0a85b6bc388df8340ced971e461f83bfb61f1e8fd5823a6ed1f68a7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 14 Feb 2020 21:42:00 GMT
RUN Install update ltsc2016-amd64
# Thu, 20 Feb 2020 01:48:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 26 Feb 2020 23:15:17 GMT
ENV JAVA_VERSION=jdk8u242-b08
# Wed, 26 Feb 2020 23:23:18 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u242-b08/OpenJDK8U-jre_x64_windows_hotspot_8u242b08.msi ...');         [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;         wget https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u242-b08/OpenJDK8U-jre_x64_windows_hotspot_8u242b08.msi -O 'openjdk.msi';         Write-Host ('Verifying sha256 (b1c486ca9fb9632bba9dd70778c7b371d5ee84cfbfaf6bd59a3e5cfd310a4f74) ...');         if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'b1c486ca9fb9632bba9dd70778c7b371d5ee84cfbfaf6bd59a3e5cfd310a4f74') {                 Write-Host 'FAILED!';                 exit 1;         };                 New-Item -ItemType Directory -Path C:\temp | Out-Null;                 Write-Host 'Installing using MSI ...';         Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',         '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;         Write-Host 'Removing openjdk.msi ...';         Remove-Item openjdk.msi -Force;         Remove-Item -Path C:\temp -Recurse | Out-Null;
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:846a2223e9e7a88a2a07d706553f144d380483d72fb9f0697c4fcd71773a8693`  
		Size: 1.7 GB (1657079102 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:72c4471958f7f0f07260f0f430bcffb0bc07811088c24cffba1439d250ea1ae3`  
		Last Modified: Thu, 20 Feb 2020 03:04:52 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdaf4b2a0af020d8d06062c1be67e1e89f1c407f937a85fb12fc8f5d68c29614`  
		Last Modified: Wed, 26 Feb 2020 23:28:09 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:814a176fe28d3b7bc2b051b73d5cf625e8361627cfd12c026bb70b71315c6eb4`  
		Last Modified: Wed, 26 Feb 2020 23:30:36 GMT  
		Size: 78.6 MB (78594099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
