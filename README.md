# pimagizer
Change easily the size to your images

>$ sudo python setup.py install

>$ pimagizer

Note: In some systems, like ArchLinux and similars, it is necessary run the installer with python2, because the program is written in Python2. You should run:
$ sudo python2 setup.py install

After run this, you also will be able to load it from apps menu
Note you may need python libraries such PIL (known as "python-imaging") and GTK+3 python bindings.
You also should be able to run this program with nautilus -> Open with...

##Creating a RPM Package with distutils

Just run the following command:
python setup.py bdist_rpm --group="Productivity/Graphics/Convertors" --packager="YOUR NAME <email@wherever.com>" --requires="pygobject3,python-imaging"

##Creating a DEB package through bzr builddeb

python setup.py sdist
cp dist/pimagizer-0.3.9b.tar.gz ../pimagizer_0.3.9b.orig.tar.gz

*NEW* Better use tools/builddeb.sh =>It almost work without bugs

##Creating a .tar.xz package to use it with pacman (Arch-based distributions)

Just go to tools/ and run makepkg -c (Note: -c flag will clean unused directories).
Then run "sudo pacman -U --force pimagizer-0.4.2-2-any.pkg.tar.xz" Note: The force 
  flag is only needed if older options are already installed: it will overwrite existing files.