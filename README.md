# Constructors

سيحتاج أي Class غالبًا إلى تنفيذ بعض مهام التهيئة عند نقطة الإنشاء. يمكن تنفيذ هذهِ المهام باستخدام Constructors ****في ****داخل Class.

لتوضيح مفهوم Constructors او ماتسمى دالة البناء لنفترض عند انشاء Object تريد اعطاء القيم له مباشره في وقت الانشاء بدون استخدام Instances لذالك نحتاج استخدام Constructor ويتم انشائه بنفس اسم Class لنخذ مثال يوضح هذا المفهوم 

 في حالة BankAccount class  المثال في السابق سيكون من المفيد أن تكون قادرًا على تهيئة رقم الحساب ورصيد الحساب  بالقيم عند إنشاء نسخة جديدة من هذا Class. لتحقيق ذلك يمكن تعريف constructor داخل Class على النحو التالي:



    
    class BankAccount {
        num accountBalance = 0.0;
        String accountName = 'Fahad Alazmi';
      
      BankAccount(this.accountBalance,this.accountName);
      
        displayBalance()
        {
           print("Name: $accountName");
           print("Current balance is $accountBalance");
        }
    }

نلاحظ تم انشاء Constructor بنفس اسم Class وهو BankAccount داخل Class وتم استخدام this للاشاره الى المتغير الموجود داخل هذا Class 

ملاحظه : this يتم استخدامها بالنيابه عن  Class للاشاره الى شيء  موجود داخله 

الان في حال تم انشاء Object من نفس Class الموجود داخل Constructor سوف يتم اعطاء القيم الخاصه في accountBalance and accountName مباشره  


    class BankAccount {
        num accountBalance = 0.0;
        String accountName = 'Fahad Alazmi';
      
      BankAccount(this.accountBalance,this.accountName);
      
        displayBalance()
        {
           print("Name: $accountName");
           print("Current balance is $accountBalance");
        }
    }
    
    main(){
     BankAccount account1 = BankAccount(103.5,'Fahad Alazmi');
     account1.displayBalance();
    }

بهذا الشكل تم انشائه وعطاء القيم مباشره وقت الانشاء 

المخرجات :

    Name: Fahad Alazmi
    Current balance is 103.5

ايضا يمكن انشاء Constructor يتم تنفيذ في وقت الانشاء بنفس الشكل السابق فقط يتم اضافة اقواس Object {} على Constructor 


    class BankAccount {
        num accountBalance = 0.0;
        String accountName = 'Fahad Alazmi';
      
      BankAccount(this.accountBalance,this.accountName){
        print("Welcome to our Bank");
      }
      
        displayBalance()
        {
           print("Name: $accountName");
           print("Current balance is $accountBalance");
        }
    }

نلاحظ تم اضافة جملة "Welcome to our Bank"  داخل Constructor  الان في حال تم انشاء اوبجكت من هذا الكلاس سوف يتم طباعة "Welcome to our Bank” في وقت الانشاء  كما هو في المثال التالي :


    class BankAccount {
        num accountBalance = 0.0;
        String accountName = 'Fahad Alazmi';
      
      BankAccount(this.accountBalance,this.accountName){
        
        print("Welcome th our Bank");
      }
      
        displayBalance()
        {
           print("Name: $accountName");
           print("Current balance is $accountBalance");
        }
    }
    
    main(){
     BankAccount account1 = BankAccount(103.5,'Fahad Alazmi');
    }

المخرجات :


    Welcome to our Bank

