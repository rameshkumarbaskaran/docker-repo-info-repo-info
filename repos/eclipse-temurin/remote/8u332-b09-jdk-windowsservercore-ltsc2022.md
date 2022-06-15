## `eclipse-temurin:8u332-b09-jdk-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:0c2169a5f14ff19f5dc3d67af88b42fedfe0a9b0fb4534b3be102ffedd643981
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.768; amd64

### `eclipse-temurin:8u332-b09-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.768; amd64

```console
$ docker pull eclipse-temurin@sha256:c2f7b4f8b13d534b40078c159fd34ad29b036f0fd3e95467f1e698833d3d84e2
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2468409686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:300a8cb3125c4a0d9b52459dfc57d5e8ac22e28d6b3223eb385590821e284cb9`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Thu, 09 Jun 2022 04:32:50 GMT
RUN Install update 10.0.20348.768
# Wed, 15 Jun 2022 12:13:32 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Jun 2022 17:26:32 GMT
ENV JAVA_VERSION=jdk8u332-b09
# Wed, 15 Jun 2022 17:27:21 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_windows_hotspot_8u332b09.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_windows_hotspot_8u332b09.msi ;     Write-Host ('Verifying sha256 (543c46b0589d71a2dc5b18c45b94c01258aecb5bcdd9f45b5898a70bed9141fa) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '543c46b0589d71a2dc5b18c45b94c01258aecb5bcdd9f45b5898a70bed9141fa') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 15 Jun 2022 17:27:48 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac -version'; javac -version;     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6c71967ff41928927e4c407171e4ffbac3c9ab4221eb64f5ca5a34ff4c230567`  
		Size: 841.6 MB (841600427 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:dec0338feaf01f35eb916b7fd9ecc08b719354163254885d5215e513c1a3eb2e`  
		Last Modified: Wed, 15 Jun 2022 12:49:26 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62d06f3e2eb09865a953503639bae0fb2a53bfe598b14e51f87548443ec17bff`  
		Last Modified: Wed, 15 Jun 2022 18:17:57 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db8a0596410b00967267bbcf33d206edfe87db9490091e1bd4d48afe7ae355b7`  
		Last Modified: Wed, 15 Jun 2022 18:21:20 GMT  
		Size: 189.4 MB (189365853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61feff7358f04c1bc05e3885083f31c74d77370f259bdf71a8c0498e37e0c72d`  
		Last Modified: Wed, 15 Jun 2022 18:17:58 GMT  
		Size: 576.9 KB (576935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
