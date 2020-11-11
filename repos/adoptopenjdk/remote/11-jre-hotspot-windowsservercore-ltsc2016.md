## `adoptopenjdk:11-jre-hotspot-windowsservercore-ltsc2016`

```console
$ docker pull adoptopenjdk@sha256:7e5ab33fa522eb79f8a272000f1852b28ae2ba0f64cd1b3775edf3319c204646
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4046; amd64

### `adoptopenjdk:11-jre-hotspot-windowsservercore-ltsc2016` - windows version 10.0.14393.4046; amd64

```console
$ docker pull adoptopenjdk@sha256:c4ab3e727a1ac98bbabe2cd6b55dd51b1a827f92d523665cc7162c9bb7fdbe0d
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5853018857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba616390e08f179cfa2d8dde25e1d57ee280c11a365191203d7622a8ba2092ac`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 28 Oct 2020 18:03:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Nov 2020 13:23:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Nov 2020 18:55:46 GMT
ENV JAVA_VERSION=jdk-11.0.9+11
# Wed, 11 Nov 2020 19:02:39 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.9%2B11.1/OpenJDK11U-jre_x64_windows_hotspot_11.0.9_11.msi ...');     [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     wget https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.9%2B11.1/OpenJDK11U-jre_x64_windows_hotspot_11.0.9_11.msi -O 'openjdk.msi';     Write-Host ('Verifying sha256 (d9d155ff0d58c2f821a30f88e0e0d7dfc8a4942c7563d277484c1ae77077fb3e) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'd9d155ff0d58c2f821a30f88e0e0d7dfc8a4942c7563d277484c1ae77077fb3e') {             Write-Host 'FAILED!';             exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;     Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4830fb08bc2df7ae80548c349b880c263ea87a7b93e13ecbc77c862b6e179558`  
		Size: 1.7 GB (1700572904 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:126d9a92c0cb7b68c56dec2dd5ba118de9dde3ec6368db734c5135fdf1528a33`  
		Last Modified: Wed, 11 Nov 2020 13:34:53 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47efa4ea66519325e506a5f51e1fcdc42b785982583e939f1c4883eb11964b2b`  
		Last Modified: Wed, 11 Nov 2020 20:06:19 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2edd874d6f62cf4057701f5a09ba390559c91fcf5990488384861f096849029e`  
		Last Modified: Wed, 11 Nov 2020 20:08:55 GMT  
		Size: 82.5 MB (82457767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
