<script>
    export let title;
    export let url;
    export let description;
</script>

<div class="text-left my-2">
    <a href={url} target="_blank" class="text-xl">{title}</a>
    <p>{description}</p>
</div>
