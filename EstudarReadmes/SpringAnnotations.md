# Annotations

No Spring Boot, as _annotations_ (anotações) são utilizadas para configurar e controlar o comportamento dos componentes da aplicação. Abaixo estão algumas das mais comuns e utilizadas neste projeto:

## 🎯 Controladores e Rotas

- **@RestController**  
  Indica que a classe é um controlador REST. Combina o comportamento de `@Controller` e `@ResponseBody`, permitindo o retorno direto de objetos Java que serão serializados em JSON.

- **@RequestMapping**  
  Define a rota base ou específica para um método ou classe. Pode ser usada com métodos `GET`, `POST`, `PUT`, `DELETE`, entre outros.

- **@RequestMapping**  
  Define a rota base ou específica para um método ou classe. Pode ser usada com métodos `GET`, `POST`, `PUT`, `DELETE`, entre outros.

- **@GetMapping**
  Especialização de `@RequestMapping` para requisições HTTP do tipo `GET`. Usada para obter dados (ex: buscar todos os usuários).

- **@PostMapping**  
  Especialização de `@RequestMapping` para requisições HTTP do tipo `POST`. Usada para criar novos recursos (ex: cadastrar um novo usuário).

- **@PutMapping**
  Especialização de `@RequestMapping` para requisições HTTP do tipo `PUT`. Usada para atualizar recursos existentes.

- **@PathVariable**  
  Indica que o valor de um parâmetro de método será extraído de uma parte da URL. Muito usado para capturar IDs, por exemplo: `/person/{id}`.

- **@RequestBody**  
  Informa ao Spring que o corpo da requisição HTTP deve ser convertido em um objeto Java. É usado principalmente em requisições `POST` e `PUT`.

## 🧩 Injeção de Dependência

- **@Autowired**  
  Permite que o Spring resolva e injete automaticamente a dependência de um componente. Ou seja, quando você precisa usar um serviço ou repositório dentro de uma classe, o `@Autowired` cuida de instanciar e fornecer esse objeto.

## ⚙️ Componentes e Serviços

- **@Service**  
  Indica que a classe é um serviço de negócio e será gerenciada pelo Spring como um _bean_. Essa anotação ajuda a organizar a lógica de negócio da aplicação, separando-a dos controladores e repositórios.

## 📦 Persistência e JPA

- **@Entity**  
  Indica que a classe é uma entidade JPA, ou seja, será mapeada para uma tabela no banco de dados.

- **@Table**  
  Especifica o nome da tabela no banco de dados correspondente à entidade. Se não for usada, o nome da tabela será igual ao nome da classe.

- **@Id**  
  Marca o campo que será usado como chave primária da entidade.

- **@GeneratedValue**  
  Define a estratégia de geração automática de valores para a chave primária (`@Id`), como `AUTO`, `IDENTITY`, `SEQUENCE`, etc.

- **@Column**  
  Permite configurar detalhes da coluna no banco de dados, como nome, tamanho, se pode ser `null`, entre outros.

## 🔧 Java Comum

- **@Override**
  Indica que um método sobrescreve um método da superclasse ou implementa um método de uma interface. Ajuda a evitar erros de digitação e melhora a legibilidade do código.

## 🧾 Serialização JSON (Jackson)

- **@JsonFilter**  
  Permite definir filtros dinâmicos de propriedades que devem ser incluídas ou excluídas durante a serialização. Requer configuração adicional no `ObjectMapper`.

- **@JsonProperty**  
  Define o nome da propriedade no JSON. Útil para mapear nomes diferentes entre os atributos Java e o JSON, ou para garantir a ordem de serialização.

- **@JsonInclude**  
  Controla quais propriedades devem ser incluídas na serialização. Por exemplo, pode ser usado para ignorar valores `null` ou vazios:

  ```java
  @JsonInclude(JsonInclude.Include.NON_NULL)
  ```

- **@JsonFormat**  
  Define o formato de datas, números ou outros valores durante a serialização. Exemplo para datas:

  ```java
  @JsonFormat(pattern = "dd/MM/yyyy")
  private LocalDate nascimento;
  ```

- **@JsonIgnore**  
  Indica que a propriedade não deve ser incluída na serialização ou desserialização JSON.

- **@JsonSerialize**  
  Permite especificar uma classe customizada de serialização. É útil quando se quer controlar exatamente como um valor será convertido para JSON.

## 🧪 Testes Unitários (JUnit 5 e Mockito)

- **@TestInstance**  
  Define o ciclo de vida da instância de teste. Com `TestInstance.Lifecycle.PER_CLASS`, o JUnit cria apenas uma instância da classe de teste, permitindo o uso de métodos não estáticos com `@BeforeAll`.

- **@ExtendWith**  
  Usado para estender o comportamento do JUnit 5, como habilitar o suporte ao Mockito com `@ExtendWith(MockitoExtension.class)`.

- **@InjectMocks**  
  Cria uma instância da classe e injeta os objetos anotados com `@Mock` nela. Usado para testar a classe com suas dependências simuladas.

- **@Mock**  
  Cria objetos mock (falsos) que simulam o comportamento de dependências externas.

- **@BeforeEach**  
  Define um método que será executado antes de cada método de teste. Ideal para inicializar variáveis ou configurar mocks.

- **@Test**  
  Indica que o método é um teste e deve ser executado pelo JUnit.
