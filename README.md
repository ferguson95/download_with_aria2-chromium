# What is this

- This extension is a completely rewritten version of [chrome-aria2-integration](https://github.com/robbielj/chrome-aria2-integration)

# Firefox Quantum

- Visit [Download with Aria2 Firefox](https://github.com/jc3213/download_with_aria2-firefox)

# Differences

Extension options
<details>
  Don't open <b>Options<b> in new tab
  <br>Ability to check for <b>JSONRPC URI</b> and <b>Secret Token</b>
  <br>Ability to modify <b>User Agent</b> for downloads
  <br>Ability to set <b>all-proxy</b> option for downloads automatically
  <br>Capture filters now have better logic, and better performance
  <br>Priority of filters: <b>Ignored Domains</b> > <b>Monitored Domains</b> > <b>File Extensions</b> > <b>File Sizes</b>
</details>
Extension task managers
<details>
  Show <b>Active</b>, <b>Waiting</b>, <b>Stopped</b> task counts
  <br>Ability to filter task queues based on their status
  <br>Show global <b>Download</b>, <b>Upload</b> speed
  <br>Better <b>progress bar</b>, click to pause or unpause the task
  <br><b>Options</b> button to open <b>Options</b> instantly
  <br>Show error message if an error happens while contacting with <b>Aria2 jsonrpc</b>
  <br>Click <b>❌</b> to stop current task or remove download result
  <br>Click <b>🔍</b> to to open <b>taskDetails</b> window for more detailed infomations
  <br>Click <b>🌌</b> to restart <b>removed</b> or <b>error<b> non-bittorrent downloads
</details>
Better performance and accessbility
<details>
    <br>Full modularization
    <br>New icons
    <br>Native i18n supports
    <br>New library <b>jQuery-3.5.1.min.js</b>
    <br>Removed libraries <b>fancysettings.js</b>, <b>store.js</b>, <b>i18n.js</b>, and <b>popuplib.min.js</b>
    <br>Removed unnecessary <b>*.js</b>, <b>chrome</b> api and <b>manifest</b> key usage
    <br>Better notifications
</details>

# How to use

Options.html
<details>
    <b>Basic</b>
    <details>
        <b>JSONRPC URI</b> - Url of your Aria2 jsonrpc
        <br><b>Secret Token</b> - Secret token of your Aria2 jsonrpc
    </details>
    <b>Advanced</b>
    <details>
        <b>User Agent</b> - You can modified user agent for every download
        <br><b>All Proxy</b> - Url of http or https protocol proxy services
        <br><b>Domains over Proxy</b> - Domains that needs a proxy service to download (auto-proxy profile)
    </details>
    <b>Download</b>
    <details>
        <b>Capture</b> - Ability to capture downloads from browser
        <details>
            <b>File Size</b> - Filter downloads based on file size
            <br><b>File Extensions</b> - Filter downloads based on file extensions
            <br><b>Monitored Domains</b> - Capture downloads from listed domains
            <br><b>Ignored Domains</b> - Ignore downloads from listed domains
        </details>
    </details>
</details>
Popup.html
<details>
    <b>Top Menu</b>
    <details>
        <b>Tabs with Status</b>
            <details>
            <b>Active</b> - Filter only active downloads on <b>Task Manager</b>
            <br><b>Waiting</b> - Filter downloads those are paused or still in queue
            <br><b>Stopped</b> - Filter downloads stopped or completed
            </details>
        <b>New</b> - Open <b>New Task Window</b>
            <details>
                <b>New Task Window</b>
                <details>
                    <b>Referer</b> - Change the referer of current download session
                    <br><b>Download Url</b> - Input the urls of current download session
                    <br><b>Use Proxy</b>
                    <details>
                        <b>checkbox</b> - Add <b>all-proxy</b> option to current download session (Only once)
                        <br><b>textarea</b> - Change proxy service of current download session (Only once)
                    </details>
                </details>
            </details>
        <br><b>Purdge</b> - Purdge all downloads that are completed or stopped
        <br><b>Cancel</b> - Close the <b>New Task Window</b>
    </details>
    <b>Task Manager</b>
    <details>
        <b>❌</b> - Stop downloading task or remove stopped task from <b>Task Manager</b>
        <br><b>🔍</b> - Click to show current <b>Task Details</b>
        <br><b>🌌️</b> - Restart <b>removed<b> or <b>error</b> non-bittorrent downloads
        <br><b>Progress Bar</b> - Click to pause or unpause targeted download
    </details>
    <b>Task Details</b>
    <details>
        <b>Task Name</b> - Click to close <b>Task Details</b> window
        <br><b>Max Download Speed</b> - Ability to limit the max download speed of current download
        <br><b>Max Upload Speed</b> - Ability to limit the max upload speed of current download
        <br><b>Proxy Server</b> - Ability to change proxy server of current download
        <br>
        <br><b>TaskFiles></b> - Files of current download, click to copy uri for non-bittorrent download
    </details>
    <b>Bottom Menu</b>
    <details>
        <b>Download Speed</b> - Global download speed
        <br><b>Upload Speed</b> - Global updload speed
        <br><b>Option</b> - Open <b>Options.html</b>
    </details>
</details>

# Disadvantages

- Neither `Google Web Store`, nor `Microsoft Store` supports
  - My country has blocked all `Google` services
  - `Google` has a $5 fee, and `Microsoft` has a $18 fee
- Embedded `popup.html` may not be powerful enough for advanced users
  - Alternative [`Aria2 WebUI`](https://ziahamza.github.io/webui-aria2/) or [`Yet Another Aria2 Web Frontend`](http://binux.github.io/yaaw/demo/)
