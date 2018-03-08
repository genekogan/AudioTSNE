This is a simple program to display and loop through a t-SNE layout of audio samples in [Processing](http://processing.org). It also requires the Minim library for Processing which can be installed from the libraries menu.

It comes with an example, Queen's "Bohemian Rhapsody" which has been segmented with the resulting audio chunks analyzed, and t-SNEd.  

If you'd like to generate your own t-SNE layout with another audio source, you may generate one using the python script [found here](https://github.com/ml4a/ml4a-guides/blob/master/notebooks/audio-tsne.ipynb). 

If you generate your own t-SNE layout from this Python script, these lines of code in AudioTSNE.pde should be changed from:

    float x = entry.getFloat("x");
    float y = entry.getFloat("y");
    
to:

    JSONArray points = entry.getJSONArray("point");
    float x = points.getFloat(0);
    float y = points.getFloat(1);
