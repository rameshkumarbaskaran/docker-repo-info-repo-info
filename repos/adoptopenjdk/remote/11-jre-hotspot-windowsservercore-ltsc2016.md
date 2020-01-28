## `adoptopenjdk:11-jre-hotspot-windowsservercore-ltsc2016`

```console
$ docker pull adoptopenjdk@sha256:9ce5b70bcb182d24d1d0a85d3d67004f057af516f16aabad2552ec1093870fc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3443; amd64

### `adoptopenjdk:11-jre-hotspot-windowsservercore-ltsc2016` - windows version 10.0.14393.3443; amd64

```console
$ docker pull adoptopenjdk@sha256:4edaf73a79028161a5cf486faa23798ff9678ae42c6ae49fc635d16c5bf41743
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5801217881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f64fc9242f704342c4013225953347c9dc9cffda00566254041f23a99ccab5ba`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Thu, 02 Jan 2020 15:48:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 14 Jan 2020 23:50:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 28 Jan 2020 00:22:43 GMT
ENV JAVA_VERSION=jdk-11.0.6+10
# Tue, 28 Jan 2020 00:31:36 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.6%2B10/OpenJDK11U-jre_x64_windows_hotspot_11.0.6_10.msi ...');         [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;         wget https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.6%2B10/OpenJDK11U-jre_x64_windows_hotspot_11.0.6_10.msi -O 'openjdk.msi';         Write-Host ('Verifying sha256 (d550fbc8348d84ddb15b2deaf322dc3433b933444eaf086ff1a8185e36ffa863) ...');         if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'd550fbc8348d84ddb15b2deaf322dc3433b933444eaf086ff1a8185e36ffa863') {                 Write-Host 'FAILED!';                 exit 1;         };                 New-Item -ItemType Directory -Path C:\temp | Out-Null;                 Write-Host 'Installing using MSI ...';         Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',         '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;         Write-Host 'Removing openjdk.msi ...';         Remove-Item openjdk.msi -Force;         Remove-Item -Path C:\temp -Recurse | Out-Null;
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:31f9df80631e7b5d379647ee7701ff50e009bd2c03b30a67a0a8e7bba4a26f94`  
		Size: 1.7 GB (1654613376 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f1c8c4c99f36cfcf87884a9382011e93fb05fa4002d8f4eca62a43e744db8e95`  
		Last Modified: Wed, 15 Jan 2020 01:46:47 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ba46f2d9018b05ad6ab9dc3e2541c03de607746b1f4b2fa8aea6b3a3524e676`  
		Last Modified: Tue, 28 Jan 2020 01:17:04 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:122fecd2436210f6423abe69669f8e89d21106d729502a3e550facad653e9e6a`  
		Last Modified: Tue, 28 Jan 2020 01:19:41 GMT  
		Size: 76.6 MB (76616215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
