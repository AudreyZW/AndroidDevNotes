#### getActionBar v.s. getSupportActionBar

If you are using AppCompat you always have to call `getSupportActionBar()` no matter which Android Version your App is running.



### Start another activity

navigation menu --> note main

**use intent**

An `Intent` is an object that provides runtime binding between separate components, such as two activities. The`Intent` represents an app’s "intent to do something."

```java
Intent intent = new Intent(this, anotherActivity.class);
startActivity(intent);

//// in new activity
Intent intent  = getIntent();
```



###Use Fragment for Share Element Transitions





###Fragments in Activity

####Static -> xml

1. Create another layout xml file for fragment
2. Create fragment by extending class of fragment
3. Set the layout xml to fragment
4. Use fragment tag to include fragment in xml layout

#### Dynamic -> Activity

1. Create another layout xml file for fragment

2. Create fragment by extending class of fragment

3. Set the layout xml to fragment

4. Add a layout that will host a Fragement (Need a placeholder where fragment will be added programmatically. e.g. a framelayout)

5. Write code to add fragment to activity in activity

   - Making a Fragment transaction

     - add
     - remove
     - replace

     1. use method from activity to get FragmentManager
     2. use beginTranssaction() and add/remove/replace

```java
private void addFragment(){
    FragmentManager fragmentManager = getSupportFragmentManager();
    FragmentTrasaction fragmentTrasavtion = fragmentManager.beginTransaction();
    SampleFragment sampleFragment = new SampleFragment();
    fragmentTransaction.add(R.id.fragmentContainer, sampleFragment); //the container is where we want to put the fragment in
    fragmentTransaction.commit();
}
```





## Activity LifeCycle

- onCreate
- onStart
- onResume
- onPause
- onStop
- onDestroy



## Fragment LifeCycle

- onAttach
- onCreate
- onCreateView
- onActivityCreated
- onResume
- onStart
- onPause
- onStop
- onDestroyView
- onDestroy
- onDetach