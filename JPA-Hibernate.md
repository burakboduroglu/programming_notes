## 📃 JPA Hibernate Annotations

#### @Entity :
- Sınıf bir varlık olduğunu belirtir.

```Java
import javax.persistence.Entity;

@Entity
public class Brand {
}
```

#### @Table :
- Bu varlığın eşlendiği veritabanındaki tablosunu belirtir.
- @Table notasyonun name niteliği, tablo adını belirtmek için kullanılır.

```Java
import javax.persistence.Entity;
import javax.persistence.Table;

@Entity
@Table(name = "brands")
public class Brand {
}
```

#### @Column :
- @Column açıklamasını kullanarak sütun eşlemesi belirtilir.
- Bu notasyonun name niteliği, tablonun sütun adını belirtmek için kullanılır.

```Java
import javax.persistence.Column;
import javax.persistence.Entity;
import javax.persistence.Table;

@Entity
@Table(name = "brands")
public class Brand {

    @Column(name = "brandName")
    private String brandName;
}
```

#### @Id :
- @Id anotasyonu eninty sınıfında "primary key" belirlemek için kullanılır.

```Java
import javax.persistence.Column;
import javax.persistence.Entity;
import javax.persistence.Table;

@Entity
@Table(name = "brands")
public class Brand {
    @Id
    @Column(name = "id")
    private int id;
  
}
```

#### @ManyToOne :
- @ManyToOne birçok marka ("brands") aynı marka detayını paylaşabilir. Yani, markadan markaya marka detayı, çoktan bire bir ilişkidir. @ManyToOne ek açıklaması aynı şekilde kullanılabilir.

```Java
@Entity
@Table(name = "brands")
public class Brand {
    @ManyToOne
    @JoinColumn(name = "brandsDetails")
    private BrandDetail brandDetail;
}
```

#### @OneToMany :
- @OneToMany Markadan marka detayına bire çok ilişki olacaktır. Bu ilişkinin sahibi marka detayıdır. Bu nedenle, iki yönlü ilişki yapmak için Markada 'mappedBy' özelliğini kullanacağız.

```Java
@Entity
@Table(name = "brands")
public class Brand {

    @OneToMany(mappedBy = "brands", fetch = FetchType.EAGER)
    private BrandDetail brandDetail;
}
```
#### @PrimaryKeyJoinColumn :
- @PrimaryKeyJoinColumn aynı birincil anahtarı paylaşan varlıkları ilişkilendirmek için kullanılır.

#### @JoinColumn :
- @JoinColumn foreign key varlıklardan biri tarafından tutulduğunda bire bir veya çoktan bire ilişkilendirmeler için kullanılır.

#### @JoinTable ve @MapsId: 
- Bir ilişkilendirme tablosu aracılığıyla bağlanan varlıklar için @JoinTable ve mappedBy kullanılmalıdır. 
- @MapsId: Paylaşılan anahtara sahip iki varlık, @MapsId ek açıklaması kullanılarak kalıcı hale getirilebilir.

````
@OneToOne
@MapsId
@JoinColumn(name = "generalDetail")
private Brand brand;
````

#### @OneToOne:
- @OneToOne Marka ve Marka Ayrıntısı varlıkları aynı birincil anahtarı paylaşır ve bunları @OneToOne ve @PrimaryKeyJoinColumn kullanarak ilişkilendirebiliriz. Bu durumda Marka Detayı id özelliğine @GeneratedValue ile açıklama eklenmez. Marka Detayının kimliği için Marka'nın id değeri kullanılacaktır.

````Java
@Entity
@Table(name = "brands")
public class Brand {
   
  @Id
  @Column(name = "id")
  @GeneratedValue
  private int id;
   
  @OneToOne(cascade = CascadeType.MERGE)
  @PrimaryKeyJoinColumn
  private BrandDetail brandDetail;
}
 
@Entity
@Table(name = "brandDetails")
public class BrandDetail {
 
  @Id
  @Column(name = "id")
  private int id;
}
```` 
⚠️ Dikkat edilecek noktalar:
- @PrimaryKeyJoinColumn, aynı birincil anahtarı paylaşan ilişkili varlıklar için kullanılmalıdır.
- @JoinColumn & @OneToOne, foreign key varlıklardan biri tarafından tutulduğunda, öznitelikle eşlenmelidir.
#### @OneToOne :
- Marka ve Marka Ayrıntısı bir foreign key aracılığıyla bağlanır, bu nedenle @OneToOne ve @JoinColumn ek açıklamaları kullanılabilir. Aşağıda belirtilen snippet'te Marka için oluşturulan id, Marka Detayı tablosunun 'brandId' sütununa eşlenecektir. @MapsId aynı şey için kullanılır.
````Java
@Entity
@Table(name = "brandDetails")
public class BrandDetail {
  @Id
  @Column(name = "id")
  @GeneratedValue
  private int id;
   
  @OneToOne
  @MapsId
  @JoinColumn(name = "brandId")
  private Brand brand;
}
 
@Entity
@Table(name = "brands")
public class Communication {
 
  @Id
  @Column(name = "ID")
  @GeneratedValue
  private Integer id;
 
  @OneToOne(mappedBy = "brand", cascade = CascadeType.ALL)
  private BrandDetail brandDetail;
}
````
✅ Beğenirseniz yıldızlamayı unutmayın. 😎
