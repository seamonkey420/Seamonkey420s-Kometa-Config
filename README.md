# Seamonkey420s-PlexMetaManager-Config
My personal Plex Meta Manager config and setup.  

IMDB collections for Movies and TV Shows:  Top 250, Popular, Trending

Rotten Tomatoes collections for Movies: Best of 2010s, 2000s, 1990s, 1980s

Trakt collections for Movies: Popular, Trending

TMDB collections for TV Shows and Cartoons: Top 250, Popular, Trending

IMDB and TMDB score overlays for Movies, TV Shows, Cartoons

4K overlay for 4K movies (including 4K DV, 4K HDR) for 4K movies

IMDB Top 250 Overlay for Movies, TV Shows, Cartoons

Decade collections for Cartoons

See config.yml for examples on how to use.  See very bottom of page for how to call a specific .yml to run vs the default config.yml


Screenshot examples below:

![pmm movies collections](https://user-images.githubusercontent.com/6142436/214715369-2cd1b228-bd77-4a4a-81c9-8dcce753bdd4.png)

![pmm IMDB overlays](https://user-images.githubusercontent.com/6142436/214715368-8c0e4b83-56ee-4d32-b6c8-7c029c3d5711.png)

![pmm tv shows overlays](https://user-images.githubusercontent.com/6142436/214715365-19505dbf-d775-469f-9bb1-012d3665b4df.png)

![pmm cartoons collections and tmdb overlay](https://user-images.githubusercontent.com/6142436/214715367-001a3687-181e-40b8-a123-6f67b2606e27.png)

![pmm 4K overlay](https://github.com/seamonkey420/Seamonkey420s-PlexMetaManager-Config/assets/6142436/c2f04e60-d5cf-4dec-a311-c3e8c92ab0ee)


Running a custom .yml via SSH/Putty on a docker PMM instance:

--4K movies in a config-4k.yml located in same config folder as the default config.yml

docker run --rm -it -v "/volume1/docker/pmm:/config:rw" meisnate12/plex-meta-manager --config "/config/config-4k.yml" --run

Running a specific .yml as a task on a schedule in Synology DSM7.x as a task (run task as root):

docker run --rm -v "/volume1/docker/pmm:/config:rw" meisnate12/plex-meta-manager --config "/config/config-4k.yml" --run

Running a specific .yml via docker terminal on a synology:

python plex_meta_manager.py --config /config/config-4k.yml

Running PMM via docker terminal on a synology (default config.yml):

python plex_meta_manager.py -r
