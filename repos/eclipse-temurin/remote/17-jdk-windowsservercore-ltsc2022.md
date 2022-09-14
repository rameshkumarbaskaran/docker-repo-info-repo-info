## `eclipse-temurin:17-jdk-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:027f45199985ff774d68fd643e34f56fcdbe71b000aa11fdade5bf9683a64c55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1006; amd64

### `eclipse-temurin:17-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.1006; amd64

```console
$ docker pull eclipse-temurin@sha256:0c98b0e68ea5a3f30a04fcceebf9b3adfeccb35b5fa72e992187cdbe490f5b02
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2700702311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a796c727faea8ad42939563a8906928eed364a518484cf9a0f6f1caca376dccd`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Thu, 08 Sep 2022 20:30:55 GMT
RUN Install update 10.0.20348.1006
# Wed, 14 Sep 2022 12:09:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Sep 2022 16:17:03 GMT
ENV JAVA_VERSION=jdk-17.0.4.1+1
# Wed, 14 Sep 2022 16:17:58 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jdk_x64_windows_hotspot_17.0.4.1_1.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jdk_x64_windows_hotspot_17.0.4.1_1.msi ;     Write-Host ('Verifying sha256 (cb0a70d663fa48729f9cfa80d655214e728406a1460f2fa744b614b98972a964) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'cb0a70d663fa48729f9cfa80d655214e728406a1460f2fa744b614b98972a964') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-17' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 14 Sep 2022 16:18:19 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 14 Sep 2022 16:18:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4486102fd3820ed9527fa3e7bfefa8305c2f054e65b46dffe9675755e3d8f288`  
		Size: 910.1 MB (910085953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c5da8902b0918fe9bb0d466157622ccaf8209e4becbdd188ec41ecb563c068e6`  
		Last Modified: Wed, 14 Sep 2022 12:41:36 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31e7a87ae7360db7cb4dd9d22f1aba9b0877b8d927223283282ef075702a3bef`  
		Last Modified: Wed, 14 Sep 2022 16:51:19 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74b28a82fadf929a041e08619a1bb92193cfe3417c355fc9aa71359a79e2ce6`  
		Last Modified: Wed, 14 Sep 2022 16:51:51 GMT  
		Size: 353.2 MB (353210376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee8e03337f57f15f2ec09131dfe01ec670a02a4e82b82f390eb295299fc44f8`  
		Last Modified: Wed, 14 Sep 2022 16:51:20 GMT  
		Size: 538.2 KB (538188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4050b61a423bd41d7de88f763d4166c3ba2a91f8151e233d5954454cc46c6a79`  
		Last Modified: Wed, 14 Sep 2022 16:51:19 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
