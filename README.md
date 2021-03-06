# assignment2--Adhikari
Assignment-2 Web Apps
# Bikash Adhikari
#### Kathmandu, Nepal
**Kathmandu Nepal is my birthplace**. It is the capital city of Nepal and I was born in the suburb of Kathmandu. The valley of Kathmandu is located in the middle of country Nepal in the Asian continent. It is surrounded by mountains on all sides. I love Kathmandu because it is my birthplace and because of it's deep **historical and cultural significance**. 

***

# Directions to Kathmandu from Maryville
1. Book two flight tickets.
    1. From Kansas City International Airport(MCI) to Los Angeles International Airport(LAX)
    2. From LAX to Kathmandu International Airport (KTM).
2. Take a taxi from Maryville to the Kansas City International Airport(MCI).
    1. You can use Maryvile Taxi Service.
3. Get on the flight to Los Angeles International Airport(LAX).
    1. At LAX go from Domestic Terminal to International Terminal.
    2. Check your bags and get on the flight.
4. After arriving at Kathmandu, you can get a taxi from the airport to get around. 

#### Things to bring
* Warm Clothes
    * Jackets
    * Hats
    * Gloves
* Camera
* Snacks from US

[AboutMe](https://github.com/bikash30851/assignment2-Adhikari/blob/main/AboutMe.md)

***

### Food and Drinks Recommendation
In the table below, I have included 4 foods and drinks that I would like to recommend. I have inclued a few foods and drinks from my tradition and some from foreign cultures that I have eaten in the past. 

| Food/drink | Location | Cost |
| --- | --- | --- |
| Momo | Kathmandu | 60 Cents |
| Chat | Delhi | 40 Cents |
| Pizza | Italy | 30 Dollars |
| Ichiraku | Tokyo | 40 Dollars |
| Hamburger | USA | 5 Dollars |

***

### Favorite Quotes
>Hope is a good thing, maybe the best of things, and no good thing ever dies. *-Andy Dufresne* 
>
>The first wealth is health. *-Ralph Waldo Emerson*

***

### Algorithm

>In mathematics, Gaussian elimination, also known as row reduction, is an algorithm for solving systems of linear equations. It consists of a sequence of operations performed on the corresponding matrix of coefficients. This method can also be used to compute the rank of a matrix, the determinant of a square matrix, and the inverse of an invertible matrix. 
Source: <https://en.wikipedia.org/wiki/Gaussian_elimination>

```
const double EPS = 1E-9;
int n;
vector < vector<double> > a (n, vector<double> (n));

double det = 1;
for (int i=0; i<n; ++i) {
    int k = i;
    for (int j=i+1; j<n; ++j)
        if (abs (a[j][i]) > abs (a[k][i]))
            k = j;
    if (abs (a[k][i]) < EPS) {
        det = 0;
        break;
    }
    swap (a[i], a[k]);
    if (i != k)
        det = -det;
    det *= a[i][i];
    for (int j=i+1; j<n; ++j)
        a[i][j] /= a[i][i];
    for (int j=0; j<n; ++j)
        if (j != i && abs (a[j][i]) > EPS)
            for (int k=i+1; k<n; ++k)
                a[j][k] -= a[i][k] * a[j][i];
}

cout << det;
```
Code Source: <https://cp-algorithms.com/linear_algebra/determinant-gauss.html>


