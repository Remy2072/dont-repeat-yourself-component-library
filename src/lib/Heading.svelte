<script>
    import { Anchor } from "$lib";
</script>

<section class="heading">
    <div class="div1">
        <small>GEORGANISEERDE GASTCOLLEGES</small>
        <h1>We Love Web</h1>
    </div>
    <div class="div2">
        <div class="div3">
            <Anchor
                anchorLink={"#"}
                anchorLabel={"Link naar fdnd.nl"}
                anchorText={"Aankomende"}
                backgroundColor={"var(--green)"}
                padding={"8px 25px"}
            ></Anchor>
        </div>
        <div class="div4">
            <Anchor
                anchorLink={"#"}
                anchorLabel={"Link naar fdnd.nl"}
                anchorText={"Afgelopen"}
                backgroundColor={"var(--yellow)"}
                padding={"8px 30px"}
            ></Anchor>
        </div>
    </div>
</section>

<style>
    section {
        position: relative;
        padding-top: 50px;
    }

    .heading::after {
        content: "";
        width: 100%;
        height: 2px;
        margin-top: 45px;
        background-color: #e9e0e9;
        border-radius: 10px;
        position: absolute;
    }

    .div1 {
    }

    small {
        font-weight: 700;
        font-size: 1rem;
        color: var(--blue);
    }

    h1 {
        font-size: 40px;
        color: var(--blue);
    }

    .div2 {
        margin-top: 14px;
        display: flex;
        justify-content: space-between;
    }

    .div3 {
    }

    .div4 {
    }

    @media (min-width: 768px) {

        section {
            padding-top: 100px;
        }

        .div1 {
            width: fit-content;
        }

        small {
        font-weight: 700;
        font-size: 18px;
    }

        h1 {
        font-size: 80px;
    }

        .div2 {
            display: block;
            position: relative;
        }

        .div3 {
            position: absolute;
            top: -80px;
            right: 140px;
        }

        .div4 {
            position: absolute;
            top: -20px;
            right: 20px;
        }
    }
</style>
