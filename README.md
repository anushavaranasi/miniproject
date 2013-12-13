miniproject
===========

code
Xml Code:
  <RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity" 
    android:background="@drawable/images1">
<TextView
        android:id="@+id/textView1"
        android:layout_width="150dp"
        android:layout_height="80dp"
        android:layout_alignParentLeft="true"
        android:layout_alignParentTop="true"
        android:layout_marginLeft="78dp"
        android:layout_marginTop="79dp"
        android:text="Optimised Railway route"
        android:textAppearance="?android:attr/textAppearanceLarge" />

    <Button
        android:id="@+id/button1"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_alignLeft="@+id/textView1"
        android:layout_alignParentBottom="true"
        android:layout_marginBottom="38dp"
        android:layout_marginLeft="22dp"
        android:text="next" />

</RelativeLayout 
Java Code: 
package com.example.project1;
import android.os.Bundle;
import android.app.Activity;
import android.content.Intent;
import android.database.sqlite.SQLiteDatabase;
import android.view.Menu;
import android.view.View;
import android.view.View.OnClickListener;
import android.widget.Button;

public class MainActivity extends Activity {
@Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        Button bt=(Button)findViewById(R.id.button1);
       bt.setOnClickListener(new OnClickListener() {
       @Override
	public void onClick(View v) {
           // TODO Auto-generated method stub
	Intent it=new Intent(MainActivity .this,Sec.class);

startActivity(it);
	}
	package com.example.project1;

import android.app.Activity;
import android.content.Intent;
import android.os.Bundle;
import android.view.TextureView;
import android.view.View;
import android.view.View.OnClickListener;
import android.widget.Button;
import android.widget.TextView;

public class Agra extends Activity {

	@Override
	protected void onCreate(Bundle savedInstanceState) {
		// TODO Auto-generated method stub
		super.onCreate(savedInstanceState);
		setContentView(R.layout.agra);

		TextView tv1=(TextView)findViewById(R.id.textView1);
		TextView tv2=(TextView)findViewById(R.id.textView2);
		TextView tv3=(TextView)findViewById(R.id.textView3);
		TextView tv4=(TextView)findViewById(R.id.textView4);
		TextView tv5=(TextView)findViewById(R.id.textView5);
		TextView tv6=(TextView)findViewById(R.id.textView6);
		TextView tv7=(TextView)findViewById(R.id.textView7);
		TextView tv8=(TextView)findViewById(R.id.textView8);
		Button bt=(Button)findViewById(R.id.button1);

		 bt.setOnClickListener(new OnClickListener() {
			
			@Override
			public void onClick(View v) {
				// TODO Auto-generated method stub
				Intent it=new Intent(Agra.this,Agra1.class);
				startActivity(it);
				
			}
		});
   }
package com.example.project1;

import android.app.Activity;
import android.os.Bundle;

public class Agra1 extends Activity{
	@Override
	protected void onCreate(Bundle savedInstanceState) {
		// TODO Auto-generated method stub
		super.onCreate(savedInstanceState);
		setContentView(R.layout.agra1);
	}



}<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent" >

    <TextView
        android:id="@+id/textView1"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_alignParentLeft="true"
        android:layout_alignParentTop="true"
        android:text="Train no :"
        android:textAppearance="?android:attr/textAppearanceLarge" />

    <TextView
        android:id="@+id/textView2"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_alignParentLeft="true"
        android:layout_below="@+id/textView1"
        android:layout_marginTop="33dp"
        android:text="Distance :"
        android:textAppearance="?android:attr/textAppearanceLarge" />

    <TextView
        android:id="@+id/textView3"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_alignParentLeft="true"
        android:layout_below="@+id/textView2"
        android:layout_marginTop="75dp"
        android:text="Place :"
        android:textAppearance="?android:attr/textAppearanceMedium" />

    <TextView
        android:id="@+id/textView4"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_alignParentRight="true"
        android:layout_alignParentTop="true"
        android:layout_marginRight="42dp"
        android:text="Large Text"
        android:textAppearance="?android:attr/textAppearanceLarge" />

    <TextView
        android:id="@+id/textView5"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_alignBottom="@+id/textView2"
        android:layout_alignLeft="@+id/textView4"
        android:text="Large Text"
        android:textAppearance="?android:attr/textAppearanceLarge" />

    <TextView
        android:id="@+id/textView6"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_alignLeft="@+id/textView5"
        android:layout_alignTop="@+id/textView3"
        android:text="Large Text"
        android:textAppearance="?android:attr/textAppearanceLarge" />

mport java.util.ArrayList;


import android.app.Activity;
import android.content.Intent;
import android.database.Cursor;
import android.database.sqlite.SQLiteDatabase;
import android.os.Bundle;
import android.view.View;
import android.widget.AdapterView;
import android.widget.ArrayAdapter;
import android.widget.ListView;
import android.widget.TextView;
import android.widget.AdapterView.OnItemClickListener;

public class Fifth extends Activity{
	 
	ArrayList<String> al=new ArrayList<String>();
	
	

		@Override
		protected void onCreate(Bundle savedInstanceState) {
	
		// TODO Auto-generated method stub
		
			super.onCreate(savedInstanceState);
			setContentView(R.layout.fifth);
			
			
			
			ListView lv=(ListView)findViewById(R.id.listView1);
			al.add("Guntur");
			al.add("Tirupathi");
			al.add("Vishakapatnam");
			al.add("Vijayawada");
			al.add("Nizamabad");
			al.add("Kurnool");
			al.add("Mahbubnagar");
			al.add("Khammam");
			
			lv.setAdapter(new ArrayAdapter<String>(getApplicationContext(), android.R.layout.simple_list_item_1, al));
			lv.setOnItemClickListener(new OnItemClickListener() {

				@Override
				public void onItemClick(AdapterView<?> arg0, View arg1,
						int arg2, long arg3) {
					// TODO Auto-generated method stub
					if (arg2 == 0) {
						Intent it = new Intent(Fifth.this, Guntur.class);
						startActivity(it);
					}
					if (arg2 == 1) {
						Intent it = new Intent(Fifth.this, Tirupathi.class);
						startActivity(it);
					}
					if (arg2 == 2) {
						Intent it = new Intent(Fifth.this, Vishakapatnam.class);
						startActivity(it);
					}
					if (arg2 == 3) {
						Intent it = new Intent(Fifth.this, Vijayawada.class);
						startActivity(it);
					}
					if (arg2 == 4) {
						Intent it = new Intent(Fifth.this, Nizamabad.class);
						startActivity(it);
					}
						if (arg2 == 5) {
							Intent it = new Intent(Fifth.this, Kurnool.class);
							startActivity(it);
						}
							if (arg2 == 6) {
								Intent it = new Intent(Fifth.this, Mahbubnagar.class);
								startActivity(it);
							}
								if (arg2 == 7) {
									Intent it = new Intent(Fifth.this, Khammam.class);
									startActivity(it);
								}
					
				}
				
			});
		}
}
		package com.example.project1;

import android.app.Activity;
import android.content.Intent;
import android.os.Bundle;
import android.view.View;
import android.view.View.OnClickListener;
import android.widget.Button;

public class Vijayawada extends Activity {
	@Override
	protected void onCreate(Bundle savedInstanceState) {
		// TODO Auto-generated method stub
		super.onCreate(savedInstanceState);
		setContentView(R.layout.vijayawada);
		Button bt=(Button)findViewById(R.id.button1);

 bt.setOnClickListener(new OnClickListener() {
				
				@Override
				public void onClick(View v) {
					// TODO Auto-generated method stub
					Intent it=new Intent(Vijayawada.this,Vijayawada1.class);
					startActivity(it);

		 

			}
	});
	}
	





package com.example.project1;

import android.app.Activity;
import android.os.Bundle;
public class Vijayawada1  extends Activity{
	@Override
	protected void onCreate(Bundle savedInstanceState) {
		// TODO Auto-generated method stub
		super.onCreate(savedInstanceState);
		setContentView(R.layout.vijayawada1);

}
}



		
		
	
