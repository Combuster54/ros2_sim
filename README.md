# Start Docker

```
sudo apt-get update
sudo apt-get install docker.io docker-compose
sudo service docker start
```

```
sudo usermod -aG docker $USER
newgrp docker
```

## Clone tortoise_ros2_bringup repository

```
cd ~/ros2_ws/src
git clone https://github.com/Combuster54/tortoise_ros2_bringup_sim.git
```

### Launch Docker Compose

```
cd ~/ros2_ws/src/tortoise_ros2_bringup_sim/
docker-compose up
```

### move robot with teleop and build your map

```
newgrp docker
docker exec -it tortoisebot-ros2-slam bash
ros2 run teleop_twist_keyboard teleop_twist_keyboard
```