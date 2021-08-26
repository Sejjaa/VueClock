<template>
{{CreateHours()}}
</template>


<script>
import $ from 'jquery';

export default{

methods:{

	CreateHours(){
		var clock=$('#clock');
		clock.append('<div id="HoursCricle"></div> ');
		var HoursCricle=$('#HoursCricle');
		HoursCricle.css({width:'50px',height:'50px',background:'black',position:'absolute',
		borderRadius:'50%',marginTop:'225px',marginLeft:'225px'	
		});

		HoursCricle.append('<div id="HoursPointer"></div> ');
		var HoursPointer=$('#HoursPointer');
		HoursPointer.css({ position:'absolute',width:'10px',height:'120px',background:'orange',left:'20px',top:'20px'  });

		HoursCricle.css({transform:'rotateZ(180deg)'})
	}

}

}



</script>