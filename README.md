# Notes 1;

## Kullanıcıdan Adını ve Soyadını Girmesini iste, daha sonra ise kişinin adı ve soyadı ile birlikte tek bir cümlede "Hoşgeldin isim1,soyisim1" şeklinde yazdır.
~~~csharp
            Console.WriteLine("Please Enter Your Name");
            string name1 = Console.ReadLine();
            Console.WriteLine("Please Enter Your Surname");
            string name2 = Console.ReadLine();
            
            Console.WriteLine($"Welcome {name1} {name2}");
          
~~~    
# Notes 2;
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
# Notes 3;
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
# Notes 4;
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
# Notes 5;
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
# Notes 6 ;
## Döngüler 1 
~~~csharp
//-----FOR DONGUSU-----
            //Ekrana girilen sayıya kadar olan çift sayilari ekrana yazdır
            Console.WriteLine("Lutfen bir sayi giriniz : ");
            int sayi = int.Parse(Console.ReadLine()); // Console.ReadLine sadece int deger alabildigi icin Parse kullanmamiz gerekti

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
            
            //----Break, Continue----

            for (int i = 0; i < 20; i++)
            {
                if(i==14)
                { break; }
                if(i==8)
                { continue; }
                Console.WriteLine(i);
                
            }
            
~~~
## Döngüler 2 
~~~csharp
//-----While Döngüsü------

            //1 den başlayarak console dan girilen sayıya kadar (sayı dahil) ortalama hesaplayaıp console a yazdıran program
            Console.WriteLine("Lutfen bir sayi giriniz : ");
            int sayi1 = int.Parse(Console.ReadLine());
            int sayac = 1;
            int toplam = 0;
            while (sayac <= sayi1)
            {
                toplam += sayac;
                sayac++;
            }

            Console.WriteLine(toplam / sayi1);



            // A dan Z ye kadar, z dahil olmak uzere  tum harfleri konsola yazdir


            char harf = 'a';
            while (harf <= 'z')
            {
                Console.Write(harf);
                harf++;
            }

            //Foreach

            string[] arabalar = { "FORD", "MERCEDES", "LADA", "BMW", "NISSAN", "TOYOTA" };
            foreach (var araba in arabalar)
            {
                Console.WriteLine(araba);
            }
~~~
# Notes 7;
## Diziler 1
~~~csharp
//Dizi Tanimlama


            string[] ArabaMarkalari = new string[5];

            string[] MotorsikletMarkalari = { "Honda", "Kawasaki", "Yamaha" };

            int[] Sayilar = new int[99];

            int[] PlakaKodlari = { 01, 02, 03, };

            string[] Film;

            Film = new string[10];

            //Dizilere Deger Atama ve Erisim
            Film[4] = "Interstellar";


            string[] Yemekler = { "Mercimek", "Yahni", "Salata", "Makarna", "Hamburger" };
            Console.WriteLine(Yemekler[3]);
            Console.WriteLine(Yemekler[0]);


            //Dongulerle Dizi Kullanimi
            // Klavyeden girilen n tane sayinin ortalamasini hesaplayan program
            Console.Write("lUTFEN DIZININ ELEMAN SAYISINI GIRINIZ : ");
            int diziuzunlugu = int.Parse(Console.ReadLine());
            int[] sayiDizisi = new int[diziuzunlugu];

            for (int i = 0; i < diziuzunlugu; i++)
            {
                Console.Write("Lutfen {0}. sayiyi giriiniz : ", i + 1);
                sayiDizisi[i] = int.Parse(Console.ReadLine());
            }
            int toplam = 0;
            foreach (var sayi in sayiDizisi)
            {
                toplam += sayi;
                Console.WriteLine($"Ortalama {toplam / diziuzunlugu}");

            }
~~~
# Notes 8;
## Metotlar 1
~~~csharp
class MainClass
    {
        public static void Main(string[] args)
        {
            //Metotlar
            //erisim_belirteci(int, string) geri_donustipi(void vs) metot_adi(parametrelistesi/arguman)
            //{
            // komutlar;
            // retunn;
            //}

            int a = 2;
            int b = 3;
            Console.WriteLine(a + b);
            //Static metotlar sadece static metolar icerisinde kullanilabilir.
            //Metot statik degil ve statik bir metotta uygulanmaya calisiyorsa hata verecekir
            // Baska bir classtaki metota ulasmak icin o metutun instance sini yani orneklemesini yaratmamiz gerekir

            int sonuc = Topla(a, b);
            Console.WriteLine(sonuc);

            //Instance yaratma
            Metotlar ornek = new Metotlar();
            ornek.EkranaYazdir(Convert.ToString(sonuc));
        }

        static int Topla(int deger1, int deger2)
        {
            return (deger1 + deger2);
        }
    }
    class Metotlar
    {
        //Baska bir classtan erisilebilmesi icin public olmasi gerekir
        //Baska bir classtan metottaki degiskenlere mudahele etmek icin degiskenleri tanimlarken ref eklememiz gerekir (ref a, ref b)
          public void EkranaYazdir(string veri)
        {
            Console.WriteLine(veri);
        }
    }
~~~
## Metotlar 2 
~~~csharp
public static void Main(string[] args)
        {
            // Out Parametreler
            string number = "111";
            int Outnumber;

            bool sonuc = int.TryParse(number, out Outnumber);
            if (sonuc)
            {
                Console.WriteLine("Cevirildi");
                Console.WriteLine(Outnumber);
            }
            else
            {
                Console.WriteLine("Cevirilemedi");
            }
            Metotlar2 instance = new Metotlar2();
            instance.Topla(4, 5, out int toplamSonuc);

            //Metot Overloading(Asiri Yukleme)
            int ifade = 111;
            instance.EkranaYazdir(ifade);

            //Metot Imzasi nedir
            //metotAdi + paranetre sayisi + paranetre
            //Metot imzasina uymazsak public kismini veya void kismini vs degistitirsek altini cizer hata aliriz


        }
    }
    class Metotlar2
    {
        public void Topla(int a, int b, out int toplam)
        {
            toplam = a + b;
            
        }

        public void EkranaYazdir(string veri)
        {
            Console.WriteLine(veri);
        }
                                        //ayni metodu hem string hem de int tipinde olusturduk bu overloadingtir
        public void EkranaYazdir(int veri)
        {
            Console.WriteLine(veri);
        }

    }
~~~
## Metotlar 3 
~~~csharp
public static void Main(string[] args)
        {
            //Rekursif(Oz Yinelemeli)
            //3^4 = 3*3*3*3
            int result = 1;
            for (int i = 1; i < 5; i++)
            {
                result = result * 3;
                Console.WriteLine(result);
                Islemler instance = new();
                Console.WriteLine(instance.Expo(3, 4));
            }

            //Extension Metotlar
            string ifade = " Efekan Bicer";
            Console.WriteLine(ifade.BoslukKontrol());
            bool sonuc = ifade.BoslukKontrol();
            Console.WriteLine(sonuc);

        }

    }

    public class Islemler {

        public int Expo(int sayi, int us)
        {
            if (us < 2)
                return sayi;

            return Expo(sayi, us - 1) * sayi;
        }

    }

      //Extension classlar static olmak zorunda yoksa erisliemez
      //this ifadesini eklersek extension olur
      public static class Extensions
    {
        public static bool BoslukKontrol(this string param)
        {
            return param.Contains(" ");
        }
~~~
# Notes 9;
## Hazir Metotlar 1
~~~csharp
 // String Metotlar

            string degisken = "IOS'mu Android mi?";
            string degisken2 = "Xaomi is the BEST!";
            //Lenght
            Console.WriteLine(degisken.Length);

            //ToUpper, ToLower

            Console.WriteLine(degisken.ToUpper());

            Console.WriteLine(degisken.ToLower());

            //Contact
            Console.WriteLine(String.Concat(degisken, "Yada BlackBerryOS mu?"));

            //CompareTO
            Console.WriteLine(degisken.CompareTo(degisken2));
            // 1. degisken 2. degiskene esit olursa 0, 1. degisken 2. degiskenden buyukse 1,  1.degisken 2. degiskenden kucukse -1 dondurur

            //Contains
            Console.WriteLine(degisken.Contains(degisken2));
            Console.WriteLine(degisken.EndsWith("mi?"));
            Console.WriteLine(degisken.StartsWith("IOS"));

            //IndexOf
            Console.WriteLine(degisken.IndexOf("An"));

            //Insert
            Console.WriteLine(degisken.Insert(0, "Selam, "));

            //PadLeft, PadRight
            Console.WriteLine(degisken + degisken2.PadLeft(30));//30 a tamamliyacak kadar bosluk ekler PadLeft(30, '-') yazarsak da 30 tane - ekler

            //Remove

            Console.WriteLine(degisken.Remove(10)); // 10. indexten sonrassini siler

            //Replace
            Console.WriteLine(degisken.Replace("IOS", "iOS"));

            //Split
            Console.WriteLine(degisken.Split(' ')[1]); // Paranteze yazilanlari es gecer. Burda bosluklari es gectik. Boyle yapinca bosluklari silip bir diziye atti ve bizde 1. indexi getir dedik

            //Substring
            Console.WriteLine(degisken.Substring(4, 6)); //4. indexten baslayip 6. indexe kadar getir dedik
~~~
## Hazir Metotlar 2 
~~~csharp
//DateTime ve Math Kutuphanesi
            Console.WriteLine(DateTime.Now);
            Console.WriteLine(DateTime.Now.Date);
            Console.WriteLine(DateTime.Now.Day);
            Console.WriteLine(DateTime.Now.Year);
            Console.WriteLine(DateTime.Now.Second);
            Console.WriteLine(DateTime.Now.Minute);
            Console.WriteLine(DateTime.Now.Month);
            Console.WriteLine(DateTime.Now.Hour);

            Console.WriteLine(DateTime.Now.DayOfWeek);
            Console.WriteLine(DateTime.Now.DayOfYear);


            Console.WriteLine(DateTime.Now.ToLongDateString());
            Console.WriteLine(DateTime.Now.ToShortDateString());

            Console.WriteLine(DateTime.Now.ToShortTimeString());
            Console.WriteLine(DateTime.Now.ToShortTimeString());

            Console.WriteLine(DateTime.Now.AddDays(2));
            Console.WriteLine(DateTime.Now.AddHours(3));
            Console.WriteLine(DateTime.Now.AddSeconds(5));
            Console.WriteLine(DateTime.Now.AddMonths(7));
            Console.WriteLine(DateTime.Now.AddYears(9));
            Console.WriteLine(DateTime.Now.AddMilliseconds(50));

            //Math Kutuphanesi

            Console.WriteLine(Math.Abs(-25));
            Console.WriteLine(Math.Sin(10));
            Console.WriteLine(Math.Cos(10));
            Console.WriteLine(Math.Tan(10));

            Console.WriteLine(Math.Ceiling(23.4));//en dusuk olabilecege yuvarlar yani 23
            Console.WriteLine(Math.Round(23.2));// Yuvarlar 23
            Console.WriteLine(Math.Round(23.8));//24
            Console.WriteLine(Math.Floor(23.8));// en kucuk tam sayiyi yuvarlar 23

            Console.WriteLine(Math.Min(3, 6));
            Console.WriteLine(Math.Max(3, 6));

            Console.WriteLine(Math.Pow(3, 6));// 3^6 yi alir
            Console.WriteLine(Math.Sqrt(3));// Karekokunu alir

~~~
# Notes 10;
## Koleksiyonlar 1
~~~csharp
//KOLEKSIYONLAR

            //Generic List (System.Collections.Generic)
            //List<T> class   T object turundedir.

            List<int> numaraListesi = new List<int>();

            numaraListesi.Add(5);
            numaraListesi.Add(4);
            numaraListesi.Add(10);
            numaraListesi.Add(16);
            numaraListesi.Add(2);


            List<string> isimListesi = new List<string>();

            isimListesi.Add("Ahmet");
            isimListesi.Add("Mehmet");
            isimListesi.Add("Selim");
            isimListesi.Add("Emir");
            isimListesi.Add("Halil");
            isimListesi.Add("Emre");
            isimListesi.Add("Tayfun");

            //Count 
            Console.WriteLine(isimListesi.Count);
            Console.WriteLine(numaraListesi.Count);

            foreach (var isim in isimListesi)
            {
                Console.WriteLine(isim);
            }
            foreach (var numara in numaraListesi)
            {
                Console.WriteLine(numara);
            }
            //Contains ile Liste icinde arama
            if (numaraListesi.Contains(10))
                Console.WriteLine("Numara Listesinde 10 bulundu!");

            //Listeden Eleman Cikartma

            numaraListesi.Remove(10);
            isimListesi.Remove("Halil");

            //Eleman Icerisinde Index Arama
            Console.WriteLine(isimListesi.BinarySearch("Emir"));

            //Diziyi Listeye Cevirme

            string[] kumesHayvanlari = { "Tavuk", "Horoz", "Hindi" };

            List<string> kumeshayvanlariListesi = new List<string>(kumesHayvanlari);

            //Liste Temizleme
            kumeshayvanlariListesi.Clear();

~~~
## Koleysiyonlar 2
~~~csharp
//ArrayList System.Collections

            ArrayList liste = new ArrayList();
            liste.Add("Mehmet");
            liste.Add(17);
            liste.Add(6);
            liste.Add(true);
            liste.Add('B');

            //Verilerini erisim
            Console.WriteLine(liste[2]);

            foreach (var item in liste)
            {
                Console.WriteLine(item);
            }

            //AddRange (Listeye ekleme yapma)

            string[] ebeveyn = { "Ali", "Fatma", "Orhan" };
            liste.AddRange(ebeveyn); // Sadece Collection tiplerini ekleyebiliriz

            //Sort
            liste.Sort(); // Sort int32 leri siralamaya baslar fakat bu arrayliste her tipten veri girdik bu yuzden compile error verecektir

            //Binary Search
            Console.WriteLine(liste.BinarySearch(5));

            //Reverse
            liste.Reverse();
            foreach (var item in liste)
            {
                Console.WriteLine(item);
            }

            //Clear
            liste.Clear();
            foreach (var item in liste)
            {                               //Foreach zorunluluk degil. Yapilan islemi gormek icin yazdim. 
                Console.WriteLine(item);
            }
~~~
## Koleksiyonlar 3
~~~csharp
//Dictionary (System.Collections.Generic)

            Dictionary<int, string> renkler = new Dictionary<int, string>();

            renkler.Add(1, "siyah");
            renkler.Add(2, "mavi");
            renkler.Add(3, "beyaz");        //TKey ve Tvalue olarak calisan bu sistem, TKey yani kodudur. Mesela 3 u cagir dersem beyaz gelir
            renkler.Add(4, "gri");

            //Dictionary dizisinin elemanlarina erisim
            Console.WriteLine(renkler[2]);

            foreach (var item in renkler)
            {
                Console.WriteLine(item); 
            }

            //Count
            Console.WriteLine(renkler.Count);

            //Contains
            Console.WriteLine(renkler.ContainsKey(4));         //Contains tip olarak value ve keyden olustugu icin contains syntaxi boyle.
            Console.WriteLine(renkler.ContainsValue("siyah"));

            //Remove
            renkler.Remove(3);
            foreach (var item in renkler)
            {
                Console.WriteLine(item);
            }

            //Keys
            foreach (var item in renkler.Keys)
            {
                Console.WriteLine(item);
            }

            //Values
            foreach (var item in renkler.Values)
            {
                Console.WriteLine(item);
            }
~~~

# Notes 11;
## Sinif Kavrami 1
~~~csharp
 //Soz Dizini
            // class SinifAdi
            //{
            //  [Erisim Belirleyici] [Veri Tipi] OzellikAdi;
            //  [Erisim Belirleyici] [Geri Donus Tipi] metotAdi(Parametre Listesi)
            //  {
            //     //Metot Komutlari
            //  }
            //}

            //Erisim Berileyicileri
            //
            //  public
            //  private
            //  protected
            //  internal

            Personeller personel1 = new Personeller();
            personel1.CalisanAdi = "Eray";
            personel1.CalisanSoyadi = "Ersoy";
            personel1.CalisanNo = 11111;
            personel1.CalisaninDepartmani = "Frontend D.";

            personel1.PersonelBilgiler();
            Console.WriteLine("-------------");

            Personeller personel2 = new Personeller();
            personel2.CalisanAdi = "Cafer Ihsan";
            personel2.CalisanSoyadi = "Biraci";
            personel2.CalisanNo = 22222;
            personel2.CalisaninDepartmani = "Hademe D,";


            personel2.PersonelBilgiler();
            Console.WriteLine("-------------");
        }
    }

    class Personeller
    {
        public string CalisanAdi;

        public string CalisanSoyadi;

        public int CalisanNo;

        public string CalisaninDepartmani;

        public void PersonelBilgiler()
        {
            Console.WriteLine("Calisan Adi:{0}", CalisanAdi);

            Console.WriteLine("Calisan Soyadi:{0}", CalisanSoyadi);

            Console.WriteLine("Calisan No:{0}", CalisanNo);

            Console.WriteLine("Calisanin Departmani:{0}", CalisaninDepartmani) ;
        }
    }
~~~
## Sinif Kavrami 2
~~~csharp
//Soz Dizini
           //Constructor yapimi , Personel adinda bir class actik ve bu klasi main class ta instance yaratar hallettik. Personeller adinda constructor method yazdik

            Personeller personel1 = new Personeller("Eray","Ersoy",11111,"Frontend D.");
            
            personel1.PersonelBilgiler();
            Console.WriteLine("-------------");

            Personeller personel2 = new Personeller("Cafer Ihsan","Biraci",22222,"Hademe D.");

            personel2.PersonelBilgiler();
            Console.WriteLine("-------------");
        }
    }

    class Personeller
    {
        public string CalisanAdi;

        public string CalisanSoyadi;

        public int CalisanNo;

        public string CalisaninDepartmani;


        public Personeller(string CalisanAdi, string CalisanSoyadi, int CalisanNo, string CalisaninDepartmani)
        {
            this.CalisanAdi = CalisanAdi;
            this.CalisanSoyadi = CalisanSoyadi;
            this.CalisanNo = CalisanNo;
            this.CalisaninDepartmani = CalisaninDepartmani;



        }

        public Personeller() { } 

        public void PersonelBilgiler()
        {
            Console.WriteLine("Calisan Adi:{0}", CalisanAdi);

            Console.WriteLine("Calisan Soyadi:{0}", CalisanSoyadi);

            Console.WriteLine("Calisan No:{0}", CalisanNo);

            Console.WriteLine("Calisanin Departmani:{0}", CalisaninDepartmani) ;
        }
    }



}

~~~
## Sinif Kavrami 3
~~~csharp
//Encapsulation

            Customers customer = new Customers();
            customer.CustomerName = "Ragnar";
            customer.CustomerSurname = "Lothbrok";
            customer.CustomerNo = 15;
            customer.CustomerScore = 1000;
            customer.GetTheCustomerInfo();

            customer.IncreaseScore();
            customer.GetTheCustomerInfo();


            Customers customer2 = new Customers();
            customer.CustomerName = "Bjron";
            customer.CustomerSurname = "Ironside";
            customer.CustomerNo = 12;
            customer.CustomerScore = 1500;
            customer.GetTheCustomerInfo();

            customer.DecreaseScore();
            customer.GetTheCustomerInfo();




        }
    }

    class Customers
    {
        private string customerName; // Sag tik quick actions a tiklayarak alttan encapsulate field and use property ye tikliyoruz

        private string customerSurname;

        private int customerNo;

        private int customerScore;




        public string CustomerName { get => customerName; set => customerName = value; }

        public string CustomerSurname { get => customerSurname; set => customerSurname = value; }

        public int CustomerNo { get => customerNo; set => customerNo = value; }

        public int CustomerScore
        {

            get => customerScore;

            set
            {
                if(customerScore <= 0)      //Musteri Puani 0 dan kucuk olamayacagi icin boyle bir kod yazdik
                {
                    Console.WriteLine("Puan 0 in altinda olamaz ");
                    customerScore = 0;
                }
                

                else
               customerScore = value;
               
               // Simdi bu sinifin constructor unu yaratalim
        // Constructor class ile ayni isime sahip olmak zorunda ayrica herhangi bir donus tipi yazilamaz

        public Customers(string customerName, string customerSurname, int customerNo, int customerScore)
        {
            CustomerName = customerName;
            CustomerSurname = customerSurname;
            CustomerNo = customerNo;
            CustomerScore = customerScore;
        }

        public Customers()
        {

        }

        public void GetTheCustomerInfo()
        {
            Console.WriteLine("------Musteri Bilgiler-------");
            Console.WriteLine("Musteri Ismi :{0} ",this.CustomerName);
            Console.WriteLine("Musteri Soyadi :{0} ", this.CustomerSurname);
            Console.WriteLine("Musteri No :{0} ", this.CustomerNo);
            Console.WriteLine("Musteri Puani :{0} ", this.CustomerScore);
        }

        public void IncreaseScore()
        {
            this.CustomerScore = this.CustomerScore +1;

        }

        public void DecreaseScore()
        {
            this.CustomerScore = this.CustomerScore - 1;
        }

            } 
~~~
