                                                          #   --------- NODE js -----------   #
                                                          -------------------------------------

// 1st programming and postman testing with JSON.

const express=require("express");   // * *
const app = express();              // * *
const PORT=process.env.PORT || 8000;// * *

app.get("/", (req,res)=>res.send("Hello World"));// 1 //  

// Receive Json Data from Postman....

app.use(express.json({extended: false}));  //recieve data from json(postman body)
app.post("/", (req,res)=>res.send(`Hello, ${req.body.name}`)); // 2 //

//  ......... 2 ........!!  //

app.get("/hello/:name",(req,res)=>res.send(`Hello ${req.params.name}`)); // 3 //

// adding Port to listening port **

app.listen(PORT,() => console.log(`Server start at
                     port ${PORT}`));  // * *


                     //  package installation
                     //  "concurrently": "^7.3.0",
                     //  "nodemon": "^2.0.19"
                     //  "express"
                     //  npm i express nodemon  concurrently. 



















