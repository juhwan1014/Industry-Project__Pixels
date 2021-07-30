# pixels Project

## About Project
Please understand that I am not authorized to disclose code details or thumbnail due to the company's request. <br /><br />
This readme focuses on what we have done for the project. <br />

## Function Requirement
### Essential
    * front camera only
    * limit iphone x or higher
### Important
    * limit user storage (up to 500mb per user)
    * compression of images/videos being uploaded to s3
    * changable username
### Nice to have
    * DM
    * private account setting
    * notification

## Priorities List
1. Front Camera only
2. Limit iphone X or higher
3. Limit user storage
4. Compression
5. Setting menu + update profile page
6. Follow
7. Private account setting
8. Likes
9. Camera auto save photo into session roll
10. Auto remove session roll photos after 24 hours if not saved
11. Notifications
12. Captions
13. DM
14. Improve home feed

##### Figma 
- [x] Recreate prototype based on current app
- [x] Add features that are requested 
- [x] Update Figma with changes while the projects are on going

##### Setting up the Local Environment
- [x] Clone the repo and setting up the gitIgnored variables
- [x] Connect to AWS (Cognito, lambda, adding post confirmation, S3)
- [x] Upload backend server in AWS elastic beanstalk (EC2 server)
- [x] Setup the local environment again due to Cognito changes
- [x] Clean up the previous team's codes

##### Bugs
- [x] Enable to display the Camera button
- [x] Enable to click the Header nav button
- [x] Enable to click the buttons on Picture edite screen
- [x] Render the changed username on the Homefeed ---> effected by enabling changing username
- [x] Prevent to render the default avatar image before the custom profile image is rendered

##### Enhancements
- [x] Change names on Camera roll screen dropdwon menu
- [x] Delete loading bar all over the app
- [x] Change bottom navbar colors
- [x] Relocate username on the top of the displayname
- [x] Roll back; Top: display name
- [x] Cancel auto Uppercase in input fields; changing username and link
- [x] Adjust Styling on Search screen; align avatar/image
- [ ] Enable to render users simultaneously when user type on search field
- [x] Styling the default avatar & user profile image + align them nicely on the entire app

##### Re-create Cognito - remove attributes from cognito & Enable to change the username
- [x] Recreate Cognito for removing the display name attribute
- [x] Modify Lambda function to be able to change username
- [x] Update the backend server
- [x] Change Register function based on changable username attribute
- [x] Change SignIn function based on changable username attribute
- [x] Move the changing username input field from edit profile screen to the setting on profile screen

##### Register page 
- [x] Remove "display name" field

##### profile screen - #5 Setting menu + update profile page
- [x]  Add default avartar image 
- [x]  Add gear icon on the top right corner
- [x]  Add drop down menu on the gear icon
- [x]  Logout function
- [x]  Username should located on the Header
- [x]  Replace useraname to displayname on the header ---> effected by enabling changing username
- [x]  Render the default user profile avatar on the Home feed
- [x]  Add UI basic counts of Post

###### profile screen - setting screens 
- [x] Add UI on the Setting screen
- [x] Add Terms and conditions in text(not PDF) on Terms and conditions screen
- [x] Add sending Email functions on Support screen

###### profile screen -> Edit profile screen 
- [x] Bring the user Profile image
- [x] Add function for choose photo from camera roll
- [x] Render the default avatar
- [ ] Add function for turning on the front camera
- [x] Enable Change username

##### Camera screen in Swift - #1, Editing profile Photo 
- [x] Eject expo
- [x] Render the app in Xcode
- [x] Making the bridge point where connects to the swift custom component with simple button
- [x] Test it out it go through in ReactNative
- [x] implement UIImagePicker as camera
- [x] Disable flipping camera button
- [ ] save image from camera into ReactNative code

##### Camera screen in ReactNative - #1, #4 , Editing profile photo
- [x] Change the camera from expo-imagePicker to Basic camera in React-native
- [x] Enable the front camera only by removing the camera switch buttons
- [x] Enable to take photo
- [x] Enable to take video
- [x] Remove the bottom tab navigation on the camera screen
- [x] Enable flash
- [x] Take Photo Continuously 
- [x] Video max length 30 seconds
- [ ] Open camera automatically when user enter the camera

##### Edit Photo Screen
- [x] Delete rotate icon & function
- [x] Add function & icon for reverting to original photo
- [x] Adjust the constras range (0.7-1.4)
- [ ] Adjust the crop area

##### Follow - #6
- [x] Edit MongoDB data table
- [x] Create UI for Followers / Following
- [x] Create function that storing the user info - Following / Follower
- [x] Display list of followers / following when Clicked
- [ ] Clicking on user in list brings to user's page

##### Limit user storage
- [x] Read the jepg/mov file size
- [x] Calculate total size of images/videos that user uploaded to s3
- [ ] Block the uploading when no space left
- [ ] Render with "%" that indicates how much space user used

##### Compression
- [x] Video file size cannot be exceed 3mb
- [ ] Image file size cannot be exceed 200kb
