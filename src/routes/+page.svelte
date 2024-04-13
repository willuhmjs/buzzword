<script lang="ts">
    import { faker } from '@faker-js/faker';

    let b: string[] = [];

    const buzzwords = () => {
        b=[];
        for (let i = 0; i < 100; i++) {
            b.push(faker.company.buzzPhrase())
        }   
    }
    buzzwords()
</script>

<button on:click={() => buzzwords()}>Generate 100 Buzzphrases</button>

<p>We must {b[0]} and {b[1]} in order to {b[2]} and {b[3]}, which will allow us to {b[4]} in order to {b[5]} and ultimately {b[6]}</p>

{#each b as buzzword}
    <p>{buzzword}</p>
{/each}