<!DOCTYPE html>
<html>
<head>
    <title>Ton Connect на GitHub Pages</title>
    <script src="https://sdk-wallet.ton.live/tonclient_1.8.0.js"></script>
    <script src="https://sdk-wallet.ton.live/tonclient_1.8.0.module.js"></script>
</head>
<body>
    <h1>Ton Connect на GitHub Pages</h1>

    <button onclick="checkVersion()">Проверить версию Ton Client</button>

    <div id="result"></div>

    <script>
        async function checkVersion() {
            const client = new TonClient({
                network: {
                    server_address: 'https://main.ton.dev/',
                },
            });

            try {
                const version = await client.version();
                document.getElementById("result").textContent = `Подключено к TON Blockchain. Версия клиента: ${version.version}`;
            } catch (error) {
                console.error(error);
                document.getElementById("result").textContent = `Ошибка подключения к TON Blockchain`;
            }
        }
    </script>
</body>
</html>
