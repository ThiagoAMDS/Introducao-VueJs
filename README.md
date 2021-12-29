<h1> Código final do curso de introdução ao VueJs


<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>

<body>
    <div id="app">

        {{messageCount}}

        <button @click="count++">contador</button>
    </div>
    <script src="https://cdn.jsdelivr.net/npm/vue@2.6.14"></script>
    <script>
        //Todos os componentes que foram gerados durante a aplicação serão "filhos" de app
        const app = new Vue({
            el: "#app",
            data: {
                message: "Hello DIO",
                count: 0,
            },
            computed: {
                messageCount() {
                    return `${this.message} - ${this.count}`;
                }

            }
        });
    </script>
</body>

</html>