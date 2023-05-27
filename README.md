This Jupyter Notebook demonstrates data manipulation and analysis using the Pandas library. The notebook focuses on processing a Spotify dataset.
Dataset

The dataset is stored in the file "spotify.csv". It is read into a Pandas DataFrame named df.
Data Manipulation

The following data manipulation steps are performed:

 Unnecessary columns ('Unnamed: 0', 'artist_ids', 'id', 'album_id') are dropped, resulting in the DataFrame core_df.
    Two DataFrames are created from core_df:
        song_df contains song-related columns and is indexed by 'song_id'.
        album_df contains album information and is indexed by 'album_id'.
    Duplicate albums are removed from album_df, and unique 'album_id' values are assigned to create unique_album.
    A filtered DataFrame filtered_df is created by selecting rows where the 'artists' column contains 'Kanye'.
    Two DataFrames, df1 and df2, are merged based on the 'ID' column to create merged_df.
    song_album is created by merging unique_album and album_df on the 'album' column, with the index renamed to 'song_id'.
    attributes_df is created by selecting specific columns related to song attributes from core_df.
    artist_df is created to extract and process artist information from the 'artists' column. The resulting DataFrame is exploded into all_artists.

Additional Tables

Apart from the data manipulation steps, an additional table named 'unique_artist' is created by extracting unique artists from artist_df.

Please note that the provided code snippets are for demonstration purposes and may require adjustments to suit specific use cases or datasets.
