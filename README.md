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
        
        
  
  <img>https://mail.google.com/mail/u/1/?ui=2&ik=7ec7fd4d14&view=fimg&th=1565f7a63fb1b59f&attid=0.2&disp=inline&realattid=1541910738180767744-local1&safe=1&attbid=ANGjdJ9tn_KdzVbmn7dP0NbaThYgKREI-CeOqx1FjjQ-lqwSvVumoTZjznKB-lvGIfeJhYQDfRnsWcgleUsEuLyDbJbTN5Qw9Yo_BM_bo26ptGuXYSieZScvWLxt4bo&ats=1470481459869&rm=1565f7a63fb1b59f&zw&sz=w1280-h611</img>

