# Brick Hill Endpoints
This is a list of all endpoints used by Brick Hill. This list is not complete, and will be updated as more endpoints are found.

>**[WARNING]** Some endpoints do not use [api.brick-hill.com](https://api.brick-hill.com) but rather [www.brick-hill.com](https://www.brick-hill.com)

## Table of Contents
- [Endpoints](#endpoints)
  - [User](#user)
  - [Shop](#shop)
  - [Sets](#sets)
  - [Trading](#trading)
  - [Authentication](#authentication)
  - [Assets](#assets)
  - [Staff](#staff)
- [Contributing](#contributing)
- [Links](#links)

# Endpoints<br>
## User
| Endpoint | Params | Description | Method | Authentication | Deprecated |
| --- | --- | --- | --- | --- | --- |
| [/settings/data](https://www.brick-hill.com/settings/data) | `None` | Retrieves the signed in user's setting data | **GET** | ✅ | ❌ |
| [/v1/user/profile](https://api.brick-hill.com/v1/user/profile) | `id: Integer` | Retrieves a user's profile information | **GET** | ❌ | ❌ |
| [/v1/user/id](https://api.brick-hill.com/v1/user/id) | `username: String` | Retrieves a user's id from their username | **GET** | ❌ | ❌ |
| [/v1/games/retrieveAvatar](https://api.brick-hill.com/v1/games/retrieveAvatar?id=1) | `id: Integer` | Retrieves an avatar information | **GET** | ❌ | ❌ |
| [/v1/user/{userId}/crate](https://api.brick-hill.com/v1/user/1/crate) | `userId: Integer` | Retrieves a list of all items a user owns | **GET** | ❌ | ❌ |
| [/v1/user/{userId}/owns/{itemId}](https://api.brick-hill.com/v1/user/1/owns/1) | `userId: Integer`<br>`itemId: Integer` | Retrieves whether a user owns an item or not | **GET** | ❌ | ❌ |
| [/v1/user/{userId}/value](https://api.brick-hill.com/v1/user/1/value) | `userId: Integer` | Retrieves a user's value, calculated daily | **GET** | ❌ | ❌ |
| [/api/settings/username](https://www.brick-hill.com/api/settings/username?u=1) | `u: String` | Retrieves whether a username is taken or not | **GET** | ❌ | ❌ |

## Shop
| Endpoint | Params | Description | Method | Authentication | Deprecated |
| --- | --- | --- | --- | --- | --- |
| [/v1/shop/list](https://api.brick-hill.com/v1/shop/list) | `None` | Retrieves a list of all items in the shop | **GET** | ❌ | ❌ |
| [/v1/shop/{itemId}](https://api.brick-hill.com/v1/shop/1) | `itemId: Integer` | Retrieves an item information | **GET** | ❌ | ❌ |
| [/v1/shop/{itemId}/owners](https://api.brick-hill.com/v1/shop/1/owners) | `itemId: Integer` | Retrieves a list of all users who own an item | **GET** | ❌ | ❌ |
| [/v1/shop/{itemId}/resellers](https://api.brick-hill.com/v1/shop/1/resellers) | `itemId: Integer` | Retrieves a list of all users who resell an item | **GET** | ❌ | ❌ |

## Sets
| Endpoint | Params | Description | Method | Authentication | Deprecated |
| --- | --- | --- | --- | --- | --- |
| [/v1/sets/{setId}](https://api.brick-hill.com/v1/sets/1) | `setId: Integer` | Retrieves a set information | **GET** | ❌ | ❌ |
| [/v1/sets/list](https://api.brick-hill.com/v1/sets/list) | `None` | Retrieves a list of all sets | **GET** | ❌ | ❌ |
| [/v1/games/postServer](https://api.brick-hill.com/v1/games/postServer) | [See here](https://gitlab.com/brickhill/open-source/node-hill/-/blob/master/src/api/postServer.ts#L12) | Sends server to games page | **POST** | ❌ | ❌ |

## Trading
| Endpoint | Params | Description | Method | Authentication | Deprecated |
| --- | --- | --- | --- | --- | --- |
| [/v1/user/trades/{userId}/{type}](https://api.brick-hill.com/v1/user/trades/1/selling) | `userId: Integer`<br>`type: String` | Retrieves a list of all trades a user has | **GET** | ✅ | ❌ |
| [/v1/user/trades/{tradeId}](https://api.brick-hill.com/v1/user/trades/1) | `tradeId: Integer` | Retrieves a trade information | **GET** | ✅ | ❌ |

## Authentication
| Endpoint | Params | Description | Method | Authentication | Deprecated |
| --- | --- | --- | --- | --- | --- |
| [/v1/auth/verifyToken](https://api.brick-hill.com/v1/auth/verifyToken?token=1&host_key=2) | `token: String`<br>`host_key: String` | Verifies a user's game token | **GET** | ❌ | ❌ |
| [/oauth/clients](https://api.brick-hill.com/oauth/clients) | [See Here](https://laravel.com/docs/10.x/passport#get-oauthclients) | Retrieves a list of owned oAuth clients | **GET** | ✅ | ❌ |
| [/oauth/clients](https://api.brick-hill.com/oauth/clients) | [See Here](https://laravel.com/docs/10.x/passport#post-oauthclients) | Makes a new oAuth client | **POST** | ✅ | ❌ |
| [/oauth/clients/{clientId}](https://api.brick-hill.com/oauth/clients/1) | [See Here](https://laravel.com/docs/10.x/passport#put-oauthclientsclient-id) | Updates an oAuth client | **PUT** | ✅ | ❌ |
| [/oauth/clients/{clientId}](https://api.brick-hill.com/oauth/clients/1) | [See Here](https://laravel.com/docs/10.x/passport#delete-oauthclientsclient-id) | Deletes an oAuth client | **DELETE** | ✅ | ❌ |
| [/oauth/tokens](https://api.brick-hill.com/oauth/tokens) | [See Here](https://laravel.com/docs/10.x/passport#get-oauthtokens) | Retrieves a list of authorized oAuth tokens | **GET** | ✅ | ❌ |
| [/oauth/tokens/{tokenId}](https://api.brick-hill.com/oauth/tokens/1) | [See Here](https://laravel.com/docs/10.x/passport#delete-oauthtokenstokenId) | Deletes an oAuth token | **DELETE** | ✅ | ❌ |

## Assets
| Endpoint | Params | Description | Method | Authentication | Deprecated |
| --- | --- | --- | --- | --- | --- |
| [/v1/assets/getPoly/{assetId}](https://api.brick-hill.com/v1/assets/getPoly/1) | `assetId: Integer` | Retrieves the asset's texture and mesh | **GET** | ❌ | ❌ |
| [/v1/assets/get/{assetId}](https://api.brick-hill.com/v1/assets/get/1) | `assetId: Integer` | Retrieves an texture or mesh | **GET** | ❌ | ❌ |
| [/v1/user/render/process](https://api.brick-hill.com/v1/user/render/process) | `?` | Renders a user's avatar | **POST** | ✅ | ❌ |
| [/v1/thumbnails/bulk](https://api.brick-hill.com/v1/thumbnails/bulk) | `?` | Retrieves a list of specified thumbnails | **POST** | ❌ | ❌ |
| [/v1/thumbnails/single](https://api.brick-hill.com/v1/thumbnails/single?type=1&id=2) | `type: String`<br>`id: Integer` | Retrieves a thumbnail based off query | **GET** | ❌ | ❌ |

## Staff
| Endpoint | Params | Description | Method | Authentication | Deprecated |
| --- | --- | --- | --- | --- | --- |
| [/v1/events/ingameRedeem](https://api.brick-hill.com/v1/events/ingameRedeem) | `user: Integer`<br>`item: Integer` | Grants in-game items to a user | **POST** | ✅ | ❌ |

## Contributing
To contribute to this repository, please fork it and make a pull request. All contributions are appreciated.

## Links
- [API Documentation](https://api.brick-hill.com/docs)
- [Laravel Documentation](https://laravel.com/docs/10.x/passport)