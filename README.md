![promo](https://github.com/Ecko95/QuickSnap/blob/master/app/src/main/promo.png)

# Welcome To QuickSnap

## Snap, Edit, Share

QuickSnap is a photo editor that allows you to capture and share your best moments with friends and family.

It enables users to view their phone's multimedia content in a simple gallery style app. When taking pictures within the app, users are given a wide selection of filters to chose from.

### Welcome to the QuickSnap wiki!

###### Login and Access
To access QuickSnap, user's must sign in to our email list in order to access its contents, this is to protect our application and    monitor our test results.

### Design architecture
###### CursorLoader:
Enables asyncTask background loading protocols for a seamless and effective image/video gallery loading.

###### MediaStore:
Lorem

###### Custom Adapters:
Lorem
 
## Views

* Recycler Viewer
* Image Views
* Buttons 
* Image Views
* 

### Disclaimer!!
QuickSnap is currently in its alpha stage are some bugs are still present and some features have not yet be implemented.


# Documentation

# Contributors
![contributors](https://github.com/Ecko95/ecko95.github.io/blob/master/img/contributors.PNG)

# Commits
![commits](https://github.com/Ecko95/ecko95.github.io/blob/master/img/commits.PNG)

# Code Frecuency
![code_frecuency](https://github.com/Ecko95/ecko95.github.io/blob/master/img/code_frecuency.PNG)

# Punch Card
![code_frecuency](https://github.com/Ecko95/ecko95.github.io/blob/master/img/punch_card.PNG)

# Network
![code_frecuency](https://github.com/Ecko95/ecko95.github.io/blob/master/img/network.PNG)


```markdown
# Firebase Connectivity Code

## initialise database Auth
  firebaseAuth = FirebaseAuth.getInstance();

  if(firebaseAuth.getCurrentUser() != null){
      //start user profile activity
      startActivity(new Intent(this, UserProfileActivity.class));
      //close current activity
      finish();
  }
  
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

```
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
    testCompile 'junit:junit:4.12'

```
**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)


For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/Ecko95/ecko95.github.io/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
