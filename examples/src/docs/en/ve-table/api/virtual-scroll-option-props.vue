<template>
    <div>
        <tpl
            :desc="desc"
            :anchor="anchor"
            :table-data="db.virtualScrollOption.data"
            :columns="db.virtualScrollOption.columns"
        />
    </div>
</template>
<script>
import tpl from "@/comp/api-tpl";
import { db } from "./db";
export default {
    components: { tpl },
    props: {
        anchor: {
            type: String,
            default: "Virtual scroll configuration",
        },
        desc: {
            type: String,
            default: "virtualScrollOption",
        },
    },
    data() {
        return {
            db: db,
        };
    },
};
</script>
