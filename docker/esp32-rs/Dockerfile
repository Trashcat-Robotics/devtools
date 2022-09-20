FROM espressif/idf-rust:esp32_v4.4_1.63.0.2

ENV LC_ALL=C.UTF-8
ENV LANG=C.UTF-8
ENV IDF_PATH=/home/esp/.espressif/frameworks/esp-idf-release-v4.4
ENV LIBCLANG_PATH=/home/esp/.espressif/tools/xtensa-esp32-elf-clang/esp-14.0.0-20220415-x86_64-unknown-linux-gnu/lib/

WORKDIR /usr/local/app

RUN chmod +x $IDF_PATH/install.sh
RUN /bin/bash -c $IDF_PATH/install.sh
RUN chmod +x $IDF_PATH/export.sh
RUN . $IDF_PATH/export.sh
CMD [ "/bin/bash" ]