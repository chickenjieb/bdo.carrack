<template>
  <div class="birdForm">
    <h1>Epheria Carrack : Advance</h1>
    <h5>เรือคาร์แร็คเอเฟเรีย : ทนทาน</h5>
    <div class="container py-3">
        <div id="fill">
            <table id="birdTable" class="table table-dark">
                <thead>
                    <tr class="row mx-0">
                        <th class="col-6">ไอเทม</th>
                        <th class="col-2">ต้องการ</th>
                        <th class="col-2">มีอยู่</th>
                        <th class="col-2">ขาดอีก</th>

                    </tr>
                </thead>
                <tbody>
                    <tr class="row mx-0" v-for="material in allMaterials">
                        <td class="col-6 text-left" :class="material.level"><img :src="material.image" :class="material.level" style="margin-right:10px;">{{ material.name }}</td>
                        <td class="col-2">{{ material.demand }}</td>
                        <td class="col-2"><input type="number" class="form-control" v-model="material.supply"></td>
                        <td class="col-2">{{ material.demand - material.supply }}</td>
                    </tr>
                </tbody>
            </table>

            <div>จำนวนเหรียญที่ต้องการ : {{ calcPercent.remainCoin }} <img width="30px;" src="https://bdocodex.com/items/new_icon/00000010_special.png"></div>

            <div class="progress my-3">
                <div class="progress-bar progress-bar-striped bg-success progress-bar-animated" role="progressbar" :aria-valuenow="calcPercent.percent" aria-valuemin="0" aria-valuemax="100" :style="calcPercent.percentStyle">
                    {{calcPercent.percent}}% Complete
                </div>
            </div>


        </div>
    </div>

  </div>
</template>

<script>

export default {
    name: 'HorseForm',
    props: {
    // cmsg: String
    },
    data(){
        return{
            allMaterials:[
                {id:1, name:'ลำต้นพืชทะเลลึก', level:'green', demand:205, supply:0, coin:600, image:'https://bdocodex.com/items/new_icon/03_etc/07_productmaterial/00005829.png'},
                {id:2, name:'แร่ใต้มหาสมุทรสีเลือดฝาด', level:'gold', demand:90, supply:0, coin:1500, image:'https://bdocodex.com/items/new_icon/03_etc/07_productmaterial/00005807.png'},

                {id:3, name:'วัตถุโบราณกลุ่มโจรสลัดค็อกซ์ (ระดับต่ำ)', level:'green', demand:60, supply:0, coin:150, image:'https://bdocodex.com/items/new_icon/03_etc/07_productmaterial/00005822.png'},
                {id:4, name:'วัตถุโบราณกลุ่มโจรสลัดค็อกซ์ (ระดับสูง)', level:'blue', demand:30, supply:0, coin:800, image:'https://bdocodex.com/items/new_icon/03_etc/07_productmaterial/00005823.png'},
                {id:5, name:'วัตถุโบราณกลุ่มโจรสลัดค็อกซ์ (ต่อสู้)', level:'gold', demand:120, supply:0, coin:800, image:'https://bdocodex.com/items/new_icon/03_etc/07_productmaterial/00005824.png'},

                {id:6, name:'ไม้อัดต้นแกะเสริมประสิทธิภาพ', level:'green', demand:300, supply:0, coin:80, image:'https://bdocodex.com/items/new_icon/03_etc/07_productmaterial/00005814.png'},
                {id:7, name:'ไม้อัดเกล็ดพระจันทร์', level:'blue', demand:400, supply:0, coin:160, image:'https://bdocodex.com/items/new_icon/03_etc/07_productmaterial/00005827.png'},
                {id:8, name:'ไม้แปรรูปที่เต็มไปด้วยสีคราม', level:'blue', demand:180, supply:0, coin:350, image:'https://bdocodex.com/items/new_icon/03_etc/07_productmaterial/00005810.png'},
                {id:9, name:'ไม้แปรรูปที่เต็มไปด้วยสีครามเข้ม', level:'gold', demand:144, supply:0, coin:1000, image:'https://bdocodex.com/items/new_icon/03_etc/07_productmaterial/00005812.png'},

                {id:10, name:'เหล็กเเห่งมหาสมุทรที่แข็งแกร่ง', level:'green', demand:150, supply:0, coin:160, image:'https://bdocodex.com/items/new_icon/03_etc/07_productmaterial/00005832.png'},

                {id:11, name:'แท่งทองสีโคบอลด์เปร่งประกาย', level:'blue', demand:30, supply:0, coin:800, image:'https://bdocodex.com/items/new_icon/03_etc/07_productmaterial/00005830.png'},
                {id:12, name:'แท่งหินเกลือเจิดจรัส', level:'gold', demand:35, supply:0, coin:1600, image:'https://bdocodex.com/items/new_icon/03_etc/07_productmaterial/00005815.png'},

                {id:13, name:'ผ้าลินินที่มีเส้นเลือดของพระจันทร์สลักอยู่', level:'gold', demand:180, supply:0, coin:600, image:'https://bdocodex.com/items/new_icon/03_etc/07_productmaterial/00005809.png'},

                {id:14, name:'น้ำตาแห่งทะเลลึก', level:'orange', demand:42, supply:0, coin:3900, image:'https://bdocodex.com/items/new_icon/03_etc/07_productmaterial/00005821.png'},

                {id:15, name:'ชิ้นส่วนหินโสโครกกระจ่างใส', level:'green', demand:180, supply:0, coin:140, image:'https://bdocodex.com/items/new_icon/03_etc/07_productmaterial/00005828.png'},

                {id:16, name:'อัญมณีมุกที่บริสุทธิ์', level:'blue', demand:45, supply:0, coin:550, image:'https://bdocodex.com/items/new_icon/03_etc/07_productmaterial/00005820.png'},
                {id:17, name:'อัญมณีมุกเจิดจรัส', level:'gold', demand:35, supply:0, coin:1600, image:'https://bdocodex.com/items/new_icon/03_etc/07_productmaterial/00005831.png'},

            ],
        }
    },
    computed:{
        calcPercent: function(){
            console.log('changed');
            var percent = 0;
            var sumAllCoin = 0;
            var existingCoin = 0;
            var result = {};
            for(var i=0; i<this.allMaterials.length; i++){
                var supply = parseInt(this.allMaterials[i].supply);
                var demand = parseInt(this.allMaterials[i].demand);
                var coin = parseInt(this.allMaterials[i].coin);

                sumAllCoin += demand * coin;
                existingCoin += supply * coin;
            }
            result.remainCoin = (sumAllCoin - existingCoin).toLocaleString('en');
            result.percent = ((existingCoin/sumAllCoin) * 100).toFixed(2);
            result.percentStyle = 'width:' + result.percent + '%';

            return result;
        }
    }
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
