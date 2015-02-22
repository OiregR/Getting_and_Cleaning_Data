


<!DOCTYPE html>
<html lang="en" class="">
  <head prefix="og: http://ogp.me/ns# fb: http://ogp.me/ns/fb# object: http://ogp.me/ns/object# article: http://ogp.me/ns/article# profile: http://ogp.me/ns/profile#">
    <meta charset='utf-8'>
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta http-equiv="Content-Language" content="en">
    
    
    <title>coursera-getting-and-cleaning-data/CodeBook.md at master · laurikoobas/coursera-getting-and-cleaning-data</title>
    <link rel="search" type="application/opensearchdescription+xml" href="/opensearch.xml" title="GitHub">
    <link rel="fluid-icon" href="https://github.com/fluidicon.png" title="GitHub">
    <link rel="apple-touch-icon" sizes="57x57" href="/apple-touch-icon-114.png">
    <link rel="apple-touch-icon" sizes="114x114" href="/apple-touch-icon-114.png">
    <link rel="apple-touch-icon" sizes="72x72" href="/apple-touch-icon-144.png">
    <link rel="apple-touch-icon" sizes="144x144" href="/apple-touch-icon-144.png">
    <meta property="fb:app_id" content="1401488693436528">

      <meta content="@github" name="twitter:site" /><meta content="summary" name="twitter:card" /><meta content="laurikoobas/coursera-getting-and-cleaning-data" name="twitter:title" /><meta content="coursera-getting-and-cleaning-data - https://class.coursera.org/getdata-003" name="twitter:description" /><meta content="https://avatars0.githubusercontent.com/u/861986?v=3&amp;s=400" name="twitter:image:src" />
      <meta content="GitHub" property="og:site_name" /><meta content="object" property="og:type" /><meta content="https://avatars0.githubusercontent.com/u/861986?v=3&amp;s=400" property="og:image" /><meta content="laurikoobas/coursera-getting-and-cleaning-data" property="og:title" /><meta content="https://github.com/laurikoobas/coursera-getting-and-cleaning-data" property="og:url" /><meta content="coursera-getting-and-cleaning-data - https://class.coursera.org/getdata-003" property="og:description" />
      <meta name="browser-stats-url" content="/_stats">
    <link rel="assets" href="https://assets-cdn.github.com/">
    <link rel="conduit-xhr" href="https://ghconduit.com:25035">
    <link rel="xhr-socket" href="/_sockets">
    <meta name="pjax-timeout" content="1000">
    <link rel="sudo-modal" href="/sessions/sudo_modal">

    <meta name="msapplication-TileImage" content="/windows-tile.png">
    <meta name="msapplication-TileColor" content="#ffffff">
    <meta name="selected-link" value="repo_source" data-pjax-transient>
      <meta name="google-analytics" content="UA-3769691-2">

    <meta content="collector.githubapp.com" name="octolytics-host" /><meta content="collector-cdn.github.com" name="octolytics-script-host" /><meta content="github" name="octolytics-app-id" /><meta content="657F1077:12AD:21EB31BF:54E9A041" name="octolytics-dimension-request_id" /><meta content="8855769" name="octolytics-actor-id" /><meta content="OiregR" name="octolytics-actor-login" /><meta content="2530200d170bc42550a08a79616c82ce4412e9afd343bef01709477bbe3d24d6" name="octolytics-actor-hash" />
    
    <meta content="Rails, view, blob#show" name="analytics-event" />

    
    
    <link rel="icon" type="image/x-icon" href="https://assets-cdn.github.com/favicon.ico">


    <meta content="authenticity_token" name="csrf-param" />
<meta content="Wn9dTgJ/oDiyxxh9Hjjd7Al2mgpa8zNBqQAwkMHJU4vyorxytcVc9U46b4Qg4ap27hPCqOAJt0OSUaEKqpLPLg==" name="csrf-token" />

    <link href="https://assets-cdn.github.com/assets/github-951e64287f8bc97e9b47e510c3be2de006cf747d5c833af0f3389ecb49313596.css" media="all" rel="stylesheet" />
    <link href="https://assets-cdn.github.com/assets/github2-f7073494168d35df2845fccdae3f73cb69dc51cf65c42dccd9cefb67ee814256.css" media="all" rel="stylesheet" />
    
    


    <meta http-equiv="x-pjax-version" content="f323dd8546e66c2e974b3bce9d06785e">

      
  <meta name="description" content="coursera-getting-and-cleaning-data - https://class.coursera.org/getdata-003">
  <meta name="go-import" content="github.com/laurikoobas/coursera-getting-and-cleaning-data git https://github.com/laurikoobas/coursera-getting-and-cleaning-data.git">

  <meta content="861986" name="octolytics-dimension-user_id" /><meta content="laurikoobas" name="octolytics-dimension-user_login" /><meta content="19675467" name="octolytics-dimension-repository_id" /><meta content="laurikoobas/coursera-getting-and-cleaning-data" name="octolytics-dimension-repository_nwo" /><meta content="true" name="octolytics-dimension-repository_public" /><meta content="false" name="octolytics-dimension-repository_is_fork" /><meta content="19675467" name="octolytics-dimension-repository_network_root_id" /><meta content="laurikoobas/coursera-getting-and-cleaning-data" name="octolytics-dimension-repository_network_root_nwo" />
  <link href="https://github.com/laurikoobas/coursera-getting-and-cleaning-data/commits/master.atom" rel="alternate" title="Recent Commits to coursera-getting-and-cleaning-data:master" type="application/atom+xml">

  </head>


  <body class="logged_in  env-production windows vis-public page-blob">
    <a href="#start-of-content" tabindex="1" class="accessibility-aid js-skip-to-content">Skip to content</a>
    <div class="wrapper">
      
      
      
      


      <div class="header header-logged-in true" role="banner">
  <div class="container clearfix">

    <a class="header-logo-invertocat" href="https://github.com/" data-hotkey="g d" aria-label="Homepage" data-ga-click="Header, go to dashboard, icon:logo">
  <span class="mega-octicon octicon-mark-github"></span>
</a>


      <div class="site-search repo-scope js-site-search" role="search">
          <form accept-charset="UTF-8" action="/laurikoobas/coursera-getting-and-cleaning-data/search" class="js-site-search-form" data-global-search-url="/search" data-repo-search-url="/laurikoobas/coursera-getting-and-cleaning-data/search" method="get"><div style="margin:0;padding:0;display:inline"><input name="utf8" type="hidden" value="&#x2713;" /></div>
  <input type="text"
    class="js-site-search-field is-clearable"
    data-hotkey="s"
    name="q"
    placeholder="Search"
    data-global-scope-placeholder="Search GitHub"
    data-repo-scope-placeholder="Search"
    tabindex="1"
    autocapitalize="off">
  <div class="scope-badge">This repository</div>
</form>
      </div>
      <ul class="header-nav left" role="navigation">
        <li class="header-nav-item explore">
          <a class="header-nav-link" href="/explore" data-ga-click="Header, go to explore, text:explore">Explore</a>
        </li>
          <li class="header-nav-item">
            <a class="header-nav-link" href="https://gist.github.com" data-ga-click="Header, go to gist, text:gist">Gist</a>
          </li>
          <li class="header-nav-item">
            <a class="header-nav-link" href="/blog" data-ga-click="Header, go to blog, text:blog">Blog</a>
          </li>
        <li class="header-nav-item">
          <a class="header-nav-link" href="https://help.github.com" data-ga-click="Header, go to help, text:help">Help</a>
        </li>
      </ul>

    
<ul class="header-nav user-nav right" id="user-links">
  <li class="header-nav-item dropdown js-menu-container">
    <a class="header-nav-link name" href="/OiregR" data-ga-click="Header, go to profile, text:username">
      <img alt="OiregR" class="avatar" data-user="8855769" height="20" src="https://avatars3.githubusercontent.com/u/8855769?v=3&amp;s=40" width="20" />
      <span class="css-truncate">
        <span class="css-truncate-target">OiregR</span>
      </span>
    </a>
  </li>

  <li class="header-nav-item dropdown js-menu-container">
    <a class="header-nav-link js-menu-target tooltipped tooltipped-s" href="#" aria-label="Create new..." data-ga-click="Header, create new, icon:add">
      <span class="octicon octicon-plus"></span>
      <span class="dropdown-caret"></span>
    </a>

    <div class="dropdown-menu-content js-menu-content">
      
<ul class="dropdown-menu">
  <li>
    <a href="/new" data-ga-click="Header, create new repository, icon:repo"><span class="octicon octicon-repo"></span> New repository</a>
  </li>
  <li>
    <a href="/organizations/new" data-ga-click="Header, create new organization, icon:organization"><span class="octicon octicon-organization"></span> New organization</a>
  </li>


    <li class="dropdown-divider"></li>
    <li class="dropdown-header">
      <span title="laurikoobas/coursera-getting-and-cleaning-data">This repository</span>
    </li>
      <li>
        <a href="/laurikoobas/coursera-getting-and-cleaning-data/issues/new" data-ga-click="Header, create new issue, icon:issue"><span class="octicon octicon-issue-opened"></span> New issue</a>
      </li>
</ul>

    </div>
  </li>

  <li class="header-nav-item">
        <a href="/notifications" aria-label="You have no unread notifications" class="header-nav-link notification-indicator tooltipped tooltipped-s" data-ga-click="Header, go to notifications, icon:read" data-hotkey="g n">
        <span class="mail-status all-read"></span>
        <span class="octicon octicon-inbox"></span>
</a>
  </li>

  <li class="header-nav-item">
    <a class="header-nav-link tooltipped tooltipped-s" href="/settings/profile" id="account_settings" aria-label="Settings" data-ga-click="Header, go to settings, icon:settings">
      <span class="octicon octicon-gear"></span>
    </a>
  </li>

  <li class="header-nav-item">
    <form accept-charset="UTF-8" action="/logout" class="logout-form" method="post"><div style="margin:0;padding:0;display:inline"><input name="utf8" type="hidden" value="&#x2713;" /><input name="authenticity_token" type="hidden" value="W9v080R2q5zmmBBFqO3fJQGJ4/QGyA6PvqK2GI2BER8Nq/Jm7UFVhAAuZ+Q2gkq7deozjYpf2rAahyO3el+eMw==" /></div>
      <button class="header-nav-link sign-out-button tooltipped tooltipped-s" aria-label="Sign out" data-ga-click="Header, sign out, icon:logout">
        <span class="octicon octicon-sign-out"></span>
      </button>
</form>  </li>

</ul>


    
  </div>
</div>

      

        


      <div id="start-of-content" class="accessibility-aid"></div>
          <div class="site" itemscope itemtype="http://schema.org/WebPage">
    <div id="js-flash-container">
      
    </div>
    <div class="pagehead repohead instapaper_ignore readability-menu">
      <div class="container">
        
<ul class="pagehead-actions">

  <li>
      <form accept-charset="UTF-8" action="/notifications/subscribe" class="js-social-container" data-autosubmit="true" data-remote="true" method="post"><div style="margin:0;padding:0;display:inline"><input name="utf8" type="hidden" value="&#x2713;" /><input name="authenticity_token" type="hidden" value="hmbYoRtPS/QD62IydRTN+HD27Svva5jT05mgvY+wIa/1+9YEIKPnzPq4A0ffp7DWhGR/iNdYHHj4iw7ZX3pdQw==" /></div>    <input id="repository_id" name="repository_id" type="hidden" value="19675467" />

      <div class="select-menu js-menu-container js-select-menu">
        <a class="social-count js-social-count" href="/laurikoobas/coursera-getting-and-cleaning-data/watchers">
          1
        </a>
        <a href="/laurikoobas/coursera-getting-and-cleaning-data/subscription"
          class="minibutton select-menu-button with-count js-menu-target" role="button" tabindex="0" aria-haspopup="true">
          <span class="js-select-button">
            <span class="octicon octicon-eye"></span>
            Watch
          </span>
        </a>

        <div class="select-menu-modal-holder">
          <div class="select-menu-modal subscription-menu-modal js-menu-content" aria-hidden="true">
            <div class="select-menu-header">
              <span class="select-menu-title">Notifications</span>
              <span class="octicon octicon-x js-menu-close" role="button" aria-label="Close"></span>
            </div>

            <div class="select-menu-list js-navigation-container" role="menu">

              <div class="select-menu-item js-navigation-item selected" role="menuitem" tabindex="0">
                <span class="select-menu-item-icon octicon octicon-check"></span>
                <div class="select-menu-item-text">
                  <input checked="checked" id="do_included" name="do" type="radio" value="included" />
                  <span class="select-menu-item-heading">Not watching</span>
                  <span class="description">Be notified when participating or @mentioned.</span>
                  <span class="js-select-button-text hidden-select-button-text">
                    <span class="octicon octicon-eye"></span>
                    Watch
                  </span>
                </div>
              </div>

              <div class="select-menu-item js-navigation-item " role="menuitem" tabindex="0">
                <span class="select-menu-item-icon octicon octicon octicon-check"></span>
                <div class="select-menu-item-text">
                  <input id="do_subscribed" name="do" type="radio" value="subscribed" />
                  <span class="select-menu-item-heading">Watching</span>
                  <span class="description">Be notified of all conversations.</span>
                  <span class="js-select-button-text hidden-select-button-text">
                    <span class="octicon octicon-eye"></span>
                    Unwatch
                  </span>
                </div>
              </div>

              <div class="select-menu-item js-navigation-item " role="menuitem" tabindex="0">
                <span class="select-menu-item-icon octicon octicon-check"></span>
                <div class="select-menu-item-text">
                  <input id="do_ignore" name="do" type="radio" value="ignore" />
                  <span class="select-menu-item-heading">Ignoring</span>
                  <span class="description">Never be notified.</span>
                  <span class="js-select-button-text hidden-select-button-text">
                    <span class="octicon octicon-mute"></span>
                    Stop ignoring
                  </span>
                </div>
              </div>

            </div>

          </div>
        </div>
      </div>
</form>

  </li>

  <li>
    
  <div class="js-toggler-container js-social-container starring-container ">

    <form accept-charset="UTF-8" action="/laurikoobas/coursera-getting-and-cleaning-data/unstar" class="js-toggler-form starred js-unstar-button" data-remote="true" method="post"><div style="margin:0;padding:0;display:inline"><input name="utf8" type="hidden" value="&#x2713;" /><input name="authenticity_token" type="hidden" value="Vhp+Vr0RU2GtXmmHrJ+IAeaBj5e/j1F3NarvwYsJUOspimQpe8wUSLXC3jShg3NFFmkpqJMHHzjR2hHyJf8oKQ==" /></div>
      <button
        class="minibutton with-count js-toggler-target"
        aria-label="Unstar this repository" title="Unstar laurikoobas/coursera-getting-and-cleaning-data">
        <span class="octicon octicon-star"></span>
        Unstar
      </button>
        <a class="social-count js-social-count" href="/laurikoobas/coursera-getting-and-cleaning-data/stargazers">
          0
        </a>
</form>
    <form accept-charset="UTF-8" action="/laurikoobas/coursera-getting-and-cleaning-data/star" class="js-toggler-form unstarred js-star-button" data-remote="true" method="post"><div style="margin:0;padding:0;display:inline"><input name="utf8" type="hidden" value="&#x2713;" /><input name="authenticity_token" type="hidden" value="3rDevJPYufyKAkD8TX2xoLv5nd/trmNqCl9C1+iie2hHDYWT78BEP1yy7sja2R4zPTU2enswMVAuLp2XRdAVJQ==" /></div>
      <button
        class="minibutton with-count js-toggler-target"
        aria-label="Star this repository" title="Star laurikoobas/coursera-getting-and-cleaning-data">
        <span class="octicon octicon-star"></span>
        Star
      </button>
        <a class="social-count js-social-count" href="/laurikoobas/coursera-getting-and-cleaning-data/stargazers">
          0
        </a>
</form>  </div>

  </li>

        <li>
          <a href="/laurikoobas/coursera-getting-and-cleaning-data/fork" class="minibutton with-count js-toggler-target tooltipped-n" title="Fork your own copy of laurikoobas/coursera-getting-and-cleaning-data to your account" aria-label="Fork your own copy of laurikoobas/coursera-getting-and-cleaning-data to your account" rel="nofollow" data-method="post">
            <span class="octicon octicon-repo-forked"></span>
            Fork
          </a>
          <a href="/laurikoobas/coursera-getting-and-cleaning-data/network" class="social-count">6</a>
        </li>

</ul>

        <h1 itemscope itemtype="http://data-vocabulary.org/Breadcrumb" class="entry-title public">
          <span class="mega-octicon octicon-repo"></span>
          <span class="author"><a href="/laurikoobas" class="url fn" itemprop="url" rel="author"><span itemprop="title">laurikoobas</span></a></span><!--
       --><span class="path-divider">/</span><!--
       --><strong><a href="/laurikoobas/coursera-getting-and-cleaning-data" class="js-current-repository" data-pjax="#js-repo-pjax-container">coursera-getting-and-cleaning-data</a></strong>

          <span class="page-context-loader">
            <img alt="" height="16" src="https://assets-cdn.github.com/assets/spinners/octocat-spinner-32-e513294efa576953719e4e2de888dd9cf929b7d62ed8d05f25e731d02452ab6c.gif" width="16" />
          </span>

        </h1>
      </div><!-- /.container -->
    </div><!-- /.repohead -->

    <div class="container">
      <div class="repository-with-sidebar repo-container new-discussion-timeline  ">
        <div class="repository-sidebar clearfix">
            
<nav class="sunken-menu repo-nav js-repo-nav js-sidenav-container-pjax js-octicon-loaders"
     role="navigation"
     data-pjax="#js-repo-pjax-container"
     data-issue-count-url="/laurikoobas/coursera-getting-and-cleaning-data/issues/counts">
  <ul class="sunken-menu-group">
    <li class="tooltipped tooltipped-w" aria-label="Code">
      <a href="/laurikoobas/coursera-getting-and-cleaning-data" aria-label="Code" class="selected js-selected-navigation-item sunken-menu-item" data-hotkey="g c" data-selected-links="repo_source repo_downloads repo_commits repo_releases repo_tags repo_branches /laurikoobas/coursera-getting-and-cleaning-data">
        <span class="octicon octicon-code"></span> <span class="full-word">Code</span>
        <img alt="" class="mini-loader" height="16" src="https://assets-cdn.github.com/assets/spinners/octocat-spinner-32-e513294efa576953719e4e2de888dd9cf929b7d62ed8d05f25e731d02452ab6c.gif" width="16" />
</a>    </li>

      <li class="tooltipped tooltipped-w" aria-label="Issues">
        <a href="/laurikoobas/coursera-getting-and-cleaning-data/issues" aria-label="Issues" class="js-selected-navigation-item sunken-menu-item" data-hotkey="g i" data-selected-links="repo_issues repo_labels repo_milestones /laurikoobas/coursera-getting-and-cleaning-data/issues">
          <span class="octicon octicon-issue-opened"></span> <span class="full-word">Issues</span>
          <span class="js-issue-replace-counter"></span>
          <img alt="" class="mini-loader" height="16" src="https://assets-cdn.github.com/assets/spinners/octocat-spinner-32-e513294efa576953719e4e2de888dd9cf929b7d62ed8d05f25e731d02452ab6c.gif" width="16" />
</a>      </li>

    <li class="tooltipped tooltipped-w" aria-label="Pull Requests">
      <a href="/laurikoobas/coursera-getting-and-cleaning-data/pulls" aria-label="Pull Requests" class="js-selected-navigation-item sunken-menu-item" data-hotkey="g p" data-selected-links="repo_pulls /laurikoobas/coursera-getting-and-cleaning-data/pulls">
          <span class="octicon octicon-git-pull-request"></span> <span class="full-word">Pull Requests</span>
          <span class="js-pull-replace-counter"></span>
          <img alt="" class="mini-loader" height="16" src="https://assets-cdn.github.com/assets/spinners/octocat-spinner-32-e513294efa576953719e4e2de888dd9cf929b7d62ed8d05f25e731d02452ab6c.gif" width="16" />
</a>    </li>


      <li class="tooltipped tooltipped-w" aria-label="Wiki">
        <a href="/laurikoobas/coursera-getting-and-cleaning-data/wiki" aria-label="Wiki" class="js-selected-navigation-item sunken-menu-item" data-hotkey="g w" data-selected-links="repo_wiki /laurikoobas/coursera-getting-and-cleaning-data/wiki">
          <span class="octicon octicon-book"></span> <span class="full-word">Wiki</span>
          <img alt="" class="mini-loader" height="16" src="https://assets-cdn.github.com/assets/spinners/octocat-spinner-32-e513294efa576953719e4e2de888dd9cf929b7d62ed8d05f25e731d02452ab6c.gif" width="16" />
</a>      </li>
  </ul>
  <div class="sunken-menu-separator"></div>
  <ul class="sunken-menu-group">

    <li class="tooltipped tooltipped-w" aria-label="Pulse">
      <a href="/laurikoobas/coursera-getting-and-cleaning-data/pulse" aria-label="Pulse" class="js-selected-navigation-item sunken-menu-item" data-selected-links="pulse /laurikoobas/coursera-getting-and-cleaning-data/pulse">
        <span class="octicon octicon-pulse"></span> <span class="full-word">Pulse</span>
        <img alt="" class="mini-loader" height="16" src="https://assets-cdn.github.com/assets/spinners/octocat-spinner-32-e513294efa576953719e4e2de888dd9cf929b7d62ed8d05f25e731d02452ab6c.gif" width="16" />
</a>    </li>

    <li class="tooltipped tooltipped-w" aria-label="Graphs">
      <a href="/laurikoobas/coursera-getting-and-cleaning-data/graphs" aria-label="Graphs" class="js-selected-navigation-item sunken-menu-item" data-selected-links="repo_graphs repo_contributors /laurikoobas/coursera-getting-and-cleaning-data/graphs">
        <span class="octicon octicon-graph"></span> <span class="full-word">Graphs</span>
        <img alt="" class="mini-loader" height="16" src="https://assets-cdn.github.com/assets/spinners/octocat-spinner-32-e513294efa576953719e4e2de888dd9cf929b7d62ed8d05f25e731d02452ab6c.gif" width="16" />
</a>    </li>
  </ul>


</nav>

              <div class="only-with-full-nav">
                  
<div class="clone-url open"
  data-protocol-type="http"
  data-url="/users/set_protocol?protocol_selector=http&amp;protocol_type=clone">
  <h3><span class="text-emphasized">HTTPS</span> clone URL</h3>
  <div class="input-group js-zeroclipboard-container">
    <input type="text" class="input-mini input-monospace js-url-field js-zeroclipboard-target"
           value="https://github.com/laurikoobas/coursera-getting-and-cleaning-data.git" readonly="readonly">
    <span class="input-group-button">
      <button aria-label="Copy to clipboard" class="js-zeroclipboard minibutton zeroclipboard-button" data-copied-hint="Copied!" type="button"><span class="octicon octicon-clippy"></span></button>
    </span>
  </div>
</div>

  
<div class="clone-url "
  data-protocol-type="ssh"
  data-url="/users/set_protocol?protocol_selector=ssh&amp;protocol_type=clone">
  <h3><span class="text-emphasized">SSH</span> clone URL</h3>
  <div class="input-group js-zeroclipboard-container">
    <input type="text" class="input-mini input-monospace js-url-field js-zeroclipboard-target"
           value="git@github.com:laurikoobas/coursera-getting-and-cleaning-data.git" readonly="readonly">
    <span class="input-group-button">
      <button aria-label="Copy to clipboard" class="js-zeroclipboard minibutton zeroclipboard-button" data-copied-hint="Copied!" type="button"><span class="octicon octicon-clippy"></span></button>
    </span>
  </div>
</div>

  
<div class="clone-url "
  data-protocol-type="subversion"
  data-url="/users/set_protocol?protocol_selector=subversion&amp;protocol_type=clone">
  <h3><span class="text-emphasized">Subversion</span> checkout URL</h3>
  <div class="input-group js-zeroclipboard-container">
    <input type="text" class="input-mini input-monospace js-url-field js-zeroclipboard-target"
           value="https://github.com/laurikoobas/coursera-getting-and-cleaning-data" readonly="readonly">
    <span class="input-group-button">
      <button aria-label="Copy to clipboard" class="js-zeroclipboard minibutton zeroclipboard-button" data-copied-hint="Copied!" type="button"><span class="octicon octicon-clippy"></span></button>
    </span>
  </div>
</div>



<p class="clone-options">You can clone with
  <a href="#" class="js-clone-selector" data-protocol="http">HTTPS</a>, <a href="#" class="js-clone-selector" data-protocol="ssh">SSH</a>, or <a href="#" class="js-clone-selector" data-protocol="subversion">Subversion</a>.
  <a href="https://help.github.com/articles/which-remote-url-should-i-use" class="help tooltipped tooltipped-n" aria-label="Get help on which URL is right for you.">
    <span class="octicon octicon-question"></span>
  </a>
</p>


  <a href="github-windows://openRepo/https://github.com/laurikoobas/coursera-getting-and-cleaning-data" class="minibutton sidebar-button" title="Save laurikoobas/coursera-getting-and-cleaning-data to your computer and use it in GitHub Desktop." aria-label="Save laurikoobas/coursera-getting-and-cleaning-data to your computer and use it in GitHub Desktop.">
    <span class="octicon octicon-device-desktop"></span>
    Clone in Desktop
  </a>

                <a href="/laurikoobas/coursera-getting-and-cleaning-data/archive/master.zip"
                   class="minibutton sidebar-button"
                   aria-label="Download the contents of laurikoobas/coursera-getting-and-cleaning-data as a zip file"
                   title="Download the contents of laurikoobas/coursera-getting-and-cleaning-data as a zip file"
                   rel="nofollow">
                  <span class="octicon octicon-cloud-download"></span>
                  Download ZIP
                </a>
              </div>
        </div><!-- /.repository-sidebar -->

        <div id="js-repo-pjax-container" class="repository-content context-loader-container" data-pjax-container>
          

<a href="/laurikoobas/coursera-getting-and-cleaning-data/blob/65b5d92ddc8895865d4c0f785e18dffd2b32425d/CodeBook.md" class="hidden js-permalink-shortcut" data-hotkey="y">Permalink</a>

<!-- blob contrib key: blob_contributors:v21:aeea7f49f4e9cb62fa9e372e66613c0f -->

<div class="file-navigation js-zeroclipboard-container">
  
<div class="select-menu js-menu-container js-select-menu left">
  <span class="minibutton select-menu-button js-menu-target css-truncate" data-hotkey="w"
    data-master-branch="master"
    data-ref="master"
    title="master"
    role="button" aria-label="Switch branches or tags" tabindex="0" aria-haspopup="true">
    <span class="octicon octicon-git-branch"></span>
    <i>branch:</i>
    <span class="js-select-button css-truncate-target">master</span>
  </span>

  <div class="select-menu-modal-holder js-menu-content js-navigation-container" data-pjax aria-hidden="true">

    <div class="select-menu-modal">
      <div class="select-menu-header">
        <span class="select-menu-title">Switch branches/tags</span>
        <span class="octicon octicon-x js-menu-close" role="button" aria-label="Close"></span>
      </div>

      <div class="select-menu-filters">
        <div class="select-menu-text-filter">
          <input type="text" aria-label="Filter branches/tags" id="context-commitish-filter-field" class="js-filterable-field js-navigation-enable" placeholder="Filter branches/tags">
        </div>
        <div class="select-menu-tabs">
          <ul>
            <li class="select-menu-tab">
              <a href="#" data-tab-filter="branches" data-filter-placeholder="Filter branches/tags" class="js-select-menu-tab">Branches</a>
            </li>
            <li class="select-menu-tab">
              <a href="#" data-tab-filter="tags" data-filter-placeholder="Find a tag…" class="js-select-menu-tab">Tags</a>
            </li>
          </ul>
        </div>
      </div>

      <div class="select-menu-list select-menu-tab-bucket js-select-menu-tab-bucket" data-tab-filter="branches">

        <div data-filterable-for="context-commitish-filter-field" data-filterable-type="substring">


            <a class="select-menu-item js-navigation-item js-navigation-open selected"
               href="/laurikoobas/coursera-getting-and-cleaning-data/blob/master/CodeBook.md"
               data-name="master"
               data-skip-pjax="true"
               rel="nofollow">
              <span class="select-menu-item-icon octicon octicon-check"></span>
              <span class="select-menu-item-text css-truncate-target" title="master">
                master
              </span>
            </a>
        </div>

          <div class="select-menu-no-results">Nothing to show</div>
      </div>

      <div class="select-menu-list select-menu-tab-bucket js-select-menu-tab-bucket" data-tab-filter="tags">
        <div data-filterable-for="context-commitish-filter-field" data-filterable-type="substring">


        </div>

        <div class="select-menu-no-results">Nothing to show</div>
      </div>

    </div>
  </div>
</div>

  <div class="button-group right">
    <a href="/laurikoobas/coursera-getting-and-cleaning-data/find/master"
          class="js-show-file-finder minibutton empty-icon tooltipped tooltipped-s"
          data-pjax
          data-hotkey="t"
          aria-label="Quickly jump between files">
      <span class="octicon octicon-list-unordered"></span>
    </a>
    <button aria-label="Copy file path to clipboard" class="js-zeroclipboard minibutton zeroclipboard-button" data-copied-hint="Copied!" type="button"><span class="octicon octicon-clippy"></span></button>
  </div>

  <div class="breadcrumb js-zeroclipboard-target">
    <span class='repo-root js-repo-root'><span itemscope="" itemtype="http://data-vocabulary.org/Breadcrumb"><a href="/laurikoobas/coursera-getting-and-cleaning-data" class="" data-branch="master" data-direction="back" data-pjax="true" itemscope="url"><span itemprop="title">coursera-getting-and-cleaning-data</span></a></span></span><span class="separator">/</span><strong class="final-path">CodeBook.md</strong>
  </div>
</div>


  <div class="commit file-history-tease">
    <div class="file-history-tease-header">
        <img alt="Lauri Koobas" class="avatar" data-user="861986" height="24" src="https://avatars1.githubusercontent.com/u/861986?v=3&amp;s=48" width="24" />
        <span class="author"><a href="/laurikoobas" rel="author">laurikoobas</a></span>
        <time datetime="2014-05-25T21:07:52Z" is="relative-time">May 26, 2014</time>
        <div class="commit-title">
            <a href="/laurikoobas/coursera-getting-and-cleaning-data/commit/65b5d92ddc8895865d4c0f785e18dffd2b32425d" class="message" data-pjax="true" title="Add CodeBook.md">Add CodeBook.md</a>
        </div>
    </div>

    <div class="participation">
      <p class="quickstat">
        <a href="#blob_contributors_box" rel="facebox">
          <strong>1</strong>
           contributor
        </a>
      </p>
      
    </div>
    <div id="blob_contributors_box" style="display:none">
      <h2 class="facebox-header">Users who have contributed to this file</h2>
      <ul class="facebox-user-list">
          <li class="facebox-user-list-item">
            <img alt="Lauri Koobas" data-user="861986" height="24" src="https://avatars1.githubusercontent.com/u/861986?v=3&amp;s=48" width="24" />
            <a href="/laurikoobas">laurikoobas</a>
          </li>
      </ul>
    </div>
  </div>

<div class="file">
  <div class="file-header">
    <div class="file-info">
        273 lines (176 sloc)
        <span class="file-info-divider"></span>
      5.724 kb
    </div>
    <div class="file-actions">
      <div class="button-group">
        <a href="/laurikoobas/coursera-getting-and-cleaning-data/raw/master/CodeBook.md" class="minibutton " id="raw-url">Raw</a>
          <a href="/laurikoobas/coursera-getting-and-cleaning-data/blame/master/CodeBook.md" class="minibutton js-update-url-with-hash">Blame</a>
        <a href="/laurikoobas/coursera-getting-and-cleaning-data/commits/master/CodeBook.md" class="minibutton " rel="nofollow">History</a>
      </div><!-- /.button-group -->

        <a class="octicon-button tooltipped tooltipped-nw"
           href="github-windows://openRepo/https://github.com/laurikoobas/coursera-getting-and-cleaning-data?branch=master&amp;filepath=CodeBook.md" aria-label="Open this file in GitHub for Windows">
            <span class="octicon octicon-device-desktop"></span>
        </a>

            <a class="octicon-button tooltipped tooltipped-n js-update-url-with-hash"
               aria-label="Clicking this button will fork this project so you can edit the file"
               href="/laurikoobas/coursera-getting-and-cleaning-data/edit/master/CodeBook.md"
               data-method="post" rel="nofollow"><span class="octicon octicon-pencil"></span></a>

          <a class="octicon-button danger tooltipped tooltipped-s"
             href="/laurikoobas/coursera-getting-and-cleaning-data/delete/master/CodeBook.md"
             aria-label="Fork this project and delete file"
             data-method="post" data-test-id="delete-blob-file" rel="nofollow">
        <span class="octicon octicon-trashcan"></span>
      </a>
    </div><!-- /.actions -->
  </div>
  
  <div id="readme" class="blob instapaper_body">
    <article class="markdown-body entry-content" itemprop="mainContentOfPage"><h1>
<a id="user-content-codebook-for-wearable-computing-dataset" class="anchor" href="#codebook-for-wearable-computing-dataset" aria-hidden="true"><span class="octicon octicon-link"></span></a>Codebook for wearable computing dataset</h1>

<h2>
<a id="user-content-variables" class="anchor" href="#variables" aria-hidden="true"><span class="octicon octicon-link"></span></a>Variables</h2>

<pre><code>subject                    1..2
    Subject number
                           1..30 .Unique identifier assigned to each subject

label                      6..18
    Acitivity label
                           "WALKING"
                           "WALKING_UPSTAIRS"
                           "WALKING_DOWNSTAIRS"
                           "SITTING"
                           "STANDING"
                           "LAYING"

tbodyaccmeanx              12
    Described below

tbodyaccmeany              12
    Described below

tbodyaccmeanz              12
    Described below

tbodyaccstdx               12
    Described below

tbodyaccstdy               12
    Described below

tbodyaccstdz               12
    Described below

tgravityaccmeanx           12
    Described below

tgravityaccmeany           12
    Described below

tgravityaccmeanz           12
    Described below

tgravityaccstdx            12
    Described below

tgravityaccstdy            12
    Described below

tgravityaccstdz            12
    Described below

tbodyaccjerkmeanx          12
    Described below

tbodyaccjerkmeany          12
    Described below

tbodyaccjerkmeanz          12
    Described below

tbodyaccjerkstdx           12
    Described below

tbodyaccjerkstdy           12
    Described below

tbodyaccjerkstdz           12
    Described below

tbodygyromeanx             12
    Described below

tbodygyromeany             12
    Described below

tbodygyromeanz             12
    Described below

tbodygyrostdx              12
    Described below

tbodygyrostdy              12
    Described below

tbodygyrostdz              12
    Described below

tbodygyrojerkmeanx         12
    Described below

tbodygyrojerkmeany         12
    Described below

tbodygyrojerkmeanz         12
    Described below

tbodygyrojerkstdx          12
    Described below

tbodygyrojerkstdy          12
    Described below

tbodygyrojerkstdz          12
    Described below

tbodyaccmagmean            12
    Described below

tbodyaccmagstd             12
    Described below

tgravityaccmagmean         12
    Described below

tgravityaccmagstd          12
    Described below

tbodyaccjerkmagmean        12
    Described below

tbodyaccjerkmagstd         12
    Described below

tbodygyromagmean           12
    Described below

tbodygyromagstd            12
    Described below

tbodygyrojerkmagmean       12
    Described below

tbodygyrojerkmagstd        12
    Described below

fbodyaccmeanx              12
    Described below

fbodyaccmeany              12
    Described below

fbodyaccmeanz              12
    Described below

fbodyaccstdx               12
    Described below

fbodyaccstdy               12
    Described below

fbodyaccstdz               12
    Described below

fbodyaccjerkmeanx          12
    Described below

fbodyaccjerkmeany          12
    Described below

fbodyaccjerkmeanz          12
    Described below

fbodyaccjerkstdx           12
    Described below

fbodyaccjerkstdy           12
    Described below

fbodyaccjerkstdz           12
    Described below

fbodygyromeanx             12
    Described below

fbodygyromeany             12
    Described below

fbodygyromeanz             12
    Described below

fbodygyrostdx              12
    Described below

fbodygyrostdy              12
    Described below

fbodygyrostdz              12
    Described below

fbodyaccmagmean            12
    Described below

fbodyaccmagstd             12
    Described below

fbodybodyaccjerkmagmean    12
    Described below

fbodybodyaccjerkmagstd     12
    Described below

fbodybodygyromagmean       12
    Described below

fbodybodygyromagstd        12
    Described below

fbodybodygyrojerkmagmean   12
    Described below

fbodybodygyrojerkmagstd    12
    Described below

</code></pre>

<h2>
<a id="user-content-data" class="anchor" href="#data" aria-hidden="true"><span class="octicon octicon-link"></span></a>Data</h2>

<p>The features selected for this database come from the accelerometer and gyroscope 3-axial raw signals tAcc-XYZ and tGyro-XYZ. These time domain signals (prefix 't' to denote time) were captured at a constant rate of 50 Hz. Then they were filtered using a median filter and a 3rd order low pass Butterworth filter with a corner frequency of 20 Hz to remove noise. Similarly, the acceleration signal was then separated into body and gravity acceleration signals (tBodyAcc-XYZ and tGravityAcc-XYZ) using another low pass Butterworth filter with a corner frequency of 0.3 Hz. </p>

<p>Subsequently, the body linear acceleration and angular velocity were derived in time to obtain Jerk signals (tBodyAccJerk-XYZ and tBodyGyroJerk-XYZ). Also the magnitude of these three-dimensional signals were calculated using the Euclidean norm (tBodyAccMag, tGravityAccMag, tBodyAccJerkMag, tBodyGyroMag, tBodyGyroJerkMag). </p>

<p>Finally a Fast Fourier Transform (FFT) was applied to some of these signals producing fBodyAcc-XYZ, fBodyAccJerk-XYZ, fBodyGyro-XYZ, fBodyAccJerkMag, fBodyGyroMag, fBodyGyroJerkMag. (Note the 'f' to indicate frequency domain signals). </p>

<p>These signals were used to estimate variables of the feature vector for each pattern:<br>
'-XYZ' is used to denote 3-axial signals in the X, Y and Z directions.</p>

<p>tbodyacc-xyz</p>

<p>tgravityacc-xyz</p>

<p>tbodyaccjerk-xyz</p>

<p>tbodygyro-xyz</p>

<p>tbodygyrojerk-xyz</p>

<p>tbodyaccmag</p>

<p>tgravityaccmag</p>

<p>tbodyaccjerkmag</p>

<p>tbodygyromag</p>

<p>tbodygyrojerkmag</p>

<p>fbodyacc-xyz</p>

<p>fbodyaccjerk-xyz</p>

<p>fbodygyro-xyz</p>

<p>fbodyaccmag</p>

<p>fbodyaccjerkmag</p>

<p>fbodygyromag</p>

<p>fbodygyrojerkmag</p>

<p>The set of variables that were estimated from these signals are: </p>

<p>mean: Mean value</p>

<p>std: Standard deviation</p>

<h2>
<a id="user-content-transformation" class="anchor" href="#transformation" aria-hidden="true"><span class="octicon octicon-link"></span></a>Transformation</h2>

<p>All the values are means, aggregated over 30 subjects and 6 activities, hence the resulting dataset is 180 rows by 68 columns.</p>
</article>
  </div>

</div>

<a href="#jump-to-line" rel="facebox[.linejump]" data-hotkey="l" style="display:none">Jump to Line</a>
<div id="jump-to-line" style="display:none">
  <form accept-charset="UTF-8" class="js-jump-to-line-form">
    <input class="linejump-input js-jump-to-line-field" type="text" placeholder="Jump to line&hellip;" autofocus>
    <button type="submit" class="button">Go</button>
  </form>
</div>

        </div>

      </div><!-- /.repo-container -->
      <div class="modal-backdrop"></div>
    </div><!-- /.container -->
  </div><!-- /.site -->


    </div><!-- /.wrapper -->

      <div class="container">
  <div class="site-footer" role="contentinfo">
    <ul class="site-footer-links right">
        <li><a href="https://status.github.com/" data-ga-click="Footer, go to status, text:status">Status</a></li>
      <li><a href="https://developer.github.com" data-ga-click="Footer, go to api, text:api">API</a></li>
      <li><a href="http://training.github.com" data-ga-click="Footer, go to training, text:training">Training</a></li>
      <li><a href="http://shop.github.com" data-ga-click="Footer, go to shop, text:shop">Shop</a></li>
        <li><a href="/blog" data-ga-click="Footer, go to blog, text:blog">Blog</a></li>
        <li><a href="/about" data-ga-click="Footer, go to about, text:about">About</a></li>

    </ul>

    <a href="/" aria-label="Homepage">
      <span class="mega-octicon octicon-mark-github" title="GitHub"></span>
    </a>

    <ul class="site-footer-links">
      <li>&copy; 2015 <span title="0.04373s from github-fe128-cp1-prd.iad.github.net">GitHub</span>, Inc.</li>
        <li><a href="/site/terms" data-ga-click="Footer, go to terms, text:terms">Terms</a></li>
        <li><a href="/site/privacy" data-ga-click="Footer, go to privacy, text:privacy">Privacy</a></li>
        <li><a href="/security" data-ga-click="Footer, go to security, text:security">Security</a></li>
        <li><a href="/contact" data-ga-click="Footer, go to contact, text:contact">Contact</a></li>
    </ul>
  </div>
</div>


    <div class="fullscreen-overlay js-fullscreen-overlay" id="fullscreen_overlay">
  <div class="fullscreen-container js-suggester-container">
    <div class="textarea-wrap">
      <textarea name="fullscreen-contents" id="fullscreen-contents" class="fullscreen-contents js-fullscreen-contents" placeholder=""></textarea>
      <div class="suggester-container">
        <div class="suggester fullscreen-suggester js-suggester js-navigation-container"></div>
      </div>
    </div>
  </div>
  <div class="fullscreen-sidebar">
    <a href="#" class="exit-fullscreen js-exit-fullscreen tooltipped tooltipped-w" aria-label="Exit Zen Mode">
      <span class="mega-octicon octicon-screen-normal"></span>
    </a>
    <a href="#" class="theme-switcher js-theme-switcher tooltipped tooltipped-w"
      aria-label="Switch themes">
      <span class="octicon octicon-color-mode"></span>
    </a>
  </div>
</div>



    

    <div id="ajax-error-message" class="flash flash-error">
      <span class="octicon octicon-alert"></span>
      <a href="#" class="octicon octicon-x flash-close js-ajax-error-dismiss" aria-label="Dismiss error"></a>
      Something went wrong with that request. Please try again.
    </div>


      <script crossorigin="anonymous" src="https://assets-cdn.github.com/assets/frameworks-9643b0378c6bcb216adcdaaaa703eed77aa239aaf1c2ae44cadb2fb5099ec172.js"></script>
      <script async="async" crossorigin="anonymous" src="https://assets-cdn.github.com/assets/github-18e60b9aac8c7c21fb47634ab0194e9f8a433423ebafc0eea0d39363aee0b8af.js"></script>
      
      

  </body>
</html>

