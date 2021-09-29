# Flex-Pannel--Gallery
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Panel</title>
    <link href='https://fonts.googleapis.com/css?family=Amatic+SC' rel='stylesheet' type='text/css'>
</head>
<body>
<style>
    html{
        background: #ffc600;
        font-family:  'Helvetica neue';
        font-size: 20px;
    }
    .panels{
        box-sizing: border-box;
        min-height: 100vh;
        overflow: hidden;
        display: flex;

    }
    *, *:before, *:after {
      box-sizing: inherit;
    }
    .panel{
        background:#6B0F9C;
        color: white;
        text-align: center;
        align-items: center;
        transition: 
            font-size 0.7s cubic-bezier(0.61,-0.19, 0.7,-0.11),
            flex 0.7s cubic-bezier(0.61,-0.19, 0.7,-0.11),
            background 0.2s;
        font-size: 20px;
        background-size: cover;
        background-position: center;
        display: flex;
        justify-content: center;
        flex-direction: column;
        flex: 1;
        



    }
    
    .panel1 { background-image:url(https://source.unsplash.com/gYl-UtwNg_I/1500x1500); }
    .panel2 { background-image:url(https://source.unsplash.com/rFKUFzjPYiQ/1500x1500); }
    .panel3 { background-image:url(https://images.unsplash.com/photo-1465188162913-8fb5709d6d57?ixlib=rb-0.3.5&q=80&fm=jpg&crop=faces&cs=tinysrgb&w=1500&h=1500&fit=crop&s=967e8a713a4e395260793fc8c802901d); }
    .panel4 { background-image:url(https://source.unsplash.com/ITjiVXcwVng/1500x1500); }
    .panel5 { background-image:url(https://source.unsplash.com/3MNzGlQM7qs/1500x1500); }

    .panel >*{
        margin: 0;
        /* border: 2px solid red; */
        width: 100%;
        transition: transform 0.5s ;
        flex: 1 0 auto;
        display: flex;
        justify-content: center;
        flex-direction: column;
    }

    .panel p{
        text-transform: uppercase ;
        font-family: 'Amatic SC', cursive;
        font-size: 2em;
    }
    .panel > *:first-child{transform: translateY(-100%);}
    .panel.open-active > *:first-child{transform: translateY(0);}
    .panel > *:last-child{transform: translateY(100%);}
    .panel.open-active > *:last-child{transform: translateY(0);}
    .panel.open{
        flex: 5;
        font-size: 40px;
    }




</style>

<div class="panels">
    <div class="panel panel1">
        <p>Hey</p>
        <p>let's</p>
        <p>Dance</p>
    </div>
    <div class="panel panel2">
        <p>Give</p>
        <p>Take</p>
        <p>Receive</p>
      </div>
      <div class="panel panel3">
        <p>Experience</p>
        <p>It</p>
        <p>Today</p>
      </div>
      <div class="panel panel4">
        <p>Give</p>
        <p>All</p>
        <p>You can</p>
      </div>
      <div class="panel panel5">
        <p>Life</p>
        <p>In</p>
        <p>Motion</p>
      </div>
    


</div>
<script>

    const panel = document.querySelectorAll('.panel');
    function toggleopen(){
        this.classList.toggle('open');
    }
    function toggleActive(e){
       if(e.propertyName.includes('flex')){
        this.classList.toggle('open-active');
       }
    }

    panel.forEach(panel=>panel.addEventListener('click',toggleopen));
    panel.forEach(panel=>panel.addEventListener('transitionend',toggleActive));


</script>



    
</body>
</html>
