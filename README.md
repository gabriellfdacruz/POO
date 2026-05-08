# Encapsulamento em Java com Getters e Setters

Este repositório demonstra conceitos fundamentais da **Programação Orientada a Objetos (POO)** em Java utilizando uma classe `Car`.

O projeto mostra como utilizar:

* encapsulamento
* atributos privados
* getters e setters
* validação de dados
* operador ternário

Tudo isso através da criação e manipulação de objetos representando carros.

---

# 📂 Estrutura do Projeto

## `Main.java`

Classe principal responsável por instanciar objetos da classe `Car`, definir seus atributos e exibir informações no console.

Também demonstra o uso de múltiplos objetos com diferentes características.

---

## `Car.java`

Classe que representa um carro.

Define atributos privados e métodos públicos para acesso e modificação controlada dos dados.

### Atributos:

* `make`
* `model`
* `color`
* `doors`
* `convertible`

### Métodos:

* getters
* setters
* `descibreCar()`

---

# 🧠 Conceitos Demonstrados

## 🔹 Encapsulamento

Os atributos da classe são privados (`private`), impedindo acesso direto externo.

```java id="m3v9op"
private String make;
private String model;
private String color;
private int doors;
private boolean convertible;
```

O acesso é controlado através de métodos públicos.

---

## 🔹 Getters e Setters

Permitem ler e modificar os atributos de maneira segura.

### Exemplo:

```java id="u4q8ka"
public String getMake() {
    return make;
}
```

```java id="k0n7wr"
public void setColor(String color) {
    this.color = color;
}
```

---

## 🔹 Validação de Dados

O método `setMake()` valida se a marca do carro é suportada.

Caso a marca não esteja entre as opções permitidas, o valor será definido como `"Unsupported"`.

```java id="t2s6ez"
switch(lowercaseMake) {
    case "holden", "porsche", "tesla" -> this.make = make;
    default -> {
        this.make = "Unsupported";
    }
}
```

---

## 🔹 Operador Ternário

O método `descibreCar()` utiliza operador ternário para verificar se o carro é conversível.

```java id="g5l1pq"
(convertible ? "Convertible" : "")
```

---

# 🚀 Exemplo de Execução

```java id="y8r4hs"
public static void main(String[] args) {

    Car car = new Car();

    car.setMake("Porsche");
    car.setModel("Carrera");
    car.setDoors(2);
    car.setConvertible(true);
    car.setColor("Green");

    System.out.println("make = " + car.getMake());
    System.out.println("model = " + car.getModel());

    car.descibreCar();

    Car targa = new Car();

    targa.setMake("Porsche");
    targa.setModel("Targa");
    targa.setDoors(2);
    targa.setConvertible(false);
    targa.setColor("Purple");

    targa.descibreCar();
}
```

---

# 💻 Saída Esperada

```txt id="p9v7qx"
make = Porsche
model = Carrera

2-door Green Porsche Carrera Convertible

2-door Purple Porsche Targa
```

---

# ⚙️ Como Executar

## 1️⃣ Clone o repositório

```bash id="r7m4tz"
git clone https://github.com/seu-usuario/java-car-encapsulation.git
```

---

## 2️⃣ Compile os arquivos

```bash id="a1c9lv"
javac Main.java Car.java
```

---

## 3️⃣ Execute o programa

```bash id="d4f8ys"
java Main
```

---

# 📚 Objetivo do Projeto

Este projeto foi desenvolvido para praticar os conceitos básicos de Programação Orientada a Objetos em Java.

Ideal para:

* iniciantes em Java
* estudo de encapsulamento
* prática com getters e setters
* exercícios de validação de atributos
* portfólio e GitHub

---

# 🛠️ Tecnologias Utilizadas

* Java
* Programação Orientada a Objetos (POO)

---

# 🤝 Contribuição

Contribuições são bem-vindas!

Sugestões de melhorias, novas funcionalidades ou otimizações podem ser enviadas via Pull Request 🚀

