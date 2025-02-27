# Heart-Trail-Animation
Overview

This project is a simple heart trail animation effect where heart icons follow the user's mouse movements on the screen.

Features

* Animated hearts appear at the mouse pointer location.
* Randomly sized hearts for a dynamic effect.
* Smooth movement and fading animation.
* Implemented using HTML, CSS, and JavaScript.

Files Structure

 /project-folder</BR>
│-- index.html  # Main HTML file for heart animation</BR>
│-- style.css   # Styling for heart animation</BR>
│-- code.js     # JavaScript logic for animation</BR>

Installation and Usage

  1. Clone the repository:
      git clone https://github.com/kavya-yadav963/project-folder.git
  2. Navigate to the project directory:   
      cd project-folder
  3. Open index.html in a browser.

Code Breakdown
  # JavaScript (code.js)
    const bodyE1 = document.querySelector("body");
    bodyE1.addEventListener("mousemove", (event) => {
        const xPos = event.offsetX;
        const yPos = event.offsetY;
        const spanE1 = document.createElement("span");
        spanE1.style.left = xPos + "px";
        spanE1.style.top = yPos + "px";
        const size = Math.random() * 100;
        spanE1.style.width = size + "px";
        spanE1.style.height = size + "px";
        bodyE1.appendChild(spanE1);
        setTimeout(() => {
            spanE1.remove();
      }, 3000);
    });

# CSS (style.css)

    body {
          margin: 0;
          height: 100vh;
          background-color: black;
    }
    span {
          background: url(https://cdn0.iconfinder.com/data/icons/small-n-flat/24/678087-heart-1024.png);
          width: 100px;
          height: 100px;
          position: absolute;
          pointer-events: none;
          background-size: cover;
          left: 50%;
          top: 50%;
          transform: translate(-50%, -50%);
          animation: animate 6s linear;
    }
    @keyframes animate {
                        0% {
                           transform: translate(-50%, -50%);
                           opacity: 1;
                           filter: hue-rotate(0);
                          }
                        100% {
                          transform: translate(-50%, -5000%);
                          opacity: 1;
                          filter: hue-rotate(720deg);
                        }
    }

Future Improvements

Improve animation smoothness.

  * Add different shapes for variety.

  * Allow users to customize colors and effects.

License

This project is open-source and available under the MIT License.

  
