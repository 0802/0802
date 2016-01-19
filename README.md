# 0802
java
package Make;

public class snsUnit {

	public static void main(String[] args) {
		// TODO Auto-generated method stub

	
		Sns sns = new Sns();
		sns.getLike(845481);
		System.out.println(sns.unit());
			
		
		
		
	
	}

}

class Sns{
	
	private int like=0;
	private String slike;
	private final int k=1000;
	private final int m=1000000;
	private final int b=100000000;

	 String unit(){
		if(like<1000){
			slike=String.valueOf(like+"like");
			return slike;
		}
		else if((k<=like)&&(like<m)){
			int kilo =like/k;
			slike=String.valueOf(kilo+"k"+"like");
			return slike;
		}
		else if((m<=like)&&(like<b)){
			int million =like/m;
			slike=String.valueOf(million+"m"+"like");
			return slike;
		}
		else if((b<=like)&&(like>2*b)){
			int billion = like/b;
			slike=String.valueOf(billion+"b"+"like");
			return slike;
		}else{
			return "over!!";
		}
		
	}
	int getLike(int like){
		this.like=like;
		return like;
	}
	public String toString(){
		return slike;
	}
}
