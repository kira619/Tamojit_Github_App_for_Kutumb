Screenshots


![image](https://user-images.githubusercontent.com/68930973/149575260-5909b3fe-f498-4024-a603-1ae2a8685f1d.png)
![screenshot1](https://user-images.githubusercontent.com/68930973/149575175-7a1ab106-4f74-4852-9b8e-fedf273e930b.png)
![image](https://user-images.githubusercontent.com/68930973/149575278-14496aea-1ee3-421d-87fc-0aab10c7b01c.png)














# Github Trending/
An android app that shows trending repositories and developers, fetching
results from <https://github-trending-api.now.sh>

This App was developed as a part of the the assignment for the recruitment process of Kutumb.
 

 
## Project Structure
The project consists of two modules
- **app**  
  The Android app with screens for trending repos and devs
- **libTrendingGithub**  
  A java-library that implements the API

### app

#### UI

The app has two activities -
- Trending Lists  
  This has a bottom-bar based navigation, and has 3 fragments
  - Trending Repositories
  - Trending Developers
  - Languages
- Repository Details  
  This is opened when clicking a repository in the list for details


#### Libraries Used
- **Android Jetpack**  
  RecyclerView, CardView, Fragments, BottomNaviation
- **Glide** (image rendering)

#### Test Setup

There are tests for UI as well as for ViewModels
For testing please run

```sh
./gradlew connectedCheck
```

### libTrendingGithub

#### Libraries Used
- **OkHttp**
- **Moshi** (JSON de/serialisation)
- **Reotrofit**

#### Test Setup
There are unit tests with 100% coverage. '

To run tests use

```sh
./gradlew :libTrendingGithub:test
```

We have both real (flaky) tests and tests with OkHttp's MockWebServer
The `assets` folder contains sample responses used in mock tests.

Gradle configuration creates a `test.jar` file too that can be
used in consuming modules (like the app) to test against the mock
server and responses. 
#GiveMeJob
