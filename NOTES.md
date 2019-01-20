So, this is the beginning of a long tutorial, (actually, a book called "Effective Testing with RSpec 3", by Marston and Dees). Over time we construct a Sinatra based app called 'Expense Tracker' and every step of the way we test different pieces of it with RSpec. I know you don't have a working familiarity with either Sinatra or RSpec, but my problem is a generic one having to do with requiring and loading gems.

For the spec/acceptance/expense_tracker_api_spec.rb file I am asked to require the rack-test gem

When I run this command from terminal: bundle exec rspec  ...
	... I get the following error:  LoadError: cannot load such file -- rack-test

I am using: 	Ruby 2.4.4
				RSpec 3.6
				rack-test 0.7.0

So this is how I got here.
	1. create an expense_tracker directory and cd into it

	2. $ gem install bundler   (to install bundler)	

	3. $ bundle init		(to write a Gemfile to the app)	

	4. Add these 4 lines to the Gemfile
		gem 'rspec', '3.6.0'
		gem 'coderay', '1.1.1'
		gem 'rack-test', '0.7.0'
		gem 'sinatra', '2.0.0'	

	5. $ bundle install 	(install gems and dependencies)

	6. $ bundle exec rspec --init 		(create .rspec and spec/spec_helper.rb files)

	7. Write my /spec/acceptance/expense_tracker_api_spec.rb file

	8. $ bundle exec rspec		(run the test)	

	*** and this is where I get my LoadError ***
