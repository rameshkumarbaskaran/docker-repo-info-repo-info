## `adoptopenjdk:14-openj9-windowsservercore-ltsc2016`

```console
$ docker pull adoptopenjdk@sha256:139d55250cf1d6cbea6707e553deb2625ba15da7ad55208b9475d0fbf38b5543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3568; amd64

### `adoptopenjdk:14-openj9-windowsservercore-ltsc2016` - windows version 10.0.14393.3568; amd64

```console
$ docker pull adoptopenjdk@sha256:8097a962426840e0909f9f0754e9c577a504b29a080f92aec706708a2de57e33
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 GB (6122843764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:825d741ceb01f15d396d43a0d3a04d399359ad6bdaa6b7556ae34a34c09e22a1`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 10 Mar 2020 08:14:00 GMT
RUN Install update ltsc2016-amd64
# Fri, 13 Mar 2020 21:32:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 26 Mar 2020 18:27:37 GMT
ENV JAVA_VERSION=jdk-14+36.1_openj9-0.19.0
# Thu, 26 Mar 2020 18:31:10 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk14-binaries/releases/download/jdk-14%2B36.1_openj9-0.19.0/OpenJDK14U-jdk_x64_windows_openj9_14_36_openj9-0.19.0.msi ...');         [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;         wget https://github.com/AdoptOpenJDK/openjdk14-binaries/releases/download/jdk-14%2B36.1_openj9-0.19.0/OpenJDK14U-jdk_x64_windows_openj9_14_36_openj9-0.19.0.msi -O 'openjdk.msi';         Write-Host ('Verifying sha256 (b245cca34f2bb6e063b19aed44efb7e22ae57d1c832554ef9deb7a7f521c3b20) ...');         if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'b245cca34f2bb6e063b19aed44efb7e22ae57d1c832554ef9deb7a7f521c3b20') {                 Write-Host 'FAILED!';                 exit 1;         };                 New-Item -ItemType Directory -Path C:\temp | Out-Null;                 Write-Host 'Installing using MSI ...';         Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',         '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;         Write-Host 'Removing openjdk.msi ...';         Remove-Item openjdk.msi -Force;         Remove-Item -Path C:\temp -Recurse | Out-Null;
# Thu, 26 Mar 2020 18:31:11 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+UseContainerSupport -XX:+IdleTuningCompactOnIdle -XX:+IdleTuningGcOnIdle
# Thu, 26 Mar 2020 18:31:12 GMT
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
	-	`sha256:af19ddcf558639b57715517a760a15178438b152f920364e66e1e728ecdd1c6e`  
		Last Modified: Thu, 26 Mar 2020 18:44:37 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7863962b2975b351276c0016f4b9f7fa111ef3a0bbc6cf0751070a7bb3b6de`  
		Last Modified: Thu, 26 Mar 2020 18:47:44 GMT  
		Size: 394.1 MB (394078103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a42f053a70e71346990e9db0256fc98c3511413568d2d51ad0c9712f498a137`  
		Last Modified: Thu, 26 Mar 2020 18:44:37 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e53a5bcfbaca96217db29fbca220c8463b160cd3856df32d08b99e4409f1621`  
		Last Modified: Thu, 26 Mar 2020 18:44:38 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
