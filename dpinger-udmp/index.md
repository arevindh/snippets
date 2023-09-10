## Monitoring udm-pro networking dpinger

dpinger Docs [dennypage/dpinger](https://github.com/dennypage/dpinger)

## Customizing

Replace withe following in service file

- influx-ip
- influx-user
- influx-pass

Replace `1.1.1.1` to change the ping server.

## Install Service

`cp dmonit@.service /etc/systemd/system/dmonit@.service`

`systemctl daemon-reload`

## Enable and start service 

Replace `ppp0` and `ppp1` with wan interface names.

`systemctl enable dmonit@ppp0`

`systemctl start dmonit@ppp0`


## Optional if has two WANS 

`systemctl enable dmonit@ppp1`

`systemctl start dmonit@ppp1`
