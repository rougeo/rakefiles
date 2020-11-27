task :default => :jenkins

task :rougeo =>[:jenkins, :hello_world] do
    puts 'Running all listed tasks before this one'
end

desc "Print Hello world"
task :hello_world do
    puts 'Hello World'
end  

task :factorial do
    n =(ENV['N'] || 10).to_i
    fact = 1
    (1..n).each do |i|
        fact = fact * i
    end 
    puts "Factorial of #{n} is #{fact}"
end

namespace :gideon do
    task:jenkins do
        puts 'Bonjour Jenkins'
        sh 'docker images'
    end
end

# check fileUtils methods
# check fileUtils methods

#Use env variable
# STUFF=hello rake show_stuff
# rake show_stuff STUFF=hello 
task :show_stuff do
    puts "STUFF = #{ENV['STUFF']}"
end

# Commands
# rake -P
## Show description if added "desc"
# rake -T [pattern start]
## -W where work for documented task
# rake -W hello_world
