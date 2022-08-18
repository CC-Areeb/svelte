<script>
    export let offer;
    export let price;
    export let ModalShow = false;
    export let isPromo = false;
</script>



<!-- <div class="show-modal">
    <button type="submit">
        Show offers
    </button>
</div> -->



{#if ModalShow}
    <div class="modal-backdrop" class:promo={isPromo} on:click>
        <div class="modal-preview">
            <p>
                {offer}
            </p>

            <p class="amount-of-offers">
                {price}
            </p>

            <button class="sign-up-btn">
                sign-up
            </button>
        </div>
    </div>
{/if}





<style>
    .modal-backdrop
    {
        width: 100%;
        height: 100%;
        position: fixed;
        background: rgba(0, 0, 0, 0.7);
    }
    .modal-preview
    {
        padding: 10px;
        border-radius: 10px;
        max-width: 400px;
        margin: 10% auto;
        text-align: center;
        background: whitesmoke;
    }

    .sign-up-btn
    {
        color: white;
        background-color: forestgreen;
        font-size: 1.5rem;
    }

    .promo .modal-preview
    {
        background: darkcyan;
        color: whitesmoke;
    }

    p
    {
        font-size: 2rem;
    }

    .amount-of-offers
    {
        background: crimson;
        margin: 20px 160px;
        border-radius: 50%;
    }

    .show-modal
    {
        text-align: center;
        margin-top: 6rem;
    }
</style>
