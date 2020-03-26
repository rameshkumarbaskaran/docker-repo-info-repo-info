## `adoptopenjdk:14-jre-openj9-windowsservercore-1809`

```console
$ docker pull adoptopenjdk@sha256:7a405cb44fd5defe5edb6ac3893495a6086505517adccf7c00e79bac05e89faf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `adoptopenjdk:14-jre-openj9-windowsservercore-1809` - windows version 10.0.17763.1098; amd64

```console
$ docker pull adoptopenjdk@sha256:7f10321dddfc15a53e89b7b9c2962905cef97b72fac615898fc21ebec9612324
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2356399469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5848a016c529394700cce16fe57040774bccefc1ae42838ba42c60e6ffdd919`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 06 Mar 2020 11:12:29 GMT
RUN Install update 1809-amd64
# Wed, 11 Mar 2020 00:42:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 26 Mar 2020 18:31:19 GMT
ENV JAVA_VERSION=jdk-14+36.1_openj9-0.19.0
# Thu, 26 Mar 2020 18:38:05 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk14-binaries/releases/download/jdk-14%2B36.1_openj9-0.19.0/OpenJDK14U-jre_x64_windows_openj9_14_36_openj9-0.19.0.msi ...');         [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;         wget https://github.com/AdoptOpenJDK/openjdk14-binaries/releases/download/jdk-14%2B36.1_openj9-0.19.0/OpenJDK14U-jre_x64_windows_openj9_14_36_openj9-0.19.0.msi -O 'openjdk.msi';         Write-Host ('Verifying sha256 (f34aeda934828af7d41728231c4a28ff9fcff32ab8271fcbbde8be538b6ebf0c) ...');         if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'f34aeda934828af7d41728231c4a28ff9fcff32ab8271fcbbde8be538b6ebf0c') {                 Write-Host 'FAILED!';                 exit 1;         };                 New-Item -ItemType Directory -Path C:\temp | Out-Null;                 Write-Host 'Installing using MSI ...';         Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',         '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;         Write-Host 'Removing openjdk.msi ...';         Remove-Item openjdk.msi -Force;         Remove-Item -Path C:\temp -Recurse | Out-Null;
# Thu, 26 Mar 2020 18:38:06 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+UseContainerSupport -XX:+IdleTuningCompactOnIdle -XX:+IdleTuningGcOnIdle
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23645bd7ee0885911e1e2ab55ebcb36ce35795e1ceba9166ffd1b26dde18c3ee`  
		Size: 730.7 MB (730650958 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a7fab05ac5ad4b2f665ad71b5c08a81e82bff7ea2fdcbb66c14193d2dd268875`  
		Last Modified: Wed, 11 Mar 2020 01:16:21 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea320567efb330ee63130007a0d0fc41fee61247c0d1f898ef792e75b2eac81`  
		Last Modified: Thu, 26 Mar 2020 18:47:59 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea0cfe3e02663aefb0511841d6a23c56f0394aea0ac6b3db5b718d12555994ee`  
		Last Modified: Thu, 26 Mar 2020 18:49:46 GMT  
		Size: 91.1 MB (91059703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b8e9e6add7ea8b4552988c7861f7da7781e9cf82ea2aa6f33b9ff6c225b5dcb`  
		Last Modified: Thu, 26 Mar 2020 18:49:30 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
