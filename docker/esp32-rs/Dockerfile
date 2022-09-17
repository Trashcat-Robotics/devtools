FROM espressif/idf-rust:esp32_v4.4_1.63.0.2

ENV LC_ALL=C.UTF-8
ENV LANG=C.UTF-8
ENV IDF_PATH=/home/esp/.espressif/frameworks/esp-idf-release-v4.4

WORKDIR /usr/local/app

RUN chmod +x /home/esp/export-esp.sh
RUN /bin/bash -c /home/esp/export-esp.sh

CMD [ "/bin/bash" ]