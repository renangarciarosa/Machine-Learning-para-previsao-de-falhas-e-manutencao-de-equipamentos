# Machine Learning para previsão de falhas e manutenção de equipamentos (PM)

Neste notebook, abordo detalhadamente um problema de manutenção preditiva. Esses tipos de problemas podem ser complicados por vários motivos. As primeiras seis seções tratam da construção de um modelo. As últimas seções tratam da avaliação da eficácia do modelo e da garantia de sua eficácia quando implantado na produção.


Quando se trata de lidar com máquinas que requerem manutenção periódica, geralmente há três resultados possíveis.

1. **você pode manter uma máquina com muita frequência**. Em outras palavras, a máquina recebe manutenção quando não é necessária. Nesse cenário, você está jogando dinheiro pela janela, desperdiçando recursos e fornecendo manutenção desnecessária. Por exemplo, você pode trocar o óleo do seu carro todos os dias. Isso não é o ideal e você desperdiçará muito dinheiro em manutenção desnecessária.

2. **você não mantém sua máquina com frequência suficiente**. A falta de manutenção de uma máquina significa que a máquina irá quebrar durante a operação. Aqui, os custos podem ser substanciais. Você não apenas tem os custos de reparo, mas também os custos associados à perda de produção. Se uma máquina na linha de montagem falhar, a linha não pode produzir nada. Nenhuma produção significa lucro perdido. Além disso, você incorrerá em custos legais e médicos se ocorrerem lesões como resultado da falha.

3. **uma máquina é mantida quando precisa de manutenção**. Esta é obviamente a melhor alternativa das três. Observe que ainda há um custo associado à manutenção oportuna.

Então, precisamos manter as máquinas quando elas precisam de manutenção, certo? Infelizmente, isso é mais fácil dizer do que fazer. Felizmente, podemos usar a manutenção preditiva (PM) para prever quando as máquinas precisam de manutenção.

Também devo mencionar que a maioria das máquinas vem com recomendações do fabricante sobre manutenção. O problema com as recomendações do fabricante é que elas representam uma média. Por exemplo, os carros, em média, precisam de uma troca de óleo a cada 3.000 milhas, mas com que frequência seu carro precisa de uma troca de óleo? Pode ser mais ou menos de 3.000 milhas, dependendo de vários fatores, incluindo onde você dirige, como dirige e com que frequência dirige.

A manutenção preditiva (PM) pode informar, com base em dados, quando uma máquina precisa de manutenção. Um programa de PM eficaz minimizará a manutenção insuficiente e excessiva de sua máquina. Para um grande fabricante com milhares de máquinas, ser preciso na manutenção das máquinas pode economizar milhões de dólares todos os anos.

Neste projeto, examinarei um caso de uso típico de manutenção preditiva (PM). À medida que passo por este exemplo, descreverei alguns dos problemas que surgem com os problemas de PM e sugerirei maneiras de resolvê-los.

Uma observação importante sobre os dados usados ​​neste exercício. É inteiramente falso. Criei os dados com base na minha experiência de lidar com esses tipos de problemas. Embora seja totalmente artificial, acredito que os dados e o caso de uso sejam muito realistas e consistentes com muitos problemas reais de PM.

A empresa em nosso caso de uso forneceu uma amostra de dados que inclui 421 máquinas que falharam em dois anos. Eles gastaram 11,766 milhões de dólares em manutenção, a maioria dos quais veio de máquinas em funcionamento até a falha.

Aqui está um resumo das máquinas mantidas ou reparadas nos últimos dois anos.

![alt tag](https://cdn-images-1.medium.com/max/1600/1*fUKUEUeqgIYU9xlxj4pwhw.png)
