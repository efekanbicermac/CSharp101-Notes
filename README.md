# Homework 1;

## Kullanıcıdan Adını ve Soyadını Girmesini iste, daha sonra ise kişinin adı ve soyadı ile birlikte tek bir cümlede "Hoşgeldin isim1,soyisim1" şeklinde yazdır.
~~~csharp
            Console.WriteLine("Please Enter Your Name");
            string name1 = Console.ReadLine();
            Console.WriteLine("Please Enter Your Surname");
            string name2 = Console.ReadLine();
            
            Console.WriteLine($"Welcome {name1} {name2}");
          
~~~    
# Homework 2;
## Değişkenler ve Veri Tipleri 
~~~csharp
   
            byte b = 5; // 1 byte
            byte c = 5; // 1 byte

            short s = 5; // 2 byte
            ushort us = 5; // 2 byte

            float f = 5; //4 byte
            double d = 5; //8 byte
            decimal b = 5; // 16 byte

            uint ui = 2; // 4byte
            long l = 4; // 8byte 
            ulong ul = 4; // 16byt
~~~   
# Homework 3;
## Operatorler
~~~csharp
 //Atama
            int a = 3;
            int b = 4;
            //İşlemli Atama
            b = b + 3;
            b += 3;
            b /= 3;
            b *= 3;

            //Mantıksal Operatorler
            // ||, &&, !

            bool isSuccess = true;
            bool isCompleted = false;

            if (isSuccess && isCompleted)
                Console.WriteLine("Well Done");
            if (isSuccess || isCompleted)
                Console.WriteLine("Perfect");
            if (isSuccess && !isCompleted)
                Console.WriteLine("Great");

            //İlişkisel Operatorler
            // <, >, <=, >=, ==, != 

            int x = 3;
            int y = 4;
            bool sonuc = a < b;

            Console.WriteLine(sonuc);
            sonuc = a < b;
            Console.WriteLine(sonuc);
            sonuc = a >= b;
            Console.WriteLine(sonuc);
            sonuc = a <= b;
            Console.WriteLine(sonuc);
            sonuc = a == b;
            Console.WriteLine(sonuc);
            sonuc = a != b;

            //Aritmetik Operatorler
            // /, +, -, *

            // % MOD ALMA YANI BOLME ISLEMINDEN KALANI BULMA
~~~
# Homework 4;
## Expection Handler
~~~csharp
//TRY CATCH YONTEMI ILE HATA BULMA

            try
            {
                Console.WriteLine("Lutfen Yasinizi Giriniz : ");
                int yas = Convert.ToInt32(Console.ReadLine());
                Console.WriteLine($"Girdiginiz yas {yas}");
            }

            catch(Exception Exc)
            {
                Console.WriteLine($"Hata: {Exc.Message.ToString()}");
            }
            finally
            {
                Console.Write("Isleminiz Tamamlandi");
            }

            //Format ve OverFlow Hatasi
            try
            {
                int a = int.Parse("-99999");
            }
            catch(FormatException ex)
            {
                Console.WriteLine("Bos deger girdiniz");
                Console.WriteLine(ex);
            }

            catch ( OverflowException OFex )
            {
                Console.WriteLine("Cok kucuk yada Asiri Buyuk deger girdiniz");
                Console.WriteLine(OFex);
            }
~~~
# Homework 5;
## Karar Yapıları 1
~~~csharp
//  If Else Between Kullanımı
            int time = DateTime.Now.Hour;

            if ((time >= 08.00) && (time <= 12.00))
            {
                Console.WriteLine("Günaydın");
            }
            else if (((18.00 <= time) && (time < 22.00)))
            {
                Console.WriteLine("İyi günler");
            }
            else
            Console.WriteLine("İyi Geceler");
~~~
## Karar Yapıları 2
~~~csharp
//Switch Case Kullanımı

            int month = DateTime.Now.Month;

            switch(month)
            {
                case 1:
                Console.WriteLine("Ocak");
                    break;

                case 2:
                    Console.WriteLine("Şubat");
                    break;

                case 3:
                    Console.WriteLine("Mart");
                    break;



                default:
                    
                    Console.WriteLine("Hata");
                break;
            }
~~~
# Homework 6 ;
## Döngüler 1 
~~~csharp
//-----FOR DONGUSU-----
            //Ekrana girilen sayıya kadar olan çift sayilari ekrana yazdır
            Console.WriteLine("Lutfen bir sayi giriniz : ");
            int sayi = int.Parse(Console.ReadLine());

            for (int i = 0; i < sayi; i++)
            {
                if(i%2 == 0)
                {
                    Console.WriteLine(i);
                }
            }

            //0 Ile 2000 arasindaki sayilarin kendi icindeki toplamini yazdir

            int t = 0;
            int c = 0;

            for (int i = 0; i < 2000; i++)
            {
                if (i % 2 == 1)
                {
                    t += i;
                }
                else
                    c += i;
            }

            Console.WriteLine($"Tek sayilarin toplami {t}");
            Console.WriteLine($"Cift sayilarin toplami {c}");
~~~

