<template>
	<div class="bruce flex-ct-x" data-title="使用attr()控制切换文本">
		<input id="text-switch" class="text-switch" type="checkbox" hidden>
		<label for="text-switch" data-true="打开" data-false="关闭"></label>
	</div>
</template>

<style lang="scss" scoped>
.text-switch {
	& + label {
		cursor: pointer;
		font-weight: blod;
		font-size: 50px;
		color: #f66;
		&::after {
			content: attr(data-true);
		}
	}
	&:checked + label::after {
		content: attr(data-false);
	}
}
</style>