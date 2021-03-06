# RESTful API exam

Create a simple RESTful API.

### Important points

You should create:
- a MVC architecture. I mean.. a database with models, controllers and views
- a few GET requests to the routes that we'll provide below
  - when you do a GET request, you should return JSON responses 
  - Once you read the json, you should cache the data. If you request the data again, you should read the cached info instead of doing another GET request.
- a few POST requests to add new records to your models
- a few PUT requests to update records
- a few DELETE requests to remove records
- tests for your controllers and models - TDD x BDD

### Instructions

The following routes should return JSON response:

- /campaigns
- /ad_groups
- /expanded_text_ad

### How you should deliver this project

- You could host your demo on Heroku if you think that would be a good idea
- Please send the repo URL or a zip file to vbrazo@gmail.com
- Provide a easy setup

``` ruby
# Create a restful API based on this JSON response

campaigns = [
  {
    :id => '1',
    :name => 'Interplanetary Cruise',
    :status => 'PAUSED',
    :budget => '3000',
    :advertising_channel_type => 'SEARCH'
  },
  {
    :id => '2',
    :name => 'Police Station',
    :status => 'ON',
    :budget => '2000',
    :advertising_channel_type => 'DISPLAY'
  }
]

ad_groups = [
  {
    :id  => '1', 
    :name => 'Facebook Ads - Napice',
    :status => 'ENABLED',
    :campaign_id => '1'
  },
  {
    :id  => '2', 
    :name => 'Google Ads - Napice',
    :status => 'ENABLED',
    :campaign_id => '1'
  },
  {
    :id  => '3', 
    :name => 'Yahoo Ads - Spotify',
    :status => 'OFFLINE',
    :campaign_id => '2'
  }
]

expanded_text_ad = [
  {
    :xsi_type => 'ExpandedTextAd',
    :ad_group_id => '1',
    :headline_part1 => 'Developers from Mars',
    :headline_part2 => '',
    :description => 'Buy your tickets now!',
    :path1 => 'all-inclusive',
    :path2 => 'deals'
  },
  {
    :xsi_type => 'ExpandedTextAd',
    :ad_group_id => '3',
    :headline_part1 => 'We are looking for the best designers',
    :headline_part2 => 'Best in the galaxy',
    :description => 'We are a team of product builders and are looking for designers',
    :path1 => 'all-inclusive',
    :path2 => 'deals'
  }
]
```
