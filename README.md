<img src="https://avatars3.githubusercontent.com/u/51751524?s=400" width="100" alt="" data-canonical-src="https://avatars2.githubusercontent.com/u/48458546?s=460&v=4g">  &nbsp;&nbsp;
<img src="https://monetizegame.com/images/unity3d-logo.png" width="100" alt="" data-canonical-src="https://monetizegame.com/images/unity3d-logo.png">


# MonetizeGame.com-SDK WebGL Unity3D
This repository contains the MonetizeGame.com SDK for WebGL Unity3D games. This allows you to display advertisements in the games published within the MonetizeGame.com network. https://MonetizeGame.com

# STEP 1:
<p><a href="https://drive.google.com/file/d/1MGHAdbfih_l7J0UbAzm_zt2rEW8yq3M-/">Download the plugin</a> and Import the .unitypackage into your game. </p>
<p>Download here: <a href="https://drive.google.com/file/d/1MGHAdbfih_l7J0UbAzm_zt2rEW8yq3M-/">https://drive.google.com/file/d/14i-5GiS18akqbeEzFTcnOuA4H0WAkHmf/</a></p>

<p><img src="https://monetizegame.com/images/unity/unity_2.png"  width="800" alt=""></p>

# STEP 2:
Drag the prefab "MonetizeGame" into your scene. 

# STEP 3:
Copy your GAME_ID in your MonetizeGame developer's control panel (in the Game Management > My games > Our game), at https://MonetizeGame.com/account/

# STEP 4:
Open the prefab and replace the GAME_ID values with your own keys. 
<p><img src="https://monetizegame.com/images/unity/unity_1.png"  width="800" alt=""></p>

# STEP 5:
Use MonetizeGame.Instance.ShowAd() to show an advertisement. 

# STEP 6:
Make use of the events MonetizeGame.OnResumeGame and MonetizeGame.OnPauseGame for resuming/pausing your game in between ads.

# Example:
<pre>public class ExampleClass: MonoBehaviour {
	void Awake()
	{
	  MonetizeGame.OnResumeGame += ResumeGame;
	  MonetizeGame.OnPauseGame += PauseGame;
	}
	
	void OnDestroy()
	{
	  MonetizeGame.OnResumeGame -= ResumeGame;
	  MonetizeGame.OnPauseGame -= PauseGame;
	}

	public void ResumeGame()
	{
	  // RESUME MY GAME
	}

	public void PauseGame()
	{
	  // PAUSE MY GAME
	}

	public void ShowAd()
	{
	  MonetizeGame.Instance.ShowAd();	
	}
}</pre>

# FAQ
<h2>How to upload a game files?</h2>
<p><b>Answer</b>: When your game is ready to upload, you need to compress all game files to .ZIP file - Root folder of .ZIP file must include index.html and game files</p>
<h2><b>Implementation self-hosted games.</b></h2>
<p>In the case where a developer wants to self-host their game, please contact us on at: info@monetizegame.com</p>

# Support:
If you have any technical questions or comments, please email us at:
info@monetizegame.com

Or simply check documentation on:
https://monetizegame.com/sdk
