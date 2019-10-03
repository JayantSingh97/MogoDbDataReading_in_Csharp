# MogoDbDataReading_in_Csharp
MogoDbDataReading_in_Csharp


# MogoDb operations in c#

        public void Connect_TO_Mongo_server(string MongoServer)
        {
            MongoClient client = new MongoClient("mongodb://" + MongoServer);
            var db = client.GetDatabase("DB"); 
            var CollectionsName =  db.ListCollectionNames();
            var CollactionData = db.GetCollection<ClickTrackMonitor>("CollectionName");
            var CollactionAsList = db.GetCollection<ClickTrackMonitor>("CollectionName").AsQueryable();


            foreach (var item in CollactionAsList)
            {
                
            }
             
             
            // Now collection has been retrived from mongo serer and available in c# object for further use.
         }
