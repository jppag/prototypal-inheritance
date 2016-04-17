(http://javascript.crockford.com/inheritance.html)

## Intro

- Javascript não é uma linguagem baseada em classes;
- Orientada a objetos, utiliza a herança prototipal  ao inves ta classica. 
- Diferente do C++ e Java, por ex.

## Herança

- conveniencia. queremos que a linguagem modele as referencias de classes similares. Muito importante Linguagens tipadas. No JS, que é loosely typed, as referências de objetos não precisam de modelagem

- Reutilização de código. Objetos utilizando os mesmos métodos. ou que compartilham métodos mas possuem alguns diferentes.

## Construtor

- qualquer função que é usada como construtor. JS não faz distinção. Uma função pode ser usada como construtor ou ser chamada normalmente como uma função

- implementado para funcionar mais como Java

- construtor é usado com o ``new``

- Quando o ``new`` é chamado, JS realiza 4 operações: 
	
	* cria um novo objeto;
	* seta a propriedade constructor do objeto ao (mostrar exemplo) Vehicle. bmw.constructor == Vehicle vai dar true. bmw vai ser uma instancia de Vehicle
	* delega ao objeto criado o Vehicle.prototype
	* chama o Vehicle() no contexto do novo objeto

- Setando uma propriedade ao .prototype do construtor, todas as instancias (bmw), terão essa propriedade em seu prototype. 

## Herança prototipal

(http://javascript.crockford.com/prototypal.html)
(http://javascript.info/tutorial/inheritance)

- objetos herdam de objetos;

- objetos são mutáveis;

- Arrays are objects. Functions are objects. Objects are objects. Coleções de pares com nome - valor;

- __proto__;

- quando um método que o objeto não tem (mas seu prototype tem) é chamado, se não for encontrado, vai para o prototype. Tendo um "this" declarado nesse método, ele é referente ao objeto. Mesmo que ele não tenha o método em si.

- se alguma propriedade for assigned, num método do prototype, dando assign no this, a propriedade vai para o objeto.

- Object.create() ou com constructor;

(https://blog.pivotal.io/labs/labs/javascript-constructors-prototypes-and-the-new-keyword)
 
- Se for utilizar o hasOwnPropertyOf(nomeDaProp), e a propriedade do objeto vier herdada do prototype, vai dar false.
