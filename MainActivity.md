package com.example.mycash;

import android.app.ActionBar;
import android.app.Activity;
import android.content.Context;
import android.database.DataSetObserver;
import android.os.Bundle;
import android.support.v4.widget.DrawerLayout;
import android.view.View;
import android.view.ViewGroup;
import android.widget.AdapterView;
import android.widget.AdapterView.OnItemClickListener;
import android.widget.ArrayAdapter;
import android.widget.ListAdapter;
import android.widget.ListView;
import android.widget.Toast;


public class MainActivity extends Activity  {
	 		DrawerLayout drawerLayout;
	 		ListView listView;
	 		AdapterList adapterList;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
     //Hide Action Bar--------------------------------------   
        View decorView = getWindow().getDecorView();
        int uiOptions = View.SYSTEM_UI_FLAG_FULLSCREEN;
        decorView.setSystemUiVisibility(uiOptions);
        ActionBar actionBar = getActionBar();
        actionBar.hide();
    //Hide Action Bar---------------------------------------  
       listView = (ListView)findViewById(R.id.listMenu);
       final AdapterList adapterList = new AdapterList(this);
       listView.setAdapter(adapterList);
      
       
       drawerLayout = (DrawerLayout)findViewById(R.id.drawerLayout); 
       
        
        
    }//OnCreate Closing...

	/*@Override
	public void onItemClick(AdapterView<?> arg0, View arg1, int arg2, long arg3) {
			//Toast.makeText(getBaseContext(), "Test", Toast.LENGTH_SHORT).show();
	}*/
    
     
    


    

    
    
    
    
    
    
   
}
