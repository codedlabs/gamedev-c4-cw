
---


# <p dir="rtl">
فيديوهات الدرس</p>




* 
[تحريك الصاروخ ١](https://www.youtube.com/watch?v=_O0atCa_ubY&list=PL_gewShnRvv_n0U2MPdkUsMqsX4_KxYHW&index=17)


* 
[تحريك الصاروخ ٢ ](https://www.youtube.com/watch?v=1A-vLa-sr8I&list=PL_gewShnRvv_n0U2MPdkUsMqsX4_KxYHW&index=16) 

---


# <p dir="rtl">
شرح الدرس </p>




* اضافة متغير من نوع Rigidbody

    ```
 Rigidbody rocketRB;
```


* يجب تعيين قيمة للمتغير داخل دالة  start()

        ```
void Start () {
		rocketRB = GetComponent<Rigidbody>();
	   }
```


* يجب كتابة دالة ال Thrust() المسؤولة عن حركة الصاروخ للأعلى

    ```
 private void Thrust(){
		if (Input.GetKey(KeyCode.Space)) {
		print ("Thrusting");
		rocketRB.AddRelativeForce (Vector3.up);
		}
		}
```



<p dir="rtl">
</p>




* 
يجب كتابة دالة الrotate() المسؤولة عن حركة الصاروخ الافقية

```
void Rotate ()
	    {
		rocketRB.freezeRotation = true; //this says that we will take manual control of the rotation
		if (Input.GetKey (KeyCode.A)) {
		    transform.Rotate (Vector3.forward);
		}
		else
		    if (Input.GetKey (KeyCode.D)) {
			transform.Rotate (-Vector3.forward);
		    }
		rocketRB.freezeRotation = false;
	    }

```



---

**[Github](https://github.com/kuwaitcodes/gamedev-c4-cw)**

<p dir="rtl">
<strong>تمرين</strong> </p>



* صمموا المرحلة عن طريق اضافة:
- مكان الإنطلاق - Launch pad
- الأرض - Terrain
* صمموا الصاروخ عن طريق اضافة اجسام ثلاثية الابعاد
* 
أضف RigidBody على الصاروخ (3D RigidBody)


* 
أنشئ دالة Thrust() - عندما يضغط المستخدم Space تتحرك المركبة إلى الأعلى


* 
أنشئ دالة Rotate()  - عندما يضغط المستخدم A أو D تتدحرج المركبة إلى اليمين أو اليسار 
