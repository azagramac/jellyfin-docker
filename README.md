[![GitHub Release](https://img.shields.io/github/v/release/linuxserver/docker-jellyfin.svg?color=7871ca&labelColor=a160c4&logoColor=ffffff&style=for-the-badge&logo=jellyfin)](https://github.com/linuxserver/docker-jellyfin/releases)

<p align="center">
  <img src="https://github.com/user-attachments/assets/6bd41850-df81-4184-8102-a1d2df8373aa" width="300" title="logo_jf">
</p>

### Requeriments
- Service docker running
  
| Architecture | Available |
| :----: | :----: |
| x86-64 | ✅ |
| amd64 | ✅ |
| aarch64 | ✅ |
| arm64v8 | ✅ |
| arm64v9 | ✅ |
| x86 | ❌ | |
| armhf | ❌ | |
| armv7 | ❌ | |

### Compatible with NAS that have the ability to run docker containers 
| Hardware | Available |
| :----: | :----: |
| Synology | ✅ |
| QNAP | ✅ |
| Asustor | ✅ |


### Install Docker (Skip this step if you are using one of the NAS mentioned above.)
    sudo update && sudo apt upgrade -y
    sudo apt install git vim wget curl net-tools ca-certificates gnupg
    curl -fsSL https://download.docker.com/linux/debian/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
    echo  "deb [arch="$(dpkg --print-architecture)" signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/debian \
	"$(. /etc/os-release && echo "$VERSION_CODENAME")" stable" | tee /etc/apt/sources.list.d/docker.list > /dev/null
    sudo apt update
    sudo apt install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin -y
    sudo usermod -aG docker $USER
    sudo apt install docker-compose-plugin -y

### Clone repo
    git clone https://github.com/azagramac/jellyfin-docker.git
    cd jellyfin-docker

### Running
    docker compose up -d

### Output
    $ docker compose up -d
    [+] Running 9/9
     ✔ jellyfin Pulled                                                                                                                                                                                                                             23.2s 
       ✔ 6d29a096dd42 Pull complete                                                                                                                                                                                                                  4.5s 
       ✔ ac69bd919a82 Pull complete                                                                                                                                                                                                                  5.2s 
       ✔ 2a534069771d Pull complete                                                                                                                                                                                                                  5.7s 
       ✔ 4f4fb700ef54 Pull complete                                                                                                                                                                                                                  5.9s 
       ✔ df1c06f9ce74 Pull complete                                                                                                                                                                                                                 10.6s 
       ✔ f9ec95325cc7 Pull complete                                                                                                                                                                                                                 10.9s 
       ✔ f71b44280505 Pull complete                                                                                                                                                                                                                 21.8s 
       ✔ 8ce81773582a Pull complete                                                                                                                                                                                                                 44.0s 
    [+] Running 2/2
     ✔ Network jellyfin_default  Created                                                                                                                                                                                                            0.4s 
     ✔ Container jellyfin        Started

### Check
    docker ps -a

### Output
    $ docker ps -a
    CONTAINER ID   IMAGE                         COMMAND                CREATED       STATUS                    PORTS                  NAMES
    3cb4d0ec5b2c   jellyfin/jellyfin:latest     "/jellyfin/jelly…"    7 days ago    Up 18 hours (healthy)                              jellyfin


### Download App
<a href="https://play.google.com/store/apps/details?id=org.jellyfin.mobile"><img src="https://lh3.googleusercontent.com/q1k2l5CwMV31JdDXcpN4Ey7O43PxnjAuZBTmcHEwQxVuv_2wCE2gAAQMWxwNUC2FYEOnYgFPOpw6kmHJWuEGeIBLTj9CuxcOEeU8UXyzWJq4NJM3lg=s0" width="130px"></a>  <a href="https://apps.apple.com/us/app/jellyfin-mobile/id1480192618"><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/3/3c/Download_on_the_App_Store_Badge.svg/640px-Download_on_the_App_Store_Badge.svg.png" width="130px"></a>
