Step 1:
cd opencv-3.4.1 					#Enter the document opencv-3.4.1
Step 2:
mkdir build output 					#Create the folders build and output
Step 3:
cd build 						#Enter the folder --build
Step 4:
cmake ../ 
-DCMAKE_BUILD_TYPE=RELEASE 
-DCMAKE_INSTALL_PREFIX=../output 			#Use CMake to compile, and the output folder is the output created above.
Step 5:
make -j && make install 				#Use make to compile, remove the -j if it gets stuck.
Step 6：
cmake ../ \
-DOPENCV_FORCE_3RDPARTY_BUILD=ON \
-DBUILD_ZLIB=ON -DWITH_GTK=OFF -DWITH_GTK=OFF \
-DWITH_GTK_2_X=OFF -DWITH_CUDA=OFF -DWITH_IPP=OFF \
-DWITH_OPENCL=OFF -DWITH_OPENCLAMDBLAS=OFF \
-DWITH_QUIRC=OFF -DWITH_OPENCLAMDFFT=OFF \
-DWITH_1394=OFF -DWITH_FFMPEG=OFF -DWITH_WEBP=OFF \
-DWITH_TIFF=OFF -DWITH_OPENEXR=OFF -DWITH_PNG=OFF \
-DWITH_PROTOBUF=OFF -DWITH_GSTREAMER=OFF -DWITH_IMGCODEC_SUNRASTER=OFF \
-DBUILD_SHARED_LIBS=ON -DBUILD_opencv_ts=OFF \
-DBUILD_opencv_shape=OFF -DBUILD_opencv_stitching=OFF \
-DBUILD_opencv_apps=OFF -DBUILD_opencv_calib3d=OFF \
-DBUILD_opencv_dnn=ON -DBUILD_opencv_features2d=OFF \
-DBUILD_opencv_flann=OFF -DBUILD_opencv_highgui=OFF \
-DBUILD_opencv_ml=OFF -DBUILD_opencv_objdetect=OFF \
-DBUILD_opencv_photo=OFF -DBUILD_opencv_video=OFF \
-DBUILD_opencv_videoio=OFF -DBUILD_opencv_videostab=OFF \
-DCMAKE_BUILD_TYPE=RELEASE \
-DCMAKE_INSTALL_PREFIX=../output \
-DCMAKE_CXX_FLAGS="-s -Os" -DCMAKE_C_FLAGS="-s -Os"	#Set the unwanted library to off
Step 7：
make -j && make install 				#Use make to compile again, remove the -j if it gets stuck.


