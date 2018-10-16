---
title : Interface 
localeTitle: جهة تعامل
---
* * *

واجهة مشابهة لفئة أو هيكل ولكن دون تنفيذ لأعضائها. تعلن الواجهة عن تعاقد أو سلوك يجب أن يتضمنه تطبيق الفئات. قد تعلن فقط الخصائص والأساليب والأحداث مع NO معدّلات الوصول.

يجب أن يتم تنفيذ جميع الأعضاء المعلنين في فئة التحكيم ، وإلا سيكون هناك خطأ في الترجمة. كالاتفاقية ، سنضع علامة على الواجهة بالحرف الأول في begenning (IMyInterface || IUserOptions). تقوم بتعريف واجهة باستخدام الكلمة الأساسية للواجهة.

جميع أعضاء الواجهة هم: مجرّد ضمنيًا ، ضمنياً ، لا يمكن الإعلان عن معدِّل وصول مثل المحمي أو الخاص الخ ...

واجهة يمكن:

*   اكتساب من واجهات أخرى.
*   اكتساب من واجهات متعددة في نفس الوقت
*   تحتوي فقط على أساليب وخصائص وأحداث ومفهرس.

لا يمكن للواجهة:

*   وراثة من فصل دراسي.
*   لديك التنفيذ.
*   لديك معدّلات الوصول بخلاف العام.

## \* يمكن استنساخه.

يسمح لنا استخدام الواجهات بتغيير تطبيقنا في مشروعنا دون كسر أجزاء أخرى ، ولا يتعين عليك سوى تغيير مكان واحد يتم فيه إنشاء الكائن.

مثال على واجهة:

 `public Interface IUserFavoriteFood 
 { 
  void AddFood(); 
  Task<User> EatFavoriteFood(int id); 
 } 
` 

* * *

الميراث واجهة والتنفيذ:

 `public class UserHungry : IUserFavoriteFood 
 { 
  public AddFood() 
  { 
    // Implementation: 
    // A method to add food. 
  } 
 
  public Task<User> EatFavoriteFood(int id) 
  { 
    // Implementation: 
    // A method to Eat food by id. 
  } 
 } 
`