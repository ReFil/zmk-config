# zmk-config
This is the ZMK-Config repo for the Polarity works BT60 keyboard, with this you can customise your layout and keymap to suit your exact needs.
We have provided base keymaps for the following layouts: ANSI, ISO, Split backspace and right shift, Tsangan and all 1u bottom rows. These can be acessed  by choosing the appropriate branch. 

# Customisation
In order to change the keymap to meet your needs you will need a github account. Click the "fork" button in the top right to create your own version of the repo, then use teh drop down menu to select the branch with your layout.
The keymap information is contained entirely within the file bt60.keymap. Download this file to your computer and open it in a text editor such as Atom or notepad++ then you can open and edit it. The full list of ZMK keycodes can be found [here](https://zmkfirmware.dev/docs/codes/keyboard-keypad/). 
After editing the keymap file upload it to the original folder using the "Add file" dialog in github, then click on "Actions" and wait for the build process to complete (The orange dot will go to either a red X or green tick).

# Compilation and downloading
 If you have made any errors in the keymap the compilation will fail and there will be a red X in the actions dialog. Click on it and it will tell you where the problem is. 
 If the build completes with no errors you will be able to find the firmware in the "Arifacts" section of the last action. 
 Put the keyboard into bootloader (Either double tap the hardware reset button or use the behaviour, typically fn + enter) and drag and drop the .uf2 file onto the usb drive that shows up
 
 # More advanced
 If you want to exercise greater control over your BT60 and have a unique layout implemented you will need to change the matrix trandform. The following diagram displays which keys connect to which row and column pins. Note that everything is zero indexed in the matrix transform
 	![alt text](rowcolmap.png)
  The matrix transform can be found in bt60.dts, more information on how to do the matrix transforms can be found in the official ZMK documentation [here](https://zmkfirmware.dev/docs/development/new-shield#optional-matrix-transform)
  We're always willing to accept pull requests if you've developed your own layouts :)
