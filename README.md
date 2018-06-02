# -
可以作为自己的算法入门

package com.melo.nio;
/**
 * 找出一个数组中的第二大值
 * @author 76009
 *
 */
public class SecondBig {

	public static void main(String[] args) {
		int[] arr = {23,12,23,43,123222,43,232,32222,1234};
		getSecondBig(arr);
	}
	
	public static void getSecondBig(int[] arr) {
		int max1, max2;//第一大数字 第二大数字
		max1 = max2 = arr[0];//初始化值
		int v;//循环中的变量值
		for (int i=1; i<arr.length; i++) {
			v = arr[i];
			if (v > max2) {//只有当前值大于初始值才有资格进入逻辑判断
				//比第二大 ，取代第二
				if (v > max1) {
					//比第一还大大，取代最大
					max2 = max1;//原来的最大值变为第二大
					max1 = v;
				} else {
					max2 = v;//当前值为第二大
				}
			}
		}
		System.out.println("第二大值是： " + max2 + ",最大值是： " + max1);
	}
}
