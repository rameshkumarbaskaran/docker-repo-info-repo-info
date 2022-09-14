## `eclipse-temurin:17-jdk-windowsservercore-1809`

```console
$ docker pull eclipse-temurin@sha256:c015f991cc517e548549680686435e028e997c0f3d04b7a1e3635d3d818b7442
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3406; amd64

### `eclipse-temurin:17-jdk-windowsservercore-1809` - windows version 10.0.17763.3406; amd64

```console
$ docker pull eclipse-temurin@sha256:c9dca3edd89bf0adee8eba4f7b561c1d76151b008bd6bc6ae5a0f1da2bd54c79
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 GB (3060459069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05c0b21c94afeb091dc336600fb1fc0cee0721056c9ca6518ff7bd6861813479`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Fri, 09 Sep 2022 22:43:02 GMT
RUN Install update 10.0.17763.3406
# Tue, 13 Sep 2022 18:21:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Sep 2022 16:18:30 GMT
ENV JAVA_VERSION=jdk-17.0.4.1+1
# Wed, 14 Sep 2022 16:20:07 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jdk_x64_windows_hotspot_17.0.4.1_1.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jdk_x64_windows_hotspot_17.0.4.1_1.msi ;     Write-Host ('Verifying sha256 (cb0a70d663fa48729f9cfa80d655214e728406a1460f2fa744b614b98972a964) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'cb0a70d663fa48729f9cfa80d655214e728406a1460f2fa744b614b98972a964') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-17' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 14 Sep 2022 16:21:10 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 14 Sep 2022 16:21:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:cee64bf279e2ca8e924884a10ecb98bfa79c7f0cc8d25e73039b9aeb940815b6`  
		Size: 826.4 MB (826398623 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2bc395c8c47e61e593d2e905e0e051d40e7d25e4aeac7dbe08d3ec57acd0e68f`  
		Last Modified: Tue, 13 Sep 2022 18:25:24 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99d824488997599b99e6b698db3c5bbe0f0517e11ac4edc8c0a875483115b3cf`  
		Last Modified: Wed, 14 Sep 2022 16:52:03 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d9d410929462eac6bf03f9aa9b6ff86a5cf173db784b53044cb970f6a071e10`  
		Last Modified: Wed, 14 Sep 2022 16:52:33 GMT  
		Size: 353.0 MB (352999458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:233accd5774fcd260623de9bdd34af64e75cb65e1127f8550429f2788df0ffbc`  
		Last Modified: Wed, 14 Sep 2022 16:52:05 GMT  
		Size: 3.9 MB (3890634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:474ce98abd32aab2029c3d67dd7609ec2280e589cb6ade37aacae1e2fbc7e22e`  
		Last Modified: Wed, 14 Sep 2022 16:52:03 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
