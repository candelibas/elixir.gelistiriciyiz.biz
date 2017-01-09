---
title: "Fonksiyonlar"
date: Jan 09, 2017 15:35
published: true
author:
  name: Ender Ahmet Yurt
  email: enderyurt@gmail.com
  link: http://enderahmetyurt.com
  bio: Full Stack Developer
  twitter: ndrx42
---

Merhaba.

Elixir, fonksiyonel bir programla dili olduğu için giriş kısmından sonra fonksiyonları anlamak daha iyi olur diye düşünüyorum. Dilin temel özelliklerine zaten konular detaylandıkça tek tek değinme fırsatımız olacak. Ben Elixir öğrenmeye kitap olarak O'Reilly'ın Introducing Elixir kitabı ile başladım ve içerik olarak o kitabı izleyeceğim.

###FN

Elixir okunabilirliği kolay bir dil olduğu için (Ruby gibi ;)) fonksiyon yaratmak ve içinde işlem yapmak çok kolay. ```fn``` keyword'ü ile anonim fonksiyon yaratabiliyoruz. Fahrenheit olarak verilen bir sıcaklık değerini santigrata çeviren bir fonksiyonu önce IEX yani Elixir konsolundan yazalım.

```elixir
$ iex
Erlang/OTP 19 [erts-8.1] [source] [64-bit] [smp:4:4] [async-threads:10] [hipe] [kernel-poll:false] [dtrace]

Interactive Elixir (1.3.4) - press Ctrl+C to exit (type h() ENTER for help)
iex(1)> convert_fah_to_cel = fn(temperature) -> (temperature - 32) * 5 / 9 end
#Function<6.52032458/1 in :erl_eval.expr/5>
```

Biraz fonksiyonu anlamaya çalışalım. ```convert_fah_to_cel``` yazarak anonim fonksiyonumuzu bir değere atıyoruz. Sonrasında ```fn() ->``` ile artık anonim fonksiyonumuzu yazmaya başlıyoruz. Bizim fonksiyonumuza bir parametre geçirmek istiyoruz bu yüzden parantez içinde parametreyi veriyoruz fakat bunu parantez olmadan da yapabiliriz. Sonrasında fonksiyon ne iş yapacaksa yazıyoruz ve ```end``` ile fonksiyonu sonlandırıyoruz. Elixir bize bir çıktı veriyor bu çıktının anlamı fonksiyonu yarattım ve bir değerli fonksiyon olarak yorumlayabiliriz şimdilik.

Şimdi bu fonksiyonu kullanmaya geldi sıra. Anonim bir fonksiyon yarattığımız için Elixir'de ```.()``` şeklinde çağrılır.

```elixir
iex(2)> convert_fah_to_cel.(100)
37.77777777777778
iex(3)>
```

İstersek bu fonksiyonu daha düzenli bir şekilde de yazabiliriz.

```elixir
iex(3)> convert_fah_to_cel_2 = fn(temperature)
...(3)> -> (temperature - 32) * 5 / 9
...(3)> end
#Function<6.52032458/1 in :erl_eval.expr/5>
```

Tekrar fonksiyonu çağırırsak.

```elixir
iex(4)> convert_fah_to_cel_2.(100)
37.77777777777778
iex(5)>
```

şeklinde olacaktır.

Bütün bu anlattıklarım aslında Ruby'deki ```lambda``` anımsatıyor. Elixir'de Ruby'de de olduğu gibi ```fn``` ile closure'lar yaratıp, kullanabiliriz.

###&

Anonim fonksiyonları kısa yoldan da kullanabiliriz. Bunu parametre atarken kullanacağız. Önceki örneği ```&``` ile yapalım.

```elixir
iex(5)> convert_fah_to_cel = &((&1 - 32) * 5 / 9)
#Function<6.52032458/1 in :erl_eval.expr/5>
iex(6)> convert_fah_to_cel.(100)
37.77777777777778
```

```fn``` ve parametre isimlerini ```&``` ile yer değiştirdik. Her parametre için ise ```&``` kullanıyoruz.

```elixir
iex(7)> sum = &(&1+&2)
&:erlang.+/2
iex(8)> sum.(5)
8
```

Anonim fonksiyonları basit yoldan öğrendik. Modüller ve fonksiyonlara geçtikçe işleri biraz daha karmaşıklaştıracağız. Şimdilik bu kadar.

Sevgiler.