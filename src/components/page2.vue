<template>
	<div class="container">
		<div class="row justify-content-center">
			<h4>Выводим комментарии</h4>
		</div>

		<div class="row">
			<div class="col-4 text-center">
				<div class="title">
					<h5>Name</h5>
					<div class='comm'>
						<h5>Email</h5>
						<p>Message</p>
					</div>
				</div>
				
			</div>
		</div>
	</div>
</template>

<style scoped>
.title {
	background-color: #4b596c;
	color: white;
	border-top-left-radius: 5px;
	border-top-right-radius: 5px; 
}
.title h5 {
	padding: 5px;
}
.comm {
	background-color: #e9eef3;
	color: #4b596c
}
.comm h5 {
	padding: 10px;
}
.comm p {
	padding-bottom: 60px;
}

</style>
