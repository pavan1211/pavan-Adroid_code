# pavan-Adroid_code

//Activity_main.xml:

        <Linearlayout 
 	android:layout-width="match_parent"
 	android:layout-width="match_parent"
 	android:Orientation="vertical"
 	android:padding="10dp">

	<TextView
 	android:text="Text"
 	android:layout-width="wrap-content"
 	android:layout-heigth="wrap-content"/>

	<EditText
 	android:id="@+id/inputText"
 	android:hint="Enter a text Here ..."
 	android:gravity="top"
 	android:layout-width="match_parent"
 	android:layout-height="match_content"/>

	<Button
	 android:id="@+id/Button"
 	android:text="save"
 	android:layout-width="match_parent"
 	android:layout-height="match_content"/>

	</Linearlayout>








//Second_Activity.xml:

	<Linearlayout
	 android:layout-width="match_parent"
	 android:layout-height="match_parent"/>
	
	<Textview
	 android:text="We are entering first time in app"
	 android:layout-width="match_parent"
	 android:layout-height="wrap_content	"/>

	</Linearlayout>








//SecondActivity.java:

	package packagename
	import ...
	public class SecondActivity Extends AppcompatActivity
	{
	  @override
	   protected void onCreate(Bundle savedInstanceState)
	   {
 	        super.onCreate(savedInstanceState);
		setContentview(R.Layout.secondActivity);
           }
	 }









//MainActivity.java

   	package package
   	import..
   	public class mainActivity extends AppcompatActivity
   	{
  	    EditText mInput;
  	    Button mSaveButton;
  	    String mText;	
     
         @override
   	protected void onCreate(Bundle savedInstanceState)
        {
  	        super.onCreate(SavedInstancestate);
  	        setContentView(R.layout.mainActivity);

  	         mInput=FindviewByid(R.id.inputText);
  	         msaveButton=Findviewbyid(R.id.button);

           	sharedpreference pref=getshoredpreference(name:"pref",mode_private);

  	         String Firststart=pref.getString(s:"FirstTime",s1:"")
  	
   	if(Firststart.equals("yes"))
 	 {
 	      Intent intent=new Intent(mainActivity.this, secondActivity.class);
 	      startActivity(intent); 
    	}
	else
	 {
	    	mSaveButton.setOnClickListener(new view.onClickListener()
	         {
	           @override
	           public void onClick(view v)
	             {
	              mText = mInput,getText().toString().trime();
	             }
	         });
	    sharedPreferences.editor editor = pref.edit();
	    editor.putString(s:"FirstTime", s1:"yes");
	    editor.apply();
        
	 }
	 
      }
      
    }


