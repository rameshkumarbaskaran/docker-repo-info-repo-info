## `eclipse-temurin:11-jre-windowsservercore-1809`

```console
$ docker pull eclipse-temurin@sha256:fedc6eb7bc9c9c956e148fbd4a0bcdbf08d76fc87130e404b7e99760321531e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3046; amd64

### `eclipse-temurin:11-jre-windowsservercore-1809` - windows version 10.0.17763.3046; amd64

```console
$ docker pull eclipse-temurin@sha256:ea3c910a9e6cb7405d2b312d1cd9da2e905d9934638acbd23e760faa1afd1d7f
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2737304852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bd4ed5880203a3f411a1e0d5382a6ab05e77b48bef7ae9ae6f9506ecf67396d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Thu, 09 Jun 2022 19:41:03 GMT
RUN Install update 10.0.17763.3046
# Wed, 15 Jun 2022 12:18:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Jun 2022 17:38:20 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Wed, 15 Jun 2022 17:45:00 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_windows_hotspot_11.0.15_10.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_windows_hotspot_11.0.15_10.msi ;     Write-Host ('Verifying sha256 (8072ed7f0235920022bd49b104cc79652d0f01cdec608848a73a320c6192ad77) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '8072ed7f0235920022bd49b104cc79652d0f01cdec608848a73a320c6192ad77') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 15 Jun 2022 17:46:00 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fc6ae6c5aa2b4920ae68469c5e7e7c3a3c85e5eaafc24660e7b3adb21d6fce77`  
		Size: 786.1 MB (786113785 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4ed911f97ae3a2a6279c70738e5692b14369ac11871a2bbd2f6ad301419527ad`  
		Last Modified: Wed, 15 Jun 2022 12:50:13 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e42772302c660d781d60a5d1fd19a72d3fb213253234584d4e78caa37f1262c3`  
		Last Modified: Wed, 15 Jun 2022 18:34:46 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bcc33bb0c8e83a892156722c8003c754a3c77019f3128bfa28e8b6b26372dd4`  
		Last Modified: Wed, 15 Jun 2022 18:39:49 GMT  
		Size: 73.7 MB (73702739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a815a9fe9074b4c5560080d4b4d3dbec14984348f28de9260707faec13014079`  
		Last Modified: Wed, 15 Jun 2022 18:39:38 GMT  
		Size: 319.5 KB (319501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
