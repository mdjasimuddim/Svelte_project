<script>
    const countryDataStore = async () => {
        const res = await fetch("https://restcountries.com/v3.1/all");
        const data = await res.json();
        console.log(data);
        return data;
    };
    countryDataStore();
</script>

<div class="w-[1170px]">
    <div class="w-2/3">
        {#await countryDataStore()}
            <p>loading ...</p>
        {:then data}
            <table class="table-auto text-center">
                <tr>
                    <th>Flag</th>
                    <th>Name</th>
                    <th>Population</th>
                    <th>CIOC</th>
                    <th>UN Member Status</th>
                    <th>Currencies</th>
                    <th>Languages</th>
                </tr>
                {#each data as { flags, name, cioc, unMember, population, currencies, languages }}
                    <tr class="py-2">
                        <td class="w-[40px] h-[40px]"
                            ><img src={flags.png} alt="" /></td
                        >
                        <td class="w-[100px]">{name.common}</td>
                        <td>{population}</td>
                        <td>{cioc}</td>
                        <td>{unMember}</td>
                        <td>{currencies}</td>
                        <td>{languages}</td>
                    </tr>
                {/each}
            </table>
        {/await}
    </div>
    <div class="1/3" />
</div>
