## `adoptopenjdk:8u232-b09-jre-openj9-0.17.0-windowsservercore-1803`

```console
$ docker pull adoptopenjdk@sha256:34f39f659f65bfa7a7269495b7aebcd2fe5a56c8c1f30e6ed617eb0a0c7ccfc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17134.1184; amd64

### `adoptopenjdk:8u232-b09-jre-openj9-0.17.0-windowsservercore-1803` - windows version 10.0.17134.1184; amd64

```console
$ docker pull adoptopenjdk@sha256:17f791a358646d391b710e3c8c0c29b4e16f970e752376cd0b05c461d66acc2f
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2449236284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccd52f1606f59328b87a842f59a6cb0c6db21c2f1e06f67f4286224c7c6c1b49`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 12 Apr 2018 09:20:54 GMT
RUN Apply image 1803-RTM-amd64
# Wed, 04 Dec 2019 15:21:18 GMT
RUN Install update 1803-amd64
# Wed, 11 Dec 2019 20:25:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2019 21:19:09 GMT
ENV JAVA_VERSION=jdk8u232-b09_openj9-0.17.0
# Wed, 11 Dec 2019 21:27:42 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09_openj9-0.17.0/OpenJDK8U-jre_x64_windows_openj9_8u232b09_openj9-0.17.0.msi ...');         [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;         wget https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09_openj9-0.17.0/OpenJDK8U-jre_x64_windows_openj9_8u232b09_openj9-0.17.0.msi -O 'openjdk.msi';         Write-Host ('Verifying sha256 (d4b3e632fe4a2d4ba1f315c3745381669a617068940166966712b9628817bb1c) ...');         if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'd4b3e632fe4a2d4ba1f315c3745381669a617068940166966712b9628817bb1c') {                 Write-Host 'FAILED!';                 exit 1;         };                 New-Item -ItemType Directory -Path C:\temp | Out-Null;                 Write-Host 'Installing using MSI ...';         Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',         '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;         Write-Host 'Removing openjdk.msi ...';         Remove-Item openjdk.msi -Force;         Remove-Item -Path C:\temp -Recurse | Out-Null;
# Wed, 11 Dec 2019 21:27:44 GMT
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
	-	`sha256:83b2b390540a91a8eb8dc86cc503cd1f4668031d778b9af0daf237db7f7f4224`  
		Last Modified: Wed, 11 Dec 2019 22:29:07 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44ca87f894242d4df6a1d1a1735f559c272c2b8491411377fa0012c67e123df0`  
		Last Modified: Wed, 11 Dec 2019 22:31:49 GMT  
		Size: 92.7 MB (92670963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bbeb2fc156c5f4d3c59b5f1fe686edf8da88a389d30ebaa856d729f9d2b4b6f`  
		Last Modified: Wed, 11 Dec 2019 22:31:35 GMT  
		Size: 1.2 KB (1198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
