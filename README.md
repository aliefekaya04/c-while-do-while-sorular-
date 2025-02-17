1-    Kullanıcıdan 10 adet sayı alın ve bir diziye ekleyin
    Sayıların kaç tanesinin çift, kaç tanesinin tek olduğunu while (do-while)döngüsü ile kontrol edin ve ekrana yazdırın
    
    int[] numbers = new int[10];
    int i = 0, teksayi = 0, ciftSayi = 0;
    Console.Write("10 TANE SAYI GİRİNİZ");
    while (i < 10)
    {
        Console.Write($"sayı  {i + 1}:");
        numbers[i] = int.Parse(Console.ReadLine());
        i++;
    }
    i = 0; //sayac sıfırlama işlemi için böyle bir atama yaptım
    
    do
    {
        if (numbers[i] % 2 == 0)
        {
            ciftSayi++;
        }
        else
        {
            teksayi++;
        }
        i++;
    
    } while (i < 10);
    
    
    Console.WriteLine($"GİRİLEN SAYILAR {ciftSayi} TANESİ ÇİFT,{teksayi} TANESİ İSE TEK SAYIDIR");



2- Kullanıcıdan sırayla 3 adet sayı alın
   Programımız sırayla 3 adet rastgele sayı üretsin
   Bu işlemler bittikten sonra kullanıcıdan aldığımız sayılar ile rastgele ürettiğimiz sayıları sırasıyla karşılaştıralım
   Eğer 1 sayı eşleşiyorsa "Kaybettiniz"
        2 sayı eşleşiyorsa "Amorti Kazandınız"
        3 sayı eşleşiyorsa "Kazandınız" şeklinde mesaj yazdıralım

        
        int[] kullanicisayilari = new int[3];
        int[] rastgelesayilar = new int[3];
        Random rastgele = new Random();
        int a = 0, eslesme_sayisi = 0;
        Console.Write("3 ADET SAYI GİRİNİZ ANCAK  1-10 ARASINDA OLSUN");
        while (a < 3)
        {
            Console.Write($"SAYI {a + 1 }:");
            kullanicisayilari[a] = int.Parse(Console.ReadLine());
            a++;
        
        }
        a = 0;
        Console.Write("RASTGELE ÜRETİLEN SAYILAR: ");
        do
        {
            rastgelesayilar[a] = rastgele.Next(1, 11);
            Console.Write($"RASTGELE SAYILAR {a + 1}:{rastgelesayilar[a]}");
            a++;
        
        
        } while (a   < 3);
        a = 0;
        do
        {
            
        
        if (Array.Exists(rastgelesayilar,eleman => eleman == kullanicisayilari[a]))
            {
                eslesme_sayisi++;
            }
            a++;
        
        } while (a < 3);
        
        Console.Write("SONUC : ");
        if (eslesme_sayisi == 1)
        {
            Console.Write("! KAYBETTİNİZ !");
        }
        else if (eslesme_sayisi == 2)
        {
            Console.Write("AMORTİ VURDUU GOL OLDU OW YEAAAHHH");
        }
        else if (eslesme_sayisi == 3)
        {
            Console.Write("TEBRİKLLLEEERRR KAZANDINIIIIZZZZ");
        }
        else
        {
            Console.Write("GİT BAK BAKAYIM ANKARA HAVASI NASILMIŞ");
        }





3- Programımız rastgele 2 sayı üretsin
   Üretilen bu 2 sayının çarpını kullanıcıya soralım
   Kullanıcı doğru cevabı verene kadar kullanıcıdan cevap isteyelim

   -no solution-

4-Kullanıcıdan 3 adet sayı talep edelim
  Kullanıcının girdiği sayıların en büyüğünü ve en küçüğünü ekrana yazdıralım

  
      int sayi1, sayi2, sayi3;
    
      Console.Write("1. sayıyı girin: ");
      sayi1 = Convert.ToInt32(Console.ReadLine());
      Console.Write("2. sayıyı girin: ");
      sayi2 = Convert.ToInt32(Console.ReadLine());
      Console.Write("3. sayıyı girin: ");
      sayi3 = Convert.ToInt32(Console.ReadLine());
      int enBuyuk = sayi1;
      if (sayi2 > enBuyuk)
          enBuyuk = sayi2;
      if (sayi3 > enBuyuk)
          enBuyuk = sayi3;
      int enKucuk = sayi1;
      if (sayi2 < enKucuk)
          enKucuk = sayi2;
      if (sayi3 < enKucuk)
          enKucuk = sayi3;
      
      Console.WriteLine("En büyük sayı: " + enBuyuk);
      Console.WriteLine("En küçük sayı: " + enKucuk);
  
    
  
  5- Rastgele 5 tane sayı üretelim
     Sonra kullanıcıdan bir değer talep edelim
     Kullanıcının belirttiği değer ürettiğimiz 5 adet sayıda var mı yok mu kontrolünü yapalım
     
     Random random = new Random();
     int[] sayilar = { random.Next(1, 101), random.Next(1, 101), random.Next(1, 101), random.Next(1, 101), random.Next(1, 101) };
  
     Console.WriteLine("Rastgele üretilen 5 sayı: " + sayilar[0] + " " + sayilar[1] + " " + sayilar[2] + " " + sayilar[3] + " " + sayilar[4]);
              
     Console.Write("Bir sayı girin: "); 
     int kullaniciSayisi = int.Parse(Console.ReadLine());
  
  
  
     bool bulundu = (sayilar[0] == kullaniciSayisi) || (sayilar[1] == kullaniciSayisi) ||
                    (sayilar[2] == kullaniciSayisi) || (sayilar[3] == kullaniciSayisi) ||
                    (sayilar[4] == kullaniciSayisi);
  
              
     Console.WriteLine(bulundu ? "Girilen sayı listede mevcut!" : "Girilen sayı listede yok."); //burada biraz chatgpt'den yardım almış olabilirim :)
  

   

6-    Kullanıcıdan iki dizi elemanları alın(Dizilerin eleman sayısını siz belirleyin iki dizininde eleman sayısı aynı olsun).
    Aynı indekslerdeki elemanların toplamını yeni bir diziye atayın ve sonucu yazdırın.

    
            int elemansayisi = 7;
            int[] dizi1 = new int[elemansayisi];
            int[] dizi2 = new int[elemansayisi];
            int[] toplamdizi = new int[elemansayisi];

            Console.Write("BİRİNCİ DİZİ ELEMANLARINI GİRİN : ");
            int indeks = 0;
            while (indeks < elemansayisi)
            {
                Console.Write(" eleman{0}: " , indeks + 1);
                dizi1 [indeks] = int.Parse(Console.ReadLine());
                indeks++;
            }
            Console.Write("ikinci dizi elemanlarını giriniz");
            indeks = 0;
            while (indeks < elemansayisi)
            {
                Console.Write(" Eleman {0}: ", indeks + 1);
                dizi2 [indeks] = int.Parse(Console.ReadLine());
                indeks++;
            }
            Console.Write("İki dizinin aynı indekslerdeki elemanlarının toplamı: ");
            indeks = 0;
            while (indeks < elemansayisi)
            {
                toplamdizi[indeks] = dizi1[indeks] + dizi2[indeks];
                Console.WriteLine("Toplam[{0}] = {1}", indeks, toplamdizi[indeks]);
                indeks++;
            }


    

7- Bir torbada 18 kırmızı 18 siyah 2 yeşil top olduğunu düşünelim . Kullanıcıya seçmek istediği rengi soralım
bundan sonra programada rastgele olacak şekilde  belli oranlar içerisinde kırmızı , siyah,yeşil
(kırmızın 18/38 , siyahın 18/38 , yeşilin 2/38) top seçtirelim . 
Eğer kullanıcın seçtiği renk ile programın seçtiği renk aynıysa "Kazandınız" değilse "Kaybettiniz" mesajını döndürelim

    int kirmiziTop = 18;
    int siyahTop = 18;
    int yesilTop = 2;
    
     
    Console.WriteLine("Hangi rengi seçmek istersiniz? (Kırmızı, Siyah, Yeşil): ");
    string secim = Console.ReadLine();
                           rm
    // büyük-küçük harf duyarlılığı (el ile kontrol sağladım diğer yolu bilmiyom)
    
    if (secim == "Kırmızı" || secim == "kırmızı" || secim == "KIRMIZI")
    {
        secim = "kirmizi";
    }
    else if (secim == "Siyah" || secim == "siyah" || secim == "SİYAH")
    {
        secim = "siyah";
    }
    else if (secim == "Yeşil" || secim == "yeşil" || secim == "YEŞİL")
    {
        secim = "yesil";
    }
    else
    {
        Console.WriteLine("Geçersiz seçim! Lütfen Kırmızı, Siyah veya Yeşil yazınız.");
        return;
    }
    
    string[] toplar = new string[kirmiziTop + siyahTop + yesilTop];
    
    toplar[0] = "kirmizi"; toplar[1] = "kirmizi"; toplar[2] = "kirmizi";
    toplar[3] = "kirmizi"; toplar[4] = "kirmizi"; toplar[5] = "kirmizi";
    toplar[6] = "kirmizi"; toplar[7] = "kirmizi"; toplar[8] = "kirmizi";
    toplar[9] = "kirmizi"; toplar[10] = "kirmizi"; toplar[11] = "kirmizi";
    toplar[12] = "kirmizi"; toplar[13] = "kirmizi"; toplar[14] = "kirmizi";
    toplar[15] = "kirmizi"; toplar[16] = "kirmizi"; toplar[17] = "kirmizi";
    
    toplar[18] = "siyah"; toplar[19] = "siyah"; toplar[20] = "siyah";
    toplar[21] = "siyah"; toplar[22] = "siyah"; toplar[23] = "siyah";
    toplar[24] = "siyah"; toplar[25] = "siyah"; toplar[26] = "siyah";
    toplar[27] = "siyah"; toplar[28] = "siyah"; toplar[29] = "siyah";
    toplar[30] = "siyah"; toplar[31] = "siyah"; toplar[32] = "siyah";
    toplar[33] = "siyah"; toplar[34] = "siyah"; toplar[35] = "siyah";
    
    toplar[36] = "yesil"; toplar[37] = "yesil";
    
    Random random = new Random();
    string programSecimi = toplar[random.Next(toplar.Length)];
    
    if (secim == programSecimi)
    {
        Console.WriteLine("Kazandınız!");
    }
    else
    {
        Console.WriteLine("Kaybettiniz!");





8- Kullanıcıya iki seçenecek yönlendirin
1-Rastgele sayı oluştur
2-Çıkış.
Kullanıcı her bir değeri girdiğinde rastgele sayı oluşturun(her oluşturulan sayı toplanacak) eğer
2 değerini girerse oluşturulan rastgele sayıların toplamını ekrana yazdırın(sayı aralığını istediğiniz 
şekilde ayarlayabilirsiniz)



    Random random = new Random();
    int toplam = 0;
    
    while (true)
    {
        Console.WriteLine("1 - Rastgele sayı oluştur");
        Console.WriteLine("2 - Çıkış");
        Console.Write("Seçiminizi yapın: ");
        string secim = Console.ReadLine();
    
        if (secim == "1")
        {
            int rastgeleSayi = random.Next(1, 101); 
            toplam += rastgeleSayi;
            Console.WriteLine($"Oluşturulan rastgele sayı: {rastgeleSayi}");
        }
        else if (secim == "2")
        {
            Console.WriteLine($"Toplam oluşturulan sayıların toplamı: {toplam}");
            break; 
        }
        else
        {
            Console.WriteLine("Geçersiz seçim! Lütfen 1 veya 2 girin.");
        }
