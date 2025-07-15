# google-clone-homepage
<html>
<head>
<title>Google</title>
    <style>
        *{
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: Arial;
        }

        body {
            color: #202124;
            display: flex;
            flex-direction: column;
            height: 100vh;
        }
        
         header {
            display: flex;
            justify-content: flex-end;
            padding: 5px 10px;
            align-items: center;
            font-size: 13px;
        }
        
        .header-links {
            display: flex;
            align-items: center;
            gap: 20px;
        }
        
        .header-links a {
            text-decoration: none;
            color: rgba(0,0,0,.87);
        }
        
        .header-links a:hover {
            text-decoration: underline;
        }
        
        .top-bar {
           display: flex;
           justify-content: flex-end;
           padding: 10px;
           background: #fff;
        }

        .app-grid-icon {
           width: 20px;
           height: 20px;
           display: grid;
           grid-template-columns: repeat(3, 1fr);
           gap: 2px;
           cursor: pointer;
        }

         .app-grid-icon div {
           width: 6px;
           height: 6px;
           background-color: #555;
           border-radius: 50%;
           opacity: none;
         }

         .app-menu {
            position: absolute;
            top: 60px;
            right: 20px;
            width: 260px;
            background: #fff;
            border-radius: 10px;
            padding: 16px;
            display: none;
            grid-template-columns: repeat(3, 1fr);
            gap: 16px;
            z-index: 100;
        }

        .app-icon {
            text-align: center;
            font-size: 12px;
            color: #222;
            cursor: pointer;
       }

        .app-icon img {
            width: 25px;
           height: 25px;
           margin-bottom:6px;
       }
        
          .bottom-section {
           grid-column: span 3;
           margin-top: 12px;
           padding-top: 10px;
           border-top: 1px solid #eee;
           text-align: center;
       }

        .bottom-section button {
           background-color: #1a73e8;
           color: white;
           border: none;
           border-radius: 20px;
           padding: 6px 12px;
           font-size: 13px;
           cursor: pointer;
       }

         .bottom-section .dismiss {
             display: block;
             margin-top: 8px;
             font-size: 13px;
             color: #555;
             cursor: pointer;
       }
  
        
        .sign-in-acc {
            background-color: #1a73e8;
            color: white;
            border: none;
            padding: 20px;
            border-radius: 100px;
            font-weight: 100;
            cursor: pointer;
            height: 10px;
            width: 5px;
            
          
        }
        
        .sign-in-acc:hover {
            background-color: #1b66c9;
            box-shadow: 0 1px 3px 1px rgba(66,64,67,.15);
        }
        
        main {
            flex: 1;
            display: flex;
            flex-direction: column;
            align-items: center;
            padding-top: 40px;
        }
       

      .btnColor {
            margin-top: 10px;
            flex-direction: grid;
             padding: 10px 10px;
             font-size: 12px;
             cursor: pointer;
        }

         .btnImage {
             margin-top: 10px;
             flex-direction: grid;
             padding: 10px 10px;
             font-size: 12px;
             cursor: pointer;
        }

        .logo {
            margin-bottom: 10px;
        }
        
        .search-container {
            width: 100%;
            max-width: 584px;
            position: relative;
            margin-bottom: 40px;
            
            
        }
        
        .search-box {
            width: 100%;
            padding: 15px 50px;
            border-radius: 24px;
            border: 1px solid #dfe1e5;
            font-size: 16px;
            outline: none;
        }
        
        .search-box:hover, .search-box:focus {
            box-shadow: 0 1px 6px rgba(32,33,36,0.28);
            border-color: rgba(223,225,229,0);
        }
        
        .search-icon, .mic-icon, .camera-icon {
            position: absolute;
            top: 20px;
            width: 15px;
            height: 15px;
        }
        
        .search-icon {
            left: 20px;
            opacity: 0.4;
        } 
        
        .mic-icon {
            right: 60px;
            cursor: pointer;
        }
        
        .camera-icon {
            right: 25px;
            cursor: pointer;
        }
        
        .buttons {
            display: flex;
            gap: 15px;
        }
        
        .search-btn, .lucky-btn {
            background-color: #f8f9fa;
            border: 1px solid #f8f9fa;
            border-radius: 4px;
            padding: 10px 16px;
            font-size: 14px;
            color: #3c4043;
            cursor: pointer;
        }
        
        .search-btn:hover, .lucky-btn:hover {
            border: 1px solid #dadce0;
            box-shadow: 0 1px 1px rgba(0,0,0,0.1);
        }
        
        .language {
            margin-top: 30px;
            font-size: 13px;
        }
        
        .language a {
            text-decoration: none;
            color: #1a0dab;
        }
        
        .language a:hover {
            text-decoration: underline;
        }
        

        footer {
            background-color: #f2f2f2;
            color: #1c1c1d;
            font-size: 14px;
        }
        
        .footer-top {
            padding: 15px 30px;
            border-bottom: 1px solid #dadce0;
        }
        
        .footer-bottom {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            padding: 15px 30px;
        }
        
        .footer-links {
            display: flex;
            gap: 20px;
        }
        
        .footer-links a {
            text-decoration: none;
            color: #1c1c1d;
        }
        
        .footer-links a:hover {
            text-decoration: underline;
        }
        
        @media (max-width: 700px) {
            .footer-bottom {
                justify-content: center;
                gap: 20px;
            }
        }
      </style>
      </head>
      <body>
        <header>
        <div class="header-links">
            <a href="#">Gmail</a>
            <a href="#">Images</a>
            <button class="sign-in-acc">J</button>
          </div>
        <div classs="header-links">

            <div class="top-bar">  
        <div class="app-grid-icon" onclick="toggleAppMenu()">
            <div></div><div></div><div></div>
            <div></div><div></div><div></div>
            <div></div><div></div><div></div>
          </div>
        

         </div>

       <div class="app-menu" id="appMenu" >
        <div class="app-icon">
         <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/a/a3/Eo_circle_blue_letter-j.svg/1200px-Eo_circle_blue_letter-j.svg.png" alt="Account">
         <div>Account</div>
       </div>

        <div class="app-icon">
         <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQ3RaendkWxwbnlsA8UyDPmcDbqIMQETxKYpw&s" alt="Drive">
          <div>Drive</div>
        </div>

      <div class="app-icon">
       <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSJ9otYnFOGrIP3LlAooxg8JxUy0YZlX4BZlQ&s" alt="Business Profile manager">
        <div>Business Profile Manager</div>
      </div>

       <div class="app-icon">
        <img src="https://brandlogos.net/wp-content/uploads/2020/10/gmail-logo-icon.png" alt="Gmail">
        <div>Gmail</div>
      </div>


        <div class="app-icon">
          <img src="https://cdn3.iconfinder.com/data/icons/social-network-30/512/social-06-512.png" alt="Youtube">
          <div>Youtube</div>
         </div>

       <div class="app-icon">
         <img src="https://uxwing.com/wp-content/themes/uxwing/download/brands-and-social-media/google-gemini-icon.png" alt="Gemini">
         <div>Gemini</div>
        </div>

       <div class="bottom-section">
          <button>Try Gemini</button>
          <span class="dismiss" onclick="toggleAppMenu()">Dismiss</span>
           </div>

           
        </div>
        

   

       </header>
        <main>
        <div class="logo">
         <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/2/2f/Google_2015_logo.svg/1200px-Google_2015_logo.svg.png" alt="Google" width="300" height="100">
        </div>

             <div class="search-container">
            <img class="search-icon" src="https://static-00.iconduck.com/assets.00/search-icon-2048x2048-cmujl7en.png" alt="Search icon">
            <input type="text" name="q" class="search-box" aria-label="Search"autofocus>

            <img class="mic-icon" src="https://cdn-icons-png.freepik.com/512/60/60540.png" alt="Voice search">

            <img class="camera-icon" src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSHzHApqUpQhJINc_1sR3L_X10-amkpr8pIsA&s" alt="Search image">
        
             </div>
        
           <div class="buttons">
            <button class="search-btn">Google Search</button>

            <button class="lucky-btn">I'm Feeling Lucky</button>
           </div>   

         <div>
          <input type="color" id="bgColorPicker">
         <button class="btnColor" onclick="setBackgroundColor()">Set Background Color</button>

         </div>

          <div>
            <input type="file" id="bgImagePicker" accept="image/*">
             <button class="btnImage" onclick="setBackgroundImage()">Set Background Image</button>
          </div>


        <div class="language">
           Google offered in: 
             <a href="#">हिन्दी</a> 
             <a href="#">বাংলা</a>
             <a href="#">తెలుగు</a>
             <a href="#">मराठी</a>
             <a href="#">தமிழ்</a>
             <a href="#">ગુજરાતી</a> 
             <a href="#">ಕನ್ನಡ</a> 
             <a href="#">മലയാളം</a>
             <a href="#">ਪੰਜਾਬੀ</a>
        </div>
    </main>
    
    <footer>
        <div class="footer-top">
            India
        </div>
        <div class="footer-bottom">
            <div class="footer-links">
                <a href="#">Advertising</a>
                <a href="#">Business</a>
                <a href="#">How Search works</a>
            </div>
            <div class="footer-links">
                <a href="#">Privacy</a>
                <a href="#">Terms</a>
                <a href="#">Settings</a>
            </div>
        </div>
    </footer>
    <script>
    function setBackgroundColor() {
  const colorPicker = document.getElementById("bgColorPicker");
  const selectedColor = colorPicker.value;

  document.body.style.backgroundColor = selectedColor;
  document.body.style.backgroundImage = "none"; 
}

function setBackgroundImage() {
  const imagePicker = document.getElementById("bgImagePicker");
  const selectedFile = imagePicker.files[0];

  if (selectedFile) {
    const imageURL = URL.createObjectURL(selectedFile);
    document.body.style.backgroundImage = `url('${imageURL}')`;
    document.body.style.backgroundSize = 'cover';
    document.body.style.backgroundRepeat = 'no-repeat';
    document.body.style.backgroundPosition = 'center';
    document.body.style.backgroundColor = '';
    
  }
}


    function toggleAppMenu() {
      const menu = document.getElementById('appMenu');
      if(menu.style.display === "grid")
  {
       menu.style.display ="none"; 
           
  }else{    

     menu.style.display ="grid"; 
  }
}

    </script>
    </body>
    </html>
