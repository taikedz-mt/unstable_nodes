# Unstable Nodes for Minetest

Nodes that can be placed and built upon.

If you dig them, they may just give way.

Unlike falling nodes, only some of their neighbours will be caused to fall as well.

## API

This mod does not by default add any nodes to the game. It serves as a library to make nodes defined by other mods unstable.

You can however edit the examples in `nodes.lua` to add any nodes for which you want unstable counterparts for.

There are 2 main ways of creating unstable nodes:

1. Creating an unstable verison of an existing non-unstable node using `unstable_nodes(nodename)`
2. Using `unstablenodes.register_node(nodename, nodedef)` instead of `minetest.register_nod(nodename, nodedef)` to register a new node
	* The definition can also include a `fallspeed` parameter to determine the falling speed of the node - a positive integer.
