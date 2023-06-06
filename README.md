# **Welcome to Noflowerzzk**

### I have nothing to say, so just _relish_ my codes

The following's readme code:

```
# **Welcome to Noflowerzzk**

### I have nothing to say, so just _relish_ my codes

The following's readme code:

```

And the blog page's code:

```
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>解压小球（有彩蛋）</title>
    <style>
        * {
            margin: 0;
            padding: 0;
        }

        body {
            background-color: #eed9eba9;
        }

        #a {
            height: 200px;
            width: 200px;
            background-color: red;
            position: absolute;
            transition-duration: 0.4s, 0.4s, 2s, 2s, 0.4s, 0.4s;
            transition-delay: 0s, 0s, 5s, 5s, 0s, 0s;
            transition-property: background-color, border-radius, height, width, top, left;
            transition-timing-function: ease-out;
            border-radius: 25%;
        }
    </style>
</head>

<body>
    <div id="a">

    </div>
    <script>
        var div_a = document.getElementById('a');
        document.getElementById('a').addEventListener('touchmove', function (e) {
            console.log('touch move');

            const e_x = e.targetTouches[0].clientX
            const e_y = e.targetTouches[0].clientY

            const h = window.getComputedStyle(div_a).height.slice(0,
                window.getComputedStyle(div_a).height.lastIndexOf('px'))
            const w = window.getComputedStyle(div_a).width.slice(0,
                window.getComputedStyle(div_a).width.lastIndexOf('px'))


            // div_a.style.transform = `translate(${e_x - 100}px, ${e_y - 100}px)`;

            div_a.style.top = `${e_y - Number(h) / 2}px`
            div_a.style.left = `${e_x - Number(w) / 2}px`

            // div_a.style.top = `${e_y - 100}px`
            // div_a.style.left = `${e_x - 100}px`


            e.preventDefault();

            // div_a.style.transitionProperty = 'borderRadius';
            // div_a.style.transitionDuration = '5s';
            // div_a.style.borderRadius = '50%';
            // div_a.classList.add('b');


            // let x = document.createElement("audio");
            // x.setAttribute("src", `./video/${parseInt(Math.random() * 26, 10) + 1}.mp3`);
            // // setInterval(() => x.setAttribute("autoplay", "autoplay"), 500);
            // x.setAttribute("autoplay", "autoplay")
        })

        document.getElementById('a').addEventListener('touchstart', function (e) {
            // div_a.style.transitionDuration = '0.5s';
            div_a.style.backgroundColor = 'blue';

            div_a.style.borderRadius = '50%';

            div_a.style.height = '400px';
            div_a.style.width = '400px'

            div_a.style.transitionDelay = '0s,0s,5s,5s,0s,0s';

        })

        document.getElementById('a').addEventListener('touchend', function (e) {
            // div_a.style.transitionDuration = '0.5s';
            div_a.style.backgroundColor = 'red';

            div_a.style.borderRadius = '25%';

            div_a.style.height = '200px';
            div_a.style.width = '200px';


            div_a.style.transitionDelay = '0s';
        })


    </script>
</body>

</html>
```