# noVNC Display Container for ROS2-Humble

## Getting Started
> [!NOTE]
> If you encounter an apt-related error, try changing the mirror URL.

### 1. Clone repository
```bash
git clone https://github.com/hi-jin/ros-humble-novnc.git
cd ros-humble-novnc
```

### 2. Build Image
```bash
docker build --no-cache -t ros-vnc .
```

### 3. Run Container
```bash
docker run -itd -p 8080:8080 --name ros-vnc ros-vnc
```

### 4. Enjoy ROS2 in your Docker container!
Connect to http://localhost:8080/vnc.html and run `rviz2` to test your environment.
```bash
rviz2
```
