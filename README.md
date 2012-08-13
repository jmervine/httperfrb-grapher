HTTPerf::Grapher
================

### [Documentation](http://rubyops.github.com/httperfrb-grapher/doc/) | [Coverage](http://rubyops.github.com/httperfrb-grapher/coverage/) | [RSpec Out](https://github.com/rubyops/httperfrb-grapher/blob/master/RSPECOUT.md)


### WARNING

The gem for this has been yank as it isn't working. It was designed to queue off of "Connection lifetime = ", which is avaiable in a specific installation of httperf I have been using that wasn't set up by me. However, I'm starting to think that this installation was hacked to include this output. Most standard installations that I've tested this code with fail, because this string isn't output. So I may have to abandon this effort.

You can use this with my version of [httperf](https://github.com/rubyops/httperf), which adds the necessary output. *This is very experimental, so use at your own risk.*

Additionall, [httperfrb](http://github.com/rubyops/httperfrb) has the supporting parsing code removed from master, you'll need to build your gem from the [grapher_handler branch](https://github.com/rubyops/httperfrb/tree/grapher_handler). I intend to update httperfrb, to automagically parse "Connection lifetime =" if it's there and work all nice without it.

If your verbose output contains the following type of output, this will work for you:

        Connection lifetime = 719.5
        Connection lifetime = 575.5
        Connection lifetime = 285.5
        Connection lifetime = 156.5
        Connection lifetime = 400.5
        Connection lifetime = 145.5
        Connection lifetime = 349.5
        Connection lifetime = 583.5
        Connection lifetime = 147.5
        Connection lifetime = 138.5


You will also know if HTTPerf::Grapher is usable if your HTTPerf parsed results contain the following keys:

        :connection_times
        :connection_time_75_pct
        :connection_time_80_pct
        :connection_time_85_pct
        :connection_time_90_pct
        :connection_time_95_pct
        :connection_time_99_pct



## Installing 'httperfrb'

#### See: [httperfrb](http://www.github.com/rubyops/httperfrb/)

## Usage - HTTPerf

#### See: [httperfrb](http://www.github.com/rubyops/httperfrb/)

## Usage - HTTPerf::Grapher

        httperf_graph = HTTPerf::Grapher.new
        httperf_graph.output_file = "/tmp/httperf_graph.png"
        
        #
        # httperf_graph.graph_settings = { ... overide Gruff defaults }
        # 
       
        httperf_graph.graph( HTTPerf::Parser( httperf_verbose_results ) ) 

