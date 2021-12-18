## `hylang:python3.9-windowsservercore-ltsc2016`

```console
$ docker pull hylang@sha256:84b206b153845ca50413fe034d9ac8f654507f3a087dbfe10d0a0b3b47aeca62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.14393.4770; amd64

### `hylang:python3.9-windowsservercore-ltsc2016` - windows version 10.0.14393.4770; amd64

```console
$ docker pull hylang@sha256:b081959aaaaa9a0f4578662ce9c12de31951dd34d111b673217ba3a64e970a65
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6330313193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9ff034e85d90199acf6a5fbf4a27e7fc0094ba8a6f5f507635e2a69e2450503`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 03 Nov 2021 23:35:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Nov 2021 01:53:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Nov 2021 01:53:27 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 16 Nov 2021 18:22:34 GMT
ENV PYTHON_VERSION=3.9.9
# Tue, 16 Nov 2021 18:22:35 GMT
ENV PYTHON_RELEASE=3.9.9
# Tue, 16 Nov 2021 18:24:43 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		Write-Host 'Complete.'
# Tue, 16 Nov 2021 18:24:45 GMT
ENV PYTHON_PIP_VERSION=21.2.4
# Tue, 16 Nov 2021 18:24:46 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Tue, 16 Nov 2021 18:24:47 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3cb8888cc2869620f57d5d2da64da38f516078c7/public/get-pip.py
# Tue, 16 Nov 2021 18:24:48 GMT
ENV PYTHON_GET_PIP_SHA256=c518250e91a70d7b20cceb15272209a4ded2a0c263ae5776f129e0d9b5674309
# Tue, 16 Nov 2021 18:26:19 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 		('setuptools=={0}' -f $env:PYTHON_SETUPTOOLS_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 16 Nov 2021 18:26:20 GMT
CMD ["python"]
# Fri, 17 Dec 2021 23:09:58 GMT
ENV HY_VERSION=1.0a3
# Fri, 17 Dec 2021 23:12:17 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION)
# Fri, 17 Dec 2021 23:12:18 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b07c368b7a04669b63c6c86a881be270ee967474a85892003b8695df3d0d5874`  
		Size: 2.2 GB (2203104946 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:68d5dfbca608972a02b334e8d053010ece888346d5ebabfc28c9f91ed2063b15`  
		Last Modified: Wed, 10 Nov 2021 02:10:39 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eee32b722eae60843ab69b9a429e222c325d19f4554fc09616632500513b4739`  
		Last Modified: Wed, 10 Nov 2021 02:10:38 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2289f841cad5817e9b44da03e2b5c6bd299942120da2b5a8417192b59abe4638`  
		Last Modified: Tue, 16 Nov 2021 18:28:09 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ec3002d69e588f7ce9da0ebd3098ef8e1ba32bce148ad956b7b0671c4dccb42`  
		Last Modified: Tue, 16 Nov 2021 18:28:09 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:549ea47f400be7a6661b264fdb26f2714a242a4f52ab645e3e01c35ebdf873f1`  
		Last Modified: Tue, 16 Nov 2021 18:28:15 GMT  
		Size: 49.6 MB (49590637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8788eee99d1be5bbfa9bb0ee00612f888c78a44938c94b3c1ed0ccda8e48a8af`  
		Last Modified: Tue, 16 Nov 2021 18:28:09 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18b0d9a2a8d84a7049b9379fb92943bbeb5a939f27a3f65babb31d456e86dbc1`  
		Last Modified: Tue, 16 Nov 2021 18:28:06 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd6f091068f8c4b774dca1099e719ef9382044c644639d849c7f54db0b65600d`  
		Last Modified: Tue, 16 Nov 2021 18:28:06 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f613f292c6024e130236ec74875fe63998e3e23aa3b00a25d893ae2d47fba0`  
		Last Modified: Tue, 16 Nov 2021 18:28:06 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:455ad1dd919cce1ad597ae462c4f9e941b78fe3a07811cfdedbad9256dc37a08`  
		Last Modified: Tue, 16 Nov 2021 18:28:08 GMT  
		Size: 6.3 MB (6296231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa5cdae8c5cf0c5ecbb55fb4550ea459eb0afdc5dab146c911e865e3f93f5eca`  
		Last Modified: Tue, 16 Nov 2021 18:28:06 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87923b4873228fac5e681b4361387719c794fd40e982379f958d0880d17bed76`  
		Last Modified: Fri, 17 Dec 2021 23:18:42 GMT  
		Size: 1.4 KB (1385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc283012ed79fc66b585c162f392a1e4019e1d65425c333c52e4b147f3a582a1`  
		Last Modified: Fri, 17 Dec 2021 23:18:43 GMT  
		Size: 1.3 MB (1319955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba0a86bf6b075a5c232f569a2ee38be0887d805d21373b3f49ea6650ce60985d`  
		Last Modified: Fri, 17 Dec 2021 23:18:42 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
