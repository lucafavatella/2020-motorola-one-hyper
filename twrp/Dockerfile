ARG DEB_REL=bullseye
FROM debian:${DEB_REL}
ARG DEB_REL
# Package `repo` is in `contrib`.
RUN echo "deb http://deb.debian.org/debian ${DEB_REL} contrib" >/etc/apt/sources.list.d/contrib.list
RUN apt-get update && apt-get install -y --no-install-recommends \
  ca-certificates \
  openssh-client \
  repo \
  && rm -rf /var/lib/apt/lists/*
RUN groupadd -r builder && useradd --no-log-init -r -g builder -m -b /home builder
USER builder
WORKDIR /home/builder
# References:
# * https://forum.xda-developers.com/motorola-one-hyper/development/recovery-twrp-3-4-0-0-t4155573
# * https://forum.xda-developers.com/showthread.php?t=1943625
# * https://forum.xda-developers.com/motorola-one-hyper/development/rom-omnirom-t4044405
# * https://github.com/omnirom/android/blob/android-10/README.md
# * https://source.android.com/setup/build/downloading
# * https://source.android.com/setup/develop/repo
# * https://source.android.com/setup/build/building
RUN repo init -u git://github.com/omnirom/android.git -b android-10 --partial-clone --clone-filter=blob:limit=10M \
  && repo sync -c
RUN grep -R RECOVERY_VARIANT .
RUN git clone -b android-10.0 --depth 1 -- git://github.com/TeamWin/android_bootable_recovery.git bootable/recovery-twrp
RUN sh -c '. build/envsetup.sh; lunch omni_def-eng'
RUN make recoveryimage
