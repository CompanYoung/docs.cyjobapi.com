# Formats and Terms

## Photo object formats
Categories of photos may be specified by their ID or string name, depending on the API method.

### Short format
The short format of a Photo object includes the following data:

- **id** — ID of the photo, integer
- **name** — Title of the photo, string
- **description** — Description of the photo, string
- **camera** — Make and model of the camera this photo was made with, string
- **lens** — This photo’s camera lens information, string
- **focal\_length** — Focal length of the shot, string
- **iso** — ISO value of the shot, string
- **shutter\_speed** — Shutter speed value of the shot, string
- **aperture** — Aperture value of the shot, string
- **times\_viewed** - The number of views this photo has, integer
- **rating** — Rating of the photo, decimal
- **status** — Status of the photo in the system, integer. An active photo always has the status of 1.
- **created\_at** — Timestamp indicating time of photo creation, timestamp
- **category** — [Category][] of the photo, (short) integer
- **location** — A human-readable name of the location where the photo was taken, string
- **privacy** - Boolean value whether or not the community page (http://500px.com/photo/:id) of this photo is available.  A value of true means the page is not available.
- **latitude** — Latitude of the location where the photo was taken, decimal
- **longitude** — Longitude of the location where the photo was taken, decimal
- **taken\_at** — Timestamp of when the photo was taken, timestamp
- **for\_sale** - Boolean value whether or not the photo is for sale
- **width** - The width of the original, unresized photo, integer
- **height** - The height of the origin, unresized photo, integer
- **votes\_count** — Number of votes cast on this photo, integer
- **favorites\_count** — Number of times this photo was added as a favorite on the website, integer
- **comments\_count** — Number of comments this photo has, integer
- **positive_votes_count** - Number of positive votes (likes) this photo has received, integer
- **nsfw** - Boolean value whether the current photo is NSFW
- **sales_count** - The number of sales this photo has
- **highest_rating** - The highest rating this photo has had, decimal
- **highest_rating_date** - The date the highest rating was reached on, timestamp
- **license_type** - [License type][] of the photo, (short) integer
- **converted** - Boolean value indicating whether or not this photo has been converted.
- **image\_url** — URL of the image, string, **deprecated**
- **images** - Array with images URL and sizes
- **user** — Author’s profile in [short format][], object
- **collections_count** - Number of collections this photo is present in, integer

[Category]: #categories
[License type]: #license_types

### Full format
The full format of a Photo object includes the following data:

- **id** — ID of the photo, integer
- **name** — Title of the photo, string
- **description** — Description of the photo, string
- **camera** — Make and model of the camera this photo was made with, string
- **lens** — This photo’s camera lens information, string
- **focal\_length** — Focal length of the shot, string
- **iso** — ISO value of the shot, string
- **shutter\_speed** — Shutter speed value of the shot, string
- **aperture** — Aperture value of the shot, string
- **times\_viewed** - The number of views this photo has, integer
- **rating** — Rating of the photo, decimal
- **status** — Status of the photo in the system, integer. An active photo always has the status of 1.
- **created\_at** — Timestamp indicating time of photo creation, timestamp
- **category** — [Category][] of the photo, (short) integer
- **location** — A human-readable name of the location where the photo was taken, string
- **privacy** - Boolean value whether or not the community page (http://500px.com/photo/:id) of this photo is available. A value of true means the page is not available.
- **latitude** — Latitude of the location where the photo was taken, decimal
- **longitude** — Longitude of the location where the photo was taken, decimal
- **taken\_at** — Timestamp of when the photo was taken, timestamp
- **for\_sale** - Boolean value whether or not the photo is for sale
- **width** - The width of the original, unresized photo, integer
- **height** - The height of the origin, unresized photo, integer
- **votes\_count** — Number of votes cast on this photo, integer
- **favorites\_count** — Number of times this photo was added as a favorite on the website, integer
- **comments\_count** — Number of comments this photo has, integer
- **positive_votes_count** - Number of positive votes (likes) this photo has received, integer
- **nsfw** - Boolean value whether the current photo is NSFW
- **sales_count** - The number of sales this photo has
- **highest_rating** - The highest rating this photo has had, decimal
- **highest_rating_date** - The date the highest rating was reached on, timestamp
- **license_type** - [License type][] of the photo, (short) integer
- **converted** - Boolean value indicating whether or not this photo has been converted.
- **image\_url** — URL of the image, string, **deprecated**
- **images** - Array with images URL and sizes
- **user** — Author’s profile in [short format][], object
- **comments** - If requested, an array of comments.
- **store_download** - Boolean value indicating whether or not the photo is for sale as a digital download.
- **store_print** - Boolean value indicating whether or not the photo is for sale as a canvas print.
- **editors_choice** - Boolean value indicating whether or not the photo is in Editors' Choice.
- **feature** - The section of the site this photo appears under, string. Possible values are popular upcoming fresh_today fresh_yesterday fresh_week
- **collections_count** - Number of collections this photo is present in, integer

If you are authenticated when making the request. These additional fields will be returned:
- **voted** — Boolean value whether the current user has voted for this photo
- **favorited** — Boolean value whether the current user has favorited this photo
- **purchased** — Boolean value whether the current user has bought this photo

***

## User object formats

### Short format
The short format of a User object includes the following data:

- **id** — ID of the user, integer
- **username** — Username, string
- **firstname** — First name, string
- **lastname** — Last name, string
- **fullname** — A combination of first and last names or a username that would naturally appear on the site, string
- **city** — City as specified in user's profile, string
- **country** — Country as specified in user's profile, string
- **userpic\_url** — Profile picture’s URL of the user, string
- **upgrade\_status** — Whether the user is a premium user, integer. Non-zero values identify premium users; a value of 2 identifies an Awesome user while a value of 1 identifies a Plus user. Other states may be added in the future, so write your parsers accordingly.
- **followers_count** — User followers count
- **affection** — Affection value, integer.


### Profile format
The profile format of a User object includes the following data:

- **id** — ID of the user, integer
- **username** — Username, string
- **firstname** — First name, string
- **lastname** — Last name, string
- **fullname** — A combination of first and last names or a username that would naturally appear on the site, string
- **sex** — Sex of the user, string. Values: 1 and 2 for male and female respectively, 0 if user refused to specify their sex.
- **city** — City as specified in user’s profile, string
- **state** — State as specified in user’s profile, string
- **country** — Country as specified in user’s profile, string
- **registration\_date** — Registration timestamp, timestamp
- **about** — User’s about text, timestamp
- **domain** - The host name of the user's portfolio, string
- **locale** — User’s preferred locale, string. Current values: <code>en, ru, de, ja, br, es</code>.
- **upgrade\_status** — Whether the user is a premium user, integer. Non-zero values identify premium users; a value of 2 identifies an Awesome user while a value of 1 identifies a Plus user. Other states may be added in the future, so write your parsers accordingly.
- **show\_nude** — Whether the user has content filter disabled, boolean.
- **userpic\_url** — Profile picture’s URL of the user, string
- **store\_on** - Whether the user has the store option enabled, boolean
- **contacts** — A dictionary of user’s contacts, object. Keys should be treated as provider names, and values as user IDs with given provider.
- **equipment** - A dictionary of a user's equipment. Possible keys are <code>camera, lens, misc</code>. Each key will have an array of values.
- **photos\_count** — Number of active photos posted by the user, integer.
- **affection** — Affection value, integer.
- **in\_favorites\_count** — Number of times any photo of the user was added to favorites, integer.
- **friends\_count** — Number of people this user follows, integer.
- **followers\_count** — Number of people this user is being followed by, integer.
- **admin** - Boolean value that will be 1 if the user is a 500px team member.
- **avatars** - A dictionary of different avatar sizes. Keys are <code>default, large, small, tiny</code>. default is up to 300x300px, large is 100x100px, small is 50x50px, tiny is 30x30px.

If the user you are requesting is the currently authenticated user these additional fields will be returned:
- **email** - The user's email address.
- **upload\_limit** - The remaining upload limit this user has, integer
- **upload\_limit\_expiry** - The date at which additional uploads will be available, timestamp
- **upgrade\_expiry\_date** - The date at which the user's subscription will expire, timestamp
- **auth** - A dictionary of a user's social network authentications. Possible keys are <code>facebook, twitter, google_oauth2</code>. Each key will have a value of '1' as existing authentication or '0' as no authentication.

If you are authenticated these additional fields will be returned:
- **following** - A boolean value indicating whether or not you are following this user.

***

## Blog Post object formats

### Short format
The short format of a Blog Post object includes the following data:

- **id** — ID of the blog post, integer
- **title** — Title of the blog post, string
- **created\_at** — Timestamp indicating time the blog post was created, timestamp
- **user** — Author’s profile in [short format][], object

### Full format
The full format of a Blog Post object includes the following data:

- **id** — ID of the blog post, integer
- **longitude** — Longitude attached to the blog post, string
- **latitude** — Latitude attached to the blog post, string
- **title** — Title, string
- **body** — Content of post, string
- **tags** — Comma separated list of tags, string
- **created\_at** — Timestamp indicating time the blog post was created, timestamp
- **user** — Author’s profile in [short format][], object
- **photos** — A list of photos given in [short format][], object

***

## Comment object formats
The profile format of a User object includes the following data:

### Full format
The full format of a Comment object includes the following data:

- **id** — ID of the comment, integer
- **body** — Content of the comment, string
- **to_whom_user_id** — To which user the comment was made, string
- **user_id** — User ID of author of the comment, string
- **created_at** — Timestamp indicating time the comment was created, timestamp
- **user** — Author's profile in [short format][], object
- **parent_id** - The ID of the comment that was replied to. If this value is null then the comment was not a reply to another comment, integer
- **flagged** - A boolean value indicating whether or not this comment was flagged for review.
- **rating** - The sum of the number of votes this comment has received, integer

If you are authenticated these additional attributes will be returned:

- **voted** - A boolean value indicating whether or not the currently authenticated user has voted on this comment.

[Category]: https://github.com/500px/api-documentation/blob/master/basics/formats_and_terms.md#categories
[short format]: https://github.com/500px/api-documentation/blob/master/basics/formats_and_terms.md#short-format-1
[License type]: https://github.com/500px/api-documentation/blob/master/basics/formats_and_terms.md#license_types