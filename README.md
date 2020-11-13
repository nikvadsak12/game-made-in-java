package javasa;

import java.util.Scanner;

public class main {
  public static void main(String[] args) {
	patient p=new patient("nikunj",20,
			new eye( "left eye","short sighend","Blue",true),
	        new eye("right eye","normal","blue",true),
	        new heart("heart","normal",65),
	        new stomatch("stomatch","pud",false),
	        new skin("skin","burned","white",40));
	System.out.println("name : "+p.getName());
	System.out.println("age : "+p.getAge());
	
	
	Scanner sc=new Scanner(System.in);
	boolean shouldfinished=false;
	while(!shouldfinished) {
	     System.out.println("\n choise an orgen"+
	            "\n\t1. left eye" +	   
	            "\n\t2. right eye" +	 
	            "\n\t3. heart" +	 
	            "\n\t4. stomatch" +	 
	            "\n\t5. skin" +	 
	            "\n\t6.  quit");
	     int choise=sc.nextInt();
	     switch(choise) {
	     case 1:
	    	 p.getEye_leftEye().getdetail();
	    	 if(p.getEye_leftEye().isIsopened()) {
	    		 System.out.println("\t\t1. close the eye");
	    		 if(sc.nextInt()==1) {
	    			 p.getEye_leftEye().close();
	    		 }
	    		 else {
	    			 continue;
	    			 
	    		 }
	    	 }else {
	    		 System.out.println("t\t1. open the eye");
	    		 if(sc.nextInt()==1) {
	    			 p.getEye_leftEye().open();
	    		 }
	    		 else {
	    			 continue;
	    		 }
	    	 }
	    	 break;
	     case 2:
	    	 p.getEye_rightEye().getdetail();
	    	 if(p.getEye_rightEye().isIsopened()) {
	    		 System.out.println("\t\t1. close the eye");
	    		 if(sc.nextInt()==1) {
	    			 p.getEye_rightEye().close();
	    		 }
	    		 else {
	    			 continue;
	    			 
	    		 }
	    	 }else {
	    		 System.out.println("t\t1. open the eye");
	    		 if(sc.nextInt()==1) {
	    			 p.getEye_rightEye().open();
	    		 }
	    		 else {
	    			 continue;
	    		 }
	    	 }
	    	 break;
	     case 3:
	    	 p.getHert();
	    	 System.out.println("\t \t1. change the herat rate");
	    	 if(sc.nextInt() ==1) {
	    		 System.out.println("enter the heart rate: ");
	    	     int newheartrate=sc.nextInt();
	    	     p.getHert().setRate(newheartrate);
                 System.out.println("heart rate changed to: "+p.getHert().getRate());
                 
	    	 }
	    	 else {
	    		 continue;
	    	 }
	    	 break;
	     case 4:
	    	 p.getStomac().getdetail();
	    	 System.out.println("\t\t1.  digest");
	         if(sc.nextInt() == 1) {
	        	 p.getStomac().isIsempty();
	        	 
	         }
	         else {
	        	 continue;
	         }
	         break;
	     case 5:
	         p.getSkin().getdetail();
	          break;
	     default:
	    	 shouldfinished = true;
	    	 break;
	    	 
	     }
	      	
	}
	 }
}
