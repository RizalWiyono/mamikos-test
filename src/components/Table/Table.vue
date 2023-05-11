<!-- eslint-disable prettier/prettier -->
<template>
    <table>
        <thead>
            <tr>
                <th v-for="header in header" :key="header">
                    {{ header  }}
                </th>
            </tr>
        </thead>
        <tbody>
            <tr v-for="(item, index) in body" :key="index">
                <td style="width: 45px; text-align: center;">
                    <img :src="item.photo" :alt="item.name" >
                </td>
                <td>
                    {{ 
                        item.name    
                    }}
                </td>
                <td>
                    {{ 
                        item.age    
                    }}
                </td>
                <td>
                    {{ 
                        item.job    
                    }}
                </td>
            </tr>
        </tbody>
    </table>
</template>
<!-- eslint-disable prettier/prettier -->

<script>
export default {
    name: "TableData",
    props: {
        header: Array,
        body: Array,
    },
};
</script>
<!-- eslint-disable prettier/prettier -->

<style scoped>
    table {
        border-radius: 8px;
        width: 100%;
        background-color: #FFFFFF;
        border-collapse: collapse;
        border-width: 1px;
        border-color: #D3D3D3;
        border-style: solid;
        color: #000000;
    }

    table td, table th {
        border-width: 1px;
        border-color: #D3D3D3;
        border-style: solid;
        padding: 15px;
    }

    table thead {
        background-color: #FFF;
    }

    tbody tr td img {
        width: 40px;
        height: 40px;
        object-fit: cover;
        border-radius: 4px;
    }
</style>