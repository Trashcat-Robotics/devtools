FROM espressif/idf:latest

ENV LC_ALL=C.UTF-8
ENV LANG=C.UTF-8
ENV IDF_PATH=/opt/esp/idf
ENV CXX=/usr/bin/clang

WORKDIR /usr/local/app

RUN apt-get update -y
RUN apt-get install -y \
    clang-format clang-tidy clang-tools clang clangd \
    libc++-dev libc++1 libc++abi-dev libc++abi1 \
    libclang-dev libclang1 liblldb-dev libllvm-ocaml-dev \
    libomp-dev libomp5 lld lldb llvm-dev llvm-runtime llvm \
    python3-clang python3-pip curl

RUN curl -fsSL https://deb.nodesource.com/setup_18.x | bash
RUN apt-get install -y nodejs
RUN rm -rf /var/lib/apt/lists/*

# Dev Flow Dependencies
RUN python3 -m pip install pre-commit
RUN npm install -g eclint

RUN . $IDF_PATH/export.sh

CMD [ "/bin/bash" ]
