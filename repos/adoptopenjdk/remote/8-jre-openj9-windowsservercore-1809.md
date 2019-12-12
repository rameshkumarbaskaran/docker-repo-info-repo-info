## `adoptopenjdk:8-jre-openj9-windowsservercore-1809`

```console
$ docker pull adoptopenjdk@sha256:ba2ed9d48e8befca0b4a8fa4887781704c235afd60610e0d3ba21f27e056304e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.914; amd64

### `adoptopenjdk:8-jre-openj9-windowsservercore-1809` - windows version 10.0.17763.914; amd64

```console
$ docker pull adoptopenjdk@sha256:7f5811bf644c746d5f003cd4c9a506ddb07292c03357980a7419c20278491a8e
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2308675756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6f77235796fe047895856a83f10f2ddb4fcb6a5ae3a855132e285013f185e72`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 29 Nov 2019 04:34:15 GMT
RUN Install update 1809-amd64
# Tue, 10 Dec 2019 21:34:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2019 21:16:36 GMT
ENV JAVA_VERSION=jdk8u232-b09_openj9-0.17.0
# Wed, 11 Dec 2019 21:25:43 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09_openj9-0.17.0/OpenJDK8U-jre_x64_windows_openj9_8u232b09_openj9-0.17.0.msi ...');         [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;         wget https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09_openj9-0.17.0/OpenJDK8U-jre_x64_windows_openj9_8u232b09_openj9-0.17.0.msi -O 'openjdk.msi';         Write-Host ('Verifying sha256 (d4b3e632fe4a2d4ba1f315c3745381669a617068940166966712b9628817bb1c) ...');         if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'd4b3e632fe4a2d4ba1f315c3745381669a617068940166966712b9628817bb1c') {                 Write-Host 'FAILED!';                 exit 1;         };                 New-Item -ItemType Directory -Path C:\temp | Out-Null;                 Write-Host 'Installing using MSI ...';         Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',         '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;         Write-Host 'Removing openjdk.msi ...';         Remove-Item openjdk.msi -Force;         Remove-Item -Path C:\temp -Recurse | Out-Null;
# Wed, 11 Dec 2019 21:25:46 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+UseContainerSupport -XX:+IdleTuningCompactOnIdle -XX:+IdleTuningGcOnIdle
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
	-	`sha256:dc8a458b25dccd8f456aca6e7bc87bdc8fabb7cb5e131f60f3a7cb9b0ea18a00`  
		Last Modified: Wed, 11 Dec 2019 22:28:05 GMT  
		Size: 1.2 KB (1215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0db549ec2e925ea24ee719cf1a53e29dce6d6c6bcdc3b155c73f783f8ef91193`  
		Last Modified: Wed, 11 Dec 2019 22:31:14 GMT  
		Size: 92.4 MB (92368796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8ee672b6799a2c39b3c2f3e240a3b224fb1615bc30116e603e8cb0a7381aded`  
		Last Modified: Wed, 11 Dec 2019 22:31:00 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
