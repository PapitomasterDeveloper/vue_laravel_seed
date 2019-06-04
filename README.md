# vue_laravel_seed
Initial setup and instructions for setting up Vue with Laravel and working components

# Steps to duplicate on your own
1. Install a composer app via composer or laravel installer
2. Change the privileges to 755 on the main folder app and storage
3. Rename .env.example to .env
4. Generate a new key with php laravel generate:key
5. Run npm install to install all the dependencies in the npm json file
6. Run npm run dev to compile all the un-compiled files like sass, less
7. Go to /resources/views and open the welcome blade file and paste the following code in the bottom part in the last div class="container"

    <div id="app">
      <example-component></example-component>
		</div>

		<script src="{{ asset('js/app.js') }}" ></script>

8. Run again to compile changes npm run dev
9. You can also run npm run watch-poll to watch for changes and a one time command run
10. To add new components, go to /resources/js and open app.js, declare your components on the same way as example-component is declared

    Vue.component('example-component', require('./components/ExampleComponent.vue').default);

11. Play with it an be happy developing!
