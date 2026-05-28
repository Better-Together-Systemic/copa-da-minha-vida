# Como publicar o álbum na Vercel (passo a passo)

O arquivo `index.html` é o seu álbum pronto. Você vai colocá-lo na Vercel e receber um link para compartilhar.

Pense assim: a Vercel é como uma **banca de revistas online**. Você entrega o "molde" do álbum uma vez, e qualquer pessoa que receber o link pega a sua própria cópia em branco para preencher — sem atrapalhar a de ninguém.

---

## Deploy pelo GitHub (recomendado)

Repositório: `Better-Together-Systemic/copa-da-minha-vida`

O `index.html` principal fica na **raiz** do repositório (a Vercel serve esse arquivo em `/`).

Na tela **New Project** da Vercel:

| Campo | Valor correto |
|-------|----------------|
| **Root Directory** | `./` — clique em **Edit**, confirme a raiz e em **Continue** |
| **Framework Preset** | **Other** |
| **Build and Output Settings** | expanda esta seção (importante) |
| **Build Command** | ative **Override**, deixe **vazio** |
| **Output Directory** | ative **Override**, deixe **vazio** ou `.` |

Depois de clicar em **Deploy**, o site fica em algo como `https://copadaminhavida.vercel.app`.

### Botão Deploy desabilitado (cinza)

Se o botão **Deploy** não clica, tente nesta ordem:

1. **Root Directory** — clique em **Edit** ao lado de `./`, selecione a pasta raiz do repo e confirme com **Continue** (só mostrar `./` às vezes não basta).
2. **Build and Output Settings** — expanda, preset **Other**, **Override** no Build Command ligado e campo vazio.
3. **Nome do projeto** — use só letras minúsculas, ex.: `copadaminhavida` (sem caracteres especiais).
4. **Acesso da Vercel ao GitHub** — em [github.com/settings/installations](https://github.com/settings/installations), abra **Vercel** → **Configure** → em **Organization access**, libere **Better-Together-Systemic** (ou reinstale o app da Vercel no org).
5. Atualize a página depois de dar `git push` no repositório.

### Alternativa sem GitHub (sempre funciona)

1. Abra [vercel.com/new](https://vercel.com/new)
2. Na parte de baixo, use **Deploy without Git** / arraste uma pasta
3. Arraste uma pasta que contenha só o `index.html`
4. Em segundos você recebe o link

---

## Jeito mais fácil: arrastar e soltar (não precisa instalar nada)

1. Entre em **https://vercel.com** e crie uma conta gratuita (pode usar o login do Google).

2. No painel, clique em **"Add New..."** e depois em **"Project"**.

3. Procure a opção de **"Deploy"** por upload manual. Se não achar de cara, use o atalho direto:
   **https://vercel.com/new** — e procure por **"deploy a template"** ou arraste a pasta.

   > Dica: a forma mais garantida de arrastar-e-soltar é colocar o `index.html` sozinho dentro de uma **pasta** (ex.: uma pasta chamada `copa-da-minha-vida`) e arrastar a **pasta inteira** para a área de upload da Vercel.

4. A Vercel vai processar em alguns segundos e te dar um link parecido com:
   `https://copa-da-minha-vida.vercel.app`

5. Pronto! Esse é o link que você compartilha. Cada pessoa que abrir faz o seu próprio álbum.

---

## Alternativa ainda mais simples (sem conta na Vercel): Netlify Drop

Se a Vercel parecer complicada, o **Netlify Drop** é literalmente arrastar:

1. Entre em **https://app.netlify.com/drop**
2. Arraste o arquivo `index.html` (ou a pasta com ele) para a tela.
3. Em segundos você recebe um link pronto para compartilhar.

Funciona exatamente igual — é só outra "banca de revistas".

---

## O que cada pessoa precisa saber ao usar

- **Salva sozinho:** o que ela escrever e as fotos que colocar ficam guardados no próprio celular/computador dela.
- **É só dela:** ninguém vê o álbum da outra pessoa.
- **Importante (avise isso):** os dados ficam salvos **só naquele aparelho e naquele navegador**. Se a pessoa:
  - trocar de celular,
  - limpar o histórico/dados do navegador, ou
  - abrir em modo anônimo/privativo,
  ...ela perde o que tinha preenchido.

  Por isso, ao terminar, ela deve tocar em **"Salvar / Imprimir"** e escolher **"Salvar como PDF"**. Esse PDF é a cópia permanente que ela pode guardar e mandar para você.

---

## Atualizar o álbum depois

Se um dia você quiser mudar alguma coisa no álbum, é só me pedir o novo `index.html` e subir de novo na Vercel/Netlify por cima — o link continua o mesmo.
