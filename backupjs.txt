const gruposWhatsapp = [
  {
    titulo: "🚀 WHATSAPP GRUPOS",
    descricao: "GRUPO DE CARIACICA ES.",
    link: "https://chat.whatsapp.com/FITyBYWMqtd3QHOZpDorMA"
  },

];

let indiceAtual = 0;

document.addEventListener("DOMContentLoaded", () => {
  const container = document.getElementById("grupos");
  const botao = document.getElementById("botao-proximo");

  function mostrarGrupo(indice) {
    if (indice < gruposWhatsapp.length) {
      const grupo = gruposWhatsapp[indice];
      const div = document.createElement("div");
      div.classList.add("grupo");
      div.innerHTML = `
        <h2>${grupo.titulo}</h2>
        <p>${grupo.descricao}</p>
        <a href="${grupo.link}" target="_blank" rel="noopener noreferrer">Entrar no grupo</a>
      `;
      container.appendChild(div);
    }
  }

  botao.addEventListener("click", () => {
    if (indiceAtual < gruposWhatsapp.length) {
      mostrarGrupo(indiceAtual);
      indiceAtual++;
    } else {
      botao.disabled = true;
      botao.innerText = "Todos os grupos exibidos";
    }
  });

  // Mostra o primeiro grupo automaticamente
  mostrarGrupo(indiceAtual);
  indiceAtual++;
});
