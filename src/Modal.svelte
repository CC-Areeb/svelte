<script>
    let ModalShow = true;
    let isPromo = true;
</script>

{#if ModalShow}
    <div class="modal-backdrop" class:promo={isPromo}>
        <div class="modal-preview">
            <p>
                Sign up for more
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
</style>
