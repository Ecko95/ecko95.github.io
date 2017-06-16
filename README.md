# Welcome To QuickSnap

![promo](https://github.com/Ecko95/QuickSnap/blob/master/app/src/main/promo.png)

## Snap, Edit, Share

QuickSnap is a photo editor that allows you to capture and share your best moments with friends and family.

It enables users to view their phone's multimedia content in a simple gallery style app. When taking pictures within the app, users are given a wide selection of filters to chose from.

### Welcome to the QuickSnap wiki!

#### Click here to download the lastest project: [Link](https://github.com/Ecko95/QuickSnap/archive/master.zip)


###### Login and Access
To access QuickSnap, user's must sign in to our email list in order to access its content. This is to protect our application and    monitor our test results.

### Design architecture
###### CursorLoader:
A loader that queries the ContentResolver and returns a Cursor. This class implements the Loader protocol in a standard way for querying cursors, building on AsyncTaskLoader to perform the cursor query on a background thread so that it does not block the application's UI.

###### MediaStore:
The Media provider contains meta data for all available media on both internal and external storage devices.

###### Adapters:
An Adapter object acts as a bridge between an AdapterView and the underlying data for that view. The Adapter provides access to the data items. The Adapter is also responsible for making a View for each item in the data set.
 
## Views

* Horizontal Scroll Views
* Progress Bars
* Recycler Viewers
* Image Buttons
* Buttons 
* Text Views
* Edit Texts
* Image Views
* Web View
* Surface View

## Disclaimer!! 
_QuickSnap is currently in its alpha stage are some bugs are still present and some features have not yet be implemented._




# Documentation

## Contributors
![contributors](https://github.com/Ecko95/ecko95.github.io/blob/master/img/contributors.PNG)

## Commits
![commits](https://github.com/Ecko95/ecko95.github.io/blob/master/img/commits.PNG)

## Code Frecuency
![code_frecuency](https://github.com/Ecko95/ecko95.github.io/blob/master/img/code_frecuency.PNG)

## Punch Card
![punch_card](https://github.com/Ecko95/ecko95.github.io/blob/master/img/punch_card.PNG)

## Network
![network](https://github.com/Ecko95/ecko95.github.io/blob/master/img/network.PNG)

## Firebase Connectivity Code
```markdown

## initialise database Auth
  firebaseAuth = FirebaseAuth.getInstance();

  if(firebaseAuth.getCurrentUser() != null){
      //start user profile activity
      startActivity(new Intent(this, UserProfileActivity.class));
      //close current activity
      finish();
  }

```

```markdown
## veryfies email and password are correct        
  firebaseAuth.signInWithEmailAndPassword(email,password)
                  .addOnCompleteListener(this, new OnCompleteListener<AuthResult>() {
                      @Override
                      public void onComplete(@NonNull Task<AuthResult> task) {

                          if(task.isSuccessful()){
                              //close current activity;
                              finish();
                              //start user profile activity
                              startActivity(new Intent(getApplicationContext(), UserProfileActivity.class));

                          }
                          else {
                              Toast.makeText(MainActivity.this, "Failed to log in", Toast.LENGTH_SHORT).show();
                          }
                          progressDialog.dismiss();
                      }
                  });

``` 
```markdown            
## creates a new User inside FireBase Database
  firebaseAuth.createUserWithEmailAndPassword(email, password)
          .addOnCompleteListener(this, new OnCompleteListener<AuthResult>() {
              @Override
              public void onComplete(@NonNull Task<AuthResult> task) {
                  if (task.isSuccessful()) {

                      //start user profile activity
                      startActivity(new Intent(getApplicationContext(), UserProfileActivity.class));
                      //close current activity
                      finish();

                      /*
                      User is registered and logged in successfully
                      Start profile activity
                      For now we only are displaying a message
                       */

                      Toast.makeText(MainActivity.this, "You have Registered Successfully", Toast.LENGTH_SHORT).show();

                  } else {
                      Toast.makeText(MainActivity.this, "Failed to register, Please try again", Toast.LENGTH_SHORT).show();
                  }
                  progressDialog.dismiss();

              }
          });
    }
```
# Repositories

```markdown
    compile 'com.android.support:appcompat-v7:25.3.1'
    compile 'com.google.firebase:firebase-auth:10.2.1'
    compile 'com.android.support:design:25.3.1'
    compile 'com.android.support:recyclerview-v7:25.3.1'
    compile 'com.github.bumptech.glide:glide:3.7.0'
    compile 'com.android.support:support-v4:25.3.1'
    compile 'com.android.support.constraint:constraint-layout:1.0.2'
    compile 'com.github.paolorotolo:appintro:4.1.0'
    compile 'com.github.mukeshsolanki:photofilter:1.0.2'
    compile 'io.github.kobakei:ratethisapp:1.2.0'

```

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
