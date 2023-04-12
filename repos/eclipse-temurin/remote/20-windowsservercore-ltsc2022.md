## `eclipse-temurin:20-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:0157bdc64a46fe6bf7748ec8693ff3d52ad8ef1e73343b94d32fb3c990e10f6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1668; amd64

### `eclipse-temurin:20-windowsservercore-ltsc2022` - windows version 10.0.20348.1668; amd64

```console
$ docker pull eclipse-temurin@sha256:2b4d9886cc257bf49cab21bec51b66af00f43f0fde1fd6bcaf9f33331cbbe61b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2133064482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49c2a8bc7575c358bd8ebb8aa71f220ba7536a43636e7c4bd49d0b79a1656f43`
-	Default Command: `["jshell"]`
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
# Wed, 12 Apr 2023 01:32:15 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin20-binaries/releases/download/jdk-20%2B36/OpenJDK20U-jdk_x64_windows_hotspot_20_36.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin20-binaries/releases/download/jdk-20%2B36/OpenJDK20U-jdk_x64_windows_hotspot_20_36.msi ;     Write-Host ('Verifying sha256 (d4e41a6fce8f86dabb0422231f4723579021479eb9331cd9d07fb01c4126a022) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'd4e41a6fce8f86dabb0422231f4723579021479eb9331cd9d07fb01c4126a022') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-20' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 12 Apr 2023 01:32:52 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 12 Apr 2023 01:32:53 GMT
CMD ["jshell"]
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
	-	`sha256:df363820becc7be9e8bce15ca46df41b8aa9850c6501babe8b0cc035e629c41e`  
		Last Modified: Wed, 12 Apr 2023 09:43:03 GMT  
		Size: 369.9 MB (369901786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6acba9768aa39a38bdc95f1e3de4e0856d6c9e9e5c10e9236d6ea6d6b278a76e`  
		Last Modified: Wed, 12 Apr 2023 09:42:29 GMT  
		Size: 556.6 KB (556571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d8be52af623db4fbcb34ffd4200c9c214a5c7a466495eb4b23a721f4b69c701`  
		Last Modified: Wed, 12 Apr 2023 09:42:28 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
