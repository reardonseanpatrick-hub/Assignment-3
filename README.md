# Assignment-3

<img width="557" height="933" alt="Screenshot 2026-03-31 195542" src="https://github.com/user-attachments/assets/702da40f-8646-4428-9e80-926c3a7b1664" />
<img width="556" height="776" alt="Screenshot 2026-03-31 195731" src="https://github.com/user-attachments/assets/3f18eebb-c68c-4c14-bedb-bb020d51feb7" />

db["movies"].find({ 
    year: 1983, 
    runtime: { $gt: 200 } 
  },
  { 
    runtime: 1, 
    title: 1, 
    year: 1, 
    _id: 0 
  }
).sort({ runtime: 1 })

db["movies"].find({ 
    year: { $gt: 2014 }, 
    "imdb.rating": { $gt: 9 } 
  },
  { 
    title: 1, 
    year: 1, 
    "imdb.rating": 1, 
    _id: 0 
  }
)
