<template>
{{EditAll()}}  


 <SecoundsApp></SecoundsApp>
 <MinutesApp />
 <Hours />
</template>

<script>
import $ from 'jquery';
import SecoundsApp from "./Comp/Secounds";
import MinutesApp from "./Comp/Minutes";  
import Hours from "./Comp/Hours";  

export default{

components:{
  SecoundsApp,
  MinutesApp,
  Hours
},


data(){
  return{

    maxRotation:359,
    minRotation:1,
    rotation1:180,
    rotation2:180,
    rotation3:180,
    MidRotation:179,
  }

},


methods:{

  EditAll(){
    let body=$('body');
    body.css({background:'violet'})
    body.append('<div id="clock"></div>');
    setTimeout( ()=>{

      var SecoundsCricle=$('#SecoundsCricle');
      var MinutesCricle=$('#MinutesCricle');
      var HoursCricle=$('#HoursCricle');
      
      setInterval( ()=>{
        this.rotation1++;
        SecoundsCricle.css({transform:'rotateZ('+this.rotation1+'deg)'});

        if(this.rotation1==this.maxRotation){
          this.rotation1=this.minRotation;
        }if(this.rotation1==this.MidRotation){
          this.rotation2++;
          console.log(this.rotation1)
          if(this.rotation2==this.maxRotation){
            this.rotation2==this.minRotation;
        }
          MinutesCricle.css({transform:'rotateZ('+this.rotation2+'deg)'});

        

        }if(this.rotation2==this.MidRotation){
          this.rotation3++;
          if(this.rotation3==this.maxRotation){
            this.rotation3==this.minRotation;
          }
          HoursCricle.css({transform:'rotateZ('+this.rotation3+'deg)'});
        }


      },0 );


    },2000 );
  }


}



 
}
</script>

<style>
#clock{
  background-image:url(./Img/clock.jpg); 
  width:500px;
  height:500px;
  margin-left:auto;
  margin-right:auto;
  margin-top:40px;
  background-repeat:no-repeat;
  background-size:cover;

}

</style>
