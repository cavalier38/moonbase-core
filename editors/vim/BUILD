  OPTS+=" --disable-perlinterp --disable-luainterp" &&

  cd src           &&
  default_config   &&
  make             &&
  prepare_install  &&
  rm -f /usr/bin/vim /usr/bin/vi  &&
  ( find /usr/share/vim -type d -exec rmdir {} \; &> /dev/null || true)  &&
  make install                        &&
  ln  -sf  /usr/bin/vim  /usr/bin/vi  &&
  cp -f $SCRIPT_DIRECTORY/vimrc /usr/share/vim/vim${MAJOR}/sample.vimrc
