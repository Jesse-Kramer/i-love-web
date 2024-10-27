<script>
    export let messages = [];
</script>
  
<section class="message-app">
    {#each messages as message}
        {#if message.type === 'incoming'}
        <p class="incoming">{@html message.text}</p>
        {/if}
        {#if message.type === 'outgoing'}
        <p class="outgoing">
            {@html message.text}
        </p>
        {/if}
        {#if message.type === 'status'}
        <p class="status">{message.text}</p>
        {/if}
    {/each}
</section>
  