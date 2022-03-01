<main>
    <div class="container">
        <select name="actors" id="actors-select" class="selector">
            <option value="Apple">Apple</option>
            <option value="Banana">Banana</option>
            <option value="Oranhe">Oranhe</option>
        </select>
        <button class="button-searcher">Search</button>
    </div>
</main>
<style>
    .container {
        width: 100%;
        height: auto;
        text-align: center;
    }
    .selector {
        width: 70%;
        border-radius: 10px;
        padding: 5px;
        font-size: 14px;

        color: #333;
    }
    .button-searcher {
        height: auto;
        border-radius: 10px;
        background-color: #00008b;
        padding: 5px;
        font-size: 14px;
        margin-left: auto;
        color: white;
        border: none;
        width: 20%;
        transition: .8s;

    }
    .button-searcher:hover {
        background-color: #0101c7;
    }
</style>