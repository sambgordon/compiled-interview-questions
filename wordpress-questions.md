
# WordPress Questions

## What are the building blocks of WP?

* Core files - usually contain only php code; do not edit
* Theme files - contain a combination of php and html
* Plugin files

## List some advantages of WordPress

* Built-in **SEO** system
* Plugins
* Flexibility
* Easy theme system
* 5-minute installation

## What are some of the disadvantages of WordPress?

* A lot of plugins are not maintained
* WordPress is PHP-based so its behavior is synchronous unless you're using the WP-REST API
* Use of multiple plugins can make a website heavy to load and very slow
* You need to **back up often** because **updates can sometimes lead to a loss of data**

## What are the **template tags** in WordPress? List some of them

**Template tags** are **PHP functions** that are used to display information **dynamically**, or customize a blog template.

* `get_header()`
* `wp_register()`
* `get_sidebar()`
* `wp_title()`
* `wp_enqueue_script()`
* `get_the_author()`
* `wp_list_authors()`
* `get_bookmarks()`

## What's the function to get a website URL in WordPress?

`get_site_url()` is used to do this.

## What are hooks in WordPress?

**Hooks** are functions that can be applied to an **Action** or **Filter** in WordPress. Actions and Filters are functions that can be modified by the theme and plugin developers to **change the *default* WordPress functionality**. Hooks are a way for one piece of code to interact with/modify another piece of code.

Arguments used to hook both filters and actions look the same, but function differently.

To use either, you need to **1. Write a custom function known as a Callback**, and then **2. Register it with the WP hook**. The **callback** function is called when an action is run, for example.


#### What are Actions?

Actions are functions performed **when a certain event occurs in WordPress** (not unlike event handling/listening). Actions allow you to **add data** or **change how WP operates**.

Callback functions for actions will run at a specific point in the execution of WP and can perform some kind of task, like **echoing output to the user**, or **inserting something into the database**.

The process of adding an action involves two steps:

1. Create a callback function, to be called when the action is run
2. Add callback function to the **hook, which performs the calling of the function**

Example of an action:

```php
<?php
function something_custom()
{
	//do something
}
add_action('init', 'something_custom');
```

#### What are Filters?

Filters allow you to ***modify* preexisting functions**.

They give you the ability to **change** data **during the execution of WordPress Core, plugins, and themes**.

Callback functions for filters will 1. Accept a variable, 2. **modify** it, and 3. return it.

Unlike actions, **filters are meant to work in an isolated manner**, and should never have side effects such as affecting global variables.

Adding a filter involves the same two steps as adding and registering an action.

Filter example:

```php
<?php
function a_filter($title) //the function be modified or "filtered"
{
	return 'The' . $title . ' was filtered';
}
add_filter('the_title', 'a_filter');
```

## List some action and filter hook functions

#### Action hooks:

* `has_action()`
* `add_action()`
* `do_action()`
* `doing_action()`

#### Filter hooks:
* `has_filter()`
* `add_filter()`
* `apply_filters()`
* `current_filter()`

## How would you run a database query in WP?

You can use the `query` function to execute any SQL query on the WP database.

It's best used for specific, custom, or otherwise complex SQL queries.

Syntax:
```php
<?php $wpdb->query('query')?>
```

## How do you disable comments in WP?

Go to *Settings* -&gt; *Discussion* -&gt; *Uncheck* "Allow people to post comments".

## What are **importers** in WP?

**Importers** are plugins that provide functionality to import a bulk **XML** file with any number of records.
It enables you to import **Posts**, **Pages**, **Custom** **Posts** and **Users** data in an XML file.

## What is a **child theme**?

It's an extension of a parent theme. This allows you to make changes to the parent theme, because **in case of an update, changes to the parent theme may be undone**. Child themes allow customizations to be preserved on update.

## What's the difference between the two URLs in General Settings?

* The **WordPress Address** is where to look for WP files
* The **Site Address** is what will be used as the base for creating URLs for web pages.

## How do you display error messages during development?

Changing `WP_DEBUG` in `wp-config.php` to `true`. This triggers the WP "debug" mode.


## What are **custom fields** in WP?

Custom fields are also known as **post meta**. Post meta is a feature in WP which allows post authors to add additional information at the time of writing a post. Users can later display this metadata by using template tags in their WP themes if required.

Other extra details can be added to a WP post.

## What are some steps to take when your site is hacked?

* Install security plugins like **WP Security**
* Re-install the latest version of WP
* Change passwords and user-ids for all of your users
* Uninstall all plugins downloaded from untrusted places


## Where is WP content stored?

In the MySQL database on the server.

## What is **taxonomy** in WP?

**Taxonomy** is a grouping mechanism for some posts, links, or custom post types.

There are four default taxonomies:

* **Category**
* **Tag**
* **Link Category**
* **Post Formats**

You can also create your own **custom taxonomies**.

## What are some of the minimum requirements to run WP?

* **PHP 7** or greater
* **MySQL 5.6** or greater
* The `mod_rewrite` Apache module
* **HTTPS** support (recommended)

## What's the most basic security measure you can take with WP?
Updating to the latest version to avoid hacking.

## Does WP use **cookies**?

Yes, they're used for verification purposes of the users when they log in.

## What's the **usermeta** function?

It's used to retrieve metadata of the users. It can return a single value, or an array of metadata.

## What's the difference between **.com** and **.org** for WP?

Hosting - with .org you host your own blog.

## What's the best multilingual plugin for WP?

**WPML** is the best multilingual plugin.

## In WP, are objects passed by value or by reference?

All objects are passed by **value**.

## What year was WP released?

2003.

## What is a **plugin**?

A plugin is a piece of code that contains one or more functions written to extend/add to the functionality of an existing WP site.

The core is designed to be lean and lightweight, to maximize flexibility and minimize code bloat.

#### What plugins come with a clean WP installation?
* **Akismet**
* **Hello Dolly**

## What are the differences between Posts and Pages?

These are the two **content types** in WP.

**Posts** are timed and **listed in chronological order**, with the latest posts at the top.
Posts are also meant to be shared and commented on.

**Pages** are static, for example an *About Us* or *Contact Us* page.

## Why is **MySQL** used in WP?

* Fast
* Open-source
* Widely used and available database server

## Is .com more secure than .org?

Yes, because WP is hosting the site, and it limits the themes as well as not allowing installation of plugins.

## What is the WP **loop**?

**The Loop** is used to **display posts**.

## How many default tables does WP have?

There are 11 tables:

* `wp_options`
* `wp_users`
* `wp_links`
* `wp_commentmeta`
* `wp_term_relationships`
* `wp_postmeta`
* `wp_posts`
* `wp_term_taxonomy`
* `wp_usermeta`
* `wp_terms`
* `wp_comments`

## Mention rules to be followed when developing a WP plugin

1. Create a unique name
2. Create a folder for the plugin
3. Create a sub-folder for PHP files, translations and assets
4. Create the main plugin file with header information
5. Create activation and deactivation functions, an uninstall script, and a readme.txt

## What's the default table prefix in WP?

`wp_` is the default table prefix.


