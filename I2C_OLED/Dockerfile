ARG BUILD_FROM
FROM $BUILD_FROM

# Install requirements for add-on
RUN \
  apk add --no-cache \
    git \
    python3 \
    py3-pip \
    py3-pillow \
    py3-smbus

RUN git clone https://github.com/georgegougoudis/rpi_i2c_oled.git /I2C_OLED

RUN pip3 install luma.oled --break-system-packages

COPY run.sh /
WORKDIR /data
RUN chmod a+x /run.sh
CMD [ "/run.sh" ]
