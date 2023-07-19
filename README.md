1. Первый фрагмент не будет работать, так как функция doubleNum определена с помощью стрелочной функции и не поднимается наверх своей области видимости, тогда как во втором фрагменте, функция определена через function, которая поднимается наверх своей области видимости, поэтому её можно вызывать с помощью console.log и ошибки не будет.

2. 
```
	<template>
		<component-name
			v-for="i of count" 
			:key="i"
			v-if="i < 10" 
		/>
	</template>

	<script>
	export default {
		data() {
			return {
				count: 20
			};
		},
	};
	</script>  
```

3. 
```
function getResourcesObject(resources) {
  const resultObj = {};

  resources.forEach((resource) => {
    resultObj[resource.id] = resource.count;
  });

  return resultObj;
}
```
