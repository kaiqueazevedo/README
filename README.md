# Kaique Azevedo

![Hello](https://user-images.githubusercontent.com/85317897/200672733-db5c25f5-a027-494a-adba-781b8707564d.svg)



<p> Estudante de Analise e Desenvolvimento de sistema</p>

<p> por fora estudo programação Web Full Stack, voltado a Stack em JavaScript, <br>
onde dedico todo o meu tempo nas tecnologias para atender o mercado <p>


<h4>Tecnologias estudadas</h4>

![html](https://user-images.githubusercontent.com/85317897/200671787-680500f5-22c1-42a2-960a-460daefd3412.png)
![css](https://user-images.githubusercontent.com/85317897/200671776-c7c5e937-566f-40c2-917b-26418ceea735.png)
![javascript](https://user-images.githubusercontent.com/85317897/200671790-16ca8ced-275d-4231-9a32-de931e2da65c.png)
![jquery](https://user-images.githubusercontent.com/85317897/200671792-c4e577db-b5af-4306-ac45-b903cc6170b4.png)
<br>
![bootstrap](https://user-images.githubusercontent.com/85317897/200671773-f73aaeff-7bf5-4534-b685-682d4849f55a.png)
![firebase](https://user-images.githubusercontent.com/85317897/200671780-dd08892e-5d3e-4c4e-af91-ae4b6eabd605.png)
![node](https://user-images.githubusercontent.com/85317897/200671797-65ace8aa-5e2b-4768-8676-718466f9e350.png)
![mongo](https://user-images.githubusercontent.com/85317897/200671794-91ca71ff-8130-43cc-8dc4-c434e0b599a8.png)
<br>
![react](https://user-images.githubusercontent.com/85317897/200671800-dfec726d-250f-4cad-898f-cb065f69c3d1.png)
![electron](https://user-images.githubusercontent.com/85317897/200671778-2698f5b7-4806-4e66-aef6-0e8c0b7560d1.png)










<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <title>Jogo Adivinhe o Número</title>
  <style>
    body { font-family: Arial, sans-serif; max-width: 400px; margin: 50px auto; text-align: center; }
    input { padding: 8px; width: 60px; font-size: 16px; }
    button { padding: 8px 12px; font-size: 16px; }
    #resultado { margin-top: 20px; font-weight: bold; }
  </style>
</head>
<body>
  <h1>Jogo: Adivinhe o Número 🎯</h1>
  <p>Tente adivinhar o número secreto entre 1 e 10.</p>
  <p>Você tem <span id="tentativas">3</span> tentativas.</p>

  <input type="number" id="palpite" min="1" max="10" />
  <button onclick="tentar()">Tentar</button>

  <div id="resultado"></div>

  <script>
    const numeroSecreto = Math.floor(Math.random() * 10) + 1;
    let tentativas = 3;

    function tentar() {
      const palpiteInput = document.getElementById('palpite');
      const resultado = document.getElementById('resultado');
      let palpite = Number(palpiteInput.value);

      if (!palpite || palpite < 1 || palpite > 10) {
        resultado.textContent = 'Digite um número entre 1 e 10!';
        return;
      }

      if (palpite === numeroSecreto) {
        resultado.textContent = '🎉 Parabéns! Você acertou!';
        document.getElementById('tentativas').textContent = tentativas;
        palpiteInput.disabled = true;
        return;
      }

      tentativas--;
      if (tentativas === 0) {
        resultado.textContent = `Suas tentativas acabaram! O número era ${numeroSecreto}.`;
        palpiteInput.disabled = true;
        document.getElementById('tentativas').textContent = tentativas;
        return;
      }

      resultado.textContent = `Errado! Tente novamente. Tentativas restantes: ${tentativas}`;
      document.getElementById('tentativas').textContent = tentativas;
      palpiteInput.value = '';
      palpiteInput.focus();
    }
  </script>
</body>
</html>


