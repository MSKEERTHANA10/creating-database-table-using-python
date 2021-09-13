# creating-database-table-using-python
# creating database and diplaying all the rows
import mysql.connector
mydb = mysql.connector.connect (
	host = "localhost",
	user = "teenu",
	password = "teenu",
	database = "moviesdb"
	)
mycursor = mydb.cursor()

mycursor.execute("CREATE TABLE movies(movie_name VARCHAR(40), actor VARCHAR(20), actress VARCHAR(20), year_of_release INT, director VARCHAR(20))")

mycursor.execute("INSERT INTO movies VALUES(%s, %s, %s, %s, %s)", ("MASTER", "VIJAY", "MALAVIKA_MOHANAN", 2021, "LOKESH_KANAGARAJ"))
mycursor.execute("INSERT INTO movies VALUES(%s, %s, %s, %s, %s)", ("JILLA", "VIJAY", "KAJAL_AGGARWAL", 2014, "R.T.NEASON"))
mycursor.execute("INSERT INTO movies VALUES(%s, %s, %s, %s, %s)", ("GHILLI", "VIJAY", "TRISHA", 2004, "DHARANI"))
mycursor.execute("INSERT INTO movies VALUES(%s, %s, %s, %s, %s)", ("SIRUTHAI", "KARTHI", "TAMANNA_BHATIA", 2011, "VIDYASAGAR"))
mycursor.execute("INSERT INTO movies VALUES(%s, %s, %s, %s, %s)", ("SULTAN", "KARTHI", "RASHMIKA_MANDANNA", 2021, "BAKKIYARAJ_KANNAN"))
mycursor.execute("INSERT INTO movies VALUES(%s, %s, %s, %s, %s)", ("SOORARAI_POTTRU", "SURIYA", "APARNA_BALAMURALI", 2021, "SUDHA_KONGARA_PRASAD"))

mydb.commit()

mycursor.execute("SELECT * FROM movies")

for i in mycursor:
	print(i)


# creating database and displaying specific rows
import mysql.connector
mydb = mysql.connector.connect (
	host = "localhost",
	user = "teenu",
	password = "teenu",
	database = "moviesdb"
	)
mycursor = mydb.cursor()

mycursor.execute("CREATE TABLE movies(movie_name VARCHAR(40), actor VARCHAR(20), actress VARCHAR(20), year_of_release INT, director VARCHAR(20))")

mycursor.execute("INSERT INTO movies VALUES(%s, %s, %s, %s, %s)", ("MASTER", "VIJAY", "MALAVIKA_MOHANAN", 2021, "LOKESH_KANAGARAJ"))
mycursor.execute("INSERT INTO movies VALUES(%s, %s, %s, %s, %s)", ("JILLA", "VIJAY", "KAJAL_AGGARWAL", 2014, "R.T.NEASON"))
mycursor.execute("INSERT INTO movies VALUES(%s, %s, %s, %s, %s)", ("GHILLI", "VIJAY", "TRISHA", 2004, "DHARANI"))
mycursor.execute("INSERT INTO movies VALUES(%s, %s, %s, %s, %s)", ("SIRUTHAI", "KARTHI", "TAMANNA_BHATIA", 2011, "VIDYASAGAR"))
mycursor.execute("INSERT INTO movies VALUES(%s, %s, %s, %s, %s)", ("SULTAN", "KARTHI", "RASHMIKA_MANDANNA", 2021, "BAKKIYARAJ_KANNAN"))
mycursor.execute("INSERT INTO movies VALUES(%s, %s, %s, %s, %s)", ("SOORARAI_POTTRU", "SURIYA", "APARNA_BALAMURALI", 2021, "SUDHA_KONGARA_PRASAD"))

mydb.commit()

mycursor.execute("SELECT * FROM movies WHERE actor='vijay' ")

for i in mycursor:
	print(i)
