## `eclipse-temurin:20-jre-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:e2b52e19b5aee42e146be73278019f37f2696941764fae23c7179fe5e0a496de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1668; amd64
	-	windows version 10.0.17763.4252; amd64

### `eclipse-temurin:20-jre-windowsservercore` - windows version 10.0.20348.1668; amd64

```console
$ docker pull eclipse-temurin@sha256:ee4482e1570cbf06c5bbe28663f1be41bb1b3c313371c2d0bf78e27c2360d119
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1841964361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9d0e061c075bee1fda683469ebba9a5237f446cd0712802659eb7de10ddb43a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Wed, 05 Apr 2023 00:38:27 GMT
RUN Install update 10.0.20348.1668
# Tue, 11 Apr 2023 23:37:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Apr 2023 01:31:00 GMT
ENV JAVA_VERSION=jdk-20+36
# Wed, 12 Apr 2023 01:38:22 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin20-binaries/releases/download/jdk-20%2B36/OpenJDK20U-jre_x64_windows_hotspot_20_36.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin20-binaries/releases/download/jdk-20%2B36/OpenJDK20U-jre_x64_windows_hotspot_20_36.msi ;     Write-Host ('Verifying sha256 (b8e923bcd2f03fa84887c14fec0c573b843c6d4b9671c3044e41706c579b4547) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'b8e923bcd2f03fa84887c14fec0c573b843c6d4b9671c3044e41706c579b4547') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-20' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 12 Apr 2023 01:38:47 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ecfa9c953d28a9da9d422b57cd0361c57c44e1faaaed7e50a2537d1c29cee1`  
		Last Modified: Wed, 12 Apr 2023 00:50:33 GMT  
		Size: 376.6 MB (376573004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98474c9b39bb0e3a2d79dca81a90952011b65d1fa352021dacd30335d1bb69f4`  
		Last Modified: Wed, 12 Apr 2023 00:49:03 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4086f086999d8787241aff1518ecfc09777cdd59e5f95d44204903bf8ab90c1`  
		Last Modified: Wed, 12 Apr 2023 09:42:28 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4078bb0e78f5d970e2cb8687df50554529a9f78b5fd6eff80dd06ae1e7151bd2`  
		Last Modified: Wed, 12 Apr 2023 09:44:50 GMT  
		Size: 78.8 MB (78802251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:403bda842ebb1641e78cb03d92c84d8a01b83ce97bfb2180a5d9db399fefb0f6`  
		Last Modified: Wed, 12 Apr 2023 09:44:39 GMT  
		Size: 557.3 KB (557275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:20-jre-windowsservercore` - windows version 10.0.17763.4252; amd64

```console
$ docker pull eclipse-temurin@sha256:01d9ce12b9851b7a9561d5d6215032717ccaf9cf3b73cd9a0eb6038581208afa
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2153242696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1995337791dd377871e5cc536395c8a87d89483487ada5a0a381e92e520a4927`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Wed, 05 Apr 2023 00:41:54 GMT
RUN Install update 10.0.17763.4252
# Tue, 11 Apr 2023 23:40:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Apr 2023 01:32:59 GMT
ENV JAVA_VERSION=jdk-20+36
# Wed, 12 Apr 2023 01:40:22 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin20-binaries/releases/download/jdk-20%2B36/OpenJDK20U-jre_x64_windows_hotspot_20_36.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin20-binaries/releases/download/jdk-20%2B36/OpenJDK20U-jre_x64_windows_hotspot_20_36.msi ;     Write-Host ('Verifying sha256 (b8e923bcd2f03fa84887c14fec0c573b843c6d4b9671c3044e41706c579b4547) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'b8e923bcd2f03fa84887c14fec0c573b843c6d4b9671c3044e41706c579b4547') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-20' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 12 Apr 2023 01:41:27 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9094c39c4b36a86359abb3da9e9d0d9c69b6930e9c7b308120310d43d63f693`  
		Last Modified: Wed, 12 Apr 2023 00:52:10 GMT  
		Size: 363.3 MB (363347289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9103f1e2cdefe8f16dae9619b88e38aa659abb17276d2362d435ad0721d3bf41`  
		Last Modified: Wed, 12 Apr 2023 00:50:55 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf58737ada6ceb6ccecf61ac725e911958369f4e22c3246ea140a32ec2727d5a`  
		Last Modified: Wed, 12 Apr 2023 09:43:18 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaffd4208b9ee93fb282a0da73d7fe1474153a4d10a7d5bcf3e314a61ce10a36`  
		Last Modified: Wed, 12 Apr 2023 09:45:11 GMT  
		Size: 78.6 MB (78562020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f32e267941e3795acadbdfbec051f5c1c3184c50a7d63f8026761b16a93d81`  
		Last Modified: Wed, 12 Apr 2023 09:45:00 GMT  
		Size: 3.4 MB (3386727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
