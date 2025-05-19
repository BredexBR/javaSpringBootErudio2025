# Annotations

No Spring Boot, as _annotations_ (anotações) são utilizadas para configurar e controlar o comportamento dos componentes da aplicação. Abaixo estão algumas das mais comuns e utilizadas neste projeto:

## 🎯 Controladores e Rotas

- **@RestController**  
  Indica que a classe é um controlador REST. Combina o comportamento de `@Controller` e `@ResponseBody`, permitindo o retorno direto de objetos Java que serão serializados em JSON.

- **@RequestMapping**  
  Define a rota base ou específica para um método ou classe. Pode ser usada com métodos `GET`, `POST`, `PUT`, `DELETE`, entre outros.

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
