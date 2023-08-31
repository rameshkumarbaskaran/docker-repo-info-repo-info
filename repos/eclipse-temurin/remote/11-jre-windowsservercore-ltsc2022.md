## `eclipse-temurin:11-jre-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:243ac962c5479c9c89f54c5bfee0d752ce0cdb8c618108384e2abf6a10a420a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1906; amd64

### `eclipse-temurin:11-jre-windowsservercore-ltsc2022` - windows version 10.0.20348.1906; amd64

```console
$ docker pull eclipse-temurin@sha256:59e94b3719b70a59e0f96b2dfa7bdaf8b28c3fabd6ddf18aab182cc4d9d9df0e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1872179583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b80cfa183b4d0c2c9a85199aa5fc51df6dd0a32843dd93c12b711362f056534`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 03 Aug 2023 10:01:10 GMT
RUN Install update 10.0.20348.1906
# Wed, 09 Aug 2023 23:35:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 31 Aug 2023 20:15:39 GMT
ENV JAVA_VERSION=jdk-11.0.20.1+1
# Thu, 31 Aug 2023 20:21:44 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jre_x64_windows_hotspot_11.0.20.1_1.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jre_x64_windows_hotspot_11.0.20.1_1.msi ;     Write-Host ('Verifying sha256 (f25a6adf1eeb005945e3255e11ea1adbd63f00872a4c6db849b4467be5c1db4d) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'f25a6adf1eeb005945e3255e11ea1adbd63f00872a4c6db849b4467be5c1db4d') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 31 Aug 2023 20:22:05 GMT
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
	-	`sha256:9c55d27186c0c2085aa3ebdff762831cca06b2f87657e25fe02d9ff51622068c`  
		Last Modified: Thu, 31 Aug 2023 20:40:36 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9669381a285b3d96000b1427d37c35e05e85e4d388aa48602eec8ece2301d79`  
		Last Modified: Thu, 31 Aug 2023 20:42:33 GMT  
		Size: 74.5 MB (74520631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba255e4740bcc9da20c52eb1b8021c53c02fc5cdcf1d6dc5fa7991145d65caec`  
		Last Modified: Thu, 31 Aug 2023 20:42:24 GMT  
		Size: 292.2 KB (292225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
