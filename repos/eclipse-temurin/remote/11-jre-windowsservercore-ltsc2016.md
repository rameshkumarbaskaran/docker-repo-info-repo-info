## `eclipse-temurin:11-jre-windowsservercore-ltsc2016`

```console
$ docker pull eclipse-temurin@sha256:d47aedd46f018913340d64125c9d633083d85dddc21c5a7a361a933a30c35615
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.14393.4704; amd64

### `eclipse-temurin:11-jre-windowsservercore-ltsc2016` - windows version 10.0.14393.4704; amd64

```console
$ docker pull eclipse-temurin@sha256:2ea3f8a8ac929bfc509796c86e91f554924c151f24c204292e792e20f8afe2cc
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6346534769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fbe5ec3b3ccf781cb5a49ff33c49a595332d1069b471559fdda3dc8baa957d3`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 06 Oct 2021 21:16:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 13 Oct 2021 12:40:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Oct 2021 18:34:43 GMT
ENV JAVA_VERSION=jdk-11.0.12+7
# Wed, 13 Oct 2021 18:43:57 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jre_x64_windows_hotspot_11.0.12_7.msi ...');     [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12 ; Invoke-WebRequest -Uri https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jre_x64_windows_hotspot_11.0.12_7.msi -O 'openjdk.msi' ;     Write-Host ('Verifying sha256 (665c22ab930ffa8a220c92b0c08f3cc993c864d7d0ddd8971ab2d738cc03db46) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '665c22ab930ffa8a220c92b0c08f3cc993c864d7d0ddd8971ab2d738cc03db46') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 13 Oct 2021 18:45:10 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0c776a8e8e3c02d360995b7fa26a3fd7c0928965795fac57b69ff07418ab07bf`  
		Size: 2.2 GB (2202780626 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6974b1bd85ba3f9ce16d86231eced43f720fed9c13411d37584dfe7193bcde60`  
		Last Modified: Wed, 13 Oct 2021 13:27:57 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea977149b0ce644c05e569294dda38aa8475b5005943e3ab463d3a195e5570f8`  
		Last Modified: Wed, 13 Oct 2021 19:26:04 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a29e7c0e079f293f4427dd324e2d6765c346d3a2feb81fac48a374097faeb005`  
		Last Modified: Wed, 13 Oct 2021 19:35:56 GMT  
		Size: 73.5 MB (73454400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ca671876b2e296f4779128217eedd12db7bab4c69b6b7bebc39a9e02309573e`  
		Last Modified: Wed, 13 Oct 2021 19:35:46 GMT  
		Size: 311.2 KB (311235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
