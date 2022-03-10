# atividade-2-html-CSS
atividade 2 html/css


    <title>Controle Financeiro</title>

    <link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Lato">
    <link rel="stylesheet" href="resources/css/default.css">
    <link rel="stylesheet" href="resources/css/style.css">
</head>

<body>
@@ -30,7 +30,7 @@ <h1 class="system-title">
                <ul>
                    <li><a href="#">dashboard</a></li>
                    <li><a href="#">resumo</a></li>
                    <li><a href="#">configurações</a></li>
                    <li class="active"><a href="#">configurações</a></li>
                </ul>
            </nav>
        </div>
@@ -41,18 +41,24 @@ <h1 class="system-title">
            <section class="section-new-transaction">
                <h1>Nova transação</h1>
                <form>
                    <label for="transaction-type">Tipo de transação</label>
                    <select name="input-transaction-type" id="transaction-type" required>
                        <option value="1">Compra</option>
                        <option value="2">Venda</option>
                    </select>

                    <label for="name">Nome da mercadoria</label>
                    <input type="text" name="input-name" id="name" placeholder="Digite o nome da mercadoria" required>

                    <label for="price">Valor (R$)</label>
                    <input type="number" name="input-price" id="price" min="0.01" step="0.01" placeholder="R$ 0,00" required>
                    <div class="form-input transaction">
                        <label for="transaction-type">Tipo de transação</label>
                        <select name="input-transaction-type" id="transaction-type" required>
                            <option value="1">Compra</option>
                            <option value="2">Venda</option>
                        </select>
                    </div>

                    <div class="form-input product">
                        <label for="name">Nome da mercadoria</label>
                        <input type="text" name="input-name" id="name" placeholder="Digite o nome da mercadoria" required>
                    </div>

                    <div class="form-input price">
                        <label for="price">Valor (R$)</label>
                        <input type="number" name="input-price" id="price" min="0.01" step="0.01" placeholder="R$ 0,00" required>
                    </div>

                    <button type="submit" class="buy-button">Adicionar transação</button>
                </form>
            </section>
@@ -79,8 +85,8 @@ <h1>Extrato de transações</h1>
                    <tfoot>
                        <tr>
                            <th></th>
                            <th><em>Total</em></th>
                            <th><em>R$ <sub>[lucro]</sub></em></th>
                            <th>Total</th>
                            <th><em>R$ [lucro]</em></th>
                        </tr>
                    </tfoot>
                </table>
                .brand{
    background-image: url(../midia/logo-viavarejo.svg);
    background-size: cover;
    width: 210px;
    width: 150px;
    height: 33px;
    background-position: 50%;
    height: 2.75em;
}

.system-title{
@@ -106,6 +106,11 @@ img{
    flex-direction: column;
}

.section-new-transaction form .form-input{
    display: flex;
    flex-direction: column;
}

.section-new-transaction {
    width: 33%;
    padding: 1em;
@@ -166,9 +171,14 @@ img{
}

.table-transaction-statement tfoot th{
    font-style: normal;
    border-top: 4px double #aaa;
}

.table-transaction-statement tfoot em{
    font-style: normal;
}

.section-transaction-statement td:first-child,
.section-transaction-statement th:first-child,
.section-transaction-statement td:last-child,
@@ -204,6 +214,11 @@ img{
        flex-grow: 1;
    }

    .system-title{
        margin: 0 auto;
        font-size: 1.5em;
    }

    .main-content .container{
        flex-direction: column;
    }
@@ -218,12 +233,11 @@ img{
        flex-direction: column;

        background: #000;
        padding: 1em;
        margin: 0;

        height: 100%;
        width: 90%;
        max-width: 300px;
        max-width: 250px;

        position: fixed;
        z-index: 1;
@@ -244,14 +258,26 @@ img{
    }

    .navbar-menu li{        
        padding: 1em 0;
        padding: 0.5em 1em;
        width: 100%;
    }

    .navbar-menu li {
        border-left: none;
    }

    .navbar-menu li:nth-child(2) {
        order: -1;
    }

    .navbar-menu .active {
        background-color: #ccc;
    }

    .navbar-menu .active a {
        color: #222;
    }

    .active-menu::after{
        content: "";
        display: block;
@@ -275,13 +301,50 @@ img{
    }
}

@media (min-width: 684px) and (max-width: 880px){
    .section-new-transaction{
        margin-bottom: 1.125em;
    }

    .section-new-transaction form {
        flex-flow: row wrap;
        justify-content: flex-end;
    }

    .section-new-transaction form button {
        padding: 0.5em 2em;
    }

    .form-input{
        margin-left: 0.5em;  
        flex-grow: 1;      
    }

    .form-input:first-child,
    .form-input:last-child{
        margin-left: 0;
    }

    .transaction,
    .price{
        flex-basis: 15%;
    }

    .product{
        flex-basis: 40%;
    }
}

@media (max-width:540px){

    .container{
        padding: 0.5em;
    }

    .brand{
        background-image: url(../midia/logo-viavarejo-mobile.svg);
        width: 120px;
        background-position: 50%;
        height: 68px;
        width: 80px;
        height: 40px;
    }

    .section-new-transaction h1{
@@ -299,6 +362,18 @@ img{
    }
}

@media (max-width:345px){
    .brand{
        width: 60px;
        height: 30px;
    }

    .system-title{
        font-size: 1.125em;
    }

}

/* mobile menu */ 
.open-menu,
.close-menu{
@@ -326,6 +401,7 @@ img{
    position: relative;
    height: 1em;
    width: 1em;
    margin: 0.375em;
}

.close-menu::before{
