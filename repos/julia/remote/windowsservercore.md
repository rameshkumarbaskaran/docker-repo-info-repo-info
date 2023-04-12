## `julia:windowsservercore`

```console
$ docker pull julia@sha256:ce0a215192fd42877ed10520197b379f3057bc82a248a3f453a4b27644dcda23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1668; amd64
	-	windows version 10.0.17763.4252; amd64

### `julia:windowsservercore` - windows version 10.0.20348.1668; amd64

```console
$ docker pull julia@sha256:28a0a50713f0786df52aaa7aaba70f52a9694e8b1e6419816a86eed7a435244b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1905803216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b92ed7e89768f716abbf8ca9d751354754eeab3f4c2324a80805fffe20267ac3`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Wed, 05 Apr 2023 00:38:27 GMT
RUN Install update 10.0.20348.1668
# Tue, 11 Apr 2023 23:37:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Apr 2023 06:06:37 GMT
ENV JULIA_VERSION=1.8.5
# Wed, 12 Apr 2023 06:06:38 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.8/julia-1.8.5-win64.exe
# Wed, 12 Apr 2023 06:06:39 GMT
ENV JULIA_SHA256=866e160d46c85167d10e8a925776c2fb1cea0f668eb8c80a605842fd35ef28b5
# Wed, 12 Apr 2023 06:08:10 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 12 Apr 2023 06:08:12 GMT
CMD ["julia"]
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
	-	`sha256:6724eb207240eb9da0d97fbf9d7740ecb1616a16b9e213e53bf434d1832b4d5e`  
		Last Modified: Wed, 12 Apr 2023 06:17:16 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d305eed397afc897b41b87897ea87ac8bb76103840580231695a6ad840f55ae`  
		Last Modified: Wed, 12 Apr 2023 06:17:17 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb4ff9e636f43df2edf7efe9d3b666c2b6ae76ff436db45088cf50fdf272765f`  
		Last Modified: Wed, 12 Apr 2023 06:17:17 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e203f445be255c9cf11b96def8a31650918ed4576fca13b75f56788f03326807`  
		Last Modified: Wed, 12 Apr 2023 06:17:49 GMT  
		Size: 143.2 MB (143194040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b0a2a5614e728907d4a758d95b40c7cf8c7671b64cccf788ecd33eba633253b`  
		Last Modified: Wed, 12 Apr 2023 06:17:17 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:windowsservercore` - windows version 10.0.17763.4252; amd64

```console
$ docker pull julia@sha256:1d7c3127a0a68d943296e3b54fd29be2933e6e9eb564c6b4d939e5d6d5eef7ea
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2214200262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce8666714c619eddaf3e7c87a01d4727ad49ba715f6941b0b90795e083addba3`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Wed, 05 Apr 2023 00:41:54 GMT
RUN Install update 10.0.17763.4252
# Tue, 11 Apr 2023 23:40:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Apr 2023 06:08:22 GMT
ENV JULIA_VERSION=1.8.5
# Wed, 12 Apr 2023 06:08:23 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.8/julia-1.8.5-win64.exe
# Wed, 12 Apr 2023 06:08:23 GMT
ENV JULIA_SHA256=866e160d46c85167d10e8a925776c2fb1cea0f668eb8c80a605842fd35ef28b5
# Wed, 12 Apr 2023 06:10:40 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 12 Apr 2023 06:10:42 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9094c39c4b36a86359abb3da9e9d0d9c69b6930e9c7b308120310d43d63f693`  
		Last Modified: Wed, 12 Apr 2023 00:52:10 GMT  
		Size: 363.3 MB (363347289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9103f1e2cdefe8f16dae9619b88e38aa659abb17276d2362d435ad0721d3bf41`  
		Last Modified: Wed, 12 Apr 2023 00:50:55 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b19c66c39719cb638439a294fbca206b5f12a5a2efee2a8a38074e39c0c7fb5`  
		Last Modified: Wed, 12 Apr 2023 06:18:02 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f139b8e77eda87e178a285dbd0134eb3d8074a72e99a0b6808ef13ca40b1195f`  
		Last Modified: Wed, 12 Apr 2023 06:18:02 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:340b3feecbf2028af8ac66d83a10f934ff5ea0158c11303b93c089c3ccba47ec`  
		Last Modified: Wed, 12 Apr 2023 06:18:02 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f641384c9c547b6a55a6b169f4c3890153c293518780912b4e873c04e013b10b`  
		Last Modified: Wed, 12 Apr 2023 06:18:35 GMT  
		Size: 142.9 MB (142901953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b65cf86844452ed64f0a478eb6e8b860ff646542d973f8198d3c7b727a76ea4`  
		Last Modified: Wed, 12 Apr 2023 06:18:02 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
