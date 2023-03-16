# Brick Hill Endpoints
All Brick Hill endpoints, in one place.

## Endpoints
| Endpoint | Params | Description | Method | Authentication Required | Deprecated |
| --- | --- | --- | --- | --- | --- |
| [/v1/games/retrieveAvatar](https://api.brick-hill.com/v1/games/retrieveAvatar?id=1) | `id: Integer` | Retrieves an avatar information | **GET** | ❌ | ❌ |
| [/v1/sets/{setId}](https://api.brick-hill.com/v1/sets/1) | `setId: Integer` | Retrieves a set information | **GET** | ❌ | ❌ |
| [/v1/shop/list](https://api.brick-hill.com/v1/shop/list) | `None` | Retrieves a list of all items in the shop | **GET** | ❌ | ❌ |
| [/v1/shop/{itemId}](https://api.brick-hill.com/v1/shop/1) | `itemId: Integer` | Retrieves an item information | **GET** | ❌ | ❌ |
| [/v1/shop/{itemId}/owners](https://api.brick-hill.com/v1/shop/1/owners) | `itemId: Integer` | Retrieves a list of all users who own an item | **GET** | ❌ | ❌ |
| [/v1/shop/{itemId}/resellers](https://api.brick-hill.com/v1/shop/1/resellers) | `itemId: Integer` | Retrieves a list of all users who resell an item | **GET** | ❌ | ❌ |
| [/v1/user/trades/{userId}/{type}](https://api.brick-hill.com/v1/user/trades/1/selling) | `userId: Integer`<br>`type: String` | Retrieves a list of all trades a user has | **GET** | ❌ | ❌ |
| [/v1/user/trades/{tradeId}](https://api.brick-hill.com/v1/user/trades/1) | `tradeId: Integer` | Retrieves a trade information | **GET** | ❌ | ❌ |
| [/v1/user/profile](https://api.brick-hill.com/v1/user/profile) | `None` | Retrieves a user's profile information | **GET** | ❌ | ❌ |
| [/v1/user/id](https://api.brick-hill.com/v1/user/id) | `None` | Retrieves a user's id from their username | **GET** | ❌ | ❌ |
| [/v1/user/{userId}/crate](https://api.brick-hill.com/v1/user/1/crate) | `userId: Integer` | Retrieves a list of all items a user owns | **GET** | ❌ | ❌ |
| [/v1/user/{userId}/owns/{itemId}](https://api.brick-hill.com/v1/user/1/owns/1) | `userId: Integer`<br>`itemId: Integer` | Retrieves whether a user owns an item or not | **GET** | ❌ | ❌ |
| [/v1/user/{userId}/value](https://api.brick-hill.com/v1/user/1/value) | `userId: Integer` | Retrieves a user's value, calculated daily | **GET** | ❌ | ❌ |

## Links
- [API Documentation](https://api.brick-hill.com/docs)