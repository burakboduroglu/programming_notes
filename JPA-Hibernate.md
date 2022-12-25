## 📃 JPA Hibernate Annotations

#### @Entity :

- This annotation is used to mark a class as an entity class.
- This annotation is used to create a table in the database.

```Java
@Entity
public class Brand {
}
```

---

#### @Table :

- @Table annotation is used to specify the details of the table that will be created in the database.
- The name attribute of the @Table annotation is used to specify the name of the table.

```Java
@Entity
@Table(name = "brands")
public class Brand {
}
```

---

#### @Column :

- @Column annotation is used to specify the details of the column that will be created in the database.
- The name attribute of the @Column annotation is used to specify the name of the column.

```Java


@Entity
@Table(name = "brands")
public class Brand {

    @Column(name = "brandName")
    private String brandName;
}
```

---

#### @Id :

- @Id annotation is used to specify the primary key of an entity.
- The @Id annotation is always used with the @GeneratedValue annotation.

```Java
@Entity
@Table(name = "brands")
public class Brand {
    @Id
    @Column(name = "id")
    private int id;

}
```

---

#### @ManyToOne :

- @ManyToOne annotation is used to specify many to one relationship with another entity.

```Java
@Entity
@Table(name = "brands")
public class Brand {
    @ManyToOne
    @JoinColumn(name = "brandsDetails")
    private BrandDetail brandDetail;
}
```

---

#### @OneToMany :

- @OneToMany annotation is used to specify one to many relationship with another entity.
- The mappedBy attribute of the @OneToMany annotation is used to specify the property of the entity that is the owner of the relationship.

```Java
@Entity
@Table(name = "brands")
public class Brand {

    @OneToMany(mappedBy = "brands", fetch = FetchType.EAGER)
    private BrandDetail brandDetail;
}
```

---

#### @PrimaryKeyJoinColumn :

- @PrimaryKeyJoinColumn annotation is used to specify the primary key of the entity that is the owner of the relationship.

```Java
@Entity
@Table(name = "brands")
public class Brand {

    @PrimaryKeyJoinColumn
    private int id;
}
```

---

#### @JoinColumn :

- @JoinColumn annotation is used to specify the column that will be created in the database as a foreign key.

```Java
@Entity
@Table(name = "brands")
public class Brand {

    @JoinColumn(name = "brandDetail")
    private BrandDetail brandDetail;
}
```

---

#### @JoinTable ve @MapsId:

- It is used to specify the join table that will be created in the database.
- @JoinTable annotation is used to specify the join table that will be created in the database.
- @MapsId annotation is used to specify the primary key of the entity that is the owner of the relationship.

```Java
@Entity
@Table(name = "brands")
public class Brand {

    @JoinTable(name = "brands")
    private BrandDetail brandDetail;
}
```

---

#### @OneToOne:

- @OneToOne annotation is used to specify one to one relationship with another entity.
- The mappedBy attribute of the @OneToOne annotation is used to specify the property of the entity that is the owner of the relationship.

```Java
@Entity
@Table(name = "brands")
public class Brand {

    @OneToOne(mappedBy = "brands")
    private BrandDetail brandDetail;
}
```

---

✅ If you like this article, you can give me a star on. 😎
Thanks for reading. 🙏
