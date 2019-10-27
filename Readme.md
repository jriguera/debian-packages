# Debian packages

* `python2python3`: Simple package to provide python2 wrapper with python3
  This package allows installing packages depending on 'python'
  By default python is a transitional package pointing to Python2.
  This package provides 'pip' and 'python'.


# Development

* https://blog.packagecloud.io/eng/2016/12/15/howto-build-debian-package-containing-simple-shell-scripts/

Install dependencies:
```
sudo apt-get install dh-make devscripts
```

Create the package 
```
cd <package>-<version>
sudo dpkg-buildpackage -us -uc --build=all
# or sudo debuild -us -uc
```

## Easy alternavite "binary" packaging

* https://www.leaseweb.com/labs/2013/06/creating-custom-debian-packages/
* http://www.sj-vs.net/creating-a-simple-debian-deb-package-based-on-a-directory-structure/
* http://www.hackgnar.com/2016/01/simple-deb-package-creation.html

No dependecies needed, `dpkg-deb` comes with `dpkg`, create the package 

```
dpkg-deb --build <package>-1/
```

### Extra docs

https://vincent.bernat.ch/en/blog/2016-pragmatic-debian-packaging

