# edit
<!--
	Redirector https to http:
		- konten gambar dan video facebook/gplus/youtube/dll
		- rule ini bebas silahkan di modifikasi untuk penambahan database yang diperlukan
-->
<ruleset name="reges007 https to http">
  <!--dibawah ini adalah daftar host yang akan di redirect ke http -->
<target host="*.akamaihd.net" />
<target host="*.googleusercontent.com" />
<target host="*.youtube.com" />
<target host="*.facebook.com" />
<target host="*.t.co" />
<target host="*.twimg.com" />
<target host="*.twitter.com" />
<target host="*.twitpic.com" />
<target host="flic.kr" />
<target host="*.flickr.com" />
<target host="*.staticflickr.com" />
<target host="*.pbsrc.com" />
<target host="*.photobucket.com" />
<target host="scbackstage.wpengine.netdna-cdn.com" />
<target host="soundcloud.wpengine.netdna-cdn.com" />
<target host="*.sndcdn.com" />
<target host="*.soundcloud.com" />
<target host="vimeo.com"/>
<target host="*.vimeo.com" />
<target host="*.vimeocdn.com" />
<target host="doubleclick.com"/>
<target host="www.doubleclick.com"/>
<target host="doubleclick.net"/>
<target host="*.doubleclick.net"/>
<target host="www.googleadservices.com"/>
<target host="google.*"/>
<target host="www.google.*"/>
<target host="google.co.*"/>
<target host="www.google.co.*"/>
<target host="google.com"/>
<target host="images.google.com"/>
<target host="google.com.*"/>
<target host="www.google.com.*"/>
<target host="apis.google.com"/>
<target host="*.apis.google.com"/>
<target host="www.google.com"/>
<target host="*.googleapis.com"/>
<target host="gstatic.com"/>
<target host="*.gstatic.com"/>

	<!--dibawah ini adalah daftar host/url pengecualian untuk tidak di proses redirect
      terkadang ada suatu url yang memang tidak bisa dipaksa ke http biasa -->
	<exclusion pattern="^https://apps.facebook.com/idant_wars" />
	<exclusion pattern="^https://apps.facebook.com/" />

  <!--dibawah ini adalah daftar url yang akan di redirect ke http secara spesifik-->

  <!--dibawah ini daftar konten gambar/video/games facebook-->	
	<rule from="^https://fbcdn-profile-a.akamaihd.net/"
		to="http://fbcdn-profile-a.akamaihd.net/" downgrade="1" />
		
	<rule from="^https://fbcdn-photos-([-a-z])-a.akamaihd.net/"
		to="http://fbcdn-photos-$1-a.akamaihd.net/" downgrade="1" />		

	<rule from="^https://fbexternal-a.akamaihd.net/(.*)"
		to="http://external.ak.fbcdn.net/$1" downgrade="1" />
	
	<rule from="^https://fbcdn-sphotos-([a-z])-a.akamaihd.net/"
		to="http://fbcdn-sphotos-$1-a.akamaihd.net/" downgrade="1" />

	<rule from="^https://fbcdn-video-a.akamaihd.net/"
		to="http://fbcdn-video-a.akamaihd.net/" downgrade="1" />
 
  <!--dibawah ini daftar dari konten google plus -->  		
	<rule from="^https://(.*).googleusercontent.com/"
		to="http://$1.googleusercontent.com/" downgrade="1" />

  <!--dibawah ini daftar dari youtube -->
	<rule from="^https://www.youtube.com/"
		to="http://www.youtube.com/" downgrade="1"/>

  <!--dibawah ini daftar dari T.CO-->
	<rule from="^https://(?:www\.)?t\.co/" 
		to="http://t.co/" downgrade="1" />
		
  <!--dibawah ini daftar dari twimg -->
	<rule from="^httpa://a\d\.twimg\.com/" 
		to="http://si0.twimg.com/" downgrade="1" />
		
	<rule from="^https://s\.twimg\.com/" 
		to="http://d2rdfnizen5apl.cloudfront.net/" downgrade="1" />
		
		  <!--dibawah ini daftar dari twitter -->
	<rule from="^https://((?:201\d|ads|(?:cdn\.)?api|business|preview(?:-dev|-stage)?\.cdn|de|dev|en|es|firefox|fr|it|ja|jp|m|media|mobile|music|oauth|p|platform|search|static|support|transparency|upload|www)\.)?twitter\.com/" 
		to="http://$1twitter.com/" downgrade="1" />
		
	<rule from="^https://(?:blo|engineerin)g\.twitter\.com/favicon\.ico" 
		to="http://www.blogger.com/favicon.ico" downgrade="1" />
		
	<rule from="^https://(?:anywhere\.|widgets\.)?platform\d?\.twitter\.com/" 
		to="http://platform.twitter.com/" downgrade="1" />	
	
	  <!--dibawah ini daftar dari twitpic -->
<rule from="^https://(?:www\.)?twitpic\.com/" 
		to="http://twitpic.com/" downgrade="1" />
		
		  <!--dibawah ini daftar dari flic.kr -->

		<rule from="^https://flic\.kr/f/" 
		to="http://www.flickr.com/short_urls.gne?favorites=" downgrade="1" />		
		
	<rule from="^https://flic\.kr/p/" 
		to="http://www.flickr.com/photo.gne?short=" downgrade="1" />
		
	<rule from="^http://flic\.kr/ps/" 
		to="http://www.flickr.com/short_urls.gne?photostream=" downgrade="1" />	
		
	<rule from="^http://flic\.kr/s/" 
		to="http://www.flickr.com/short_urls.gne?photoset=" downgrade="1" />

	
	  <!--dibawah ini daftar dari flickr-->
	<rule from="^https://(?:api\.|www\.)?flickr\.com/" 
		to="http://www.flickr.com/" downgrade="1" />	
		
	<rule from="^https://s(ecure|tatic)\.flickr\.com/" 
		to="http://s$1.flickr.com/" downgrade="1" />	
		
	  <!--dibawah ini daftar dari staticflickr -->
	<rule from="^https://farm(\d+)\.static(\.)?flickr\.com/" 
		to="http://farm$1.static$2flickr.com/" downgrade="1" />	
		
	  <!--dibawah ini daftar dari yimg -->	
	<rule from="^https://ads\.yimg\.com/" 
		to="http://s.yimg.com/zz/" downgrade="1" />
  
	<rule from="^https://(?:d|(?:a\.)?l\d?|us\.(?:a2|i1|js2?))\.yimg\.com/(?:a|d|us(?:\.js)?\.yimg\.com)/" 
		to="http://s.yimg.com/lq/" downgrade="1" />
		
	<rule from="^https://(?:d|(?:a\.)?l\d?|mail)\.yimg\.com/(ao|ck|cv|dh|ea|kj|kx|lo|mi|nt|ok|pj|pp|qa|rq|rx|ugcwidgets|zz)/" 
		to="http://s.yimg.com/$1/" downgrade="1" />
		
	<rule from="^https://(?:d|(?:a\.)?l\d?|us\.js1?|mail|xa)\.yimg\.com/(bb|bt|dg|(?:eur|us)\.yimg\.com|fg|[ghijqt]|gh|ho|j[ghn]|kq|lh|lm|ml|nn|nq|os|pb|pv|qb|qw|qz|r[luwz]|sc|ts)/" 
		to="http://s.yimg.com/zz/$1/" downgrade="1" />
		
	<rule from="^https://s(ec|xp)?\.yimg\.com/" 
		to="http://s$1.yimg.com/" downgrade="1" />
		
	<rule from="^https://s?ep\.yimg\.com/" 
		to="http://sep.yimg.com/" downgrade="1" />
		
	<rule from="^https://s\.yimg\.com/common/img/" 
		to="http://s.yimg.com/kj/ydn/common/img/" downgrade="1" />
		

		  <!--dibawah ini daftar dari pbsrc -->		
	<rule from="^https://(www\.)?pbsrc\.com/" 
		to="http://$1pbsrc.com/" downgrade="1"/>
	
	<rule from="^https://pic\.p(?:bsrc|hotobucket)\.com/" 
		to="http://pbsrc.com/" downgrade="1"/>
	
	<rule from="^https://o?(pic|static)2\.pbsrc\.com/" 
		to="http://o$12.pbsrc.com/" downgrade="1"/>
		
		  <!--dibawah ini daftar dari photobucket -->	
	<rule from="^https://b\.photobucket\.com/" 
		to="http://crtl.aimatch.com/" downgrade="1"/>
	
	<rule from="^https://(?:s619\.|secure-)?beta\.photobucket\.com/" 
		to="http://secure-beta.photobucket.com/" downgrade="1"/>
	
	<rule from="^https://secure\.photobucket\.com/" 
		to="http://secure.photobucket.com/" downgrade="1"/>
		
		<!--dibawah ini daftar dari sndcdn -->
	<rule from="^https://([aiw]\d|api|wis|i1|a[0-100])\.sndcdn\.com/" 
		to="http://$1.sndcdn.com/" downgrade="1"/>
	
	<!--dibawah ini daftar dari soundcloud -->
	<rule from="^https://((?:api|backstage|blog|connect|developers|ec-media|eventlogger|help-assets|media|visuals|w|www)\.)?soundcloud\.com/" 
		to="http://$1soundcloud.com/" downgrade="1"/>
		
	<rule from="^https?://scbackstage\.wpengine\.netdna-cdn\.com/" 
		to="http://backstage.soundcloud.com/" downgrade="1"/>
		
	<rule from="^https?://soundcloud\.wpengine\.netdna-cdn\.com/" 
		to="http://blog.soundcloud.com/" downgrade="1"/>
		
	<!--dibawah ini daftar dari vimeo -->
	<rule from="^https://((?:developer|player|secure|www)\.)?vimeo\.com/"
		to="http://$1vimeo.com/" downgrade="1" />
		
	<rule from="^https://av\.vimeo\.com/" 
		to="http://a248.e.akamai.net/f/808/9207/8m/av.vimeo.com/" downgrade="1" />
		
	<!--dibawah ini daftar dari vimeocdn -->
<rule from="^https://secure-$1.vimeocdn.com/" 
to="http://(?:secure-)?([a-z])\.vimeocdn\.com/"  downgrade="1" />
		
	<rule from="^https://pdl\.vimeocdn\.com/" 
		to="http://a248.e.akamai.net/f/1189/4415/8d/pdl.vimeocdn.com/" downgrade="1" />

		<!--dibawah ini daftar dari doubleclick -->
			
<rule from="^https://(?:www\.)?doubleclick\.com/" 
to="http://www.doubleclick.com/" downgrade="1" />
<rule from="^https://doubleclick\.net/" 
to="http://doubleclick.net/" downgrade="1" />
<rule from="^https://([^/:@\.]+)\.(?:es|nl|no)\.doubleclick\.net/" 
to="http://$1.doubleclick.net/" downgrade="1" />
<rule from="^https://([^/:@\.]+)(\.(?:au|de|fls|fr|g|jp|mo|uk))?\.doubleclick\.net/" 
to="http://$1$2.doubleclick.net/" downgrade="1" />
<rule from="^https://www\.googleadservices\.com/" 
to="http ://www.googleadservices.com/" downgrade="1" />

<rule from="^https://(?:www\.)?google\.(com?\.)?(ae|ar|at|au|bg|bh|br|ca|ch|cl|co|cr|cu|de|eg|es|fi|fr|gh|gt|hr|id|ie|il|it|jo|jp|jm|ke|kw|lb|ly|my|na|ng|nl|no|nz|om|pa|pe|pk|pl|pt|py|qa|ro|ru|rw|sa|se|sv|th|tr|uk|uy|ve|za|zw)/"
 to="http://www.google.$1$2/" downgrade="1" /> 	-->

 <rule from="^https://(?:www\.)?google\.com/(afsonline/|chart|jsapi|recaptcha/|uds)" 
 to="http://www.google.com/$1" downgrade="1" /> 	
 <rule from="^https://(api|[\w-]+\.client)s\.google\.com/" 
 to="http://$1s.google.com/" downgrade="1" /> 	
 <rule from="^https://chart\.apis\.google\.com/chart" 
 to="http://chart.googleapis.com/chart" downgrade="1" /> 	
 <rule from="^https://(ssl|www)\.google-analytics\.com/" 
 to="http://$1.google-analytics.com/" downgrade="1" />

 <rule from="^https://(?:www\.)?gstatic\.com/" 
 to="http://www.gstatic.com/" downgrade="1" />

</ruleset>
