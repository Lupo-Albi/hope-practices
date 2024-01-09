# Descrição

Não é possível salvar as seguintes funções em arquivos de extensão .hop e carregá-las no ambiente Hope por serem funções anônimas, então optei por colocar apenas as contruções delas em um .md mesmo, porque funções anônimas devem ser utilizadas assim que são definidas.

- Sucessor de um número

```hope
>: (\x => x + 1) 1;
>> 2 : num
```

- Quadrado da soma de dois números

```hope
>: (\\(a, b) => pow((a + b), 2)) (1, 9);
>> 100 : num
>:
>: (\a => \b => pow((a + b), 2)) 2 4;
>> 36: num
```

- Cálculo do IMC

```hope
>: (\(p, a) => (p / pow(a, 2))) (85, 1.80);
>> 26.2345679012346 : num
>:
>: (\p => \a => (p / pow(a, 2))) 85 1.80;
>> 26.2345679012346 : num
```
