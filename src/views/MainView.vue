<!-- eslint-disable prettier/prettier -->
<template>
    <div>
        <h1>
            Daftar nama
        </h1>
      
        <SearchInput 
            :searchAction="search" 
            placeholder="Search by name..." 
        />

        <div class="table">
            <Table 
                :header="DataHeaderTable" 
                :body="DataBodyTable" 
            />
        </div>
    </div>
  </template>
<!-- eslint-disable prettier/prettier -->
<script>
    import SearchInput from "@/components/SearchFilter/SearchFilter.vue";
    import Table from "@/components/Table/Table.vue";

    import DataHeader from "@/assets/variables/DataHeader.json";
    import DataBody from "@/assets/variables/DataBody.json";

    export default {
        name: "HomeView",
        components: {
            SearchInput,
            Table
        },
        data() {
            return {
                DataHeaderTable: DataHeader,
                DataBodyTable: DataBody
            }
        },
        methods: {
            search(e) {
                var data = DataBody.filter(function(item) {
                    return item.name.toLowerCase().includes(e.toLowerCase());
                });

                this.DataBodyTable = data
            },
        }
    };
</script>
<!-- eslint-disable prettier/prettier -->
<style>
    h1 {
        color: #484848;
        font-size: 32px;
        font-weight: 700;
        line-height: 42px;
    }

    .table {
        margin: 20px 0;
    }
</style>