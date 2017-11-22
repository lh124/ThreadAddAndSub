package com.lh.uitl;

public class Test {
	public static void main(String[] args) {
		Numbers number=new Numbers();
		for(int i=0;i<2;i++) {
			new Thread(()->{
				for(int j=0;j<20;j++) {
					number.add();
				}
				
			},"A线程"+i) .start();
		}
		
		for(int i=0;i<2;i++) {
			new Thread(()->{
				for(int j=0;j<20;j++) {
					number.sub();
				}
				
			},"B线程"+i) .start();
		}
	}
}
