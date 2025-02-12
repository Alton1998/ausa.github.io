# Installing IoT Edge for Raspberry pi
## Steps for setting up raspberry pi
1. Install Raspberry pi imager
2. Install Debian 12 which is bookworm.
3. Remember to set the Wifi and password and enable SSH
4. After imaging try to ssh into your raspberry pi to enable vnc server if you need to use it. Refer the following link: https://www.pitunnel.com/doc/access-vnc-remote-desktop-raspberry-pi-over-internet

## Steps for installing iot Edge
https://learn.microsoft.com/en-us/azure/iot-edge/how-to-provision-devices-at-scale-linux-x509?tabs=individual-enrollment%2Cdebian#install-iot-edge - The tutorial is for debian 11 if using 12 just replace the numbers in the urls

## Create IoT Hub and DPS 

To create IoT Hub use the terraform script here - https://github.com/Alton1998/ausa-infra add the necessary details in the `providers.tf` file
```
cd DPS
terraform init
terraform plan
terraform apply
```

## Creating Certificates

Follow this to create three Certificates: https://learn.microsoft.com/en-us/azure/iot-dps/tutorial-custom-hsm-enrollment-group-x509?pivots=programming-language-csharp#create-an-x509-certificate-chain

Add the root certificate to the Certificates.
Add the CA Certificates to the enrollment group
Add the device full chain certificates to the device.

## Developing modules
https://learn.microsoft.com/en-us/azure/iot-edge/tutorial-develop-for-linux?tabs=python&pivots=iotedge-dev-cli

