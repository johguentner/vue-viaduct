<template>
	<div class="w-full h-full p-20 bg-gray-800">
		<div class="p-10 overflow-hidden bg-white rounded-2xl">
			<div class="flex items-center justify-between">
				<div class="text-5xl font-thin">vue-aqueduct</div>
				<div class="pr-3 text-5xl font-thin">
					<a href="https://github.com/johguentner/vue-aqueduct" target="_blank"
						><svg
							
							xmlns="http://www.w3.org/2000/svg"
							xmlns:xlink="http://www.w3.org/1999/xlink"
							aria-hidden="true"
							focusable="false"
							width="1.03em"
							height="1em"
							style="
								-ms-transform: rotate(360deg);
								-webkit-transform: rotate(360deg);
								transform: rotate(360deg);
							"
							preserveAspectRatio="xMidYMid meet"
							viewBox="0 0 256 250"
						>
							<path
								d="M128.001 0C57.317 0 0 57.307 0 128.001c0 56.554 36.676 104.535 87.535 121.46c6.397 1.185 8.746-2.777 8.746-6.158c0-3.052-.12-13.135-.174-23.83c-35.61 7.742-43.124-15.103-43.124-15.103c-5.823-14.795-14.213-18.73-14.213-18.73c-11.613-7.944.876-7.78.876-7.78c12.853.902 19.621 13.19 19.621 13.19c11.417 19.568 29.945 13.911 37.249 10.64c1.149-8.272 4.466-13.92 8.127-17.116c-28.431-3.236-58.318-14.212-58.318-63.258c0-13.975 5-25.394 13.188-34.358c-1.329-3.224-5.71-16.242 1.24-33.874c0 0 10.749-3.44 35.21 13.121c10.21-2.836 21.16-4.258 32.038-4.307c10.878.049 21.837 1.47 32.066 4.307c24.431-16.56 35.165-13.12 35.165-13.12c6.967 17.63 2.584 30.65 1.255 33.873c8.207 8.964 13.173 20.383 13.173 34.358c0 49.163-29.944 59.988-58.447 63.157c4.591 3.972 8.682 11.762 8.682 23.704c0 17.126-.148 30.91-.148 35.126c0 3.407 2.304 7.398 8.792 6.14C219.37 232.5 256 184.537 256 128.002C256 57.307 198.691 0 128.001 0zm-80.06 182.34c-.282.636-1.283.827-2.194.39c-.929-.417-1.45-1.284-1.15-1.922c.276-.655 1.279-.838 2.205-.399c.93.418 1.46 1.293 1.139 1.931zm6.296 5.618c-.61.566-1.804.303-2.614-.591c-.837-.892-.994-2.086-.375-2.66c.63-.566 1.787-.301 2.626.591c.838.903 1 2.088.363 2.66zm4.32 7.188c-.785.545-2.067.034-2.86-1.104c-.784-1.138-.784-2.503.017-3.05c.795-.547 2.058-.055 2.861 1.075c.782 1.157.782 2.522-.019 3.08zm7.304 8.325c-.701.774-2.196.566-3.29-.49c-1.119-1.032-1.43-2.496-.726-3.27c.71-.776 2.213-.558 3.315.49c1.11 1.03 1.45 2.505.701 3.27zm9.442 2.81c-.31 1.003-1.75 1.459-3.199 1.033c-1.448-.439-2.395-1.613-2.103-2.626c.301-1.01 1.747-1.484 3.207-1.028c1.446.436 2.396 1.602 2.095 2.622zm10.744 1.193c.036 1.055-1.193 1.93-2.715 1.95c-1.53.034-2.769-.82-2.786-1.86c0-1.065 1.202-1.932 2.733-1.958c1.522-.03 2.768.818 2.768 1.868zm10.555-.405c.182 1.03-.875 2.088-2.387 2.37c-1.485.271-2.861-.365-3.05-1.386c-.184-1.056.893-2.114 2.376-2.387c1.514-.263 2.868.356 3.061 1.403z"
								fill="#161614"
							/>
						</svg>
						</a
					>
				</div>
			</div>
			<div class="flex items-center justify-center mb-10">
				<img alt="Vue logo" src="./assets/logo.png" />
			</div>
			<div class="grid gap-4">
				<div class="p-10 bg-gray-100 rounded-xl">
					<span class="block mb-10 text-4xl font-light text-gray-800"
						>Message Modal</span
					>
					<button class="p-2 text-white bg-gray-700 rounded" @click="test">
						Show Simple Dialog
					</button>
				</div>
				<div class="p-10 bg-gray-100 rounded-xl">
					<div class="grid items-center justify-center grid-cols-2">
						<div>
							<span class="block mb-10 text-4xl font-light text-gray-800"
								>Alerts</span
							>
							<button
								class="block p-2 mb-2 text-white bg-gray-700 rounded"
								@click="$alert.error('blub', 'testing')"
							>
								Show Error
							</button>
							<button
								class="block p-2 mb-2 text-white bg-gray-700 rounded"
								@click="$alert.info('blub', 'testing', 1000)"
							>
								Show Info (+ 1 sec timout)
							</button>
							<button
								class="block p-2 mb-2 text-white bg-gray-700 rounded"
								@click="$alert.plain('blub', 'testing')"
							>
								Show Plain
							</button>
							<button
								class="block p-2 mb-2 text-white bg-gray-700 rounded"
								@click="$alert.success('blub', 'testing')"
							>
								Show Success
							</button>
						</div>
						<div>
							<Alert></Alert>
						</div>
					</div>
				</div>
				<div class="p-10 bg-gray-100 rounded-xl">
					<span class="block mb-10 text-4xl font-light text-gray-800"
						>Message Modal</span
					>
					<button class="p-2 text-white bg-gray-700 rounded" @click="test">
						Show Simple Dialog
					</button>
				</div>
				<div class="flex items-center justify-between px-4 mt-14">
					<div class="flex items-center">
						<img alt="Vue logo" class="mr-3 h-7" src="./assets/logo.png" />
						<a target="_blank" href="https://github.com/johguentner/vue-aqueduct" class="hover:underline">vue-aqueduct</a>
					</div>
					<div>With 💚 From Bavaria - <a target="_blank" href="https://twitter.com/Johannesguent" class="hover:underline">Johannes Güntner</a></div>
				</div>
			</div>
		</div>
	</div>
	<Message> </Message>
</template>

<script lang="ts">
import { Options, Vue } from "vue-class-component";
import HelloWorld from "./components/HelloWorld.vue";
import Message from "../../src/Message.vue";
import VAqueduct from "../../src/vAqueduct";
import Alert from "../../src/Alert.vue";
import Aqueduct from "../../src/aqueduct";
import Prism from "prismjs";

@Options({
	components: {
		HelloWorld,
		VAqueduct,
		Message,
		Alert,
	},
})
export default class App extends Vue {
	counter = 0;

	test() {
		this.$msg
			.title("Modal To Go")
			.plain("What do you think ? 😊")
			.button("Close")
			.button("Approve", "success")
			.then((e, destroy) => {
				if (e == "Close") {
					this.$msg
						.plain("oh no... 😞 ... I'm closing now", 1500)
						.keepButtons();
				} else {
					this.$msg
						.plain(
							"AWESOME! 🤙 \nsee ya later!\n\n\n\n\n\n\n\n\nsecret: this is a modal"
						)
						.button("k bye", "default", "col-span-2")
						.then((e, destroy) => {
							destroy();
						});
				}
			});
		this.counter++;
	}
	mounted() {}
}
</script>


