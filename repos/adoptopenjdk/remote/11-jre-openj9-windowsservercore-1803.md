## `adoptopenjdk:11-jre-openj9-windowsservercore-1803`

```console
$ docker pull adoptopenjdk@sha256:db3d8578a99de28686d0577404555867792f1943a2608bcf83775737ba4bc927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17134.1184; amd64

### `adoptopenjdk:11-jre-openj9-windowsservercore-1803` - windows version 10.0.17134.1184; amd64

```console
$ docker pull adoptopenjdk@sha256:f15f8bce15c2465e6e5da826b5242cacf39427f4f7868be8912cffa6a0fa1a9b
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2432382355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9a2e366a44a7c84aa069afa572968c75ff862ac35f38ee1cea22c7d1752d380`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 12 Apr 2018 09:20:54 GMT
RUN Apply image 1803-RTM-amd64
# Wed, 04 Dec 2019 15:21:18 GMT
RUN Install update 1803-amd64
# Wed, 11 Dec 2019 20:25:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2019 21:35:33 GMT
ENV JAVA_VERSION=jdk-11.0.5+10_openj9-0.17.0
# Wed, 11 Dec 2019 21:44:22 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.5%2B10_openj9-0.17.0/OpenJDK11U-jre_x64_windows_openj9_11.0.5_10_openj9-0.17.0.msi ...');         [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;         wget https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.5%2B10_openj9-0.17.0/OpenJDK11U-jre_x64_windows_openj9_11.0.5_10_openj9-0.17.0.msi -O 'openjdk.msi';         Write-Host ('Verifying sha256 (53fd0efde528d20bcbed03320a07e39d6fa91b92695f22fe05fce0c9a4187b5b) ...');         if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '53fd0efde528d20bcbed03320a07e39d6fa91b92695f22fe05fce0c9a4187b5b') {                 Write-Host 'FAILED!';                 exit 1;         };                 New-Item -ItemType Directory -Path C:\temp | Out-Null;                 Write-Host 'Installing using MSI ...';         Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',         '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;         Write-Host 'Removing openjdk.msi ...';         Remove-Item openjdk.msi -Force;         Remove-Item -Path C:\temp -Recurse | Out-Null;
# Wed, 11 Dec 2019 21:44:25 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+UseContainerSupport -XX:+IdleTuningCompactOnIdle -XX:+IdleTuningGcOnIdle
```

-	Layers:
	-	`sha256:d9e8b01179bfc94a5bdb1810fbd76b999aa52016001ace2d3a4c4bc7065a9601`  
		Last Modified: Tue, 18 Sep 2018 22:43:55 GMT  
		Size: 1.7 GB (1659688273 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d117323cd539488e5ef3bef575a41fa714d83119b0da1896607d96ec2a5e3b52`  
		Size: 696.9 MB (696873564 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:76b68c2d6c99fac63a7998081753df26697a83f71d1138943905bde6cb959583`  
		Last Modified: Wed, 11 Dec 2019 22:12:46 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f77e915de0c1a9141c70a40d4278acdcac9f57cf8da82321dafc5050d4296f0`  
		Last Modified: Wed, 11 Dec 2019 22:35:44 GMT  
		Size: 1.2 KB (1197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c4b33a3d38b86fb7aca789fe5689c9da55ca8ee670022e8a321a046eb1a41ab`  
		Last Modified: Wed, 11 Dec 2019 22:38:22 GMT  
		Size: 75.8 MB (75816978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba761a7b56692edf21de2d2c35eb386f5e61366b7e3811dbf1744fc707951752`  
		Last Modified: Wed, 11 Dec 2019 22:38:09 GMT  
		Size: 1.2 KB (1202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
