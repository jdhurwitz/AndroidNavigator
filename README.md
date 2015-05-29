# Nav

Navigator framework code for proximity pass. Allows for easy intent starting and testing of individual code sections. Integrated file explorer allowing for file selection. Ability to return full file path. 

<b>Current Rev Notes</b>
<br>
-Default activity not specified for startup. 
<br>
-File explorer does not store file path of last selected variable yet
<br>
-File explorer returns to the home menu after selection (as expected)
<br>

<b>Design Hierarchy Notes</b>
<br>
-Default activity startup will be list of nearby android devices on wifi direct. (Rob)
<br>
-Once devices have been paired onSuccess, start file explorer activity
<br>
-Browse file system and select file. Once item has been selected, start Nate's code.
<br>


<b>To use the navigator: </b>
<br>
1) Download and unzip.
<br>
2) Open android studio and import existing project.
<br>
3) Select the Nav project.
<br>
4) Go to project structure and hit the "+".
<br>
5) Add the project/code you want to test as a library module.
<br>
6) Set dependencies in the build.gradle for "app" (the main Nav build.gradle)
<br>
7) Figure out all the random Gradle errors you get.
<br>
8) Remove the Intent filter for your imported module.
<br>
9) Go to the NavigationDrawerFragment and start your activity by using one of the cases (not 0.)
<br>
  -0 corresponds to the first thing on the list, n-1 is the last
  <br>


    /*
    Determine which activity to start based on selected item.
     */
    private void selectItem(int position) {
        Intent selectedIntent = null;
        switch(position){
            case 0:
                break;
            case 1:
            {
                selectedIntent = new Intent(this.getActivity(), FileChooser.class);
                startActivity(selectedIntent);
                break;
            }
            case 2:
            {
                //start an activity here
                break;
            }
            case 3:
            {
                //start an activity here
                break;
            }
            default:
                break;

        }
    }
