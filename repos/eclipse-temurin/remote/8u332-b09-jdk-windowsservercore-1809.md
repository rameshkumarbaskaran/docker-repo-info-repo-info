## `eclipse-temurin:8u332-b09-jdk-windowsservercore-1809`

```console
$ docker pull eclipse-temurin@sha256:fbb68349332e14ae69757398e35d73a7aeb7fdb8fdc9c196cef824aa68380176
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2803; amd64

### `eclipse-temurin:8u332-b09-jdk-windowsservercore-1809` - windows version 10.0.17763.2803; amd64

```console
$ docker pull eclipse-temurin@sha256:55980688243cef782b65d0574e4e94e616a3cc00172f7f8cb2470fea9f9191a8
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2905389544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a32125824abd9be5c71416d5ab4e41ea928aed1d21e13bc8d9062d8cc51437b5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 04 Apr 2022 11:20:25 GMT
RUN Install update 1809-amd64
# Wed, 13 Apr 2022 02:34:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 05 May 2022 18:18:23 GMT
ENV JAVA_VERSION=jdk8u332-b09
# Thu, 05 May 2022 18:20:21 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_windows_hotspot_8u332b09.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_windows_hotspot_8u332b09.msi ;     Write-Host ('Verifying sha256 (543c46b0589d71a2dc5b18c45b94c01258aecb5bcdd9f45b5898a70bed9141fa) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '543c46b0589d71a2dc5b18c45b94c01258aecb5bcdd9f45b5898a70bed9141fa') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 05 May 2022 18:21:41 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac -version'; javac -version;     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba8181afd4264392fbbf8df14fb4cddc55fbe085ab000e986b789678bc2bb171`  
		Size: 997.6 MB (997587446 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba1c113303b8371787710ec139807b93d58a8b0789523fc35afdb65f6e94bc61`  
		Last Modified: Wed, 13 Apr 2022 03:15:12 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03a4a837cb67f4430e1ba610e80834a3389b7db7081462647df0979867c36898`  
		Last Modified: Thu, 05 May 2022 21:21:02 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890e4b7e2eb33bc623d7a7f0dc0768723838aa997d3c0dcd462e0a0baf22a507`  
		Last Modified: Thu, 05 May 2022 21:21:20 GMT  
		Size: 189.1 MB (189135212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:982b3ee03eabd35ab6b9c1d897f04cb72988fb5f70f22592cd11f5143bd81c8b`  
		Last Modified: Thu, 05 May 2022 21:21:02 GMT  
		Size: 331.2 KB (331188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
