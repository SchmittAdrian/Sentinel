# Sentinel
Sentinel - Camera Monitoring System

Overview

Sentinel is a camera monitoring system developed in Python, utilizing the Ultralytics YOLO library for real-time object detection. The system features a graphical interface built with the Flet framework and integrates with a MySQL database for camera management.

## Features

- Real-time Visualization: The system allows real-time viewing of registered cameras, highlighting detected objects in the image.

- Camera Registration: It is possible to register new cameras, providing a number, establishment name, address, environment, and contact associated with each one.

- Camera Deletion: Registered cameras can be removed from the system.

- Recording Explorer: The system has a button that opens the file explorer in the recordings folder, facilitating access to video records.

- Light/Dark Mode: The system offers the option to switch between light and dark modes for better user preference adaptation.

## Prerequisites

Before running the system, make sure to have the following dependencies installed:

- Python 3.x
- OpenCV
- Ultralytics YOLO
- Flet
- MySQL Connector
- Winsound (for Windows)

## Database Configuration

The system uses a MySQL database to store camera information. Make sure to correctly configure the credentials in the backend.py file::

```bash
  db_connection = mysql.connector.connect(
    host="localhost",
    user="root",
    password="sua_senha",
    database="sentinel"
)
```
Use these parameters to create the database:
```bash
CREATE DATABASE sentinel;

CREATE TABLE cameras (
    numero INT PRIMARY KEY,
    localizacao VARCHAR(255),
    endereco VARCHAR(255),
    comodo VARCHAR(255),
    contato VARCHAR(255)
);
```
## Running the System
Clone the repository to your local machine:

```bash
git clone https://github.com/SchmittAdrian/Sentinel.git
cd sentinel
```
Install the dependencies:
```bash
pip install -r requirements.txt
```

Run the application:
```bash
python main.py
```
