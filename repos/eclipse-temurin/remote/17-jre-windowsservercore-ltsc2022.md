## `eclipse-temurin:17-jre-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:b36a33c7d66151f4b573202a152e449791308bc29e0547f1ec7ff0ccd7cc9d9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1906; amd64

### `eclipse-temurin:17-jre-windowsservercore-ltsc2022` - windows version 10.0.20348.1906; amd64

```console
$ docker pull eclipse-temurin@sha256:0f1b5828d203d59a62c86aeedc809be559be9ed33b3612d99b8e98920b74cbf8
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1872420640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13448e4ad01b3d0099f74bcc278eb84f3e57972bd8dad2ee335b9afcd4f2577c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 03 Aug 2023 10:01:10 GMT
RUN Install update 10.0.20348.1906
# Wed, 09 Aug 2023 23:35:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 31 Aug 2023 20:25:14 GMT
ENV JAVA_VERSION=jdk-17.0.8.1+1
# Thu, 31 Aug 2023 20:31:19 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_x64_windows_hotspot_17.0.8.1_1.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_x64_windows_hotspot_17.0.8.1_1.msi ;     Write-Host ('Verifying sha256 (80a1c1c8896ef36f1e3476340a187bb6bdcaf72c66c4b6c844722a5ba8d6a61d) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '80a1c1c8896ef36f1e3476340a187bb6bdcaf72c66c4b6c844722a5ba8d6a61d') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-17' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 31 Aug 2023 20:31:38 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22a441455ace20af58f01367d769afc2b25c3db3e4a7aee67a634d14826f6f19`  
		Last Modified: Tue, 08 Aug 2023 18:20:41 GMT  
		Size: 408.8 MB (408765102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a53d0f5bc5dd4cb7976f788ee32f7195b84c7964cb22bc38a49eb55673629149`  
		Last Modified: Thu, 10 Aug 2023 00:18:32 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ad23f073ddb50de3c226a444409e7b41a9970bfecb79d4f713b30ba22049694`  
		Last Modified: Thu, 31 Aug 2023 20:43:19 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd45130b201f2b70ced79b00cb2e6c920b3904633c2377e7d06cc32b2141420b`  
		Last Modified: Thu, 31 Aug 2023 20:45:17 GMT  
		Size: 74.8 MB (74775071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aecf060171f3bca57acdccd0df43b86f7d8f476660eeb50932943d661f28b93b`  
		Last Modified: Thu, 31 Aug 2023 20:45:08 GMT  
		Size: 278.8 KB (278840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
