# Rails File Structure 

One of the most daunting tasks when learning Rails can be understanding the default file structure. After typing one short line, you suddenly find yourself with a folder full of folders and files and no idea where anything goes. Well, rest assured, it's not nearly as bad as it looks! In truth, there are only a small handful of files and folders that will be important to us right now. For example, you will spend nearly all of your time at first, in the App folder.

## app/
This folder contains the 'project directory' as you may imagine it. Most of the files you need to work with are located here and you will find that this is where you spend most of your time.

### app/assets
As the name implies, you can look in here for your project's assets like images and stylesheets. This is where you put things you want to be served to the Asset Pipeline.

#### app/assets/images
You can store project images here. You shouldn't fill this up with images, as it is much better to learn to work with a cloud-based image storage solution, but it still an option as you are starting to develop your project.

#### app/assets/stylesheets
This directory houses all the stylesheets for your project. It doesn't matter if it's CSS or SCSS, put them all in this folder.

### app/controllers
This is where your Controllers go. You will immediately find two things in this folder. Concerns are not a major concern at this time and the application_controller is your project's default controller.

### app/helpers
The helper folder is where you save files for all the View helper methods you create. You will find a default application_helper already.

### app/javascript
Until JavaScript gained greater traction in Rails, this folder used to be kept in the `app/assets` directory. It is still an asset but as it is so popular, it has been moved up one level. Your default application.js can already be found here.

### app/models
The model folder is where Model files are stored. You will find another concerns folder here, pay it no mind for now. There should be a default application_record already.

### app/views
The Views folder should already have a layouts folder inside it, which houses your application.html file. This directory should contain additional folders that match each controller and HTML files inside should match to each Controller action that requires a View.

## config/
If you set up your project with SQLite3 and need to swap to PostgreSQL, you will need to look for the database.yml file located here. Aside from that, for the most part, you will only need the routes.rb file found in this folder.

## db/
This folder is going to hold all the database information. Schemas, seeds, and migration files can be found here. You should never need to touch the schema file directly but you may find yourself in `db/migrations` regularly.

## public/
Just like any other project, we have some files and images we may want to have open to the public. A 404 HTML response and a favicon, for example. This is where those things go. There are better ways of storing files so don't put everything here.

## test/ or spec/
Whether you use the default MiniTest or switch to RSpec, it's important that you have tests and these will be the corresponding folders for those tests. Each one has a unique structure but for now, it's enough to know that test/ = MiniTest and spec/ = RSpec.

### Gemfile
This file is where you will list all the Gems (or packages) that you will be using in your project. You can set Gems to be used in different environments here and when running `bundle install`, this is the file used to generate the Gemfile.lock file.

## Additional materials
 - For a more detailed look at the file structure, check out this [Rails directory structure guide](https://github.com/jwipeout/rails-directory-structure-guide) on GitHub.

------

_If you spot any bugs or issues in this activity, you can [open an issue with your proposed change](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/open_issue.md)._
