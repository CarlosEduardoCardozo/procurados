<script>
    export default {
        props: {
            procurado: {
                type: Object
            }
        }
    }
</script>
<template>
    <div class="previa">
        <div class="img">
            <img :src="procurado.images[0].original">
        </div>
        <div class="infos">
            <h2>ABDELKARIM HUSSEIN MOHAMED AL-NASSER</h2>
            <p>Conspiracy to Kill U.S. Nationals; Conspiracy to Murder U.S. Employees; Conspiracy to Use Weapons of Mass Destruction Against U.S. Nationals; Conspiracy to Destroy Property of the U.S.; Conspiracy to Attack National Defense Utilities; Bombing Resulting in Death; Use of Weapons of Mass Destruction Against U.S. Nationals; Murder While Using Destructive Device During a Crime of Violence; Murder of Federal Employees; Attempted Murder of Federal Employees</p>
        </div>
        <div class="ttimg">
            <img src="../img/tt.png" alt="">
        </div>
        
    </div>
</template>