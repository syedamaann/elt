what i've come to realise is that machine learning, deep learning or building ai applications is not possible without great data pipelines working behind the scenes. so, i've spent a weekend (and plan to spend a lot more) on learning deeply about data engineering. 

this repo is simple and seemingly straightforward, but what's interesting is this worked as a great exercise in understanding the intricacies of data engineering. let me outline some bits here for anyone interested (but most importantly, for my future reference):

- i started off with just the file structure: an empty elt_script, a compose file, an empty source db. that's it.  
- then wrote the compose file. kept it simple. just three services (source db, destination db, elt app) and a network connecting them.
- then it dawned upon me that i also need to populate the source db (else, what data would go through the pipeline). haha. so, filled the source data with some random movie data.
- then it was time to write the elt script. but before that, i thought having a dockerfile would be good. so did that.
- then, as expected, jumped onto the elt_script. did not wanted to spend a lot of time on the script so took an external reference and put it together. 

now that the things seemed a little okay, it was time to docker compose up --build! It worked just fine. I used postgres and now tested if i was able to get the data from the source db to the destination db. and yo, it worked :)

just a super basic pipeline, but had to start somewhere. i'll work on this further and complexify as i learn more about data engineering. wish me luck and i'm always open to help from kind souls who keep appearing every now and then to guide me on to the right path, i mean, right tech path, haha.
