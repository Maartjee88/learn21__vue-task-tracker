<template>
  <div class="container">
    <Header title="Tast Tracker" />
    <Tasks :tasks="tasks"/>

    <a href="https://youtu.be/qZXt1Aom3Cs?t=2453">Verder kijken</a>
  </div>
</template>

<script>
  import Header from './components/Header'
  import Tasks from './components/Tasks'

  export default {
    name: "App",
    components: {
      Header,
      Tasks
    },
    data() {
      return {
        tasks: []
      }
    },
    created() {
      this.tasks = [
        {
          id: 1,
          text: 'Corgi petting',
          day: ' March 19th at 11:00am',
          reminder: true,
        },
        {
          id: 2,
          text: 'Crossfit training',
          day: 'March 19th at 5pm',
          reminder: true,
        },
        {
          id: 3,
          text: 'Portfolio live',
          day: 'March 20th at 12pm',
          reminder: false,
        },
      ]
    }
  };
</script>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400&display=swap');

  * {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }

  body {
    font-family: 'Poppins', sans-serif;
  }

  .container {
    max-width: 500px;
    margin: 30px auto;
    overflow: auto;
    min-height: 300px;
    border: 1px solid teal;
    padding: 30px;
    border-radius: 5px;
  }

  .btn {
    display: inline-block;
    background: #000;
    color: #fff;
    border: none;
    padding: 10px 20px;
    margin: 5px;
    border-radius: 5px;
    cursor: pointer;
    text-decoration: none;
    font-size: 15px;
    font-family: inherit;
  }

  .btn:focus {
    outline: none;
  }

  .btn:active {
    transform: scale(0.98);
  }

  .btn-block {
    display: block;
    width: 100%;
  }
</style>
