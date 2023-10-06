# MQTT_ApacheMosquitto_DynamicSecurityPlugin

persistence true

persistence_location /var/lib/mosquitto/


log_dest file /var/log/mosquitto/mosquitto.log

include_dir /etc/mosquitto/conf.d

listener 1883

allow_anonymous false

peer_listener_settings false


plugin /usr/lib/x86_64-linux-gnu/mosquitto_dynamic_security.so

plugin_opts_config_file /var/lib/mosquitto/dynamic-security.json

pid_file /run/mosquitto/mosquitto.pid
