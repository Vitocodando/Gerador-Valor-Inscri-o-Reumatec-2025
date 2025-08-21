<script>
function getURLParameter(name) {
    const urlParams = new URLSearchParams(window.location.search);
    return urlParams.get(name);
}

function calcularValor() {
    const tipo = getURLParameter("tipo");
    const dataAtual = new Date();
    const dataDesconto = new Date("2024-11-10");

    let valor = 0;
    let total = 0

    switch (tipo) {
        case "Médico Sócio da SBR":
            valor = 150;
            desconto = 135;
            break;
        case "Médico Sócio da Simers":
            valor = 150;
            desconto = 135;
            break;
        case "Médico Sócio da SRRS":
            valor = 150;
            desconto = 0;
            break;
        case "Médico Sócio da Amrigs":
            valor = 135;
            desconto = 135;
            break;
        case "Médico não Sócios SBR ou Inadimplentes":
            valor = 180;
            desconto = 162;
            break;
        case "Residentes Sócios da SBR":
            valor = 70;
            desconto = 63;
            break;
        case "Residentes não Sócios/Pós-graduandos":
            valor = 100;
            desconto = 90;
            break;
        default:
            location.href = 'https://reumatologiars.com.br/reumatec/'
            return;
    }


    total = dataAtual < dataDesconto ? desconto : valor;

    document.querySelector("#valor .elementor-heading-title").innerText = `R$${total.toFixed(2)}`;
}

window.onload = calcularValor;

function copiarTexto() {
    const texto = '00020126360014br.gov.bcb.pix0114007169640001305204000053039865802BR5923SOC  REUMATOLOGIA DO RS6012Porto Alegre62160512naoinformado63049BBB';
    navigator.clipboard.writeText(texto)
        .then(() => alert("Conteúdo copiado para a área de transferência!"))
        .catch(err => console.error("Erro ao copiar texto: ", err));
}

document.querySelector("#codigo .elementor-heading-title").addEventListener("click", copiarTexto);
</script>
