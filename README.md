# tobeto_app
Scaffold: Uygulamanızın temel yapısını oluşturmak için bir Scaffold widget'ı kullanabilirsiniz. Scaffold, app bar, body ve floating action button gibi standart app layout özelliklerini sağlar.

Gradient Background: Arkaplan için, görseldeki gibi bir degrade efekti uygulamak için Container widget'ını BoxDecoration ve LinearGradient veya RadialGradient ile birlikte kullanabilirsiniz.

Custom Shapes and Shadows: Görseldeki gibi bir kartvizit efekti oluşturmak için, Card veya Container widget'ını BoxDecoration ile özelleştirebilirsiniz. Kenarları yuvarlak ve gölge efektleri için borderRadius ve boxShadow özelliklerini kullanabilirsiniz.

TextFormField: Kullanıcı kodu ve parola girişi için TextFormField widget'ları kullanılabilir. İkonlar ve içerik dolgusu (contentPadding) gibi özelleştirmelerle kullanıcı dostu bir giriş alanı sağlayabilirsiniz.

Button: Giriş yapma butonu için ElevatedButton veya FlatButton gibi widget'ları kullanabilirsiniz. Görseldeki gibi özel bir şekil ve renk için style özelliğini özelleştirmeniz gerekecek.

Text Styling: "Parolamı Unuttum" gibi metinler için Text widget'ını kullanarak, TextStyle ile metin stilini özelleştirebilirsiniz.

Form and Validation: Formların doğru kullanılması ve girişlerin doğrulanması için Form widget'ı içinde TextFormField widget'larını gruplayabilir ve gerekli validasyonları ekleyebilirsiniz.

Responsive Design: Farklı ekran boyutları ve oranları için uygulamanızın duyarlı olmasını sağlamak amacıyla, MediaQuery kullanarak boyut ve padding değerlerini ayarlayabilirsiniz.

State Management: Kullanıcı giriş durumunu yönetmek için, sağlayıcı (Provider), setState, StreamBuilder, veya başka bir state management çözümü kullanmanız gerekebilir.


Container(
  width: 200.0, // Konteyner genişliği
  height: 100.0, // Konteyner yüksekliği
  decoration: BoxDecoration(
    color: Colors.blue, // Arka plan rengi
    borderRadius: BorderRadius.circular(10.0), // Kenar yuvarlaklığı
    boxShadow: [ // Gölge efekti
      BoxShadow(
        color: Colors.black.withOpacity(0.15), // Gölge rengi
        spreadRadius: 4.0, // Gölgenin yayılma yarıçapı
        blurRadius: 10.0, // Gölgenin bulanıklık yarıçapı
        offset: Offset(0, 4), // Gölgenin yatay ve dikey pozisyonu
      ),
    ],
    gradient: LinearGradient( // Degrade renk geçişi
      begin: Alignment.topLeft, // Gradient başlangıç noktası
      end: Alignment.bottomRight, // Gradient bitiş noktası
      colors: [Colors.blue, Colors.purple], // Gradient renkleri
    ),
    border: Border.all( // Kenarlık
      color: Colors.white, // Kenarlık rengi
      width: 2.0, // Kenarlık genişliği
    ),
    image: DecorationImage( // Arka plan resmi
      image: NetworkImage('https://example.com/image.jpg'), // Resim URL'si
      fit: BoxFit.cover, // Resmin konteyneri nasıl kaplayacağı
    ),
  ),
  child: Center( // Konteyner içindeki çocuk widget
    child: Text(
      'Merhaba Flutter!', 
      style: TextStyle(color: Colors.white), // Text stil özellikleri
    ),
  ),
)

Container(
  width: double.infinity, // ya da belirli bir genişlik
  height: double.infinity, // ya da belirli bir yükseklik
  decoration: BoxDecoration(
    image: DecorationImage(
      image: AssetImage('assets/images/resminiz.jpg'),
      fit: BoxFit.cover, // resmin konteyner içinde nasıl yerleşeceğini ayarlar
    ),
    // Diğer dekorasyon özellikleri
  ),

