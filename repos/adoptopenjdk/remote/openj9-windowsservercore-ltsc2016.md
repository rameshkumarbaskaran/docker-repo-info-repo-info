## `adoptopenjdk:openj9-windowsservercore-ltsc2016`

```console
$ docker pull adoptopenjdk@sha256:f323102e5eea7898a3ec1400a3f522f1df14578beecf888fa650cc9b79c1dc69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3506; amd64

### `adoptopenjdk:openj9-windowsservercore-ltsc2016` - windows version 10.0.14393.3506; amd64

```console
$ docker pull adoptopenjdk@sha256:56e422f7f0d8836d0b91aa41e0c40a8978f0ebfe5b17c76f9ebfa66cf9d7fac8
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 GB (6127395741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7959b4f1ac81199bac96909e25158158179f12978d37a292ebc80808cf18e143`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 14 Feb 2020 21:42:00 GMT
RUN Install update ltsc2016-amd64
# Thu, 20 Feb 2020 01:48:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 20 Feb 2020 11:32:21 GMT
ENV JAVA_VERSION=jdk-13.0.2+8_openj9-0.18.0
# Thu, 20 Feb 2020 11:35:55 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.2%2B8_openj9-0.18.0/OpenJDK13U-jdk_x64_windows_openj9_13.0.2_8_openj9-0.18.0.msi ...');         [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;         wget https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.2%2B8_openj9-0.18.0/OpenJDK13U-jdk_x64_windows_openj9_13.0.2_8_openj9-0.18.0.msi -O 'openjdk.msi';         Write-Host ('Verifying sha256 (b96fdec7f69ff3a36ed3b03774d7ad3fc9385c80de7d8df9c4e6b4fbec70dcd9) ...');         if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'b96fdec7f69ff3a36ed3b03774d7ad3fc9385c80de7d8df9c4e6b4fbec70dcd9') {                 Write-Host 'FAILED!';                 exit 1;         };                 New-Item -ItemType Directory -Path C:\temp | Out-Null;                 Write-Host 'Installing using MSI ...';         Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',         '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;         Write-Host 'Removing openjdk.msi ...';         Remove-Item openjdk.msi -Force;         Remove-Item -Path C:\temp -Recurse | Out-Null;
# Thu, 20 Feb 2020 11:35:57 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+UseContainerSupport -XX:+IdleTuningCompactOnIdle -XX:+IdleTuningGcOnIdle
# Thu, 20 Feb 2020 11:35:59 GMT
CMD ["jshell"]
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
	-	`sha256:c4159ac1bd5966c43bb6d96cd14dcf1f998fe884d3dc35342201f2b18976b343`  
		Last Modified: Thu, 20 Feb 2020 12:10:50 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b4882f3cf85b0abe3784581a8a3d08340e95063c112bd0a29fd784e6c9108eb`  
		Last Modified: Thu, 20 Feb 2020 12:11:25 GMT  
		Size: 400.3 MB (400325983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6b3231d2016186e9f6c2a97d6bc054bb3519fbedf5a0ecf0b8ea982cf98f38f`  
		Last Modified: Thu, 20 Feb 2020 12:10:49 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9628f5b9b25a47ea2d1504370c3b7e62785c1149baa223c09bf200ec5be1e4f8`  
		Last Modified: Thu, 20 Feb 2020 12:10:49 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
