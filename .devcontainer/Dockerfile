FROM osrf/ros:humble-desktop

ARG USERNAME=ros
RUN apt-get update && apt-get install -y sudo python3-colcon-common-extensions python3-rosdep git \
    && useradd -m -s /bin/bash -G sudo $USERNAME \
    && echo "$USERNAME ALL=(ALL) NOPASSWD:ALL" > /etc/sudoers.d/$USERNAME \
    && echo "source /opt/ros/humble/setup.bash" >> /home/$USERNAME/.bashrc \
    && echo "source /workspaces/ros2_humble_ws/ros2_ws/install/setup.bash 2>/dev/null" >> /home/$USERNAME/.bashrc \
    && rm -rf /var/lib/apt/lists/*
