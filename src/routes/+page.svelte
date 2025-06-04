<script>
    import { onMount } from 'svelte';
    const weekday = ["SUN","MON","TUE","WED","THU","FRI","SAT"];
    let time = new Date();
    $: hours = getHours(time); 

    const getHours = (date) => {
        let temp = date.getHours()
        if (temp > 12) {
            return temp - 12
        }
        return temp
    }

    onMount(() => {
        const interval = setInterval(() => {
            time = new Date();
        }, 1000)

    })

</script>
<main>
    <h1>Derick Diaz</h1>
    <hr/>
    <div class="content-grid">
        <div class="content-item profile pad-10">
            <div style="text-align: right; padding: 30px;box-sizing:border-box" class="gray">
                <p style="color: white;font-size: 1.5rem;"><span style="color: red">{weekday[time.getDay()]}</span> {time.getDate()}</p>
                <p style="color: white;font-size: 3rem;">{hours}:{time.getMinutes()}</p>
            </div>
        </div>
        <div class="content-item info-grid">
            <div class="content-item pad-10">
                <div class="gray" />
            </div>
            <div class="content-item pad-10">
                <div class="gray" />
            </div>
        </div>
    </div>
</main>

<style>
    h1 {
        color: white;
        font-size: 3rem;
    }

    hr {
        margin-bottom: 30px;
        position: relative;
        /* transform: translateY(-10px); */
    }

    .content-grid {
        /* border: 1px solid white; */
        height: 500px;
        display: grid;
        grid-template-columns: 40% auto;
        gap:10px;
    }

    .content-item {
        /* border: 1px solid white; */
        gap: 10px;
    }

    .info-grid {
        display: grid;
        grid-template-rows: auto auto;
    }

    .gray {
        border: 1px solid gray;
        height: 100%;
        border-radius: 20px;
        transition: all 500ms;
    }

    .gray:hover {
        transform: scale(1.02);
    }
</style>
