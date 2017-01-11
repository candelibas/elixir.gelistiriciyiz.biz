---
title: "Kurulum ve İlk Program"
date: Jan 05, 2017 00:14
tags: setup,iex
cover: introducing-elixir-cover.png
published: true
author:
  name: Ender Ahmet Yurt
  email: enderyurt@gmail.com
  link: http://enderahmetyurt.com
  bio: Full Stack Developer
  twitter: ndrx42
---

Merhaba.

Uzun bir Ruby macerasından sonra kendimi başka bir programlama diline atmak 
istiyordum. Aslında programla dilinden ziyade isteğim daha farklı bir disiplini 
barındıran bir dil olmasaydı. READ_MOREDaha önceden de merak edip baktığım ama aklım o günlerde pek çalışmadığı için anlayamadığım, sıkıldığım programlama dili **Elixir**'e bugünlerde tekrardan başladım. Bu site üzerinden sizle maceramı paylaşacağım. Umarım herkes için faydalı olur. Hadi yola koyulalım.

###Elixir

Fonksiyonel bir dil olan ve Erlang VM'i üzerinde çalışan Elixir, sytanx'i ile kolay okunabilirlik sağlıyor.

###Kısa bir kurulum

Kişisel olarak kurulumlardan ve bir şeylerin setup'ını yapmaktan nefret ediyorum. Hele hele hata alıp, onu çözmek ile uğraşmak beni deli ediyor resmen. Elixir, bu konuda pek sıkıntı değil şükür ki. En güzel yanı çok hızlı bir şekilde kurulması (macOS için konuşuyorum) ve development sürecine sizi hemen geçirmesi.

Burada kurulum olarak macOS işletim sistemini vereceğim. Başka bir işletim sistemi kullanıyorsunuz [http://elixir-lang.org/install.html](http://elixir-lang.org/install.html) yardım alabilirsiniz.

Her güzel paket gibi Elixir de Homebrew veya Macport üzerinden hızlıca kurulabiliyor.

Homebrew için önce bir update geçiyoruz.

```
$ brew update
```

Sonrasında ise Elixir'i indiriyor ve kuruyoruz.

```
$ brew install elixir
```

Macports ile ise direk indirip, kurulum yapabiliriz.

```
$ sudo port install elixir
```

###Komut Satırı

Elixir'de diğer diller gibi bir komut satırına sahip. ```iex``` yazıp Elixir terminal'i açabiliriz.

```elixir
$ iex
Erlang/OTP 19 [erts-8.1] [source] [64-bit] [smp:4:4] [async-threads:10] [hipe] [kernel-poll:false] [dtrace]

Interactive Elixir (1.3.4) - press Ctrl+C to exit (type h() ENTER for help)
iex(1)>
```

Burada istediğimiz her türlü işlemi yapabiliriz.

```elixir
iex(1)> 1+1
2
iex(2)>
```

İstediğimiz fonksiyonları çağırabiliriz.

```elixir
iex(2)> div(100,20)
5
iex(3)> rem(100,20)
0
iex(4)>
```


###İlk Program

Basitçe bir script yazarak Elixir'e ilk adımı atabiliriz. Bundan sonraki yazılarda büyük ihtimal Elixir'in nasıl derlendiğinden ve bahsedeceğiz.

Elixir scriptlerinin uzantası ```exs``` oluyor ve console'dan ```elixir``` komutu ile çağrılıyor.

```elixir
# hello_world.exs
IO.puts "Hello world"
```

```
$ elixir hello_world.exs
Hello world
```

İlk yazı biraz kolay gelmiş olabilir ancak asıl olay bundan sonra başlıyor. Biraz dinlenip devam etmekte yarar var.

Sevgiler.

_**Note:** Ruby'i hala profesyonel olarak kullanıyorum. Bıraktığım falan yok. Çünkü ilk aşklar unutulmaz. <3_