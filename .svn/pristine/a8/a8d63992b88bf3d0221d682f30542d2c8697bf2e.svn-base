package com.lh.uitl;

public class Numbers {
	//4���߳�
	private int num;
	private boolean flag=true;
	public synchronized void add() {
		while(flag==false) {
			try {
				this.wait();
			} catch (InterruptedException e) {
				e.printStackTrace();
			}
		}
		
		System.out.println(Thread.currentThread().getName()+","+this.num++);
		this.flag=false;
		this.notifyAll();
	}
	public synchronized void sub() {
		while(this.flag==true) {
			try {
				this.wait();
			} catch (InterruptedException e) {
				// TODO Auto-generated catch block
				e.printStackTrace();
			}
		}
		
		System.out.println(Thread.currentThread().getName()+","+this.num--);
		this.flag=true;
		this.notifyAll();
	}
}

//=====================
//Numbers number=new Numbers();
//for(int i=0;i<2;i++) {
//	new Thread(()->{
//		for(int j=0;j<20;j++) {
//			number.add();
//		}
//		
//	},"A�߳�"+i) .start();
//}
//
//for(int i=0;i<2;i++) {
//	new Thread(()->{
//		for(int j=0;j<20;j++) {
//			number.sub();
//		}
//		
//	},"B�߳�"+i) .start();
//}
//}
