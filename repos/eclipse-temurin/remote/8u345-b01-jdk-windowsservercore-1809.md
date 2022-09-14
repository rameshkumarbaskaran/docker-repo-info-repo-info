## `eclipse-temurin:8u345-b01-jdk-windowsservercore-1809`

```console
$ docker pull eclipse-temurin@sha256:622aedcb5cee2defa5d6af3bebf0aae1a05ec807e5bc4bccebe9cea6920e43d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3406; amd64

### `eclipse-temurin:8u345-b01-jdk-windowsservercore-1809` - windows version 10.0.17763.3406; amd64

```console
$ docker pull eclipse-temurin@sha256:89131bec02da3994b06c2d96c1063ba055f72862608aefee11f8eaf1d329da07
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2893720470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac7410c51ae9dc3d46de5c1cb1edffdb273f8d5992fcfdaed2d0724b443d85c7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Fri, 09 Sep 2022 22:43:02 GMT
RUN Install update 10.0.17763.3406
# Tue, 13 Sep 2022 18:21:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Sep 2022 16:00:03 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Wed, 14 Sep 2022 16:01:36 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_x64_windows_hotspot_8u345b01.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_x64_windows_hotspot_8u345b01.msi ;     Write-Host ('Verifying sha256 (a19b85fedcc830aa81c6aeb07449905032b7b391c033a1647639486b25f2e1f3) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'a19b85fedcc830aa81c6aeb07449905032b7b391c033a1647639486b25f2e1f3') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 14 Sep 2022 16:02:43 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac -version'; javac -version;     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:cee64bf279e2ca8e924884a10ecb98bfa79c7f0cc8d25e73039b9aeb940815b6`  
		Size: 826.4 MB (826398623 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2bc395c8c47e61e593d2e905e0e051d40e7d25e4aeac7dbe08d3ec57acd0e68f`  
		Last Modified: Tue, 13 Sep 2022 18:25:24 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eb60d65564d0ac5040e222e0d050e314bd45ead06a1c32f2bcdc11434c03e57`  
		Last Modified: Wed, 14 Sep 2022 16:46:40 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:372d1339a282c61ef17433cd34e1029d73045b33739d7eb5b62703f31c40014b`  
		Last Modified: Wed, 14 Sep 2022 16:46:57 GMT  
		Size: 189.8 MB (189835025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8b08bd93ba3f3b0aeb55557cf1e25f72e1ece3b90c721b7ac7b4b05f6fab20`  
		Last Modified: Wed, 14 Sep 2022 16:46:40 GMT  
		Size: 317.9 KB (317881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
