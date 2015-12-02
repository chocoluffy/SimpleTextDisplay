**The basic workflow to establish a working app on heroku:**


```
rails new railsgirls

rails scaffold idea name:string description:text message:string

rake db:migrate

rails server
```

in Gemfile file

group :production do
	gem 'pg'
	gem 'rails_12factor'
end

group :environment do
	gem 'sqlite3'
end

bundle intall --without-production

heroku create

git push heroku origin 

heroku rake:



