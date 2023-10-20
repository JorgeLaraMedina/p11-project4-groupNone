<script>
    const url =
        "https://api.themoviedb.org/3/discover/movie?include_adult=false&include_video=false&language=en-US&page=1&sort_by=popularity.desc";
    const options = {
        method: "GET",
        headers: {
            accept: "application/json",
            Authorization:
                "Bearer eyJhbGciOiJIUzI1NiJ9.eyJhdWQiOiI1NTM2MjFmMDNkMDQxOWU4ZGJkZjU3Mjc5NzAyMTY2NCIsInN1YiI6IjY1MzIyYzY0ZWZlMzdjMDBjN2ViZGIwNyIsInNjb3BlcyI6WyJhcGlfcmVhZCJdLCJ2ZXJzaW9uIjoxfQ.4OEYfdzVj5-SNTVWUsZOiMdb3Vu0g-RRaZNIa_0JSW8",
        },
    };

    let movies = [];

    fetch(url, options)
        .then((response) => response.json())
        .then(data => movies = data.results )
        .catch((err) => console.error(err));
</script>
<div>
{#each movies as movie }
<img alt="caratula"src={`https://image.tmdb.org/t/p/original/${movie.poster_path}`}>
{/each}
</div>

<style>
   img{
    height:331px;
    width:226px;
    object-fit:cover;
    margin-top:100px;
   }
   div{
    display: flex;
    justify-content:center;
    flex-wrap:wrap;
    gap: 15px;
   }
</style>