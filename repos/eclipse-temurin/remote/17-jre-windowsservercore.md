## `eclipse-temurin:17-jre-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:fdc1c5ab4f479333e6ae5e76e6c818d36d5a0d6c8e9dc96cfd37eec75fe467ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1906; amd64
	-	windows version 10.0.17763.4737; amd64

### `eclipse-temurin:17-jre-windowsservercore` - windows version 10.0.20348.1906; amd64

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

### `eclipse-temurin:17-jre-windowsservercore` - windows version 10.0.17763.4737; amd64

```console
$ docker pull eclipse-temurin@sha256:15febb828a36733a7429d2acb5702182963876a72bcd4044cb1388b4950bb4f2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2073962405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7579d3d470141158a2ae1f08e0e15aa78824380e15cb068eca7f4bb9b727b693`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 02 Aug 2023 09:07:15 GMT
RUN Install update 10.0.17763.4737
# Wed, 09 Aug 2023 23:36:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 31 Aug 2023 20:26:59 GMT
ENV JAVA_VERSION=jdk-17.0.8.1+1
# Thu, 31 Aug 2023 20:33:02 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_x64_windows_hotspot_17.0.8.1_1.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_x64_windows_hotspot_17.0.8.1_1.msi ;     Write-Host ('Verifying sha256 (80a1c1c8896ef36f1e3476340a187bb6bdcaf72c66c4b6c844722a5ba8d6a61d) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '80a1c1c8896ef36f1e3476340a187bb6bdcaf72c66c4b6c844722a5ba8d6a61d') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-17' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 31 Aug 2023 20:33:59 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95f433aa7d90194e65f6b08a599b3ee12292e124d47c204107baedfd71054c1`  
		Last Modified: Tue, 08 Aug 2023 18:31:16 GMT  
		Size: 345.3 MB (345334986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03d23fbbd4f650b6f60106a3cc28d711efce2f97cfb80b67e2dec305e011aa3`  
		Last Modified: Thu, 10 Aug 2023 00:19:47 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:725e8d8c56bb4169511a878a5c291fffe218ac285b4603b072f9ae6ac21dc553`  
		Last Modified: Thu, 31 Aug 2023 20:43:57 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05c74f9ae0a5d049fe1c860c981a71a040239e416fb1919ac98df82f7335b97f`  
		Last Modified: Thu, 31 Aug 2023 20:45:37 GMT  
		Size: 74.8 MB (74817498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49a26b51d737766e6bd376329579e9e69c023817f3dbaaedc272f0c7ae135558`  
		Last Modified: Thu, 31 Aug 2023 20:45:28 GMT  
		Size: 3.2 MB (3186739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
