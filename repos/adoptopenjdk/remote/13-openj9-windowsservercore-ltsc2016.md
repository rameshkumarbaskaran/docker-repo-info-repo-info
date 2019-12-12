## `adoptopenjdk:13-openj9-windowsservercore-ltsc2016`

```console
$ docker pull adoptopenjdk@sha256:d14c714b85c2dbd7fa4ab44d00371e53099e44d7792bd561618865e60e47c218
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3384; amd64

### `adoptopenjdk:13-openj9-windowsservercore-ltsc2016` - windows version 10.0.14393.3384; amd64

```console
$ docker pull adoptopenjdk@sha256:ade4bca5bf8cc147fec423e4036fed7bd24b578e7feb3fcc12e98b5318fa428d
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 GB (6124325987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8a1a4cbe116ca41e94f68a9deffe23f78301c9ab50723806e1f5ac8b030d1a8`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 27 Nov 2019 14:43:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Dec 2019 00:35:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2019 21:44:49 GMT
ENV JAVA_VERSION=jdk-13.0.1+9_openj9-0.17.0
# Wed, 11 Dec 2019 21:48:17 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9_openj9-0.17.0/OpenJDK13U-jdk_x64_windows_openj9_13.0.1_9_openj9-0.17.0.msi ...');         [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;         wget https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9_openj9-0.17.0/OpenJDK13U-jdk_x64_windows_openj9_13.0.1_9_openj9-0.17.0.msi -O 'openjdk.msi';         Write-Host ('Verifying sha256 (bdcd3349615c7f6ab2102686d2ed1704b1e033bbbb227d278b9c280913af778f) ...');         if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'bdcd3349615c7f6ab2102686d2ed1704b1e033bbbb227d278b9c280913af778f') {                 Write-Host 'FAILED!';                 exit 1;         };                 New-Item -ItemType Directory -Path C:\temp | Out-Null;                 Write-Host 'Installing using MSI ...';         Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',         '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;         Write-Host 'Removing openjdk.msi ...';         Remove-Item openjdk.msi -Force;         Remove-Item -Path C:\temp -Recurse | Out-Null;
# Wed, 11 Dec 2019 21:48:19 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+UseContainerSupport -XX:+IdleTuningCompactOnIdle -XX:+IdleTuningGcOnIdle
# Wed, 11 Dec 2019 21:48:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:55d044e60c8959ce88aee467913bb11827c1ec057a2fd108a293e274dbd74f1d`  
		Size: 1.7 GB (1652717978 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:530e4240d4261ce165890648d1df6230dc4f9ce5df2e6cf9f0d5876694c3d4f0`  
		Last Modified: Wed, 11 Dec 2019 01:14:39 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb780d586fe0cf5d5f55ac6dbe57faecb84ecff6abfdf3ffba71855c68de53c`  
		Last Modified: Wed, 11 Dec 2019 22:38:44 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbd1bec987fd657a3ba4d86d7c865a04ce68b64552e73276d48c19c68aa99302`  
		Last Modified: Wed, 11 Dec 2019 22:39:37 GMT  
		Size: 401.6 MB (401617310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ddb766972f6c8575b0cc3fb86817cfb8f05435a0011c1ed0160c6aabb746477`  
		Last Modified: Wed, 11 Dec 2019 22:38:43 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dbe78b6b580b3c4968cc0d40df6ff8244e609a98dfeb4cfc0c4710e25366f87`  
		Last Modified: Wed, 11 Dec 2019 22:38:44 GMT  
		Size: 1.2 KB (1204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
