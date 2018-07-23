# Warp

Here's why this class exists: WordPress pollutes the global namespace
something awful, and there's nothing we can do about that.

However, we can voluntarily "wrap" WordPress in a class, and choose
to only access it through that class. Why would we want to do that?
The main reason is unit testing. By accessing WordPress's global functions
only through this class, we can easily mock it up and test without
instantiating all of WordPress, setting up a database, so on and so forth.

## Installation

Install using [Composer][composer]:

````
    composer require loresjoberg/warp
````

## Usage

$warp = new \LoreSjoberg\Warp();

$result = $warp->count_users();