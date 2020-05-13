## `hylang:0-python3.8-windowsservercore-1809`

```console
$ docker pull hylang@sha256:4198cd2c81fcce3263830789c178f1025711a6e457ff6f91ee91358efacecc98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1217; amd64

### `hylang:0-python3.8-windowsservercore-1809` - windows version 10.0.17763.1217; amd64

```console
$ docker pull hylang@sha256:67b3beb831cdac77699fc69040d34e51656925c56dcebce4d4da665553fc7686
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1772585757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8343dad1eddf81e72c4178e0dfcbb98f1d68e428d078829a92ab8ed80bad5ee`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-amd64
# Wed, 13 May 2020 12:41:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 May 2020 15:07:32 GMT
ENV PYTHON_VERSION=3.8.2
# Wed, 13 May 2020 15:07:33 GMT
ENV PYTHON_RELEASE=3.8.2
# Wed, 13 May 2020 15:09:00 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	Start-Process python.exe -Wait 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		); 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 		Write-Host 'Complete.'
# Wed, 13 May 2020 15:09:01 GMT
ENV PYTHON_PIP_VERSION=20.1
# Wed, 13 May 2020 15:09:02 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/1fe530e9e3d800be94e04f6428460fc4fb94f5a9/get-pip.py
# Wed, 13 May 2020 15:09:03 GMT
ENV PYTHON_GET_PIP_SHA256=ce486cddac44e99496a702aa5c06c5028414ef48fdfd5242cd2fe559b13d4348
# Wed, 13 May 2020 15:09:50 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 13 May 2020 15:09:51 GMT
CMD ["python"]
# Wed, 13 May 2020 21:23:27 GMT
ENV HY_VERSION=0.18.0
# Wed, 13 May 2020 21:24:06 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION)
# Wed, 13 May 2020 21:24:07 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:77613e754ba9d62c0acd4ef271c4ee7d3af091b8c8b310afa404560a9d281f82`  
		Last Modified: Wed, 13 May 2020 13:00:20 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05fab5857724b65ce3760875976d2b25ae3b65d3a16246e15c57ae93a12b43bf`  
		Last Modified: Wed, 13 May 2020 15:19:45 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f683dd9db8121354e1b800a5322376f19e69703185c2a0cd0a5bc9832ac905f9`  
		Last Modified: Wed, 13 May 2020 15:19:44 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0872723947fa430854455aba1fb6d3c7399455fcdfec40171ba0dd2f819c2f24`  
		Last Modified: Wed, 13 May 2020 15:19:54 GMT  
		Size: 47.6 MB (47611835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0db9661fd5aa388d1b16da89d37d6e0520fa511914b5dfeff43c64040179eb64`  
		Last Modified: Wed, 13 May 2020 15:19:42 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f790438fa02e722731228861500a8fc6156c92a0e38f44c11e1d82460162aefc`  
		Last Modified: Wed, 13 May 2020 15:19:42 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb092d497657bcada80965fc454ac3ec966e75a5270cce3b7c173e6f520365d1`  
		Last Modified: Wed, 13 May 2020 15:19:42 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a046484f476a0b284c9cc3327bfbf1c42e29a415656e99fbf97f667ccead9716`  
		Last Modified: Wed, 13 May 2020 15:19:43 GMT  
		Size: 5.5 MB (5494169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a7b92a47923933a6b9791f7edf8a5d16a9132949ada6d4d2022a751e9656889`  
		Last Modified: Wed, 13 May 2020 15:19:42 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fc07801e6bbb1ed3ecab39082d641889edee16c2b629953d80e32c7edd40d08`  
		Last Modified: Wed, 13 May 2020 21:29:10 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ff367549dc2df7e429a7b6b0bdde4cc317760485b1d8024a977833a420df751`  
		Last Modified: Wed, 13 May 2020 21:29:11 GMT  
		Size: 1.1 MB (1136482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f44da0304fdf6326dd5278b5f0c79609c88395c67cf227ce49ce480bb32a3230`  
		Last Modified: Wed, 13 May 2020 21:29:10 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
