HTTPerf::Grapher
================

### [Documentation](http://rubyops.github.com/httperfrb-grapher/doc/) | [Coverage](http://rubyops.github.com/httperfrb-grapher/coverage/) | [RSpec Out](https://github.com/rubyops/httperfrb-grapher/blob/master/RSPECOUT.md)


### WARNING

This isn't working in all cases. 

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
       
        httperf_graph.graph( HTTPerf::Parser( httperf_results ) ) 

