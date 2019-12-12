## `adoptopenjdk:13-openj9-windowsservercore-1803`

```console
$ docker pull adoptopenjdk@sha256:750e1f49bdfcc1caa2cf352e3a95a73f6db65f1506fb1269a3cbb0e720df5986
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17134.1184; amd64

### `adoptopenjdk:13-openj9-windowsservercore-1803` - windows version 10.0.17134.1184; amd64

```console
$ docker pull adoptopenjdk@sha256:5c8cae35a85dcaa3520cf6cc7a477fd0a246579d0b5987932dbed3738c5e2ec1
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2753281319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d378b73e7ce6b3ed415325d3e62616c062c8836723b27cb34e71eca6a4adc8e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 12 Apr 2018 09:20:54 GMT
RUN Apply image 1803-RTM-amd64
# Wed, 04 Dec 2019 15:21:18 GMT
RUN Install update 1803-amd64
# Wed, 11 Dec 2019 20:25:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2019 21:51:59 GMT
ENV JAVA_VERSION=jdk-13.0.1+9_openj9-0.17.0
# Wed, 11 Dec 2019 21:55:09 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9_openj9-0.17.0/OpenJDK13U-jdk_x64_windows_openj9_13.0.1_9_openj9-0.17.0.msi ...');         [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;         wget https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9_openj9-0.17.0/OpenJDK13U-jdk_x64_windows_openj9_13.0.1_9_openj9-0.17.0.msi -O 'openjdk.msi';         Write-Host ('Verifying sha256 (bdcd3349615c7f6ab2102686d2ed1704b1e033bbbb227d278b9c280913af778f) ...');         if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'bdcd3349615c7f6ab2102686d2ed1704b1e033bbbb227d278b9c280913af778f') {                 Write-Host 'FAILED!';                 exit 1;         };                 New-Item -ItemType Directory -Path C:\temp | Out-Null;                 Write-Host 'Installing using MSI ...';         Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',         '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;         Write-Host 'Removing openjdk.msi ...';         Remove-Item openjdk.msi -Force;         Remove-Item -Path C:\temp -Recurse | Out-Null;
# Wed, 11 Dec 2019 21:55:11 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+UseContainerSupport -XX:+IdleTuningCompactOnIdle -XX:+IdleTuningGcOnIdle
# Wed, 11 Dec 2019 21:55:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d9e8b01179bfc94a5bdb1810fbd76b999aa52016001ace2d3a4c4bc7065a9601`  
		Last Modified: Tue, 18 Sep 2018 22:43:55 GMT  
		Size: 1.7 GB (1659688273 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d117323cd539488e5ef3bef575a41fa714d83119b0da1896607d96ec2a5e3b52`  
		Size: 696.9 MB (696873564 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:76b68c2d6c99fac63a7998081753df26697a83f71d1138943905bde6cb959583`  
		Last Modified: Wed, 11 Dec 2019 22:12:46 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:052354ee9db4276e1545c772825eb58308f883567b67d241eb8d2446b95f13f4`  
		Last Modified: Wed, 11 Dec 2019 22:42:20 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddf81e0cc5d4d24749021a64fec91ba79331b52ed4c9e00a02fba70d69f1e73a`  
		Last Modified: Wed, 11 Dec 2019 22:43:09 GMT  
		Size: 396.7 MB (396714847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35cbb1b56db27293739d2ab21b53de1964d82b2ebcae9117cd6edfba323f4471`  
		Last Modified: Wed, 11 Dec 2019 22:42:20 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7f6ae01f6084da37abf9b8ec25b0a04420144b57430ebe8b9267d3811463ed0`  
		Last Modified: Wed, 11 Dec 2019 22:42:20 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
