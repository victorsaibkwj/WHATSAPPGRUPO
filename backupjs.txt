const gruposWhatsapp = [
  {
    titulo: "🚀 WHATSAPP GRUPOS",
    descricao: "GRUPO DE CARIACICA ES.",
    link: "https://chat.whatsapp.com/FITyBYWMqtd3QHOZpDorMA"
  },

];

document.addEventListener("DOMContentLoaded", () => {
  const container = document.getElementById("grupos");

  gruposWhatsapp.forEach(grupo => {
    const div = document.createElement("div");
    div.classList.add("grupo");

    div.innerHTML = `
      <h2>${grupo.titulo}</h2>
      <p>${grupo.descricao}</p>
      <a href="${grupo.link}" target="_blank" rel="noopener noreferrer">Entrar no grupo</a>
    `;

    container.appendChild(div);
  });
});
