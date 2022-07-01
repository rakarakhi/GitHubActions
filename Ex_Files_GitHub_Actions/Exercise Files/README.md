# Exercise Files for Learning GitHub Actions

The exercise files are located in folders named to match the chapter and lesson they accompany.

- *PREREQUSITES: You'll need to have the `git` command line tool installed for your system and access to a terminal program like [GitBash](https://gitforwindows.org/) on Windows or [iTerm2](https://www.iterm2.com/) on macOS.  The default terminal program for your system will work as well as long as the git program is in your PATH.*

## Using Exercise Files with Repositories

Follow these steps if you want to use the exercise files the same way they are used within the course.

We'll use the exercise files from Chapter 1, Lesson 1 for this example.

- Create a repository on GitHub using the [New Repository](https://github.com/new) page.  Name it something that relates to the lesson like `ch01-01-01`.

- Download the exercise files and unzip the archive.  If you are reading this, you have most likely completed this step! :D

- Open a terminal window and change directories to the location where you unzipped archive.  "CD" into the directory with the lesson you want to work with; for this example, we'll use Ch01/01_01.

        cd Ch01/01_01

- Run the following commands to initialize the directory as a git repository.

        git init
        git add .
        git commit -m 'first check in'

- Now add the new repository you created as a remote for the local repo.

        git remote add origin git@github.com:YOUR_GITHUB_USER_NAME_HERE/ch01-01-01.git

- After the remote is added, push the files to the remote.

        git push -u origin master

 - Browse to the repository on GitHub.com and reload the page to confirm the files have been properly pushed.

Once the files are hosted on GitHub.com, you're ready to start making changes locally and pushing them to the remote repo.

- If there is issue with SSH.
        
        C:\Users\rchakrab\GitHubActions>git push -u origin main
        git@github.com: Permission denied (publickey).
        fatal: Could not read from remote repository.

        Please make sure you have the correct access rights
        and the repository exists.

        C:\Users\rchakrab\GitHubActions>ssh -vT git@github.com
        OpenSSH_for_Windows_8.1p1, LibreSSL 3.0.2
        debug1: Connecting to github.com [20.205.243.166] port 22.
        debug1: Connection established.
        debug1: identity file C:\\Users\\rchakrab/.ssh/id_rsa type 0
        debug1: identity file C:\\Users\\rchakrab/.ssh/id_rsa-cert type -1
        debug1: identity file C:\\Users\\rchakrab/.ssh/id_dsa type -1
        debug1: identity file C:\\Users\\rchakrab/.ssh/id_dsa-cert type -1
        debug1: identity file C:\\Users\\rchakrab/.ssh/id_ecdsa type -1
        debug1: identity file C:\\Users\\rchakrab/.ssh/id_ecdsa-cert type -1
        debug1: identity file C:\\Users\\rchakrab/.ssh/id_ed25519 type -1
        debug1: identity file C:\\Users\\rchakrab/.ssh/id_ed25519-cert type -1
        debug1: identity file C:\\Users\\rchakrab/.ssh/id_xmss type -1
        debug1: identity file C:\\Users\\rchakrab/.ssh/id_xmss-cert type -1
        debug1: Local version string SSH-2.0-OpenSSH_for_Windows_8.1
        debug1: Remote protocol version 2.0, remote software version babeld-7f91b4d6
        debug1: no match: babeld-7f91b4d6
        debug1: Authenticating to github.com:22 as 'git'
        debug1: SSH2_MSG_KEXINIT sent
        debug1: SSH2_MSG_KEXINIT received
        debug1: kex: algorithm: curve25519-sha256
        debug1: kex: host key algorithm: ssh-ed25519
        debug1: kex: server->client cipher: chacha20-poly1305@openssh.com MAC: <implicit> compression: none
        debug1: kex: client->server cipher: chacha20-poly1305@openssh.com MAC: <implicit> compression: none
        debug1: expecting SSH2_MSG_KEX_ECDH_REPLY
        debug1: Server host key: ssh-ed25519 SHA256:+DiY3wvvV6TuJJhbpZisF/zLDA0zPMSvHdkr4UvCOqU
        debug1: Host 'github.com' is known and matches the ED25519 host key.
        debug1: Found key in C:\\Users\\rchakrab/.ssh/known_hosts:1
        debug1: rekey out after 134217728 blocks
        debug1: SSH2_MSG_NEWKEYS sent
        debug1: expecting SSH2_MSG_NEWKEYS
        debug1: SSH2_MSG_NEWKEYS received
        debug1: rekey in after 134217728 blocks
        debug1: pubkey_prepare: ssh_get_authentication_socket: No such file or directory
        debug1: Will attempt key: C:\\Users\\rchakrab/.ssh/id_rsa RSA SHA256:k2G2IC1fKVKEwFPRCT9MvJA6uuBgRybJ5laSVif/cTE
        debug1: Will attempt key: C:\\Users\\rchakrab/.ssh/id_dsa
        debug1: Will attempt key: C:\\Users\\rchakrab/.ssh/id_ecdsa
        debug1: Will attempt key: C:\\Users\\rchakrab/.ssh/id_ed25519
        debug1: Will attempt key: C:\\Users\\rchakrab/.ssh/id_xmss
        debug1: SSH2_MSG_EXT_INFO received
        debug1: kex_input_ext_info: server-sig-algs=<ssh-ed25519-cert-v01@openssh.com,ecdsa-sha2-nistp521-cert-v01@openssh.com,ecdsa-sha2-nistp384-             cert-v01@openssh.com,ecdsa-sha2-nistp256-cert-v01@openssh.com,sk-ssh-ed25519-cert-v01@openssh.com,sk-ecdsa-sha2-nistp256-cert-                         v01@openssh.com,rsa-sha2-512-cert-v01@openssh.com,rsa-sha2-256-cert-v01@openssh.com,ssh-rsa-cert-v01@openssh.com,sk-ssh-                               ed25519@openssh.com,sk-ecdsa-sha2-nistp256@openssh.com,ssh-ed25519,ecdsa-sha2-nistp521,ecdsa-sha2-nistp384,ecdsa-sha2-nistp256,rsa-sha2-               512,rsa-sha2-256,ssh-rsa>
        debug1: SSH2_MSG_SERVICE_ACCEPT received
        debug1: Authentications that can continue: publickey
        debug1: Next authentication method: publickey
        debug1: Offering public key: C:\\Users\\rchakrab/.ssh/id_rsa RSA SHA256:k2G2IC1fKVKEwFPRCT9MvJA6uuBgRybJ5laSVif/cTE
        debug1: Authentications that can continue: publickey
        debug1: Trying private key: C:\\Users\\rchakrab/.ssh/id_dsa
        debug1: Trying private key: C:\\Users\\rchakrab/.ssh/id_ecdsa
        debug1: Trying private key: C:\\Users\\rchakrab/.ssh/id_ed25519
        debug1: Trying private key: C:\\Users\\rchakrab/.ssh/id_xmss
        debug1: No more authentication methods to try.
        git@github.com: Permission denied (publickey).

        C:\Users\rchakrab\GitHubActions>
        
- Use this Fix:
        https://stackoverflow.com/questions/26505980/github-permission-denied-ssh-add-agent-has-no-identities/28444641#comment68731110_28444641
        Refer Answer 10
        Run the following commands:

        ssh-keygen -t rsa
        ssh-add /Users/*yourUserNameHere*/.ssh/id_rsa** 
        pbcopy < ~/.ssh/id_rsa.pub**
        Go to your Github account : https://github.com/settings/profile

        1) Click : SSH and GPG keys

        2) New SSH Key and Past it there

        3) Add SSH Key

        Done!

- Open Git BASH
        
        https://docs.github.com/en/get-started/getting-started-with-git/about-remote-repositories
        
        rchakrab@DESKTOP-K4R48QN MINGW64 ~
        $  eval $(ssh-agent -s)
        Agent pid 218

        rchakrab@DESKTOP-K4R48QN MINGW64 ~
        $ ssh-add -l -E sha256
        The agent has no identities.

        rchakrab@DESKTOP-K4R48QN MINGW64 ~
        $ ssh-add /c/Users/rchakrab/.ssh/id_rsa
        Identity added: /c/Users/rchakrab/.ssh/id_rsa (rchakrab@DESKTOP-K4R48QN)

        rchakrab@DESKTOP-K4R48QN MINGW64 ~
        $ ssh-add -l -E sha256
        3072 SHA256:k2G2IC1fKVKEwFPRCT9MvJA6uuBgRybJ5laSVif/cTE rchakrab@DESKTOP-K4R48QN (RSA)

        rchakrab@DESKTOP-K4R48QN MINGW64 ~
        $ pwd
        /c/Users/rchakrab

        rchakrab@DESKTOP-K4R48QN MINGW64 ~
        $ cd GitHubActions/

        rchakrab@DESKTOP-K4R48QN MINGW64 ~/GitHubActions (main)
        $ git push origin main
        git@github.com: Permission denied (publickey).
        fatal: Could not read from remote repository.

        Please make sure you have the correct access rights
        and the repository exists.

        rchakrab@DESKTOP-K4R48QN MINGW64 ~/GitHubActions (main)
        $ git remote set-url https://github.com/rakarakhi/GitHubActions.git
        usage: git remote set-url [--push] <name> <newurl> [<oldurl>]
           or: git remote set-url --add <name> <newurl>
           or: git remote set-url --delete <name> <url>

            --push                manipulate push URLs
            --add                 add URL
            --delete              delete URLs


        rchakrab@DESKTOP-K4R48QN MINGW64 ~/GitHubActions (main)
        $ git remote set-url --add origin https://github.com/rakarakhi/GitHubActions.git

        rchakrab@DESKTOP-K4R48QN MINGW64 ~/GitHubActions (main)
        $ git remote -v
        origin  git@github.com:rakarakhi/GitHubActions.git (fetch)
        origin  git@github.com:rakarakhi/GitHubActions.git (push)
        origin  https://github.com/rakarakhi/GitHubActions.git (push)

        rchakrab@DESKTOP-K4R48QN MINGW64 ~/GitHubActions (main)
        $ git remote set-url origin git@github.com:rakarakhi/GitHubActions.git
        warning: remote.origin.url has multiple values
        fatal: could not set 'remote.origin.url' to 'git@github.com:rakarakhi/GitHubActi
        ons.git'

        rchakrab@DESKTOP-K4R48QN MINGW64 ~/GitHubActions (main)
        $ git remote set-url --delete origin git@github.com:rakarakhi/GitHubActions.git

        rchakrab@DESKTOP-K4R48QN MINGW64 ~/GitHubActions (main)
        $ git remote -v
        origin  https://github.com/rakarakhi/GitHubActions.git (fetch)
        origin  https://github.com/rakarakhi/GitHubActions.git (push)

        rchakrab@DESKTOP-K4R48QN MINGW64 ~/GitHubActions (main)
        $ git push origin main
        info: please complete authentication in your browser...
        Enumerating objects: 128, done.
        Counting objects: 100% (128/128), done.
        Delta compression using up to 2 threads
        Compressing objects: 100% (90/90), done.
        Writing objects: 100% (128/128), 128.05 KiB | 1.86 MiB/s, done.
        Total 128 (delta 31), reused 0 (delta 0), pack-reused 0
        remote: Resolving deltas: 100% (31/31), done.
        To https://github.com/rakarakhi/GitHubActions.git
         * [new branch]      main -> main

        rchakrab@DESKTOP-K4R48QN MINGW64 ~/GitHubActions (main)
        $

- GIT Should be added to system path:

        https://stackoverflow.com/questions/68571010/cant-start-ssh-agent-with-git-bash-on-windows-10

        Make sure first in a CMD session to:

        upgrade to the latest Git for Windows
        the PATH correctly set to Git, for testing.
        That is:

        set GH=C:\path\to\git
        set PATH=C:\windows\system32;C:\windows\System32\Wbem;C:\windows\System32\WindowsPowerShell\v1.0\
        set PATH=%GH%\bin;%GH%\usr\bin;%GH%\mingw64\bin;%GH%\mingw64\libexec\git-core;%PATH%
         

