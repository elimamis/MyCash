package com.example.mycash;

import android.content.Context;
import android.view.LayoutInflater;
import android.view.View;
import android.view.ViewGroup;
import android.widget.AdapterView;
import android.widget.AdapterView.OnItemClickListener;
import android.widget.BaseAdapter;
import android.widget.ImageView;
import android.widget.TextView;
import android.widget.Toast;

public class AdapterList extends BaseAdapter {
	
	private Context context;
	 
	String[] menu = {"How Much Did I Work"
			,"Add/Edit Work Space"
			,"My Profile"
			,"Send Work Doc Via Mail"
			,"Send FeedBack"
			,"Bug Report"};
	 int[] icons = {R.drawable.clock,R.drawable.edit,R.drawable.profile,R.drawable.mail,R.drawable.sendfeed,R.drawable.bug};
	
	public AdapterList(Context context){
		this.context = context;
		
	}

	@Override
	public int getCount() {
		
		return menu.length;
	}

	@Override
	public Object getItem(int position) {
		
		return menu[position];
	}

	@Override
	public long getItemId(int position) {
		// Not In Use  For Future Uses...
		return position;
	}

	@Override
	public View getView(int position, View convertView, ViewGroup parent) {
		View row = null;
		if(convertView == null){
			
			LayoutInflater inflater = (LayoutInflater) context.getSystemService(Context.LAYOUT_INFLATER_SERVICE);
			row = inflater.inflate(R.layout.custom_row_layout, null);
			
		}else{
			 row = null;
		}
		TextView customTextView = (TextView)row.findViewById(R.id.customText1);
		ImageView customImageView = (ImageView)row.findViewById(R.id.customImage1);
		
		customTextView.setText(menu[position]);
		customImageView.setImageResource(icons[position]);
		
		return row;
	}

	
}
