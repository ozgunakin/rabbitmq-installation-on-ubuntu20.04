# RabbitMQ Installation on Ubuntu 20.04

This is a step by step guide for RabbitMQ installation on Ubuntu 20.04

## Step - 1 Install RabbitMQ via APT

You can directly install RabbitMQ using APT package manager. It is better to update the server before run "apt install" code.

```text
sudo apt update

sudo apt install rabbitmq-server

sudo service rabbitmq-server start

sudo systemctl enable rabbitmq-server
```

## Step - 2 Create an Admin User

We will create an admin user and give grant access to RabbitMQ . 

```text
sudo rabbitmqctl add_user admin SecurePassword

sudo rabbitmqctl set_user_tags admin administrator
```

## Step - 3 Activate RabbitMQ UI

```text
sudo rabbitmq-plugins enable rabbitmq_management

sudo service rabbitmq-server restart
```

You can reach web UI over [http://your\_IP:15672](http://your_IP:15672)



