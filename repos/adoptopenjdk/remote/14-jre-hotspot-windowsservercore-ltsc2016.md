## `adoptopenjdk:14-jre-hotspot-windowsservercore-ltsc2016`

```console
$ docker pull adoptopenjdk@sha256:e227f03a512cfae8bcf2d430f5835b78de6c4803d21fc3bb37a9c152e40a2a9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3630; amd64

### `adoptopenjdk:14-jre-hotspot-windowsservercore-ltsc2016` - windows version 10.0.14393.3630; amd64

```console
$ docker pull adoptopenjdk@sha256:b398eff296fb293a3e676d394832741b1df97966a4191bedc024ac00c1e511fc
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5826846604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:055ca07a7203c7200ab7334e5987eede4b460e42a625b1f28f3b37dbac0ebc14`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
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
# Tue, 21 Apr 2020 20:05:16 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk14-binaries/releases/download/jdk-14.0.1%2B7/OpenJDK14U-jre_x64_windows_hotspot_14.0.1_7.msi ...');         [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;         wget https://github.com/AdoptOpenJDK/openjdk14-binaries/releases/download/jdk-14.0.1%2B7/OpenJDK14U-jre_x64_windows_hotspot_14.0.1_7.msi -O 'openjdk.msi';         Write-Host ('Verifying sha256 (27350710fe290fd99e0cd75da99fb29892ca934c41dcd248d859fbd501e2d4ac) ...');         if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '27350710fe290fd99e0cd75da99fb29892ca934c41dcd248d859fbd501e2d4ac') {                 Write-Host 'FAILED!';                 exit 1;         };                 New-Item -ItemType Directory -Path C:\temp | Out-Null;                 Write-Host 'Installing using MSI ...';         Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',         '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;         Write-Host 'Removing openjdk.msi ...';         Remove-Item openjdk.msi -Force;         Remove-Item -Path C:\temp -Recurse | Out-Null;
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
	-	`sha256:15b673aa4e435e8dba56855047cc434cfb303e9b93ced1f06d7727e2e1fe097f`  
		Last Modified: Tue, 21 Apr 2020 20:13:23 GMT  
		Size: 98.8 MB (98776749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
