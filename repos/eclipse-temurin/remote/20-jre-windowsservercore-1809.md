## `eclipse-temurin:20-jre-windowsservercore-1809`

```console
$ docker pull eclipse-temurin@sha256:e2281854e2cbebb4f37ba64041555516abe23359a815986022a6d487cfe50e82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4252; amd64

### `eclipse-temurin:20-jre-windowsservercore-1809` - windows version 10.0.17763.4252; amd64

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
