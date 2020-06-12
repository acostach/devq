FROM nvcr.io/nvidia/l4t-base:r32.4.2

RUN apt-get update && apt-get install -y --no-install-recommends make g++
COPY ./samples /tmp/samples
COPY ./Common /tmp/Common

WORKDIR /tmp/samples/deviceQuery
RUN make clean && make

ENV NVIDIA_VISIBLE_DEVICES all
ENV NVIDIA_DRIVER_CAPABILITIES all


CMD ["bash"]
