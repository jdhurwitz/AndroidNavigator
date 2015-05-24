# Nav

Navigator code for proximity pass. Allows for easy intent starting and testing of individual code sections.

To use the navigator:
1) Download and unzip.
2) Open android studio and import existing project.
3) Select the Nav project.
4) Go to project structure and hit the "+"
5) Add the project/code you want to test as a library module.
6) Set dependencies in the build.gradle for "app" (the main Nav build.gradle)
7) Figure out all the random Gradle errors you get.
8) Remove the Intent filter for your imported module.
9) Go to the NavigationDrawerFragment and start your activity by using one of the cases (not 0.)
  -0 corresponds to the first thing on the list, n-1 is the last


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
