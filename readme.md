## Front end Assessment by Roshini Thangavel
    using Vue JS


### To Run the Project:
    - cd into the frontendassessment folder
    - npm install
    - npm run serve

Both the exercises can be switched between each other using the tabs on the top of the screen

I faced some difficulties in loading the desktop banner, mobile banner and content images using the provided placeholder links. Therefore I added offline images to combat the issue in case that persists. If that problem persist when testing please uncomment the lines in the following file: frontendassessment\src\components\Ex-1.vue , line numbers: 32, 38, 44, 64, 74 and comment out the lines: 31, 37,43, 63, 73.

#### Bonus Exercise:

#### Explain why the result of ('b' + 'a' + + 'a' + 'a').toLowerCase() is banana.

##### Answer:
 'b' + 'a' is a regular concatination which gives you 'ba'
 'ba' + + 'a' has a unary operator '+' which results in NaN (not a number) because it attempts to convert a operand to a number. This is then converted to a string when concatenated which results in baNaN
 Next 'baNaN' + 'a' results in 'baNaNa'a regular concatination
 This string is then converted to lower case using the .toLowerCase() function which results in the result 'banana'.


Thank you for considering my application!

