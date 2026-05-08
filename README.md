Encapsulamento e Validação de Dados em Java

Este projeto demonstra conceitos fundamentais da Programação Orientada a Objetos (POO) em Java utilizando uma classe Car.

A aplicação mostra como utilizar:

atributos privados
getters e setters
encapsulamento
validação de dados
operadores condicionais

Tudo isso através da criação e manipulação de objetos representando carros.

📂 Estrutura do Projeto
Main.java

Classe principal responsável por criar os objetos Car, definir seus atributos e exibir as informações no console.

Neste arquivo são criados dois carros:

Porsche Carrera
Porsche Targa
Car.java

Classe que representa um carro.

Contém atributos privados e métodos públicos para acesso e modificação dos dados.

🧠 Conceitos Demonstrados
🔹 Encapsulamento

Os atributos da classe são definidos como private, impedindo acesso direto externo.

private String make;
private String model;
private String color;
private int doors;
private boolean convertible;

O acesso é feito através de métodos get e set.

🔹 Getters e Setters

Permitem controlar leitura e alteração dos atributos.

Exemplo:
public String getMake() {
    return make;
}
public void setColor(String color) {
    this.color = color;
}
🔹 Validação de Dados

O método setMake() valida se a marca informada é suportada.

Caso contrário, define automaticamente como "Unsupported".

switch(lowercaseMake) {
    case "holden", "porsche", "tesla" -> this.make = make;
    default -> this.make = "Unsupported";
}
🔹 Operador Ternário

O método descibreCar() utiliza operador ternário para verificar se o carro é conversível.

(convertible ? "Convertible" : "")
🚀 Exemplo de Execução
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
💻 Saída Esperada
make = Porsche
model = Carrera

2-door Green Porsche Carrera Convertible

2-door Purple Porsche Targa
⚙️ Como Executar
1️⃣ Clone o repositório
git clone https://github.com/seu-usuario/car-java-oop.git
2️⃣ Compile os arquivos
javac Main.java Car.java
3️⃣ Execute o programa
java Main
📚 Objetivo do Projeto

Este projeto foi desenvolvido para praticar conceitos básicos e essenciais da Programação Orientada a Objetos em Java.

Ideal para:

iniciantes em Java
prática de encapsulamento
entendimento de getters/setters
exercícios de validação de atributos
projetos para GitHub e portfólio
🛠️ Tecnologias Utilizadas
Java
Programação Orientada a Objetos (POO)
