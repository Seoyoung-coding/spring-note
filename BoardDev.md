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
