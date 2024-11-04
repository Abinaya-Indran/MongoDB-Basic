Step 1: Create the Database

use movies

Step 2: Create a Collection

db.createCollection("moviedetails")

Step 3: Insert the Movie Documents

db.moviedetails.insertMany([
  { title: "Vikram", genre: "Drama", director: "Lokesh Kanakaraj", release_year: 2022 },
  { title: "Vettaiyan", genre: "Action", director: "Ganavel", release_year: 2024 },
  { title: "Kanguva", genre: "Fantasy", director: "Siva", release_year: 2025 },
  { title: "Leo", genre: "Action", director: "Lokesh Kanakaraj", release_year: 2023 },
  { title: "Vidamuyatchi", genre: "Thriller", director: "Magizh Thirumeni", release_year: 2025 }
])

Step 4: List All Documents

db.moviedetails.find()

Step 5: List Lokesh Kanakaraj’s Movies

db.moviedetails.find({ director: "Lokesh Kanakaraj" })

Step 6: List Lokesh Kanakaraj’s Movies Released in 2023

db.moviedetails.find({ director: "Lokesh Kanakaraj", release_year: 2023 })

Step 7: Delete the Movie You Don’t Like

Replace "Movie_Title" with the title of the movie you want to delete:

db.moviedetails.deleteOne({ title: "Movie_Title" })

Step 8: Add Your Favorite Movie
Replace "Your_Movie_Title", "Your_Genre", "Your_Director", and Your_Year with your favorite movie details:


db.moviedetails.insertOne({
  title: "Your_Movie_Title",
  genre: "Your_Genre",
  director: "Your_Director",
  release_year: Your_Year
})

Step 9: List the Movie Directed by Magizh Thirumeni in 2025

db.moviedetails.find({ director: "Magizh Thirumeni", release_year: 2025 })


Step 10: List Out All Director’s Names

db.moviedetails.distinct("director")











