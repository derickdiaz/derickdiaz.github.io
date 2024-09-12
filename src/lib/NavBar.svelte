<nav>
    <div class="left-nav centered">
        <h1>Derick Diaz</h1>
    </div>
    <div class="right-nav">
        <ul>
            <li class="centered active">Home</li>
            <li class="centered">Contact Me</li>
        </ul>
    </div>
</nav>

<style>
    nav {
        display: flex;
        justify-content: space-between;
        padding: 20px 20px;
        background-color: white;
        filter: drop-shadow(0px 5px 10px lightgray)
    }

    .right-nav > ul {
        display: flex;
        justify-content: space-between;
        gap: 20px;
    }

    .active {
        background-color: #2DA5EB;
        color: white;
    }

    .centered {
        display: flex;
        justify-content: center;
        align-items: center;
    }

    .right-nav > ul > li {
        padding: 10px;
        border-radius: 5px;
        cursor: pointer;
    }

    .right-nav > ul > li:hover {
        background-color: #2DA5EB;
        color: white;
    }

</style>