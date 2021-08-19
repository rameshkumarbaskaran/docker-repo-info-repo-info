## `eclipse-temurin:8u302-b08-jre-windowsservercore-1809`

```console
$ docker pull eclipse-temurin@sha256:3aa79db223d3bfc3f588f7a83edadef8d73de71f18c1cde46bbcbdada44b5faa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2114; amd64

### `eclipse-temurin:8u302-b08-jre-windowsservercore-1809` - windows version 10.0.17763.2114; amd64

```console
$ docker pull eclipse-temurin@sha256:b48c8596379632eb0d7326e05715750e2c65d4d1bd511666f6e51fe69dff6a93
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2756965689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6134357607772d8358e333f99a678216379e649232eec2418e5110535551f389`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 05 Aug 2021 19:44:34 GMT
RUN Install update 1809-amd64
# Wed, 11 Aug 2021 12:16:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 13 Aug 2021 21:32:38 GMT
ENV JAVA_VERSION=jdk8u302-b08
# Thu, 19 Aug 2021 20:16:23 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_x64_windows_hotspot_8u302b08.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_x64_windows_hotspot_8u302b08.msi ;     Write-Host ('Verifying sha256 (34e5eea737dfaca57ec5162e6fece5259f403fa419c7bcab572e9cdd2bcf8dd1) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '34e5eea737dfaca57ec5162e6fece5259f403fa419c7bcab572e9cdd2bcf8dd1') {             Write-Host 'FAILED!';             exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {             Write-Host 'FAILED installing MSI!' ;             exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 19 Aug 2021 20:17:54 GMT
RUN Write-Host 'Verifying install ...';     Write-Host '  java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c67ded6868b61d392a0c096f911563fd6bc0bc3ed4fe401d077b3718a1b0cdaf`  
		Size: 967.7 MB (967665054 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f5be68d5dab08a1dcc52a6ee52dd4901e4d6a384f0df3a12cba3d53649f7c602`  
		Last Modified: Wed, 11 Aug 2021 13:29:37 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4366f6dcb586d60ea7d0031a2dcac52b65aff56b1029ade45a73aa1df80b279`  
		Last Modified: Fri, 13 Aug 2021 22:00:10 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d41e89342d74afcd4485007252993c065ea8445afb3e5818bb9867e21de6601`  
		Last Modified: Thu, 19 Aug 2021 20:25:49 GMT  
		Size: 70.6 MB (70621145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f28e23fd65d57423793eaf946468fd91cdd77e4492ebf84297e04fa667c479c`  
		Last Modified: Thu, 19 Aug 2021 20:24:27 GMT  
		Size: 343.7 KB (343749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
