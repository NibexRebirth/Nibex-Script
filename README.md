<article class="markdown-body entry-content" itemprop="text"><p><a target="_blank" rel="noopener noreferrer" href="https://camo.githubusercontent.com/7b31b628ecbc45dd5739a3b56bf579e40183aa82/68747470733a2f2f63646e2e646973636f72646170702e636f6d2f6174746163686d656e74732f3436303830333834353631343836323333372f3436323130353739343439383738393337362f4e696265782e706e67"><img src="https://camo.githubusercontent.com/7b31b628ecbc45dd5739a3b56bf579e40183aa82/68747470733a2f2f63646e2e646973636f72646170702e636f6d2f6174746163686d656e74732f3436303830333834353631343836323333372f3436323130353739343439383738393337362f4e696265782e706e67" alt="" data-canonical-src="https://cdn.discordapp.com/attachments/460803845614862337/462105794498789376/Nibex.png" style="max-width:100%;"></a></p>
<h1><a id="user-content-nibex-v23-masternode-setup-guide--ubuntu-1604-" class="anchor" aria-hidden="true" href="#nibex-v23-masternode-setup-guide--ubuntu-1604-"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Nibex v2.3 Masternode Setup Guide [ Ubuntu 16.04 ]</h1>
<p>THIS GUIDE IS FOR ROOT USERS -</p>
<p>YOU MUST BE A MEMBER OF THE FOLLOWING GROUP</p>
<pre><code>User=root
Group=root
</code></pre>
<p>Shell script to install a <a href="https://www.nibex.io/" rel="nofollow">Nibex Masternode</a> on a Linux server running Ubuntu 16.04. Use it on your own risk.</p>
<hr>
<h2><a id="user-content-private-key" class="anchor" aria-hidden="true" href="#private-key"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Private Key</h2>
<p><strong>This script can generate a private key for you, or you can generate your own private key on the Desktop software.</strong></p>
<p>Steps generate your own private key.</p>
<ol>
<li>Download and install Nibex v2.3 for Windows -   Download Link  - <a href="https://github.com/NibexRebirth/nibex/releases">https://github.com/NibexRebirth/nibex/releases</a></li>
<li>Go to <strong>Tools -&gt; Click "Debug Console"</strong></li>
<li>Type the following command: <strong>masternode genkey</strong></li>
<li>You now have your generated <strong>Private Key</strong>  (MasternodePrivKey)</li>
</ol>
<h2><a id="user-content-vps-installation" class="anchor" aria-hidden="true" href="#vps-installation"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>VPS installation</h2>
<pre><code>wget -q https://github.com/NibexRebirth/Nibex-Script/raw/master/nibex-install.sh
bash nibex-install.sh
</code></pre>
<p>Once the VPS installation is finished.</p>
<p>Check the block height</p>
<p>We want the blocks to match whats on the Nibex block explorer (<a href="http://explorer.nibex.io/" rel="nofollow">http://explorer.nibex.io/</a>)</p>
<p>Once they match you can proceed with the rest of the guide.</p>
<p>Check the block height with the following command</p>
<pre><code>watch nibex-cli getinfo
</code></pre>
<p>Make sure the version number matches.</p>
<pre><code>"version" : 2030000,     ------------------This is the latest version (Nibex v2.3)
</code></pre>
<p>Once the block height matches the block explorer issue the following command.</p>
<pre><code>CTRL and C  at the same time  (CTRL KEY and C KEY)
</code></pre>
<hr>
<h2><a id="user-content-desktop-wallet-setup" class="anchor" aria-hidden="true" href="#desktop-wallet-setup"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Desktop wallet setup</h2>
<p>After the MN is up and running, you need to configure the desktop wallet accordingly. Here are the steps:</p>
<ol>
<li>Open the Nibex Desktop Wallet.</li>
<li>Go to RECEIVE and create a New Address: <strong>MN1</strong></li>
<li>Send <strong>5000</strong> Nibex to <strong>MN1</strong>. You need to send 5000 coins in one single transaction.</li>
<li>Wait for 15 confirmations.</li>
<li>Go to <strong>Tools -&gt; Click "Debug Console"</strong></li>
<li>Type the following command: <strong>masternode outputs</strong></li>
<li>Go to  <strong>Tools -&gt; "Open Masternode Configuration File"</strong></li>
<li>Add the following entry:</li>
</ol>
<pre><code>Alias Address Privkey TxHash TxIndex
</code></pre>
<h2><a id="user-content-sample-of-how-your-masternodeconf-should-look-like--this-should-all-be-on-one-line" class="anchor" aria-hidden="true" href="#sample-of-how-your-masternodeconf-should-look-like--this-should-all-be-on-one-line"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>SAMPLE OF HOW YOUR MASTERNODE.CONF SHOULD LOOK LIKE.  (This should all be on one line)</h2>
<pre><code>MN1 127.0.0.2:11122 93HaYBVUCYjEMeeH1Y4sBGLALQZE1Yc1K64xiqgX37tGBDQL8Xg 2bcd3c84c84f87eaa86e4e56834c92927a07f9e18718810b92e0d0324456a67c 0
</code></pre>
<ul>
<li>Alias: <strong>MN1</strong></li>
<li>Address: <strong>VPS_IP:PORT</strong></li>
<li>Privkey: <strong>Masternode Private Key</strong></li>
<li>TxHash: <strong>First value from Step 6</strong></li>
<li>TxIndex:  <strong>Second value from Step 6</strong></li>
</ul>
<ol start="9">
<li>Save and close the file.</li>
<li>Go to <strong>Masternode Tab</strong>.
If you tab is not shown, please enable it from: <strong>Settings - Options - Wallet - Show Masternodes Tab</strong></li>
<li>Click <strong>Update status</strong> to see your node. If it is not shown, close the wallet and start it again.</li>
<li>Select your MN and right click on the masternode <strong>Start Alias</strong> to start it.</li>
<li>Alternatively, open <strong>Debug Console</strong> and type:</li>
</ol>
<pre><code>startmasternode alias 0 MN1 
</code></pre>
<ol start="14">
<li>Login to your VPS and check your masternode status by running the following command:.</li>
</ol>
<pre><code>nibex-cli masternode status
</code></pre>
<p>You want to see <strong>"Masternode started successfully and Status 4"</strong></p>
<hr>
<h2><a id="user-content-usage" class="anchor" aria-hidden="true" href="#usage"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Usage:</h2>
<pre><code>nibex-cli masternode status  
nibex-cli getinfo
</code></pre>
<p>Also, if you want to check/start/stop <strong>Nibex</strong>, run one of the following commands as <strong>root</strong>:</p>
<pre><code>systemctl status Nibex.service          #To check if Nibex service is running  
systemctl start Nibex.service           #To start Nibex service  
systemctl stop Nibex.service           #To stop Nibex service  
systemctl is-enabled Nibex.service      #To check if Nibex service is enabled on boot  
</code></pre>
</article>
