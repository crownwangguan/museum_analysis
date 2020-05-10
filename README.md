# Museum Vistors Analysis

To get the result:

1. Navigate to the folder and build the docker image: `docker build -t museum_analysis .`

2. After image has been built, run the container: `docker run -p 8888:8888 museum_analysis`

3. In the terminal there will be a url like: `http://127.0.0.1:8888/?token={your_token}`

4. In the jupyter notebook directory: **/work** you will find three `ipynb` file. To retrive the data run `musuem-data-retrival.ipynb` to load data into 2 sqlite files.

5. There are two solutions:
* `museum-analysis.ipynb` use **`Pandas`** to analyse the correlation between city population and number of museums visitors. The advantage of using Pandas is simpler, more flexible, more libs, and easier to implement algorithm.
* `museum_analysis_spark.ipynb` use **`Spark`** to analyse the data. Not like Pandas can only use single machine only scale up, Spark can scale out, the more worker node you have, the better performance.