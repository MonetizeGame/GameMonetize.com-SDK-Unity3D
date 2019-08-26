<img src="https://avatars1.githubusercontent.com/u/54474115?s=460&v=4" width="100" alt="" data-canonical-src="https://avatars1.githubusercontent.com/u/54474115?s=460&v=4">  &nbsp;&nbsp;
<img src="https://gamemonetize.com/images/unity3d-logo.png" width="100" alt="" data-canonical-src="https://gamemonetize.com/images/unity3d-logo.png">


# GameMonetize.com-SDK WebGL Unity3D
This repository contains the GameMonetize.com SDK for WebGL Unity3D games. This allows you to display advertisements in the games published within the GameMonetize.com network. https://GameMonetize.com

# STEP 1:
<p><a href="https://drive.google.com/file/d/1BrJ0MuNBWh7_hoNRIEXw9exgqpE1uQZh/">Download the plugin</a> and Import the .unitypackage into your game. </p>
<p>Download here: <a href="https://drive.google.com/file/d/1BrJ0MuNBWh7_hoNRIEXw9exgqpE1uQZh/">https://drive.google.com/file/d/1BrJ0MuNBWh7_hoNRIEXw9exgqpE1uQZh/</a></p>

<p><img src="https://gamemonetize.com/images/unity3d/unity1.png"  width="800" alt=""></p>

# STEP 2:
Drag the prefab "GameMonetize" into your scene. 

# STEP 3:
Copy your GAME_ID in your GameMonetize developer's control panel (in the Game Management > My games > Our game), at https://gamemonetize.com/account/

# STEP 4:
Open the prefab and replace the GAME_ID values with your own keys. 
<p><img src="https://gamemonetize.com/images/unity3d/unity2.png"  width="800" alt=""></p>

# STEP 5:
Use GameMonetize.Instance.ShowAd() to show an advertisement. 

# STEP 6:
Make use of the events GameMonetize.OnResumeGame and GameMonetize.OnPauseGame for resuming/pausing your game in between ads.

# Example:
<pre>public class ExampleClass: MonoBehaviour {
	void Awake()
	{
	  GameMonetize.OnResumeGame += ResumeGame;
	  GameMonetize.OnPauseGame += PauseGame;
	}
	
	void OnDestroy()
	{
	  GameMonetize.OnResumeGame -= ResumeGame;
	  GameMonetize.OnPauseGame -= PauseGame;
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
	  GameMonetize.Instance.ShowAd();	
	}
}</pre>

# FAQ
<h2>How to upload a game files?</h2>
<p><b>Answer</b>: When your game is ready to upload, you need to compress all game files to .ZIP file - Root folder of .ZIP file must include index.html and game files</p>
<h2><b>Implementation self-hosted games.</b></h2>
<p>In the case where a developer wants to self-host their game, please contact us on at: info@gamemonetize.com</p>

# Support:
If you have any technical questions or comments, please email us at:
info@gamemonetize.com

Or simply check documentation on:
https://gamemonetize.com/sdk
