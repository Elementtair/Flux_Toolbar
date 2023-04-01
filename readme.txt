##
##
##        Mod title:  FluxToolBar
##
##      Mod version:  2.1.2
##  Works on FluxBB:  1.5.0, 1.5.1, 1.5.2, 1.5.3, 1.5.4, 1.5.11
##     Release date:  2013-08-14
##
##           Author:  Mpok (mpok@fluxbb.fr)
##     Contributors:  Vin100 (PunToolBar), CodeXP, adaur, Elementair
##
##      Description:  This mod displays a bar of buttons in post forms
##                    which makes it possible to add BBCode easily.
##                    Also adds some new bbcodes : inline quote,
##                    acronym, superscript, subscript, text alignments,
##                    and video.
##
##   Repository URL:  https://github.com/Elementtair/Flux_Toolbar
##
##   Affected files:  include/parser.php
##                    include/search_idx.php
##                    include/functions.php
##                    edit.php
##                    post.php
##                    viewtopic.php
##
##       Affects DB:  Yes
##
##       DISCLAIMER:  Please note that "mods" are not officially supported by
##                    FluxBB. Installation of this modification is done at
##                    your own risk. Backup your forum database and any and
##                    all applicable files before proceeding.
##
##

#
#---------[ 1. UPLOAD ]----------------------------------------------------
#---------[ 1. TELECHARGER LES FICHIERS ]----------------------------------
#

/files/install_mod.php				to	/your_forum_folder/
/files/smiley_picker.php			to	/your_forum_folder/
/files/img/fluxtoolbar/				to	/your_forum_folder/img/fluxtoolbar/
/files/include/cache_fluxtoolbar.php		to	/your_forum_folder/include/
/files/include/toolbar_func.js			to	/your_forum_folder/include/
/files/include/jscolor/				to	/your_forum_folder/include/jscolor/
/files/plugins/AP_FluxToolBar.php		to	/your_forum_folder/plugins/
/files/lang/English/fluxtoolbar.php		to	/your_forum_folder/lang/English/
/files/lang/English/fluxtoolbar_admin.php	to	/your_forum_folder/lang/English/
/files/lang/French/fluxtoolbar.php		to	/your_forum_folder/lang/French/
/files/lang/French/fluxtoolbar_admin.php	to	/your_forum_folder/lang/French/

#
#---------[ 2. RUN ]-------------------------------------------------------
#---------[ 2. LANCER ]----------------------------------------------------
#

install_mod.php

#
#---------[ 3. DELETE ]----------------------------------------------------
#---------[ 3. SUPPRIMER ]-------------------------------------------------
#

install_mod.php

#
#---------[ 4. OPEN ]------------------------------------------------------
#---------[ 4. OUVRIR ]----------------------------------------------------
#

post.php

#
#---------[ 5. FIND ]------------------------------------------------------
#---------[ 5. TROUVER ]---------------------------------------------------
#

<?php endif; ?>						<label class="required"><strong><?php echo $lang_common['Message'] ?> <span><?php echo $lang_common['Required'] ?></span></strong><br />
						<textarea name="req_message" rows="20" cols="95" tabindex="<?php echo $cur_index++ ?>"><?php echo isset($_POST['req_message']) ? pun_htmlspecialchars($orig_message) : (isset($quote) ? $quote : ''); ?></textarea><br /></label>

#
#---------[ 6. REPLACE WITH ]----------------------------------------------
#---------[ 6. REMPLACER PAR ]---------------------------------------------
#

<?php endif; ?>						<label class="required"><strong><?php echo $lang_common['Message'] ?> <span><?php echo $lang_common['Required'] ?></span></strong><br />
						<textarea id="req_message" name="req_message" rows="20" cols="95" tabindex="<?php echo $cur_index++ ?>"><?php echo isset($_POST['req_message']) ? pun_htmlspecialchars($orig_message) : (isset($quote) ? $quote : ''); ?></textarea><br /></label>
<?php /* FluxToolBar */
if (file_exists(FORUM_CACHE_DIR.'cache_fluxtoolbar_form.php'))
	include FORUM_CACHE_DIR.'cache_fluxtoolbar_form.php';
else
{
	require_once PUN_ROOT.'include/cache_fluxtoolbar.php';
	generate_ftb_cache('form');
	require FORUM_CACHE_DIR.'cache_fluxtoolbar_form.php';
}
?>

#
#---------[ 7. OPEN ]------------------------------------------------------
#---------[ 7. OUVRIR ]----------------------------------------------------
#

edit.php

#
#---------[ 8. FIND ]------------------------------------------------------
#---------[ 8. TROUVER ]---------------------------------------------------
#

<?php endif; ?>						<label class="required"><strong><?php echo $lang_common['Message'] ?> <span><?php echo $lang_common['Required'] ?></span></strong><br />
						<textarea name="req_message" rows="20" cols="95" tabindex="<?php echo $cur_index++ ?>"><?php echo pun_htmlspecialchars(isset($_POST['req_message']) ? $message : $cur_post['message']) ?></textarea><br /></label>

#
#---------[ 9. REPLACE WITH ]----------------------------------------------
#---------[ 9. REMPLACER PAR ]---------------------------------------------
#

<?php endif; ?>						<label class="required"><strong><?php echo $lang_common['Message'] ?> <span><?php echo $lang_common['Required'] ?></span></strong><br />
						<textarea id="req_message" name="req_message" rows="20" cols="95" tabindex="<?php echo $cur_index++ ?>"><?php echo pun_htmlspecialchars(isset($_POST['req_message']) ? $message : $cur_post['message']) ?></textarea><br /></label>
<?php /* FluxToolBar */
if (file_exists(FORUM_CACHE_DIR.'cache_fluxtoolbar_form.php'))
	include FORUM_CACHE_DIR.'cache_fluxtoolbar_form.php';
else
{
	require_once PUN_ROOT.'include/cache_fluxtoolbar.php';
	generate_ftb_cache('form');
	require FORUM_CACHE_DIR.'cache_fluxtoolbar_form.php';
}
?>

#
#---------[ 10. OPEN ]-----------------------------------------------------
#---------[ 10. OUVRIR ]---------------------------------------------------
#

viewtopic.php

#
#---------[ 11. FIND ]-----------------------------------------------------
#---------[ 11. TROUVER ]--------------------------------------------------
#

<textarea name="req_message" rows="7" cols="75" tabindex="<?php echo $cur_index++ ?>"></textarea></label>

#
#---------[ 12. REPLACE WITH ]---------------------------------------------
#---------[ 12. REMPLACER PAR ]--------------------------------------------
#

<textarea id="req_message" name="req_message" rows="7" cols="75" tabindex="<?php echo $cur_index++ ?>"></textarea></label>
<?php /* FluxToolBar */
if (file_exists(FORUM_CACHE_DIR.'cache_fluxtoolbar_quickform.php'))
	include FORUM_CACHE_DIR.'cache_fluxtoolbar_quickform.php';
else
{
	require_once PUN_ROOT.'include/cache_fluxtoolbar.php';
	generate_ftb_cache('quickform');
	require FORUM_CACHE_DIR.'cache_fluxtoolbar_quickform.php';
}
?>

#
#---------[ 13. OPEN ]-----------------------------------------------------
#---------[ 13. OUVRIR ]---------------------------------------------------
#

include/search_idx.php

#
#---------[ 14. FIND ]-----------------------------------------------------
#---------[ 14. TROUVER ]--------------------------------------------------
#

// Remove BBCode
	$text = preg_replace('%\[/?(b|u|s|ins|del|em|i|h|colou?r|quote|code|img|url|email|list|topic|post|forum|user)(?:\=[^\]]*)?\]%', ' ', $text);

	
#
#---------[ 15. ADD AFTER ]------------------------------------------------
#---------[ 15. AJOUTER APRES ]--------------------------------------------
#

	/* FluxToolBar */
	if (file_exists(FORUM_CACHE_DIR.'cache_fluxtoolbar_tag_search.php'))
		include FORUM_CACHE_DIR.'cache_fluxtoolbar_tag_search.php';
	else
	{
		require_once PUN_ROOT.'include/cache_fluxtoolbar.php';
		generate_ftb_cache('tags');
		require FORUM_CACHE_DIR.'cache_fluxtoolbar_tag_search.php';
	}


#
#---------[ 16. OPEN ]-----------------------------------------------------
#---------[ 16. OUVRIR ]---------------------------------------------------
#

include/functions.php

#
#---------[ 17. FIND ]-----------------------------------------------------
#---------[ 17. TROUVER ]--------------------------------------------------
#

	else if (preg_match('%(?:\[/?(?:b|u|s|ins|del|em|i|h|colou?r|quote|code|img|url|email|list|\*|topic|post|forum|user)\]|\[(?:img|url|quote|list)=)%i', $username))
		$errors[] = $lang_prof_reg['Username BBCode'];

#
#---------[ 18. ADD AFTER ]------------------------------------------------
#---------[ 18. AJOUTER APRES ]--------------------------------------------
#

	/* FluxToolBar */
	if (file_exists(FORUM_CACHE_DIR.'cache_fluxtoolbar_tag_check.php'))
		include FORUM_CACHE_DIR.'cache_fluxtoolbar_tag_check.php';
	else
	{
		require_once PUN_ROOT.'include/cache_fluxtoolbar.php';
		generate_ftb_cache('tags');
		require FORUM_CACHE_DIR.'cache_fluxtoolbar_tag_check.php';
	}

#
#---------[ 19. OPEN ]-----------------------------------------------------
#---------[ 19. OUVRIR ]---------------------------------------------------
#

include/parser.php

#
#---------[ 20. FIND ]-----------------------------------------------------
#---------[ 20. TROUVER ]--------------------------------------------------
#

		global $lang_profile;

		if (preg_match('%\[/?(?:quote|code|list|h)\b[^\]]*\]%i', $text))
			$errors[] = $lang_profile['Signature quote/code/list/h'];

#
#---------[ 21. ADD AFTER ]------------------------------------------------
#---------[ 21. AJOUTER APRES ]--------------------------------------------
#

		global $pun_user;
		if (preg_match('%\[/?(?:video|left|right|center|justify)\b[^\]]*\]%i', $text))
		{
			if (file_exists(PUN_ROOT.'lang/'.$pun_user['language'].'/fluxtoolbar.php'))
				require PUN_ROOT.'lang/'.$pun_user['language'].'/fluxtoolbar.php';
			else
				require PUN_ROOT.'lang/English/fluxtoolbar.php';
			$errors[] = $lang_ftb['Signature balises'];
		}

#
#---------[ 22. FIND ]-----------------------------------------------------
#---------[ 22. TROUVER ]--------------------------------------------------
#

	// Remove empty tags
	while (!is_null($new_text = preg_replace('%\[(b|u|s|ins|del|em|i|h|colou?r|quote|img|url|email|list|topic|post|forum|user)(?:\=[^\]]*)?\]\s*\[/\1\]%', '', $text)))

#
#---------[ 23. REPLACE WITH ]---------------------------------------------
#---------[ 23. REMPLACER PAR ]--------------------------------------------
#

	// Remove empty tags
	while (!is_null($new_text = preg_replace('%\[(b|u|s|ins|del|em|i|h|colou?r|quote|img|url|email|list|topic|post|forum|user|acronym|q|sup|sub|left|right|center|justify|video)(?:\=[^\]]*)?\]\s*\[/\1\]%', '', $text)))

#
#---------[ 24. FIND ]-----------------------------------------------------
#---------[ 24. TROUVER ]--------------------------------------------------
#

	// List of all the tags
	$tags = array('quote', 'code', 'b', 'i', 'u', 's', 'ins', 'del', 'em', 'color', 'colour', 'url', 'email', 'img', 'list', '*', 'h', 'topic', 'post', 'forum', 'user');
	// List of tags that we need to check are open (You could not put b,i,u in here then illegal nesting like [b][i][/b][/i] would be allowed)
	$tags_opened = $tags;
	// and tags we need to check are closed (the same as above, added it just in case)
	$tags_closed = $tags;
	// Tags we can nest and the depth they can be nested to
	$tags_nested = array('quote' => $pun_config['o_quote_depth'], 'list' => 5, '*' => 5);
	// Tags to ignore the contents of completely (just code)
	$tags_ignore = array('code');
	// Tags not allowed
	$tags_forbidden = array();
	// Block tags, block tags can only go within another block tag, they cannot be in a normal tag
	$tags_block = array('quote', 'code', 'list', 'h', '*');
	// Inline tags, we do not allow new lines in these
	$tags_inline = array('b', 'i', 'u', 's', 'ins', 'del', 'em', 'color', 'colour', 'h', 'topic', 'post', 'forum', 'user');
	// Tags we trim interior space
	$tags_trim = array('img');
	// Tags we remove quotes from the argument
	$tags_quotes = array('url', 'email', 'img', 'topic', 'post', 'forum', 'user');
	// Tags we limit bbcode in
	$tags_limit_bbcode = array(
		'*' 	=> array('b', 'i', 'u', 's', 'ins', 'del', 'em', 'color', 'colour', 'url', 'email', 'list', 'img', 'code', 'topic', 'post', 'forum', 'user'),
		'list' 	=> array('*'),
		'url' 	=> array('img'),
		'email' => array('img'),
		'topic' => array('img'),
		'post'  => array('img'),
		'forum' => array('img'),
		'user'  => array('img'),
		'img' 	=> array(),
		'h'	=> array('b', 'i', 'u', 's', 'ins', 'del', 'em', 'color', 'colour', 'url', 'email', 'topic', 'post', 'forum', 'user'),
	);
	// Tags we can automatically fix bad nesting
	


#
#---------[ 25. REPLACE WITH ]---------------------------------------------
#---------[ 25. REMPLACER PAR ]--------------------------------------------
#

	// List of all the tags
	$tags = array('quote', 'code', 'b', 'i', 'u', 's', 'ins', 'del', 'em', 'color', 'colour', 'url', 'email', 'img', 'list', '*', 'h', 'topic', 'post', 'forum', 'user', 'acronym', 'q', 'sup', 'sub', 'left', 'right', 'center', 'justify', 'video');
	// List of tags that we need to check are open (You could not put b,i,u in here then illegal nesting like [b][i][/b][/i] would be allowed)
	$tags_opened = $tags;
	// and tags we need to check are closed (the same as above, added it just in case)
	$tags_closed = $tags;
	// Tags we can nest and the depth they can be nested to
	$tags_nested = array('quote' => $pun_config['o_quote_depth'], 'list' => 5, '*' => 5);
	// Tags to ignore the contents of completely (just code)
	$tags_ignore = array('code');
	// Tags not allowed
	$tags_forbidden = array();
	// Block tags, block tags can only go within another block tag, they cannot be in a normal tag
	$tags_block = array('quote', 'code', 'list', 'h', '*', 'left', 'right', 'center', 'justify');
	// Inline tags, we do not allow new lines in these
	$tags_inline = array('b', 'i', 'u', 's', 'ins', 'del', 'em', 'color', 'colour', 'h', 'topic', 'post', 'forum', 'user', 'acronym', 'q', 'sup', 'sub', 'video');
	// Tags we trim interior space
	$tags_trim = array('img', 'video');
	// Tags we remove quotes from the argument
	$tags_quotes = array('url', 'email', 'img', 'topic', 'post', 'forum', 'user', 'video');
	// Tags we limit bbcode in
	$tags_limit_bbcode = array(
		'*' 	=> array('b', 'i', 'u', 's', 'ins', 'del', 'em', 'color', 'colour', 'url', 'email', 'list', 'img', 'code', 'topic', 'post', 'forum', 'user', 'acronym', 'q', 'sup', 'sub', 'video'),
		'list' 	=> array('*'),
		'url' 	=> array('img', 'acronym', 'q', 'sup', 'sub'),
		'email' => array('img', 'acronym', 'q', 'sup', 'sub'),
		'topic' => array('img'),
		'post'  => array('img'),
		'forum' => array('img'),
		'user'  => array('img'),
		'img' 	=> array(),
		'h'	=> array('b', 'i', 'u', 's', 'ins', 'del', 'em', 'color', 'colour', 'url', 'email', 'topic', 'post', 'forum', 'user'),
		'video'  => array()
	);
	// Tags we can automatically fix bad nesting

#
#---------[ 26. FIND ]-----------------------------------------------------
#---------[ 26. TROUVER ]--------------------------------------------------
#

	$pattern[] = '%\[b\](.*?)\[/b\]%ms';
	$pattern[] = '%\[i\](.*?)\[/i\]%ms';
	$pattern[] = '%\[u\](.*?)\[/u\]%ms';
	$pattern[] = '%\[s\](.*?)\[/s\]%ms';
	$pattern[] = '%\[del\](.*?)\[/del\]%ms';
	$pattern[] = '%\[ins\](.*?)\[/ins\]%ms';
	$pattern[] = '%\[em\](.*?)\[/em\]%ms';
	$pattern[] = '%\[colou?r=([a-zA-Z]{3,20}|\#[0-9a-fA-F]{6}|\#[0-9a-fA-F]{3})](.*?)\[/colou?r\]%ms';
	$pattern[] = '%\[h\](.*?)\[/h\]%ms';

	$replace[] = '<strong>$1</strong>';
	$replace[] = '<em>$1</em>';
	$replace[] = '<span class="bbu">$1</span>';
	$replace[] = '<span class="bbs">$1</span>';
	$replace[] = '<del>$1</del>';
	$replace[] = '<ins>$1</ins>';
	$replace[] = '<em>$1</em>';
	$replace[] = '<span style="color: $1">$2</span>';
	$replace[] = '</p><h5>$1</h5><p>';

#
#---------[ 27. REPLACE WITH ]---------------------------------------------
#---------[ 27. REMPLACER PAR ]--------------------------------------------
#

	$pattern[] = '%\[b\](.*?)\[/b\]%ms';
	$pattern[] = '%\[i\](.*?)\[/i\]%ms';
	$pattern[] = '%\[u\](.*?)\[/u\]%ms';
	$pattern[] = '%\[s\](.*?)\[/s\]%ms';
	$pattern[] = '%\[del\](.*?)\[/del\]%ms';
	$pattern[] = '%\[ins\](.*?)\[/ins\]%ms';
	$pattern[] = '%\[em\](.*?)\[/em\]%ms';
	$pattern[] = '%\[colou?r=([a-zA-Z]{3,20}|\#[0-9a-fA-F]{6}|\#[0-9a-fA-F]{3})](.*?)\[/colou?r\]%ms';
	$pattern[] = '%\[h\](.*?)\[/h\]%ms';
	$pattern[] = '%\[acronym\](.*?)\[/acronym\]%ms';
	$pattern[] = '%\[acronym=(.*?)\](.*?)\[/acronym\]%ms';
	$pattern[] = '%\[q\](.*?)\[/q\]%ms';
	$pattern[] = '%\[sup\](.*?)\[/sup\]%ms';
	$pattern[] = '%\[sub\](.*?)\[/sub\]%ms';
	$pattern[] = '%\[left\](.*?)\[/left\]%ms';
	$pattern[] = '%\[right\](.*?)\[/right\]%ms';
	$pattern[] = '%\[center\](.*?)\[/center\]%ms';
	$pattern[] = '%\[justify\](.*?)\[/justify\]%ms';
	$pattern[] = '%\[video\]([^\[<]*?)/video/([^\[<]*?)\[/video\]%ms';
	$pattern[] = '%\[video=([0-9]+),([0-9]+)\]([^\[<]*?)/video/([^_\[<]*?)_([^\[<]*?)\[/video\]%ms';
	$pattern[] = '%\[video\]([^\[<]*?)/(v/|watch\?v=)([^\[<]*?)\[/video\]%ms';
	$pattern[] = '%\[video=([0-9]+),([0-9]+)\]([^\[<]*?)/(v/|watch\?v=)([^\[<]*?)\[/video\]%ms';

	$replace[] = '<strong>$1</strong>';
	$replace[] = '<em>$1</em>';
	$replace[] = '<span class="bbu">$1</span>';
	$replace[] = '<span class="bbs">$1</span>';
	$replace[] = '<del>$1</del>';
	$replace[] = '<ins>$1</ins>';
	$replace[] = '<em>$1</em>';
	$replace[] = '<span style="color: $1">$2</span>';
	$replace[] = '</p><h5>$1</h5><p>';
	$replace[] = '<acronym>$1</acronym>';
	$replace[] = '<acronym title="$1">$2</acronym>';
	$replace[] = '<q>$1</q>';
	$replace[] = '<sup>$1</sup>';
	$replace[] = '<sub>$1</sub>';
	$replace[] = '</p><p style="text-align: left">$1</p><p>';
	$replace[] = '</p><p style="text-align: right">$1</p><p>';
	$replace[] = '</p><p style="text-align: center">$1</p><p>';
	$replace[] = '</p><p style="text-align: justify">$1</p><p>';
	$replace[] = '<iframe frameborder="0" width="200" height="145" src="https://www.dailymotion.com/embed/video/$2" allow="autoplay; fullscreen"></iframe>';
	$replace[] = '<iframe frameborder="0" width="200" height="145" src="https://www.dailymotion.com/embed/video/$4" allow="autoplay; fullscreen"></iframe>';
	$replace[] = '<iframe width="300" height="200" src="https://www.youtube.com/embed/$3" allowfullscreen></iframe>';
	$replace[] = '<object type="application/x-shockwave-flash" data="http://www.youtube.com/v/$5" width="$1" height="$2"><param name="movie" value="http://www.youtube.com/v/$5" /><param name="allowFullScreen" value="true" /><param name="allowScriptAccess" value="always" /><p>Flash required</p></object>';

#
#---------[ 28. SAVE / UPLOAD ]--------------------------------------------
#---------[ 28. ENREGISTRER / ENVOYER SUR LE SERVEUR ]---------------------
#

include/parser.php
include/search_idx.php
include/functions.php
edit.php
post.php
viewtopic.php

#
#---------[ 29. NOTES (English) ]------------------------------------------
#

You can now go to the plugin "FluxToolBar" for general settings, and to decide what buttons are displayed or not on the classic form and / or the quick reply form.
You can also decide to modify or remove certain buttons (note: only non-standard ones).

In the second page of the plugin, you can add new button images and create new buttons (ie new BBCodes).
When adding a button, you must edit include/parser.php and add messages for the corresponding button in your lang files.

#
#---------[ 29bis. NOTES (Français) ]--------------------------------------
#

Vous pouvez maintenant vous rendre sur le plugin "FluxToolBar" pour effectuer les réglages généraux, et décider quels boutons seront affichés ou non sur le formulaire classique et/ou le formulaire réponse rapide.
Vous pouvez également décider de modifier ou supprimer certains boutons (note : uniquement les boutons non-standards).

Dans la seconde page du plugin, vous pouvez ajouter de nouvelles images de bouton et créer de nouveaux boutons (c'est à dire de nouveaux BBCodes). Lors d'un ajout de bouton, vous devez modifier include/parser.php et ajouter les messages correspondants au bouton dans vos fichiers de langue.