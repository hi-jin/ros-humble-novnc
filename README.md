# noVNC Display Container for ROS2-Humble

## Getting Started
> [!NOTE]
> If you encounter an apt-related error, try changing the mirror URL.

### 1. Clone repository
```bash
git clone https://github.com/hi-jin/ros-humble-novnc.git
cd ros-humble-novnc
```

### 2. Install colima
```bash
brew install colima
```

### 3. Start colima
```bash
colima start --arch aarch64 --vm-type=vz --vz-rosetta
```

### 4. Build Image
```bash
docker build --platform linux/amd64 --no-cache -t ros-vnc .
```

### 5. Run Container
```bash
docker run --platform linux/amd64 -itd -p 8080:8080 --name ros-vnc ros-vnc
```

### 6. Enjoy ROS2 in your Docker container!
Connect to http://localhost:8080/vnc.html and run `rviz2` to test your environment.
```bash
rviz2
```

### 7. (Optional) Do you want to run gazebo in the container?
```bash
curl -sSL http://get.gazebosim.org | sh
```

and then,

```bash
gazebo
```
