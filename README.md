1. Install dependencies
    ```shell
        npm install @tensorflow/tfjs @tensorflow-models/facemesh react-webcam
    ```
2. Import dependencies
    ```js
        import React, {useRef} from 'react'
        import * as tf from '@tensorflow/tfjs'
        import * as facemesh from '@tensorflow-models/facemesh'
        import Webcam from 'react-webcam'
    ```
3. Set up webcam and canvas
    ```js
         <Webcam ref={webcamRef} style={
            {
                position: 'absolute',
                marginLeft: 'auto',
                marginRight: 'auto',
                left: 0,
                right: 0,
                textAlign: 'center',
                zIndex:9,
                width: 640,
                height: 480,
            }
        }/>
        <canvas ref={canvasRef} style={
            {
                position: 'absolute',
                marginLeft: 'auto',
                marginRight: 'auto',
                left: 0,
                right: 0,
                textAlign: 'center',
                zIndex:9,
                width: 640,
                height: 480,
            }
        }/>
    ```

4. Load facemesh