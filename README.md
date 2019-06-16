# FileBot-Custom-Format-Expressions
```python
E:\Filme\{
	def dottedName = n.space('.')
	any{"$collection/$y.$dottedName.$vf.$vc"}
	{
		def tmpGenre = ""
		if(genres.contains("Documentary") || genres.contains("Dokumentation")) {
			tmpGenre = "Doku"
		}else if(genres.contains("Comedy")) {
			tmpGenre = "Comedy"
		}else if(genres.contains("Animation")) {
			tmpGenre = "Animation"
		}else if(genres.contains("Action")) {
			if(genres.contains("Adventure") || genres.contains("Abenteuer")) {
				tmpGenre = "Action-Adventure"
			}else if(genres.contains("Komödie")) {
				tmpGenre = "Action-Komödie"
			}else if(genres.contains("Drama")) {
				tmpGenre = "Action-Drama"
			}else if(genres.contains("Thriller")) {
				tmpGenre = "Action-Thriller"
			}else {
				tmpGenre = "Action"
			}
		}else if(genres.contains("Science Fiction")) {
			tmpGenre = "Sci-Fi"
		}else if(genres.contains("Drama")) {
			if(genres.contains("Thriller")) {
				tmpGenre = "Drama-Thriller"
			}else {
				tmpGenre = "Drama"
			}
		}else if(genres.contains("Horror")) {
			if(genres.contains("Thriller")) {
				tmpGenre = "Horror-Thriller"
			}else {
				tmpGenre = "Horror"
			}
		}else {
			tmpGenre = genre
		}
		"Genre/$tmpGenre/$dottedName.$y.$vf.$vc"
	}
}
```
