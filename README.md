# FaceCropLib

I had a requirement where I needed to crop the image on face.
Android's Centre crop was not working when the face was at the top or bottom so I made this library which uses google vision to detect face and square crop it
accordingly.

In your project gradle put

   maven { url "https://jitpack.io" }

In your app gradle put

compile 'com.github.nitin-jaiman:facecroplib:1.0'

How to use library

        // to load photos async from url or local uri
        FaceCrop faceCrop=new FaceCrop(this);
        faceCrop.setFaceCropAsync(imageView, Uri.parse("some photo link ")));
        
        or 
        
          // to load photos async from bitmap
        FaceCrop faceCrop=new FaceCrop(this);
        faceCrop.setFaceCropAsync(imageView, bitmap);
        
        or 
          // If you want to load on main thread
        FaceCrop faceCrop=new FaceCrop(this);
        faceCrop.setFaceCrop(imageView, Uri.parse("some photo link ")));
        
        

![screenshot_20160806-161858 2](https://cloud.githubusercontent.com/assets/8062921/17456490/c3091db8-5bf6-11e6-9083-209d6a0637dd.png)
![screenshot_20160806-161905 2](https://cloud.githubusercontent.com/assets/8062921/17456489/c3088402-5bf6-11e6-88b4-38f3b341a2f6.png)
