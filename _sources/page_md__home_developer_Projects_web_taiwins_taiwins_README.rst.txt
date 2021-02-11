.. index:: pair: page; Taiwins, a modern wayland window manager
.. _doxid-d6/d56/md__home_developer__projects_web_taiwins_taiwins__r_e_a_d_m_e:

Taiwins, a modern wayland window manager
========================================

Taiwins is a dynamic wayland window manager, supports both tiling and floating layout. It is designed to be modern and modular. It is extensible through lua script and it has built-in **shell** and **widgets** implementation through `nuklear GUI <https://github.com/Immediate-Mode-UI/Nuklear>`__. It also supports popular tiling window manager features like gapping.

The name of the project pronounces as ['taiwinz], it is inspired by the philosophy of Taichi as I hope it would be dynamic and balanced.

Taiwins is usable now with potential bugs and some missing features. Continues developement in progress and helps are wanted. If you like to join, I drafted some pages of ``notes`` to guide you through the starting steps. You can also join the chat on `Gitter <https://gitter.im/taiwins>`__ for any questions and disscussions. There is a :ref:`feature list <doxid-d6/d3c/md__home_developer__projects_web_taiwins_taiwins_docs_progress>` available if you want to know more about what taiwins can do.



.. _doxid-d6/d56/md__home_developer__projects_web_taiwins_taiwins__r_e_a_d_m_e_1autotoc_md87:

Dependencies
~~~~~~~~~~~~

you will need following dependencies

* Pixman

* xkbcommon

* xwayland

* libx11, libxcb (if you want X11 backen support)

* libinput

* wayland

* wayland protocols

* cairo

* lua

* librsvg

* opengl or opengles

* meson

* ninja

* pam

* fontconfig

* freetype2





.. _doxid-d6/d56/md__home_developer__projects_web_taiwins_taiwins__r_e_a_d_m_e_1autotoc_md88:

Build steps:
~~~~~~~~~~~~

with source code, you can easily compile and try out:

.. code-block:: none

	git clone https://github.com/taiwins/taiwins --recursive taiwins && cd taiwins
	
	meson build && ninja -C build

For those who use Archlinux, there is an `aur <https://aur.archlinux.org/packages/taiwins-git>`__ package you can simply install(Outdated).





.. _doxid-d6/d56/md__home_developer__projects_web_taiwins_taiwins__r_e_a_d_m_e_1autotoc_md89:

How to run
~~~~~~~~~~

Taiwins starts with default shell and default console they are found. You can also specifiy the shell application and console application through command line options.

.. code-block:: none

	cd build
	./bin/taiwins -s ./bin/taiwins-shell -c ./bin/taiwins-console

Or if you install systemwisely, you can simply use

.. code-block:: none

	taiwins -s taiwins-shell -c taiwins-console

If you prefer not to have the shell, try ``taiwins -n`` which will make taiwins run without shell, user can start a shell later.

The default configuration is ``$XDG_CONFIG_PATH/taiwins/config.lua``, see the `sample config <docs/config.lua>`__ for an example.



.. _doxid-d6/d56/md__home_developer__projects_web_taiwins_taiwins__r_e_a_d_m_e_1autotoc_md90:

Key-bindings
------------

Taiwins has a versatile binding system, you can chain key-presses like in Emacs(up to 5) and add custom bindings through lua functions. The bindings is configurable, by default available bindings are

* ``F12`` : quit taiwins

* ``Super+Shift+c`` close current application

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





.. _doxid-d6/d56/md__home_developer__projects_web_taiwins_taiwins__r_e_a_d_m_e_1autotoc_md91:

Documentation
-------------

Currently documentation is generated through doxygen. enable ``build_doc`` option to enable building documentation. We also host a online themed `documentation <https://taiwins.org/page_doc.html>`__ which you can access.





.. _doxid-d6/d56/md__home_developer__projects_web_taiwins_taiwins__r_e_a_d_m_e_1autotoc_md92:

Screenshots
-----------

There are some example screen shots of taiwins, check out the :ref:`screenshot <doxid-dd/d4a/md__home_developer__projects_web_taiwins_taiwins_docs_screenshots>` page" for more details.

