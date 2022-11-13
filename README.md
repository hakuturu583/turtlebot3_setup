# turtlebot3_setup playbook 

Ansible playbook for setting up Turtlebot3 image

## How to use


## Creating venv (optional but highly recommended)

The easiest way to ensure you have the right ansible and properly libs installed is to use a python venv. You only have to set it up once:

```
    python3 -m venv .env
    .env/bin/pip install --upgrade pip
    .env/bin/pip install ansible[azure]==2.9.13
```

After creating the venv you can enter it in order to use ansible (this has to be repeated once per shell session):

```
    source .env/bin/activate
```

### Running playbook locally

1. Run `ansible-galaxy install -r roles/requirements.yml -p roles` in this directory to get the required Ansible roles.
2. Run `ansible-playbook -c local -i inventory/inventory.ini turtlebot3_setup-playbook.yml --ask-become-pass -t (ROS_DISTRO) -e sd_device=(SD_DEVICE)`

ROS_DISTRO is a ROS1/ROS2 distribution name you want to install in SD card.
SD_DEVICE is a Device filename for sd card.

## License

Apache Software License 2.0

## Author

[Masaya Kataoka](mailto:ms.kataoka@gmail.com)

## Version

Release date: 2022-11-05
Version: 0.1.0