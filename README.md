Live demo: https://sarang9970-nhspc.github.io/WasmProject
Instructions:
-------------

1. Install Emscripten:

    http://emscripten.org

2. Clone this repo:

    ```git clone https://github.com/timhutton/opengl-canvas-wasm.git```
    
    ```cd opengl-canvas-wasm```
    
3. Build index.js and index.wasm:

    ```emcc main.cpp -std=c++11 -s WASM=1 -s USE_SDL=2 -O3 -o index.js```

4. Open index.html in a web browser. You should see a colorful animated triangle:

    <img width="400px" src="https://user-images.githubusercontent.com/647092/37932094-866c158e-313f-11e8-84f9-3873223373c5.png" />

    Chrome doesn't support file:// XHR requests, so you need to first start a webserver, e.g.:

    with Python 2: ```python -m SimpleHTTPServer 8080```
    
    with Python 3: ```python -m http.server 8080```

    and then open this URL:

    http://localhost:8080/


