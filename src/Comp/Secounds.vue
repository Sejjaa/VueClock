<template>
{{CreateSecounds()}}
</template>


<script>
import $ from 'jquery';

export default{

methods:{

	CreateSecounds(){
		var clock=$('#clock');
		clock.append('<div id="SecoundsCricle"></div> ');
		var SecoundsCricle=$('#SecoundsCricle');
		SecoundsCricle.css({width:'50px',height:'50px',background:'black',position:'absolute',
		borderRadius:'50%',marginTop:'225px',marginLeft:'225px'	
		});

		SecoundsCricle.append('<div id="SecoundsPointer"></div> ');
		var SecoundsPointer=$('#SecoundsPointer');
		SecoundsPointer.css({ position:'absolute',width:'5px',height:'150px',background:'red',left:'22.5px',top:'22.5px'  });

		SecoundsCricle.css({transform:'rotateZ(180deg)'})
	}

}

}



</script>