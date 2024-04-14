# noVNC Display Container for ROS2-Humble

## Getting Started
> [!NOTE]
> If you encounter an apt-related error, try changing the mirror URL.

### 1. Build Image
```bash
docker build --no-cache -t ros-vnc .
```

### 2. Run Container
```bash
docker run -itd -p 8080:8080 --name ros-vnc ros-vnc
```

### 3. Enjoy ROS2 in your Docker container!
Run `rviz2` and connect to http://localhost:8080 to test your environment.
```bash
rviz2
```
