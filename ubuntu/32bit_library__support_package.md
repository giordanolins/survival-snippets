##32-bit library support package

    sudo apt-get install ia32-libs
	
	
The ia32-libs package was a hack to get 32-bit packages installed on a 64-bit installation. Since Ubuntu version 11.10 (Oneiric), Multi Arch has been added. One of the objectives for it is removing the ia32-libs package. Instead, you have to install the 32-bit libraries of a package with:

    sudo apt-get install package-name:i386

You don't have to worry about this for packages in the standard repositories (e.g. the wine package). For external software, it's a bit more difficult because you have to find the dependencies manually. In that case, use your favorite search engine to find which libraries you need.
It seems that ia32-libs still exist, but merely as a convenience package to include common 32-bit libraries. This package now uses Multi Arch to install the 32-bit packages correctly.