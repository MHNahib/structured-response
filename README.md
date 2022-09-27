
# Structured Response

![npm](https://img.shields.io/npm/v/structured-response?color=green&style=flat-square) ![npm](https://img.shields.io/npm/dm/structured-response?color=orange&style=flat-square)


The `structured-response` is a way to send the response to the client app from Express Js. Send data to the client in an organized way so that the front-end developer enjoys the work.

## How to install?

```bash
  npm i structured-response
```




## Why to use it?

| Regular way  | Using `Structured Response` |
| ------------- | ------------- |
| Needs to write `more code` to send a simple standard json response.  | Needs to write `less code` to send a simple standard json response.  |
| Can send response in unstructured way. | Only sends response in a structured way. |
| Developers have to repeat the same code again and again. | Doesn't need to repeat the response same code. |


## How to use it?

To use the package you need to use ExpressJs as your backend framework. The package gives you the freedom to send data in a structured way so that you don't need to write repeated code, again and again, to send the response for your REST API. 
The package takes the`res (response)` object from the ExpressJs and also takes`status code`, `data`, and `message` after that it returns `JSON` data to the client app.

In the regular ExpressJs app, we send responses in the given way.

### In regular way
```javascript

    app.get("/", (req, res) => {
    res.status(200).send({
            status: true,
            data: {
            key: "value",
            },
            message: "OK",
        });
    });

```

After using the package user doesn't need to face the hassle again and again. He/she can easily send the response with just a function provided by the package.
The package takes four parameters.

| Parameters | Required    | Default value   | Type |
| :---:   | :---: | :---: | :---: |
| `res (response)` | YES   |    | |
| `status code` | NO   |  200  | Number |
| `status` | NO   |  true  | Boolean |
| `data` | NO   |  {}  | Object |
| `message` | NO   |  OK  | String: Automaticly generated based on `status code` |


### In `Structured Response` way
```javascript

    const response = require("structured-response");

    app.get("/", (req, res) => {
        response(res, 200, true, { key: "value" }, "OK");
    });


```
## 🚀 Authors

[@MHNahib](https://www.github.com/MHNahib)

[![portfolio](https://img.shields.io/badge/facebook-000?style=for-the-badge&logo=facebook&logoColor=white)](https://www.facebook.com/profile.php?id=100017094937153)
[![portfolio](https://img.shields.io/badge/github-000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/MHNahib)
[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/mhnahib)
[![twitter](https://img.shields.io/badge/twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white)](https://twitter.com/HNahib)

## License

[MIT](https://choosealicense.com/licenses/mit/)
