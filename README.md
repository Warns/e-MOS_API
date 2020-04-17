# e-MOS API Notes

## 1. Get Token

```sh
{
  "password": "72d6a5b5-dc4a-ceb5-fe19-f6....",
  "grant_type": "password"
}
```
![](https://snipboard.io/j8Q2iU.jpg)

In return you get 3 values; **access_token**, **session** and **priceKey**. Make sure to add **"token_type": "bearer"** to the beginning of the token. So your token should look like the following:

```sh
bearer IAkHlz6l47seOCZVOFzTqZN0Is4JVsQHEE...
```

## 2. addCartLine

```sh
{
  "productId": "575118",
  "quantity": 1,
}
```

After you add a product you will get a new **session** ID in *Response Headers* you need to use that after this point instead of the old session ID.

## 3. getCart
With the new session ID that you got after addCartLine and the old token you can now getCart

```sh
{
  "cartLocation": "basket",
}
```
![](https://snipboard.io/YhTsK0.jpg)

You should get a response similar to below:

![](https://snipboard.io/ThWcn6.jpg)

> It is recommended that you use the new session ID with every action such as AddCartLine, DeleteCartLine etc. 
