system log file 
openssl-1.1.1 

 export ANDROID_NDK=/opt/android-ndk-r20
 export PATH=$ANDROID_NDK/toolchains/llvm/prebuilt/linux-x86_64/bin:$PATH
   ./Configure android-arm -D__ANDROID_API__=19 shared --prefix=/opt/android-openssl --openssldir=/opt/android-openssl shared
  make SHLIB_EXT=.so install_sw

android pjsip: 

$ ./aconfigure-android -with-ssl=/opt/android-openssl --disable-video --disable-ext-sounds --disable-speex-aec --disable-l16-codec --disable-gsm-codec --disable-g722-codec --disable-g7221-codec --disable-speex-codec --disable-sdl --disable-v4l2 --disable-libyuv

