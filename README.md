# codeigniter-upload
Codeigniter 3 – Upload file and insert data into database!

Basic Setup:

<strong>MYSQL PART:</strong>

Go to MySQL or open phpMyadmin and create a database name called '<strong>codeigniter3</strong>' and then create a table called <strong>'pictures'</strong>. I am attaching the table structure here:
<pre class="toolbar-overlay:false lang:mysql decode:true ">CREATE TABLE `pictures` (
  `pic_id` int(11) NOT NULL PRIMARY KEY AUTO_INCREMENT,
  `pic_title` varchar(255) COLLATE utf8_unicode_ci NOT NULL,
  `pic_desc` text COLLATE utf8_unicode_ci NOT NULL,
  `pic_file` varchar(255) COLLATE utf8_unicode_ci NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8 COLLATE=utf8_unicode_ci;</pre>
MySQL part is over. No need to go to the database again.

<strong>CODEIGNITER CONFIGURATIONS:</strong>

1) First, open the <strong>database.php</strong> file inside <strong>/codigniter3/application/config/database.php </strong>and change the mysql <strong>hostname, username and password</strong> as per your database server configuration:
<pre class="toolbar-overlay:false lang:php decode:true">$db['default'] = array(
	'dsn'	=&gt; '',
	'hostname' =&gt; 'localhost',//change this as per your server
	'username' =&gt; 'root',//change this as per your server
	'password' =&gt; '', //change this as per your server
	'database' =&gt; 'codeigniter3',
	'dbdriver' =&gt; 'mysqli',
	'dbprefix' =&gt; '',
	'pconnect' =&gt; FALSE,
	'db_debug' =&gt; (ENVIRONMENT !== 'production'),
	'cache_on' =&gt; FALSE,
	'cachedir' =&gt; '',
	'char_set' =&gt; 'utf8',
	'dbcollat' =&gt; 'utf8_general_ci',
	'swap_pre' =&gt; '',
	'encrypt' =&gt; FALSE,
	'compress' =&gt; FALSE,
	'stricton' =&gt; FALSE,
	'failover' =&gt; array(),
	'save_queries' =&gt; TRUE
);</pre>

2) Then, open config.php file inside <strong>/codigniter3/application/config/config.php </strong>and set the <strong>$config['base_url']</strong> to <strong>$config['base_url'] = 'http://localhost/codeigniter3/'</strong>;
