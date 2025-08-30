<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Morphing Website</title>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/animejs/3.2.1/anime.min.js"></script>
  <style>
    body {
      margin: 0;
      padding: 0;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      height: 100vh;
      background: linear-gradient(135deg, #0f2027, #203a43, #2c5364);
      font-family: Arial, sans-serif;
      color: #fff;
      overflow: hidden;
    }

    h1 {
      font-size: 2.5rem;
      margin-bottom: 20px;
      text-align: center;
      animation: fadeIn 2s ease-in-out;
    }

    p {
      font-size: 1.2rem;
      margin-bottom: 40px;
      text-align: center;
      max-width: 500px;
      animation: fadeIn 3s ease-in-out;
    }

    svg {
      width: 300px;
      height: 300px;
    }

    path {
      fill: #ff0055;
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(20px); }
      to { opacity: 1; transform: translateY(0); }
    }
  </style>
</head>
<body>
  <h1>Welcome to My Morphing Website</h1>
  <p>This website morphs shapes smoothly. You can replace this text with your own brand or project info.</p>

  <svg viewBox="0 0 500 500">
    <path d="M250,60C300,100 400,150 350,250C300,350 200,400 150,300C100,200 200,100 250,60Z"/>
  </svg>

  <script>
    anime({
      targets: 'path',
      d: [
        { value: 'M250,100C350,150 400,250 300,350C200,450 100,300 150,200C200,100 150,50 250,100Z' },
        { value: 'M200,80C280,100 420,200 300,320C180,440 100,280 120,200C140,120 120,60 200,80Z' }
      ],
      easing: 'easeInOutQuad',
      duration: 4000,
      loop: true,
      direction: 'alternate'
    });
  </script>
</body>
</html>
