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
	private final int k=1000;//천
	private final int m=1000000;//백만
	private final int b=100000000;//십억

	 String unit(){
		if(like<1000){
			slike=String.valueOf(like+"좋아요");
			return slike;
		}
		else if((k<=like)&&(like<m)){
			int kilo =like/k;
			slike=String.valueOf(kilo+"k"+"좋아요");
			return slike;
		}
		else if((m<=like)&&(like<b)){
			int million =like/m;
			slike=String.valueOf(million+"m"+"좋아요");
			return slike;
		}
		else if((b<=like)&&(like>2*b)){
			int billion = like/b;
			slike=String.valueOf(billion+"b"+"좋아요");
			return slike;
		}else{
			return "값을 잘못입력 또는 값이 오버";
		}
		
	}
	int getLike(int like){
		this.like=like;
		return like;
	}
	void returnLikeUnit(){//문자열 클래스에서 문자열안에서 원하는 한 글자를 찾는 기능에 메서드를 찾아서 JAVA카테고리에 쓰고 하기
		
	}
	public String toString(){
		return slike;
	}
}
