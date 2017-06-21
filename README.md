[![Build Status](https://travis-ci.org/rileyschuit/rpi-docker-sabnzbd.svg?branch=master)](https://travis-ci.org/rileyschuit/rpi-docker-sabnzbd)  
  
# docker sabnzbd
This is a Dockerfile to set up "SABnzbd" - (http://sabnzbd.org/)
Build from docker file
```
git clone https://github.com/rileyschuit/rpi-docker-sabnzbd.git
cd rpi-docker-sabnzbd
docker build -t rpi-docker-sabnzbd .
```

```
docker run -d \
  -h *your_host_name* \
  -v /*your_config_location*:/config \
  -v /*your_videos_location*:/data \
  -e UID=*your user's numeric UID* \
  -e GID=*your user's numeric GID* \
  -p 8080:8080 \
  --restart=always sabnzbd
```

# Environment variable

- **UID**: The user's numeric UID. All downloaded files will have that UID. Default value if not present: **0** (files will belong to the user root)
- **GID**: The user's numeric GID. All downloaded files will have that GID. Default value if not present: **0** (files will belong to the group root)



