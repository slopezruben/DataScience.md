# Data Acquisition:
    - Loading data from various sources
    - Consider
        - Format (csv, json, etc)
        - File Path (where is on our computer or the internet)

    - For pandas,
        - csv -> read_csv()
        ```python
            import pandas as pd
            url = "..."
            df = pd.read_csv(url, header = "") // Allows for header or no header

            df.head() // cabesa
            df.tail() // Final del df

            headers = [...]
            df.columns = headers // set headers for headerless panda

            path = "..."
            df.to_csv(path)     // save df.
        ```


