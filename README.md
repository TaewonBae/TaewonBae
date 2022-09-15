# Profile
**👋 I'm a Android Devloper from South Korea, TaewonBae😘**


[![Gmail Badge](https://img.shields.io/badge/olegunnarsolskjaer1283@gmail.com-D14836?style=flat&logo=Gmail&logoColor=white)](mailto:olegunnarsolskjaer1283@gmail.com)
[![Instagram Badge](https://img.shields.io/badge/tae1ne-E4405F?style=flat&logo=Instagram&logoColor=white)](https://www.instagram.com/tae1ne/?hl=ko)
<br>
<br>
<!--
<img align='right' src="http://mazassumnida.wtf/api/v2/generate_badge?boj=tae1ne">
-->
### Who Am I


* 🔭 I'm a software major student at Gachon University.

* 🌱 I’m currently learning Java & Kotlin

* ❤ I value relationships.
<img src="https://github-readme-stats.vercel.app/api?username=TaewonBae&show_icons=true&theme=radical" height="165">

<br>
<br>



### My Favorite

* ⚽ Football

* ✈ Trip

* 💪🏻 Fitness

<br>
<br>

----------------------
<br>

**💪Tech Stack💪**

<img src="https://img.shields.io/badge/Android-3DDC84?style=flat-square&logo=Android&logoColor=white" /> <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=Python&logoColor=white"/> 
<img src="https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=OpenCV&logoColor=white" /> <img src="https://img.shields.io/badge/Numpy-013243?style=flat-square&logo=Numpy&logoColor=white" /> <img src="https://img.shields.io/badge/pandas-150458?style=flat-square&logo=pandas&logoColor=white" />
<img src="https://img.shields.io/badge/Swift-F05138?style=flat-square&logo=swift&logoColor=white" /> <img src="https://img.shields.io/badge/iOS-353E58?style=flat-square&logo=apple&logoColor=white" /> 
<br>

**🛠Cowork Tools🛠**

<img src="https://img.shields.io/badge/Visual Studio Code-007ACC?style=flat-square&logo=Visual Studio Code&logoColor=white" /> <img src="https://img.shields.io/badge/Atom-66595C?style=flat-square&logo=Atom&logoColor=white" />

<img src="https://img.shields.io/badge/Github-181717?style=flat-square&logo=Github&logoColor=white" /> <img src="https://img.shields.io/badge/Android Studio-3DDC84?style=flat-square&logo=Android Studio&logoColor=white" /> <img src="https://img.shields.io/badge/PyCharm-000000?style=flat-square&logo=PyCharm&logoColor=white" /> <img src="https://img.shields.io/badge/Xcode-147EFB?style=flat-square&logo=xcode&logoColor=white" />
 

<!--
**TaewonBae/TaewonBae** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on Android UI/UX Screen
- 🌱 I’m currently learning Java & Kotlin
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

<img align='right' src="https://github-readme-stats.vercel.app/api/top-langs/?username=TaewonBae&layout=compact" height="165">
-->

package codingTest;

public class Test2 {
	// 문제2 : 요세푸스 알고리즘
	// 숫자 2개 입력 ex) 7, 3
	// 첫번째 입력숫자 7 : 1,2,3,4,5,6,7
	// 두번째 입력숫자 3 : {1,2,3}=3 {4,5,6}=6 {7,1,2}=2 {4,5,7}=7 {1,4,5}=5 {1,4,1}=1 {4,4,4}=4
	// 최종 출력 숫자 {3,6,2,7,5,1,4}
	public static void main(String[]args){
		int a = 10;
		int b = 4;
		
		int good = 0; 
		int cnt = 0; 
		int[] data = new int[a];//O
		int[] test = new int[a];
		
		for(int i = 0; i < a; i++)
		{
			data[i] = i+1;
		}
		/////////
		for(int j = 0; j < a; j++) {
			for(int i = 0; i < 99; i++)
			{
				if(good == a)
				{
					good = 0;
				}
				
				if(data[good] < 0)
				{
					good++;
					continue;
				}
				else
				{
					cnt++;
					if(cnt == b)
					{
						test[j] = data[good];
						data[good] = -1;
						cnt = 0;
						break;
					}
					good++;
				}
			}
		}
		
		for(int i = 0; i < a; i++)
		{
			System.out.println(test[i]+" / " );
		}
		
	}
}
