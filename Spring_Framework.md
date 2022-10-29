## 🌱 Spring Annotations

#### @Repository : 
- Sınıf düzeyinde bir açıklamadır. 
- Depo veritabanına erişen bir DAO'dur.
- Depo veritabanı ile ilgili tüm işlemleri yapar.

```java
@Repository
public class TestRepo{
   public void add(){
      System.out.println("Added");
   }
}
```
#### @Service :
- Sınıf düzeyinde kullanılır.
- Spring'e sınıfın iş mantığını söyler.

```java
@Service
public class TestService{
   public void service1(){
      //business code (iş kodları)
   }
}
```

#### @Controller :
- Sınıf düzeyinde bir açıklamadır.
- Bir sınıfı web istek işleyicisi olarak işaretler.
- Genellikle Web sayfalarını sunmak için kullanılır.
- Çoğunlukla @RequestMapping açıklaması ile kullanılır.

```java
@Controller  
@RequestMapping("/api/brands")  
public class BrandsController{
   @GetMapping(/getall)  
   public Employee getAll(){  
       return brandService.getAll(); 
   }  
}  
```

#### @RequestMapping :
- Web isteklerini eşleştirmek için kullanılır.

```java
@Controller  
@RequestMapping("/api/brands")  
public class BrandsController{
   @GetMapping(/getall)  
   public Employee getAll(){  
       return brandService.getAll(); 
   }  
}  
```

#### @GetMapping :
- Belirli işleyici yöntemiyle HTTP GET isteklerini işler.
- Veri listelemek veya görüntülemek için kullanılır.
- @RequestMapping(method = RequestMethod.GET) yerine kullanılır.

#### @PostMapping :
- Belirli işleyici yöntemiyle HTTP POST isteklerini işler.
- Veri eklemek için kullanılır.
- @RequestMapping(method = RequestMethod.POST) yerine kullanılır.

#### @PutMapping :
- Belirli işleyici yöntemiyle HTTP PUT isteklerini işler.
- Veriyi güncellemek için kullanılır.
- @RequestMapping(method = RequestMethod.PUT) yerine kullanılır.

#### @DeleteMapping :
- Belirli işleyici yöntemiyle HTTP DELETE isteklerini işler.
- Veriyi silmek için kullanılır.
- @RequestMapping(method = RequestMethod.DELETE) yerine kullanılır.
- 
#### @PathVariable :
- URL'den değerleri çıkarmak için kullanılır.
- URL'nin bir yol değişkeni içerdiği RESTful web hizmeti için en uygundur.
- Bir metotta birden fazla @PathVariable tanımlayabiliriz.


#### @RequestBody:
- Bir yöntem parametresindeki bir nesneyle HTTP isteğini bağlamak için kullanılır.

#### @RequestParam:
- URL'den sorgu parametrelerini çıkarmak için kullanılır. 
- Sorgu parametresi olarak da bilinir.

#### @RestController:
- @Controller ve @ResponseBody ek açıklamalarının bir kombinasyonu olarak düşünülebilir. 
- @RestController ek açıklamasının kendisi @ResponseBody ek açıklamasıyla açıklanmıştır. 
- @ResponseBody ile her yönteme açıklama ekleme ihtiyacını ortadan kaldırır.

#### Örnek proje için "Kodlama.ioHM" repository'i içinde "Java-Camp-2022" ziyaret edebilirsiniz veya aşağıda bulunan linki kullanarak erişebilirsiniz.
#### -> [Java-Camp-2022](https://github.com/BurakBoduroglu/Kodlama.ioHM/tree/main/Java-Camp-2022) <-


