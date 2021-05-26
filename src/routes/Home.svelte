<script>
import TextComponent from "../components/TextComponent.svelte";

export const image = [
        {path: './img/computer.png', id: 'Computer', header: 'Rubrik 1'},
        {path: './img/eagle.png', id: 'Eagle', header: 'Rubrik 2'},
        {path: './img/tree.png', id: 'Tree', header: 'Rubrik 3'}
    ];

    
</script>

<div class="content-wrapper">
 {#each image as img}
    <TextComponent images="{img.path}" header="{img.header}" altText="{img.id}"/>
 {/each}
</div>
