## `eclipse-temurin:17-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:df4d36f64c981d38c03bbf616e1577fa0673b3a9ed6d8684995ba804ddc8595d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1906; amd64

### `eclipse-temurin:17-windowsservercore-ltsc2022` - windows version 10.0.20348.1906; amd64

```console
$ docker pull eclipse-temurin@sha256:495a0dca1ba1303f3448a69a0294bbf8ab9c2c30b8d9aaa11a006765940bc2cc
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2150844608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de2ebb063def72b770bc509ef798820c0a82722b33e0af812c636b333012269b`
-	Default Command: `["jshell"]`
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
# Thu, 31 Aug 2023 20:26:17 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_x64_windows_hotspot_17.0.8.1_1.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_x64_windows_hotspot_17.0.8.1_1.msi ;     Write-Host ('Verifying sha256 (430bc8e8f25d4d41b21ab9a8a0008db36b97f9f70863b300628a95e9692efcaa) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '430bc8e8f25d4d41b21ab9a8a0008db36b97f9f70863b300628a95e9692efcaa') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-17' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 31 Aug 2023 20:26:39 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Thu, 31 Aug 2023 20:26:40 GMT
CMD ["jshell"]
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
	-	`sha256:b63b14e001af1d1180daab2af8fe2b1be755653e2819a8b579dc3e7efa4c236c`  
		Last Modified: Thu, 31 Aug 2023 20:43:46 GMT  
		Size: 353.2 MB (353188004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e03326327052c75a75ed157b3a5fdf3e3db119db026b35ad83d3459c64ea65c`  
		Last Modified: Thu, 31 Aug 2023 20:43:19 GMT  
		Size: 288.5 KB (288476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35eae7f2b4c07a87c7e356ae1973ace6fb455a49cd32ef1ab74e77632da24ca2`  
		Last Modified: Thu, 31 Aug 2023 20:43:19 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
