# 📚 GUIA COMPLETO DE BOAS PRÁTICAS - BANCO DE CONHECIMENTO

**Versão:** 2.0 - Guia de Referência Definitivo
**Data:** 13 de Novembro de 2025
**Propósito:** Guia completo para consulta sobre como aplicar SOLID, Clean Architecture, Arquiteturas de Software, DDD, Design Patterns e GRASP

> 🎯 **Este documento é seu banco de conhecimento**
>
> Consulte sempre que tiver dúvidas sobre:
> - Como aplicar um princípio SOLID corretamente
> - Quando usar um Design Pattern específico
> - Como estruturar código seguindo Clean Architecture
> - Qual arquitetura escolher (Monolito Modular vs Microsserviços)
> - Como implementar DDD na prática
> - Como aplicar GRASP para atribuir responsabilidades
>
> **Foco:** Otimização, eficiência e perfeição no código

---

## 📖 ÍNDICE DETALHADO

### 🏗️ FUNDAMENTOS
1. [Introdução ao Guia](#-introdução-ao-guia)
2. [Como Usar Este Guia](#-como-usar-este-guia)
3. [Filosofia: Código Perfeito](#-filosofia-código-perfeito)

### 🎯 SOLID (Princípios)
4. [S - Single Responsibility Principle (SRP)](#-s---single-responsibility-principle-srp)
5. [O - Open/Closed Principle (OCP)](#-o---openclosed-principle-ocp)
6. [L - Liskov Substitution Principle (LSP)](#-l---liskov-substitution-principle-lsp)
7. [I - Interface Segregation Principle (ISP)](#-i---interface-segregation-principle-isp)
8. [D - Dependency Inversion Principle (DIP)](#-d---dependency-inversion-principle-dip)

### 🏛️ CLEAN ARCHITECTURE
9. [Clean Architecture - Visão Geral](#-clean-architecture---visão-geral)
10. [Camadas e Regra de Dependência](#-camadas-e-regra-de-dependência)
11. [Ports and Adapters (Hexagonal)](#-ports-and-adapters-hexagonal)

### 🏗️ ARQUITETURAS DE SOFTWARE
12. [Arquiteturas de Software - Visão Geral](#-arquiteturas-de-software---visão-geral)
13. [Monolito Modular por Domínio](#-monolito-modular-por-domínio)
14. [Microsserviços](#-microsserviços)
15. [Migração: Monolito → Microsserviços](#-migração-monolito--microsserviços)

### 🎨 DOMAIN-DRIVEN DESIGN (DDD)
16. [DDD - Visão Geral](#-ddd---visão-geral)
17. [Entidades Ricas vs Anêmicas](#-entidades-ricas-vs-anêmicas)
18. [Aggregate Root](#-aggregate-root)
19. [Value Objects](#-value-objects)
20. [Domain Services](#-domain-services)
21. [Invariantes](#-invariantes)
22. [Métodos de Domínio - Guia Completo](#-métodos-de-domínio---guia-completo)

### 🎭 DESIGN PATTERNS
23. [Design Patterns - Catálogo](#-design-patterns---catálogo)
24. [Repository Pattern](#-repository-pattern)
25. [Adapter Pattern](#-adapter-pattern)
26. [Facade Pattern](#-facade-pattern)
27. [Strategy Pattern](#-strategy-pattern)
28. [Specification Pattern](#-specification-pattern)
29. [CQRS Pattern](#-cqrs-pattern)
30. [Builder Pattern](#-builder-pattern)
31. [Factory Pattern](#-factory-pattern)

### 🎯 GRASP (Atribuição de Responsabilidade)
32. [GRASP - Visão Geral](#-grasp---visão-geral)
33. [Information Expert](#-information-expert)
34. [Creator](#-creator)
35. [Controller](#-controller)
36. [Low Coupling](#-low-coupling)
37. [High Cohesion](#-high-cohesion)

### 🏛️ PILARES DE POO
38. [Encapsulamento](#-encapsulamento)
39. [Abstração](#-abstração)
40. [Polimorfismo](#-polimorfismo)
41. [Herança](#-herança)

### ✅ VALIDAÇÃO E CHECKLIST
42. [Checklist de Código Perfeito](#-checklist-de-código-perfeito)
43. [Anti-Patterns a Evitar](#-anti-patterns-a-evitar)
44. [Referência Rápida](#-referência-rápida)

---

## 🎯 INTRODUÇÃO AO GUIA

### O QUE É ESTE GUIA?

Este é seu **banco de conhecimento completo** sobre as melhores práticas de desenvolvimento de software. Ele contém:

✅ **SOLID:** Os 5 princípios fundamentais de design OO
✅ **Clean Architecture:** Como estruturar aplicações mantíveis
✅ **Arquiteturas de Software:** Monolito Modular vs Microsserviços
✅ **DDD:** Domain-Driven Design na prática
✅ **Design Patterns:** Catálogo de padrões com exemplos
✅ **GRASP:** Princípios de atribuição de responsabilidade
✅ **POO:** Pilares da orientação a objetos

### PARA QUEM É ESTE GUIA?

- 🎓 Desenvolvedores que querem escrever código **perfeito**
- 🏆 Times que buscam **excelência técnica**
- 📚 Estudantes aprendendo **arquitetura de software**
- 🔍 Code reviewers buscando **referência de qualidade**

### O QUE VOCÊ VAI ENCONTRAR AQUI?

Cada tópico contém:

1. **O QUE É** - Definição clara do conceito
2. **POR QUE USAR** - Benefícios e motivação
3. **QUANDO USAR** - Situações apropriadas
4. **COMO APLICAR** - Passo a passo prático
5. **EXEMPLOS** - Código certo vs errado
6. **CHECKLIST** - Como validar aplicação correta
7. **ANTI-PATTERNS** - O que evitar

---

## 💡 COMO USAR ESTE GUIA

### 📖 MODO CONSULTA (Recomendado)

**Quando consultar:**
- ❓ "Como aplicar SRP nesta classe?"
- ❓ "Devo usar Strategy ou Specification aqui?"
- ❓ "Onde colocar esta lógica de negócio?"
- ❓ "Esta classe está violando algum princípio?"

**Como usar:**
1. Veja o **Índice** acima
2. Navegue até o tópico específico
3. Leia a seção **"COMO APLICAR"**
4. Veja os **EXEMPLOS**
5. Use o **CHECKLIST** para validar

### 📚 MODO ESTUDO

**Para aprendizado:**
1. Leia seção por seção sequencialmente
2. Pratique cada exemplo
3. Implemente no seu código
4. Use o checklist para validar

### 🔍 MODO REVISÃO DE CÓDIGO

**Durante code review:**
1. Use a [Referência Rápida](#-referência-rápida)
2. Verifique cada princípio SOLID
3. Valide estrutura Clean Architecture
4. Confirme padrões DDD

---

## 🎯 FILOSOFIA: CÓDIGO PERFEITO

### O QUE É CÓDIGO PERFEITO?

Código perfeito é aquele que:

✅ **É fácil de entender** - Qualquer dev lê e entende rapidamente
✅ **É fácil de testar** - Testes simples e isolados
✅ **É fácil de modificar** - Mudanças não quebram outras partes
✅ **É fácil de estender** - Novas features sem modificar existente
✅ **Tem zero bugs** - Invariantes sempre mantidas
✅ **É performático** - Otimizado e eficiente
✅ **É autodocumentado** - Código expressa intenção claramente

### PRINCÍPIOS DE CÓDIGO PERFEITO

#### 1. **YAGNI (You Aren't Gonna Need It)**
❌ Não adicione funcionalidades que "pode precisar no futuro"
✅ Adicione apenas o necessário agora

#### 2. **KISS (Keep It Simple, Stupid)**
❌ Não complique desnecessariamente
✅ Solução simples é melhor que complexa

#### 3. **DRY (Don't Repeat Yourself)**
❌ Não duplique código ou lógica
✅ Centralize conhecimento em um lugar

#### 4. **Tell, Don't Ask**
❌ Não pergunte dados e faça algo com eles
✅ Diga ao objeto o que fazer

#### 5. **Composition Over Inheritance**
❌ Não use herança para tudo
✅ Prefira composição

---

## 🎯 S - SINGLE RESPONSIBILITY PRINCIPLE (SRP)

### 📖 O QUE É?

> **"Uma classe deve ter apenas uma razão para mudar"**
>
> Ou seja: **1 classe = 1 responsabilidade**

**Definição técnica:** Uma classe deve ter apenas um motivo para ser modificada. Se você consegue pensar em mais de um motivo para mudar uma classe, ela tem mais de uma responsabilidade.

### 💡 POR QUE USAR?

✅ **Facilita manutenção** - Mudanças em uma responsabilidade não afetam outras
✅ **Facilita testes** - Classes pequenas são mais fáceis de testar
✅ **Aumenta coesão** - Tudo na classe está relacionado
✅ **Reduz acoplamento** - Menos dependências
✅ **Melhora legibilidade** - Fácil entender o propósito da classe

### 📋 QUANDO USAR?

**SEMPRE!** SRP deve ser aplicado em **todas as classes**.

**Sinais de violação:**
- ❌ Classe com mais de 300 linhas
- ❌ Classe com nome vago (Manager, Helper, Util)
- ❌ Classe que faz várias coisas diferentes
- ❌ Muitos motivos para modificar a classe

### 🔧 COMO APLICAR?

#### PASSO 1: Identifique responsabilidades

Pergunte: **"O que esta classe faz?"**

Se a resposta tem **"E"**, viola SRP:
- ❌ "Valida usuário **E** envia email **E** salva no banco"
- ✅ "Valida usuário" (única responsabilidade)

#### PASSO 2: Separe responsabilidades

Crie uma classe para cada responsabilidade:

```java
// ❌ ERRADO: UserService faz TUDO (viola SRP)
@Service
public class UserService {
    // Responsabilidade 1: Validação
    public void validateUser(User user) { }

    // Responsabilidade 2: Persistência
    public void saveUser(User user) { }

    // Responsabilidade 3: Email
    public void sendWelcomeEmail(User user) { }

    // Responsabilidade 4: Autenticação
    public boolean authenticate(String username, String password) { }
}
```

```java
// ✅ CORRETO: 1 classe = 1 responsabilidade
@Service
public class UserValidator {
    public void validate(User user) { }
}

@Service
public class UserPersistenceService {
    public void save(User user) { }
}

@Service
public class WelcomeEmailService {
    public void send(User user) { }
}

@Service
public class AuthenticationService {
    public boolean authenticate(String username, String password) { }
}
```

#### PASSO 3: Use composição

```java
// Orquestre serviços especializados
@Service
public class CreateUserUseCase {
    private final UserValidator validator;
    private final UserPersistenceService persistence;
    private final WelcomeEmailService emailService;

    public void execute(User user) {
        validator.validate(user);
        persistence.save(user);
        emailService.send(user);
    }
}
```

### 📝 EXEMPLOS PRÁTICOS

#### Exemplo 1: Use Cases

```java
// ❌ ERRADO: PropertyService faz CRUD completo (múltiplas responsabilidades)
@Service
public class PropertyService {
    public Property create(PropertyDTO dto) { }
    public Property update(Long id, PropertyDTO dto) { }
    public void delete(Long id) { }
    public Property findById(Long id) { }
    public List<Property> findAll() { }
}
```

```java
// ✅ CORRETO: 1 Use Case = 1 operação
@Service
public class CreatePropertyUseCase {
    public Property execute(PropertyDTO dto) { }
}

@Service
public class UpdatePropertyUseCase {
    public Property execute(Long id, PropertyDTO dto) { }
}

@Service
public class DeletePropertyUseCase {
    public void execute(Long id) { }
}

@Service
public class FindPropertyUseCase {
    public Property findById(Long id) { }
    public List<Property> findAll() { }
}
```

#### Exemplo 2: Entidades

```java
// ❌ ERRADO: User faz validação, persistência e notificação
@Entity
public class User {
    private String email;

    // ❌ Responsabilidade 1: Validação
    public boolean isValid() {
        return email.contains("@");
    }

    // ❌ Responsabilidade 2: Persistência
    public void save() {
        repository.save(this);
    }

    // ❌ Responsabilidade 3: Notificação
    public void sendNotification() {
        emailService.send(this.email);
    }
}
```

```java
// ✅ CORRETO: User apenas mantém estado e comportamentos de domínio
@Entity
public class User {
    private String email;

    // ✅ Comportamento de domínio (pertence à entidade)
    public boolean hasValidEmail() {
        return email != null && email.contains("@");
    }

    // Persistência vai para Repository
    // Notificação vai para NotificationService
}
```

### ✅ CHECKLIST DE VALIDAÇÃO

Use estas perguntas para validar SRP:

- [ ] A classe tem apenas **UMA** responsabilidade clara?
- [ ] O nome da classe expressa **exatamente** o que ela faz?
- [ ] Existe apenas **UM** motivo para modificar esta classe?
- [ ] Todos os métodos estão relacionados à mesma responsabilidade?
- [ ] A classe tem menos de 300 linhas?
- [ ] A classe **NÃO** tem nomes genéricos (Manager, Helper, Util)?

### ❌ ANTI-PATTERNS

#### 1. God Class (Classe Deus)

```java
// ❌ Classe que faz TUDO
public class UserManager {
    public void validateUser() { }
    public void saveUser() { }
    public void deleteUser() { }
    public void sendEmail() { }
    public void authenticate() { }
    public void generateReport() { }
    public void exportToCSV() { }
    // ... 50+ métodos
}
```

**Solução:** Divida em classes especializadas

#### 2. Swiss Army Knife (Canivete Suíço)

```java
// ❌ Classe utilitária que faz várias coisas não relacionadas
public class Utils {
    public static String formatDate() { }
    public static boolean validateEmail() { }
    public static int calculateAge() { }
    public static void sendEmail() { }
}
```

**Solução:** Crie classes específicas (DateFormatter, EmailValidator, etc)

---

## 🎯 O - OPEN/CLOSED PRINCIPLE (OCP)

### 📖 O QUE É?

> **"Aberto para extensão, fechado para modificação"**
>
> Ou seja: **Adicione funcionalidades SEM modificar código existente**

**Definição técnica:** Classes devem ser projetadas de forma que novos comportamentos possam ser adicionados através de extensão (herança, implementação de interfaces), não modificando código existente.

### 💡 POR QUE USAR?

✅ **Reduz bugs** - Código existente não é tocado
✅ **Facilita testes** - Testes existentes continuam válidos
✅ **Aumenta confiabilidade** - Código testado não muda
✅ **Permite evolução** - Sistema cresce sem quebrar
✅ **Respeita dependências** - Não quebra código de clientes

### 📋 QUANDO USAR?

**Use quando:**
- ✅ Precisa adicionar novo comportamento
- ✅ Sistema precisa ser extensível
- ✅ Múltiplas variações de um comportamento

**Sinais de violação:**
- ❌ Modificar classe existente para adicionar feature
- ❌ Switches/ifs crescendo a cada nova variação
- ❌ Modificar testes existentes constantemente

### 🔧 COMO APLICAR?

#### Técnica 1: Abstração via Interfaces

```java
// ❌ ERRADO: Modifica classe para cada novo tipo
public class PaymentProcessor {
    public void processPayment(String type, BigDecimal amount) {
        if (type.equals("CREDIT_CARD")) {
            // processar cartão
        } else if (type.equals("PIX")) {
            // processar pix
        } else if (type.equals("BOLETO")) {
            // processar boleto
        }
        // ❌ Adicionar novo tipo = modificar esta classe
    }
}
```

```java
// ✅ CORRETO: Abstração permite extensão
public interface PaymentMethod {
    void process(BigDecimal amount);
}

@Component
public class CreditCardPayment implements PaymentMethod {
    public void process(BigDecimal amount) {
        // processar cartão
    }
}

@Component
public class PixPayment implements PaymentMethod {
    public void process(BigDecimal amount) {
        // processar pix
    }
}

// ✅ Adicionar novo tipo = criar nova classe (extensão, não modificação)
@Component
public class BoletoPayment implements PaymentMethod {
    public void process(BigDecimal amount) {
        // processar boleto
    }
}

// Uso
@Service
public class PaymentProcessor {
    private final Map<String, PaymentMethod> paymentMethods;

    public void processPayment(String type, BigDecimal amount) {
        paymentMethods.get(type).process(amount);
    }
}
```

#### Técnica 2: Strategy Pattern

```java
// ✅ CORRETO: Use Strategy para comportamentos variáveis
public interface DiscountStrategy {
    BigDecimal calculate(BigDecimal price);
}

@Component
public class NoDiscount implements DiscountStrategy {
    public BigDecimal calculate(BigDecimal price) {
        return price;
    }
}

@Component
public class SeasonalDiscount implements DiscountStrategy {
    public BigDecimal calculate(BigDecimal price) {
        return price.multiply(new BigDecimal("0.9")); // 10% off
    }
}

// Adicionar nova estratégia = criar nova classe (OCP)
@Component
public class VIPDiscount implements DiscountStrategy {
    public BigDecimal calculate(BigDecimal price) {
        return price.multiply(new BigDecimal("0.8")); // 20% off
    }
}
```

### 📝 EXEMPLOS PRÁTICOS

#### Exemplo 1: Validadores

```java
// ❌ ERRADO: Adicionar validação = modificar classe
public class UserValidator {
    public void validate(User user) {
        if (user.getEmail() == null) throw new Exception();
        if (user.getName() == null) throw new Exception();
        // Adicionar nova validação aqui = modificação
    }
}
```

```java
// ✅ CORRETO: Validadores extensíveis
public interface ValidationRule<T> {
    void validate(T entity);
}

@Component
public class EmailValidationRule implements ValidationRule<User> {
    public void validate(User user) {
        if (user.getEmail() == null) {
            throw new ValidationException("Email obrigatório");
        }
    }
}

@Component
public class NameValidationRule implements ValidationRule<User> {
    public void validate(User user) {
        if (user.getName() == null) {
            throw new ValidationException("Nome obrigatório");
        }
    }
}

// ✅ Adicionar nova regra = criar nova classe
@Component
public class AgeValidationRule implements ValidationRule<User> {
    public void validate(User user) {
        if (user.getAge() < 18) {
            throw new ValidationException("Deve ser maior de 18");
        }
    }
}

// Validador genérico
@Component
public class UserValidator {
    private final List<ValidationRule<User>> rules;

    public void validate(User user) {
        rules.forEach(rule -> rule.validate(user));
    }
}
```

### ✅ CHECKLIST DE VALIDAÇÃO

- [ ] Novas funcionalidades podem ser adicionadas **sem modificar código existente**?
- [ ] Comportamentos variáveis usam **abstrações** (interfaces)?
- [ ] Usa **Strategy, Specification ou similar** para variações?
- [ ] Não há **if/switch crescentes** para cada nova variação?
- [ ] Classes concretas dependem de **abstrações**, não de implementações?

### ❌ ANTI-PATTERNS

#### 1. Switch/If Crescente

```java
// ❌ Cada novo tipo = modificar esta classe
public void processNotification(String type, String message) {
    if (type.equals("EMAIL")) {
        // send email
    } else if (type.equals("SMS")) {
        // send sms
    } else if (type.equals("PUSH")) {
        // send push
    }
    // Adicionar WhatsApp = modificar aqui ❌
}
```

#### 2. Modificação de Código Testado

```java
// ❌ Adicionar feature = modificar código testado
@Service
public class ReportGenerator {
    public void generate(String format) {
        // 100 linhas de código testado

        // ❌ Adiciona novo formato = modifica tudo
        if (format.equals("NEW_FORMAT")) {
            // nova lógica
        }
    }
}
```

---

## 🎯 L - LISKOV SUBSTITUTION PRINCIPLE (LSP)

### 📖 O QUE É?

> **"Subtipos devem ser substituíveis por seus tipos base"**
>
> Ou seja: **Se S é subtipo de T, então T pode ser substituído por S sem quebrar o programa**

**Definição técnica:** Objetos de uma classe derivada devem poder substituir objetos da classe base sem alterar as propriedades desejáveis do programa (correção, execução de tarefas, etc).

### 💡 POR QUE USAR?

✅ **Garante polimorfismo correto** - Subst substituição funciona
✅ **Previne surpresas** - Subclasses se comportam como esperado
✅ **Facilita extensão** - Novas implementações funcionam automaticamente
✅ **Melhora confiabilidade** - Contratos são respeitados

### 📋 QUANDO USAR?

**Aplicável quando:**
- ✅ Usando herança
- ✅ Implementando interfaces
- ✅ Criando abstrações
- ✅ Usando polimorfismo

**Sinais de violação:**
- ❌ Subtipo lança exceções que base não lança
- ❌ Subtipo tem pré-condições mais fortes
- ❌ Subtipo tem pós-condições mais fracas
- ❌ Subtipo remove funcionalidades da base

### 🔧 COMO APLICAR?

#### Regra 1: Não fortaleça pré-condições

```java
// ❌ ERRADO: Subtipo adiciona restrição
public class Rectangle {
    protected int width;
    protected int height;

    public void setWidth(int width) {
        this.width = width; // Aceita qualquer valor
    }
}

public class Square extends Rectangle {
    @Override
    public void setWidth(int width) {
        if (width < 0) {
            throw new IllegalArgumentException(); // ❌ Restrição adicional
        }
        this.width = width;
        this.height = width; // ❌ Comportamento diferente
    }
}
```

```java
// ✅ CORRETO: Mesmas pré-condições
public interface Shape {
    void setDimension(int value);
}

public class Rectangle implements Shape {
    public void setDimension(int value) {
        if (value < 0) throw new IllegalArgumentException();
        this.width = value;
    }
}

public class Square implements Shape {
    public void setDimension(int value) {
        if (value < 0) throw new IllegalArgumentException(); // ✅ Mesma restrição
        this.side = value;
    }
}
```

#### Regra 2: Não enfraqueça pós-condições

```java
// ❌ ERRADO: Subtipo retorna menos do que promete
public interface PaymentPort {
    /**
     * @return Payment confirmado com ID gerado
     */
    Payment process(Payment payment);
}

@Component
public class FakePaymentAdapter implements PaymentPort {
    public Payment process(Payment payment) {
        return null; // ❌ Retorna null, viola contrato
    }
}
```

```java
// ✅ CORRETO: Respeita contrato
@Component
public class FakePaymentAdapter implements PaymentPort {
    public Payment process(Payment payment) {
        payment.setId(1L); // ✅ Retorna payment válido
        payment.setStatus(PaymentStatus.CONFIRMED);
        return payment;
    }
}
```

#### Regra 3: Respeite invariantes da base

```java
// ❌ ERRADO: Subtipo quebra invariante
public class BankAccount {
    protected BigDecimal balance;

    // Invariante: balance nunca pode ser negativo
    public void withdraw(BigDecimal amount) {
        if (balance.compareTo(amount) < 0) {
            throw new InsufficientFundsException();
        }
        balance = balance.subtract(amount);
    }
}

public class OverdraftAccount extends BankAccount {
    @Override
    public void withdraw(BigDecimal amount) {
        // ❌ Permite saldo negativo (quebra invariante)
        balance = balance.subtract(amount);
    }
}
```

```java
// ✅ CORRETO: Mantém invariante
public abstract class BankAccount {
    protected BigDecimal balance;
    protected BigDecimal minBalance; // Cada tipo define seu mínimo

    public void withdraw(BigDecimal amount) {
        if (balance.subtract(amount).compareTo(minBalance) < 0) {
            throw new InsufficientFundsException();
        }
        balance = balance.subtract(amount);
    }
}

public class StandardAccount extends BankAccount {
    public StandardAccount() {
        this.minBalance = BigDecimal.ZERO; // ✅ Não permite negativo
    }
}

public class OverdraftAccount extends BankAccount {
    public OverdraftAccount(BigDecimal overdraftLimit) {
        this.minBalance = overdraftLimit.negate(); // ✅ Permite até o limite
    }
}
```

### 📝 EXEMPLOS PRÁTICOS

#### Exemplo 1: Adapters

```java
// ✅ CORRETO: Adapters respeitam contratos
public interface PropertySavePort {
    Property save(Property property); // Contrato: sempre retorna property salva
}

@Component
public class PropertyJpaAdapter implements PropertySavePort {
    public Property save(Property property) {
        return repository.save(property); // ✅ Respeita contrato
    }
}

@Component
public class PropertyInMemoryAdapter implements PropertySavePort {
    public Property save(Property property) {
        property.setId(generateId());
        map.put(property.getId(), property);
        return property; // ✅ Respeita contrato
    }
}

// Cliente pode usar qualquer implementação
@Service
public class CreatePropertyUseCase {
    private final PropertySavePort savePort; // Pode ser qualquer implementação

    public Property execute(PropertyDTO dto) {
        Property property = mapper.toEntity(dto);
        return savePort.save(property); // ✅ Funciona com qualquer adapter
    }
}
```

### ✅ CHECKLIST DE VALIDAÇÃO

- [ ] Subtipo pode **substituir** o tipo base sem quebrar?
- [ ] Pré-condições do subtipo **não são mais fortes**?
- [ ] Pós-condições do subtipo **não são mais fracas**?
- [ ] Invariantes da classe base são **mantidas**?
- [ ] Subtipo **não lança exceções** que base não lança?
- [ ] Métodos do subtipo **respeitam o contrato** da base?

---

## 🎯 I - INTERFACE SEGREGATION PRINCIPLE (ISP)

### 📖 O QUE É?

> **"Nenhum cliente deve ser forçado a depender de métodos que não utiliza"**
>
> Ou seja: **Interfaces pequenas e específicas, não "gordas"**

**Definição técnica:** É melhor ter várias interfaces específicas do que uma interface genérica. Clientes não devem ser forçados a implementar métodos que não usam.

### 💡 POR QUE USAR?

✅ **Reduz acoplamento** - Clientes dependem apenas do necessário
✅ **Facilita testes** - Mocks mais simples
✅ **Aumenta flexibilidade** - Implementações parciais possíveis
✅ **Melhora manutenibilidade** - Mudanças afetam menos código
✅ **Clareza** - Fica claro o que cada cliente precisa

### 📋 QUANDO USAR?

**Use quando:**
- ✅ Interface tem muitos métodos
- ✅ Clientes usam apenas parte da interface
- ✅ Mudanças em um método afetam clientes que não o usam

**Sinais de violação:**
- ❌ Interface com mais de 5 métodos
- ❌ Implementações com métodos vazios ou lançando `UnsupportedOperationException`
- ❌ Clientes mockando métodos que não usam

### 🔧 COMO APLICAR?

#### PASSO 1: Identifique interface "gorda"

```java
// ❌ Interface "gorda" (viola ISP)
public interface PropertyRepositoryPort {
    // WRITE
    Property save(Property property);
    Property update(Property property);

    // READ
    Optional<Property> findById(Long id);
    Property findByIdOrThrow(Long id);
    List<Property> findAll();
    List<Property> findByUserId(Long userId);

    // DELETE
    void delete(Property property);
    void deleteById(Long id);

    // ANALYTICS
    Long count();
    boolean exists(Long id);
}
```

**Problema:** Use Case que só precisa SALVAR é forçado a depender de FIND, DELETE, ANALYTICS.

#### PASSO 2: Segregue por responsabilidade

```java
// ✅ CORRETO: Interfaces segregadas

// Port de escrita
public interface PropertySavePort {
    Property save(Property property);
}

// Port de leitura
public interface PropertyFindPort {
    Optional<Property> findById(Long id);
    Property findByIdOrThrow(Long id);
    List<Property> findAll();
    List<Property> findByUserId(Long userId);
}

// Port de deleção
public interface PropertyDeletePort {
    void delete(Property property);
    void deleteById(Long id);
}

// Port de analytics
public interface PropertyAnalyticsPort {
    Long count();
    boolean exists(Long id);
}
```

#### PASSO 3: Clientes dependem apenas do necessário

```java
// ✅ Use Case depende apenas do que precisa

@Service
public class CreatePropertyUseCase {
    private final PropertySavePort savePort;  // Apenas SAVE
    private final UserFindPort userFindPort;  // Apenas FIND

    // ✅ Não precisa de Delete, Analytics, etc
}

@Service
public class DeletePropertyUseCase {
    private final PropertyFindPort findPort;    // Apenas FIND
    private final PropertyDeletePort deletePort; // Apenas DELETE

    // ✅ Não precisa de Save, Analytics, etc
}

@Service
public class FindPropertyUseCase {
    private final PropertyFindPort findPort;  // Apenas FIND

    // ✅ Não precisa de Save, Delete, Analytics
}
```

#### PASSO 4: Adapter implementa todas

```java
// ✅ Adapter implementa todas as interfaces
@Component
public class PropertyRepositoryAdapter
        implements PropertySavePort,
                   PropertyFindPort,
                   PropertyDeletePort,
                   PropertyAnalyticsPort {

    private final PropertyRepository repository;

    // Implementa todos os métodos
    public Property save(Property property) {
        return repository.save(property);
    }

    public Optional<Property> findById(Long id) {
        return repository.findById(id);
    }

    public void delete(Property property) {
        repository.delete(property);
    }

    public Long count() {
        return repository.count();
    }
}
```

### 📝 EXEMPLOS PRÁTICOS

#### Exemplo 1: CQRS com ISP

```java
// ✅ Separação Command/Query com ISP

// Commands (Write)
public interface CreateCommand<T> {
    T create(T entity);
}

public interface UpdateCommand<T> {
    T update(T entity);
}

public interface DeleteCommand<T> {
    void delete(T entity);
}

// Queries (Read)
public interface FindQuery<T, ID> {
    Optional<T> findById(ID id);
    List<T> findAll();
}

// Adapter implementa o que precisa
@Component
public class PropertyRepositoryAdapter
        implements CreateCommand<Property>,
                   UpdateCommand<Property>,
                   DeleteCommand<Property>,
                   FindQuery<Property, Long> {
    // Implementação
}

// Use Cases dependem apenas do necessário
@Service
public class CreatePropertyUseCase {
    private final CreateCommand<Property> createCommand; // Apenas create
}

@Service
public class FindPropertyUseCase {
    private final FindQuery<Property, Long> findQuery; // Apenas find
}
```

### ✅ CHECKLIST DE VALIDAÇÃO

- [ ] Interfaces têm **no máximo 5 métodos**?
- [ ] Cada interface tem **uma única responsabilidade**?
- [ ] Clientes dependem **apenas do que usam**?
- [ ] **Não há** métodos vazios ou `UnsupportedOperationException` nas implementações?
- [ ] **Não há** clientes mockando métodos que não usam?
- [ ] Interfaces são **coesas** (métodos relacionados)?

### ❌ ANTI-PATTERNS

#### 1. Interface "Gorda"

```java
// ❌ 15+ métodos em uma interface
public interface UserRepositoryPort {
    User save(User user);
    User update(User user);
    void delete(User user);
    Optional<User> findById(Long id);
    List<User> findAll();
    List<User> findByRole(Role role);
    boolean existsByEmail(String email);
    Long count();
    void deleteAll();
    List<User> findByAgeGreaterThan(int age);
    // ... mais 10 métodos
}
```

#### 2. Implementação parcial forçada

```java
// ❌ Forçado a implementar métodos que não usa
public class InMemoryPropertyAdapter implements PropertyRepositoryPort {
    public Property save(Property property) {
        // implementação
    }

    public Optional<Property> findById(Long id) {
        // implementação
    }

    // ❌ Não usa, mas é forçado a implementar
    public void deleteAll() {
        throw new UnsupportedOperationException("Not implemented");
    }

    public Long count() {
        throw new UnsupportedOperationException("Not implemented");
    }
}
```

---

## 🎯 D - DEPENDENCY INVERSION PRINCIPLE (DIP)

### 📖 O QUE É?

> **"Dependa de abstrações, não de implementações concretas"**
>
> **Regras:**
> 1. Módulos de alto nível NÃO devem depender de módulos de baixo nível. Ambos devem depender de abstrações.
> 2. Abstrações NÃO devem depender de detalhes. Detalhes devem depender de abstrações.

**Definição técnica:** A regra de dependência deve apontar para abstrações (interfaces), não para implementações concretas (classes).

### 💡 POR QUE USAR?

✅ **Desacopla camadas** - Camadas não dependem de implementações
✅ **Facilita testes** - Pode injetar mocks
✅ **Permite substituição** - Troca implementações facilmente
✅ **Melhora flexibilidade** - Múltiplas implementações possíveis
✅ **Respeita Clean Architecture** - Regra de dependência correta

### 📋 QUANDO USAR?

**SEMPRE!** DIP é fundamental para arquitetura limpa.

**Sinais de violação:**
- ❌ Use Cases dependem de classes concretas de Infrastructure
- ❌ `new` dentro de classes de negócio
- ❌ Domain conhece Infrastructure
- ❌ Importa classes de camadas externas

### 🔧 COMO APLICAR?

#### PASSO 1: Identifique dependências concretas

```java
// ❌ ERRADO: Use Case depende de implementação concreta
@Service
public class CreatePropertyUseCase {
    private final PropertyRepository propertyRepository; // ❌ Classe concreta do Spring Data
    private final PropertyMapper propertyMapper;

    public Property execute(PropertyDTO dto) {
        Property property = propertyMapper.toEntity(dto);
        return propertyRepository.save(property); // ❌ Acoplado ao JPA
    }
}
```

**Problemas:**
- ❌ Use Case conhece tecnologia (JPA)
- ❌ Não pode trocar implementação facilmente
- ❌ Difícil testar (precisa de Spring context)

#### PASSO 2: Crie abstração (Port) no Domain

```java
// ✅ CORRETO: Port (abstração) no Domain
package com.example.ecommerce.product.domain.port.output;

public interface ProductSavePort {
    Product save(Product product);
}
```

**Por quê aqui?**
- ✅ Domain define o que precisa (não conhece como)
- ✅ Infrastructure implementa (conhece tecnologia)

#### PASSO 3: Use Case depende da abstração

```java
// ✅ CORRETO: Depende de abstração (Port)
@Service
public class CreatePropertyUseCase {
    private final PropertySavePort propertySavePort; // ✅ Interface (abstração)
    private final PropertyMapper propertyMapper;

    public Property execute(PropertyDTO dto) {
        Property property = propertyMapper.toEntity(dto);
        return propertySavePort.save(property); // ✅ Não sabe se é JPA, MongoDB, InMemory...
    }
}
```

#### PASSO 4: Adapter (Infrastructure) implementa Port

```java
// ✅ CORRETO: Adapter implementa Port
package com.example.ecommerce.product.infrastructure.adapter;

@Component
public class ProductRepositoryAdapter implements ProductSavePort {
    private final ProductRepository productRepository; // Spring Data JPA

    @Override
    public Product save(Product product) {
        return productRepository.save(product); // Usa JPA aqui
    }
}
```

#### PASSO 5: Spring injeta implementação

```java
// Spring automaticamente injeta PropertyRepositoryAdapter
// quando Use Case pede PropertySavePort

@Service
public class CreatePropertyUseCase {
    private final PropertySavePort propertySavePort;
    // ↑ Spring injeta PropertyRepositoryAdapter aqui
}
```

### 📝 EXEMPLO COMPLETO

```
┌─────────────────────────────────────────────────────────┐
│                     API LAYER                           │
│  PropertyController → PropertyFacade                    │
└─────────────────┬───────────────────────────────────────┘
                  │ (usa)
                  ↓
┌─────────────────────────────────────────────────────────┐
│                APPLICATION LAYER                        │
│  CreatePropertyUseCase                                  │
│      │                                                   │
│      │ (depende de)                                     │
│      ↓                                                   │
│  PropertySavePort (interface) ←────────┐               │
└──────────────────────────────────────┬──┘              │
                                       │                  │
                  (implementa)         │                  │
                                       │                  │
┌──────────────────────────────────────┴──────────────────┐
│                  DOMAIN LAYER                           │
│  Property (entity)                                      │
│  PropertySavePort (port/interface)                      │
└────────────────────────┬────────────────────────────────┘
                         │ (implementa)
                         ↓
┌─────────────────────────────────────────────────────────┐
│               INFRASTRUCTURE LAYER                      │
│  PropertyRepositoryAdapter implements PropertySavePort  │
│      │                                                   │
│      │ (usa)                                            │
│      ↓                                                   │
│  PropertyRepository (Spring Data JPA)                   │
└─────────────────────────────────────────────────────────┘
```

**Fluxo de dependência:**
```
Infrastructure → Domain ← Application ← API
```

**Todos dependem do Domain (centro)!**

### ✅ CHECKLIST DE VALIDAÇÃO

- [ ] Use Cases dependem de **interfaces (Ports)**, não de classes concretas?
- [ ] Ports estão no **Domain** (`domain/port/output/`)?
- [ ] Adapters estão na **Infrastructure** (`infrastructure/adapter/`)?
- [ ] Domain **NÃO** importa nada de Infrastructure?
- [ ] Domain **NÃO** importa nada de Application?
- [ ] Regra de dependência: **Infrastructure → Domain ← Application ← API**?
- [ ] **Não há `new`** de classes de Infrastructure no Domain/Application?

### ❌ ANTI-PATTERNS

#### 1. Dependência direta de implementação

```java
// ❌ Use Case depende de classe concreta
@Service
public class CreatePropertyUseCase {
    private final PropertyJpaRepository repository; // ❌ Implementação JPA

    public Property execute(PropertyDTO dto) {
        return repository.save(property); // ❌ Acoplado ao JPA
    }
}
```

#### 2. Domain conhecendo Infrastructure

```java
// ❌ Domain importando Infrastructure
package com.example.ecommerce.product.domain.service;

import com.example.ecommerce.product.infrastructure.ProductRepository; // ❌ ERRADO!

@Service
public class ProductDomainService {
    private final ProductRepository repository; // ❌ Domain conhece Infrastructure
}
```

#### 3. `new` de dependências

```java
// ❌ Instancia dependência com `new`
@Service
public class CreatePropertyUseCase {
    public Property execute(PropertyDTO dto) {
        PropertyRepository repository = new PropertyJpaRepository(); // ❌ ERRADO!
        return repository.save(property);
    }
}
```

---

## 🏛️ CLEAN ARCHITECTURE - VISÃO GERAL

### 📖 O QUE É?

**Clean Architecture** é uma arquitetura em camadas que:

1. **Separa preocupações** - Cada camada tem responsabilidade clara
2. **Regra de dependência** - Dependências apontam para o centro (Domain)
3. **Independência de frameworks** - Domain não conhece Spring, JPA, etc
4. **Testabilidade** - Camadas testáveis isoladamente

### 🎯 CAMADAS

```
                   ┌─────────────┐
                   │     API     │ (Controllers, DTOs, Mappers)
                   └──────┬──────┘
                          │ (usa)
                   ┌──────▼──────┐
                   │ APPLICATION │ (Facades, Use Cases, Orchestrators)
                   └──────┬──────┘
                          │ (usa Ports)
                   ┌──────▼──────┐
                   │   DOMAIN    │ (Entities, Ports, Services, Exceptions) ← NÚCLEO
                   └──────▲──────┘
                          │ (implementa Ports)
                   ┌──────┴──────┐
                   │INFRASTRUCTURE│ (Adapters, Repositories, External APIs)
                   └─────────────┘
```

### 📐 REGRA DE DEPENDÊNCIA

> **Dependências sempre apontam para DENTRO (Domain)**

```
Infrastructure → Domain ← Application ← API
```

**O que isso significa:**
- ✅ Infrastructure **pode** importar Domain
- ✅ Application **pode** importar Domain
- ✅ API **pode** importar Application
- ❌ Domain **NUNCA** importa nada externo
- ❌ Application **NUNCA** importa Infrastructure
- ❌ Domain **NUNCA** importa Application

### 🔧 ESTRUTURA DE PACOTES

```
com.example.ecommerce.product/
│
├── api/                            # Camada API (Controllers, DTOs)
│   ├── controller/
│   │   └── ProductController.java
│   ├── dto/
│   │   ├── request/
│   │   │   └── ProductRequestDTO.java
│   │   └── response/
│   │       └── ProductResponseDTO.java
│   └── mapper/
│       └── ProductMapper.java
│
├── application/                    # Camada Application (Use Cases, Facades)
│   ├── facade/
│   │   ├── ProductFacade.java (interface)
│   │   └── impl/
│   │       └── ProductFacadeImpl.java
│   ├── usecase/
│   │   ├── command/                # Commands (CQRS - Write)
│   │   │   ├── CreateProductUseCase.java
│   │   │   ├── UpdateProductUseCase.java
│   │   │   └── DeleteProductUseCase.java
│   │   └── query/                  # Queries (CQRS - Read)
│   │       └── FindProductUseCase.java
│   └── orchestrator/               # Orchestrators (transações complexas)
│       └── ProductSaveOrchestrator.java
│
├── domain/                         # Camada Domain (NÚCLEO)
│   ├── entity/
│   │   └── Product.java            # Entidade com métodos de domínio
│   ├── port/
│   │   └── output/                 # Ports (abstrações para Infrastructure)
│   │       ├── ProductSavePort.java
│   │       ├── ProductFindPort.java
│   │       └── ProductDeletePort.java
│   ├── service/                    # Domain Services (lógica entre entidades)
│   │   ├── ProductPricingValidator.java
│   │   └── ValidateStockAvailabilityService.java
│   ├── exception/                  # Exceções de domínio
│   │   ├── ProductException.java
│   │   └── ProductNotFoundException.java
│   └── enums/
│       └── ProductStatus.java
│
└── infrastructure/                 # Camada Infrastructure (Adapters, Repositories)
    ├── adapter/                    # Adapters (implementam Ports)
    │   └── ProductRepositoryAdapter.java
    ├── ProductRepository.java      # Spring Data JPA Repository
    └── external/                   # Integrações externas
        └── ProductExternalApi.java
```

### ✅ CHECKLIST DE VALIDAÇÃO

- [ ] **API** depende apenas de **Application**?
- [ ] **Application** depende apenas de **Domain**?
- [ ] **Infrastructure** depende apenas de **Domain**?
- [ ] **Domain** NÃO depende de nada externo?
- [ ] Ports estão em **domain/port/output/**?
- [ ] Adapters estão em **infrastructure/adapter/**?
- [ ] Use Cases estão em **application/usecase/**?
- [ ] Entities estão em **domain/entity/**?

---

## 🏗️ ARQUITETURAS DE SOFTWARE - VISÃO GERAL

### 📖 O QUE SÃO ARQUITETURAS DE SOFTWARE?

**Arquitetura de Software** é a organização fundamental de um sistema, definindo:

1. **Estrutura de componentes** - Como o código é organizado
2. **Relacionamentos** - Como componentes interagem
3. **Princípios de design** - Regras que guiam decisões
4. **Evolução** - Como o sistema cresce e se adapta

### 🎯 TIPOS DE ARQUITETURA

| Arquitetura | Características | Quando Usar |
|------------|-----------------|-------------|
| **Monolito Tradicional** | Tudo em um único código, acoplado | Protótipos, MVPs simples |
| **Monolito Modular** | Modular por domínio, baixo acoplamento | Maioria dos projetos modernos |
| **Microsserviços** | Serviços independentes, deployáveis separadamente | Escala extrema, times grandes |
| **Serverless** | Funções isoladas, sem servidor | Eventos, processamento pontual |

### 🎯 NOSSA ESCOLHA: MONOLITO MODULAR POR DOMÍNIO

**Por que escolhemos Monolito Modular?**

✅ **Simplicidade operacional** - Um deploy, um servidor
✅ **Performance** - Sem latência de rede entre módulos
✅ **Desenvolvimento rápido** - Compartilhamento de código fácil
✅ **Transações ACID** - Facilidade de consistência
✅ **Preparado para Microsserviços** - Módulos já separados

---

## 🏗️ MONOLITO MODULAR POR DOMÍNIO

### 📖 O QUE É MONOLITO MODULAR POR DOMÍNIO?

É uma arquitetura onde:

1. **Um único artefato deployável** (JAR, WAR)
2. **Módulos fortemente separados por domínio** (Property, User, Supply, etc.)
3. **Baixo acoplamento entre módulos**
4. **Alta coesão dentro de cada módulo**
5. **Cada módulo segue Clean Architecture**

### 🎯 POR QUE USAR MONOLITO MODULAR?

#### ✅ **VANTAGENS**

**1. Simplicidade Operacional**
```
Monolito Modular:
- 1 servidor
- 1 banco de dados
- 1 deploy
- 1 log centralizado

Microsserviços:
- 10+ servidores
- 10+ bancos de dados
- 10+ deploys coordenados
- Logs distribuídos (complexo)
```

**2. Performance Superior**
```java
// MONOLITO MODULAR: Chamada em memória (< 1ms)
Property property = propertyService.findById(1L);
User owner = userService.findById(property.getOwnerId());

// MICROSSERVIÇOS: Chamada HTTP (50-200ms)
Property property = propertyClient.findById(1L);  // HTTP call
User owner = userClient.findById(property.getOwnerId()); // HTTP call
```

**3. Transações ACID Simples**
```java
// MONOLITO MODULAR: Transação ACID fácil
@Transactional
public void transferProperty(Long propertyId, Long newOwnerId) {
    Property property = propertyRepository.findById(propertyId);
    User newOwner = userRepository.findById(newOwnerId);
    property.setOwner(newOwner);
    propertyRepository.save(property);
    notificationService.notifyOwnerChange(property); // Tudo ou nada
}

// MICROSSERVIÇOS: Saga Pattern complexo
public void transferProperty(Long propertyId, Long newOwnerId) {
    // 1. Reserve property
    // 2. Validate user
    // 3. Update property (pode falhar)
    // 4. Notify (compensating transaction se falhar)
    // Muito mais complexo!
}
```

**4. Desenvolvimento Mais Rápido**
- Refatoração fácil entre módulos
- Compartilhamento de código comum
- Debugging simples
- Testes integrados mais fáceis

**5. Preparado para Microsserviços**
```
Monolito Modular estruturado = Microsserviços adormecidos

modules/
├── property/        → Futuro: Property Microservice
├── user/           → Futuro: User Microservice
├── supply/         → Futuro: Supply Microservice
└── stock/          → Futuro: Stock Microservice
```

#### ❌ **QUANDO NÃO USAR**

- ❌ Precisa escalar módulos de forma **totalmente independente**
- ❌ Times **geograficamente distribuídos** em fusos muito diferentes
- ❌ Tecnologias **completamente diferentes** por módulo (Java + Python + Go)
- ❌ Requisitos regulatórios de **isolamento físico**

### 🛠️ COMO IMPLEMENTAR MONOLITO MODULAR?

#### **REGRA #1: Módulos Independentes**

```
✅ ESTRUTURA CORRETA (Exemplo E-commerce):

com.example.ecommerce/
├── product/                     # Módulo Product
│   ├── api/
│   ├── application/
│   ├── domain/
│   └── infrastructure/
├── user/                        # Módulo User
│   ├── api/
│   ├── application/
│   ├── domain/
│   └── infrastructure/
├── order/                       # Módulo Order
│   ├── api/
│   ├── application/
│   ├── domain/
│   └── infrastructure/
└── shared/                      # Código compartilhado
    └── common/
        ├── exception/
        └── util/
```

#### **REGRA #2: Comunicação entre Módulos via Facade**

```java
// ❌ ERRADO: Acoplamento direto
@Service
public class OrderService {
    @Autowired
    private ProductRepository productRepository; // ❌ Acoplamento com outro módulo!

    public void addProductToOrder(Long orderId, Long productId) {
        Order order = orderRepository.findById(orderId);
        Product product = productRepository.findById(productId); // ❌ Acessando outro módulo diretamente
        order.addProduct(product);
    }
}

// ✅ CORRETO: Comunicação via Facade
@Service
public class OrderService {
    private final ProductFacade productFacade; // ✅ Interface pública do módulo Product

    public void addProductToOrder(Long orderId, Long productId) {
        Order order = orderRepository.findById(orderId);
        Product product = productFacade.findProductById(productId); // ✅ Via Facade
        order.addProduct(product);
    }
}
```

#### **REGRA #3: Cada Módulo = Clean Architecture Completa**

```
product/
├── api/                         # Camada API
│   ├── controller/
│   ├── dto/
│   └── mapper/
├── application/                 # Camada Application
│   ├── facade/                  # ← Facade (ponto de entrada público)
│   └── usecase/
├── domain/                      # Camada Domain
│   ├── entity/
│   ├── port/
│   └── service/
└── infrastructure/              # Camada Infrastructure
    ├── adapter/
    └── ProductRepository.java
```

#### **REGRA #4: Dependências entre Módulos**

```java
// Ordem de dependência:
// shared ← domain ← application ← api ← infrastructure

// ✅ Order pode depender de Product (via Facade)
com.example.ecommerce.order.application.facade.OrderFacadeImpl
    → depende de ProductFacade (interface pública)

// ❌ Product NÃO pode depender de Order (dependência cíclica)
```

### 📊 EXEMPLO PRÁTICO: SISTEMA E-COMMERCE

```
Arquitetura: Monolito Modular por Domínio

Módulos:
├── product/     → Catálogo de produtos
├── user/        → Autenticação e usuários
├── order/       → Gestão de pedidos
├── payment/     → Processamento de pagamentos
├── shipping/    → Gestão de entregas
└── inventory/   → Controle de estoque

Características:
✅ Deploy único (1 JAR)
✅ Banco de dados compartilhado (PostgreSQL)
✅ Módulos comunicam via Facade
✅ Cada módulo segue Clean Architecture
✅ Preparado para extração de microsserviços
```

### ✅ CHECKLIST DE MONOLITO MODULAR

- [ ] Cada módulo tem suas 4 camadas (API, Application, Domain, Infrastructure)?
- [ ] Módulos comunicam apenas via Facades (interfaces públicas)?
- [ ] Não há dependências cíclicas entre módulos?
- [ ] Cada módulo pode ser testado independentemente?
- [ ] Cada módulo tem seu próprio agregado de domínio?
- [ ] Código compartilhado está em `shared/common/`?
- [ ] Transações não cruzam múltiplos módulos sem necessidade?
- [ ] Cada módulo poderia ser extraído como microsserviço?

### 🚫 ANTI-PATTERNS A EVITAR

#### ❌ **Big Ball of Mud**
```java
// ❌ ANTI-PATTERN: Tudo misturado
@Service
public class PropertyService {
    // Mistura Property + User + Supply + Stock
    public void processEverything() {
        // 1000 linhas de código misturado
    }
}
```

#### ❌ **Acoplamento Direto entre Módulos**
```java
// ❌ PropertyService acessando UserRepository diretamente
@Service
public class PropertyService {
    @Autowired
    private UserRepository userRepository; // ❌ Acoplamento!
}
```

#### ❌ **Shared Database como API**
```java
// ❌ Property acessando tabela de User diretamente via SQL
@Query("SELECT u FROM User u WHERE u.id IN " +
       "(SELECT p.ownerId FROM Property p WHERE p.id = :propertyId)")
List<User> findOwners(@Param("propertyId") Long propertyId);
// ❌ Violação de encapsulamento do módulo User
```

---

## 🌐 MICROSSERVIÇOS

### 📖 O QUE SÃO MICROSSERVIÇOS?

**Microsserviços** é uma arquitetura onde:

1. **Serviços independentes** - Cada serviço é um processo separado
2. **Deploy independente** - Pode atualizar um serviço sem afetar outros
3. **Banco de dados por serviço** - Cada serviço tem seu próprio BD
4. **Comunicação via rede** - HTTP/REST, gRPC, mensageria
5. **Tecnologia heterogênea** - Cada serviço pode usar tech diferente

### 🎯 POR QUE USAR MICROSSERVIÇOS?

#### ✅ **VANTAGENS**

**1. Escalabilidade Independente**
```
Exemplo: Black Friday no e-commerce

Monolito:
- Precisa escalar TUDO (mesmo partes não usadas)
- 10 instâncias de toda aplicação

Microsserviços:
- Escala só o que precisa
- 50 instâncias do Payment Service
- 20 instâncias do Catalog Service
- 2 instâncias do Admin Service
```

**2. Deploy Independente**
```
Monolito:
- Bug no módulo X → Precisa redeployar TUDO
- Risco alto a cada deploy

Microsserviços:
- Bug no Payment → Redeploy só Payment Service
- Outros serviços continuam rodando
```

**3. Times Autônomos**
```
Microsserviços permitem:
- Time Payment → mantém Payment Service (Java)
- Time Catalog → mantém Catalog Service (Go)
- Time Search → mantém Search Service (Python)
- Cada time com autonomia total
```

**4. Resiliência**
```java
// Circuit Breaker Pattern
@CircuitBreaker(name = "userService")
public User getUserById(Long id) {
    return userServiceClient.findById(id);
}

// Se User Service cair, Property Service continua funcionando
// (com fallback ou dados em cache)
```

**5. Tecnologia Heterogênea**
```
Property Service → Java + Spring Boot
User Service → Go + Gin
Search Service → Python + FastAPI + Elasticsearch
Analytics Service → Node.js + Express
```

#### ❌ **DESVANTAGENS**

**1. Complexidade Operacional**
```
Monolito:
- 1 deploy
- 1 log
- 1 monitoramento

Microsserviços:
- 10+ deploys coordenados
- Logs distribuídos (ELK Stack)
- Tracing distribuído (Jaeger, Zipkin)
- Service mesh (Istio)
- API Gateway
- Load balancers
```

**2. Latência de Rede**
```java
// Monolito: 1ms
property.getOwner().getName();

// Microsserviços: 50-200ms
User owner = httpClient.get("http://user-service/users/" + ownerId);
```

**3. Transações Distribuídas (Complexidade++)**
```java
// Monolito: ACID simples
@Transactional
public void transferProperty(Long propertyId, Long newOwnerId) {
    property.setOwner(newOwner);
    propertyRepository.save(property);
}

// Microsserviços: Saga Pattern
public void transferProperty(Long propertyId, Long newOwnerId) {
    // 1. Reserve property (Property Service)
    // 2. Validate owner (User Service)
    // 3. Transfer ownership (Property Service)
    // 4. Send notification (Notification Service)
    // 5. Compensating transactions se algo falhar
}
```

**4. Custo de Infraestrutura**
```
Monolito:
- 1 servidor (4 vCPUs, 8GB RAM) = $50/mês

Microsserviços:
- 10 serviços × $20/mês = $200/mês
- Kubernetes cluster = $150/mês
- Load balancer = $30/mês
- API Gateway = $50/mês
Total = $430/mês (8.6x mais caro)
```

### 🛠️ COMO IMPLEMENTAR MICROSSERVIÇOS?

#### **PASSO 1: Identificar Bounded Contexts**

```
Bounded Contexts (Exemplo E-commerce):

Product Context        → Product Microservice
User Context          → User Microservice
Order Context         → Order Microservice
Payment Context       → Payment Microservice
Shipping Context      → Shipping Microservice
Inventory Context     → Inventory Microservice
Notification Context  → Notification Microservice
```

#### **PASSO 2: Separar Bancos de Dados**

```
Antes (Monolito):
PostgreSQL (shared)
├── product_table
├── user_table
├── order_table
└── inventory_table

Depois (Microsserviços):
Product Service   → PostgreSQL 1 (product_table)
User Service      → PostgreSQL 2 (user_table)
Order Service     → PostgreSQL 3 (order_table)
Inventory Service → MongoDB (inventory_collection)
```

#### **PASSO 3: Comunicação entre Serviços**

```java
// Opção 1: REST/HTTP (Síncrono)
@FeignClient(name = "user-service")
public interface UserServiceClient {
    @GetMapping("/users/{id}")
    User findById(@PathVariable Long id);
}

// Opção 2: Mensageria (Assíncrono)
@Service
public class PropertyService {
    private final RabbitTemplate rabbitTemplate;

    public void notifyPropertyCreated(Property property) {
        rabbitTemplate.convertAndSend(
            "property-events",
            "property.created",
            property
        );
    }
}
```

#### **PASSO 4: API Gateway**

```
Cliente → API Gateway → Microsserviços

API Gateway (Kong, Spring Cloud Gateway):
├── /api/products/**   → Product Service
├── /api/users/**      → User Service
├── /api/orders/**     → Order Service
└── /api/inventory/**  → Inventory Service

Responsabilidades do Gateway:
✅ Roteamento
✅ Autenticação/Autorização
✅ Rate limiting
✅ Logging
```

### ✅ CHECKLIST DE MICROSSERVIÇOS

- [ ] Cada serviço tem seu próprio banco de dados?
- [ ] Serviços podem ser deployados independentemente?
- [ ] Há API Gateway para roteamento?
- [ ] Implementou Circuit Breaker para resiliência?
- [ ] Logs centralizados (ELK, Splunk)?
- [ ] Distributed Tracing (Jaeger, Zipkin)?
- [ ] Service Discovery (Eureka, Consul)?
- [ ] Mensageria para comunicação assíncrona (RabbitMQ, Kafka)?
- [ ] Monitoramento (Prometheus + Grafana)?
- [ ] Cada serviço tem seu próprio CI/CD?

### 🚫 ANTI-PATTERNS A EVITAR

#### ❌ **Nano-services (Granularidade excessiva)**
```
❌ ERRADO:
- PropertyCreateService
- PropertyUpdateService
- PropertyDeleteService
- PropertyFindService
(Muito granular!)

✅ CORRETO:
- PropertyService (com todos os casos de uso)
```

#### ❌ **Shared Database**
```
❌ ANTI-PATTERN:
Property Service ─┐
User Service     ─┼→ PostgreSQL (shared)
Supply Service   ─┘

✅ PATTERN CORRETO:
Property Service → PostgreSQL 1
User Service     → PostgreSQL 2
Supply Service   → PostgreSQL 3
```

#### ❌ **Chatty Communication**
```java
// ❌ ANTI-PATTERN: 10 chamadas HTTP para renderizar 1 página
public PropertyDetails getPropertyDetails(Long id) {
    Property property = propertyClient.findById(id);      // HTTP 1
    User owner = userClient.findById(property.getOwnerId()); // HTTP 2
    List<Field> fields = fieldClient.findByProperty(id);    // HTTP 3
    // ... 7 chamadas adicionais
}

// ✅ CORRETO: Agregação no backend ou BFF (Backend for Frontend)
@Service
public class PropertyAggregationService {
    public PropertyDetailsDTO getPropertyDetails(Long id) {
        // 1 chamada que retorna tudo agregado
    }
}
```

---

## 🔄 MIGRAÇÃO: MONOLITO → MICROSSERVIÇOS

### 📖 POR QUE COMEÇAR COM MONOLITO MODULAR?

**Monolito Modular é o caminho ideal para Microsserviços:**

```
Estratégia: Modular First, Microservices When Needed

1. Comece com Monolito Modular        (Desenvolvimento rápido)
2. Aplique Clean Architecture         (Preparação para migração)
3. Separe módulos por domínio         (Bounded Contexts claros)
4. Use Facades para comunicação       (Contratos bem definidos)
5. Extraia microsserviços quando necessário (Migração gradual)
```

### 🎯 QUANDO MIGRAR PARA MICROSSERVIÇOS?

#### ✅ **SINAIS DE QUE É HORA DE MIGRAR**

**1. Problemas de Escalabilidade**
```
Sintoma:
- Módulo X precisa 10x mais recursos que módulo Y
- Desperdício de recursos escalando tudo junto

Solução:
- Extrair Módulo X como microsserviço
- Escalar apenas o que precisa
```

**2. Times Grandes (> 50 desenvolvedores)**
```
Problema:
- 50+ devs commitando no mesmo repositório
- Conflitos de merge constantes
- Deploy coordenado complexo

Solução:
- Dividir em microsserviços
- 1 time por serviço (8-10 pessoas)
```

**3. Deploy Muito Arriscado**
```
Problema:
- Mudança pequena no módulo X = redeploy de TUDO
- Downtime inaceitável

Solução:
- Microsserviços permitem deploy independente
- Zero downtime com blue-green deployment
```

**4. Tecnologias Diferentes por Contexto**
```
Necessidade:
- Search precisa Python + Elasticsearch
- Analytics precisa Node.js + Redis
- Core precisa Java + PostgreSQL

Solução:
- Microsserviços com stacks heterogêneas
```

#### ❌ **QUANDO NÃO MIGRAR**

- ❌ Time pequeno (< 10 pessoas)
- ❌ Tráfego baixo (< 10k req/min)
- ❌ Startup em estágio inicial (MVP)
- ❌ Falta de expertise em DevOps/Infra
- ❌ "Porque está na moda" ⚠️

### 🛠️ ESTRATÉGIA DE MIGRAÇÃO: STRANGLER FIG PATTERN

```
Padrão: Migração Gradual (não Big Bang!)

Monolito                          Microsserviços
┌─────────────────┐               ┌──────────────┐
│  Product        │               │  Product     │
│  User           │  ──────────>  │  Service     │
│  Order          │               └──────────────┘
│  Payment        │               ┌──────────────┐
│  Shipping       │               │  User        │
│  Inventory      │               │  Service     │
└─────────────────┘               └──────────────┘
                                  ┌──────────────┐
                                  │  Order       │
                                  │  Service     │
                                  └──────────────┘
```

#### **PASSO 1: Extrair Módulo Independente (ex: User)**

```java
// 1. User já está modular no monolito
com.example.ecommerce.user/
├── api/
├── application/
│   └── facade/UserFacade.java  // ← Interface pública
├── domain/
└── infrastructure/

// 2. Criar User Microservice (projeto separado)
user-service/
├── src/
│   └── (copiar código do módulo user)
├── pom.xml                      // Dependências próprias
└── Dockerfile

// 3. Deployar User Service separadamente
- Docker container
- Kubernetes pod
- URL: http://user-service:8081
```

#### **PASSO 2: Alterar Monolito para Chamar User Service**

```java
// ANTES: Chamada local
@Service
public class PropertyFacadeImpl implements PropertyFacade {
    private final UserFacade userFacade; // Injeção local

    public void addEmployee(Long propertyId, Long userId) {
        User user = userFacade.findUserById(userId); // Chamada em memória
        // ...
    }
}

// DEPOIS: Chamada remota via Feign Client
@Service
public class PropertyFacadeImpl implements PropertyFacade {
    private final UserServiceClient userServiceClient; // HTTP Client

    public void addEmployee(Long propertyId, Long userId) {
        User user = userServiceClient.findUserById(userId); // HTTP call
        // ...
    }
}

@FeignClient(name = "user-service", url = "${user.service.url}")
public interface UserServiceClient {
    @GetMapping("/users/{id}")
    User findUserById(@PathVariable Long id);
}
```

#### **PASSO 3: Separar Banco de Dados**

```sql
-- ANTES: PostgreSQL shared
CREATE TABLE user (id, name, email, ...);
CREATE TABLE property (id, owner_id, ...); -- FK para user

-- DEPOIS: 2 bancos separados
-- User Service DB:
CREATE TABLE user (id, name, email, ...);

-- Property Service DB:
CREATE TABLE property (
    id,
    owner_id,  -- Não é mais FK! Apenas referência
    owner_name, -- Desnormalização (cache local)
    ...
);
```

#### **PASSO 4: Implementar Event-Driven para Consistência**

```java
// User Service: Publica evento quando user muda
@Service
public class UserService {
    private final RabbitTemplate rabbitTemplate;

    public void updateUser(User user) {
        userRepository.save(user);

        // Publica evento
        rabbitTemplate.convertAndSend(
            "user-events",
            "user.updated",
            new UserUpdatedEvent(user.getId(), user.getName())
        );
    }
}

// Property Service: Escuta evento e atualiza cache local
@Service
public class PropertyEventListener {
    @RabbitListener(queues = "property-user-events")
    public void handleUserUpdated(UserUpdatedEvent event) {
        // Atualiza campo desnormalizado owner_name
        propertyRepository.updateOwnerName(
            event.getUserId(),
            event.getNewName()
        );
    }
}
```

#### **PASSO 5: Repetir para Outros Módulos**

```
Ordem Recomendada de Extração:

1. User Service         (± independente, poucos acoplamentos)
2. Notification Service (± independente)
3. Inventory Service    (acoplamento médio)
4. Shipping Service     (acoplamento médio)
5. Product Service      (core, extrair por último)
6. Order Service        (core, depende de Product)
7. Payment Service      (core, depende de Order)
```

### 📊 COMPARAÇÃO: ANTES E DEPOIS

```
╔═══════════════════════════════════════════════════════════════╗
║           MONOLITO MODULAR → MICROSSERVIÇOS                   ║
╠═══════════════════════════════════════════════════════════════╣
║  ANTES (Monolito Modular)      │  DEPOIS (Microsserviços)     ║
╠═══════════════════════════════════════════════════════════════╣
║  1 repositório                 │  7 repositórios              ║
║  1 deploy                      │  7 deploys independentes     ║
║  1 servidor                    │  7+ containers               ║
║  1 banco de dados              │  7 bancos de dados           ║
║  Chamadas em memória (1ms)     │  Chamadas HTTP (50-200ms)    ║
║  ACID simples                  │  Eventual consistency + Saga ║
║  Infraestrutura simples        │  Kubernetes + Service Mesh   ║
║  Custo: $50/mês                │  Custo: $500/mês             ║
║  Time: 5-20 pessoas            │  Time: 50+ pessoas           ║
╚═══════════════════════════════════════════════════════════════╝
```

### ✅ CHECKLIST DE MIGRAÇÃO

**Preparação (ainda no Monolito):**
- [ ] Módulos seguem Clean Architecture?
- [ ] Módulos comunicam apenas via Facades?
- [ ] Não há dependências cíclicas?
- [ ] Cada módulo tem testes independentes?
- [ ] Bounded Contexts bem definidos?

**Durante a Migração:**
- [ ] Extrair 1 módulo por vez (Strangler Fig)?
- [ ] Implementar Feign Client / HTTP communication?
- [ ] Separar banco de dados?
- [ ] Implementar Circuit Breaker?
- [ ] Configurar API Gateway?
- [ ] Implementar Event-Driven (RabbitMQ/Kafka)?
- [ ] Logs centralizados (ELK)?
- [ ] Distributed Tracing (Jaeger)?

**Pós-Migração:**
- [ ] Monitoramento (Prometheus + Grafana)?
- [ ] Alertas configurados?
- [ ] Documentação atualizada (Swagger/OpenAPI)?
- [ ] Runbooks para incidentes?
- [ ] Testes de carga?
- [ ] Disaster recovery plan?

### 🎯 DECISÃO FINAL: QUAL ARQUITETURA ESCOLHER?

```
┌─────────────────────────────────────────────────────────────┐
│  ÁRVORE DE DECISÃO: ARQUITETURA                            │
└─────────────────────────────────────────────────────────────┘

Time < 10 pessoas?
  │
  └─ SIM → MONOLITO MODULAR ✅
  │
  └─ NÃO → Continuar...

Tráfego < 10k req/min?
  │
  └─ SIM → MONOLITO MODULAR ✅
  │
  └─ NÃO → Continuar...

Precisa escalar partes diferentes de forma independente?
  │
  └─ NÃO → MONOLITO MODULAR ✅
  │
  └─ SIM → Continuar...

Tem expertise DevOps/Infra?
  │
  └─ NÃO → MONOLITO MODULAR ✅
  │
  └─ SIM → MICROSSERVIÇOS ✅
```

### 📚 RECURSOS PARA APROFUNDAR

**Livros:**
- "Building Microservices" - Sam Newman
- "Monolith to Microservices" - Sam Newman
- "Domain-Driven Design" - Eric Evans

**Patterns:**
- Strangler Fig Pattern (migração gradual)
- Saga Pattern (transações distribuídas)
- Circuit Breaker Pattern (resiliência)
- API Gateway Pattern (roteamento)
- Event Sourcing (auditoria + eventos)

---

## 🎨 DDD - VISÃO GERAL

### 📖 O QUE É DOMAIN-DRIVEN DESIGN?

**DDD** é uma abordagem de desenvolvimento de software que:

1. **Foca no domínio** - Entenda profundamente o negócio
2. **Linguagem ubíqua** - Mesma linguagem entre dev e negócio
3. **Entidades ricas** - Lógica de negócio nas entidades
4. **Bounded Contexts** - Divisão clara de contextos
5. **Agregados** - Consistência transacional

### 🎯 CONCEITOS PRINCIPAIS

#### 1. **Entidade (Entity)**
Objeto com identidade única (ID).

```java
@Entity
public class Property {
    @Id
    private Long id; // Identidade única

    private String name;
    private BigDecimal areaSize;
}
```

#### 2. **Value Object**
Objeto sem identidade, definido por seus valores.

```java
@Embeddable
public class Address {
    private String street;
    private String city;
    private String zipCode;

    // Sem ID, comparação por valores
    @Override
    public boolean equals(Object o) {
        // compara todos os campos
    }
}
```

#### 3. **Aggregate Root**
Entidade principal que controla o acesso a outras entidades.

```java
@Entity
public class Property {  // Aggregate Root
    @OneToMany(mappedBy = "property")
    private List<Field> fields;      // Controlada pelo Aggregate

    @OneToMany(mappedBy = "property")
    private List<Machine> machines;  // Controlada pelo Aggregate

    // Métodos para adicionar/remover fields e machines
}
```

#### 4. **Domain Service**
Lógica de negócio que não pertence a uma entidade específica.

```java
@Service
public class PropertyOwnershipValidator { // Domain Service
    public void validate(Property property, Long userId) {
        if (!property.isOwnedBy(userId)) {
            throw new PropertyException("Sem permissão");
        }
    }
}
```

#### 5. **Repository**
Abstração para persistência de Aggregates.

```java
public interface PropertyRepository {
    Property save(Property property);
    Optional<Property> findById(Long id);
}
```

### 🎯 ENTIDADES RICAS VS ANÊMICAS

#### ❌ ENTIDADE ANÊMICA (ERRADO)

```java
// Apenas getters/setters (anêmica)
@Entity
public class Order {
    private Long id;
    private List<OrderItem> items = new ArrayList<>();
    private BigDecimal total;

    // ❌ Sem comportamentos
    public List<OrderItem> getItems() { return items; }
    public void setItems(List<OrderItem> items) { this.items = items; }
    public BigDecimal getTotal() { return total; }
    public void setTotal(BigDecimal total) { this.total = total; }
}

// ❌ Lógica fora da entidade
@Service
public class OrderService {
    public void addItem(Order order, Product product, int quantity) {
        OrderItem item = new OrderItem(product, quantity);
        order.getItems().add(item);
        order.setTotal(calculateTotal(order)); // ❌ Cálculo fora
    }
}
```

**Problemas:**
- ❌ Lógica espalhada em services
- ❌ Fácil violar invariantes
- ❌ Difícil de testar
- ❌ Não expressa domínio

#### ✅ ENTIDADE RICA (DDD CORRETO)

```java
// Entidade rica com comportamentos
@Entity
public class Order {
    private Long id;
    private List<OrderItem> items = new ArrayList<>();
    private BigDecimal total = BigDecimal.ZERO;
    private OrderStatus status = OrderStatus.PENDING;

    // ✅ MÉTODOS DE DOMÍNIO

    /**
     * Adiciona produto ao pedido.
     * Invariante: Não pode adicionar itens após confirmação.
     */
    public void addItem(Product product, int quantity) {
        // Validações
        if (product == null) {
            throw new IllegalArgumentException("Product não pode ser null");
        }
        if (quantity <= 0) {
            throw new IllegalArgumentException("Quantity deve ser positiva");
        }

        // Invariante
        if (this.status != OrderStatus.PENDING) {
            throw new IllegalStateException("Não pode modificar pedido confirmado");
        }

        // Adiciona item e recalcula total
        OrderItem item = new OrderItem(product, quantity);
        this.items.add(item);
        this.recalculateTotal();
    }

    public boolean belongsTo(Long userId) {
        return this.customerId != null && this.customerId.equals(userId);
    }

    public int getItemsCount() {
        return items.size();
    }

    private void recalculateTotal() {
        this.total = items.stream()
            .map(OrderItem::getSubtotal)
            .reduce(BigDecimal.ZERO, BigDecimal::add);
    }
}

// ✅ Service apenas orquestra
@Service
public class AddItemToOrderUseCase {
    public void execute(Long orderId, Long productId, int quantity) {
        Order order = orderFindPort.findByIdOrThrow(orderId);
        Product product = productFindPort.findByIdOrThrow(productId);

        // ✅ Delega para método de domínio
        order.addItem(product, quantity);

        orderSavePort.save(order);
    }
}
```

**Benefícios:**
- ✅ Lógica centralizada na entidade
- ✅ Invariantes protegidas
- ✅ Fácil de testar isoladamente
- ✅ Expressa domínio claramente

---

## 🧠 MÉTODOS DE DOMÍNIO - GUIA COMPLETO

### 📖 O QUE SÃO MÉTODOS DE DOMÍNIO?

**Métodos de domínio** são comportamentos que pertencem naturalmente à entidade, encapsulando a lógica de negócio dentro do próprio objeto.

**Princípio Tell, Don't Ask:**
- ❌ Não **pergunte** dados e faça algo com eles
- ✅ **Diga** ao objeto o que fazer

### 🎯 CATEGORIAS DE MÉTODOS DE DOMÍNIO

#### 1. **MÉTODOS DE VALIDAÇÃO/CONSULTA**

Retornam `boolean` ou valor, **NÃO modificam** estado.

```java
/**
 * Verifica se pedido pertence ao usuário.
 */
public boolean belongsTo(Long userId) {
    return this.customerId != null && this.customerId.equals(userId);
}

/**
 * Verifica se pedido tem itens.
 */
public boolean hasItems() {
    return items != null && !items.isEmpty();
}

/**
 * Verifica se estoque está baixo.
 */
public boolean isLowStock() {
    return this.quantity.compareTo(new BigDecimal("10")) < 0;
}
```

**Quando usar:**
- ✅ Verificações de propriedade/estado
- ✅ Validações booleanas
- ✅ Consultas simples sobre a entidade

**Por que usar:**
- ✅ Encapsula lógica de verificação
- ✅ Código legível: `order.belongsTo(userId)`
- ✅ Facilita mudanças futuras
- ✅ Tell, Don't Ask

#### 2. **MÉTODOS DE CÁLCULO**

Retornam valores calculados, **NÃO modificam** estado.

```java
/**
 * Calcula valor total do pedido.
 */
public BigDecimal getTotalAmount() {
    if (items == null || items.isEmpty()) {
        return BigDecimal.ZERO;
    }
    return items.stream()
        .map(OrderItem::getSubtotal)
        .reduce(BigDecimal.ZERO, BigDecimal::add);
}

/**
 * Conta itens do pedido.
 */
public int getItemsCount() {
    return items != null ? items.size() : 0;
}

/**
 * Calcula valor total do item.
 */
public BigDecimal getSubtotal() {
    return price.multiply(new BigDecimal(quantity));
}
```

**Quando usar:**
- ✅ Cálculos baseados em campos da entidade
- ✅ Contagens, somatórias, agregações
- ✅ Valores derivados

**Por que usar:**
- ✅ Cálculos junto aos dados que usam
- ✅ Evita duplicação
- ✅ Fácil de testar isoladamente
- ✅ Information Expert (GRASP)

#### 3. **MÉTODOS DE MANIPULAÇÃO**

**MODIFICAM** estado com validações.

```java
/**
 * Adiciona item ao pedido.
 * Invariante: Não pode modificar pedido confirmado.
 */
public void addItem(Product product, int quantity) {
    // Validação 1: Null check
    if (product == null) {
        throw new IllegalArgumentException("Product não pode ser null");
    }

    // Validação 2: Invariante
    if (this.status != OrderStatus.PENDING) {
        throw new IllegalStateException("Não pode modificar pedido confirmado");
    }

    // Validação 3: Quantidade positiva
    if (quantity <= 0) {
        throw new IllegalArgumentException("Quantidade deve ser positiva");
    }

    // Adiciona item e recalcula total
    OrderItem item = new OrderItem(product, quantity);
    this.items.add(item);
    this.recalculateTotal();
}

/**
 * Remove item do pedido.
 */
public void removeItem(OrderItem item) {
    if (this.status != OrderStatus.PENDING) {
        throw new IllegalStateException("Não pode modificar pedido confirmado");
    }
    if (this.items.remove(item)) {
        this.recalculateTotal();  // Recalcula total
    }
}

/**
 * Decrementa quantidade em estoque.
 * Invariante: quantity >= 0
 */
public void decrementStock(int amount) {
    if (amount <= 0) {
        throw new IllegalArgumentException("Quantidade deve ser positiva");
    }
    if (this.stockQuantity < amount) {
        throw new IllegalStateException("Estoque insuficiente");
    }
    this.stockQuantity -= amount;
}
```

**Quando usar:**
- ✅ Adicionar/remover em coleções
- ✅ Modificar campos com validação
- ✅ Manter consistência bidirecional

**Por que usar:**
- ✅ **PROTEGE INVARIANTES**
- ✅ Mantém consistência
- ✅ Valida antes de modificar
- ✅ Centraliza regras

#### 4. **MÉTODOS DE TRANSIÇÃO DE ESTADO**

Modificam estado com regras de transição.

```java
/**
 * Define machine como em manutenção.
 */
public void setInMaintenance() {
    if (this.status == MachineStatus.OUT_OF_SERVICE) {
        throw new IllegalStateException(
            "Máquina fora de serviço não pode entrar em manutenção"
        );
    }
    this.status = MachineStatus.MAINTENANCE;
}

/**
 * Ativa field.
 */
public void activate() {
    this.status = FieldStatus.ACTIVE;
}

/**
 * Desativa field.
 */
public void deactivate() {
    this.status = FieldStatus.INACTIVE;
}
```

**Quando usar:**
- ✅ Mudanças de estado com regras
- ✅ Status da entidade
- ✅ Máquina de estados

**Por que usar:**
- ✅ Garante transições válidas
- ✅ Previne estados inconsistentes
- ✅ Expressa operações de negócio

### 🔍 COMO IDENTIFICAR MÉTODO DE DOMÍNIO?

Use estas perguntas:

| Pergunta | Resposta | Ação |
|----------|----------|------|
| Manipula apenas dados desta entidade? | Sim | ✅ Método de domínio |
| Protege invariante da entidade? | Sim | ✅ Método de domínio |
| Usa apenas campos da entidade? | Sim | ✅ Método de domínio |
| Útil em múltiplos Use Cases? | Sim | ✅ Método de domínio |
| Expressa ação do negócio? | Sim | ✅ Método de domínio |
| Envolve múltiplas entidades? | Sim | ❌ Domain Service |
| Acessa banco de dados? | Sim | ❌ Repository |
| Chama API externa? | Sim | ❌ Infrastructure |

### ✅ CHECKLIST

- [ ] Método **apenas manipula dados da própria entidade**?
- [ ] Método **protege invariantes**?
- [ ] Método **mantém consistência bidirecional**?
- [ ] Método **NÃO acessa banco de dados**?
- [ ] Método **NÃO chama serviços externos**?
- [ ] Método **é testável isoladamente** (sem Spring/BD)?
- [ ] Nome do método **expressa claramente a intenção**?

### ❌ O QUE NÃO É MÉTODO DE DOMÍNIO

```java
// ❌ Persistência (Infrastructure)
public void save() {
    repository.save(this);
}

// ❌ Enviar email (Infrastructure)
public void sendWelcomeEmail() {
    emailService.send(...);
}

// ❌ Chamar API externa (Infrastructure)
public void notifyExternalSystem() {
    api.notify(...);
}

// ❌ Buscar outras entidades (Infrastructure)
public User findOwner() {
    return userRepository.findById(this.userId);
}

// ❌ Lógica entre múltiplas entidades (Domain Service)
public boolean canDelete(User user, List<Property> properties) {
    // Envolve múltiplas entidades
}
```

---

## 🎭 DESIGN PATTERNS - CATÁLOGO

### 📖 INTRODUÇÃO

Design Patterns são **soluções reutilizáveis para problemas comuns**.

**Princípio fundamental:**
> **Use patterns para resolver problemas REAIS, não para "ficar bonito"**

### ✅ PATTERNS USADOS NO PROJETO

| Pattern | Quando Usar | Onde Aplicado |
|---------|-------------|---------------|
| **Repository** | Abstrair persistência | PropertyRepository |
| **Adapter** | Adaptar tecnologia externa | PropertyRepositoryAdapter |
| **Facade** | Simplificar acesso a subsistemas | PropertyFacadeImpl |
| **CQRS** | Separar leitura e escrita | command/query |
| **Strategy** | Múltiplas formas de fazer algo | DiscountStrategy |
| **Specification** | Queries complexas reutilizáveis | PropertySpecification |

### 🆕 PATTERNS RECOMENDADOS (quando necessário)

| Pattern | Use Se | Não Use Se |
|---------|--------|------------|
| **Builder** | DTOs com muitos campos opcionais | Objetos simples (2-3 campos) |
| **Factory** | Criação de entidades com regras | Criação simples sem lógica |

### ❌ PATTERNS A EVITAR

| Pattern | Por Que Evitar |
|---------|----------------|
| **Singleton** | Spring já gerencia instâncias |
| **Observer** | Use Spring Events |
| **Abstract Factory** | Muito complexo |
| **Proxy** | Spring AOP já faz |
| **Decorator** | Adicione só se necessário |

---

## 📚 REPOSITORY PATTERN

### 📖 O QUE É?

Abstração que encapsula acesso a dados, separando lógica de negócio da persistência.

### 💡 POR QUE USAR?

✅ **Desacopla persistência** - Troca tecnologia sem afetar negócio
✅ **Facilita testes** - Mock do repository
✅ **Centraliza queries** - Um lugar para queries
✅ **Abstrai tecnologia** - Domain não conhece JPA, MongoDB, etc

### 🔧 COMO APLICAR?

```java
// Spring Data JPA Repository
@Repository
public interface PropertyRepository extends JpaRepository<Property, Long> {
    List<Property> findByUserId(Long userId);
    List<Property> findByNameContaining(String name);
}
```

### ✅ CHECKLIST

- [ ] Repository é **interface**?
- [ ] Repository retorna **entidades de domínio**?
- [ ] Repository está na camada **Infrastructure**?
- [ ] Use Cases dependem de **Ports**, não de Repository?

---

## 🔌 ADAPTER PATTERN

### 📖 O QUE É?

Adapta uma tecnologia externa (JPA, API, etc) para o domínio (Port).

### 💡 POR QUE USAR?

✅ **Isola tecnologia** - Domain não conhece JPA
✅ **Facilita troca** - Troca adapter, não muda domain
✅ **Respeita DIP** - Domain define port, Infrastructure implementa

### 🔧 COMO APLICAR?

```java
// Port (Domain)
public interface PropertySavePort {
    Property save(Property property);
}

// Adapter (Infrastructure)
@Component
public class PropertyRepositoryAdapter implements PropertySavePort {
    private final PropertyRepository repository; // JPA

    @Override
    public Property save(Property property) {
        return repository.save(property); // Adapta JPA para Domain
    }
}
```

### ✅ CHECKLIST

- [ ] Adapter está na camada **Infrastructure**?
- [ ] Adapter implementa **Port do Domain**?
- [ ] Adapter **NÃO expõe** detalhes de tecnologia?
- [ ] Use Cases dependem do **Port**, não do Adapter?

---

## 🏛️ FACADE PATTERN

### 📖 O QUE É?

Simplifica acesso a um subsistema complexo fornecendo interface única.

### 💡 POR QUE USAR?

✅ **Simplifica API** - Uma interface para múltiplos Use Cases
✅ **Reduz acoplamento** - Controller não conhece Use Cases individuais
✅ **Facilita mudanças** - Muda Use Cases sem afetar Controllers

### 🔧 COMO APLICAR?

```java
// Facade (Application)
@Service
public class PropertyFacadeImpl implements PropertyFacade {
    private final CreatePropertyUseCase createUseCase;
    private final UpdatePropertyUseCase updateUseCase;
    private final DeletePropertyUseCase deleteUseCase;
    private final FindPropertyUseCase findUseCase;

    @Override
    public PropertyResponseDTO create(PropertyRequestDTO dto, Long userId) {
        return createUseCase.execute(dto, userId);
    }

    @Override
    public void delete(Long propertyId, Long userId) {
        deleteUseCase.execute(propertyId, userId);
    }

    // ... outros métodos
}

// Controller usa Facade
@RestController
public class PropertyController {
    private final PropertyFacade propertyFacade; // Uma única dependência

    @PostMapping
    public ResponseEntity<PropertyResponseDTO> create(@RequestBody PropertyRequestDTO dto) {
        return ResponseEntity.ok(propertyFacade.create(dto, getUserId()));
    }
}
```

### ✅ CHECKLIST

- [ ] Facade está na camada **Application**?
- [ ] Facade **apenas delega** para Use Cases?
- [ ] Facade **NÃO contém lógica de negócio**?
- [ ] Controller depende da **Facade**, não de Use Cases individuais?

---

## 🎯 CQRS PATTERN

### 📖 O QUE É?

**Command Query Responsibility Segregation**: Separa operações de leitura (Query) e escrita (Command).

### 💡 POR QUE USAR?

✅ **Clareza** - Fica claro o que modifica e o que consulta
✅ **Otimização** - Otimize leitura e escrita independentemente
✅ **Escalabilidade** - Escale leitura e escrita separadamente
✅ **SRP** - Separação clara de responsabilidades

### 🔧 COMO APLICAR?

```
application/
├── usecase/
│   ├── command/          # Commands (WRITE - modificam estado)
│   │   ├── CreatePropertyUseCase.java
│   │   ├── UpdatePropertyUseCase.java
│   │   └── DeletePropertyUseCase.java
│   └── query/            # Queries (READ - não modificam estado)
│       └── FindPropertyUseCase.java
```

```java
// Command (WRITE)
@Service
public class CreatePropertyUseCase {
    @Transactional
    public PropertyResponseDTO execute(PropertyDTO dto, Long userId) {
        // Modifica estado
        Property property = mapper.toEntity(dto);
        Property saved = propertySavePort.save(property);
        return mapper.toDTO(saved);
    }
}

// Query (READ)
@Service
public class FindPropertyUseCase {
    @Transactional(readOnly = true) // ✅ Read-only
    public PropertyResponseDTO findById(Long id) {
        // Não modifica estado
        Property property = propertyFindPort.findByIdOrThrow(id);
        return mapper.toDTO(property);
    }
}
```

### ✅ CHECKLIST

- [ ] Commands estão em **application/usecase/command/**?
- [ ] Queries estão em **application/usecase/query/**?
- [ ] Commands **modificam estado**?
- [ ] Queries **NÃO modificam estado**?
- [ ] Queries usam **@Transactional(readOnly = true)**?

---

## 🎯 STRATEGY PATTERN

### 📖 O QUE É?

Define família de algoritmos, encapsula cada um e torna-os intercambiáveis.

### 💡 POR QUE USAR?

✅ **OCP** - Adiciona estratégia sem modificar código
✅ **SRP** - Cada estratégia em sua classe
✅ **Elimina if/else** - Sem switch/if crescentes
✅ **Testabilidade** - Testa cada estratégia isoladamente

### 🔧 COMO APLICAR?

```java
// Interface Strategy
public interface DiscountStrategy {
    BigDecimal calculate(BigDecimal price);
}

// Estratégias concretas
@Component("noDiscount")
public class NoDiscount implements DiscountStrategy {
    public BigDecimal calculate(BigDecimal price) {
        return price;
    }
}

@Component("seasonalDiscount")
public class SeasonalDiscount implements DiscountStrategy {
    public BigDecimal calculate(BigDecimal price) {
        return price.multiply(new BigDecimal("0.9")); // 10% off
    }
}

@Component("vipDiscount")
public class VIPDiscount implements DiscountStrategy {
    public BigDecimal calculate(BigDecimal price) {
        return price.multiply(new BigDecimal("0.8")); // 20% off
    }
}

// Uso
@Service
public class PriceCalculator {
    private final Map<String, DiscountStrategy> strategies;

    public BigDecimal calculatePrice(BigDecimal price, String discountType) {
        DiscountStrategy strategy = strategies.get(discountType);
        return strategy.calculate(price);
    }
}
```

### ✅ CHECKLIST

- [ ] Estratégias implementam **interface comum**?
- [ ] Cada estratégia está em **classe separada**?
- [ ] **Não há if/switch** para selecionar estratégia?
- [ ] Estratégias são **intercambiáveis**?

---

## 📋 CHECKLIST DE CÓDIGO PERFEITO

Use este checklist para validar seu código:

### ✅ SOLID

- [ ] **SRP:** Cada classe tem 1 responsabilidade?
- [ ] **OCP:** Novo comportamento via extensão, não modificação?
- [ ] **LSP:** Subtipos são substituíveis?
- [ ] **ISP:** Interfaces segregadas (não gordas)?
- [ ] **DIP:** Depende de abstrações, não implementações?

### ✅ CLEAN ARCHITECTURE

- [ ] Estrutura de pacotes correta (api/application/domain/infrastructure)?
- [ ] Regra de dependência: Infrastructure → Domain ← Application ← API?
- [ ] Ports em domain/port/output/?
- [ ] Adapters em infrastructure/adapter/?
- [ ] Use Cases em application/usecase/?

### ✅ DDD

- [ ] Entidades ricas com métodos de domínio?
- [ ] Invariantes protegidas?
- [ ] Aggregate Roots identificados?
- [ ] Domain Services para lógica entre entidades?
- [ ] Linguagem ubíqua respeitada?

### ✅ DESIGN PATTERNS

- [ ] Repository Pattern para persistência?
- [ ] Adapter Pattern para tecnologias externas?
- [ ] Facade Pattern para simplificar API?
- [ ] CQRS para separar leitura/escrita?

### ✅ GRASP

- [ ] Information Expert: Dados e comportamento juntos?
- [ ] Creator: Quem cria sabe como criar?
- [ ] Controller: Ponto de entrada claro?
- [ ] Low Coupling: Dependências mínimas?
- [ ] High Cohesion: Elementos relacionados juntos?

### ✅ POO

- [ ] Encapsulamento: Dados protegidos?
- [ ] Abstração: Interfaces bem definidas?
- [ ] Polimorfismo: Múltiplas implementações?
- [ ] Herança: Usada com moderação?

### ✅ CÓDIGO

- [ ] Testes passando?
- [ ] Cobertura > 80%?
- [ ] Sem warnings do compilador?
- [ ] Sem código duplicado?
- [ ] Nomes expressivos?
- [ ] Métodos < 20 linhas?
- [ ] Classes < 300 linhas?

---

## ⚠️ ANTI-PATTERNS A EVITAR

### ❌ GOD CLASS

Classe que faz TUDO.

**Solução:** Divida em classes especializadas (SRP).

### ❌ ENTIDADE ANÊMICA

Entidade apenas com getters/setters.

**Solução:** Adicione métodos de domínio (DDD).

### ❌ INTERFACE GORDA

Interface com muitos métodos.

**Solução:** Segregue interface (ISP).

### ❌ IF/SWITCH CRESCENTE

Switch que cresce a cada nova variação.

**Solução:** Use Strategy Pattern (OCP).

### ❌ DEPENDÊNCIA CONCRETA

Classe depende de implementação.

**Solução:** Dependa de abstração (DIP).

### ❌ LÓGICA NO CONTROLLER

Controller com lógica de negócio.

**Solução:** Mova para Use Case/Domain.

### ❌ DOMAIN CONHECE INFRASTRUCTURE

Domain importando Infrastructure.

**Solução:** Use Ports (DIP).

---

## 🎯 REFERÊNCIA RÁPIDA

### ONDE COLOCAR CADA COISA?

| O QUE | ONDE | EXEMPLO |
|-------|------|---------|
| Entidade JPA | domain/entity/ | Product.java |
| Port (interface) | domain/port/output/ | ProductSavePort.java |
| Domain Service | domain/service/ | ProductPricingValidator.java |
| Exception | domain/exception/ | ProductNotFoundException.java |
| Use Case Command | application/usecase/command/ | CreateProductUseCase.java |
| Use Case Query | application/usecase/query/ | FindProductUseCase.java |
| Facade | application/facade/impl/ | ProductFacadeImpl.java |
| Adapter | infrastructure/adapter/ | ProductRepositoryAdapter.java |
| Repository | infrastructure/ | ProductRepository.java |
| Controller | api/controller/ | ProductController.java |
| DTO Request | api/dto/request/ | ProductRequestDTO.java |
| DTO Response | api/dto/response/ | ProductResponseDTO.java |
| Mapper | api/mapper/ | ProductMapper.java |

### NOMENCLATURA

| TIPO | PADRÃO | EXEMPLO |
|------|--------|---------|
| Use Case (Command) | [Verbo][Entidade]UseCase | CreateProductUseCase |
| Use Case (Query) | Find[Entidade]UseCase | FindProductUseCase |
| Port (Save) | [Entidade]SavePort | ProductSavePort |
| Port (Find) | [Entidade]FindPort | ProductFindPort |
| Port (Delete) | [Entidade]DeletePort | ProductDeletePort |
| Adapter | [Entidade]RepositoryAdapter | ProductRepositoryAdapter |
| Repository | [Entidade]Repository | ProductRepository |
| Domain Service | [Entidade][Ação]Validator/Service | ProductPricingValidator |
| Facade | [Entidade]FacadeImpl | ProductFacadeImpl |
| Exception | [Entidade][Tipo]Exception | ProductNotFoundException |

### ARQUITETURAS: QUANDO USAR?

| CRITÉRIO | MONOLITO MODULAR | MICROSSERVIÇOS |
|----------|------------------|----------------|
| **Tamanho do Time** | < 20 pessoas | > 50 pessoas |
| **Tráfego** | < 10k req/min | > 100k req/min |
| **Complexidade Operacional** | Simples (1 deploy) | Alta (múltiplos deploys) |
| **Custo Infraestrutura** | Baixo ($50-100/mês) | Alto ($500+/mês) |
| **Escalabilidade** | Vertical (escala tudo junto) | Horizontal (escala independente) |
| **Latência entre Módulos** | ~1ms (em memória) | ~50-200ms (HTTP) |
| **Transações** | ACID simples | Saga Pattern (complexo) |
| **Deploy** | Risco médio/alto | Risco baixo (independente) |
| **Tecnologias** | Homogênea (Java) | Heterogênea (Java, Go, Python) |
| **Fase do Projeto** | MVP, Crescimento | Escala massiva |

**Recomendação:** Comece com **Monolito Modular**, migre para **Microsserviços** quando necessário!

---

**Este é seu guia definitivo! Consulte sempre que tiver dúvidas! 📚✨**
