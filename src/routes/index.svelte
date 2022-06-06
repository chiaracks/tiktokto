<script>
    var feld1 = "";
    var feld2 = "";
    var feld3 = "";
    var feld4 = "";
    var feld5 = "";
    var feld6 = "";
    var feld7 = "";
    var feld8 = "";
    var feld9 = "";

    var spieler = 1
    var winner = ""
    var zuge = 0
    $: console.log(zuge)

    function jonas(){
        spieler = 1
        zuge =0
        winner = ""
         feld1 = "";
         feld2 = "";
         feld3 = "";
         feld4 = "";
         feld5 = "";
         feld6 = "";
         feld7 = "";
         feld8 = "";
         feld9 = "";
    }

    function name(feld){
        var penis = zuge
        zuge = penis + 1
        if(feld === "feld1") {
            feld1 = (spieler === 1 ? "𓂺" : "𓃸")
        }
        if(feld === "feld2") {
            feld2 = (spieler === 1 ? "𓂺" : "𓃸")
            
        }
        if(feld === "feld3") {
            feld3 = (spieler === 1 ? "𓂺" : "𓃸")
        }
        if(feld === "feld4") {
            feld4 = (spieler === 1 ? "𓂺" : "𓃸")
        }
        if(feld === "feld5") {
            feld5 = (spieler === 1 ? "𓂺" : "𓃸")
        }

        if(feld === "feld6") {
            feld6 = (spieler === 1 ? "𓂺" : "𓃸")
        }
        if(feld === "feld7") {
            feld7 = (spieler === 1 ? "𓂺" : "𓃸")
        }
        if(feld === "feld8") {
            feld8 = (spieler === 1 ? "𓂺" : "𓃸")
        }
        if(feld === "feld9") {
            feld9 = (spieler === 1 ? "𓂺" : "𓃸")
        }
        if(spieler === 1) {spieler = 2} else {spieler = 1}

        if(feld1 === "𓃸" && feld2 === "𓃸" && feld3 === "𓃸") {winner = "𓃸"}
        if(feld1 === "𓃸" && feld4 === "𓃸" && feld7 === "𓃸") {winner = "𓃸"}
        if(feld1 === "𓃸" && feld5 === "𓃸" && feld9 === "𓃸") {winner = "𓃸"}
        if(feld3 === "𓃸" && feld6 === "𓃸" && feld9 === "𓃸") {winner = "𓃸"}
        if(feld3 === "𓃸" && feld5 === "𓃸" && feld7 === "𓃸") {winner = "𓃸"}
        if(feld7 === "𓃸" && feld8 === "𓃸" && feld9 === "𓃸") {winner = "𓃸"}
        if(feld2 === "𓃸" && feld5 === "𓃸" && feld8 === "𓃸") {winner = "𓃸"}
        if(feld4 === "𓃸" && feld5 === "𓃸" && feld6 === "𓃸") {winner = "𓃸"}

        if(feld1 === "𓂺" && feld2 === "𓂺" && feld3 === "𓂺") {winner = "𓂺"}
        if(feld1 === "𓂺" && feld4 === "𓂺" && feld7 === "𓂺") {winner = "𓂺"}
        if(feld1 === "𓂺" && feld5 === "𓂺" && feld9 === "𓂺") {winner = "𓂺"}
        if(feld3 === "𓂺" && feld6 === "𓂺" && feld9 === "𓂺") {winner = "𓂺"}
        if(feld3 === "𓂺" && feld5 === "𓂺" && feld7 === "𓂺") {winner = "𓂺"}
        if(feld7 === "𓂺" && feld8 === "𓂺" && feld9 === "𓂺") {winner = "𓂺"}
        if(feld2 === "𓂺" && feld5 === "𓂺" && feld8 === "𓂺") {winner = "𓂺"}
        if(feld4 === "𓂺" && feld5 === "𓂺" && feld6 === "𓂺") {winner = "𓂺"}

        if(zuge >= 9) {winner = "Niemand "}

    }
</script>

<h1><strong>ich liebé JONAS UND WILL SCHLAFEN</strong></h1>
<h2>GEWINNER: {winner}</h2>

<div class="game-board">
    <div on:click={() => name("feld1")} class="box">{feld1}</div>
    <div on:click={() => name("feld2")} class="box">{feld2}</div>
    <div on:click={() => name("feld3")} class="box">{feld3}</div>
    <div on:click={() => name("feld4")} class="box">{feld4}</div>
    <div on:click={() => name("feld5")} class="box">{feld5}</div>
    <div on:click={() => name("feld6")} class="box">{feld6}</div>
    <div on:click={() => name("feld7")} class="box">{feld7}</div>
    <div on:click={() => name("feld8")} class="box">{feld8}</div>
    <div on:click={() => name("feld9")} class="box">{feld9}</div>
  </div>
<button on:click={jonas}>start</button>

  <style>
    .game-board
        {
        width: 90vw;
        height: 70vh;
        margin: 0 auto;
        background-color: #34495e;
        color: #fff;
        border: 6px solid #2c3e50;
        border-radius: 10px;
            
        display: grid;
        grid-template: repeat(3, 1fr) / repeat(3, 1fr);
        }

    .box
        {
        border: 6px solid #2c3e50;
        border-radius: 2px;
        font-family: Helvetica;
        font-weight: bold;
        font-size: 4em;
        display: flex;
        justify-content: center;
        align-items: center;
        }
    button{
        font-size: x-large;
        padding: 30px;
        background-color: #2c3e50;
        border-radius: 10px;
        color: white;
        font-weight: 900;
        box-shadow: rgba(0, 0, 0, 0.35) 0px 5px 15px;
        margin-top: 30px;
        margin-left: 30px;
        transition: all 150ms ease-in-out;
    }

    button:hover{
        box-shadow: none;
        padding: 40px;
    }
  </style>