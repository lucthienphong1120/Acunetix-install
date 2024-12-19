FROM kalilinux/kali-rolling

RUN apt-get update -y && \
    apt-get -y install libxdamage1 libgtk-3-0 libasound2 libnss3 libxss1 sudo bzip2 wget expect libxdamage1 libgtk-3-0 libasound2 libnss3 libxss1 libx11-xcb1

ADD acunetix_13.0.200715107_x64.sh /tmp/acunetix_13.0.200715107_x64.sh
RUN chmod +x /tmp/acunetix_13.0.200715107_x64.sh

ADD install.expect /tmp/install.expect
ADD wvsc /tmp/wvsc
ADD license_info.json /tmp/license_info.json

RUN cd /tmp && chmod +x /tmp/install.expect && expect /tmp/install.expect
RUN cp /tmp/wvsc /home/acunetix/.acunetix/v_200715107/scanner/
RUN cp /tmp/license_info.json /home/acunetix/.acunetix/data/license/

USER acunetix

ENTRYPOINT ["/home/acunetix/.acunetix/start.sh"]
