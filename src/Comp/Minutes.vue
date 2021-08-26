<template>
{{CreateMinutes()}}
</template>


<script>
import $ from 'jquery';

export default{

methods:{

	CreateMinutes(){
		var clock=$('#clock');
		clock.append('<div id="MinutesCricle"></div> ');
		var MinutesCricle=$('#MinutesCricle');
		MinutesCricle.css({width:'50px',height:'50px',background:'black',position:'absolute',
		borderRadius:'50%',marginTop:'225px',marginLeft:'225px'	
		});

		MinutesCricle.append('<div id="MinutesPointer"></div> ');
		var MinutesPointer=$('#MinutesPointer');
		MinutesPointer.css({ position:'absolute',width:'10px',height:'150px',background:'blue',left:'20px',top:'20px'  });

		MinutesCricle.css({transform:'rotateZ(180deg)'})
	}

}

}



</script>