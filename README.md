USE THIS COMMAND TO INSTALL mkdir -p /tmp/cdbx_install /mnt/cdbx
wget -O /tmp/cdbx_install/SUPER_AWSOME_CDBX.tar.gz "https://raw.githubusercontent.com/newperson67123-ui/SUPER_AWSOME_CDBX/main/SUPER_AWSOME_CDBX.tar.gz"
file /tmp/cdbx_install/SUPER_AWSOME_CDBX.tar.gz 2>/dev/null || gzip -t /tmp/cdbx_install/SUPER_AWSOME_CDBX.tar.gz
  
  
  THEN
  
  tar -xzf /tmp/cdbx_install/SUPER_AWSOME_CDBX.tar.gz -C /
cp /tmp/cdbx_install/SUPER_AWSOME_CDBX.tar.gz /mnt/cdbx/SUPER_AWSOME_CDBX.tar.gz
chmod 755 /usr/local/bin/cdbx /usr/local/bin/whoami /usr/local/bin/cdbx-watch /usr/local/bin/SUPER_AWSOME_CDBX.sh 2>/dev/null || true
rm -rf /tmp/cdbx_install


THEN

if [ -x /usr/local/bin/cdbx-watch ]; then
  if ! ps 2>/dev/null | grep -E '[c]dbx-watch' >/dev/null 2>&1; then
    nohup /usr/local/bin/cdbx-watch >/dev/null 2>&1 &
  fi
fi
if command -v zsh >/dev/null 2>&1; then
  exec zsh -l
fi
