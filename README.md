HTTPerf::Grapher
================

### [Documentation](http://rubyops.github.com/httperfrb-grapher/doc/) | [Coverage](http://rubyops.github.com/httperfrb-grapher/coverage/) | [RSpec Out](https://github.com/rubyops/httperfrb-grapher/blob/master/RSPECOUT.md)


### WARNING

This isn't working in all cases. It was designed to queue off of "Connection lifetime = ", which is avaiable in a specific installation of httperf I have been using that wasn't set up by me. However, I'm starting to think that this installation was hacked to include this output. Most standard installations that I've tested this code with fail, because this string isn't output. So I may have to abandon this effort.

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

