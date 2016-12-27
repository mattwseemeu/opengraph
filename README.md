# Open Graph Protocol helper for PHP

A small library for making accessing of Open Graph Protocol data easier

## Note
Keys with a dash (-) or color (:) in the name are converted to _ for easy access as a property
in PHP

Any time a key is used more than once, it will be converted into an array containing all of the values present.

## Required Extensions
* DOM for parsing

## Usage
	require_once('OpenGraph.php');

	$graph = OpenGraph::fetch('http://www.rottentomatoes.com/m/10011268-oceans/');
	var_dump($graph->keys());
	var_dump($graph->schema);

	foreach ($graph as $key => $value) {
		echo "$key => $value";
	}
