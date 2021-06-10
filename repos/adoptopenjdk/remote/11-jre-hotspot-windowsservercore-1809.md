## `adoptopenjdk:11-jre-hotspot-windowsservercore-1809`

```console
$ docker pull adoptopenjdk@sha256:10ecf4f607cf7f7a63060a6fabd8c40f49da4dfeddace45d26bf0ec9af7d0a80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1999; amd64

### `adoptopenjdk:11-jre-hotspot-windowsservercore-1809` - windows version 10.0.17763.1999; amd64

```console
$ docker pull adoptopenjdk@sha256:41074f0e69b7d7ffb53672670a5716522426a3e66465acb4be921b9e2b10ca3d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2714769359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f86fcb1256cef7eb11ebc05f873c7610d57200c2ce5b15ac061063fe16aaa90d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Sun, 06 Jun 2021 04:28:43 GMT
RUN Install update 1809-amd64
# Wed, 09 Jun 2021 12:10:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Jun 2021 18:01:41 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Wed, 09 Jun 2021 18:06:56 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jre_x64_windows_hotspot_11.0.11_9.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jre_x64_windows_hotspot_11.0.11_9.msi ;     Write-Host ('Verifying sha256 (d52262a1ac6d86326cd071b687dcc5bb546bedda6d03c6bd26a046070a013df3) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'd52262a1ac6d86326cd071b687dcc5bb546bedda6d03c6bd26a046070a013df3') {             Write-Host 'FAILED!';             exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {             Write-Host 'FAILED installing MSI!' ;             exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:639bb6bb2beb4cfdcacb9f0844344448fe26494665d5fe78a494419f86fbb18f`  
		Size: 923.3 MB (923252167 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7863ef96846d497ea06fe442ea13dcecaf5c248ce238c69800475281a4fa848e`  
		Last Modified: Wed, 09 Jun 2021 12:20:41 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df0dd76638fc06d0475a891090d106195abdabd342df755f585bf3c290801a46`  
		Last Modified: Wed, 09 Jun 2021 19:07:57 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:243893949f93f48d765bf1699d23e6211617ecded35eeb6981f7833d402350cf`  
		Last Modified: Wed, 09 Jun 2021 19:17:49 GMT  
		Size: 73.2 MB (73181440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
