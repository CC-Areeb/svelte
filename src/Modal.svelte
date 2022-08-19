<script>
    export let ModalShow = false;
    export let isPromo = false;
</script>




{#if ModalShow}
    <div class="modal-backdrop" class:promo={isPromo} on:click|self>
        <div class="modal-preview">
            <slot name="title"></slot>
            <slot></slot>            
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

    .promo .modal-preview
    {
        background: darkcyan;
        color: whitesmoke;
    }
</style>
