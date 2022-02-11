## `eclipse-temurin:17-windowsservercore-1809`

```console
$ docker pull eclipse-temurin@sha256:375757ce9094a0c8c9175d3213ae7d6754fd13b3b556d9dcfbf9ef6f6e495a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2565; amd64

### `eclipse-temurin:17-windowsservercore-1809` - windows version 10.0.17763.2565; amd64

```console
$ docker pull eclipse-temurin@sha256:a7af6f93135c463aeb48aec1e406693c28f5a4c6f4e02b49fef3846e1bb631e8
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 GB (3069960010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51e213c9143294c0753cbad8bc26ba0c5af225418a3c59a01859a1ff1c7af26b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 02 Feb 2022 19:28:56 GMT
RUN Install update 1809-amd64
# Wed, 09 Feb 2022 13:09:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Feb 2022 20:10:59 GMT
ENV JAVA_VERSION=jdk-17.0.2+8
# Wed, 09 Feb 2022 20:13:13 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jdk_x64_windows_hotspot_17.0.2_8.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jdk_x64_windows_hotspot_17.0.2_8.msi ;     Write-Host ('Verifying sha256 (f66f21f0b25e4fe0449c41555dbeb7ba890d54e5a6e48e35b1a6309409eaf2d1) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'f66f21f0b25e4fe0449c41555dbeb7ba890d54e5a6e48e35b1a6309409eaf2d1') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-17' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 09 Feb 2022 20:14:14 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 09 Feb 2022 20:14:16 GMT
CMD ["jshell"]
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
	-	`sha256:eb6814b2f18a0f247e5f7477657e251a2616cfbf5e3e0164a012f053fa888c86`  
		Last Modified: Thu, 10 Feb 2022 21:06:27 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a83e2986a6f717db81aa11741e44ba42371f12ddc0cae26f2e4beb48674b83e`  
		Last Modified: Thu, 10 Feb 2022 21:12:37 GMT  
		Size: 352.3 MB (352337594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae1914c916b997948b99f73ec747aac2a73cf3d5632df765b211178674345943`  
		Last Modified: Thu, 10 Feb 2022 21:06:31 GMT  
		Size: 3.9 MB (3903406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4611955f89a1d4831809cf20ebd0c8a356100b30f82c95e42d48d0ac3cbab989`  
		Last Modified: Thu, 10 Feb 2022 21:06:26 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
