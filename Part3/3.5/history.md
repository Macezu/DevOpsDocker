**Backend**

_Initial_  
  example-backend   latest       846957e1610c   2 minutes ago    1.01GB  
  56e0ac7fd84e   3 minutes ago   /bin/sh -c go build              146MB  
 
_Improved_  
  example-backend   latest       08dafa9490d1   46 seconds ago   448MB  
  9052f96cc607   16 seconds ago   /bin/sh -c apk add --no-cache build-base  gc…   142MB  

_Final_  
 example-backend   latest       4f227bbb14b6   33 seconds ago   378MB  
 e26303c7e1a2   About a minute ago   /bin/sh -c apk add --no-cache build-base    …   75.7MB 

**Frontend**

_Initial_  
  example-frontend   latest       54f722f6fcd0   9 seconds ago        1.17GB  
  9e99d99b68ba   48 seconds ago       /bin/sh -c npm install && npm install -g ser…   217MB 
  
_Final_
  example-frontend   latest       2ad26bd3ce03   16 seconds ago   315MB  
  741d0ae22f60   About a minute ago   /bin/sh -c npm install && npm install -g ser…   225MB 
