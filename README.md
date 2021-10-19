# fastapi-and-graphql
FastAPI&amp;GraphQLでサンプルAPIを作成

## Requirements

Python3.9

## Install&Run

```bash
$ python3 -m venv venv
$ source venv/bin/activate
(venv) $ docker-compose up -d
```

## View

http://localhost:8000/graphql

### 新規投稿

`mutation CreateNewPost{ createNewPost(title:"<タイトル>", content:"<コンテンツ>") { ok } }`

<img width="1632" alt="スクリーンショット 2021-10-19 12 00 21" src="https://user-images.githubusercontent.com/66961071/137837445-64986c5d-e39d-4bec-b93f-f35d7044b8c5.png">

### 全ての投稿を取得

`query{ allPosts{ title } }`

<img width="1632" alt="スクリーンショット 2021-10-19 12 00 36" src="https://user-images.githubusercontent.com/66961071/137837448-9ee8934f-9361-4b1e-8e30-162c6eca901f.png">

### IDで投稿を取得

`query{ postById(postId:<id(int)>){ id title content } }`

<img width="1632" alt="スクリーンショット 2021-10-19 12 00 49" src="https://user-images.githubusercontent.com/66961071/137837452-116f50a8-a442-45f6-9f1d-744324164e47.png">
