<!DOCTYPE html>
<html>
<head>
    <title>Подключение к кошельку с помощью Ton Connect</title>
    <script src="https://sdk-wallet.ton.live/tonclient_1.8.0.js"></script>
    <script src="https://sdk-wallet.ton.live/tonclient_1.8.0.module.js"></script>
</head>
<body>
    <h1>Подключение к кошельку с помощью Ton Connect</h1>

    <div>
        <button onclick="getWalletBalance()">Получить баланс кошелька</button>
    </div>

    <div id="balance"></div>

    <script>
        async function getWalletBalance() {
            const client = new TonClient({
                network: {
                    server_address: 'https://main.ton.dev/',
                },
            });

            try {
                const accounts = await client.queries.accounts.query({ id: { eq: 'UQB-R8y2IWXTX3cjB17BOVHj52y1abHVym1xMD0djeZRROvv' } });
                if (accounts.length > 0) {
                    const balance = accounts[0].balance;
                    document.getElementById("balance").textContent = `Баланс кошелька: ${balance} TON`;
                } else {
                    document.getElementById("balance").textContent = `Кошелек не найден`;
                }
            } catch (error) {
                console.error(error);
                document.getElementById("balance").textContent = `Ошибка при получении баланса`;
            }
        }
    </script>
</body>
</html>
