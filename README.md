# cffi-travis-wheel

This repository is a tool for cffi wheel deployment on pypi. It uses multibuild to build the wheels and twine to upload the wheel on pypi.  

# Environment setup  
To upload the wheel on pypi, your pypi credential must be configured in travis or else it can be provided with twine command in travis file as well. Please have a look at below-  

1) Setting pypi credential as travis environment variable  
  i)	Select your package on travis.  
  ii)	Go to *`settings`* page.  
  iii)	Set environment variable *`TWINE_USERNAME`* and *`WINE_PASSWORD`* with your pypi *`username`* and *`password`*.  
  iv)	Trigger the build.  
  
2) Feeding pypi credential to twine command  
  i)	Open *`.travis.yml`* file  
  ii)	Modify twine upload command as *"twine upload `-u <pypi username> -p <pypi password>` ${TRAVIS_BUILD_DIR}/wheelhouse/*"*  
  iii) Trigger the build if required.

