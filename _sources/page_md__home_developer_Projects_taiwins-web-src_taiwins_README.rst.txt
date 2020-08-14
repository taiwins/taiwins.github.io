.. index:: pair: page; Taiwins, a morden wayland window manager
.. _doxid-d1/d72/md__home_developer__projects_taiwins-web-src_taiwins__r_e_a_d_m_e:

Taiwins, a morden wayland window manager
========================================

Taiwins is a wayland window manager, supports both tiling and floating layout. It is designed to be mordern and modular. It is extensible through lua script and it has built-in **shell** and **widgets** implementation through `nuklear GUI <https://github.com/vurtun/nuklear>`__. It also supports popular tiling window manager features like gapping.

Taiwins is usable but currently under heavy developement. You can refer to `progress <docs/progress.org>`__ for current progress.



.. _doxid-d1/d72/md__home_developer__projects_taiwins-web-src_taiwins__r_e_a_d_m_e_1autotoc_md56:

How to build
~~~~~~~~~~~~

you will need following dependencies

* Pixman

* libweston(if you have an nvidia graphics card you may need weston-eglstream)

* xkbcommon

* libinput

* wayland

* wayland protocols

* cairo

* lua

* librsvg

* opengl>=3.3

* vulkan

* cmake

* pam

* fontconfig

* freetype2

* xcursor-themes(required for whiteglass cursor)





.. _doxid-d1/d72/md__home_developer__projects_taiwins-web-src_taiwins__r_e_a_d_m_e_1autotoc_md57:

build steps:
~~~~~~~~~~~~

with source code, you can easily compile and try out:

.. code-block:: none

	git clone https://github.com/taiwins/taiwins taiwins && cd taiwins
	git submodule init
	git submodule update
	mkdir build && cd build
	cmake ..
	make -j8

For those who use Archlinux, there is an `aur <https://aur.archlinux.org/packages/taiwins-git>`__ package you can simply install.





.. _doxid-d1/d72/md__home_developer__projects_taiwins-web-src_taiwins__r_e_a_d_m_e_1autotoc_md58:

How to run
~~~~~~~~~~

Here is currently how I run the compositor, lua configuration is supported(in progress), see the `sample config <docs/config.lua>`__ for example

.. code-block:: none

	cd build
	./bin/taiwins ./bin/taiwins-shell ./bin/taiwins-console

Or if you install systemwisely, you can simply use

.. code-block:: none

	taiwins taiwins-shell taiwins-console



.. _doxid-d1/d72/md__home_developer__projects_taiwins-web-src_taiwins__r_e_a_d_m_e_1autotoc_md59:

key-bindings
------------

Though it is configurable, by default available bindings are

* ``F12`` : quit taiwins

* ``Ctrl+LEFT/RIGHT`` switch to previous/next workspace

* ``Alt+Super+b`` switch to last workspace

* ``Alt+LEFT`` resize window to the left (only in tiling mode)

* ``Alt+RIGHT`` resize window to the right (only in tiling mode)

* ``Super+Space`` toggle vertical/horizental layout (only in tiling mode)

* ``Alt+Shift+Space`` toggle window floating/tiling

* ``Alt+Shift+j`` cycle through applications

* ``Super+v`` creating vertical sub-layout (only in tiling mode)

* ``Super+h`` creating horizontal sub-layout (only in tiling mode)

* ``Super+m`` merge current application to parent layout

* ``Super+p`` calling **shell-console** to launch application





.. _doxid-d1/d72/md__home_developer__projects_taiwins-web-src_taiwins__r_e_a_d_m_e_1autotoc_md60:

Documentation
-------------

Currently documentation is generated through doxygen. SET ``BUILD_DOC=ON`` option with cmake to enable building documentation.





.. _doxid-d1/d72/md__home_developer__projects_taiwins-web-src_taiwins__r_e_a_d_m_e_1autotoc_md61:

Screenshots
-----------

* widget example
  
  .. image:: ../../imgs/with-nuklear.png

* opening application in floating mode
  
  .. image:: ../../imgs/use-emacs.png

* opening application in tiling mode
  
  .. image:: ../../imgs/resizing.png

