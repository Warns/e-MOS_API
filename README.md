# e-MOS API Notes

## 1. Get Token

```sh
{
  "password": "72d6a5b5-dc4a-ceb5-fe19-f695f1258ca8",
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
  "productId": "575094",
  "quantity": 1,
}
```

After you add a product you will get a new **session** ID you need to use that after this point instead of the old session ID.

## 3. getCart

```sh
{
  "cartLocation": "basket",
}
```
![](https://snipboard.io/YhTsK0.jpg)
