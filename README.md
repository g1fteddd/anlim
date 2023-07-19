1. Первый фрагмент не будет работать, так как функция doubleNum определена с помощью стрелочной функции и не поднимается наверх своей области видимости, тогда как во втором фрагменте, функция определена через function, которая поднимается наверх своей области видимости, поэтому её можно вызывать с помощью console.log и ошибки не будет.

2. В данном фрагменте свойство ```count``` объекта ```data``` инициализировано значением ```20;```, содержащим лишнюю точку с запятой.
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

3. Создаём пустой объект. Проходимся по всем элементам массива resources и добавляем в объект ключ и значение из текущего элемента. И возвращаем объект.
```
function getResourcesObject(resources) {
  const resultObj = {};

  resources.forEach((resource) => {
    resultObj[resource.id] = resource.count;
  });

  return resultObj;
}
```
