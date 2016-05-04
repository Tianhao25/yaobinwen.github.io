---
layout: draft
title: SSH Authentication Failure
date: 2016-04-11
comments: true
category: Draft
tags: ssh, authentication
description:

---

## Log Messages
```/var/log/auth.log```

    Apr 11 09:44:05 mucker sshd[32003]: Invalid user mapping from 10.66.171.100
    Apr 11 09:44:05 mucker sshd[32003]: input_userauth_request: invalid user mapping [preauth]
    Apr 11 09:44:18 mucker sshd[32003]: pam_unix(sshd:auth): check pass; user unknown
    Apr 11 09:44:18 mucker sshd[32003]: pam_unix(sshd:auth): authentication failure; logname= uid=0 euid=0 tty=ssh ruser= rhost=tablet
    Apr 11 09:44:20 mucker sshd[32003]: Failed password for invalid user mapping from 10.66.171.100 port 33585 ssh2
    Apr 11 09:44:54 mucker sshd[32003]: Connection closed by 10.66.171.100 [preauth]


Search ```input_userauth_request: invalid user mapping [preauth]```

[authentication failure using SSH pam_unix(sshd:auth): authentication failure;  ](http://kura2gurun.blogspot.com/2011/10/authentication-failure-using-ssh.html)

[15.3. PAM Configuration File Format](https://access.redhat.com/documentation/en-US/Red_Hat_Enterprise_Linux/3/html/Reference_Guide/s1-pam-format.html)

[ssh server config - input_userauth_request: invalid user](http://serverfault.com/questions/665587/ssh-server-config-input-userauth-request-invalid-user)

[How To Use PAM to Configure Authentication on an Ubuntu 12.04 VPS](https://www.digitalocean.com/community/tutorials/how-to-use-pam-to-configure-authentication-on-an-ubuntu-12-04-vps)

[Problems with Ubuntu 12.04 joined to Active Directory](http://ubuntuforums.org/showthread.php?t=2152487)

## Pending Questions
* What is the "pam" module?
*

===

/freebsd/crypto/openssh/auth-passwd.c

    118#if defined(USE_SHADOW) && defined(HAS_SHADOW_EXPIRE)
    119	if (!expire_checked) {    
    120		expire_checked = 1;
    121		if (auth_shadow_pwexpired(authctxt))
    122			authctxt->force_pwchange = 1;
    123	}
    124#endif


/freebsd/crypto/openssh/auth-shadow.c:

    int
    auth_shadow_pwexpired(Authctxt *ctxt)
    {
      struct spwd *spw = NULL;
  	  const char *user = ctxt->pw->pw_name;  
  	  char buf[256];
  	  time_t today;
  	  int daysleft, disabled = 0;

  	  if ((spw = getspnam((char *)user)) == NULL) {
  		  error("Could not get shadow information for %.100s", user);
  		  return 0;
  	  }

/freebsd/crypto/openssh/auth.h

      49struct Authctxt {
      50	sig_atomic_t	 success;
      51	int		 authenticated;	/* authenticated and alarms cancelled */
      52	int		 postponed;	/* authentication needs another step */
      53	int		 valid;		/* user exists and is allowed to login */
      54	int		 attempt;
      55	int		 failures;
      56	int		 server_caused_failure;
      57	int		 force_pwchange;
      58	char		*user;		/* username sent by the client */
      59	char		*service;
      60	struct passwd	*pw;		/* set if 'valid' */
      61	char		*style;
      62	void		*kbdintctxt;
      63	char		*info;		/* Extra info for next auth_log */
      64#ifdef BSD_AUTH
      65	auth_session_t	*as;
      66#endif
      67	char		**auth_methods;	/* modified from server config */
      68	u_int		 num_auth_methods;
      69#ifdef KRB5
      70	krb5_context	 krb5_ctx;
      71	krb5_ccache	 krb5_fwd_ccache;
      72	krb5_principal	 krb5_user;
      73	char		*krb5_ticket_file;
      74	char		*krb5_ccname;
      75#endif
      76	Buffer		*loginmsg;
      77	void		*methoddata;
      78};

/freebsd/include/pwd.h

    112struct passwd {
    113	char	*pw_name;		/* user name */
    114	char	*pw_passwd;		/* encrypted password */
    115	uid_t	pw_uid;			/* user uid */
    116	gid_t	pw_gid;			/* user gid */
    117	time_t	pw_change;		/* password change time */
    118	char	*pw_class;		/* user access class */
    119	char	*pw_gecos;		/* Honeywell login info */
    120	char	*pw_dir;		/* home directory */
    121	char	*pw_shell;		/* default shell */
    122	time_t	pw_expire;		/* account expiration */
    123	int	pw_fields;		/* internal: fields filled in */
    124};
