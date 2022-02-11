## `eclipse-temurin:11-jre-windowsservercore-1809`

```console
$ docker pull eclipse-temurin@sha256:b72123b377647d87eca050d58e78366e6ad699ee973758932926f83aa9b52796
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2565; amd64

### `eclipse-temurin:11-jre-windowsservercore-1809` - windows version 10.0.17763.2565; amd64

```console
$ docker pull eclipse-temurin@sha256:59ae83697c933f6f4963174aee84f7242e4b5593380a913d166300e7671d7849
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2787721540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07fd5c7c65c58a668a13a8dae36db0cdca97fd29e6810772c4b16da6c2cb8c05`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 02 Feb 2022 19:28:56 GMT
RUN Install update 1809-amd64
# Wed, 09 Feb 2022 13:09:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 10 Feb 2022 20:18:47 GMT
ENV JAVA_VERSION=jdk-11.0.14.1+1
# Thu, 10 Feb 2022 20:26:19 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_x64_windows_hotspot_11.0.14.1_1.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_x64_windows_hotspot_11.0.14.1_1.msi ;     Write-Host ('Verifying sha256 (8559c143021508f70885adc84b5be4ce56e4fe7d9d2b74ac45fc2effc841b92d) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '8559c143021508f70885adc84b5be4ce56e4fe7d9d2b74ac45fc2effc841b92d') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 10 Feb 2022 20:27:21 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1bd78008c728d8f9e56dc2093e6eb55f0f0b1aa96e5d0c7ccc830c5f60876cdf`  
		Size: 995.4 MB (995381853 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f0c1566a9285d9465334dc923e9d6fd93a51b3ef6cb8497efcacbcf64e3b93fc`  
		Last Modified: Wed, 09 Feb 2022 13:26:13 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc27bdddb8879204876f5a95dbc73c22b95baab525c7b3ed1d06350acee9468c`  
		Last Modified: Thu, 10 Feb 2022 20:46:09 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc83f01c5db8f8139bad3c38a29133ebf52351b0ecdab2f7b79460f76af2982b`  
		Last Modified: Thu, 10 Feb 2022 20:49:12 GMT  
		Size: 73.7 MB (73663830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e759524cbb995bb26ca71e135c2dae375de83d679dd226b9e481ef29f35ec0f`  
		Last Modified: Thu, 10 Feb 2022 20:49:02 GMT  
		Size: 340.2 KB (340234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
