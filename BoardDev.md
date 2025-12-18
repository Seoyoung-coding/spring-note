## Annotation
@Table("board")
@Id (id 필드)
@Data, @NoArgsConstructor, @AllArgsConstructor

## 1. 도메인 작성
### 1.1 필드 작성
```
public class BoardDomain {
    @Id
    private Long id;
    private String name;
    private String title;
    private String content;
    private String password;
    LocalDateTime createTime;
    LocalDateTime updatedAt;
}
```

### 1.2 비지니스 메소드 작성 
`this` 는 객체 자기 자신 - 지금 이 대상 자기 자신”을 가리키는 말이다.
해결: 앞에 붙은 **this**는 "이 객체(일기장)의 진짜 주인"을 뜻합니다.
의미: "밖에서 가져온 content를, 이 일기장의 content 칸에 집어넣어라!"라는 명령입니다.

생성자(Constructor)
이 코드는 **"새로운 일기장(객체)을 딱 펼쳤을 때, 첫 페이지에 내용을 적고 날짜 도장을 쾅 찍어주는 과정"**이라고 생각하면 됩니다.

```
public Devlog(String content) {
    this.content = content;
    this.createdAt = LocalDateTime.now();
}
```


