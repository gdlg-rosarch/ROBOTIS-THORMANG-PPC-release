# Script generated with Bloom
pkgdesc="ROS - The thormang3_walking_demo package This package describes how to use thormang3_walking_module."
url='http://wiki.ros.org/thormang3_walking_demo'

pkgname='ros-kinetic-thormang3-walking-demo'
pkgver='0.2.0_1'
pkgrel=1
arch=('any')
license=('Apache 2.0'
)

makedepends=('ros-kinetic-catkin'
'ros-kinetic-robotis-controller-msgs'
'ros-kinetic-roscpp'
'ros-kinetic-roslib'
'ros-kinetic-std-msgs'
'ros-kinetic-thormang3-walking-module-msgs'
'yaml-cpp'
)

depends=('ros-kinetic-robotis-controller-msgs'
'ros-kinetic-roscpp'
'ros-kinetic-roslib'
'ros-kinetic-std-msgs'
'ros-kinetic-thormang3-walking-module-msgs'
'yaml-cpp'
)

conflicts=()
replaces=()

_dir=thormang3_walking_demo
source=()
md5sums=()

prepare() {
    cp -R $startdir/thormang3_walking_demo $srcdir/thormang3_walking_demo
}

build() {
  # Use ROS environment variables
  source /usr/share/ros-build-tools/clear-ros-env.sh
  [ -f /opt/ros/kinetic/setup.bash ] && source /opt/ros/kinetic/setup.bash

  # Create build directory
  [ -d ${srcdir}/build ] || mkdir ${srcdir}/build
  cd ${srcdir}/build

  # Fix Python2/Python3 conflicts
  /usr/share/ros-build-tools/fix-python-scripts.sh -v 2 ${srcdir}/${_dir}

  # Build project
  cmake ${srcdir}/${_dir} \
        -DCMAKE_BUILD_TYPE=Release \
        -DCATKIN_BUILD_BINARY_PACKAGE=ON \
        -DCMAKE_INSTALL_PREFIX=/opt/ros/kinetic \
        -DPYTHON_EXECUTABLE=/usr/bin/python2 \
        -DPYTHON_INCLUDE_DIR=/usr/include/python2.7 \
        -DPYTHON_LIBRARY=/usr/lib/libpython2.7.so \
        -DPYTHON_BASENAME=-python2.7 \
        -DSETUPTOOLS_DEB_LAYOUT=OFF
  make
}

package() {
  cd "${srcdir}/build"
  make DESTDIR="${pkgdir}/" install
}

