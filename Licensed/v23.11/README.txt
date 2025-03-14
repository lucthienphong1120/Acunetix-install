Setup:
1) Download Zip File and extract
3) Now install the tools: "sudo bash acunetix_xxxxx.sh"
4) Once installed let's stop its service with: "sudo systemctl stop acunetix"
5) Let's replace wvsc file:

```
sudo cp wvsc /home/acunetix/.acunetix/v_231123131/scanner/wvsc
sudo chown acunetix:acunetix /home/acunetix/.acunetix/v_231123131/scanner/wvsc
sudo chmod +x /home/acunetix/.acunetix/v_231123131/scanner/wvsc
```

6) Time to add licenses:
```
sudo rm /home/acunetix/.acunetix/data/license/*
sudo cp license_info.json /home/acunetix/.acunetix/data/license/
sudo cp wa_data.dat /home/acunetix/.acunetix/data/license/
sudo chown acunetix:acunetix /home/acunetix/.acunetix/data/license/license_info.json
sudo chown acunetix:acunetix /home/acunetix/.acunetix/data/license/wa_data.dat
sudo chmod 444 /home/acunetix/.acunetix/data/license/license_info.json
sudo chmod 444 /home/acunetix/.acunetix/data/license/wa_data.dat
sudo chattr +i /home/acunetix/.acunetix/data/license/license_info.json
sudo chattr +i /home/acunetix/.acunetix/data/license/wa_data.dat
```

7) Now let's restart acunetix:
```
sudo systemctl start acunetix
```

8) Now login back to application, and you should be able to use it
