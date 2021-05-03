# EDA--Haberman-Survival-Data-Set
Exploratory data analysis on Haberman Survival Data Set
<html><head><meta charset="utf-8">
<title>EDA</title><script src="https://cdnjs.cloudflare.com/ajax/libs/require.js/2.1.10/require.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/2.0.3/jquery.min.js"></script>

<style type="text/css">
    /*!
*
* Twitter Bootstrap
*
*/
/*!
 * Bootstrap v3.3.7 (http://getbootstrap.com)
 * Copyright 2011-2016 Twitter, Inc.
 * Licensed under MIT (https://github.com/twbs/bootstrap/blob/master/LICENSE)
 */
/*! normalize.css v3.0.3 | MIT License | github.com/necolas/normalize.css */
html {
  font-family: sans-serif;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
}
body {
  margin: 0;
}
article,
aside,
details,
figcaption,
figure,
footer,
header,
hgroup,
main,
menu,
nav,
section,
summary {
  display: block;
}
audio,
canvas,
progress,
video {
  display: inline-block;
  vertical-align: baseline;
}
audio:not([controls]) {
  display: none;
  height: 0;
}
[hidden],
template {
  display: none;
}
a {
  background-color: transparent;
}
a:active,
a:hover {
  outline: 0;
}
abbr[title] {
  border-bottom: 1px dotted;
}
b,
strong {
  font-weight: bold;
}
dfn {
  font-style: italic;
}
h1 {
  font-size: 2em;
  margin: 0.67em 0;
}
mark {
  background: #ff0;
  color: #000;
}
small {
  font-size: 80%;
}
sub,
sup {
  font-size: 75%;
  line-height: 0;
  position: relative;
  vertical-align: baseline;
}
sup {
  top: -0.5em;
}
sub {
  bottom: -0.25em;
}
img {
  border: 0;
}
svg:not(:root) {
  overflow: hidden;
}
figure {
  margin: 1em 40px;
}
hr {
  box-sizing: content-box;
  height: 0;
}
pre {
  overflow: auto;
}
code,
kbd,
pre,
samp {
  font-family: monospace, monospace;
  font-size: 1em;
}
button,
input,
optgroup,
select,
textarea {
  color: inherit;
  font: inherit;
  margin: 0;
}
button {
  overflow: visible;
}
button,
select {
  text-transform: none;
}
button,
html input[type="button"],
input[type="reset"],
input[type="submit"] {
  -webkit-appearance: button;
  cursor: pointer;
}
button[disabled],
html input[disabled] {
  cursor: default;
}
button::-moz-focus-inner,
input::-moz-focus-inner {
  border: 0;
  padding: 0;
}
input {
  line-height: normal;
}
input[type="checkbox"],
input[type="radio"] {
  box-sizing: border-box;
  padding: 0;
}
input[type="number"]::-webkit-inner-spin-button,
input[type="number"]::-webkit-outer-spin-button {
  height: auto;
}
input[type="search"] {
  -webkit-appearance: textfield;
  box-sizing: content-box;
}
input[type="search"]::-webkit-search-cancel-button,
input[type="search"]::-webkit-search-decoration {
  -webkit-appearance: none;
}
fieldset {
  border: 1px solid #c0c0c0;
  margin: 0 2px;
  padding: 0.35em 0.625em 0.75em;
}
legend {
  border: 0;
  padding: 0;
}
textarea {
  overflow: auto;
}
optgroup {
  font-weight: bold;
}
table {
  border-collapse: collapse;
  border-spacing: 0;
}
td,
th {
  padding: 0;
}
/*! Source: https://github.com/h5bp/html5-boilerplate/blob/master/src/css/main.css */
@media print {
  *,
  *:before,
  *:after {
    background: transparent !important;
    color: #000 !important;
    box-shadow: none !important;
    text-shadow: none !important;
  }
  a,
  a:visited {
    text-decoration: underline;
  }
  a[href]:after {
    content: " (" attr(href) ")";
  }
  abbr[title]:after {
    content: " (" attr(title) ")";
  }
  a[href^="#"]:after,
  a[href^="javascript:"]:after {
    content: "";
  }
  pre,
  blockquote {
    border: 1px solid #999;
    page-break-inside: avoid;
  }
  thead {
    display: table-header-group;
  }
  tr,
  img {
    page-break-inside: avoid;
  }
  img {
    max-width: 100% !important;
  }
  p,
  h2,
  h3 {
    orphans: 3;
    widows: 3;
  }
  h2,
  h3 {
    page-break-after: avoid;
  }
  .navbar {
    display: none;
  }
  .btn > .caret,
  .dropup > .btn > .caret {
    border-top-color: #000 !important;
  }
  .label {
    border: 1px solid #000;
  }
  .table {
    border-collapse: collapse !important;
  }
  .table td,
  .table th {
    background-color: #fff !important;
  }
  .table-bordered th,
  .table-bordered td {
    border: 1px solid #ddd !important;
  }
}
@font-face {
  font-family: 'Glyphicons Halflings';
  src: url('../components/bootstrap/fonts/glyphicons-halflings-regular.eot');
  src: url('../components/bootstrap/fonts/glyphicons-halflings-regular.eot?#iefix') format('embedded-opentype'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.woff2') format('woff2'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.woff') format('woff'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.ttf') format('truetype'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.svg#glyphicons_halflingsregular') format('svg');
}
.glyphicon {
  position: relative;
  top: 1px;
  display: inline-block;
  font-family: 'Glyphicons Halflings';
  font-style: normal;
  font-weight: normal;
  line-height: 1;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
.glyphicon-asterisk:before {
  content: "\002a";
}
.glyphicon-plus:before {
  content: "\002b";
}
.glyphicon-euro:before,
.glyphicon-eur:before {
  content: "\20ac";
}
.glyphicon-minus:before {
  content: "\2212";
}
.glyphicon-cloud:before {
  content: "\2601";
}
.glyphicon-envelope:before {
  content: "\2709";
}
.glyphicon-pencil:before {
  content: "\270f";
}
.glyphicon-glass:before {
  content: "\e001";
}
.glyphicon-music:before {
  content: "\e002";
}
.glyphicon-search:before {
  content: "\e003";
}
.glyphicon-heart:before {
  content: "\e005";
}
.glyphicon-star:before {
  content: "\e006";
}
.glyphicon-star-empty:before {
  content: "\e007";
}
.glyphicon-user:before {
  content: "\e008";
}
.glyphicon-film:before {
  content: "\e009";
}
.glyphicon-th-large:before {
  content: "\e010";
}
.glyphicon-th:before {
  content: "\e011";
}
.glyphicon-th-list:before {
  content: "\e012";
}
.glyphicon-ok:before {
  content: "\e013";
}
.glyphicon-remove:before {
  content: "\e014";
}
.glyphicon-zoom-in:before {
  content: "\e015";
}
.glyphicon-zoom-out:before {
  content: "\e016";
}
.glyphicon-off:before {
  content: "\e017";
}
.glyphicon-signal:before {
  content: "\e018";
}
.glyphicon-cog:before {
  content: "\e019";
}
.glyphicon-trash:before {
  content: "\e020";
}
.glyphicon-home:before {
  content: "\e021";
}
.glyphicon-file:before {
  content: "\e022";
}
.glyphicon-time:before {
  content: "\e023";
}
.glyphicon-road:before {
  content: "\e024";
}
.glyphicon-download-alt:before {
  content: "\e025";
}
.glyphicon-download:before {
  content: "\e026";
}
.glyphicon-upload:before {
  content: "\e027";
}
.glyphicon-inbox:before {
  content: "\e028";
}
.glyphicon-play-circle:before {
  content: "\e029";
}
.glyphicon-repeat:before {
  content: "\e030";
}
.glyphicon-refresh:before {
  content: "\e031";
}
.glyphicon-list-alt:before {
  content: "\e032";
}
.glyphicon-lock:before {
  content: "\e033";
}
.glyphicon-flag:before {
  content: "\e034";
}
.glyphicon-headphones:before {
  content: "\e035";
}
.glyphicon-volume-off:before {
  content: "\e036";
}
.glyphicon-volume-down:before {
  content: "\e037";
}
.glyphicon-volume-up:before {
  content: "\e038";
}
.glyphicon-qrcode:before {
  content: "\e039";
}
.glyphicon-barcode:before {
  content: "\e040";
}
.glyphicon-tag:before {
  content: "\e041";
}
.glyphicon-tags:before {
  content: "\e042";
}
.glyphicon-book:before {
  content: "\e043";
}
.glyphicon-bookmark:before {
  content: "\e044";
}
.glyphicon-print:before {
  content: "\e045";
}
.glyphicon-camera:before {
  content: "\e046";
}
.glyphicon-font:before {
  content: "\e047";
}
.glyphicon-bold:before {
  content: "\e048";
}
.glyphicon-italic:before {
  content: "\e049";
}
.glyphicon-text-height:before {
  content: "\e050";
}
.glyphicon-text-width:before {
  content: "\e051";
}
.glyphicon-align-left:before {
  content: "\e052";
}
.glyphicon-align-center:before {
  content: "\e053";
}
.glyphicon-align-right:before {
  content: "\e054";
}
.glyphicon-align-justify:before {
  content: "\e055";
}
.glyphicon-list:before {
  content: "\e056";
}
.glyphicon-indent-left:before {
  content: "\e057";
}
.glyphicon-indent-right:before {
  content: "\e058";
}
.glyphicon-facetime-video:before {
  content: "\e059";
}
.glyphicon-picture:before {
  content: "\e060";
}
.glyphicon-map-marker:before {
  content: "\e062";
}
.glyphicon-adjust:before {
  content: "\e063";
}
.glyphicon-tint:before {
  content: "\e064";
}
.glyphicon-edit:before {
  content: "\e065";
}
.glyphicon-share:before {
  content: "\e066";
}
.glyphicon-check:before {
  content: "\e067";
}
.glyphicon-move:before {
  content: "\e068";
}
.glyphicon-step-backward:before {
  content: "\e069";
}
.glyphicon-fast-backward:before {
  content: "\e070";
}
.glyphicon-backward:before {
  content: "\e071";
}
.glyphicon-play:before {
  content: "\e072";
}
.glyphicon-pause:before {
  content: "\e073";
}
.glyphicon-stop:before {
  content: "\e074";
}
.glyphicon-forward:before {
  content: "\e075";
}
.glyphicon-fast-forward:before {
  content: "\e076";
}
.glyphicon-step-forward:before {
  content: "\e077";
}
.glyphicon-eject:before {
  content: "\e078";
}
.glyphicon-chevron-left:before {
  content: "\e079";
}
.glyphicon-chevron-right:before {
  content: "\e080";
}
.glyphicon-plus-sign:before {
  content: "\e081";
}
.glyphicon-minus-sign:before {
  content: "\e082";
}
.glyphicon-remove-sign:before {
  content: "\e083";
}
.glyphicon-ok-sign:before {
  content: "\e084";
}
.glyphicon-question-sign:before {
  content: "\e085";
}
.glyphicon-info-sign:before {
  content: "\e086";
}
.glyphicon-screenshot:before {
  content: "\e087";
}
.glyphicon-remove-circle:before {
  content: "\e088";
}
.glyphicon-ok-circle:before {
  content: "\e089";
}
.glyphicon-ban-circle:before {
  content: "\e090";
}
.glyphicon-arrow-left:before {
  content: "\e091";
}
.glyphicon-arrow-right:before {
  content: "\e092";
}
.glyphicon-arrow-up:before {
  content: "\e093";
}
.glyphicon-arrow-down:before {
  content: "\e094";
}
.glyphicon-share-alt:before {
  content: "\e095";
}
.glyphicon-resize-full:before {
  content: "\e096";
}
.glyphicon-resize-small:before {
  content: "\e097";
}
.glyphicon-exclamation-sign:before {
  content: "\e101";
}
.glyphicon-gift:before {
  content: "\e102";
}
.glyphicon-leaf:before {
  content: "\e103";
}
.glyphicon-fire:before {
  content: "\e104";
}
.glyphicon-eye-open:before {
  content: "\e105";
}
.glyphicon-eye-close:before {
  content: "\e106";
}
.glyphicon-warning-sign:before {
  content: "\e107";
}
.glyphicon-plane:before {
  content: "\e108";
}
.glyphicon-calendar:before {
  content: "\e109";
}
.glyphicon-random:before {
  content: "\e110";
}
.glyphicon-comment:before {
  content: "\e111";
}
.glyphicon-magnet:before {
  content: "\e112";
}
.glyphicon-chevron-up:before {
  content: "\e113";
}
.glyphicon-chevron-down:before {
  content: "\e114";
}
.glyphicon-retweet:before {
  content: "\e115";
}
.glyphicon-shopping-cart:before {
  content: "\e116";
}
.glyphicon-folder-close:before {
  content: "\e117";
}
.glyphicon-folder-open:before {
  content: "\e118";
}
.glyphicon-resize-vertical:before {
  content: "\e119";
}
.glyphicon-resize-horizontal:before {
  content: "\e120";
}
.glyphicon-hdd:before {
  content: "\e121";
}
.glyphicon-bullhorn:before {
  content: "\e122";
}
.glyphicon-bell:before {
  content: "\e123";
}
.glyphicon-certificate:before {
  content: "\e124";
}
.glyphicon-thumbs-up:before {
  content: "\e125";
}
.glyphicon-thumbs-down:before {
  content: "\e126";
}
.glyphicon-hand-right:before {
  content: "\e127";
}
.glyphicon-hand-left:before {
  content: "\e128";
}
.glyphicon-hand-up:before {
  content: "\e129";
}
.glyphicon-hand-down:before {
  content: "\e130";
}
.glyphicon-circle-arrow-right:before {
  content: "\e131";
}
.glyphicon-circle-arrow-left:before {
  content: "\e132";
}
.glyphicon-circle-arrow-up:before {
  content: "\e133";
}
.glyphicon-circle-arrow-down:before {
  content: "\e134";
}
.glyphicon-globe:before {
  content: "\e135";
}
.glyphicon-wrench:before {
  content: "\e136";
}
.glyphicon-tasks:before {
  content: "\e137";
}
.glyphicon-filter:before {
  content: "\e138";
}
.glyphicon-briefcase:before {
  content: "\e139";
}
.glyphicon-fullscreen:before {
  content: "\e140";
}
.glyphicon-dashboard:before {
  content: "\e141";
}
.glyphicon-paperclip:before {
  content: "\e142";
}
.glyphicon-heart-empty:before {
  content: "\e143";
}
.glyphicon-link:before {
  content: "\e144";
}
.glyphicon-phone:before {
  content: "\e145";
}
.glyphicon-pushpin:before {
  content: "\e146";
}
.glyphicon-usd:before {
  content: "\e148";
}
.glyphicon-gbp:before {
  content: "\e149";
}
.glyphicon-sort:before {
  content: "\e150";
}
.glyphicon-sort-by-alphabet:before {
  content: "\e151";
}
.glyphicon-sort-by-alphabet-alt:before {
  content: "\e152";
}
.glyphicon-sort-by-order:before {
  content: "\e153";
}
.glyphicon-sort-by-order-alt:before {
  content: "\e154";
}
.glyphicon-sort-by-attributes:before {
  content: "\e155";
}
.glyphicon-sort-by-attributes-alt:before {
  content: "\e156";
}
.glyphicon-unchecked:before {
  content: "\e157";
}
.glyphicon-expand:before {
  content: "\e158";
}
.glyphicon-collapse-down:before {
  content: "\e159";
}
.glyphicon-collapse-up:before {
  content: "\e160";
}
.glyphicon-log-in:before {
  content: "\e161";
}
.glyphicon-flash:before {
  content: "\e162";
}
.glyphicon-log-out:before {
  content: "\e163";
}
.glyphicon-new-window:before {
  content: "\e164";
}
.glyphicon-record:before {
  content: "\e165";
}
.glyphicon-save:before {
  content: "\e166";
}
.glyphicon-open:before {
  content: "\e167";
}
.glyphicon-saved:before {
  content: "\e168";
}
.glyphicon-import:before {
  content: "\e169";
}
.glyphicon-export:before {
  content: "\e170";
}
.glyphicon-send:before {
  content: "\e171";
}
.glyphicon-floppy-disk:before {
  content: "\e172";
}
.glyphicon-floppy-saved:before {
  content: "\e173";
}
.glyphicon-floppy-remove:before {
  content: "\e174";
}
.glyphicon-floppy-save:before {
  content: "\e175";
}
.glyphicon-floppy-open:before {
  content: "\e176";
}
.glyphicon-credit-card:before {
  content: "\e177";
}
.glyphicon-transfer:before {
  content: "\e178";
}
.glyphicon-cutlery:before {
  content: "\e179";
}
.glyphicon-header:before {
  content: "\e180";
}
.glyphicon-compressed:before {
  content: "\e181";
}
.glyphicon-earphone:before {
  content: "\e182";
}
.glyphicon-phone-alt:before {
  content: "\e183";
}
.glyphicon-tower:before {
  content: "\e184";
}
.glyphicon-stats:before {
  content: "\e185";
}
.glyphicon-sd-video:before {
  content: "\e186";
}
.glyphicon-hd-video:before {
  content: "\e187";
}
.glyphicon-subtitles:before {
  content: "\e188";
}
.glyphicon-sound-stereo:before {
  content: "\e189";
}
.glyphicon-sound-dolby:before {
  content: "\e190";
}
.glyphicon-sound-5-1:before {
  content: "\e191";
}
.glyphicon-sound-6-1:before {
  content: "\e192";
}
.glyphicon-sound-7-1:before {
  content: "\e193";
}
.glyphicon-copyright-mark:before {
  content: "\e194";
}
.glyphicon-registration-mark:before {
  content: "\e195";
}
.glyphicon-cloud-download:before {
  content: "\e197";
}
.glyphicon-cloud-upload:before {
  content: "\e198";
}
.glyphicon-tree-conifer:before {
  content: "\e199";
}
.glyphicon-tree-deciduous:before {
  content: "\e200";
}
.glyphicon-cd:before {
  content: "\e201";
}
.glyphicon-save-file:before {
  content: "\e202";
}
.glyphicon-open-file:before {
  content: "\e203";
}
.glyphicon-level-up:before {
  content: "\e204";
}
.glyphicon-copy:before {
  content: "\e205";
}
.glyphicon-paste:before {
  content: "\e206";
}
.glyphicon-alert:before {
  content: "\e209";
}
.glyphicon-equalizer:before {
  content: "\e210";
}
.glyphicon-king:before {
  content: "\e211";
}
.glyphicon-queen:before {
  content: "\e212";
}
.glyphicon-pawn:before {
  content: "\e213";
}
.glyphicon-bishop:before {
  content: "\e214";
}
.glyphicon-knight:before {
  content: "\e215";
}
.glyphicon-baby-formula:before {
  content: "\e216";
}
.glyphicon-tent:before {
  content: "\26fa";
}
.glyphicon-blackboard:before {
  content: "\e218";
}
.glyphicon-bed:before {
  content: "\e219";
}
.glyphicon-apple:before {
  content: "\f8ff";
}
.glyphicon-erase:before {
  content: "\e221";
}
.glyphicon-hourglass:before {
  content: "\231b";
}
.glyphicon-lamp:before {
  content: "\e223";
}
.glyphicon-duplicate:before {
  content: "\e224";
}
.glyphicon-piggy-bank:before {
  content: "\e225";
}
.glyphicon-scissors:before {
  content: "\e226";
}
.glyphicon-bitcoin:before {
  content: "\e227";
}
.glyphicon-btc:before {
  content: "\e227";
}
.glyphicon-xbt:before {
  content: "\e227";
}
.glyphicon-yen:before {
  content: "\00a5";
}
.glyphicon-jpy:before {
  content: "\00a5";
}
.glyphicon-ruble:before {
  content: "\20bd";
}
.glyphicon-rub:before {
  content: "\20bd";
}
.glyphicon-scale:before {
  content: "\e230";
}
.glyphicon-ice-lolly:before {
  content: "\e231";
}
.glyphicon-ice-lolly-tasted:before {
  content: "\e232";
}
.glyphicon-education:before {
  content: "\e233";
}
.glyphicon-option-horizontal:before {
  content: "\e234";
}
.glyphicon-option-vertical:before {
  content: "\e235";
}
.glyphicon-menu-hamburger:before {
  content: "\e236";
}
.glyphicon-modal-window:before {
  content: "\e237";
}
.glyphicon-oil:before {
  content: "\e238";
}
.glyphicon-grain:before {
  content: "\e239";
}
.glyphicon-sunglasses:before {
  content: "\e240";
}
.glyphicon-text-size:before {
  content: "\e241";
}
.glyphicon-text-color:before {
  content: "\e242";
}
.glyphicon-text-background:before {
  content: "\e243";
}
.glyphicon-object-align-top:before {
  content: "\e244";
}
.glyphicon-object-align-bottom:before {
  content: "\e245";
}
.glyphicon-object-align-horizontal:before {
  content: "\e246";
}
.glyphicon-object-align-left:before {
  content: "\e247";
}
.glyphicon-object-align-vertical:before {
  content: "\e248";
}
.glyphicon-object-align-right:before {
  content: "\e249";
}
.glyphicon-triangle-right:before {
  content: "\e250";
}
.glyphicon-triangle-left:before {
  content: "\e251";
}
.glyphicon-triangle-bottom:before {
  content: "\e252";
}
.glyphicon-triangle-top:before {
  content: "\e253";
}
.glyphicon-console:before {
  content: "\e254";
}
.glyphicon-superscript:before {
  content: "\e255";
}
.glyphicon-subscript:before {
  content: "\e256";
}
.glyphicon-menu-left:before {
  content: "\e257";
}
.glyphicon-menu-right:before {
  content: "\e258";
}
.glyphicon-menu-down:before {
  content: "\e259";
}
.glyphicon-menu-up:before {
  content: "\e260";
}
* {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}
*:before,
*:after {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}
html {
  font-size: 10px;
  -webkit-tap-highlight-color: rgba(0, 0, 0, 0);
}
body {
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-size: 13px;
  line-height: 1.42857143;
  color: #000;
  background-color: #fff;
}
input,
button,
select,
textarea {
  font-family: inherit;
  font-size: inherit;
  line-height: inherit;
}
a {
  color: #337ab7;
  text-decoration: none;
}
a:hover,
a:focus {
  color: #23527c;
  text-decoration: underline;
}
a:focus {
  outline: 5px auto -webkit-focus-ring-color;
  outline-offset: -2px;
}
figure {
  margin: 0;
}
img {
  vertical-align: middle;
}
.img-responsive,
.thumbnail > img,
.thumbnail a > img,
.carousel-inner > .item > img,
.carousel-inner > .item > a > img {
  display: block;
  max-width: 100%;
  height: auto;
}
.img-rounded {
  border-radius: 3px;
}
.img-thumbnail {
  padding: 4px;
  line-height: 1.42857143;
  background-color: #fff;
  border: 1px solid #ddd;
  border-radius: 2px;
  -webkit-transition: all 0.2s ease-in-out;
  -o-transition: all 0.2s ease-in-out;
  transition: all 0.2s ease-in-out;
  display: inline-block;
  max-width: 100%;
  height: auto;
}
.img-circle {
  border-radius: 50%;
}
hr {
  margin-top: 18px;
  margin-bottom: 18px;
  border: 0;
  border-top: 1px solid #eeeeee;
}
.sr-only {
  position: absolute;
  width: 1px;
  height: 1px;
  margin: -1px;
  padding: 0;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
  border: 0;
}
.sr-only-focusable:active,
.sr-only-focusable:focus {
  position: static;
  width: auto;
  height: auto;
  margin: 0;
  overflow: visible;
  clip: auto;
}
[role="button"] {
  cursor: pointer;
}
h1,
h2,
h3,
h4,
h5,
h6,
.h1,
.h2,
.h3,
.h4,
.h5,
.h6 {
  font-family: inherit;
  font-weight: 500;
  line-height: 1.1;
  color: inherit;
}
h1 small,
h2 small,
h3 small,
h4 small,
h5 small,
h6 small,
.h1 small,
.h2 small,
.h3 small,
.h4 small,
.h5 small,
.h6 small,
h1 .small,
h2 .small,
h3 .small,
h4 .small,
h5 .small,
h6 .small,
.h1 .small,
.h2 .small,
.h3 .small,
.h4 .small,
.h5 .small,
.h6 .small {
  font-weight: normal;
  line-height: 1;
  color: #777777;
}
h1,
.h1,
h2,
.h2,
h3,
.h3 {
  margin-top: 18px;
  margin-bottom: 9px;
}
h1 small,
.h1 small,
h2 small,
.h2 small,
h3 small,
.h3 small,
h1 .small,
.h1 .small,
h2 .small,
.h2 .small,
h3 .small,
.h3 .small {
  font-size: 65%;
}
h4,
.h4,
h5,
.h5,
h6,
.h6 {
  margin-top: 9px;
  margin-bottom: 9px;
}
h4 small,
.h4 small,
h5 small,
.h5 small,
h6 small,
.h6 small,
h4 .small,
.h4 .small,
h5 .small,
.h5 .small,
h6 .small,
.h6 .small {
  font-size: 75%;
}
h1,
.h1 {
  font-size: 33px;
}
h2,
.h2 {
  font-size: 27px;
}
h3,
.h3 {
  font-size: 23px;
}
h4,
.h4 {
  font-size: 17px;
}
h5,
.h5 {
  font-size: 13px;
}
h6,
.h6 {
  font-size: 12px;
}
p {
  margin: 0 0 9px;
}
.lead {
  margin-bottom: 18px;
  font-size: 14px;
  font-weight: 300;
  line-height: 1.4;
}
@media (min-width: 768px) {
  .lead {
    font-size: 19.5px;
  }
}
small,
.small {
  font-size: 92%;
}
mark,
.mark {
  background-color: #fcf8e3;
  padding: .2em;
}
.text-left {
  text-align: left;
}
.text-right {
  text-align: right;
}
.text-center {
  text-align: center;
}
.text-justify {
  text-align: justify;
}
.text-nowrap {
  white-space: nowrap;
}
.text-lowercase {
  text-transform: lowercase;
}
.text-uppercase {
  text-transform: uppercase;
}
.text-capitalize {
  text-transform: capitalize;
}
.text-muted {
  color: #777777;
}
.text-primary {
  color: #337ab7;
}
a.text-primary:hover,
a.text-primary:focus {
  color: #286090;
}
.text-success {
  color: #3c763d;
}
a.text-success:hover,
a.text-success:focus {
  color: #2b542c;
}
.text-info {
  color: #31708f;
}
a.text-info:hover,
a.text-info:focus {
  color: #245269;
}
.text-warning {
  color: #8a6d3b;
}
a.text-warning:hover,
a.text-warning:focus {
  color: #66512c;
}
.text-danger {
  color: #a94442;
}
a.text-danger:hover,
a.text-danger:focus {
  color: #843534;
}
.bg-primary {
  color: #fff;
  background-color: #337ab7;
}
a.bg-primary:hover,
a.bg-primary:focus {
  background-color: #286090;
}
.bg-success {
  background-color: #dff0d8;
}
a.bg-success:hover,
a.bg-success:focus {
  background-color: #c1e2b3;
}
.bg-info {
  background-color: #d9edf7;
}
a.bg-info:hover,
a.bg-info:focus {
  background-color: #afd9ee;
}
.bg-warning {
  background-color: #fcf8e3;
}
a.bg-warning:hover,
a.bg-warning:focus {
  background-color: #f7ecb5;
}
.bg-danger {
  background-color: #f2dede;
}
a.bg-danger:hover,
a.bg-danger:focus {
  background-color: #e4b9b9;
}
.page-header {
  padding-bottom: 8px;
  margin: 36px 0 18px;
  border-bottom: 1px solid #eeeeee;
}
ul,
ol {
  margin-top: 0;
  margin-bottom: 9px;
}
ul ul,
ol ul,
ul ol,
ol ol {
  margin-bottom: 0;
}
.list-unstyled {
  padding-left: 0;
  list-style: none;
}
.list-inline {
  padding-left: 0;
  list-style: none;
  margin-left: -5px;
}
.list-inline > li {
  display: inline-block;
  padding-left: 5px;
  padding-right: 5px;
}
dl {
  margin-top: 0;
  margin-bottom: 18px;
}
dt,
dd {
  line-height: 1.42857143;
}
dt {
  font-weight: bold;
}
dd {
  margin-left: 0;
}
@media (min-width: 541px) {
  .dl-horizontal dt {
    float: left;
    width: 160px;
    clear: left;
    text-align: right;
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
  }
  .dl-horizontal dd {
    margin-left: 180px;
  }
}
abbr[title],
abbr[data-original-title] {
  cursor: help;
  border-bottom: 1px dotted #777777;
}
.initialism {
  font-size: 90%;
  text-transform: uppercase;
}
blockquote {
  padding: 9px 18px;
  margin: 0 0 18px;
  font-size: inherit;
  border-left: 5px solid #eeeeee;
}
blockquote p:last-child,
blockquote ul:last-child,
blockquote ol:last-child {
  margin-bottom: 0;
}
blockquote footer,
blockquote small,
blockquote .small {
  display: block;
  font-size: 80%;
  line-height: 1.42857143;
  color: #777777;
}
blockquote footer:before,
blockquote small:before,
blockquote .small:before {
  content: '\2014 \00A0';
}
.blockquote-reverse,
blockquote.pull-right {
  padding-right: 15px;
  padding-left: 0;
  border-right: 5px solid #eeeeee;
  border-left: 0;
  text-align: right;
}
.blockquote-reverse footer:before,
blockquote.pull-right footer:before,
.blockquote-reverse small:before,
blockquote.pull-right small:before,
.blockquote-reverse .small:before,
blockquote.pull-right .small:before {
  content: '';
}
.blockquote-reverse footer:after,
blockquote.pull-right footer:after,
.blockquote-reverse small:after,
blockquote.pull-right small:after,
.blockquote-reverse .small:after,
blockquote.pull-right .small:after {
  content: '\00A0 \2014';
}
address {
  margin-bottom: 18px;
  font-style: normal;
  line-height: 1.42857143;
}
code,
kbd,
pre,
samp {
  font-family: monospace;
}
code {
  padding: 2px 4px;
  font-size: 90%;
  color: #c7254e;
  background-color: #f9f2f4;
  border-radius: 2px;
}
kbd {
  padding: 2px 4px;
  font-size: 90%;
  color: #888;
  background-color: transparent;
  border-radius: 1px;
  box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.25);
}
kbd kbd {
  padding: 0;
  font-size: 100%;
  font-weight: bold;
  box-shadow: none;
}
pre {
  display: block;
  padding: 8.5px;
  margin: 0 0 9px;
  font-size: 12px;
  line-height: 1.42857143;
  word-break: break-all;
  word-wrap: break-word;
  color: #333333;
  background-color: #f5f5f5;
  border: 1px solid #ccc;
  border-radius: 2px;
}
pre code {
  padding: 0;
  font-size: inherit;
  color: inherit;
  white-space: pre-wrap;
  background-color: transparent;
  border-radius: 0;
}
.pre-scrollable {
  max-height: 340px;
  overflow-y: scroll;
}
.container {
  margin-right: auto;
  margin-left: auto;
  padding-left: 0px;
  padding-right: 0px;
}
@media (min-width: 768px) {
  .container {
    width: 768px;
  }
}
@media (min-width: 992px) {
  .container {
    width: 940px;
  }
}
@media (min-width: 1200px) {
  .container {
    width: 1140px;
  }
}
.container-fluid {
  margin-right: auto;
  margin-left: auto;
  padding-left: 0px;
  padding-right: 0px;
}
.row {
  margin-left: 0px;
  margin-right: 0px;
}
.col-xs-1, .col-sm-1, .col-md-1, .col-lg-1, .col-xs-2, .col-sm-2, .col-md-2, .col-lg-2, .col-xs-3, .col-sm-3, .col-md-3, .col-lg-3, .col-xs-4, .col-sm-4, .col-md-4, .col-lg-4, .col-xs-5, .col-sm-5, .col-md-5, .col-lg-5, .col-xs-6, .col-sm-6, .col-md-6, .col-lg-6, .col-xs-7, .col-sm-7, .col-md-7, .col-lg-7, .col-xs-8, .col-sm-8, .col-md-8, .col-lg-8, .col-xs-9, .col-sm-9, .col-md-9, .col-lg-9, .col-xs-10, .col-sm-10, .col-md-10, .col-lg-10, .col-xs-11, .col-sm-11, .col-md-11, .col-lg-11, .col-xs-12, .col-sm-12, .col-md-12, .col-lg-12 {
  position: relative;
  min-height: 1px;
  padding-left: 0px;
  padding-right: 0px;
}
.col-xs-1, .col-xs-2, .col-xs-3, .col-xs-4, .col-xs-5, .col-xs-6, .col-xs-7, .col-xs-8, .col-xs-9, .col-xs-10, .col-xs-11, .col-xs-12 {
  float: left;
}
.col-xs-12 {
  width: 100%;
}
.col-xs-11 {
  width: 91.66666667%;
}
.col-xs-10 {
  width: 83.33333333%;
}
.col-xs-9 {
  width: 75%;
}
.col-xs-8 {
  width: 66.66666667%;
}
.col-xs-7 {
  width: 58.33333333%;
}
.col-xs-6 {
  width: 50%;
}
.col-xs-5 {
  width: 41.66666667%;
}
.col-xs-4 {
  width: 33.33333333%;
}
.col-xs-3 {
  width: 25%;
}
.col-xs-2 {
  width: 16.66666667%;
}
.col-xs-1 {
  width: 8.33333333%;
}
.col-xs-pull-12 {
  right: 100%;
}
.col-xs-pull-11 {
  right: 91.66666667%;
}
.col-xs-pull-10 {
  right: 83.33333333%;
}
.col-xs-pull-9 {
  right: 75%;
}
.col-xs-pull-8 {
  right: 66.66666667%;
}
.col-xs-pull-7 {
  right: 58.33333333%;
}
.col-xs-pull-6 {
  right: 50%;
}
.col-xs-pull-5 {
  right: 41.66666667%;
}
.col-xs-pull-4 {
  right: 33.33333333%;
}
.col-xs-pull-3 {
  right: 25%;
}
.col-xs-pull-2 {
  right: 16.66666667%;
}
.col-xs-pull-1 {
  right: 8.33333333%;
}
.col-xs-pull-0 {
  right: auto;
}
.col-xs-push-12 {
  left: 100%;
}
.col-xs-push-11 {
  left: 91.66666667%;
}
.col-xs-push-10 {
  left: 83.33333333%;
}
.col-xs-push-9 {
  left: 75%;
}
.col-xs-push-8 {
  left: 66.66666667%;
}
.col-xs-push-7 {
  left: 58.33333333%;
}
.col-xs-push-6 {
  left: 50%;
}
.col-xs-push-5 {
  left: 41.66666667%;
}
.col-xs-push-4 {
  left: 33.33333333%;
}
.col-xs-push-3 {
  left: 25%;
}
.col-xs-push-2 {
  left: 16.66666667%;
}
.col-xs-push-1 {
  left: 8.33333333%;
}
.col-xs-push-0 {
  left: auto;
}
.col-xs-offset-12 {
  margin-left: 100%;
}
.col-xs-offset-11 {
  margin-left: 91.66666667%;
}
.col-xs-offset-10 {
  margin-left: 83.33333333%;
}
.col-xs-offset-9 {
  margin-left: 75%;
}
.col-xs-offset-8 {
  margin-left: 66.66666667%;
}
.col-xs-offset-7 {
  margin-left: 58.33333333%;
}
.col-xs-offset-6 {
  margin-left: 50%;
}
.col-xs-offset-5 {
  margin-left: 41.66666667%;
}
.col-xs-offset-4 {
  margin-left: 33.33333333%;
}
.col-xs-offset-3 {
  margin-left: 25%;
}
.col-xs-offset-2 {
  margin-left: 16.66666667%;
}
.col-xs-offset-1 {
  margin-left: 8.33333333%;
}
.col-xs-offset-0 {
  margin-left: 0%;
}
@media (min-width: 768px) {
  .col-sm-1, .col-sm-2, .col-sm-3, .col-sm-4, .col-sm-5, .col-sm-6, .col-sm-7, .col-sm-8, .col-sm-9, .col-sm-10, .col-sm-11, .col-sm-12 {
    float: left;
  }
  .col-sm-12 {
    width: 100%;
  }
  .col-sm-11 {
    width: 91.66666667%;
  }
  .col-sm-10 {
    width: 83.33333333%;
  }
  .col-sm-9 {
    width: 75%;
  }
  .col-sm-8 {
    width: 66.66666667%;
  }
  .col-sm-7 {
    width: 58.33333333%;
  }
  .col-sm-6 {
    width: 50%;
  }
  .col-sm-5 {
    width: 41.66666667%;
  }
  .col-sm-4 {
    width: 33.33333333%;
  }
  .col-sm-3 {
    width: 25%;
  }
  .col-sm-2 {
    width: 16.66666667%;
  }
  .col-sm-1 {
    width: 8.33333333%;
  }
  .col-sm-pull-12 {
    right: 100%;
  }
  .col-sm-pull-11 {
    right: 91.66666667%;
  }
  .col-sm-pull-10 {
    right: 83.33333333%;
  }
  .col-sm-pull-9 {
    right: 75%;
  }
  .col-sm-pull-8 {
    right: 66.66666667%;
  }
  .col-sm-pull-7 {
    right: 58.33333333%;
  }
  .col-sm-pull-6 {
    right: 50%;
  }
  .col-sm-pull-5 {
    right: 41.66666667%;
  }
  .col-sm-pull-4 {
    right: 33.33333333%;
  }
  .col-sm-pull-3 {
    right: 25%;
  }
  .col-sm-pull-2 {
    right: 16.66666667%;
  }
  .col-sm-pull-1 {
    right: 8.33333333%;
  }
  .col-sm-pull-0 {
    right: auto;
  }
  .col-sm-push-12 {
    left: 100%;
  }
  .col-sm-push-11 {
    left: 91.66666667%;
  }
  .col-sm-push-10 {
    left: 83.33333333%;
  }
  .col-sm-push-9 {
    left: 75%;
  }
  .col-sm-push-8 {
    left: 66.66666667%;
  }
  .col-sm-push-7 {
    left: 58.33333333%;
  }
  .col-sm-push-6 {
    left: 50%;
  }
  .col-sm-push-5 {
    left: 41.66666667%;
  }
  .col-sm-push-4 {
    left: 33.33333333%;
  }
  .col-sm-push-3 {
    left: 25%;
  }
  .col-sm-push-2 {
    left: 16.66666667%;
  }
  .col-sm-push-1 {
    left: 8.33333333%;
  }
  .col-sm-push-0 {
    left: auto;
  }
  .col-sm-offset-12 {
    margin-left: 100%;
  }
  .col-sm-offset-11 {
    margin-left: 91.66666667%;
  }
  .col-sm-offset-10 {
    margin-left: 83.33333333%;
  }
  .col-sm-offset-9 {
    margin-left: 75%;
  }
  .col-sm-offset-8 {
    margin-left: 66.66666667%;
  }
  .col-sm-offset-7 {
    margin-left: 58.33333333%;
  }
  .col-sm-offset-6 {
    margin-left: 50%;
  }
  .col-sm-offset-5 {
    margin-left: 41.66666667%;
  }
  .col-sm-offset-4 {
    margin-left: 33.33333333%;
  }
  .col-sm-offset-3 {
    margin-left: 25%;
  }
  .col-sm-offset-2 {
    margin-left: 16.66666667%;
  }
  .col-sm-offset-1 {
    margin-left: 8.33333333%;
  }
  .col-sm-offset-0 {
    margin-left: 0%;
  }
}
@media (min-width: 992px) {
  .col-md-1, .col-md-2, .col-md-3, .col-md-4, .col-md-5, .col-md-6, .col-md-7, .col-md-8, .col-md-9, .col-md-10, .col-md-11, .col-md-12 {
    float: left;
  }
  .col-md-12 {
    width: 100%;
  }
  .col-md-11 {
    width: 91.66666667%;
  }
  .col-md-10 {
    width: 83.33333333%;
  }
  .col-md-9 {
    width: 75%;
  }
  .col-md-8 {
    width: 66.66666667%;
  }
  .col-md-7 {
    width: 58.33333333%;
  }
  .col-md-6 {
    width: 50%;
  }
  .col-md-5 {
    width: 41.66666667%;
  }
  .col-md-4 {
    width: 33.33333333%;
  }
  .col-md-3 {
    width: 25%;
  }
  .col-md-2 {
    width: 16.66666667%;
  }
  .col-md-1 {
    width: 8.33333333%;
  }
  .col-md-pull-12 {
    right: 100%;
  }
  .col-md-pull-11 {
    right: 91.66666667%;
  }
  .col-md-pull-10 {
    right: 83.33333333%;
  }
  .col-md-pull-9 {
    right: 75%;
  }
  .col-md-pull-8 {
    right: 66.66666667%;
  }
  .col-md-pull-7 {
    right: 58.33333333%;
  }
  .col-md-pull-6 {
    right: 50%;
  }
  .col-md-pull-5 {
    right: 41.66666667%;
  }
  .col-md-pull-4 {
    right: 33.33333333%;
  }
  .col-md-pull-3 {
    right: 25%;
  }
  .col-md-pull-2 {
    right: 16.66666667%;
  }
  .col-md-pull-1 {
    right: 8.33333333%;
  }
  .col-md-pull-0 {
    right: auto;
  }
  .col-md-push-12 {
    left: 100%;
  }
  .col-md-push-11 {
    left: 91.66666667%;
  }
  .col-md-push-10 {
    left: 83.33333333%;
  }
  .col-md-push-9 {
    left: 75%;
  }
  .col-md-push-8 {
    left: 66.66666667%;
  }
  .col-md-push-7 {
    left: 58.33333333%;
  }
  .col-md-push-6 {
    left: 50%;
  }
  .col-md-push-5 {
    left: 41.66666667%;
  }
  .col-md-push-4 {
    left: 33.33333333%;
  }
  .col-md-push-3 {
    left: 25%;
  }
  .col-md-push-2 {
    left: 16.66666667%;
  }
  .col-md-push-1 {
    left: 8.33333333%;
  }
  .col-md-push-0 {
    left: auto;
  }
  .col-md-offset-12 {
    margin-left: 100%;
  }
  .col-md-offset-11 {
    margin-left: 91.66666667%;
  }
  .col-md-offset-10 {
    margin-left: 83.33333333%;
  }
  .col-md-offset-9 {
    margin-left: 75%;
  }
  .col-md-offset-8 {
    margin-left: 66.66666667%;
  }
  .col-md-offset-7 {
    margin-left: 58.33333333%;
  }
  .col-md-offset-6 {
    margin-left: 50%;
  }
  .col-md-offset-5 {
    margin-left: 41.66666667%;
  }
  .col-md-offset-4 {
    margin-left: 33.33333333%;
  }
  .col-md-offset-3 {
    margin-left: 25%;
  }
  .col-md-offset-2 {
    margin-left: 16.66666667%;
  }
  .col-md-offset-1 {
    margin-left: 8.33333333%;
  }
  .col-md-offset-0 {
    margin-left: 0%;
  }
}
@media (min-width: 1200px) {
  .col-lg-1, .col-lg-2, .col-lg-3, .col-lg-4, .col-lg-5, .col-lg-6, .col-lg-7, .col-lg-8, .col-lg-9, .col-lg-10, .col-lg-11, .col-lg-12 {
    float: left;
  }
  .col-lg-12 {
    width: 100%;
  }
  .col-lg-11 {
    width: 91.66666667%;
  }
  .col-lg-10 {
    width: 83.33333333%;
  }
  .col-lg-9 {
    width: 75%;
  }
  .col-lg-8 {
    width: 66.66666667%;
  }
  .col-lg-7 {
    width: 58.33333333%;
  }
  .col-lg-6 {
    width: 50%;
  }
  .col-lg-5 {
    width: 41.66666667%;
  }
  .col-lg-4 {
    width: 33.33333333%;
  }
  .col-lg-3 {
    width: 25%;
  }
  .col-lg-2 {
    width: 16.66666667%;
  }
  .col-lg-1 {
    width: 8.33333333%;
  }
  .col-lg-pull-12 {
    right: 100%;
  }
  .col-lg-pull-11 {
    right: 91.66666667%;
  }
  .col-lg-pull-10 {
    right: 83.33333333%;
  }
  .col-lg-pull-9 {
    right: 75%;
  }
  .col-lg-pull-8 {
    right: 66.66666667%;
  }
  .col-lg-pull-7 {
    right: 58.33333333%;
  }
  .col-lg-pull-6 {
    right: 50%;
  }
  .col-lg-pull-5 {
    right: 41.66666667%;
  }
  .col-lg-pull-4 {
    right: 33.33333333%;
  }
  .col-lg-pull-3 {
    right: 25%;
  }
  .col-lg-pull-2 {
    right: 16.66666667%;
  }
  .col-lg-pull-1 {
    right: 8.33333333%;
  }
  .col-lg-pull-0 {
    right: auto;
  }
  .col-lg-push-12 {
    left: 100%;
  }
  .col-lg-push-11 {
    left: 91.66666667%;
  }
  .col-lg-push-10 {
    left: 83.33333333%;
  }
  .col-lg-push-9 {
    left: 75%;
  }
  .col-lg-push-8 {
    left: 66.66666667%;
  }
  .col-lg-push-7 {
    left: 58.33333333%;
  }
  .col-lg-push-6 {
    left: 50%;
  }
  .col-lg-push-5 {
    left: 41.66666667%;
  }
  .col-lg-push-4 {
    left: 33.33333333%;
  }
  .col-lg-push-3 {
    left: 25%;
  }
  .col-lg-push-2 {
    left: 16.66666667%;
  }
  .col-lg-push-1 {
    left: 8.33333333%;
  }
  .col-lg-push-0 {
    left: auto;
  }
  .col-lg-offset-12 {
    margin-left: 100%;
  }
  .col-lg-offset-11 {
    margin-left: 91.66666667%;
  }
  .col-lg-offset-10 {
    margin-left: 83.33333333%;
  }
  .col-lg-offset-9 {
    margin-left: 75%;
  }
  .col-lg-offset-8 {
    margin-left: 66.66666667%;
  }
  .col-lg-offset-7 {
    margin-left: 58.33333333%;
  }
  .col-lg-offset-6 {
    margin-left: 50%;
  }
  .col-lg-offset-5 {
    margin-left: 41.66666667%;
  }
  .col-lg-offset-4 {
    margin-left: 33.33333333%;
  }
  .col-lg-offset-3 {
    margin-left: 25%;
  }
  .col-lg-offset-2 {
    margin-left: 16.66666667%;
  }
  .col-lg-offset-1 {
    margin-left: 8.33333333%;
  }
  .col-lg-offset-0 {
    margin-left: 0%;
  }
}
table {
  background-color: transparent;
}
caption {
  padding-top: 8px;
  padding-bottom: 8px;
  color: #777777;
  text-align: left;
}
th {
  text-align: left;
}
.table {
  width: 100%;
  max-width: 100%;
  margin-bottom: 18px;
}
.table > thead > tr > th,
.table > tbody > tr > th,
.table > tfoot > tr > th,
.table > thead > tr > td,
.table > tbody > tr > td,
.table > tfoot > tr > td {
  padding: 8px;
  line-height: 1.42857143;
  vertical-align: top;
  border-top: 1px solid #ddd;
}
.table > thead > tr > th {
  vertical-align: bottom;
  border-bottom: 2px solid #ddd;
}
.table > caption + thead > tr:first-child > th,
.table > colgroup + thead > tr:first-child > th,
.table > thead:first-child > tr:first-child > th,
.table > caption + thead > tr:first-child > td,
.table > colgroup + thead > tr:first-child > td,
.table > thead:first-child > tr:first-child > td {
  border-top: 0;
}
.table > tbody + tbody {
  border-top: 2px solid #ddd;
}
.table .table {
  background-color: #fff;
}
.table-condensed > thead > tr > th,
.table-condensed > tbody > tr > th,
.table-condensed > tfoot > tr > th,
.table-condensed > thead > tr > td,
.table-condensed > tbody > tr > td,
.table-condensed > tfoot > tr > td {
  padding: 5px;
}
.table-bordered {
  border: 1px solid #ddd;
}
.table-bordered > thead > tr > th,
.table-bordered > tbody > tr > th,
.table-bordered > tfoot > tr > th,
.table-bordered > thead > tr > td,
.table-bordered > tbody > tr > td,
.table-bordered > tfoot > tr > td {
  border: 1px solid #ddd;
}
.table-bordered > thead > tr > th,
.table-bordered > thead > tr > td {
  border-bottom-width: 2px;
}
.table-striped > tbody > tr:nth-of-type(odd) {
  background-color: #f9f9f9;
}
.table-hover > tbody > tr:hover {
  background-color: #f5f5f5;
}
table col[class*="col-"] {
  position: static;
  float: none;
  display: table-column;
}
table td[class*="col-"],
table th[class*="col-"] {
  position: static;
  float: none;
  display: table-cell;
}
.table > thead > tr > td.active,
.table > tbody > tr > td.active,
.table > tfoot > tr > td.active,
.table > thead > tr > th.active,
.table > tbody > tr > th.active,
.table > tfoot > tr > th.active,
.table > thead > tr.active > td,
.table > tbody > tr.active > td,
.table > tfoot > tr.active > td,
.table > thead > tr.active > th,
.table > tbody > tr.active > th,
.table > tfoot > tr.active > th {
  background-color: #f5f5f5;
}
.table-hover > tbody > tr > td.active:hover,
.table-hover > tbody > tr > th.active:hover,
.table-hover > tbody > tr.active:hover > td,
.table-hover > tbody > tr:hover > .active,
.table-hover > tbody > tr.active:hover > th {
  background-color: #e8e8e8;
}
.table > thead > tr > td.success,
.table > tbody > tr > td.success,
.table > tfoot > tr > td.success,
.table > thead > tr > th.success,
.table > tbody > tr > th.success,
.table > tfoot > tr > th.success,
.table > thead > tr.success > td,
.table > tbody > tr.success > td,
.table > tfoot > tr.success > td,
.table > thead > tr.success > th,
.table > tbody > tr.success > th,
.table > tfoot > tr.success > th {
  background-color: #dff0d8;
}
.table-hover > tbody > tr > td.success:hover,
.table-hover > tbody > tr > th.success:hover,
.table-hover > tbody > tr.success:hover > td,
.table-hover > tbody > tr:hover > .success,
.table-hover > tbody > tr.success:hover > th {
  background-color: #d0e9c6;
}
.table > thead > tr > td.info,
.table > tbody > tr > td.info,
.table > tfoot > tr > td.info,
.table > thead > tr > th.info,
.table > tbody > tr > th.info,
.table > tfoot > tr > th.info,
.table > thead > tr.info > td,
.table > tbody > tr.info > td,
.table > tfoot > tr.info > td,
.table > thead > tr.info > th,
.table > tbody > tr.info > th,
.table > tfoot > tr.info > th {
  background-color: #d9edf7;
}
.table-hover > tbody > tr > td.info:hover,
.table-hover > tbody > tr > th.info:hover,
.table-hover > tbody > tr.info:hover > td,
.table-hover > tbody > tr:hover > .info,
.table-hover > tbody > tr.info:hover > th {
  background-color: #c4e3f3;
}
.table > thead > tr > td.warning,
.table > tbody > tr > td.warning,
.table > tfoot > tr > td.warning,
.table > thead > tr > th.warning,
.table > tbody > tr > th.warning,
.table > tfoot > tr > th.warning,
.table > thead > tr.warning > td,
.table > tbody > tr.warning > td,
.table > tfoot > tr.warning > td,
.table > thead > tr.warning > th,
.table > tbody > tr.warning > th,
.table > tfoot > tr.warning > th {
  background-color: #fcf8e3;
}
.table-hover > tbody > tr > td.warning:hover,
.table-hover > tbody > tr > th.warning:hover,
.table-hover > tbody > tr.warning:hover > td,
.table-hover > tbody > tr:hover > .warning,
.table-hover > tbody > tr.warning:hover > th {
  background-color: #faf2cc;
}
.table > thead > tr > td.danger,
.table > tbody > tr > td.danger,
.table > tfoot > tr > td.danger,
.table > thead > tr > th.danger,
.table > tbody > tr > th.danger,
.table > tfoot > tr > th.danger,
.table > thead > tr.danger > td,
.table > tbody > tr.danger > td,
.table > tfoot > tr.danger > td,
.table > thead > tr.danger > th,
.table > tbody > tr.danger > th,
.table > tfoot > tr.danger > th {
  background-color: #f2dede;
}
.table-hover > tbody > tr > td.danger:hover,
.table-hover > tbody > tr > th.danger:hover,
.table-hover > tbody > tr.danger:hover > td,
.table-hover > tbody > tr:hover > .danger,
.table-hover > tbody > tr.danger:hover > th {
  background-color: #ebcccc;
}
.table-responsive {
  overflow-x: auto;
  min-height: 0.01%;
}
@media screen and (max-width: 767px) {
  .table-responsive {
    width: 100%;
    margin-bottom: 13.5px;
    overflow-y: hidden;
    -ms-overflow-style: -ms-autohiding-scrollbar;
    border: 1px solid #ddd;
  }
  .table-responsive > .table {
    margin-bottom: 0;
  }
  .table-responsive > .table > thead > tr > th,
  .table-responsive > .table > tbody > tr > th,
  .table-responsive > .table > tfoot > tr > th,
  .table-responsive > .table > thead > tr > td,
  .table-responsive > .table > tbody > tr > td,
  .table-responsive > .table > tfoot > tr > td {
    white-space: nowrap;
  }
  .table-responsive > .table-bordered {
    border: 0;
  }
  .table-responsive > .table-bordered > thead > tr > th:first-child,
  .table-responsive > .table-bordered > tbody > tr > th:first-child,
  .table-responsive > .table-bordered > tfoot > tr > th:first-child,
  .table-responsive > .table-bordered > thead > tr > td:first-child,
  .table-responsive > .table-bordered > tbody > tr > td:first-child,
  .table-responsive > .table-bordered > tfoot > tr > td:first-child {
    border-left: 0;
  }
  .table-responsive > .table-bordered > thead > tr > th:last-child,
  .table-responsive > .table-bordered > tbody > tr > th:last-child,
  .table-responsive > .table-bordered > tfoot > tr > th:last-child,
  .table-responsive > .table-bordered > thead > tr > td:last-child,
  .table-responsive > .table-bordered > tbody > tr > td:last-child,
  .table-responsive > .table-bordered > tfoot > tr > td:last-child {
    border-right: 0;
  }
  .table-responsive > .table-bordered > tbody > tr:last-child > th,
  .table-responsive > .table-bordered > tfoot > tr:last-child > th,
  .table-responsive > .table-bordered > tbody > tr:last-child > td,
  .table-responsive > .table-bordered > tfoot > tr:last-child > td {
    border-bottom: 0;
  }
}
fieldset {
  padding: 0;
  margin: 0;
  border: 0;
  min-width: 0;
}
legend {
  display: block;
  width: 100%;
  padding: 0;
  margin-bottom: 18px;
  font-size: 19.5px;
  line-height: inherit;
  color: #333333;
  border: 0;
  border-bottom: 1px solid #e5e5e5;
}
label {
  display: inline-block;
  max-width: 100%;
  margin-bottom: 5px;
  font-weight: bold;
}
input[type="search"] {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}
input[type="radio"],
input[type="checkbox"] {
  margin: 4px 0 0;
  margin-top: 1px \9;
  line-height: normal;
}
input[type="file"] {
  display: block;
}
input[type="range"] {
  display: block;
  width: 100%;
}
select[multiple],
select[size] {
  height: auto;
}
input[type="file"]:focus,
input[type="radio"]:focus,
input[type="checkbox"]:focus {
  outline: 5px auto -webkit-focus-ring-color;
  outline-offset: -2px;
}
output {
  display: block;
  padding-top: 7px;
  font-size: 13px;
  line-height: 1.42857143;
  color: #555555;
}
.form-control {
  display: block;
  width: 100%;
  height: 32px;
  padding: 6px 12px;
  font-size: 13px;
  line-height: 1.42857143;
  color: #555555;
  background-color: #fff;
  background-image: none;
  border: 1px solid #ccc;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  -webkit-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  -o-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
}
.form-control:focus {
  border-color: #66afe9;
  outline: 0;
  -webkit-box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
  box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
}
.form-control::-moz-placeholder {
  color: #999;
  opacity: 1;
}
.form-control:-ms-input-placeholder {
  color: #999;
}
.form-control::-webkit-input-placeholder {
  color: #999;
}
.form-control::-ms-expand {
  border: 0;
  background-color: transparent;
}
.form-control[disabled],
.form-control[readonly],
fieldset[disabled] .form-control {
  background-color: #eeeeee;
  opacity: 1;
}
.form-control[disabled],
fieldset[disabled] .form-control {
  cursor: not-allowed;
}
textarea.form-control {
  height: auto;
}
input[type="search"] {
  -webkit-appearance: none;
}
@media screen and (-webkit-min-device-pixel-ratio: 0) {
  input[type="date"].form-control,
  input[type="time"].form-control,
  input[type="datetime-local"].form-control,
  input[type="month"].form-control {
    line-height: 32px;
  }
  input[type="date"].input-sm,
  input[type="time"].input-sm,
  input[type="datetime-local"].input-sm,
  input[type="month"].input-sm,
  .input-group-sm input[type="date"],
  .input-group-sm input[type="time"],
  .input-group-sm input[type="datetime-local"],
  .input-group-sm input[type="month"] {
    line-height: 30px;
  }
  input[type="date"].input-lg,
  input[type="time"].input-lg,
  input[type="datetime-local"].input-lg,
  input[type="month"].input-lg,
  .input-group-lg input[type="date"],
  .input-group-lg input[type="time"],
  .input-group-lg input[type="datetime-local"],
  .input-group-lg input[type="month"] {
    line-height: 45px;
  }
}
.form-group {
  margin-bottom: 15px;
}
.radio,
.checkbox {
  position: relative;
  display: block;
  margin-top: 10px;
  margin-bottom: 10px;
}
.radio label,
.checkbox label {
  min-height: 18px;
  padding-left: 20px;
  margin-bottom: 0;
  font-weight: normal;
  cursor: pointer;
}
.radio input[type="radio"],
.radio-inline input[type="radio"],
.checkbox input[type="checkbox"],
.checkbox-inline input[type="checkbox"] {
  position: absolute;
  margin-left: -20px;
  margin-top: 4px \9;
}
.radio + .radio,
.checkbox + .checkbox {
  margin-top: -5px;
}
.radio-inline,
.checkbox-inline {
  position: relative;
  display: inline-block;
  padding-left: 20px;
  margin-bottom: 0;
  vertical-align: middle;
  font-weight: normal;
  cursor: pointer;
}
.radio-inline + .radio-inline,
.checkbox-inline + .checkbox-inline {
  margin-top: 0;
  margin-left: 10px;
}
input[type="radio"][disabled],
input[type="checkbox"][disabled],
input[type="radio"].disabled,
input[type="checkbox"].disabled,
fieldset[disabled] input[type="radio"],
fieldset[disabled] input[type="checkbox"] {
  cursor: not-allowed;
}
.radio-inline.disabled,
.checkbox-inline.disabled,
fieldset[disabled] .radio-inline,
fieldset[disabled] .checkbox-inline {
  cursor: not-allowed;
}
.radio.disabled label,
.checkbox.disabled label,
fieldset[disabled] .radio label,
fieldset[disabled] .checkbox label {
  cursor: not-allowed;
}
.form-control-static {
  padding-top: 7px;
  padding-bottom: 7px;
  margin-bottom: 0;
  min-height: 31px;
}
.form-control-static.input-lg,
.form-control-static.input-sm {
  padding-left: 0;
  padding-right: 0;
}
.input-sm {
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
select.input-sm {
  height: 30px;
  line-height: 30px;
}
textarea.input-sm,
select[multiple].input-sm {
  height: auto;
}
.form-group-sm .form-control {
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
.form-group-sm select.form-control {
  height: 30px;
  line-height: 30px;
}
.form-group-sm textarea.form-control,
.form-group-sm select[multiple].form-control {
  height: auto;
}
.form-group-sm .form-control-static {
  height: 30px;
  min-height: 30px;
  padding: 6px 10px;
  font-size: 12px;
  line-height: 1.5;
}
.input-lg {
  height: 45px;
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
select.input-lg {
  height: 45px;
  line-height: 45px;
}
textarea.input-lg,
select[multiple].input-lg {
  height: auto;
}
.form-group-lg .form-control {
  height: 45px;
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
.form-group-lg select.form-control {
  height: 45px;
  line-height: 45px;
}
.form-group-lg textarea.form-control,
.form-group-lg select[multiple].form-control {
  height: auto;
}
.form-group-lg .form-control-static {
  height: 45px;
  min-height: 35px;
  padding: 11px 16px;
  font-size: 17px;
  line-height: 1.3333333;
}
.has-feedback {
  position: relative;
}
.has-feedback .form-control {
  padding-right: 40px;
}
.form-control-feedback {
  position: absolute;
  top: 0;
  right: 0;
  z-index: 2;
  display: block;
  width: 32px;
  height: 32px;
  line-height: 32px;
  text-align: center;
  pointer-events: none;
}
.input-lg + .form-control-feedback,
.input-group-lg + .form-control-feedback,
.form-group-lg .form-control + .form-control-feedback {
  width: 45px;
  height: 45px;
  line-height: 45px;
}
.input-sm + .form-control-feedback,
.input-group-sm + .form-control-feedback,
.form-group-sm .form-control + .form-control-feedback {
  width: 30px;
  height: 30px;
  line-height: 30px;
}
.has-success .help-block,
.has-success .control-label,
.has-success .radio,
.has-success .checkbox,
.has-success .radio-inline,
.has-success .checkbox-inline,
.has-success.radio label,
.has-success.checkbox label,
.has-success.radio-inline label,
.has-success.checkbox-inline label {
  color: #3c763d;
}
.has-success .form-control {
  border-color: #3c763d;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
}
.has-success .form-control:focus {
  border-color: #2b542c;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #67b168;
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #67b168;
}
.has-success .input-group-addon {
  color: #3c763d;
  border-color: #3c763d;
  background-color: #dff0d8;
}
.has-success .form-control-feedback {
  color: #3c763d;
}
.has-warning .help-block,
.has-warning .control-label,
.has-warning .radio,
.has-warning .checkbox,
.has-warning .radio-inline,
.has-warning .checkbox-inline,
.has-warning.radio label,
.has-warning.checkbox label,
.has-warning.radio-inline label,
.has-warning.checkbox-inline label {
  color: #8a6d3b;
}
.has-warning .form-control {
  border-color: #8a6d3b;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
}
.has-warning .form-control:focus {
  border-color: #66512c;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #c0a16b;
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #c0a16b;
}
.has-warning .input-group-addon {
  color: #8a6d3b;
  border-color: #8a6d3b;
  background-color: #fcf8e3;
}
.has-warning .form-control-feedback {
  color: #8a6d3b;
}
.has-error .help-block,
.has-error .control-label,
.has-error .radio,
.has-error .checkbox,
.has-error .radio-inline,
.has-error .checkbox-inline,
.has-error.radio label,
.has-error.checkbox label,
.has-error.radio-inline label,
.has-error.checkbox-inline label {
  color: #a94442;
}
.has-error .form-control {
  border-color: #a94442;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
}
.has-error .form-control:focus {
  border-color: #843534;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #ce8483;
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #ce8483;
}
.has-error .input-group-addon {
  color: #a94442;
  border-color: #a94442;
  background-color: #f2dede;
}
.has-error .form-control-feedback {
  color: #a94442;
}
.has-feedback label ~ .form-control-feedback {
  top: 23px;
}
.has-feedback label.sr-only ~ .form-control-feedback {
  top: 0;
}
.help-block {
  display: block;
  margin-top: 5px;
  margin-bottom: 10px;
  color: #404040;
}
@media (min-width: 768px) {
  .form-inline .form-group {
    display: inline-block;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .form-inline .form-control {
    display: inline-block;
    width: auto;
    vertical-align: middle;
  }
  .form-inline .form-control-static {
    display: inline-block;
  }
  .form-inline .input-group {
    display: inline-table;
    vertical-align: middle;
  }
  .form-inline .input-group .input-group-addon,
  .form-inline .input-group .input-group-btn,
  .form-inline .input-group .form-control {
    width: auto;
  }
  .form-inline .input-group > .form-control {
    width: 100%;
  }
  .form-inline .control-label {
    margin-bottom: 0;
    vertical-align: middle;
  }
  .form-inline .radio,
  .form-inline .checkbox {
    display: inline-block;
    margin-top: 0;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .form-inline .radio label,
  .form-inline .checkbox label {
    padding-left: 0;
  }
  .form-inline .radio input[type="radio"],
  .form-inline .checkbox input[type="checkbox"] {
    position: relative;
    margin-left: 0;
  }
  .form-inline .has-feedback .form-control-feedback {
    top: 0;
  }
}
.form-horizontal .radio,
.form-horizontal .checkbox,
.form-horizontal .radio-inline,
.form-horizontal .checkbox-inline {
  margin-top: 0;
  margin-bottom: 0;
  padding-top: 7px;
}
.form-horizontal .radio,
.form-horizontal .checkbox {
  min-height: 25px;
}
.form-horizontal .form-group {
  margin-left: 0px;
  margin-right: 0px;
}
@media (min-width: 768px) {
  .form-horizontal .control-label {
    text-align: right;
    margin-bottom: 0;
    padding-top: 7px;
  }
}
.form-horizontal .has-feedback .form-control-feedback {
  right: 0px;
}
@media (min-width: 768px) {
  .form-horizontal .form-group-lg .control-label {
    padding-top: 11px;
    font-size: 17px;
  }
}
@media (min-width: 768px) {
  .form-horizontal .form-group-sm .control-label {
    padding-top: 6px;
    font-size: 12px;
  }
}
.btn {
  display: inline-block;
  margin-bottom: 0;
  font-weight: normal;
  text-align: center;
  vertical-align: middle;
  touch-action: manipulation;
  cursor: pointer;
  background-image: none;
  border: 1px solid transparent;
  white-space: nowrap;
  padding: 6px 12px;
  font-size: 13px;
  line-height: 1.42857143;
  border-radius: 2px;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}
.btn:focus,
.btn:active:focus,
.btn.active:focus,
.btn.focus,
.btn:active.focus,
.btn.active.focus {
  outline: 5px auto -webkit-focus-ring-color;
  outline-offset: -2px;
}
.btn:hover,
.btn:focus,
.btn.focus {
  color: #333;
  text-decoration: none;
}
.btn:active,
.btn.active {
  outline: 0;
  background-image: none;
  -webkit-box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
  box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
}
.btn.disabled,
.btn[disabled],
fieldset[disabled] .btn {
  cursor: not-allowed;
  opacity: 0.65;
  filter: alpha(opacity=65);
  -webkit-box-shadow: none;
  box-shadow: none;
}
a.btn.disabled,
fieldset[disabled] a.btn {
  pointer-events: none;
}
.btn-default {
  color: #333;
  background-color: #fff;
  border-color: #ccc;
}
.btn-default:focus,
.btn-default.focus {
  color: #333;
  background-color: #e6e6e6;
  border-color: #8c8c8c;
}
.btn-default:hover {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.btn-default:active,
.btn-default.active,
.open > .dropdown-toggle.btn-default {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.btn-default:active:hover,
.btn-default.active:hover,
.open > .dropdown-toggle.btn-default:hover,
.btn-default:active:focus,
.btn-default.active:focus,
.open > .dropdown-toggle.btn-default:focus,
.btn-default:active.focus,
.btn-default.active.focus,
.open > .dropdown-toggle.btn-default.focus {
  color: #333;
  background-color: #d4d4d4;
  border-color: #8c8c8c;
}
.btn-default:active,
.btn-default.active,
.open > .dropdown-toggle.btn-default {
  background-image: none;
}
.btn-default.disabled:hover,
.btn-default[disabled]:hover,
fieldset[disabled] .btn-default:hover,
.btn-default.disabled:focus,
.btn-default[disabled]:focus,
fieldset[disabled] .btn-default:focus,
.btn-default.disabled.focus,
.btn-default[disabled].focus,
fieldset[disabled] .btn-default.focus {
  background-color: #fff;
  border-color: #ccc;
}
.btn-default .badge {
  color: #fff;
  background-color: #333;
}
.btn-primary {
  color: #fff;
  background-color: #337ab7;
  border-color: #2e6da4;
}
.btn-primary:focus,
.btn-primary.focus {
  color: #fff;
  background-color: #286090;
  border-color: #122b40;
}
.btn-primary:hover {
  color: #fff;
  background-color: #286090;
  border-color: #204d74;
}
.btn-primary:active,
.btn-primary.active,
.open > .dropdown-toggle.btn-primary {
  color: #fff;
  background-color: #286090;
  border-color: #204d74;
}
.btn-primary:active:hover,
.btn-primary.active:hover,
.open > .dropdown-toggle.btn-primary:hover,
.btn-primary:active:focus,
.btn-primary.active:focus,
.open > .dropdown-toggle.btn-primary:focus,
.btn-primary:active.focus,
.btn-primary.active.focus,
.open > .dropdown-toggle.btn-primary.focus {
  color: #fff;
  background-color: #204d74;
  border-color: #122b40;
}
.btn-primary:active,
.btn-primary.active,
.open > .dropdown-toggle.btn-primary {
  background-image: none;
}
.btn-primary.disabled:hover,
.btn-primary[disabled]:hover,
fieldset[disabled] .btn-primary:hover,
.btn-primary.disabled:focus,
.btn-primary[disabled]:focus,
fieldset[disabled] .btn-primary:focus,
.btn-primary.disabled.focus,
.btn-primary[disabled].focus,
fieldset[disabled] .btn-primary.focus {
  background-color: #337ab7;
  border-color: #2e6da4;
}
.btn-primary .badge {
  color: #337ab7;
  background-color: #fff;
}
.btn-success {
  color: #fff;
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.btn-success:focus,
.btn-success.focus {
  color: #fff;
  background-color: #449d44;
  border-color: #255625;
}
.btn-success:hover {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.btn-success:active,
.btn-success.active,
.open > .dropdown-toggle.btn-success {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.btn-success:active:hover,
.btn-success.active:hover,
.open > .dropdown-toggle.btn-success:hover,
.btn-success:active:focus,
.btn-success.active:focus,
.open > .dropdown-toggle.btn-success:focus,
.btn-success:active.focus,
.btn-success.active.focus,
.open > .dropdown-toggle.btn-success.focus {
  color: #fff;
  background-color: #398439;
  border-color: #255625;
}
.btn-success:active,
.btn-success.active,
.open > .dropdown-toggle.btn-success {
  background-image: none;
}
.btn-success.disabled:hover,
.btn-success[disabled]:hover,
fieldset[disabled] .btn-success:hover,
.btn-success.disabled:focus,
.btn-success[disabled]:focus,
fieldset[disabled] .btn-success:focus,
.btn-success.disabled.focus,
.btn-success[disabled].focus,
fieldset[disabled] .btn-success.focus {
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.btn-success .badge {
  color: #5cb85c;
  background-color: #fff;
}
.btn-info {
  color: #fff;
  background-color: #5bc0de;
  border-color: #46b8da;
}
.btn-info:focus,
.btn-info.focus {
  color: #fff;
  background-color: #31b0d5;
  border-color: #1b6d85;
}
.btn-info:hover {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.btn-info:active,
.btn-info.active,
.open > .dropdown-toggle.btn-info {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.btn-info:active:hover,
.btn-info.active:hover,
.open > .dropdown-toggle.btn-info:hover,
.btn-info:active:focus,
.btn-info.active:focus,
.open > .dropdown-toggle.btn-info:focus,
.btn-info:active.focus,
.btn-info.active.focus,
.open > .dropdown-toggle.btn-info.focus {
  color: #fff;
  background-color: #269abc;
  border-color: #1b6d85;
}
.btn-info:active,
.btn-info.active,
.open > .dropdown-toggle.btn-info {
  background-image: none;
}
.btn-info.disabled:hover,
.btn-info[disabled]:hover,
fieldset[disabled] .btn-info:hover,
.btn-info.disabled:focus,
.btn-info[disabled]:focus,
fieldset[disabled] .btn-info:focus,
.btn-info.disabled.focus,
.btn-info[disabled].focus,
fieldset[disabled] .btn-info.focus {
  background-color: #5bc0de;
  border-color: #46b8da;
}
.btn-info .badge {
  color: #5bc0de;
  background-color: #fff;
}
.btn-warning {
  color: #fff;
  background-color: #f0ad4e;
  border-color: #eea236;
}
.btn-warning:focus,
.btn-warning.focus {
  color: #fff;
  background-color: #ec971f;
  border-color: #985f0d;
}
.btn-warning:hover {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.btn-warning:active,
.btn-warning.active,
.open > .dropdown-toggle.btn-warning {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.btn-warning:active:hover,
.btn-warning.active:hover,
.open > .dropdown-toggle.btn-warning:hover,
.btn-warning:active:focus,
.btn-warning.active:focus,
.open > .dropdown-toggle.btn-warning:focus,
.btn-warning:active.focus,
.btn-warning.active.focus,
.open > .dropdown-toggle.btn-warning.focus {
  color: #fff;
  background-color: #d58512;
  border-color: #985f0d;
}
.btn-warning:active,
.btn-warning.active,
.open > .dropdown-toggle.btn-warning {
  background-image: none;
}
.btn-warning.disabled:hover,
.btn-warning[disabled]:hover,
fieldset[disabled] .btn-warning:hover,
.btn-warning.disabled:focus,
.btn-warning[disabled]:focus,
fieldset[disabled] .btn-warning:focus,
.btn-warning.disabled.focus,
.btn-warning[disabled].focus,
fieldset[disabled] .btn-warning.focus {
  background-color: #f0ad4e;
  border-color: #eea236;
}
.btn-warning .badge {
  color: #f0ad4e;
  background-color: #fff;
}
.btn-danger {
  color: #fff;
  background-color: #d9534f;
  border-color: #d43f3a;
}
.btn-danger:focus,
.btn-danger.focus {
  color: #fff;
  background-color: #c9302c;
  border-color: #761c19;
}
.btn-danger:hover {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.btn-danger:active,
.btn-danger.active,
.open > .dropdown-toggle.btn-danger {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.btn-danger:active:hover,
.btn-danger.active:hover,
.open > .dropdown-toggle.btn-danger:hover,
.btn-danger:active:focus,
.btn-danger.active:focus,
.open > .dropdown-toggle.btn-danger:focus,
.btn-danger:active.focus,
.btn-danger.active.focus,
.open > .dropdown-toggle.btn-danger.focus {
  color: #fff;
  background-color: #ac2925;
  border-color: #761c19;
}
.btn-danger:active,
.btn-danger.active,
.open > .dropdown-toggle.btn-danger {
  background-image: none;
}
.btn-danger.disabled:hover,
.btn-danger[disabled]:hover,
fieldset[disabled] .btn-danger:hover,
.btn-danger.disabled:focus,
.btn-danger[disabled]:focus,
fieldset[disabled] .btn-danger:focus,
.btn-danger.disabled.focus,
.btn-danger[disabled].focus,
fieldset[disabled] .btn-danger.focus {
  background-color: #d9534f;
  border-color: #d43f3a;
}
.btn-danger .badge {
  color: #d9534f;
  background-color: #fff;
}
.btn-link {
  color: #337ab7;
  font-weight: normal;
  border-radius: 0;
}
.btn-link,
.btn-link:active,
.btn-link.active,
.btn-link[disabled],
fieldset[disabled] .btn-link {
  background-color: transparent;
  -webkit-box-shadow: none;
  box-shadow: none;
}
.btn-link,
.btn-link:hover,
.btn-link:focus,
.btn-link:active {
  border-color: transparent;
}
.btn-link:hover,
.btn-link:focus {
  color: #23527c;
  text-decoration: underline;
  background-color: transparent;
}
.btn-link[disabled]:hover,
fieldset[disabled] .btn-link:hover,
.btn-link[disabled]:focus,
fieldset[disabled] .btn-link:focus {
  color: #777777;
  text-decoration: none;
}
.btn-lg,
.btn-group-lg > .btn {
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
.btn-sm,
.btn-group-sm > .btn {
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
.btn-xs,
.btn-group-xs > .btn {
  padding: 1px 5px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
.btn-block {
  display: block;
  width: 100%;
}
.btn-block + .btn-block {
  margin-top: 5px;
}
input[type="submit"].btn-block,
input[type="reset"].btn-block,
input[type="button"].btn-block {
  width: 100%;
}
.fade {
  opacity: 0;
  -webkit-transition: opacity 0.15s linear;
  -o-transition: opacity 0.15s linear;
  transition: opacity 0.15s linear;
}
.fade.in {
  opacity: 1;
}
.collapse {
  display: none;
}
.collapse.in {
  display: block;
}
tr.collapse.in {
  display: table-row;
}
tbody.collapse.in {
  display: table-row-group;
}
.collapsing {
  position: relative;
  height: 0;
  overflow: hidden;
  -webkit-transition-property: height, visibility;
  transition-property: height, visibility;
  -webkit-transition-duration: 0.35s;
  transition-duration: 0.35s;
  -webkit-transition-timing-function: ease;
  transition-timing-function: ease;
}
.caret {
  display: inline-block;
  width: 0;
  height: 0;
  margin-left: 2px;
  vertical-align: middle;
  border-top: 4px dashed;
  border-top: 4px solid \9;
  border-right: 4px solid transparent;
  border-left: 4px solid transparent;
}
.dropup,
.dropdown {
  position: relative;
}
.dropdown-toggle:focus {
  outline: 0;
}
.dropdown-menu {
  position: absolute;
  top: 100%;
  left: 0;
  z-index: 1000;
  display: none;
  float: left;
  min-width: 160px;
  padding: 5px 0;
  margin: 2px 0 0;
  list-style: none;
  font-size: 13px;
  text-align: left;
  background-color: #fff;
  border: 1px solid #ccc;
  border: 1px solid rgba(0, 0, 0, 0.15);
  border-radius: 2px;
  -webkit-box-shadow: 0 6px 12px rgba(0, 0, 0, 0.175);
  box-shadow: 0 6px 12px rgba(0, 0, 0, 0.175);
  background-clip: padding-box;
}
.dropdown-menu.pull-right {
  right: 0;
  left: auto;
}
.dropdown-menu .divider {
  height: 1px;
  margin: 8px 0;
  overflow: hidden;
  background-color: #e5e5e5;
}
.dropdown-menu > li > a {
  display: block;
  padding: 3px 20px;
  clear: both;
  font-weight: normal;
  line-height: 1.42857143;
  color: #333333;
  white-space: nowrap;
}
.dropdown-menu > li > a:hover,
.dropdown-menu > li > a:focus {
  text-decoration: none;
  color: #262626;
  background-color: #f5f5f5;
}
.dropdown-menu > .active > a,
.dropdown-menu > .active > a:hover,
.dropdown-menu > .active > a:focus {
  color: #fff;
  text-decoration: none;
  outline: 0;
  background-color: #337ab7;
}
.dropdown-menu > .disabled > a,
.dropdown-menu > .disabled > a:hover,
.dropdown-menu > .disabled > a:focus {
  color: #777777;
}
.dropdown-menu > .disabled > a:hover,
.dropdown-menu > .disabled > a:focus {
  text-decoration: none;
  background-color: transparent;
  background-image: none;
  filter: progid:DXImageTransform.Microsoft.gradient(enabled = false);
  cursor: not-allowed;
}
.open > .dropdown-menu {
  display: block;
}
.open > a {
  outline: 0;
}
.dropdown-menu-right {
  left: auto;
  right: 0;
}
.dropdown-menu-left {
  left: 0;
  right: auto;
}
.dropdown-header {
  display: block;
  padding: 3px 20px;
  font-size: 12px;
  line-height: 1.42857143;
  color: #777777;
  white-space: nowrap;
}
.dropdown-backdrop {
  position: fixed;
  left: 0;
  right: 0;
  bottom: 0;
  top: 0;
  z-index: 990;
}
.pull-right > .dropdown-menu {
  right: 0;
  left: auto;
}
.dropup .caret,
.navbar-fixed-bottom .dropdown .caret {
  border-top: 0;
  border-bottom: 4px dashed;
  border-bottom: 4px solid \9;
  content: "";
}
.dropup .dropdown-menu,
.navbar-fixed-bottom .dropdown .dropdown-menu {
  top: auto;
  bottom: 100%;
  margin-bottom: 2px;
}
@media (min-width: 541px) {
  .navbar-right .dropdown-menu {
    left: auto;
    right: 0;
  }
  .navbar-right .dropdown-menu-left {
    left: 0;
    right: auto;
  }
}
.btn-group,
.btn-group-vertical {
  position: relative;
  display: inline-block;
  vertical-align: middle;
}
.btn-group > .btn,
.btn-group-vertical > .btn {
  position: relative;
  float: left;
}
.btn-group > .btn:hover,
.btn-group-vertical > .btn:hover,
.btn-group > .btn:focus,
.btn-group-vertical > .btn:focus,
.btn-group > .btn:active,
.btn-group-vertical > .btn:active,
.btn-group > .btn.active,
.btn-group-vertical > .btn.active {
  z-index: 2;
}
.btn-group .btn + .btn,
.btn-group .btn + .btn-group,
.btn-group .btn-group + .btn,
.btn-group .btn-group + .btn-group {
  margin-left: -1px;
}
.btn-toolbar {
  margin-left: -5px;
}
.btn-toolbar .btn,
.btn-toolbar .btn-group,
.btn-toolbar .input-group {
  float: left;
}
.btn-toolbar > .btn,
.btn-toolbar > .btn-group,
.btn-toolbar > .input-group {
  margin-left: 5px;
}
.btn-group > .btn:not(:first-child):not(:last-child):not(.dropdown-toggle) {
  border-radius: 0;
}
.btn-group > .btn:first-child {
  margin-left: 0;
}
.btn-group > .btn:first-child:not(:last-child):not(.dropdown-toggle) {
  border-bottom-right-radius: 0;
  border-top-right-radius: 0;
}
.btn-group > .btn:last-child:not(:first-child),
.btn-group > .dropdown-toggle:not(:first-child) {
  border-bottom-left-radius: 0;
  border-top-left-radius: 0;
}
.btn-group > .btn-group {
  float: left;
}
.btn-group > .btn-group:not(:first-child):not(:last-child) > .btn {
  border-radius: 0;
}
.btn-group > .btn-group:first-child:not(:last-child) > .btn:last-child,
.btn-group > .btn-group:first-child:not(:last-child) > .dropdown-toggle {
  border-bottom-right-radius: 0;
  border-top-right-radius: 0;
}
.btn-group > .btn-group:last-child:not(:first-child) > .btn:first-child {
  border-bottom-left-radius: 0;
  border-top-left-radius: 0;
}
.btn-group .dropdown-toggle:active,
.btn-group.open .dropdown-toggle {
  outline: 0;
}
.btn-group > .btn + .dropdown-toggle {
  padding-left: 8px;
  padding-right: 8px;
}
.btn-group > .btn-lg + .dropdown-toggle {
  padding-left: 12px;
  padding-right: 12px;
}
.btn-group.open .dropdown-toggle {
  -webkit-box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
  box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
}
.btn-group.open .dropdown-toggle.btn-link {
  -webkit-box-shadow: none;
  box-shadow: none;
}
.btn .caret {
  margin-left: 0;
}
.btn-lg .caret {
  border-width: 5px 5px 0;
  border-bottom-width: 0;
}
.dropup .btn-lg .caret {
  border-width: 0 5px 5px;
}
.btn-group-vertical > .btn,
.btn-group-vertical > .btn-group,
.btn-group-vertical > .btn-group > .btn {
  display: block;
  float: none;
  width: 100%;
  max-width: 100%;
}
.btn-group-vertical > .btn-group > .btn {
  float: none;
}
.btn-group-vertical > .btn + .btn,
.btn-group-vertical > .btn + .btn-group,
.btn-group-vertical > .btn-group + .btn,
.btn-group-vertical > .btn-group + .btn-group {
  margin-top: -1px;
  margin-left: 0;
}
.btn-group-vertical > .btn:not(:first-child):not(:last-child) {
  border-radius: 0;
}
.btn-group-vertical > .btn:first-child:not(:last-child) {
  border-top-right-radius: 2px;
  border-top-left-radius: 2px;
  border-bottom-right-radius: 0;
  border-bottom-left-radius: 0;
}
.btn-group-vertical > .btn:last-child:not(:first-child) {
  border-top-right-radius: 0;
  border-top-left-radius: 0;
  border-bottom-right-radius: 2px;
  border-bottom-left-radius: 2px;
}
.btn-group-vertical > .btn-group:not(:first-child):not(:last-child) > .btn {
  border-radius: 0;
}
.btn-group-vertical > .btn-group:first-child:not(:last-child) > .btn:last-child,
.btn-group-vertical > .btn-group:first-child:not(:last-child) > .dropdown-toggle {
  border-bottom-right-radius: 0;
  border-bottom-left-radius: 0;
}
.btn-group-vertical > .btn-group:last-child:not(:first-child) > .btn:first-child {
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.btn-group-justified {
  display: table;
  width: 100%;
  table-layout: fixed;
  border-collapse: separate;
}
.btn-group-justified > .btn,
.btn-group-justified > .btn-group {
  float: none;
  display: table-cell;
  width: 1%;
}
.btn-group-justified > .btn-group .btn {
  width: 100%;
}
.btn-group-justified > .btn-group .dropdown-menu {
  left: auto;
}
[data-toggle="buttons"] > .btn input[type="radio"],
[data-toggle="buttons"] > .btn-group > .btn input[type="radio"],
[data-toggle="buttons"] > .btn input[type="checkbox"],
[data-toggle="buttons"] > .btn-group > .btn input[type="checkbox"] {
  position: absolute;
  clip: rect(0, 0, 0, 0);
  pointer-events: none;
}
.input-group {
  position: relative;
  display: table;
  border-collapse: separate;
}
.input-group[class*="col-"] {
  float: none;
  padding-left: 0;
  padding-right: 0;
}
.input-group .form-control {
  position: relative;
  z-index: 2;
  float: left;
  width: 100%;
  margin-bottom: 0;
}
.input-group .form-control:focus {
  z-index: 3;
}
.input-group-lg > .form-control,
.input-group-lg > .input-group-addon,
.input-group-lg > .input-group-btn > .btn {
  height: 45px;
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
select.input-group-lg > .form-control,
select.input-group-lg > .input-group-addon,
select.input-group-lg > .input-group-btn > .btn {
  height: 45px;
  line-height: 45px;
}
textarea.input-group-lg > .form-control,
textarea.input-group-lg > .input-group-addon,
textarea.input-group-lg > .input-group-btn > .btn,
select[multiple].input-group-lg > .form-control,
select[multiple].input-group-lg > .input-group-addon,
select[multiple].input-group-lg > .input-group-btn > .btn {
  height: auto;
}
.input-group-sm > .form-control,
.input-group-sm > .input-group-addon,
.input-group-sm > .input-group-btn > .btn {
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
select.input-group-sm > .form-control,
select.input-group-sm > .input-group-addon,
select.input-group-sm > .input-group-btn > .btn {
  height: 30px;
  line-height: 30px;
}
textarea.input-group-sm > .form-control,
textarea.input-group-sm > .input-group-addon,
textarea.input-group-sm > .input-group-btn > .btn,
select[multiple].input-group-sm > .form-control,
select[multiple].input-group-sm > .input-group-addon,
select[multiple].input-group-sm > .input-group-btn > .btn {
  height: auto;
}
.input-group-addon,
.input-group-btn,
.input-group .form-control {
  display: table-cell;
}
.input-group-addon:not(:first-child):not(:last-child),
.input-group-btn:not(:first-child):not(:last-child),
.input-group .form-control:not(:first-child):not(:last-child) {
  border-radius: 0;
}
.input-group-addon,
.input-group-btn {
  width: 1%;
  white-space: nowrap;
  vertical-align: middle;
}
.input-group-addon {
  padding: 6px 12px;
  font-size: 13px;
  font-weight: normal;
  line-height: 1;
  color: #555555;
  text-align: center;
  background-color: #eeeeee;
  border: 1px solid #ccc;
  border-radius: 2px;
}
.input-group-addon.input-sm {
  padding: 5px 10px;
  font-size: 12px;
  border-radius: 1px;
}
.input-group-addon.input-lg {
  padding: 10px 16px;
  font-size: 17px;
  border-radius: 3px;
}
.input-group-addon input[type="radio"],
.input-group-addon input[type="checkbox"] {
  margin-top: 0;
}
.input-group .form-control:first-child,
.input-group-addon:first-child,
.input-group-btn:first-child > .btn,
.input-group-btn:first-child > .btn-group > .btn,
.input-group-btn:first-child > .dropdown-toggle,
.input-group-btn:last-child > .btn:not(:last-child):not(.dropdown-toggle),
.input-group-btn:last-child > .btn-group:not(:last-child) > .btn {
  border-bottom-right-radius: 0;
  border-top-right-radius: 0;
}
.input-group-addon:first-child {
  border-right: 0;
}
.input-group .form-control:last-child,
.input-group-addon:last-child,
.input-group-btn:last-child > .btn,
.input-group-btn:last-child > .btn-group > .btn,
.input-group-btn:last-child > .dropdown-toggle,
.input-group-btn:first-child > .btn:not(:first-child),
.input-group-btn:first-child > .btn-group:not(:first-child) > .btn {
  border-bottom-left-radius: 0;
  border-top-left-radius: 0;
}
.input-group-addon:last-child {
  border-left: 0;
}
.input-group-btn {
  position: relative;
  font-size: 0;
  white-space: nowrap;
}
.input-group-btn > .btn {
  position: relative;
}
.input-group-btn > .btn + .btn {
  margin-left: -1px;
}
.input-group-btn > .btn:hover,
.input-group-btn > .btn:focus,
.input-group-btn > .btn:active {
  z-index: 2;
}
.input-group-btn:first-child > .btn,
.input-group-btn:first-child > .btn-group {
  margin-right: -1px;
}
.input-group-btn:last-child > .btn,
.input-group-btn:last-child > .btn-group {
  z-index: 2;
  margin-left: -1px;
}
.nav {
  margin-bottom: 0;
  padding-left: 0;
  list-style: none;
}
.nav > li {
  position: relative;
  display: block;
}
.nav > li > a {
  position: relative;
  display: block;
  padding: 10px 15px;
}
.nav > li > a:hover,
.nav > li > a:focus {
  text-decoration: none;
  background-color: #eeeeee;
}
.nav > li.disabled > a {
  color: #777777;
}
.nav > li.disabled > a:hover,
.nav > li.disabled > a:focus {
  color: #777777;
  text-decoration: none;
  background-color: transparent;
  cursor: not-allowed;
}
.nav .open > a,
.nav .open > a:hover,
.nav .open > a:focus {
  background-color: #eeeeee;
  border-color: #337ab7;
}
.nav .nav-divider {
  height: 1px;
  margin: 8px 0;
  overflow: hidden;
  background-color: #e5e5e5;
}
.nav > li > a > img {
  max-width: none;
}
.nav-tabs {
  border-bottom: 1px solid #ddd;
}
.nav-tabs > li {
  float: left;
  margin-bottom: -1px;
}
.nav-tabs > li > a {
  margin-right: 2px;
  line-height: 1.42857143;
  border: 1px solid transparent;
  border-radius: 2px 2px 0 0;
}
.nav-tabs > li > a:hover {
  border-color: #eeeeee #eeeeee #ddd;
}
.nav-tabs > li.active > a,
.nav-tabs > li.active > a:hover,
.nav-tabs > li.active > a:focus {
  color: #555555;
  background-color: #fff;
  border: 1px solid #ddd;
  border-bottom-color: transparent;
  cursor: default;
}
.nav-tabs.nav-justified {
  width: 100%;
  border-bottom: 0;
}
.nav-tabs.nav-justified > li {
  float: none;
}
.nav-tabs.nav-justified > li > a {
  text-align: center;
  margin-bottom: 5px;
}
.nav-tabs.nav-justified > .dropdown .dropdown-menu {
  top: auto;
  left: auto;
}
@media (min-width: 768px) {
  .nav-tabs.nav-justified > li {
    display: table-cell;
    width: 1%;
  }
  .nav-tabs.nav-justified > li > a {
    margin-bottom: 0;
  }
}
.nav-tabs.nav-justified > li > a {
  margin-right: 0;
  border-radius: 2px;
}
.nav-tabs.nav-justified > .active > a,
.nav-tabs.nav-justified > .active > a:hover,
.nav-tabs.nav-justified > .active > a:focus {
  border: 1px solid #ddd;
}
@media (min-width: 768px) {
  .nav-tabs.nav-justified > li > a {
    border-bottom: 1px solid #ddd;
    border-radius: 2px 2px 0 0;
  }
  .nav-tabs.nav-justified > .active > a,
  .nav-tabs.nav-justified > .active > a:hover,
  .nav-tabs.nav-justified > .active > a:focus {
    border-bottom-color: #fff;
  }
}
.nav-pills > li {
  float: left;
}
.nav-pills > li > a {
  border-radius: 2px;
}
.nav-pills > li + li {
  margin-left: 2px;
}
.nav-pills > li.active > a,
.nav-pills > li.active > a:hover,
.nav-pills > li.active > a:focus {
  color: #fff;
  background-color: #337ab7;
}
.nav-stacked > li {
  float: none;
}
.nav-stacked > li + li {
  margin-top: 2px;
  margin-left: 0;
}
.nav-justified {
  width: 100%;
}
.nav-justified > li {
  float: none;
}
.nav-justified > li > a {
  text-align: center;
  margin-bottom: 5px;
}
.nav-justified > .dropdown .dropdown-menu {
  top: auto;
  left: auto;
}
@media (min-width: 768px) {
  .nav-justified > li {
    display: table-cell;
    width: 1%;
  }
  .nav-justified > li > a {
    margin-bottom: 0;
  }
}
.nav-tabs-justified {
  border-bottom: 0;
}
.nav-tabs-justified > li > a {
  margin-right: 0;
  border-radius: 2px;
}
.nav-tabs-justified > .active > a,
.nav-tabs-justified > .active > a:hover,
.nav-tabs-justified > .active > a:focus {
  border: 1px solid #ddd;
}
@media (min-width: 768px) {
  .nav-tabs-justified > li > a {
    border-bottom: 1px solid #ddd;
    border-radius: 2px 2px 0 0;
  }
  .nav-tabs-justified > .active > a,
  .nav-tabs-justified > .active > a:hover,
  .nav-tabs-justified > .active > a:focus {
    border-bottom-color: #fff;
  }
}
.tab-content > .tab-pane {
  display: none;
}
.tab-content > .active {
  display: block;
}
.nav-tabs .dropdown-menu {
  margin-top: -1px;
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.navbar {
  position: relative;
  min-height: 30px;
  margin-bottom: 18px;
  border: 1px solid transparent;
}
@media (min-width: 541px) {
  .navbar {
    border-radius: 2px;
  }
}
@media (min-width: 541px) {
  .navbar-header {
    float: left;
  }
}
.navbar-collapse {
  overflow-x: visible;
  padding-right: 0px;
  padding-left: 0px;
  border-top: 1px solid transparent;
  box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.1);
  -webkit-overflow-scrolling: touch;
}
.navbar-collapse.in {
  overflow-y: auto;
}
@media (min-width: 541px) {
  .navbar-collapse {
    width: auto;
    border-top: 0;
    box-shadow: none;
  }
  .navbar-collapse.collapse {
    display: block !important;
    height: auto !important;
    padding-bottom: 0;
    overflow: visible !important;
  }
  .navbar-collapse.in {
    overflow-y: visible;
  }
  .navbar-fixed-top .navbar-collapse,
  .navbar-static-top .navbar-collapse,
  .navbar-fixed-bottom .navbar-collapse {
    padding-left: 0;
    padding-right: 0;
  }
}
.navbar-fixed-top .navbar-collapse,
.navbar-fixed-bottom .navbar-collapse {
  max-height: 340px;
}
@media (max-device-width: 540px) and (orientation: landscape) {
  .navbar-fixed-top .navbar-collapse,
  .navbar-fixed-bottom .navbar-collapse {
    max-height: 200px;
  }
}
.container > .navbar-header,
.container-fluid > .navbar-header,
.container > .navbar-collapse,
.container-fluid > .navbar-collapse {
  margin-right: 0px;
  margin-left: 0px;
}
@media (min-width: 541px) {
  .container > .navbar-header,
  .container-fluid > .navbar-header,
  .container > .navbar-collapse,
  .container-fluid > .navbar-collapse {
    margin-right: 0;
    margin-left: 0;
  }
}
.navbar-static-top {
  z-index: 1000;
  border-width: 0 0 1px;
}
@media (min-width: 541px) {
  .navbar-static-top {
    border-radius: 0;
  }
}
.navbar-fixed-top,
.navbar-fixed-bottom {
  position: fixed;
  right: 0;
  left: 0;
  z-index: 1030;
}
@media (min-width: 541px) {
  .navbar-fixed-top,
  .navbar-fixed-bottom {
    border-radius: 0;
  }
}
.navbar-fixed-top {
  top: 0;
  border-width: 0 0 1px;
}
.navbar-fixed-bottom {
  bottom: 0;
  margin-bottom: 0;
  border-width: 1px 0 0;
}
.navbar-brand {
  float: left;
  padding: 6px 0px;
  font-size: 17px;
  line-height: 18px;
  height: 30px;
}
.navbar-brand:hover,
.navbar-brand:focus {
  text-decoration: none;
}
.navbar-brand > img {
  display: block;
}
@media (min-width: 541px) {
  .navbar > .container .navbar-brand,
  .navbar > .container-fluid .navbar-brand {
    margin-left: 0px;
  }
}
.navbar-toggle {
  position: relative;
  float: right;
  margin-right: 0px;
  padding: 9px 10px;
  margin-top: -2px;
  margin-bottom: -2px;
  background-color: transparent;
  background-image: none;
  border: 1px solid transparent;
  border-radius: 2px;
}
.navbar-toggle:focus {
  outline: 0;
}
.navbar-toggle .icon-bar {
  display: block;
  width: 22px;
  height: 2px;
  border-radius: 1px;
}
.navbar-toggle .icon-bar + .icon-bar {
  margin-top: 4px;
}
@media (min-width: 541px) {
  .navbar-toggle {
    display: none;
  }
}
.navbar-nav {
  margin: 3px 0px;
}
.navbar-nav > li > a {
  padding-top: 10px;
  padding-bottom: 10px;
  line-height: 18px;
}
@media (max-width: 540px) {
  .navbar-nav .open .dropdown-menu {
    position: static;
    float: none;
    width: auto;
    margin-top: 0;
    background-color: transparent;
    border: 0;
    box-shadow: none;
  }
  .navbar-nav .open .dropdown-menu > li > a,
  .navbar-nav .open .dropdown-menu .dropdown-header {
    padding: 5px 15px 5px 25px;
  }
  .navbar-nav .open .dropdown-menu > li > a {
    line-height: 18px;
  }
  .navbar-nav .open .dropdown-menu > li > a:hover,
  .navbar-nav .open .dropdown-menu > li > a:focus {
    background-image: none;
  }
}
@media (min-width: 541px) {
  .navbar-nav {
    float: left;
    margin: 0;
  }
  .navbar-nav > li {
    float: left;
  }
  .navbar-nav > li > a {
    padding-top: 6px;
    padding-bottom: 6px;
  }
}
.navbar-form {
  margin-left: 0px;
  margin-right: 0px;
  padding: 10px 0px;
  border-top: 1px solid transparent;
  border-bottom: 1px solid transparent;
  -webkit-box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.1), 0 1px 0 rgba(255, 255, 255, 0.1);
  box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.1), 0 1px 0 rgba(255, 255, 255, 0.1);
  margin-top: -1px;
  margin-bottom: -1px;
}
@media (min-width: 768px) {
  .navbar-form .form-group {
    display: inline-block;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .navbar-form .form-control {
    display: inline-block;
    width: auto;
    vertical-align: middle;
  }
  .navbar-form .form-control-static {
    display: inline-block;
  }
  .navbar-form .input-group {
    display: inline-table;
    vertical-align: middle;
  }
  .navbar-form .input-group .input-group-addon,
  .navbar-form .input-group .input-group-btn,
  .navbar-form .input-group .form-control {
    width: auto;
  }
  .navbar-form .input-group > .form-control {
    width: 100%;
  }
  .navbar-form .control-label {
    margin-bottom: 0;
    vertical-align: middle;
  }
  .navbar-form .radio,
  .navbar-form .checkbox {
    display: inline-block;
    margin-top: 0;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .navbar-form .radio label,
  .navbar-form .checkbox label {
    padding-left: 0;
  }
  .navbar-form .radio input[type="radio"],
  .navbar-form .checkbox input[type="checkbox"] {
    position: relative;
    margin-left: 0;
  }
  .navbar-form .has-feedback .form-control-feedback {
    top: 0;
  }
}
@media (max-width: 540px) {
  .navbar-form .form-group {
    margin-bottom: 5px;
  }
  .navbar-form .form-group:last-child {
    margin-bottom: 0;
  }
}
@media (min-width: 541px) {
  .navbar-form {
    width: auto;
    border: 0;
    margin-left: 0;
    margin-right: 0;
    padding-top: 0;
    padding-bottom: 0;
    -webkit-box-shadow: none;
    box-shadow: none;
  }
}
.navbar-nav > li > .dropdown-menu {
  margin-top: 0;
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.navbar-fixed-bottom .navbar-nav > li > .dropdown-menu {
  margin-bottom: 0;
  border-top-right-radius: 2px;
  border-top-left-radius: 2px;
  border-bottom-right-radius: 0;
  border-bottom-left-radius: 0;
}
.navbar-btn {
  margin-top: -1px;
  margin-bottom: -1px;
}
.navbar-btn.btn-sm {
  margin-top: 0px;
  margin-bottom: 0px;
}
.navbar-btn.btn-xs {
  margin-top: 4px;
  margin-bottom: 4px;
}
.navbar-text {
  margin-top: 6px;
  margin-bottom: 6px;
}
@media (min-width: 541px) {
  .navbar-text {
    float: left;
    margin-left: 0px;
    margin-right: 0px;
  }
}
@media (min-width: 541px) {
  .navbar-left {
    float: left !important;
    float: left;
  }
  .navbar-right {
    float: right !important;
    float: right;
    margin-right: 0px;
  }
  .navbar-right ~ .navbar-right {
    margin-right: 0;
  }
}
.navbar-default {
  background-color: #f8f8f8;
  border-color: #e7e7e7;
}
.navbar-default .navbar-brand {
  color: #777;
}
.navbar-default .navbar-brand:hover,
.navbar-default .navbar-brand:focus {
  color: #5e5e5e;
  background-color: transparent;
}
.navbar-default .navbar-text {
  color: #777;
}
.navbar-default .navbar-nav > li > a {
  color: #777;
}
.navbar-default .navbar-nav > li > a:hover,
.navbar-default .navbar-nav > li > a:focus {
  color: #333;
  background-color: transparent;
}
.navbar-default .navbar-nav > .active > a,
.navbar-default .navbar-nav > .active > a:hover,
.navbar-default .navbar-nav > .active > a:focus {
  color: #555;
  background-color: #e7e7e7;
}
.navbar-default .navbar-nav > .disabled > a,
.navbar-default .navbar-nav > .disabled > a:hover,
.navbar-default .navbar-nav > .disabled > a:focus {
  color: #ccc;
  background-color: transparent;
}
.navbar-default .navbar-toggle {
  border-color: #ddd;
}
.navbar-default .navbar-toggle:hover,
.navbar-default .navbar-toggle:focus {
  background-color: #ddd;
}
.navbar-default .navbar-toggle .icon-bar {
  background-color: #888;
}
.navbar-default .navbar-collapse,
.navbar-default .navbar-form {
  border-color: #e7e7e7;
}
.navbar-default .navbar-nav > .open > a,
.navbar-default .navbar-nav > .open > a:hover,
.navbar-default .navbar-nav > .open > a:focus {
  background-color: #e7e7e7;
  color: #555;
}
@media (max-width: 540px) {
  .navbar-default .navbar-nav .open .dropdown-menu > li > a {
    color: #777;
  }
  .navbar-default .navbar-nav .open .dropdown-menu > li > a:hover,
  .navbar-default .navbar-nav .open .dropdown-menu > li > a:focus {
    color: #333;
    background-color: transparent;
  }
  .navbar-default .navbar-nav .open .dropdown-menu > .active > a,
  .navbar-default .navbar-nav .open .dropdown-menu > .active > a:hover,
  .navbar-default .navbar-nav .open .dropdown-menu > .active > a:focus {
    color: #555;
    background-color: #e7e7e7;
  }
  .navbar-default .navbar-nav .open .dropdown-menu > .disabled > a,
  .navbar-default .navbar-nav .open .dropdown-menu > .disabled > a:hover,
  .navbar-default .navbar-nav .open .dropdown-menu > .disabled > a:focus {
    color: #ccc;
    background-color: transparent;
  }
}
.navbar-default .navbar-link {
  color: #777;
}
.navbar-default .navbar-link:hover {
  color: #333;
}
.navbar-default .btn-link {
  color: #777;
}
.navbar-default .btn-link:hover,
.navbar-default .btn-link:focus {
  color: #333;
}
.navbar-default .btn-link[disabled]:hover,
fieldset[disabled] .navbar-default .btn-link:hover,
.navbar-default .btn-link[disabled]:focus,
fieldset[disabled] .navbar-default .btn-link:focus {
  color: #ccc;
}
.navbar-inverse {
  background-color: #222;
  border-color: #080808;
}
.navbar-inverse .navbar-brand {
  color: #9d9d9d;
}
.navbar-inverse .navbar-brand:hover,
.navbar-inverse .navbar-brand:focus {
  color: #fff;
  background-color: transparent;
}
.navbar-inverse .navbar-text {
  color: #9d9d9d;
}
.navbar-inverse .navbar-nav > li > a {
  color: #9d9d9d;
}
.navbar-inverse .navbar-nav > li > a:hover,
.navbar-inverse .navbar-nav > li > a:focus {
  color: #fff;
  background-color: transparent;
}
.navbar-inverse .navbar-nav > .active > a,
.navbar-inverse .navbar-nav > .active > a:hover,
.navbar-inverse .navbar-nav > .active > a:focus {
  color: #fff;
  background-color: #080808;
}
.navbar-inverse .navbar-nav > .disabled > a,
.navbar-inverse .navbar-nav > .disabled > a:hover,
.navbar-inverse .navbar-nav > .disabled > a:focus {
  color: #444;
  background-color: transparent;
}
.navbar-inverse .navbar-toggle {
  border-color: #333;
}
.navbar-inverse .navbar-toggle:hover,
.navbar-inverse .navbar-toggle:focus {
  background-color: #333;
}
.navbar-inverse .navbar-toggle .icon-bar {
  background-color: #fff;
}
.navbar-inverse .navbar-collapse,
.navbar-inverse .navbar-form {
  border-color: #101010;
}
.navbar-inverse .navbar-nav > .open > a,
.navbar-inverse .navbar-nav > .open > a:hover,
.navbar-inverse .navbar-nav > .open > a:focus {
  background-color: #080808;
  color: #fff;
}
@media (max-width: 540px) {
  .navbar-inverse .navbar-nav .open .dropdown-menu > .dropdown-header {
    border-color: #080808;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu .divider {
    background-color: #080808;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > li > a {
    color: #9d9d9d;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > li > a:hover,
  .navbar-inverse .navbar-nav .open .dropdown-menu > li > a:focus {
    color: #fff;
    background-color: transparent;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > .active > a,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .active > a:hover,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .active > a:focus {
    color: #fff;
    background-color: #080808;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > .disabled > a,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .disabled > a:hover,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .disabled > a:focus {
    color: #444;
    background-color: transparent;
  }
}
.navbar-inverse .navbar-link {
  color: #9d9d9d;
}
.navbar-inverse .navbar-link:hover {
  color: #fff;
}
.navbar-inverse .btn-link {
  color: #9d9d9d;
}
.navbar-inverse .btn-link:hover,
.navbar-inverse .btn-link:focus {
  color: #fff;
}
.navbar-inverse .btn-link[disabled]:hover,
fieldset[disabled] .navbar-inverse .btn-link:hover,
.navbar-inverse .btn-link[disabled]:focus,
fieldset[disabled] .navbar-inverse .btn-link:focus {
  color: #444;
}
.breadcrumb {
  padding: 8px 15px;
  margin-bottom: 18px;
  list-style: none;
  background-color: #f5f5f5;
  border-radius: 2px;
}
.breadcrumb > li {
  display: inline-block;
}
.breadcrumb > li + li:before {
  content: "/\00a0";
  padding: 0 5px;
  color: #5e5e5e;
}
.breadcrumb > .active {
  color: #777777;
}
.pagination {
  display: inline-block;
  padding-left: 0;
  margin: 18px 0;
  border-radius: 2px;
}
.pagination > li {
  display: inline;
}
.pagination > li > a,
.pagination > li > span {
  position: relative;
  float: left;
  padding: 6px 12px;
  line-height: 1.42857143;
  text-decoration: none;
  color: #337ab7;
  background-color: #fff;
  border: 1px solid #ddd;
  margin-left: -1px;
}
.pagination > li:first-child > a,
.pagination > li:first-child > span {
  margin-left: 0;
  border-bottom-left-radius: 2px;
  border-top-left-radius: 2px;
}
.pagination > li:last-child > a,
.pagination > li:last-child > span {
  border-bottom-right-radius: 2px;
  border-top-right-radius: 2px;
}
.pagination > li > a:hover,
.pagination > li > span:hover,
.pagination > li > a:focus,
.pagination > li > span:focus {
  z-index: 2;
  color: #23527c;
  background-color: #eeeeee;
  border-color: #ddd;
}
.pagination > .active > a,
.pagination > .active > span,
.pagination > .active > a:hover,
.pagination > .active > span:hover,
.pagination > .active > a:focus,
.pagination > .active > span:focus {
  z-index: 3;
  color: #fff;
  background-color: #337ab7;
  border-color: #337ab7;
  cursor: default;
}
.pagination > .disabled > span,
.pagination > .disabled > span:hover,
.pagination > .disabled > span:focus,
.pagination > .disabled > a,
.pagination > .disabled > a:hover,
.pagination > .disabled > a:focus {
  color: #777777;
  background-color: #fff;
  border-color: #ddd;
  cursor: not-allowed;
}
.pagination-lg > li > a,
.pagination-lg > li > span {
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
}
.pagination-lg > li:first-child > a,
.pagination-lg > li:first-child > span {
  border-bottom-left-radius: 3px;
  border-top-left-radius: 3px;
}
.pagination-lg > li:last-child > a,
.pagination-lg > li:last-child > span {
  border-bottom-right-radius: 3px;
  border-top-right-radius: 3px;
}
.pagination-sm > li > a,
.pagination-sm > li > span {
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
}
.pagination-sm > li:first-child > a,
.pagination-sm > li:first-child > span {
  border-bottom-left-radius: 1px;
  border-top-left-radius: 1px;
}
.pagination-sm > li:last-child > a,
.pagination-sm > li:last-child > span {
  border-bottom-right-radius: 1px;
  border-top-right-radius: 1px;
}
.pager {
  padding-left: 0;
  margin: 18px 0;
  list-style: none;
  text-align: center;
}
.pager li {
  display: inline;
}
.pager li > a,
.pager li > span {
  display: inline-block;
  padding: 5px 14px;
  background-color: #fff;
  border: 1px solid #ddd;
  border-radius: 15px;
}
.pager li > a:hover,
.pager li > a:focus {
  text-decoration: none;
  background-color: #eeeeee;
}
.pager .next > a,
.pager .next > span {
  float: right;
}
.pager .previous > a,
.pager .previous > span {
  float: left;
}
.pager .disabled > a,
.pager .disabled > a:hover,
.pager .disabled > a:focus,
.pager .disabled > span {
  color: #777777;
  background-color: #fff;
  cursor: not-allowed;
}
.label {
  display: inline;
  padding: .2em .6em .3em;
  font-size: 75%;
  font-weight: bold;
  line-height: 1;
  color: #fff;
  text-align: center;
  white-space: nowrap;
  vertical-align: baseline;
  border-radius: .25em;
}
a.label:hover,
a.label:focus {
  color: #fff;
  text-decoration: none;
  cursor: pointer;
}
.label:empty {
  display: none;
}
.btn .label {
  position: relative;
  top: -1px;
}
.label-default {
  background-color: #777777;
}
.label-default[href]:hover,
.label-default[href]:focus {
  background-color: #5e5e5e;
}
.label-primary {
  background-color: #337ab7;
}
.label-primary[href]:hover,
.label-primary[href]:focus {
  background-color: #286090;
}
.label-success {
  background-color: #5cb85c;
}
.label-success[href]:hover,
.label-success[href]:focus {
  background-color: #449d44;
}
.label-info {
  background-color: #5bc0de;
}
.label-info[href]:hover,
.label-info[href]:focus {
  background-color: #31b0d5;
}
.label-warning {
  background-color: #f0ad4e;
}
.label-warning[href]:hover,
.label-warning[href]:focus {
  background-color: #ec971f;
}
.label-danger {
  background-color: #d9534f;
}
.label-danger[href]:hover,
.label-danger[href]:focus {
  background-color: #c9302c;
}
.badge {
  display: inline-block;
  min-width: 10px;
  padding: 3px 7px;
  font-size: 12px;
  font-weight: bold;
  color: #fff;
  line-height: 1;
  vertical-align: middle;
  white-space: nowrap;
  text-align: center;
  background-color: #777777;
  border-radius: 10px;
}
.badge:empty {
  display: none;
}
.btn .badge {
  position: relative;
  top: -1px;
}
.btn-xs .badge,
.btn-group-xs > .btn .badge {
  top: 0;
  padding: 1px 5px;
}
a.badge:hover,
a.badge:focus {
  color: #fff;
  text-decoration: none;
  cursor: pointer;
}
.list-group-item.active > .badge,
.nav-pills > .active > a > .badge {
  color: #337ab7;
  background-color: #fff;
}
.list-group-item > .badge {
  float: right;
}
.list-group-item > .badge + .badge {
  margin-right: 5px;
}
.nav-pills > li > a > .badge {
  margin-left: 3px;
}
.jumbotron {
  padding-top: 30px;
  padding-bottom: 30px;
  margin-bottom: 30px;
  color: inherit;
  background-color: #eeeeee;
}
.jumbotron h1,
.jumbotron .h1 {
  color: inherit;
}
.jumbotron p {
  margin-bottom: 15px;
  font-size: 20px;
  font-weight: 200;
}
.jumbotron > hr {
  border-top-color: #d5d5d5;
}
.container .jumbotron,
.container-fluid .jumbotron {
  border-radius: 3px;
  padding-left: 0px;
  padding-right: 0px;
}
.jumbotron .container {
  max-width: 100%;
}
@media screen and (min-width: 768px) {
  .jumbotron {
    padding-top: 48px;
    padding-bottom: 48px;
  }
  .container .jumbotron,
  .container-fluid .jumbotron {
    padding-left: 60px;
    padding-right: 60px;
  }
  .jumbotron h1,
  .jumbotron .h1 {
    font-size: 59px;
  }
}
.thumbnail {
  display: block;
  padding: 4px;
  margin-bottom: 18px;
  line-height: 1.42857143;
  background-color: #fff;
  border: 1px solid #ddd;
  border-radius: 2px;
  -webkit-transition: border 0.2s ease-in-out;
  -o-transition: border 0.2s ease-in-out;
  transition: border 0.2s ease-in-out;
}
.thumbnail > img,
.thumbnail a > img {
  margin-left: auto;
  margin-right: auto;
}
a.thumbnail:hover,
a.thumbnail:focus,
a.thumbnail.active {
  border-color: #337ab7;
}
.thumbnail .caption {
  padding: 9px;
  color: #000;
}
.alert {
  padding: 15px;
  margin-bottom: 18px;
  border: 1px solid transparent;
  border-radius: 2px;
}
.alert h4 {
  margin-top: 0;
  color: inherit;
}
.alert .alert-link {
  font-weight: bold;
}
.alert > p,
.alert > ul {
  margin-bottom: 0;
}
.alert > p + p {
  margin-top: 5px;
}
.alert-dismissable,
.alert-dismissible {
  padding-right: 35px;
}
.alert-dismissable .close,
.alert-dismissible .close {
  position: relative;
  top: -2px;
  right: -21px;
  color: inherit;
}
.alert-success {
  background-color: #dff0d8;
  border-color: #d6e9c6;
  color: #3c763d;
}
.alert-success hr {
  border-top-color: #c9e2b3;
}
.alert-success .alert-link {
  color: #2b542c;
}
.alert-info {
  background-color: #d9edf7;
  border-color: #bce8f1;
  color: #31708f;
}
.alert-info hr {
  border-top-color: #a6e1ec;
}
.alert-info .alert-link {
  color: #245269;
}
.alert-warning {
  background-color: #fcf8e3;
  border-color: #faebcc;
  color: #8a6d3b;
}
.alert-warning hr {
  border-top-color: #f7e1b5;
}
.alert-warning .alert-link {
  color: #66512c;
}
.alert-danger {
  background-color: #f2dede;
  border-color: #ebccd1;
  color: #a94442;
}
.alert-danger hr {
  border-top-color: #e4b9c0;
}
.alert-danger .alert-link {
  color: #843534;
}
@-webkit-keyframes progress-bar-stripes {
  from {
    background-position: 40px 0;
  }
  to {
    background-position: 0 0;
  }
}
@keyframes progress-bar-stripes {
  from {
    background-position: 40px 0;
  }
  to {
    background-position: 0 0;
  }
}
.progress {
  overflow: hidden;
  height: 18px;
  margin-bottom: 18px;
  background-color: #f5f5f5;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 2px rgba(0, 0, 0, 0.1);
  box-shadow: inset 0 1px 2px rgba(0, 0, 0, 0.1);
}
.progress-bar {
  float: left;
  width: 0%;
  height: 100%;
  font-size: 12px;
  line-height: 18px;
  color: #fff;
  text-align: center;
  background-color: #337ab7;
  -webkit-box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.15);
  box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.15);
  -webkit-transition: width 0.6s ease;
  -o-transition: width 0.6s ease;
  transition: width 0.6s ease;
}
.progress-striped .progress-bar,
.progress-bar-striped {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-size: 40px 40px;
}
.progress.active .progress-bar,
.progress-bar.active {
  -webkit-animation: progress-bar-stripes 2s linear infinite;
  -o-animation: progress-bar-stripes 2s linear infinite;
  animation: progress-bar-stripes 2s linear infinite;
}
.progress-bar-success {
  background-color: #5cb85c;
}
.progress-striped .progress-bar-success {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.progress-bar-info {
  background-color: #5bc0de;
}
.progress-striped .progress-bar-info {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.progress-bar-warning {
  background-color: #f0ad4e;
}
.progress-striped .progress-bar-warning {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.progress-bar-danger {
  background-color: #d9534f;
}
.progress-striped .progress-bar-danger {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.media {
  margin-top: 15px;
}
.media:first-child {
  margin-top: 0;
}
.media,
.media-body {
  zoom: 1;
  overflow: hidden;
}
.media-body {
  width: 10000px;
}
.media-object {
  display: block;
}
.media-object.img-thumbnail {
  max-width: none;
}
.media-right,
.media > .pull-right {
  padding-left: 10px;
}
.media-left,
.media > .pull-left {
  padding-right: 10px;
}
.media-left,
.media-right,
.media-body {
  display: table-cell;
  vertical-align: top;
}
.media-middle {
  vertical-align: middle;
}
.media-bottom {
  vertical-align: bottom;
}
.media-heading {
  margin-top: 0;
  margin-bottom: 5px;
}
.media-list {
  padding-left: 0;
  list-style: none;
}
.list-group {
  margin-bottom: 20px;
  padding-left: 0;
}
.list-group-item {
  position: relative;
  display: block;
  padding: 10px 15px;
  margin-bottom: -1px;
  background-color: #fff;
  border: 1px solid #ddd;
}
.list-group-item:first-child {
  border-top-right-radius: 2px;
  border-top-left-radius: 2px;
}
.list-group-item:last-child {
  margin-bottom: 0;
  border-bottom-right-radius: 2px;
  border-bottom-left-radius: 2px;
}
a.list-group-item,
button.list-group-item {
  color: #555;
}
a.list-group-item .list-group-item-heading,
button.list-group-item .list-group-item-heading {
  color: #333;
}
a.list-group-item:hover,
button.list-group-item:hover,
a.list-group-item:focus,
button.list-group-item:focus {
  text-decoration: none;
  color: #555;
  background-color: #f5f5f5;
}
button.list-group-item {
  width: 100%;
  text-align: left;
}
.list-group-item.disabled,
.list-group-item.disabled:hover,
.list-group-item.disabled:focus {
  background-color: #eeeeee;
  color: #777777;
  cursor: not-allowed;
}
.list-group-item.disabled .list-group-item-heading,
.list-group-item.disabled:hover .list-group-item-heading,
.list-group-item.disabled:focus .list-group-item-heading {
  color: inherit;
}
.list-group-item.disabled .list-group-item-text,
.list-group-item.disabled:hover .list-group-item-text,
.list-group-item.disabled:focus .list-group-item-text {
  color: #777777;
}
.list-group-item.active,
.list-group-item.active:hover,
.list-group-item.active:focus {
  z-index: 2;
  color: #fff;
  background-color: #337ab7;
  border-color: #337ab7;
}
.list-group-item.active .list-group-item-heading,
.list-group-item.active:hover .list-group-item-heading,
.list-group-item.active:focus .list-group-item-heading,
.list-group-item.active .list-group-item-heading > small,
.list-group-item.active:hover .list-group-item-heading > small,
.list-group-item.active:focus .list-group-item-heading > small,
.list-group-item.active .list-group-item-heading > .small,
.list-group-item.active:hover .list-group-item-heading > .small,
.list-group-item.active:focus .list-group-item-heading > .small {
  color: inherit;
}
.list-group-item.active .list-group-item-text,
.list-group-item.active:hover .list-group-item-text,
.list-group-item.active:focus .list-group-item-text {
  color: #c7ddef;
}
.list-group-item-success {
  color: #3c763d;
  background-color: #dff0d8;
}
a.list-group-item-success,
button.list-group-item-success {
  color: #3c763d;
}
a.list-group-item-success .list-group-item-heading,
button.list-group-item-success .list-group-item-heading {
  color: inherit;
}
a.list-group-item-success:hover,
button.list-group-item-success:hover,
a.list-group-item-success:focus,
button.list-group-item-success:focus {
  color: #3c763d;
  background-color: #d0e9c6;
}
a.list-group-item-success.active,
button.list-group-item-success.active,
a.list-group-item-success.active:hover,
button.list-group-item-success.active:hover,
a.list-group-item-success.active:focus,
button.list-group-item-success.active:focus {
  color: #fff;
  background-color: #3c763d;
  border-color: #3c763d;
}
.list-group-item-info {
  color: #31708f;
  background-color: #d9edf7;
}
a.list-group-item-info,
button.list-group-item-info {
  color: #31708f;
}
a.list-group-item-info .list-group-item-heading,
button.list-group-item-info .list-group-item-heading {
  color: inherit;
}
a.list-group-item-info:hover,
button.list-group-item-info:hover,
a.list-group-item-info:focus,
button.list-group-item-info:focus {
  color: #31708f;
  background-color: #c4e3f3;
}
a.list-group-item-info.active,
button.list-group-item-info.active,
a.list-group-item-info.active:hover,
button.list-group-item-info.active:hover,
a.list-group-item-info.active:focus,
button.list-group-item-info.active:focus {
  color: #fff;
  background-color: #31708f;
  border-color: #31708f;
}
.list-group-item-warning {
  color: #8a6d3b;
  background-color: #fcf8e3;
}
a.list-group-item-warning,
button.list-group-item-warning {
  color: #8a6d3b;
}
a.list-group-item-warning .list-group-item-heading,
button.list-group-item-warning .list-group-item-heading {
  color: inherit;
}
a.list-group-item-warning:hover,
button.list-group-item-warning:hover,
a.list-group-item-warning:focus,
button.list-group-item-warning:focus {
  color: #8a6d3b;
  background-color: #faf2cc;
}
a.list-group-item-warning.active,
button.list-group-item-warning.active,
a.list-group-item-warning.active:hover,
button.list-group-item-warning.active:hover,
a.list-group-item-warning.active:focus,
button.list-group-item-warning.active:focus {
  color: #fff;
  background-color: #8a6d3b;
  border-color: #8a6d3b;
}
.list-group-item-danger {
  color: #a94442;
  background-color: #f2dede;
}
a.list-group-item-danger,
button.list-group-item-danger {
  color: #a94442;
}
a.list-group-item-danger .list-group-item-heading,
button.list-group-item-danger .list-group-item-heading {
  color: inherit;
}
a.list-group-item-danger:hover,
button.list-group-item-danger:hover,
a.list-group-item-danger:focus,
button.list-group-item-danger:focus {
  color: #a94442;
  background-color: #ebcccc;
}
a.list-group-item-danger.active,
button.list-group-item-danger.active,
a.list-group-item-danger.active:hover,
button.list-group-item-danger.active:hover,
a.list-group-item-danger.active:focus,
button.list-group-item-danger.active:focus {
  color: #fff;
  background-color: #a94442;
  border-color: #a94442;
}
.list-group-item-heading {
  margin-top: 0;
  margin-bottom: 5px;
}
.list-group-item-text {
  margin-bottom: 0;
  line-height: 1.3;
}
.panel {
  margin-bottom: 18px;
  background-color: #fff;
  border: 1px solid transparent;
  border-radius: 2px;
  -webkit-box-shadow: 0 1px 1px rgba(0, 0, 0, 0.05);
  box-shadow: 0 1px 1px rgba(0, 0, 0, 0.05);
}
.panel-body {
  padding: 15px;
}
.panel-heading {
  padding: 10px 15px;
  border-bottom: 1px solid transparent;
  border-top-right-radius: 1px;
  border-top-left-radius: 1px;
}
.panel-heading > .dropdown .dropdown-toggle {
  color: inherit;
}
.panel-title {
  margin-top: 0;
  margin-bottom: 0;
  font-size: 15px;
  color: inherit;
}
.panel-title > a,
.panel-title > small,
.panel-title > .small,
.panel-title > small > a,
.panel-title > .small > a {
  color: inherit;
}
.panel-footer {
  padding: 10px 15px;
  background-color: #f5f5f5;
  border-top: 1px solid #ddd;
  border-bottom-right-radius: 1px;
  border-bottom-left-radius: 1px;
}
.panel > .list-group,
.panel > .panel-collapse > .list-group {
  margin-bottom: 0;
}
.panel > .list-group .list-group-item,
.panel > .panel-collapse > .list-group .list-group-item {
  border-width: 1px 0;
  border-radius: 0;
}
.panel > .list-group:first-child .list-group-item:first-child,
.panel > .panel-collapse > .list-group:first-child .list-group-item:first-child {
  border-top: 0;
  border-top-right-radius: 1px;
  border-top-left-radius: 1px;
}
.panel > .list-group:last-child .list-group-item:last-child,
.panel > .panel-collapse > .list-group:last-child .list-group-item:last-child {
  border-bottom: 0;
  border-bottom-right-radius: 1px;
  border-bottom-left-radius: 1px;
}
.panel > .panel-heading + .panel-collapse > .list-group .list-group-item:first-child {
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.panel-heading + .list-group .list-group-item:first-child {
  border-top-width: 0;
}
.list-group + .panel-footer {
  border-top-width: 0;
}
.panel > .table,
.panel > .table-responsive > .table,
.panel > .panel-collapse > .table {
  margin-bottom: 0;
}
.panel > .table caption,
.panel > .table-responsive > .table caption,
.panel > .panel-collapse > .table caption {
  padding-left: 15px;
  padding-right: 15px;
}
.panel > .table:first-child,
.panel > .table-responsive:first-child > .table:first-child {
  border-top-right-radius: 1px;
  border-top-left-radius: 1px;
}
.panel > .table:first-child > thead:first-child > tr:first-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child,
.panel > .table:first-child > tbody:first-child > tr:first-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child {
  border-top-left-radius: 1px;
  border-top-right-radius: 1px;
}
.panel > .table:first-child > thead:first-child > tr:first-child td:first-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child td:first-child,
.panel > .table:first-child > tbody:first-child > tr:first-child td:first-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child td:first-child,
.panel > .table:first-child > thead:first-child > tr:first-child th:first-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child th:first-child,
.panel > .table:first-child > tbody:first-child > tr:first-child th:first-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child th:first-child {
  border-top-left-radius: 1px;
}
.panel > .table:first-child > thead:first-child > tr:first-child td:last-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child td:last-child,
.panel > .table:first-child > tbody:first-child > tr:first-child td:last-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child td:last-child,
.panel > .table:first-child > thead:first-child > tr:first-child th:last-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child th:last-child,
.panel > .table:first-child > tbody:first-child > tr:first-child th:last-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child th:last-child {
  border-top-right-radius: 1px;
}
.panel > .table:last-child,
.panel > .table-responsive:last-child > .table:last-child {
  border-bottom-right-radius: 1px;
  border-bottom-left-radius: 1px;
}
.panel > .table:last-child > tbody:last-child > tr:last-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child {
  border-bottom-left-radius: 1px;
  border-bottom-right-radius: 1px;
}
.panel > .table:last-child > tbody:last-child > tr:last-child td:first-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child td:first-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child td:first-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child td:first-child,
.panel > .table:last-child > tbody:last-child > tr:last-child th:first-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child th:first-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child th:first-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child th:first-child {
  border-bottom-left-radius: 1px;
}
.panel > .table:last-child > tbody:last-child > tr:last-child td:last-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child td:last-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child td:last-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child td:last-child,
.panel > .table:last-child > tbody:last-child > tr:last-child th:last-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child th:last-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child th:last-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child th:last-child {
  border-bottom-right-radius: 1px;
}
.panel > .panel-body + .table,
.panel > .panel-body + .table-responsive,
.panel > .table + .panel-body,
.panel > .table-responsive + .panel-body {
  border-top: 1px solid #ddd;
}
.panel > .table > tbody:first-child > tr:first-child th,
.panel > .table > tbody:first-child > tr:first-child td {
  border-top: 0;
}
.panel > .table-bordered,
.panel > .table-responsive > .table-bordered {
  border: 0;
}
.panel > .table-bordered > thead > tr > th:first-child,
.panel > .table-responsive > .table-bordered > thead > tr > th:first-child,
.panel > .table-bordered > tbody > tr > th:first-child,
.panel > .table-responsive > .table-bordered > tbody > tr > th:first-child,
.panel > .table-bordered > tfoot > tr > th:first-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > th:first-child,
.panel > .table-bordered > thead > tr > td:first-child,
.panel > .table-responsive > .table-bordered > thead > tr > td:first-child,
.panel > .table-bordered > tbody > tr > td:first-child,
.panel > .table-responsive > .table-bordered > tbody > tr > td:first-child,
.panel > .table-bordered > tfoot > tr > td:first-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > td:first-child {
  border-left: 0;
}
.panel > .table-bordered > thead > tr > th:last-child,
.panel > .table-responsive > .table-bordered > thead > tr > th:last-child,
.panel > .table-bordered > tbody > tr > th:last-child,
.panel > .table-responsive > .table-bordered > tbody > tr > th:last-child,
.panel > .table-bordered > tfoot > tr > th:last-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > th:last-child,
.panel > .table-bordered > thead > tr > td:last-child,
.panel > .table-responsive > .table-bordered > thead > tr > td:last-child,
.panel > .table-bordered > tbody > tr > td:last-child,
.panel > .table-responsive > .table-bordered > tbody > tr > td:last-child,
.panel > .table-bordered > tfoot > tr > td:last-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > td:last-child {
  border-right: 0;
}
.panel > .table-bordered > thead > tr:first-child > td,
.panel > .table-responsive > .table-bordered > thead > tr:first-child > td,
.panel > .table-bordered > tbody > tr:first-child > td,
.panel > .table-responsive > .table-bordered > tbody > tr:first-child > td,
.panel > .table-bordered > thead > tr:first-child > th,
.panel > .table-responsive > .table-bordered > thead > tr:first-child > th,
.panel > .table-bordered > tbody > tr:first-child > th,
.panel > .table-responsive > .table-bordered > tbody > tr:first-child > th {
  border-bottom: 0;
}
.panel > .table-bordered > tbody > tr:last-child > td,
.panel > .table-responsive > .table-bordered > tbody > tr:last-child > td,
.panel > .table-bordered > tfoot > tr:last-child > td,
.panel > .table-responsive > .table-bordered > tfoot > tr:last-child > td,
.panel > .table-bordered > tbody > tr:last-child > th,
.panel > .table-responsive > .table-bordered > tbody > tr:last-child > th,
.panel > .table-bordered > tfoot > tr:last-child > th,
.panel > .table-responsive > .table-bordered > tfoot > tr:last-child > th {
  border-bottom: 0;
}
.panel > .table-responsive {
  border: 0;
  margin-bottom: 0;
}
.panel-group {
  margin-bottom: 18px;
}
.panel-group .panel {
  margin-bottom: 0;
  border-radius: 2px;
}
.panel-group .panel + .panel {
  margin-top: 5px;
}
.panel-group .panel-heading {
  border-bottom: 0;
}
.panel-group .panel-heading + .panel-collapse > .panel-body,
.panel-group .panel-heading + .panel-collapse > .list-group {
  border-top: 1px solid #ddd;
}
.panel-group .panel-footer {
  border-top: 0;
}
.panel-group .panel-footer + .panel-collapse .panel-body {
  border-bottom: 1px solid #ddd;
}
.panel-default {
  border-color: #ddd;
}
.panel-default > .panel-heading {
  color: #333333;
  background-color: #f5f5f5;
  border-color: #ddd;
}
.panel-default > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #ddd;
}
.panel-default > .panel-heading .badge {
  color: #f5f5f5;
  background-color: #333333;
}
.panel-default > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #ddd;
}
.panel-primary {
  border-color: #337ab7;
}
.panel-primary > .panel-heading {
  color: #fff;
  background-color: #337ab7;
  border-color: #337ab7;
}
.panel-primary > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #337ab7;
}
.panel-primary > .panel-heading .badge {
  color: #337ab7;
  background-color: #fff;
}
.panel-primary > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #337ab7;
}
.panel-success {
  border-color: #d6e9c6;
}
.panel-success > .panel-heading {
  color: #3c763d;
  background-color: #dff0d8;
  border-color: #d6e9c6;
}
.panel-success > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #d6e9c6;
}
.panel-success > .panel-heading .badge {
  color: #dff0d8;
  background-color: #3c763d;
}
.panel-success > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #d6e9c6;
}
.panel-info {
  border-color: #bce8f1;
}
.panel-info > .panel-heading {
  color: #31708f;
  background-color: #d9edf7;
  border-color: #bce8f1;
}
.panel-info > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #bce8f1;
}
.panel-info > .panel-heading .badge {
  color: #d9edf7;
  background-color: #31708f;
}
.panel-info > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #bce8f1;
}
.panel-warning {
  border-color: #faebcc;
}
.panel-warning > .panel-heading {
  color: #8a6d3b;
  background-color: #fcf8e3;
  border-color: #faebcc;
}
.panel-warning > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #faebcc;
}
.panel-warning > .panel-heading .badge {
  color: #fcf8e3;
  background-color: #8a6d3b;
}
.panel-warning > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #faebcc;
}
.panel-danger {
  border-color: #ebccd1;
}
.panel-danger > .panel-heading {
  color: #a94442;
  background-color: #f2dede;
  border-color: #ebccd1;
}
.panel-danger > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #ebccd1;
}
.panel-danger > .panel-heading .badge {
  color: #f2dede;
  background-color: #a94442;
}
.panel-danger > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #ebccd1;
}
.embed-responsive {
  position: relative;
  display: block;
  height: 0;
  padding: 0;
  overflow: hidden;
}
.embed-responsive .embed-responsive-item,
.embed-responsive iframe,
.embed-responsive embed,
.embed-responsive object,
.embed-responsive video {
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  height: 100%;
  width: 100%;
  border: 0;
}
.embed-responsive-16by9 {
  padding-bottom: 56.25%;
}
.embed-responsive-4by3 {
  padding-bottom: 75%;
}
.well {
  min-height: 20px;
  padding: 19px;
  margin-bottom: 20px;
  background-color: #f5f5f5;
  border: 1px solid #e3e3e3;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.05);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.05);
}
.well blockquote {
  border-color: #ddd;
  border-color: rgba(0, 0, 0, 0.15);
}
.well-lg {
  padding: 24px;
  border-radius: 3px;
}
.well-sm {
  padding: 9px;
  border-radius: 1px;
}
.close {
  float: right;
  font-size: 19.5px;
  font-weight: bold;
  line-height: 1;
  color: #000;
  text-shadow: 0 1px 0 #fff;
  opacity: 0.2;
  filter: alpha(opacity=20);
}
.close:hover,
.close:focus {
  color: #000;
  text-decoration: none;
  cursor: pointer;
  opacity: 0.5;
  filter: alpha(opacity=50);
}
button.close {
  padding: 0;
  cursor: pointer;
  background: transparent;
  border: 0;
  -webkit-appearance: none;
}
.modal-open {
  overflow: hidden;
}
.modal {
  display: none;
  overflow: hidden;
  position: fixed;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  z-index: 1050;
  -webkit-overflow-scrolling: touch;
  outline: 0;
}
.modal.fade .modal-dialog {
  -webkit-transform: translate(0, -25%);
  -ms-transform: translate(0, -25%);
  -o-transform: translate(0, -25%);
  transform: translate(0, -25%);
  -webkit-transition: -webkit-transform 0.3s ease-out;
  -moz-transition: -moz-transform 0.3s ease-out;
  -o-transition: -o-transform 0.3s ease-out;
  transition: transform 0.3s ease-out;
}
.modal.in .modal-dialog {
  -webkit-transform: translate(0, 0);
  -ms-transform: translate(0, 0);
  -o-transform: translate(0, 0);
  transform: translate(0, 0);
}
.modal-open .modal {
  overflow-x: hidden;
  overflow-y: auto;
}
.modal-dialog {
  position: relative;
  width: auto;
  margin: 10px;
}
.modal-content {
  position: relative;
  background-color: #fff;
  border: 1px solid #999;
  border: 1px solid rgba(0, 0, 0, 0.2);
  border-radius: 3px;
  -webkit-box-shadow: 0 3px 9px rgba(0, 0, 0, 0.5);
  box-shadow: 0 3px 9px rgba(0, 0, 0, 0.5);
  background-clip: padding-box;
  outline: 0;
}
.modal-backdrop {
  position: fixed;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  z-index: 1040;
  background-color: #000;
}
.modal-backdrop.fade {
  opacity: 0;
  filter: alpha(opacity=0);
}
.modal-backdrop.in {
  opacity: 0.5;
  filter: alpha(opacity=50);
}
.modal-header {
  padding: 15px;
  border-bottom: 1px solid #e5e5e5;
}
.modal-header .close {
  margin-top: -2px;
}
.modal-title {
  margin: 0;
  line-height: 1.42857143;
}
.modal-body {
  position: relative;
  padding: 15px;
}
.modal-footer {
  padding: 15px;
  text-align: right;
  border-top: 1px solid #e5e5e5;
}
.modal-footer .btn + .btn {
  margin-left: 5px;
  margin-bottom: 0;
}
.modal-footer .btn-group .btn + .btn {
  margin-left: -1px;
}
.modal-footer .btn-block + .btn-block {
  margin-left: 0;
}
.modal-scrollbar-measure {
  position: absolute;
  top: -9999px;
  width: 50px;
  height: 50px;
  overflow: scroll;
}
@media (min-width: 768px) {
  .modal-dialog {
    width: 600px;
    margin: 30px auto;
  }
  .modal-content {
    -webkit-box-shadow: 0 5px 15px rgba(0, 0, 0, 0.5);
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.5);
  }
  .modal-sm {
    width: 300px;
  }
}
@media (min-width: 992px) {
  .modal-lg {
    width: 900px;
  }
}
.tooltip {
  position: absolute;
  z-index: 1070;
  display: block;
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-style: normal;
  font-weight: normal;
  letter-spacing: normal;
  line-break: auto;
  line-height: 1.42857143;
  text-align: left;
  text-align: start;
  text-decoration: none;
  text-shadow: none;
  text-transform: none;
  white-space: normal;
  word-break: normal;
  word-spacing: normal;
  word-wrap: normal;
  font-size: 12px;
  opacity: 0;
  filter: alpha(opacity=0);
}
.tooltip.in {
  opacity: 0.9;
  filter: alpha(opacity=90);
}
.tooltip.top {
  margin-top: -3px;
  padding: 5px 0;
}
.tooltip.right {
  margin-left: 3px;
  padding: 0 5px;
}
.tooltip.bottom {
  margin-top: 3px;
  padding: 5px 0;
}
.tooltip.left {
  margin-left: -3px;
  padding: 0 5px;
}
.tooltip-inner {
  max-width: 200px;
  padding: 3px 8px;
  color: #fff;
  text-align: center;
  background-color: #000;
  border-radius: 2px;
}
.tooltip-arrow {
  position: absolute;
  width: 0;
  height: 0;
  border-color: transparent;
  border-style: solid;
}
.tooltip.top .tooltip-arrow {
  bottom: 0;
  left: 50%;
  margin-left: -5px;
  border-width: 5px 5px 0;
  border-top-color: #000;
}
.tooltip.top-left .tooltip-arrow {
  bottom: 0;
  right: 5px;
  margin-bottom: -5px;
  border-width: 5px 5px 0;
  border-top-color: #000;
}
.tooltip.top-right .tooltip-arrow {
  bottom: 0;
  left: 5px;
  margin-bottom: -5px;
  border-width: 5px 5px 0;
  border-top-color: #000;
}
.tooltip.right .tooltip-arrow {
  top: 50%;
  left: 0;
  margin-top: -5px;
  border-width: 5px 5px 5px 0;
  border-right-color: #000;
}
.tooltip.left .tooltip-arrow {
  top: 50%;
  right: 0;
  margin-top: -5px;
  border-width: 5px 0 5px 5px;
  border-left-color: #000;
}
.tooltip.bottom .tooltip-arrow {
  top: 0;
  left: 50%;
  margin-left: -5px;
  border-width: 0 5px 5px;
  border-bottom-color: #000;
}
.tooltip.bottom-left .tooltip-arrow {
  top: 0;
  right: 5px;
  margin-top: -5px;
  border-width: 0 5px 5px;
  border-bottom-color: #000;
}
.tooltip.bottom-right .tooltip-arrow {
  top: 0;
  left: 5px;
  margin-top: -5px;
  border-width: 0 5px 5px;
  border-bottom-color: #000;
}
.popover {
  position: absolute;
  top: 0;
  left: 0;
  z-index: 1060;
  display: none;
  max-width: 276px;
  padding: 1px;
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-style: normal;
  font-weight: normal;
  letter-spacing: normal;
  line-break: auto;
  line-height: 1.42857143;
  text-align: left;
  text-align: start;
  text-decoration: none;
  text-shadow: none;
  text-transform: none;
  white-space: normal;
  word-break: normal;
  word-spacing: normal;
  word-wrap: normal;
  font-size: 13px;
  background-color: #fff;
  background-clip: padding-box;
  border: 1px solid #ccc;
  border: 1px solid rgba(0, 0, 0, 0.2);
  border-radius: 3px;
  -webkit-box-shadow: 0 5px 10px rgba(0, 0, 0, 0.2);
  box-shadow: 0 5px 10px rgba(0, 0, 0, 0.2);
}
.popover.top {
  margin-top: -10px;
}
.popover.right {
  margin-left: 10px;
}
.popover.bottom {
  margin-top: 10px;
}
.popover.left {
  margin-left: -10px;
}
.popover-title {
  margin: 0;
  padding: 8px 14px;
  font-size: 13px;
  background-color: #f7f7f7;
  border-bottom: 1px solid #ebebeb;
  border-radius: 2px 2px 0 0;
}
.popover-content {
  padding: 9px 14px;
}
.popover > .arrow,
.popover > .arrow:after {
  position: absolute;
  display: block;
  width: 0;
  height: 0;
  border-color: transparent;
  border-style: solid;
}
.popover > .arrow {
  border-width: 11px;
}
.popover > .arrow:after {
  border-width: 10px;
  content: "";
}
.popover.top > .arrow {
  left: 50%;
  margin-left: -11px;
  border-bottom-width: 0;
  border-top-color: #999999;
  border-top-color: rgba(0, 0, 0, 0.25);
  bottom: -11px;
}
.popover.top > .arrow:after {
  content: " ";
  bottom: 1px;
  margin-left: -10px;
  border-bottom-width: 0;
  border-top-color: #fff;
}
.popover.right > .arrow {
  top: 50%;
  left: -11px;
  margin-top: -11px;
  border-left-width: 0;
  border-right-color: #999999;
  border-right-color: rgba(0, 0, 0, 0.25);
}
.popover.right > .arrow:after {
  content: " ";
  left: 1px;
  bottom: -10px;
  border-left-width: 0;
  border-right-color: #fff;
}
.popover.bottom > .arrow {
  left: 50%;
  margin-left: -11px;
  border-top-width: 0;
  border-bottom-color: #999999;
  border-bottom-color: rgba(0, 0, 0, 0.25);
  top: -11px;
}
.popover.bottom > .arrow:after {
  content: " ";
  top: 1px;
  margin-left: -10px;
  border-top-width: 0;
  border-bottom-color: #fff;
}
.popover.left > .arrow {
  top: 50%;
  right: -11px;
  margin-top: -11px;
  border-right-width: 0;
  border-left-color: #999999;
  border-left-color: rgba(0, 0, 0, 0.25);
}
.popover.left > .arrow:after {
  content: " ";
  right: 1px;
  border-right-width: 0;
  border-left-color: #fff;
  bottom: -10px;
}
.carousel {
  position: relative;
}
.carousel-inner {
  position: relative;
  overflow: hidden;
  width: 100%;
}
.carousel-inner > .item {
  display: none;
  position: relative;
  -webkit-transition: 0.6s ease-in-out left;
  -o-transition: 0.6s ease-in-out left;
  transition: 0.6s ease-in-out left;
}
.carousel-inner > .item > img,
.carousel-inner > .item > a > img {
  line-height: 1;
}
@media all and (transform-3d), (-webkit-transform-3d) {
  .carousel-inner > .item {
    -webkit-transition: -webkit-transform 0.6s ease-in-out;
    -moz-transition: -moz-transform 0.6s ease-in-out;
    -o-transition: -o-transform 0.6s ease-in-out;
    transition: transform 0.6s ease-in-out;
    -webkit-backface-visibility: hidden;
    -moz-backface-visibility: hidden;
    backface-visibility: hidden;
    -webkit-perspective: 1000px;
    -moz-perspective: 1000px;
    perspective: 1000px;
  }
  .carousel-inner > .item.next,
  .carousel-inner > .item.active.right {
    -webkit-transform: translate3d(100%, 0, 0);
    transform: translate3d(100%, 0, 0);
    left: 0;
  }
  .carousel-inner > .item.prev,
  .carousel-inner > .item.active.left {
    -webkit-transform: translate3d(-100%, 0, 0);
    transform: translate3d(-100%, 0, 0);
    left: 0;
  }
  .carousel-inner > .item.next.left,
  .carousel-inner > .item.prev.right,
  .carousel-inner > .item.active {
    -webkit-transform: translate3d(0, 0, 0);
    transform: translate3d(0, 0, 0);
    left: 0;
  }
}
.carousel-inner > .active,
.carousel-inner > .next,
.carousel-inner > .prev {
  display: block;
}
.carousel-inner > .active {
  left: 0;
}
.carousel-inner > .next,
.carousel-inner > .prev {
  position: absolute;
  top: 0;
  width: 100%;
}
.carousel-inner > .next {
  left: 100%;
}
.carousel-inner > .prev {
  left: -100%;
}
.carousel-inner > .next.left,
.carousel-inner > .prev.right {
  left: 0;
}
.carousel-inner > .active.left {
  left: -100%;
}
.carousel-inner > .active.right {
  left: 100%;
}
.carousel-control {
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  width: 15%;
  opacity: 0.5;
  filter: alpha(opacity=50);
  font-size: 20px;
  color: #fff;
  text-align: center;
  text-shadow: 0 1px 2px rgba(0, 0, 0, 0.6);
  background-color: rgba(0, 0, 0, 0);
}
.carousel-control.left {
  background-image: -webkit-linear-gradient(left, rgba(0, 0, 0, 0.5) 0%, rgba(0, 0, 0, 0.0001) 100%);
  background-image: -o-linear-gradient(left, rgba(0, 0, 0, 0.5) 0%, rgba(0, 0, 0, 0.0001) 100%);
  background-image: linear-gradient(to right, rgba(0, 0, 0, 0.5) 0%, rgba(0, 0, 0, 0.0001) 100%);
  background-repeat: repeat-x;
  filter: progid:DXImageTransform.Microsoft.gradient(startColorstr='#80000000', endColorstr='#00000000', GradientType=1);
}
.carousel-control.right {
  left: auto;
  right: 0;
  background-image: -webkit-linear-gradient(left, rgba(0, 0, 0, 0.0001) 0%, rgba(0, 0, 0, 0.5) 100%);
  background-image: -o-linear-gradient(left, rgba(0, 0, 0, 0.0001) 0%, rgba(0, 0, 0, 0.5) 100%);
  background-image: linear-gradient(to right, rgba(0, 0, 0, 0.0001) 0%, rgba(0, 0, 0, 0.5) 100%);
  background-repeat: repeat-x;
  filter: progid:DXImageTransform.Microsoft.gradient(startColorstr='#00000000', endColorstr='#80000000', GradientType=1);
}
.carousel-control:hover,
.carousel-control:focus {
  outline: 0;
  color: #fff;
  text-decoration: none;
  opacity: 0.9;
  filter: alpha(opacity=90);
}
.carousel-control .icon-prev,
.carousel-control .icon-next,
.carousel-control .glyphicon-chevron-left,
.carousel-control .glyphicon-chevron-right {
  position: absolute;
  top: 50%;
  margin-top: -10px;
  z-index: 5;
  display: inline-block;
}
.carousel-control .icon-prev,
.carousel-control .glyphicon-chevron-left {
  left: 50%;
  margin-left: -10px;
}
.carousel-control .icon-next,
.carousel-control .glyphicon-chevron-right {
  right: 50%;
  margin-right: -10px;
}
.carousel-control .icon-prev,
.carousel-control .icon-next {
  width: 20px;
  height: 20px;
  line-height: 1;
  font-family: serif;
}
.carousel-control .icon-prev:before {
  content: '\2039';
}
.carousel-control .icon-next:before {
  content: '\203a';
}
.carousel-indicators {
  position: absolute;
  bottom: 10px;
  left: 50%;
  z-index: 15;
  width: 60%;
  margin-left: -30%;
  padding-left: 0;
  list-style: none;
  text-align: center;
}
.carousel-indicators li {
  display: inline-block;
  width: 10px;
  height: 10px;
  margin: 1px;
  text-indent: -999px;
  border: 1px solid #fff;
  border-radius: 10px;
  cursor: pointer;
  background-color: #000 \9;
  background-color: rgba(0, 0, 0, 0);
}
.carousel-indicators .active {
  margin: 0;
  width: 12px;
  height: 12px;
  background-color: #fff;
}
.carousel-caption {
  position: absolute;
  left: 15%;
  right: 15%;
  bottom: 20px;
  z-index: 10;
  padding-top: 20px;
  padding-bottom: 20px;
  color: #fff;
  text-align: center;
  text-shadow: 0 1px 2px rgba(0, 0, 0, 0.6);
}
.carousel-caption .btn {
  text-shadow: none;
}
@media screen and (min-width: 768px) {
  .carousel-control .glyphicon-chevron-left,
  .carousel-control .glyphicon-chevron-right,
  .carousel-control .icon-prev,
  .carousel-control .icon-next {
    width: 30px;
    height: 30px;
    margin-top: -10px;
    font-size: 30px;
  }
  .carousel-control .glyphicon-chevron-left,
  .carousel-control .icon-prev {
    margin-left: -10px;
  }
  .carousel-control .glyphicon-chevron-right,
  .carousel-control .icon-next {
    margin-right: -10px;
  }
  .carousel-caption {
    left: 20%;
    right: 20%;
    padding-bottom: 30px;
  }
  .carousel-indicators {
    bottom: 20px;
  }
}
.clearfix:before,
.clearfix:after,
.dl-horizontal dd:before,
.dl-horizontal dd:after,
.container:before,
.container:after,
.container-fluid:before,
.container-fluid:after,
.row:before,
.row:after,
.form-horizontal .form-group:before,
.form-horizontal .form-group:after,
.btn-toolbar:before,
.btn-toolbar:after,
.btn-group-vertical > .btn-group:before,
.btn-group-vertical > .btn-group:after,
.nav:before,
.nav:after,
.navbar:before,
.navbar:after,
.navbar-header:before,
.navbar-header:after,
.navbar-collapse:before,
.navbar-collapse:after,
.pager:before,
.pager:after,
.panel-body:before,
.panel-body:after,
.modal-header:before,
.modal-header:after,
.modal-footer:before,
.modal-footer:after,
.item_buttons:before,
.item_buttons:after {
  content: " ";
  display: table;
}
.clearfix:after,
.dl-horizontal dd:after,
.container:after,
.container-fluid:after,
.row:after,
.form-horizontal .form-group:after,
.btn-toolbar:after,
.btn-group-vertical > .btn-group:after,
.nav:after,
.navbar:after,
.navbar-header:after,
.navbar-collapse:after,
.pager:after,
.panel-body:after,
.modal-header:after,
.modal-footer:after,
.item_buttons:after {
  clear: both;
}
.center-block {
  display: block;
  margin-left: auto;
  margin-right: auto;
}
.pull-right {
  float: right !important;
}
.pull-left {
  float: left !important;
}
.hide {
  display: none !important;
}
.show {
  display: block !important;
}
.invisible {
  visibility: hidden;
}
.text-hide {
  font: 0/0 a;
  color: transparent;
  text-shadow: none;
  background-color: transparent;
  border: 0;
}
.hidden {
  display: none !important;
}
.affix {
  position: fixed;
}
@-ms-viewport {
  width: device-width;
}
.visible-xs,
.visible-sm,
.visible-md,
.visible-lg {
  display: none !important;
}
.visible-xs-block,
.visible-xs-inline,
.visible-xs-inline-block,
.visible-sm-block,
.visible-sm-inline,
.visible-sm-inline-block,
.visible-md-block,
.visible-md-inline,
.visible-md-inline-block,
.visible-lg-block,
.visible-lg-inline,
.visible-lg-inline-block {
  display: none !important;
}
@media (max-width: 767px) {
  .visible-xs {
    display: block !important;
  }
  table.visible-xs {
    display: table !important;
  }
  tr.visible-xs {
    display: table-row !important;
  }
  th.visible-xs,
  td.visible-xs {
    display: table-cell !important;
  }
}
@media (max-width: 767px) {
  .visible-xs-block {
    display: block !important;
  }
}
@media (max-width: 767px) {
  .visible-xs-inline {
    display: inline !important;
  }
}
@media (max-width: 767px) {
  .visible-xs-inline-block {
    display: inline-block !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm {
    display: block !important;
  }
  table.visible-sm {
    display: table !important;
  }
  tr.visible-sm {
    display: table-row !important;
  }
  th.visible-sm,
  td.visible-sm {
    display: table-cell !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm-block {
    display: block !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm-inline {
    display: inline !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm-inline-block {
    display: inline-block !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md {
    display: block !important;
  }
  table.visible-md {
    display: table !important;
  }
  tr.visible-md {
    display: table-row !important;
  }
  th.visible-md,
  td.visible-md {
    display: table-cell !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md-block {
    display: block !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md-inline {
    display: inline !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md-inline-block {
    display: inline-block !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg {
    display: block !important;
  }
  table.visible-lg {
    display: table !important;
  }
  tr.visible-lg {
    display: table-row !important;
  }
  th.visible-lg,
  td.visible-lg {
    display: table-cell !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg-block {
    display: block !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg-inline {
    display: inline !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg-inline-block {
    display: inline-block !important;
  }
}
@media (max-width: 767px) {
  .hidden-xs {
    display: none !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .hidden-sm {
    display: none !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .hidden-md {
    display: none !important;
  }
}
@media (min-width: 1200px) {
  .hidden-lg {
    display: none !important;
  }
}
.visible-print {
  display: none !important;
}
@media print {
  .visible-print {
    display: block !important;
  }
  table.visible-print {
    display: table !important;
  }
  tr.visible-print {
    display: table-row !important;
  }
  th.visible-print,
  td.visible-print {
    display: table-cell !important;
  }
}
.visible-print-block {
  display: none !important;
}
@media print {
  .visible-print-block {
    display: block !important;
  }
}
.visible-print-inline {
  display: none !important;
}
@media print {
  .visible-print-inline {
    display: inline !important;
  }
}
.visible-print-inline-block {
  display: none !important;
}
@media print {
  .visible-print-inline-block {
    display: inline-block !important;
  }
}
@media print {
  .hidden-print {
    display: none !important;
  }
}
/*!
*
* Font Awesome
*
*/
/*!
 *  Font Awesome 4.2.0 by @davegandy - http://fontawesome.io - @fontawesome
 *  License - http://fontawesome.io/license (Font: SIL OFL 1.1, CSS: MIT License)
 */
/* FONT PATH
 * -------------------------- */
@font-face {
  font-family: 'FontAwesome';
  src: url('../components/font-awesome/fonts/fontawesome-webfont.eot?v=4.2.0');
  src: url('../components/font-awesome/fonts/fontawesome-webfont.eot?#iefix&v=4.2.0') format('embedded-opentype'), url('../components/font-awesome/fonts/fontawesome-webfont.woff?v=4.2.0') format('woff'), url('../components/font-awesome/fonts/fontawesome-webfont.ttf?v=4.2.0') format('truetype'), url('../components/font-awesome/fonts/fontawesome-webfont.svg?v=4.2.0#fontawesomeregular') format('svg');
  font-weight: normal;
  font-style: normal;
}
.fa {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
/* makes the font 33% larger relative to the icon container */
.fa-lg {
  font-size: 1.33333333em;
  line-height: 0.75em;
  vertical-align: -15%;
}
.fa-2x {
  font-size: 2em;
}
.fa-3x {
  font-size: 3em;
}
.fa-4x {
  font-size: 4em;
}
.fa-5x {
  font-size: 5em;
}
.fa-fw {
  width: 1.28571429em;
  text-align: center;
}
.fa-ul {
  padding-left: 0;
  margin-left: 2.14285714em;
  list-style-type: none;
}
.fa-ul > li {
  position: relative;
}
.fa-li {
  position: absolute;
  left: -2.14285714em;
  width: 2.14285714em;
  top: 0.14285714em;
  text-align: center;
}
.fa-li.fa-lg {
  left: -1.85714286em;
}
.fa-border {
  padding: .2em .25em .15em;
  border: solid 0.08em #eee;
  border-radius: .1em;
}
.pull-right {
  float: right;
}
.pull-left {
  float: left;
}
.fa.pull-left {
  margin-right: .3em;
}
.fa.pull-right {
  margin-left: .3em;
}
.fa-spin {
  -webkit-animation: fa-spin 2s infinite linear;
  animation: fa-spin 2s infinite linear;
}
@-webkit-keyframes fa-spin {
  0% {
    -webkit-transform: rotate(0deg);
    transform: rotate(0deg);
  }
  100% {
    -webkit-transform: rotate(359deg);
    transform: rotate(359deg);
  }
}
@keyframes fa-spin {
  0% {
    -webkit-transform: rotate(0deg);
    transform: rotate(0deg);
  }
  100% {
    -webkit-transform: rotate(359deg);
    transform: rotate(359deg);
  }
}
.fa-rotate-90 {
  filter: progid:DXImageTransform.Microsoft.BasicImage(rotation=1);
  -webkit-transform: rotate(90deg);
  -ms-transform: rotate(90deg);
  transform: rotate(90deg);
}
.fa-rotate-180 {
  filter: progid:DXImageTransform.Microsoft.BasicImage(rotation=2);
  -webkit-transform: rotate(180deg);
  -ms-transform: rotate(180deg);
  transform: rotate(180deg);
}
.fa-rotate-270 {
  filter: progid:DXImageTransform.Microsoft.BasicImage(rotation=3);
  -webkit-transform: rotate(270deg);
  -ms-transform: rotate(270deg);
  transform: rotate(270deg);
}
.fa-flip-horizontal {
  filter: progid:DXImageTransform.Microsoft.BasicImage(rotation=0, mirror=1);
  -webkit-transform: scale(-1, 1);
  -ms-transform: scale(-1, 1);
  transform: scale(-1, 1);
}
.fa-flip-vertical {
  filter: progid:DXImageTransform.Microsoft.BasicImage(rotation=2, mirror=1);
  -webkit-transform: scale(1, -1);
  -ms-transform: scale(1, -1);
  transform: scale(1, -1);
}
:root .fa-rotate-90,
:root .fa-rotate-180,
:root .fa-rotate-270,
:root .fa-flip-horizontal,
:root .fa-flip-vertical {
  filter: none;
}
.fa-stack {
  position: relative;
  display: inline-block;
  width: 2em;
  height: 2em;
  line-height: 2em;
  vertical-align: middle;
}
.fa-stack-1x,
.fa-stack-2x {
  position: absolute;
  left: 0;
  width: 100%;
  text-align: center;
}
.fa-stack-1x {
  line-height: inherit;
}
.fa-stack-2x {
  font-size: 2em;
}
.fa-inverse {
  color: #fff;
}
/* Font Awesome uses the Unicode Private Use Area (PUA) to ensure screen
   readers do not read off random characters that represent icons */
.fa-glass:before {
  content: "\f000";
}
.fa-music:before {
  content: "\f001";
}
.fa-search:before {
  content: "\f002";
}
.fa-envelope-o:before {
  content: "\f003";
}
.fa-heart:before {
  content: "\f004";
}
.fa-star:before {
  content: "\f005";
}
.fa-star-o:before {
  content: "\f006";
}
.fa-user:before {
  content: "\f007";
}
.fa-film:before {
  content: "\f008";
}
.fa-th-large:before {
  content: "\f009";
}
.fa-th:before {
  content: "\f00a";
}
.fa-th-list:before {
  content: "\f00b";
}
.fa-check:before {
  content: "\f00c";
}
.fa-remove:before,
.fa-close:before,
.fa-times:before {
  content: "\f00d";
}
.fa-search-plus:before {
  content: "\f00e";
}
.fa-search-minus:before {
  content: "\f010";
}
.fa-power-off:before {
  content: "\f011";
}
.fa-signal:before {
  content: "\f012";
}
.fa-gear:before,
.fa-cog:before {
  content: "\f013";
}
.fa-trash-o:before {
  content: "\f014";
}
.fa-home:before {
  content: "\f015";
}
.fa-file-o:before {
  content: "\f016";
}
.fa-clock-o:before {
  content: "\f017";
}
.fa-road:before {
  content: "\f018";
}
.fa-download:before {
  content: "\f019";
}
.fa-arrow-circle-o-down:before {
  content: "\f01a";
}
.fa-arrow-circle-o-up:before {
  content: "\f01b";
}
.fa-inbox:before {
  content: "\f01c";
}
.fa-play-circle-o:before {
  content: "\f01d";
}
.fa-rotate-right:before,
.fa-repeat:before {
  content: "\f01e";
}
.fa-refresh:before {
  content: "\f021";
}
.fa-list-alt:before {
  content: "\f022";
}
.fa-lock:before {
  content: "\f023";
}
.fa-flag:before {
  content: "\f024";
}
.fa-headphones:before {
  content: "\f025";
}
.fa-volume-off:before {
  content: "\f026";
}
.fa-volume-down:before {
  content: "\f027";
}
.fa-volume-up:before {
  content: "\f028";
}
.fa-qrcode:before {
  content: "\f029";
}
.fa-barcode:before {
  content: "\f02a";
}
.fa-tag:before {
  content: "\f02b";
}
.fa-tags:before {
  content: "\f02c";
}
.fa-book:before {
  content: "\f02d";
}
.fa-bookmark:before {
  content: "\f02e";
}
.fa-print:before {
  content: "\f02f";
}
.fa-camera:before {
  content: "\f030";
}
.fa-font:before {
  content: "\f031";
}
.fa-bold:before {
  content: "\f032";
}
.fa-italic:before {
  content: "\f033";
}
.fa-text-height:before {
  content: "\f034";
}
.fa-text-width:before {
  content: "\f035";
}
.fa-align-left:before {
  content: "\f036";
}
.fa-align-center:before {
  content: "\f037";
}
.fa-align-right:before {
  content: "\f038";
}
.fa-align-justify:before {
  content: "\f039";
}
.fa-list:before {
  content: "\f03a";
}
.fa-dedent:before,
.fa-outdent:before {
  content: "\f03b";
}
.fa-indent:before {
  content: "\f03c";
}
.fa-video-camera:before {
  content: "\f03d";
}
.fa-photo:before,
.fa-image:before,
.fa-picture-o:before {
  content: "\f03e";
}
.fa-pencil:before {
  content: "\f040";
}
.fa-map-marker:before {
  content: "\f041";
}
.fa-adjust:before {
  content: "\f042";
}
.fa-tint:before {
  content: "\f043";
}
.fa-edit:before,
.fa-pencil-square-o:before {
  content: "\f044";
}
.fa-share-square-o:before {
  content: "\f045";
}
.fa-check-square-o:before {
  content: "\f046";
}
.fa-arrows:before {
  content: "\f047";
}
.fa-step-backward:before {
  content: "\f048";
}
.fa-fast-backward:before {
  content: "\f049";
}
.fa-backward:before {
  content: "\f04a";
}
.fa-play:before {
  content: "\f04b";
}
.fa-pause:before {
  content: "\f04c";
}
.fa-stop:before {
  content: "\f04d";
}
.fa-forward:before {
  content: "\f04e";
}
.fa-fast-forward:before {
  content: "\f050";
}
.fa-step-forward:before {
  content: "\f051";
}
.fa-eject:before {
  content: "\f052";
}
.fa-chevron-left:before {
  content: "\f053";
}
.fa-chevron-right:before {
  content: "\f054";
}
.fa-plus-circle:before {
  content: "\f055";
}
.fa-minus-circle:before {
  content: "\f056";
}
.fa-times-circle:before {
  content: "\f057";
}
.fa-check-circle:before {
  content: "\f058";
}
.fa-question-circle:before {
  content: "\f059";
}
.fa-info-circle:before {
  content: "\f05a";
}
.fa-crosshairs:before {
  content: "\f05b";
}
.fa-times-circle-o:before {
  content: "\f05c";
}
.fa-check-circle-o:before {
  content: "\f05d";
}
.fa-ban:before {
  content: "\f05e";
}
.fa-arrow-left:before {
  content: "\f060";
}
.fa-arrow-right:before {
  content: "\f061";
}
.fa-arrow-up:before {
  content: "\f062";
}
.fa-arrow-down:before {
  content: "\f063";
}
.fa-mail-forward:before,
.fa-share:before {
  content: "\f064";
}
.fa-expand:before {
  content: "\f065";
}
.fa-compress:before {
  content: "\f066";
}
.fa-plus:before {
  content: "\f067";
}
.fa-minus:before {
  content: "\f068";
}
.fa-asterisk:before {
  content: "\f069";
}
.fa-exclamation-circle:before {
  content: "\f06a";
}
.fa-gift:before {
  content: "\f06b";
}
.fa-leaf:before {
  content: "\f06c";
}
.fa-fire:before {
  content: "\f06d";
}
.fa-eye:before {
  content: "\f06e";
}
.fa-eye-slash:before {
  content: "\f070";
}
.fa-warning:before,
.fa-exclamation-triangle:before {
  content: "\f071";
}
.fa-plane:before {
  content: "\f072";
}
.fa-calendar:before {
  content: "\f073";
}
.fa-random:before {
  content: "\f074";
}
.fa-comment:before {
  content: "\f075";
}
.fa-magnet:before {
  content: "\f076";
}
.fa-chevron-up:before {
  content: "\f077";
}
.fa-chevron-down:before {
  content: "\f078";
}
.fa-retweet:before {
  content: "\f079";
}
.fa-shopping-cart:before {
  content: "\f07a";
}
.fa-folder:before {
  content: "\f07b";
}
.fa-folder-open:before {
  content: "\f07c";
}
.fa-arrows-v:before {
  content: "\f07d";
}
.fa-arrows-h:before {
  content: "\f07e";
}
.fa-bar-chart-o:before,
.fa-bar-chart:before {
  content: "\f080";
}
.fa-twitter-square:before {
  content: "\f081";
}
.fa-facebook-square:before {
  content: "\f082";
}
.fa-camera-retro:before {
  content: "\f083";
}
.fa-key:before {
  content: "\f084";
}
.fa-gears:before,
.fa-cogs:before {
  content: "\f085";
}
.fa-comments:before {
  content: "\f086";
}
.fa-thumbs-o-up:before {
  content: "\f087";
}
.fa-thumbs-o-down:before {
  content: "\f088";
}
.fa-star-half:before {
  content: "\f089";
}
.fa-heart-o:before {
  content: "\f08a";
}
.fa-sign-out:before {
  content: "\f08b";
}
.fa-linkedin-square:before {
  content: "\f08c";
}
.fa-thumb-tack:before {
  content: "\f08d";
}
.fa-external-link:before {
  content: "\f08e";
}
.fa-sign-in:before {
  content: "\f090";
}
.fa-trophy:before {
  content: "\f091";
}
.fa-github-square:before {
  content: "\f092";
}
.fa-upload:before {
  content: "\f093";
}
.fa-lemon-o:before {
  content: "\f094";
}
.fa-phone:before {
  content: "\f095";
}
.fa-square-o:before {
  content: "\f096";
}
.fa-bookmark-o:before {
  content: "\f097";
}
.fa-phone-square:before {
  content: "\f098";
}
.fa-twitter:before {
  content: "\f099";
}
.fa-facebook:before {
  content: "\f09a";
}
.fa-github:before {
  content: "\f09b";
}
.fa-unlock:before {
  content: "\f09c";
}
.fa-credit-card:before {
  content: "\f09d";
}
.fa-rss:before {
  content: "\f09e";
}
.fa-hdd-o:before {
  content: "\f0a0";
}
.fa-bullhorn:before {
  content: "\f0a1";
}
.fa-bell:before {
  content: "\f0f3";
}
.fa-certificate:before {
  content: "\f0a3";
}
.fa-hand-o-right:before {
  content: "\f0a4";
}
.fa-hand-o-left:before {
  content: "\f0a5";
}
.fa-hand-o-up:before {
  content: "\f0a6";
}
.fa-hand-o-down:before {
  content: "\f0a7";
}
.fa-arrow-circle-left:before {
  content: "\f0a8";
}
.fa-arrow-circle-right:before {
  content: "\f0a9";
}
.fa-arrow-circle-up:before {
  content: "\f0aa";
}
.fa-arrow-circle-down:before {
  content: "\f0ab";
}
.fa-globe:before {
  content: "\f0ac";
}
.fa-wrench:before {
  content: "\f0ad";
}
.fa-tasks:before {
  content: "\f0ae";
}
.fa-filter:before {
  content: "\f0b0";
}
.fa-briefcase:before {
  content: "\f0b1";
}
.fa-arrows-alt:before {
  content: "\f0b2";
}
.fa-group:before,
.fa-users:before {
  content: "\f0c0";
}
.fa-chain:before,
.fa-link:before {
  content: "\f0c1";
}
.fa-cloud:before {
  content: "\f0c2";
}
.fa-flask:before {
  content: "\f0c3";
}
.fa-cut:before,
.fa-scissors:before {
  content: "\f0c4";
}
.fa-copy:before,
.fa-files-o:before {
  content: "\f0c5";
}
.fa-paperclip:before {
  content: "\f0c6";
}
.fa-save:before,
.fa-floppy-o:before {
  content: "\f0c7";
}
.fa-square:before {
  content: "\f0c8";
}
.fa-navicon:before,
.fa-reorder:before,
.fa-bars:before {
  content: "\f0c9";
}
.fa-list-ul:before {
  content: "\f0ca";
}
.fa-list-ol:before {
  content: "\f0cb";
}
.fa-strikethrough:before {
  content: "\f0cc";
}
.fa-underline:before {
  content: "\f0cd";
}
.fa-table:before {
  content: "\f0ce";
}
.fa-magic:before {
  content: "\f0d0";
}
.fa-truck:before {
  content: "\f0d1";
}
.fa-pinterest:before {
  content: "\f0d2";
}
.fa-pinterest-square:before {
  content: "\f0d3";
}
.fa-google-plus-square:before {
  content: "\f0d4";
}
.fa-google-plus:before {
  content: "\f0d5";
}
.fa-money:before {
  content: "\f0d6";
}
.fa-caret-down:before {
  content: "\f0d7";
}
.fa-caret-up:before {
  content: "\f0d8";
}
.fa-caret-left:before {
  content: "\f0d9";
}
.fa-caret-right:before {
  content: "\f0da";
}
.fa-columns:before {
  content: "\f0db";
}
.fa-unsorted:before,
.fa-sort:before {
  content: "\f0dc";
}
.fa-sort-down:before,
.fa-sort-desc:before {
  content: "\f0dd";
}
.fa-sort-up:before,
.fa-sort-asc:before {
  content: "\f0de";
}
.fa-envelope:before {
  content: "\f0e0";
}
.fa-linkedin:before {
  content: "\f0e1";
}
.fa-rotate-left:before,
.fa-undo:before {
  content: "\f0e2";
}
.fa-legal:before,
.fa-gavel:before {
  content: "\f0e3";
}
.fa-dashboard:before,
.fa-tachometer:before {
  content: "\f0e4";
}
.fa-comment-o:before {
  content: "\f0e5";
}
.fa-comments-o:before {
  content: "\f0e6";
}
.fa-flash:before,
.fa-bolt:before {
  content: "\f0e7";
}
.fa-sitemap:before {
  content: "\f0e8";
}
.fa-umbrella:before {
  content: "\f0e9";
}
.fa-paste:before,
.fa-clipboard:before {
  content: "\f0ea";
}
.fa-lightbulb-o:before {
  content: "\f0eb";
}
.fa-exchange:before {
  content: "\f0ec";
}
.fa-cloud-download:before {
  content: "\f0ed";
}
.fa-cloud-upload:before {
  content: "\f0ee";
}
.fa-user-md:before {
  content: "\f0f0";
}
.fa-stethoscope:before {
  content: "\f0f1";
}
.fa-suitcase:before {
  content: "\f0f2";
}
.fa-bell-o:before {
  content: "\f0a2";
}
.fa-coffee:before {
  content: "\f0f4";
}
.fa-cutlery:before {
  content: "\f0f5";
}
.fa-file-text-o:before {
  content: "\f0f6";
}
.fa-building-o:before {
  content: "\f0f7";
}
.fa-hospital-o:before {
  content: "\f0f8";
}
.fa-ambulance:before {
  content: "\f0f9";
}
.fa-medkit:before {
  content: "\f0fa";
}
.fa-fighter-jet:before {
  content: "\f0fb";
}
.fa-beer:before {
  content: "\f0fc";
}
.fa-h-square:before {
  content: "\f0fd";
}
.fa-plus-square:before {
  content: "\f0fe";
}
.fa-angle-double-left:before {
  content: "\f100";
}
.fa-angle-double-right:before {
  content: "\f101";
}
.fa-angle-double-up:before {
  content: "\f102";
}
.fa-angle-double-down:before {
  content: "\f103";
}
.fa-angle-left:before {
  content: "\f104";
}
.fa-angle-right:before {
  content: "\f105";
}
.fa-angle-up:before {
  content: "\f106";
}
.fa-angle-down:before {
  content: "\f107";
}
.fa-desktop:before {
  content: "\f108";
}
.fa-laptop:before {
  content: "\f109";
}
.fa-tablet:before {
  content: "\f10a";
}
.fa-mobile-phone:before,
.fa-mobile:before {
  content: "\f10b";
}
.fa-circle-o:before {
  content: "\f10c";
}
.fa-quote-left:before {
  content: "\f10d";
}
.fa-quote-right:before {
  content: "\f10e";
}
.fa-spinner:before {
  content: "\f110";
}
.fa-circle:before {
  content: "\f111";
}
.fa-mail-reply:before,
.fa-reply:before {
  content: "\f112";
}
.fa-github-alt:before {
  content: "\f113";
}
.fa-folder-o:before {
  content: "\f114";
}
.fa-folder-open-o:before {
  content: "\f115";
}
.fa-smile-o:before {
  content: "\f118";
}
.fa-frown-o:before {
  content: "\f119";
}
.fa-meh-o:before {
  content: "\f11a";
}
.fa-gamepad:before {
  content: "\f11b";
}
.fa-keyboard-o:before {
  content: "\f11c";
}
.fa-flag-o:before {
  content: "\f11d";
}
.fa-flag-checkered:before {
  content: "\f11e";
}
.fa-terminal:before {
  content: "\f120";
}
.fa-code:before {
  content: "\f121";
}
.fa-mail-reply-all:before,
.fa-reply-all:before {
  content: "\f122";
}
.fa-star-half-empty:before,
.fa-star-half-full:before,
.fa-star-half-o:before {
  content: "\f123";
}
.fa-location-arrow:before {
  content: "\f124";
}
.fa-crop:before {
  content: "\f125";
}
.fa-code-fork:before {
  content: "\f126";
}
.fa-unlink:before,
.fa-chain-broken:before {
  content: "\f127";
}
.fa-question:before {
  content: "\f128";
}
.fa-info:before {
  content: "\f129";
}
.fa-exclamation:before {
  content: "\f12a";
}
.fa-superscript:before {
  content: "\f12b";
}
.fa-subscript:before {
  content: "\f12c";
}
.fa-eraser:before {
  content: "\f12d";
}
.fa-puzzle-piece:before {
  content: "\f12e";
}
.fa-microphone:before {
  content: "\f130";
}
.fa-microphone-slash:before {
  content: "\f131";
}
.fa-shield:before {
  content: "\f132";
}
.fa-calendar-o:before {
  content: "\f133";
}
.fa-fire-extinguisher:before {
  content: "\f134";
}
.fa-rocket:before {
  content: "\f135";
}
.fa-maxcdn:before {
  content: "\f136";
}
.fa-chevron-circle-left:before {
  content: "\f137";
}
.fa-chevron-circle-right:before {
  content: "\f138";
}
.fa-chevron-circle-up:before {
  content: "\f139";
}
.fa-chevron-circle-down:before {
  content: "\f13a";
}
.fa-html5:before {
  content: "\f13b";
}
.fa-css3:before {
  content: "\f13c";
}
.fa-anchor:before {
  content: "\f13d";
}
.fa-unlock-alt:before {
  content: "\f13e";
}
.fa-bullseye:before {
  content: "\f140";
}
.fa-ellipsis-h:before {
  content: "\f141";
}
.fa-ellipsis-v:before {
  content: "\f142";
}
.fa-rss-square:before {
  content: "\f143";
}
.fa-play-circle:before {
  content: "\f144";
}
.fa-ticket:before {
  content: "\f145";
}
.fa-minus-square:before {
  content: "\f146";
}
.fa-minus-square-o:before {
  content: "\f147";
}
.fa-level-up:before {
  content: "\f148";
}
.fa-level-down:before {
  content: "\f149";
}
.fa-check-square:before {
  content: "\f14a";
}
.fa-pencil-square:before {
  content: "\f14b";
}
.fa-external-link-square:before {
  content: "\f14c";
}
.fa-share-square:before {
  content: "\f14d";
}
.fa-compass:before {
  content: "\f14e";
}
.fa-toggle-down:before,
.fa-caret-square-o-down:before {
  content: "\f150";
}
.fa-toggle-up:before,
.fa-caret-square-o-up:before {
  content: "\f151";
}
.fa-toggle-right:before,
.fa-caret-square-o-right:before {
  content: "\f152";
}
.fa-euro:before,
.fa-eur:before {
  content: "\f153";
}
.fa-gbp:before {
  content: "\f154";
}
.fa-dollar:before,
.fa-usd:before {
  content: "\f155";
}
.fa-rupee:before,
.fa-inr:before {
  content: "\f156";
}
.fa-cny:before,
.fa-rmb:before,
.fa-yen:before,
.fa-jpy:before {
  content: "\f157";
}
.fa-ruble:before,
.fa-rouble:before,
.fa-rub:before {
  content: "\f158";
}
.fa-won:before,
.fa-krw:before {
  content: "\f159";
}
.fa-bitcoin:before,
.fa-btc:before {
  content: "\f15a";
}
.fa-file:before {
  content: "\f15b";
}
.fa-file-text:before {
  content: "\f15c";
}
.fa-sort-alpha-asc:before {
  content: "\f15d";
}
.fa-sort-alpha-desc:before {
  content: "\f15e";
}
.fa-sort-amount-asc:before {
  content: "\f160";
}
.fa-sort-amount-desc:before {
  content: "\f161";
}
.fa-sort-numeric-asc:before {
  content: "\f162";
}
.fa-sort-numeric-desc:before {
  content: "\f163";
}
.fa-thumbs-up:before {
  content: "\f164";
}
.fa-thumbs-down:before {
  content: "\f165";
}
.fa-youtube-square:before {
  content: "\f166";
}
.fa-youtube:before {
  content: "\f167";
}
.fa-xing:before {
  content: "\f168";
}
.fa-xing-square:before {
  content: "\f169";
}
.fa-youtube-play:before {
  content: "\f16a";
}
.fa-dropbox:before {
  content: "\f16b";
}
.fa-stack-overflow:before {
  content: "\f16c";
}
.fa-instagram:before {
  content: "\f16d";
}
.fa-flickr:before {
  content: "\f16e";
}
.fa-adn:before {
  content: "\f170";
}
.fa-bitbucket:before {
  content: "\f171";
}
.fa-bitbucket-square:before {
  content: "\f172";
}
.fa-tumblr:before {
  content: "\f173";
}
.fa-tumblr-square:before {
  content: "\f174";
}
.fa-long-arrow-down:before {
  content: "\f175";
}
.fa-long-arrow-up:before {
  content: "\f176";
}
.fa-long-arrow-left:before {
  content: "\f177";
}
.fa-long-arrow-right:before {
  content: "\f178";
}
.fa-apple:before {
  content: "\f179";
}
.fa-windows:before {
  content: "\f17a";
}
.fa-android:before {
  content: "\f17b";
}
.fa-linux:before {
  content: "\f17c";
}
.fa-dribbble:before {
  content: "\f17d";
}
.fa-skype:before {
  content: "\f17e";
}
.fa-foursquare:before {
  content: "\f180";
}
.fa-trello:before {
  content: "\f181";
}
.fa-female:before {
  content: "\f182";
}
.fa-male:before {
  content: "\f183";
}
.fa-gittip:before {
  content: "\f184";
}
.fa-sun-o:before {
  content: "\f185";
}
.fa-moon-o:before {
  content: "\f186";
}
.fa-archive:before {
  content: "\f187";
}
.fa-bug:before {
  content: "\f188";
}
.fa-vk:before {
  content: "\f189";
}
.fa-weibo:before {
  content: "\f18a";
}
.fa-renren:before {
  content: "\f18b";
}
.fa-pagelines:before {
  content: "\f18c";
}
.fa-stack-exchange:before {
  content: "\f18d";
}
.fa-arrow-circle-o-right:before {
  content: "\f18e";
}
.fa-arrow-circle-o-left:before {
  content: "\f190";
}
.fa-toggle-left:before,
.fa-caret-square-o-left:before {
  content: "\f191";
}
.fa-dot-circle-o:before {
  content: "\f192";
}
.fa-wheelchair:before {
  content: "\f193";
}
.fa-vimeo-square:before {
  content: "\f194";
}
.fa-turkish-lira:before,
.fa-try:before {
  content: "\f195";
}
.fa-plus-square-o:before {
  content: "\f196";
}
.fa-space-shuttle:before {
  content: "\f197";
}
.fa-slack:before {
  content: "\f198";
}
.fa-envelope-square:before {
  content: "\f199";
}
.fa-wordpress:before {
  content: "\f19a";
}
.fa-openid:before {
  content: "\f19b";
}
.fa-institution:before,
.fa-bank:before,
.fa-university:before {
  content: "\f19c";
}
.fa-mortar-board:before,
.fa-graduation-cap:before {
  content: "\f19d";
}
.fa-yahoo:before {
  content: "\f19e";
}
.fa-google:before {
  content: "\f1a0";
}
.fa-reddit:before {
  content: "\f1a1";
}
.fa-reddit-square:before {
  content: "\f1a2";
}
.fa-stumbleupon-circle:before {
  content: "\f1a3";
}
.fa-stumbleupon:before {
  content: "\f1a4";
}
.fa-delicious:before {
  content: "\f1a5";
}
.fa-digg:before {
  content: "\f1a6";
}
.fa-pied-piper:before {
  content: "\f1a7";
}
.fa-pied-piper-alt:before {
  content: "\f1a8";
}
.fa-drupal:before {
  content: "\f1a9";
}
.fa-joomla:before {
  content: "\f1aa";
}
.fa-language:before {
  content: "\f1ab";
}
.fa-fax:before {
  content: "\f1ac";
}
.fa-building:before {
  content: "\f1ad";
}
.fa-child:before {
  content: "\f1ae";
}
.fa-paw:before {
  content: "\f1b0";
}
.fa-spoon:before {
  content: "\f1b1";
}
.fa-cube:before {
  content: "\f1b2";
}
.fa-cubes:before {
  content: "\f1b3";
}
.fa-behance:before {
  content: "\f1b4";
}
.fa-behance-square:before {
  content: "\f1b5";
}
.fa-steam:before {
  content: "\f1b6";
}
.fa-steam-square:before {
  content: "\f1b7";
}
.fa-recycle:before {
  content: "\f1b8";
}
.fa-automobile:before,
.fa-car:before {
  content: "\f1b9";
}
.fa-cab:before,
.fa-taxi:before {
  content: "\f1ba";
}
.fa-tree:before {
  content: "\f1bb";
}
.fa-spotify:before {
  content: "\f1bc";
}
.fa-deviantart:before {
  content: "\f1bd";
}
.fa-soundcloud:before {
  content: "\f1be";
}
.fa-database:before {
  content: "\f1c0";
}
.fa-file-pdf-o:before {
  content: "\f1c1";
}
.fa-file-word-o:before {
  content: "\f1c2";
}
.fa-file-excel-o:before {
  content: "\f1c3";
}
.fa-file-powerpoint-o:before {
  content: "\f1c4";
}
.fa-file-photo-o:before,
.fa-file-picture-o:before,
.fa-file-image-o:before {
  content: "\f1c5";
}
.fa-file-zip-o:before,
.fa-file-archive-o:before {
  content: "\f1c6";
}
.fa-file-sound-o:before,
.fa-file-audio-o:before {
  content: "\f1c7";
}
.fa-file-movie-o:before,
.fa-file-video-o:before {
  content: "\f1c8";
}
.fa-file-code-o:before {
  content: "\f1c9";
}
.fa-vine:before {
  content: "\f1ca";
}
.fa-codepen:before {
  content: "\f1cb";
}
.fa-jsfiddle:before {
  content: "\f1cc";
}
.fa-life-bouy:before,
.fa-life-buoy:before,
.fa-life-saver:before,
.fa-support:before,
.fa-life-ring:before {
  content: "\f1cd";
}
.fa-circle-o-notch:before {
  content: "\f1ce";
}
.fa-ra:before,
.fa-rebel:before {
  content: "\f1d0";
}
.fa-ge:before,
.fa-empire:before {
  content: "\f1d1";
}
.fa-git-square:before {
  content: "\f1d2";
}
.fa-git:before {
  content: "\f1d3";
}
.fa-hacker-news:before {
  content: "\f1d4";
}
.fa-tencent-weibo:before {
  content: "\f1d5";
}
.fa-qq:before {
  content: "\f1d6";
}
.fa-wechat:before,
.fa-weixin:before {
  content: "\f1d7";
}
.fa-send:before,
.fa-paper-plane:before {
  content: "\f1d8";
}
.fa-send-o:before,
.fa-paper-plane-o:before {
  content: "\f1d9";
}
.fa-history:before {
  content: "\f1da";
}
.fa-circle-thin:before {
  content: "\f1db";
}
.fa-header:before {
  content: "\f1dc";
}
.fa-paragraph:before {
  content: "\f1dd";
}
.fa-sliders:before {
  content: "\f1de";
}
.fa-share-alt:before {
  content: "\f1e0";
}
.fa-share-alt-square:before {
  content: "\f1e1";
}
.fa-bomb:before {
  content: "\f1e2";
}
.fa-soccer-ball-o:before,
.fa-futbol-o:before {
  content: "\f1e3";
}
.fa-tty:before {
  content: "\f1e4";
}
.fa-binoculars:before {
  content: "\f1e5";
}
.fa-plug:before {
  content: "\f1e6";
}
.fa-slideshare:before {
  content: "\f1e7";
}
.fa-twitch:before {
  content: "\f1e8";
}
.fa-yelp:before {
  content: "\f1e9";
}
.fa-newspaper-o:before {
  content: "\f1ea";
}
.fa-wifi:before {
  content: "\f1eb";
}
.fa-calculator:before {
  content: "\f1ec";
}
.fa-paypal:before {
  content: "\f1ed";
}
.fa-google-wallet:before {
  content: "\f1ee";
}
.fa-cc-visa:before {
  content: "\f1f0";
}
.fa-cc-mastercard:before {
  content: "\f1f1";
}
.fa-cc-discover:before {
  content: "\f1f2";
}
.fa-cc-amex:before {
  content: "\f1f3";
}
.fa-cc-paypal:before {
  content: "\f1f4";
}
.fa-cc-stripe:before {
  content: "\f1f5";
}
.fa-bell-slash:before {
  content: "\f1f6";
}
.fa-bell-slash-o:before {
  content: "\f1f7";
}
.fa-trash:before {
  content: "\f1f8";
}
.fa-copyright:before {
  content: "\f1f9";
}
.fa-at:before {
  content: "\f1fa";
}
.fa-eyedropper:before {
  content: "\f1fb";
}
.fa-paint-brush:before {
  content: "\f1fc";
}
.fa-birthday-cake:before {
  content: "\f1fd";
}
.fa-area-chart:before {
  content: "\f1fe";
}
.fa-pie-chart:before {
  content: "\f200";
}
.fa-line-chart:before {
  content: "\f201";
}
.fa-lastfm:before {
  content: "\f202";
}
.fa-lastfm-square:before {
  content: "\f203";
}
.fa-toggle-off:before {
  content: "\f204";
}
.fa-toggle-on:before {
  content: "\f205";
}
.fa-bicycle:before {
  content: "\f206";
}
.fa-bus:before {
  content: "\f207";
}
.fa-ioxhost:before {
  content: "\f208";
}
.fa-angellist:before {
  content: "\f209";
}
.fa-cc:before {
  content: "\f20a";
}
.fa-shekel:before,
.fa-sheqel:before,
.fa-ils:before {
  content: "\f20b";
}
.fa-meanpath:before {
  content: "\f20c";
}
/*!
*
* IPython base
*
*/
.modal.fade .modal-dialog {
  -webkit-transform: translate(0, 0);
  -ms-transform: translate(0, 0);
  -o-transform: translate(0, 0);
  transform: translate(0, 0);
}
code {
  color: #000;
}
pre {
  font-size: inherit;
  line-height: inherit;
}
label {
  font-weight: normal;
}
/* Make the page background atleast 100% the height of the view port */
/* Make the page itself atleast 70% the height of the view port */
.border-box-sizing {
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
.corner-all {
  border-radius: 2px;
}
.no-padding {
  padding: 0px;
}
/* Flexible box model classes */
/* Taken from Alex Russell http://infrequently.org/2009/08/css-3-progress/ */
/* This file is a compatability layer.  It allows the usage of flexible box 
model layouts accross multiple browsers, including older browsers.  The newest,
universal implementation of the flexible box model is used when available (see
`Modern browsers` comments below).  Browsers that are known to implement this 
new spec completely include:

    Firefox 28.0+
    Chrome 29.0+
    Internet Explorer 11+ 
    Opera 17.0+

Browsers not listed, including Safari, are supported via the styling under the
`Old browsers` comments below.
*/
.hbox {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
.hbox > * {
  /* Old browsers */
  -webkit-box-flex: 0;
  -moz-box-flex: 0;
  box-flex: 0;
  /* Modern browsers */
  flex: none;
}
.vbox {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
}
.vbox > * {
  /* Old browsers */
  -webkit-box-flex: 0;
  -moz-box-flex: 0;
  box-flex: 0;
  /* Modern browsers */
  flex: none;
}
.hbox.reverse,
.vbox.reverse,
.reverse {
  /* Old browsers */
  -webkit-box-direction: reverse;
  -moz-box-direction: reverse;
  box-direction: reverse;
  /* Modern browsers */
  flex-direction: row-reverse;
}
.hbox.box-flex0,
.vbox.box-flex0,
.box-flex0 {
  /* Old browsers */
  -webkit-box-flex: 0;
  -moz-box-flex: 0;
  box-flex: 0;
  /* Modern browsers */
  flex: none;
  width: auto;
}
.hbox.box-flex1,
.vbox.box-flex1,
.box-flex1 {
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
.hbox.box-flex,
.vbox.box-flex,
.box-flex {
  /* Old browsers */
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
.hbox.box-flex2,
.vbox.box-flex2,
.box-flex2 {
  /* Old browsers */
  -webkit-box-flex: 2;
  -moz-box-flex: 2;
  box-flex: 2;
  /* Modern browsers */
  flex: 2;
}
.box-group1 {
  /*  Deprecated */
  -webkit-box-flex-group: 1;
  -moz-box-flex-group: 1;
  box-flex-group: 1;
}
.box-group2 {
  /* Deprecated */
  -webkit-box-flex-group: 2;
  -moz-box-flex-group: 2;
  box-flex-group: 2;
}
.hbox.start,
.vbox.start,
.start {
  /* Old browsers */
  -webkit-box-pack: start;
  -moz-box-pack: start;
  box-pack: start;
  /* Modern browsers */
  justify-content: flex-start;
}
.hbox.end,
.vbox.end,
.end {
  /* Old browsers */
  -webkit-box-pack: end;
  -moz-box-pack: end;
  box-pack: end;
  /* Modern browsers */
  justify-content: flex-end;
}
.hbox.center,
.vbox.center,
.center {
  /* Old browsers */
  -webkit-box-pack: center;
  -moz-box-pack: center;
  box-pack: center;
  /* Modern browsers */
  justify-content: center;
}
.hbox.baseline,
.vbox.baseline,
.baseline {
  /* Old browsers */
  -webkit-box-pack: baseline;
  -moz-box-pack: baseline;
  box-pack: baseline;
  /* Modern browsers */
  justify-content: baseline;
}
.hbox.stretch,
.vbox.stretch,
.stretch {
  /* Old browsers */
  -webkit-box-pack: stretch;
  -moz-box-pack: stretch;
  box-pack: stretch;
  /* Modern browsers */
  justify-content: stretch;
}
.hbox.align-start,
.vbox.align-start,
.align-start {
  /* Old browsers */
  -webkit-box-align: start;
  -moz-box-align: start;
  box-align: start;
  /* Modern browsers */
  align-items: flex-start;
}
.hbox.align-end,
.vbox.align-end,
.align-end {
  /* Old browsers */
  -webkit-box-align: end;
  -moz-box-align: end;
  box-align: end;
  /* Modern browsers */
  align-items: flex-end;
}
.hbox.align-center,
.vbox.align-center,
.align-center {
  /* Old browsers */
  -webkit-box-align: center;
  -moz-box-align: center;
  box-align: center;
  /* Modern browsers */
  align-items: center;
}
.hbox.align-baseline,
.vbox.align-baseline,
.align-baseline {
  /* Old browsers */
  -webkit-box-align: baseline;
  -moz-box-align: baseline;
  box-align: baseline;
  /* Modern browsers */
  align-items: baseline;
}
.hbox.align-stretch,
.vbox.align-stretch,
.align-stretch {
  /* Old browsers */
  -webkit-box-align: stretch;
  -moz-box-align: stretch;
  box-align: stretch;
  /* Modern browsers */
  align-items: stretch;
}
div.error {
  margin: 2em;
  text-align: center;
}
div.error > h1 {
  font-size: 500%;
  line-height: normal;
}
div.error > p {
  font-size: 200%;
  line-height: normal;
}
div.traceback-wrapper {
  text-align: left;
  max-width: 800px;
  margin: auto;
}
/**
 * Primary styles
 *
 * Author: Jupyter Development Team
 */
body {
  background-color: #fff;
  /* This makes sure that the body covers the entire window and needs to
       be in a different element than the display: box in wrapper below */
  position: absolute;
  left: 0px;
  right: 0px;
  top: 0px;
  bottom: 0px;
  overflow: visible;
}
body > #header {
  /* Initially hidden to prevent FLOUC */
  display: none;
  background-color: #fff;
  /* Display over codemirror */
  position: relative;
  z-index: 100;
}
body > #header #header-container {
  padding-bottom: 5px;
  padding-top: 5px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
body > #header .header-bar {
  width: 100%;
  height: 1px;
  background: #e7e7e7;
  margin-bottom: -1px;
}
@media print {
  body > #header {
    display: none !important;
  }
}
#header-spacer {
  width: 100%;
  visibility: hidden;
}
@media print {
  #header-spacer {
    display: none;
  }
}
#ipython_notebook {
  padding-left: 0px;
  padding-top: 1px;
  padding-bottom: 1px;
}
@media (max-width: 991px) {
  #ipython_notebook {
    margin-left: 10px;
  }
}
[dir="rtl"] #ipython_notebook {
  float: right !important;
}
#noscript {
  width: auto;
  padding-top: 16px;
  padding-bottom: 16px;
  text-align: center;
  font-size: 22px;
  color: red;
  font-weight: bold;
}
#ipython_notebook img {
  height: 28px;
}
#site {
  width: 100%;
  display: none;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  overflow: auto;
}
@media print {
  #site {
    height: auto !important;
  }
}
/* Smaller buttons */
.ui-button .ui-button-text {
  padding: 0.2em 0.8em;
  font-size: 77%;
}
input.ui-button {
  padding: 0.3em 0.9em;
}
span#login_widget {
  float: right;
}
span#login_widget > .button,
#logout {
  color: #333;
  background-color: #fff;
  border-color: #ccc;
}
span#login_widget > .button:focus,
#logout:focus,
span#login_widget > .button.focus,
#logout.focus {
  color: #333;
  background-color: #e6e6e6;
  border-color: #8c8c8c;
}
span#login_widget > .button:hover,
#logout:hover {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
span#login_widget > .button:active,
#logout:active,
span#login_widget > .button.active,
#logout.active,
.open > .dropdown-togglespan#login_widget > .button,
.open > .dropdown-toggle#logout {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
span#login_widget > .button:active:hover,
#logout:active:hover,
span#login_widget > .button.active:hover,
#logout.active:hover,
.open > .dropdown-togglespan#login_widget > .button:hover,
.open > .dropdown-toggle#logout:hover,
span#login_widget > .button:active:focus,
#logout:active:focus,
span#login_widget > .button.active:focus,
#logout.active:focus,
.open > .dropdown-togglespan#login_widget > .button:focus,
.open > .dropdown-toggle#logout:focus,
span#login_widget > .button:active.focus,
#logout:active.focus,
span#login_widget > .button.active.focus,
#logout.active.focus,
.open > .dropdown-togglespan#login_widget > .button.focus,
.open > .dropdown-toggle#logout.focus {
  color: #333;
  background-color: #d4d4d4;
  border-color: #8c8c8c;
}
span#login_widget > .button:active,
#logout:active,
span#login_widget > .button.active,
#logout.active,
.open > .dropdown-togglespan#login_widget > .button,
.open > .dropdown-toggle#logout {
  background-image: none;
}
span#login_widget > .button.disabled:hover,
#logout.disabled:hover,
span#login_widget > .button[disabled]:hover,
#logout[disabled]:hover,
fieldset[disabled] span#login_widget > .button:hover,
fieldset[disabled] #logout:hover,
span#login_widget > .button.disabled:focus,
#logout.disabled:focus,
span#login_widget > .button[disabled]:focus,
#logout[disabled]:focus,
fieldset[disabled] span#login_widget > .button:focus,
fieldset[disabled] #logout:focus,
span#login_widget > .button.disabled.focus,
#logout.disabled.focus,
span#login_widget > .button[disabled].focus,
#logout[disabled].focus,
fieldset[disabled] span#login_widget > .button.focus,
fieldset[disabled] #logout.focus {
  background-color: #fff;
  border-color: #ccc;
}
span#login_widget > .button .badge,
#logout .badge {
  color: #fff;
  background-color: #333;
}
.nav-header {
  text-transform: none;
}
#header > span {
  margin-top: 10px;
}
.modal_stretch .modal-dialog {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  min-height: 80vh;
}
.modal_stretch .modal-dialog .modal-body {
  max-height: calc(100vh - 200px);
  overflow: auto;
  flex: 1;
}
@media (min-width: 768px) {
  .modal .modal-dialog {
    width: 700px;
  }
}
@media (min-width: 768px) {
  select.form-control {
    margin-left: 12px;
    margin-right: 12px;
  }
}
/*!
*
* IPython auth
*
*/
.center-nav {
  display: inline-block;
  margin-bottom: -4px;
}
/*!
*
* IPython tree view
*
*/
/* We need an invisible input field on top of the sentense*/
/* "Drag file onto the list ..." */
.alternate_upload {
  background-color: none;
  display: inline;
}
.alternate_upload.form {
  padding: 0;
  margin: 0;
}
.alternate_upload input.fileinput {
  text-align: center;
  vertical-align: middle;
  display: inline;
  opacity: 0;
  z-index: 2;
  width: 12ex;
  margin-right: -12ex;
}
.alternate_upload .btn-upload {
  height: 22px;
}
/**
 * Primary styles
 *
 * Author: Jupyter Development Team
 */
[dir="rtl"] #tabs li {
  float: right;
}
ul#tabs {
  margin-bottom: 4px;
}
[dir="rtl"] ul#tabs {
  margin-right: 0px;
}
ul#tabs a {
  padding-top: 6px;
  padding-bottom: 4px;
}
ul.breadcrumb a:focus,
ul.breadcrumb a:hover {
  text-decoration: none;
}
ul.breadcrumb i.icon-home {
  font-size: 16px;
  margin-right: 4px;
}
ul.breadcrumb span {
  color: #5e5e5e;
}
.list_toolbar {
  padding: 4px 0 4px 0;
  vertical-align: middle;
}
.list_toolbar .tree-buttons {
  padding-top: 1px;
}
[dir="rtl"] .list_toolbar .tree-buttons {
  float: left !important;
}
[dir="rtl"] .list_toolbar .pull-right {
  padding-top: 1px;
  float: left !important;
}
[dir="rtl"] .list_toolbar .pull-left {
  float: right !important;
}
.dynamic-buttons {
  padding-top: 3px;
  display: inline-block;
}
.list_toolbar [class*="span"] {
  min-height: 24px;
}
.list_header {
  font-weight: bold;
  background-color: #EEE;
}
.list_placeholder {
  font-weight: bold;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 7px;
  padding-right: 7px;
}
.list_container {
  margin-top: 4px;
  margin-bottom: 20px;
  border: 1px solid #ddd;
  border-radius: 2px;
}
.list_container > div {
  border-bottom: 1px solid #ddd;
}
.list_container > div:hover .list-item {
  background-color: red;
}
.list_container > div:last-child {
  border: none;
}
.list_item:hover .list_item {
  background-color: #ddd;
}
.list_item a {
  text-decoration: none;
}
.list_item:hover {
  background-color: #fafafa;
}
.list_header > div,
.list_item > div {
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 7px;
  padding-right: 7px;
  line-height: 22px;
}
.list_header > div input,
.list_item > div input {
  margin-right: 7px;
  margin-left: 14px;
  vertical-align: baseline;
  line-height: 22px;
  position: relative;
  top: -1px;
}
.list_header > div .item_link,
.list_item > div .item_link {
  margin-left: -1px;
  vertical-align: baseline;
  line-height: 22px;
}
.new-file input[type=checkbox] {
  visibility: hidden;
}
.item_name {
  line-height: 22px;
  height: 24px;
}
.item_icon {
  font-size: 14px;
  color: #5e5e5e;
  margin-right: 7px;
  margin-left: 7px;
  line-height: 22px;
  vertical-align: baseline;
}
.item_buttons {
  line-height: 1em;
  margin-left: -5px;
}
.item_buttons .btn,
.item_buttons .btn-group,
.item_buttons .input-group {
  float: left;
}
.item_buttons > .btn,
.item_buttons > .btn-group,
.item_buttons > .input-group {
  margin-left: 5px;
}
.item_buttons .btn {
  min-width: 13ex;
}
.item_buttons .running-indicator {
  padding-top: 4px;
  color: #5cb85c;
}
.item_buttons .kernel-name {
  padding-top: 4px;
  color: #5bc0de;
  margin-right: 7px;
  float: left;
}
.toolbar_info {
  height: 24px;
  line-height: 24px;
}
.list_item input:not([type=checkbox]) {
  padding-top: 3px;
  padding-bottom: 3px;
  height: 22px;
  line-height: 14px;
  margin: 0px;
}
.highlight_text {
  color: blue;
}
#project_name {
  display: inline-block;
  padding-left: 7px;
  margin-left: -2px;
}
#project_name > .breadcrumb {
  padding: 0px;
  margin-bottom: 0px;
  background-color: transparent;
  font-weight: bold;
}
#tree-selector {
  padding-right: 0px;
}
[dir="rtl"] #tree-selector a {
  float: right;
}
#button-select-all {
  min-width: 50px;
}
#select-all {
  margin-left: 7px;
  margin-right: 2px;
}
.menu_icon {
  margin-right: 2px;
}
.tab-content .row {
  margin-left: 0px;
  margin-right: 0px;
}
.folder_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f114";
}
.folder_icon:before.pull-left {
  margin-right: .3em;
}
.folder_icon:before.pull-right {
  margin-left: .3em;
}
.notebook_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f02d";
  position: relative;
  top: -1px;
}
.notebook_icon:before.pull-left {
  margin-right: .3em;
}
.notebook_icon:before.pull-right {
  margin-left: .3em;
}
.running_notebook_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f02d";
  position: relative;
  top: -1px;
  color: #5cb85c;
}
.running_notebook_icon:before.pull-left {
  margin-right: .3em;
}
.running_notebook_icon:before.pull-right {
  margin-left: .3em;
}
.file_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f016";
  position: relative;
  top: -2px;
}
.file_icon:before.pull-left {
  margin-right: .3em;
}
.file_icon:before.pull-right {
  margin-left: .3em;
}
#notebook_toolbar .pull-right {
  padding-top: 0px;
  margin-right: -1px;
}
ul#new-menu {
  left: auto;
  right: 0;
}
[dir="rtl"] #new-menu {
  text-align: right;
}
.kernel-menu-icon {
  padding-right: 12px;
  width: 24px;
  content: "\f096";
}
.kernel-menu-icon:before {
  content: "\f096";
}
.kernel-menu-icon-current:before {
  content: "\f00c";
}
#tab_content {
  padding-top: 20px;
}
#running .panel-group .panel {
  margin-top: 3px;
  margin-bottom: 1em;
}
#running .panel-group .panel .panel-heading {
  background-color: #EEE;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 7px;
  padding-right: 7px;
  line-height: 22px;
}
#running .panel-group .panel .panel-heading a:focus,
#running .panel-group .panel .panel-heading a:hover {
  text-decoration: none;
}
#running .panel-group .panel .panel-body {
  padding: 0px;
}
#running .panel-group .panel .panel-body .list_container {
  margin-top: 0px;
  margin-bottom: 0px;
  border: 0px;
  border-radius: 0px;
}
#running .panel-group .panel .panel-body .list_container .list_item {
  border-bottom: 1px solid #ddd;
}
#running .panel-group .panel .panel-body .list_container .list_item:last-child {
  border-bottom: 0px;
}
[dir="rtl"] #running .col-sm-8 {
  float: right !important;
}
.delete-button {
  display: none;
}
.duplicate-button {
  display: none;
}
.rename-button {
  display: none;
}
.shutdown-button {
  display: none;
}
.dynamic-instructions {
  display: inline-block;
  padding-top: 4px;
}
/*!
*
* IPython text editor webapp
*
*/
.selected-keymap i.fa {
  padding: 0px 5px;
}
.selected-keymap i.fa:before {
  content: "\f00c";
}
#mode-menu {
  overflow: auto;
  max-height: 20em;
}
.edit_app #header {
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
}
.edit_app #menubar .navbar {
  /* Use a negative 1 bottom margin, so the border overlaps the border of the
    header */
  margin-bottom: -1px;
}
.dirty-indicator {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 20px;
}
.dirty-indicator.pull-left {
  margin-right: .3em;
}
.dirty-indicator.pull-right {
  margin-left: .3em;
}
.dirty-indicator-dirty {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 20px;
}
.dirty-indicator-dirty.pull-left {
  margin-right: .3em;
}
.dirty-indicator-dirty.pull-right {
  margin-left: .3em;
}
.dirty-indicator-clean {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 20px;
}
.dirty-indicator-clean.pull-left {
  margin-right: .3em;
}
.dirty-indicator-clean.pull-right {
  margin-left: .3em;
}
.dirty-indicator-clean:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f00c";
}
.dirty-indicator-clean:before.pull-left {
  margin-right: .3em;
}
.dirty-indicator-clean:before.pull-right {
  margin-left: .3em;
}
#filename {
  font-size: 16pt;
  display: table;
  padding: 0px 5px;
}
#current-mode {
  padding-left: 5px;
  padding-right: 5px;
}
#texteditor-backdrop {
  padding-top: 20px;
  padding-bottom: 20px;
}
@media not print {
  #texteditor-backdrop {
    background-color: #EEE;
  }
}
@media print {
  #texteditor-backdrop #texteditor-container .CodeMirror-gutter,
  #texteditor-backdrop #texteditor-container .CodeMirror-gutters {
    background-color: #fff;
  }
}
@media not print {
  #texteditor-backdrop #texteditor-container .CodeMirror-gutter,
  #texteditor-backdrop #texteditor-container .CodeMirror-gutters {
    background-color: #fff;
  }
}
@media not print {
  #texteditor-backdrop #texteditor-container {
    padding: 0px;
    background-color: #fff;
    -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
    box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  }
}
/*!
*
* IPython notebook
*
*/
/* CSS font colors for translated ANSI colors. */
.ansibold {
  font-weight: bold;
}
/* use dark versions for foreground, to improve visibility */
.ansiblack {
  color: black;
}
.ansired {
  color: darkred;
}
.ansigreen {
  color: darkgreen;
}
.ansiyellow {
  color: #c4a000;
}
.ansiblue {
  color: darkblue;
}
.ansipurple {
  color: darkviolet;
}
.ansicyan {
  color: steelblue;
}
.ansigray {
  color: gray;
}
/* and light for background, for the same reason */
.ansibgblack {
  background-color: black;
}
.ansibgred {
  background-color: red;
}
.ansibggreen {
  background-color: green;
}
.ansibgyellow {
  background-color: yellow;
}
.ansibgblue {
  background-color: blue;
}
.ansibgpurple {
  background-color: magenta;
}
.ansibgcyan {
  background-color: cyan;
}
.ansibggray {
  background-color: gray;
}
div.cell {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  border-radius: 2px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  border-width: 1px;
  border-style: solid;
  border-color: transparent;
  width: 100%;
  padding: 5px;
  /* This acts as a spacer between cells, that is outside the border */
  margin: 0px;
  outline: none;
  border-left-width: 1px;
  padding-left: 5px;
  background: linear-gradient(to right, transparent -40px, transparent 1px, transparent 1px, transparent 100%);
}
div.cell.jupyter-soft-selected {
  border-left-color: #90CAF9;
  border-left-color: #E3F2FD;
  border-left-width: 1px;
  padding-left: 5px;
  border-right-color: #E3F2FD;
  border-right-width: 1px;
  background: #E3F2FD;
}
@media print {
  div.cell.jupyter-soft-selected {
    border-color: transparent;
  }
}
div.cell.selected {
  border-color: #ababab;
  border-left-width: 0px;
  padding-left: 6px;
  background: linear-gradient(to right, #42A5F5 -40px, #42A5F5 5px, transparent 5px, transparent 100%);
}
@media print {
  div.cell.selected {
    border-color: transparent;
  }
}
div.cell.selected.jupyter-soft-selected {
  border-left-width: 0;
  padding-left: 6px;
  background: linear-gradient(to right, #42A5F5 -40px, #42A5F5 7px, #E3F2FD 7px, #E3F2FD 100%);
}
.edit_mode div.cell.selected {
  border-color: #66BB6A;
  border-left-width: 0px;
  padding-left: 6px;
  background: linear-gradient(to right, #66BB6A -40px, #66BB6A 5px, transparent 5px, transparent 100%);
}
@media print {
  .edit_mode div.cell.selected {
    border-color: transparent;
  }
}
.prompt {
  /* This needs to be wide enough for 3 digit prompt numbers: In[100]: */
  min-width: 14ex;
  /* This padding is tuned to match the padding on the CodeMirror editor. */
  padding: 0.4em;
  margin: 0px;
  font-family: monospace;
  text-align: right;
  /* This has to match that of the the CodeMirror class line-height below */
  line-height: 1.21429em;
  /* Don't highlight prompt number selection */
  -webkit-touch-callout: none;
  -webkit-user-select: none;
  -khtml-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
  /* Use default cursor */
  cursor: default;
}
@media (max-width: 540px) {
  .prompt {
    text-align: left;
  }
}
div.inner_cell {
  min-width: 0;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
/* input_area and input_prompt must match in top border and margin for alignment */
div.input_area {
  border: 1px solid #cfcfcf;
  border-radius: 2px;
  background: #f7f7f7;
  line-height: 1.21429em;
}
/* This is needed so that empty prompt areas can collapse to zero height when there
   is no content in the output_subarea and the prompt. The main purpose of this is
   to make sure that empty JavaScript output_subareas have no height. */
div.prompt:empty {
  padding-top: 0;
  padding-bottom: 0;
}
div.unrecognized_cell {
  padding: 5px 5px 5px 0px;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
div.unrecognized_cell .inner_cell {
  border-radius: 2px;
  padding: 5px;
  font-weight: bold;
  color: red;
  border: 1px solid #cfcfcf;
  background: #eaeaea;
}
div.unrecognized_cell .inner_cell a {
  color: inherit;
  text-decoration: none;
}
div.unrecognized_cell .inner_cell a:hover {
  color: inherit;
  text-decoration: none;
}
@media (max-width: 540px) {
  div.unrecognized_cell > div.prompt {
    display: none;
  }
}
div.code_cell {
  /* avoid page breaking on code cells when printing */
}
@media print {
  div.code_cell {
    page-break-inside: avoid;
  }
}
/* any special styling for code cells that are currently running goes here */
div.input {
  page-break-inside: avoid;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
@media (max-width: 540px) {
  div.input {
    /* Old browsers */
    display: -webkit-box;
    -webkit-box-orient: vertical;
    -webkit-box-align: stretch;
    display: -moz-box;
    -moz-box-orient: vertical;
    -moz-box-align: stretch;
    display: box;
    box-orient: vertical;
    box-align: stretch;
    /* Modern browsers */
    display: flex;
    flex-direction: column;
    align-items: stretch;
  }
}
/* input_area and input_prompt must match in top border and margin for alignment */
div.input_prompt {
  color: #303F9F;
  border-top: 1px solid transparent;
}
div.input_area > div.highlight {
  margin: 0.4em;
  border: none;
  padding: 0px;
  background-color: transparent;
}
div.input_area > div.highlight > pre {
  margin: 0px;
  border: none;
  padding: 0px;
  background-color: transparent;
}
/* The following gets added to the <head> if it is detected that the user has a
 * monospace font with inconsistent normal/bold/italic height.  See
 * notebookmain.js.  Such fonts will have keywords vertically offset with
 * respect to the rest of the text.  The user should select a better font.
 * See: https://github.com/ipython/ipython/issues/1503
 *
 * .CodeMirror span {
 *      vertical-align: bottom;
 * }
 */
.CodeMirror {
  line-height: 1.21429em;
  /* Changed from 1em to our global default */
  font-size: 14px;
  height: auto;
  /* Changed to auto to autogrow */
  background: none;
  /* Changed from white to allow our bg to show through */
}
.CodeMirror-scroll {
  /*  The CodeMirror docs are a bit fuzzy on if overflow-y should be hidden or visible.*/
  /*  We have found that if it is visible, vertical scrollbars appear with font size changes.*/
  overflow-y: hidden;
  overflow-x: auto;
}
.CodeMirror-lines {
  /* In CM2, this used to be 0.4em, but in CM3 it went to 4px. We need the em value because */
  /* we have set a different line-height and want this to scale with that. */
  padding: 0.4em;
}
.CodeMirror-linenumber {
  padding: 0 8px 0 4px;
}
.CodeMirror-gutters {
  border-bottom-left-radius: 2px;
  border-top-left-radius: 2px;
}
.CodeMirror pre {
  /* In CM3 this went to 4px from 0 in CM2. We need the 0 value because of how we size */
  /* .CodeMirror-lines */
  padding: 0;
  border: 0;
  border-radius: 0;
}
/*

Original style from softwaremaniacs.org (c) Ivan Sagalaev <Maniac@SoftwareManiacs.Org>
Adapted from GitHub theme

*/
.highlight-base {
  color: #000;
}
.highlight-variable {
  color: #000;
}
.highlight-variable-2 {
  color: #1a1a1a;
}
.highlight-variable-3 {
  color: #333333;
}
.highlight-string {
  color: #BA2121;
}
.highlight-comment {
  color: #408080;
  font-style: italic;
}
.highlight-number {
  color: #080;
}
.highlight-atom {
  color: #88F;
}
.highlight-keyword {
  color: #008000;
  font-weight: bold;
}
.highlight-builtin {
  color: #008000;
}
.highlight-error {
  color: #f00;
}
.highlight-operator {
  color: #AA22FF;
  font-weight: bold;
}
.highlight-meta {
  color: #AA22FF;
}
/* previously not defined, copying from default codemirror */
.highlight-def {
  color: #00f;
}
.highlight-string-2 {
  color: #f50;
}
.highlight-qualifier {
  color: #555;
}
.highlight-bracket {
  color: #997;
}
.highlight-tag {
  color: #170;
}
.highlight-attribute {
  color: #00c;
}
.highlight-header {
  color: blue;
}
.highlight-quote {
  color: #090;
}
.highlight-link {
  color: #00c;
}
/* apply the same style to codemirror */
.cm-s-ipython span.cm-keyword {
  color: #008000;
  font-weight: bold;
}
.cm-s-ipython span.cm-atom {
  color: #88F;
}
.cm-s-ipython span.cm-number {
  color: #080;
}
.cm-s-ipython span.cm-def {
  color: #00f;
}
.cm-s-ipython span.cm-variable {
  color: #000;
}
.cm-s-ipython span.cm-operator {
  color: #AA22FF;
  font-weight: bold;
}
.cm-s-ipython span.cm-variable-2 {
  color: #1a1a1a;
}
.cm-s-ipython span.cm-variable-3 {
  color: #333333;
}
.cm-s-ipython span.cm-comment {
  color: #408080;
  font-style: italic;
}
.cm-s-ipython span.cm-string {
  color: #BA2121;
}
.cm-s-ipython span.cm-string-2 {
  color: #f50;
}
.cm-s-ipython span.cm-meta {
  color: #AA22FF;
}
.cm-s-ipython span.cm-qualifier {
  color: #555;
}
.cm-s-ipython span.cm-builtin {
  color: #008000;
}
.cm-s-ipython span.cm-bracket {
  color: #997;
}
.cm-s-ipython span.cm-tag {
  color: #170;
}
.cm-s-ipython span.cm-attribute {
  color: #00c;
}
.cm-s-ipython span.cm-header {
  color: blue;
}
.cm-s-ipython span.cm-quote {
  color: #090;
}
.cm-s-ipython span.cm-link {
  color: #00c;
}
.cm-s-ipython span.cm-error {
  color: #f00;
}
.cm-s-ipython span.cm-tab {
  background: url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADAAAAAMCAYAAAAkuj5RAAAAAXNSR0IArs4c6QAAAGFJREFUSMft1LsRQFAQheHPowAKoACx3IgEKtaEHujDjORSgWTH/ZOdnZOcM/sgk/kFFWY0qV8foQwS4MKBCS3qR6ixBJvElOobYAtivseIE120FaowJPN75GMu8j/LfMwNjh4HUpwg4LUAAAAASUVORK5CYII=);
  background-position: right;
  background-repeat: no-repeat;
}
div.output_wrapper {
  /* this position must be relative to enable descendents to be absolute within it */
  position: relative;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  z-index: 1;
}
/* class for the output area when it should be height-limited */
div.output_scroll {
  /* ideally, this would be max-height, but FF barfs all over that */
  height: 24em;
  /* FF needs this *and the wrapper* to specify full width, or it will shrinkwrap */
  width: 100%;
  overflow: auto;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 2px 8px rgba(0, 0, 0, 0.8);
  box-shadow: inset 0 2px 8px rgba(0, 0, 0, 0.8);
  display: block;
}
/* output div while it is collapsed */
div.output_collapsed {
  margin: 0px;
  padding: 0px;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
}
div.out_prompt_overlay {
  height: 100%;
  padding: 0px 0.4em;
  position: absolute;
  border-radius: 2px;
}
div.out_prompt_overlay:hover {
  /* use inner shadow to get border that is computed the same on WebKit/FF */
  -webkit-box-shadow: inset 0 0 1px #000;
  box-shadow: inset 0 0 1px #000;
  background: rgba(240, 240, 240, 0.5);
}
div.output_prompt {
  color: #D84315;
}
/* This class is the outer container of all output sections. */
div.output_area {
  padding: 0px;
  page-break-inside: avoid;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
div.output_area .MathJax_Display {
  text-align: left !important;
}
div.output_area .rendered_html table {
  margin-left: 0;
  margin-right: 0;
}
div.output_area .rendered_html img {
  margin-left: 0;
  margin-right: 0;
}
div.output_area img,
div.output_area svg {
  max-width: 100%;
  height: auto;
}
div.output_area img.unconfined,
div.output_area svg.unconfined {
  max-width: none;
}
/* This is needed to protect the pre formating from global settings such
   as that of bootstrap */
.output {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
}
@media (max-width: 540px) {
  div.output_area {
    /* Old browsers */
    display: -webkit-box;
    -webkit-box-orient: vertical;
    -webkit-box-align: stretch;
    display: -moz-box;
    -moz-box-orient: vertical;
    -moz-box-align: stretch;
    display: box;
    box-orient: vertical;
    box-align: stretch;
    /* Modern browsers */
    display: flex;
    flex-direction: column;
    align-items: stretch;
  }
}
div.output_area pre {
  margin: 0;
  padding: 0;
  border: 0;
  vertical-align: baseline;
  color: black;
  background-color: transparent;
  border-radius: 0;
}
/* This class is for the output subarea inside the output_area and after
   the prompt div. */
div.output_subarea {
  overflow-x: auto;
  padding: 0.4em;
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
  max-width: calc(100% - 14ex);
}
div.output_scroll div.output_subarea {
  overflow-x: visible;
}
/* The rest of the output_* classes are for special styling of the different
   output types */
/* all text output has this class: */
div.output_text {
  text-align: left;
  color: #000;
  /* This has to match that of the the CodeMirror class line-height below */
  line-height: 1.21429em;
}
/* stdout/stderr are 'text' as well as 'stream', but execute_result/error are *not* streams */
div.output_stderr {
  background: #fdd;
  /* very light red background for stderr */
}
div.output_latex {
  text-align: left;
}
/* Empty output_javascript divs should have no height */
div.output_javascript:empty {
  padding: 0;
}
.js-error {
  color: darkred;
}
/* raw_input styles */
div.raw_input_container {
  line-height: 1.21429em;
  padding-top: 5px;
}
pre.raw_input_prompt {
  /* nothing needed here. */
}
input.raw_input {
  font-family: monospace;
  font-size: inherit;
  color: inherit;
  width: auto;
  /* make sure input baseline aligns with prompt */
  vertical-align: baseline;
  /* padding + margin = 0.5em between prompt and cursor */
  padding: 0em 0.25em;
  margin: 0em 0.25em;
}
input.raw_input:focus {
  box-shadow: none;
}
p.p-space {
  margin-bottom: 10px;
}
div.output_unrecognized {
  padding: 5px;
  font-weight: bold;
  color: red;
}
div.output_unrecognized a {
  color: inherit;
  text-decoration: none;
}
div.output_unrecognized a:hover {
  color: inherit;
  text-decoration: none;
}
.rendered_html {
  color: #000;
  /* any extras will just be numbers: */
}
.rendered_html em {
  font-style: italic;
}
.rendered_html strong {
  font-weight: bold;
}
.rendered_html u {
  text-decoration: underline;
}
.rendered_html :link {
  text-decoration: underline;
}
.rendered_html :visited {
  text-decoration: underline;
}
.rendered_html h1 {
  font-size: 185.7%;
  margin: 1.08em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h2 {
  font-size: 157.1%;
  margin: 1.27em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h3 {
  font-size: 128.6%;
  margin: 1.55em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h4 {
  font-size: 100%;
  margin: 2em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h5 {
  font-size: 100%;
  margin: 2em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
  font-style: italic;
}
.rendered_html h6 {
  font-size: 100%;
  margin: 2em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
  font-style: italic;
}
.rendered_html h1:first-child {
  margin-top: 0.538em;
}
.rendered_html h2:first-child {
  margin-top: 0.636em;
}
.rendered_html h3:first-child {
  margin-top: 0.777em;
}
.rendered_html h4:first-child {
  margin-top: 1em;
}
.rendered_html h5:first-child {
  margin-top: 1em;
}
.rendered_html h6:first-child {
  margin-top: 1em;
}
.rendered_html ul {
  list-style: disc;
  margin: 0em 2em;
  padding-left: 0px;
}
.rendered_html ul ul {
  list-style: square;
  margin: 0em 2em;
}
.rendered_html ul ul ul {
  list-style: circle;
  margin: 0em 2em;
}
.rendered_html ol {
  list-style: decimal;
  margin: 0em 2em;
  padding-left: 0px;
}
.rendered_html ol ol {
  list-style: upper-alpha;
  margin: 0em 2em;
}
.rendered_html ol ol ol {
  list-style: lower-alpha;
  margin: 0em 2em;
}
.rendered_html ol ol ol ol {
  list-style: lower-roman;
  margin: 0em 2em;
}
.rendered_html ol ol ol ol ol {
  list-style: decimal;
  margin: 0em 2em;
}
.rendered_html * + ul {
  margin-top: 1em;
}
.rendered_html * + ol {
  margin-top: 1em;
}
.rendered_html hr {
  color: black;
  background-color: black;
}
.rendered_html pre {
  margin: 1em 2em;
}
.rendered_html pre,
.rendered_html code {
  border: 0;
  background-color: #fff;
  color: #000;
  font-size: 100%;
  padding: 0px;
}
.rendered_html blockquote {
  margin: 1em 2em;
}
.rendered_html table {
  margin-left: auto;
  margin-right: auto;
  border: 1px solid black;
  border-collapse: collapse;
}
.rendered_html tr,
.rendered_html th,
.rendered_html td {
  border: 1px solid black;
  border-collapse: collapse;
  margin: 1em 2em;
}
.rendered_html td,
.rendered_html th {
  text-align: left;
  vertical-align: middle;
  padding: 4px;
}
.rendered_html th {
  font-weight: bold;
}
.rendered_html * + table {
  margin-top: 1em;
}
.rendered_html p {
  text-align: left;
}
.rendered_html * + p {
  margin-top: 1em;
}
.rendered_html img {
  display: block;
  margin-left: auto;
  margin-right: auto;
}
.rendered_html * + img {
  margin-top: 1em;
}
.rendered_html img,
.rendered_html svg {
  max-width: 100%;
  height: auto;
}
.rendered_html img.unconfined,
.rendered_html svg.unconfined {
  max-width: none;
}
div.text_cell {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
@media (max-width: 540px) {
  div.text_cell > div.prompt {
    display: none;
  }
}
div.text_cell_render {
  /*font-family: "Helvetica Neue", Arial, Helvetica, Geneva, sans-serif;*/
  outline: none;
  resize: none;
  width: inherit;
  border-style: none;
  padding: 0.5em 0.5em 0.5em 0.4em;
  color: #000;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
a.anchor-link:link {
  text-decoration: none;
  padding: 0px 20px;
  visibility: hidden;
}
h1:hover .anchor-link,
h2:hover .anchor-link,
h3:hover .anchor-link,
h4:hover .anchor-link,
h5:hover .anchor-link,
h6:hover .anchor-link {
  visibility: visible;
}
.text_cell.rendered .input_area {
  display: none;
}
.text_cell.rendered .rendered_html {
  overflow-x: auto;
  overflow-y: hidden;
}
.text_cell.unrendered .text_cell_render {
  display: none;
}
.cm-header-1,
.cm-header-2,
.cm-header-3,
.cm-header-4,
.cm-header-5,
.cm-header-6 {
  font-weight: bold;
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
}
.cm-header-1 {
  font-size: 185.7%;
}
.cm-header-2 {
  font-size: 157.1%;
}
.cm-header-3 {
  font-size: 128.6%;
}
.cm-header-4 {
  font-size: 110%;
}
.cm-header-5 {
  font-size: 100%;
  font-style: italic;
}
.cm-header-6 {
  font-size: 100%;
  font-style: italic;
}
/*!
*
* IPython notebook webapp
*
*/
@media (max-width: 767px) {
  .notebook_app {
    padding-left: 0px;
    padding-right: 0px;
  }
}
#ipython-main-app {
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  height: 100%;
}
div#notebook_panel {
  margin: 0px;
  padding: 0px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  height: 100%;
}
div#notebook {
  font-size: 14px;
  line-height: 20px;
  overflow-y: hidden;
  overflow-x: auto;
  width: 100%;
  /* This spaces the page away from the edge of the notebook area */
  padding-top: 20px;
  margin: 0px;
  outline: none;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  min-height: 100%;
}
@media not print {
  #notebook-container {
    padding: 15px;
    background-color: #fff;
    min-height: 0;
    -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
    box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  }
}
@media print {
  #notebook-container {
    width: 100%;
  }
}
div.ui-widget-content {
  border: 1px solid #ababab;
  outline: none;
}
pre.dialog {
  background-color: #f7f7f7;
  border: 1px solid #ddd;
  border-radius: 2px;
  padding: 0.4em;
  padding-left: 2em;
}
p.dialog {
  padding: 0.2em;
}
/* Word-wrap output correctly.  This is the CSS3 spelling, though Firefox seems
   to not honor it correctly.  Webkit browsers (Chrome, rekonq, Safari) do.
 */
pre,
code,
kbd,
samp {
  white-space: pre-wrap;
}
#fonttest {
  font-family: monospace;
}
p {
  margin-bottom: 0;
}
.end_space {
  min-height: 100px;
  transition: height .2s ease;
}
.notebook_app > #header {
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
}
@media not print {
  .notebook_app {
    background-color: #EEE;
  }
}
kbd {
  border-style: solid;
  border-width: 1px;
  box-shadow: none;
  margin: 2px;
  padding-left: 2px;
  padding-right: 2px;
  padding-top: 1px;
  padding-bottom: 1px;
}
/* CSS for the cell toolbar */
.celltoolbar {
  border: thin solid #CFCFCF;
  border-bottom: none;
  background: #EEE;
  border-radius: 2px 2px 0px 0px;
  width: 100%;
  height: 29px;
  padding-right: 4px;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
  /* Old browsers */
  -webkit-box-pack: end;
  -moz-box-pack: end;
  box-pack: end;
  /* Modern browsers */
  justify-content: flex-end;
  display: -webkit-flex;
}
@media print {
  .celltoolbar {
    display: none;
  }
}
.ctb_hideshow {
  display: none;
  vertical-align: bottom;
}
/* ctb_show is added to the ctb_hideshow div to show the cell toolbar.
   Cell toolbars are only shown when the ctb_global_show class is also set.
*/
.ctb_global_show .ctb_show.ctb_hideshow {
  display: block;
}
.ctb_global_show .ctb_show + .input_area,
.ctb_global_show .ctb_show + div.text_cell_input,
.ctb_global_show .ctb_show ~ div.text_cell_render {
  border-top-right-radius: 0px;
  border-top-left-radius: 0px;
}
.ctb_global_show .ctb_show ~ div.text_cell_render {
  border: 1px solid #cfcfcf;
}
.celltoolbar {
  font-size: 87%;
  padding-top: 3px;
}
.celltoolbar select {
  display: block;
  width: 100%;
  height: 32px;
  padding: 6px 12px;
  font-size: 13px;
  line-height: 1.42857143;
  color: #555555;
  background-color: #fff;
  background-image: none;
  border: 1px solid #ccc;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  -webkit-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  -o-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
  width: inherit;
  font-size: inherit;
  height: 22px;
  padding: 0px;
  display: inline-block;
}
.celltoolbar select:focus {
  border-color: #66afe9;
  outline: 0;
  -webkit-box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
  box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
}
.celltoolbar select::-moz-placeholder {
  color: #999;
  opacity: 1;
}
.celltoolbar select:-ms-input-placeholder {
  color: #999;
}
.celltoolbar select::-webkit-input-placeholder {
  color: #999;
}
.celltoolbar select::-ms-expand {
  border: 0;
  background-color: transparent;
}
.celltoolbar select[disabled],
.celltoolbar select[readonly],
fieldset[disabled] .celltoolbar select {
  background-color: #eeeeee;
  opacity: 1;
}
.celltoolbar select[disabled],
fieldset[disabled] .celltoolbar select {
  cursor: not-allowed;
}
textarea.celltoolbar select {
  height: auto;
}
select.celltoolbar select {
  height: 30px;
  line-height: 30px;
}
textarea.celltoolbar select,
select[multiple].celltoolbar select {
  height: auto;
}
.celltoolbar label {
  margin-left: 5px;
  margin-right: 5px;
}
.completions {
  position: absolute;
  z-index: 110;
  overflow: hidden;
  border: 1px solid #ababab;
  border-radius: 2px;
  -webkit-box-shadow: 0px 6px 10px -1px #adadad;
  box-shadow: 0px 6px 10px -1px #adadad;
  line-height: 1;
}
.completions select {
  background: white;
  outline: none;
  border: none;
  padding: 0px;
  margin: 0px;
  overflow: auto;
  font-family: monospace;
  font-size: 110%;
  color: #000;
  width: auto;
}
.completions select option.context {
  color: #286090;
}
#kernel_logo_widget {
  float: right !important;
  float: right;
}
#kernel_logo_widget .current_kernel_logo {
  display: none;
  margin-top: -1px;
  margin-bottom: -1px;
  width: 32px;
  height: 32px;
}
#menubar {
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  margin-top: 1px;
}
#menubar .navbar {
  border-top: 1px;
  border-radius: 0px 0px 2px 2px;
  margin-bottom: 0px;
}
#menubar .navbar-toggle {
  float: left;
  padding-top: 7px;
  padding-bottom: 7px;
  border: none;
}
#menubar .navbar-collapse {
  clear: left;
}
.nav-wrapper {
  border-bottom: 1px solid #e7e7e7;
}
i.menu-icon {
  padding-top: 4px;
}
ul#help_menu li a {
  overflow: hidden;
  padding-right: 2.2em;
}
ul#help_menu li a i {
  margin-right: -1.2em;
}
.dropdown-submenu {
  position: relative;
}
.dropdown-submenu > .dropdown-menu {
  top: 0;
  left: 100%;
  margin-top: -6px;
  margin-left: -1px;
}
.dropdown-submenu:hover > .dropdown-menu {
  display: block;
}
.dropdown-submenu > a:after {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  display: block;
  content: "\f0da";
  float: right;
  color: #333333;
  margin-top: 2px;
  margin-right: -10px;
}
.dropdown-submenu > a:after.pull-left {
  margin-right: .3em;
}
.dropdown-submenu > a:after.pull-right {
  margin-left: .3em;
}
.dropdown-submenu:hover > a:after {
  color: #262626;
}
.dropdown-submenu.pull-left {
  float: none;
}
.dropdown-submenu.pull-left > .dropdown-menu {
  left: -100%;
  margin-left: 10px;
}
#notification_area {
  float: right !important;
  float: right;
  z-index: 10;
}
.indicator_area {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
}
#kernel_indicator {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
  border-left: 1px solid;
}
#kernel_indicator .kernel_indicator_name {
  padding-left: 5px;
  padding-right: 5px;
}
#modal_indicator {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
}
#readonly-indicator {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
  margin-top: 2px;
  margin-bottom: 0px;
  margin-left: 0px;
  margin-right: 0px;
  display: none;
}
.modal_indicator:before {
  width: 1.28571429em;
  text-align: center;
}
.edit_mode .modal_indicator:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f040";
}
.edit_mode .modal_indicator:before.pull-left {
  margin-right: .3em;
}
.edit_mode .modal_indicator:before.pull-right {
  margin-left: .3em;
}
.command_mode .modal_indicator:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: ' ';
}
.command_mode .modal_indicator:before.pull-left {
  margin-right: .3em;
}
.command_mode .modal_indicator:before.pull-right {
  margin-left: .3em;
}
.kernel_idle_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f10c";
}
.kernel_idle_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_idle_icon:before.pull-right {
  margin-left: .3em;
}
.kernel_busy_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f111";
}
.kernel_busy_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_busy_icon:before.pull-right {
  margin-left: .3em;
}
.kernel_dead_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f1e2";
}
.kernel_dead_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_dead_icon:before.pull-right {
  margin-left: .3em;
}
.kernel_disconnected_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f127";
}
.kernel_disconnected_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_disconnected_icon:before.pull-right {
  margin-left: .3em;
}
.notification_widget {
  color: #777;
  z-index: 10;
  background: rgba(240, 240, 240, 0.5);
  margin-right: 4px;
  color: #333;
  background-color: #fff;
  border-color: #ccc;
}
.notification_widget:focus,
.notification_widget.focus {
  color: #333;
  background-color: #e6e6e6;
  border-color: #8c8c8c;
}
.notification_widget:hover {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.notification_widget:active,
.notification_widget.active,
.open > .dropdown-toggle.notification_widget {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.notification_widget:active:hover,
.notification_widget.active:hover,
.open > .dropdown-toggle.notification_widget:hover,
.notification_widget:active:focus,
.notification_widget.active:focus,
.open > .dropdown-toggle.notification_widget:focus,
.notification_widget:active.focus,
.notification_widget.active.focus,
.open > .dropdown-toggle.notification_widget.focus {
  color: #333;
  background-color: #d4d4d4;
  border-color: #8c8c8c;
}
.notification_widget:active,
.notification_widget.active,
.open > .dropdown-toggle.notification_widget {
  background-image: none;
}
.notification_widget.disabled:hover,
.notification_widget[disabled]:hover,
fieldset[disabled] .notification_widget:hover,
.notification_widget.disabled:focus,
.notification_widget[disabled]:focus,
fieldset[disabled] .notification_widget:focus,
.notification_widget.disabled.focus,
.notification_widget[disabled].focus,
fieldset[disabled] .notification_widget.focus {
  background-color: #fff;
  border-color: #ccc;
}
.notification_widget .badge {
  color: #fff;
  background-color: #333;
}
.notification_widget.warning {
  color: #fff;
  background-color: #f0ad4e;
  border-color: #eea236;
}
.notification_widget.warning:focus,
.notification_widget.warning.focus {
  color: #fff;
  background-color: #ec971f;
  border-color: #985f0d;
}
.notification_widget.warning:hover {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.notification_widget.warning:active,
.notification_widget.warning.active,
.open > .dropdown-toggle.notification_widget.warning {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.notification_widget.warning:active:hover,
.notification_widget.warning.active:hover,
.open > .dropdown-toggle.notification_widget.warning:hover,
.notification_widget.warning:active:focus,
.notification_widget.warning.active:focus,
.open > .dropdown-toggle.notification_widget.warning:focus,
.notification_widget.warning:active.focus,
.notification_widget.warning.active.focus,
.open > .dropdown-toggle.notification_widget.warning.focus {
  color: #fff;
  background-color: #d58512;
  border-color: #985f0d;
}
.notification_widget.warning:active,
.notification_widget.warning.active,
.open > .dropdown-toggle.notification_widget.warning {
  background-image: none;
}
.notification_widget.warning.disabled:hover,
.notification_widget.warning[disabled]:hover,
fieldset[disabled] .notification_widget.warning:hover,
.notification_widget.warning.disabled:focus,
.notification_widget.warning[disabled]:focus,
fieldset[disabled] .notification_widget.warning:focus,
.notification_widget.warning.disabled.focus,
.notification_widget.warning[disabled].focus,
fieldset[disabled] .notification_widget.warning.focus {
  background-color: #f0ad4e;
  border-color: #eea236;
}
.notification_widget.warning .badge {
  color: #f0ad4e;
  background-color: #fff;
}
.notification_widget.success {
  color: #fff;
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.notification_widget.success:focus,
.notification_widget.success.focus {
  color: #fff;
  background-color: #449d44;
  border-color: #255625;
}
.notification_widget.success:hover {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.notification_widget.success:active,
.notification_widget.success.active,
.open > .dropdown-toggle.notification_widget.success {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.notification_widget.success:active:hover,
.notification_widget.success.active:hover,
.open > .dropdown-toggle.notification_widget.success:hover,
.notification_widget.success:active:focus,
.notification_widget.success.active:focus,
.open > .dropdown-toggle.notification_widget.success:focus,
.notification_widget.success:active.focus,
.notification_widget.success.active.focus,
.open > .dropdown-toggle.notification_widget.success.focus {
  color: #fff;
  background-color: #398439;
  border-color: #255625;
}
.notification_widget.success:active,
.notification_widget.success.active,
.open > .dropdown-toggle.notification_widget.success {
  background-image: none;
}
.notification_widget.success.disabled:hover,
.notification_widget.success[disabled]:hover,
fieldset[disabled] .notification_widget.success:hover,
.notification_widget.success.disabled:focus,
.notification_widget.success[disabled]:focus,
fieldset[disabled] .notification_widget.success:focus,
.notification_widget.success.disabled.focus,
.notification_widget.success[disabled].focus,
fieldset[disabled] .notification_widget.success.focus {
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.notification_widget.success .badge {
  color: #5cb85c;
  background-color: #fff;
}
.notification_widget.info {
  color: #fff;
  background-color: #5bc0de;
  border-color: #46b8da;
}
.notification_widget.info:focus,
.notification_widget.info.focus {
  color: #fff;
  background-color: #31b0d5;
  border-color: #1b6d85;
}
.notification_widget.info:hover {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.notification_widget.info:active,
.notification_widget.info.active,
.open > .dropdown-toggle.notification_widget.info {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.notification_widget.info:active:hover,
.notification_widget.info.active:hover,
.open > .dropdown-toggle.notification_widget.info:hover,
.notification_widget.info:active:focus,
.notification_widget.info.active:focus,
.open > .dropdown-toggle.notification_widget.info:focus,
.notification_widget.info:active.focus,
.notification_widget.info.active.focus,
.open > .dropdown-toggle.notification_widget.info.focus {
  color: #fff;
  background-color: #269abc;
  border-color: #1b6d85;
}
.notification_widget.info:active,
.notification_widget.info.active,
.open > .dropdown-toggle.notification_widget.info {
  background-image: none;
}
.notification_widget.info.disabled:hover,
.notification_widget.info[disabled]:hover,
fieldset[disabled] .notification_widget.info:hover,
.notification_widget.info.disabled:focus,
.notification_widget.info[disabled]:focus,
fieldset[disabled] .notification_widget.info:focus,
.notification_widget.info.disabled.focus,
.notification_widget.info[disabled].focus,
fieldset[disabled] .notification_widget.info.focus {
  background-color: #5bc0de;
  border-color: #46b8da;
}
.notification_widget.info .badge {
  color: #5bc0de;
  background-color: #fff;
}
.notification_widget.danger {
  color: #fff;
  background-color: #d9534f;
  border-color: #d43f3a;
}
.notification_widget.danger:focus,
.notification_widget.danger.focus {
  color: #fff;
  background-color: #c9302c;
  border-color: #761c19;
}
.notification_widget.danger:hover {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.notification_widget.danger:active,
.notification_widget.danger.active,
.open > .dropdown-toggle.notification_widget.danger {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.notification_widget.danger:active:hover,
.notification_widget.danger.active:hover,
.open > .dropdown-toggle.notification_widget.danger:hover,
.notification_widget.danger:active:focus,
.notification_widget.danger.active:focus,
.open > .dropdown-toggle.notification_widget.danger:focus,
.notification_widget.danger:active.focus,
.notification_widget.danger.active.focus,
.open > .dropdown-toggle.notification_widget.danger.focus {
  color: #fff;
  background-color: #ac2925;
  border-color: #761c19;
}
.notification_widget.danger:active,
.notification_widget.danger.active,
.open > .dropdown-toggle.notification_widget.danger {
  background-image: none;
}
.notification_widget.danger.disabled:hover,
.notification_widget.danger[disabled]:hover,
fieldset[disabled] .notification_widget.danger:hover,
.notification_widget.danger.disabled:focus,
.notification_widget.danger[disabled]:focus,
fieldset[disabled] .notification_widget.danger:focus,
.notification_widget.danger.disabled.focus,
.notification_widget.danger[disabled].focus,
fieldset[disabled] .notification_widget.danger.focus {
  background-color: #d9534f;
  border-color: #d43f3a;
}
.notification_widget.danger .badge {
  color: #d9534f;
  background-color: #fff;
}
div#pager {
  background-color: #fff;
  font-size: 14px;
  line-height: 20px;
  overflow: hidden;
  display: none;
  position: fixed;
  bottom: 0px;
  width: 100%;
  max-height: 50%;
  padding-top: 8px;
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  /* Display over codemirror */
  z-index: 100;
  /* Hack which prevents jquery ui resizable from changing top. */
  top: auto !important;
}
div#pager pre {
  line-height: 1.21429em;
  color: #000;
  background-color: #f7f7f7;
  padding: 0.4em;
}
div#pager #pager-button-area {
  position: absolute;
  top: 8px;
  right: 20px;
}
div#pager #pager-contents {
  position: relative;
  overflow: auto;
  width: 100%;
  height: 100%;
}
div#pager #pager-contents #pager-container {
  position: relative;
  padding: 15px 0px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
div#pager .ui-resizable-handle {
  top: 0px;
  height: 8px;
  background: #f7f7f7;
  border-top: 1px solid #cfcfcf;
  border-bottom: 1px solid #cfcfcf;
  /* This injects handle bars (a short, wide = symbol) for 
        the resize handle. */
}
div#pager .ui-resizable-handle::after {
  content: '';
  top: 2px;
  left: 50%;
  height: 3px;
  width: 30px;
  margin-left: -15px;
  position: absolute;
  border-top: 1px solid #cfcfcf;
}
.quickhelp {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
  line-height: 1.8em;
}
.shortcut_key {
  display: inline-block;
  width: 21ex;
  text-align: right;
  font-family: monospace;
}
.shortcut_descr {
  display: inline-block;
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
span.save_widget {
  margin-top: 6px;
}
span.save_widget span.filename {
  height: 1em;
  line-height: 1em;
  padding: 3px;
  margin-left: 16px;
  border: none;
  font-size: 146.5%;
  border-radius: 2px;
}
span.save_widget span.filename:hover {
  background-color: #e6e6e6;
}
span.checkpoint_status,
span.autosave_status {
  font-size: small;
}
@media (max-width: 767px) {
  span.save_widget {
    font-size: small;
  }
  span.checkpoint_status,
  span.autosave_status {
    display: none;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  span.checkpoint_status {
    display: none;
  }
  span.autosave_status {
    font-size: x-small;
  }
}
.toolbar {
  padding: 0px;
  margin-left: -5px;
  margin-top: 2px;
  margin-bottom: 5px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
.toolbar select,
.toolbar label {
  width: auto;
  vertical-align: middle;
  margin-right: 2px;
  margin-bottom: 0px;
  display: inline;
  font-size: 92%;
  margin-left: 0.3em;
  margin-right: 0.3em;
  padding: 0px;
  padding-top: 3px;
}
.toolbar .btn {
  padding: 2px 8px;
}
.toolbar .btn-group {
  margin-top: 0px;
  margin-left: 5px;
}
#maintoolbar {
  margin-bottom: -3px;
  margin-top: -8px;
  border: 0px;
  min-height: 27px;
  margin-left: 0px;
  padding-top: 11px;
  padding-bottom: 3px;
}
#maintoolbar .navbar-text {
  float: none;
  vertical-align: middle;
  text-align: right;
  margin-left: 5px;
  margin-right: 0px;
  margin-top: 0px;
}
.select-xs {
  height: 24px;
}
.pulse,
.dropdown-menu > li > a.pulse,
li.pulse > a.dropdown-toggle,
li.pulse.open > a.dropdown-toggle {
  background-color: #F37626;
  color: white;
}
/**
 * Primary styles
 *
 * Author: Jupyter Development Team
 */
/** WARNING IF YOU ARE EDITTING THIS FILE, if this is a .css file, It has a lot
 * of chance of beeing generated from the ../less/[samename].less file, you can
 * try to get back the less file by reverting somme commit in history
 **/
/*
 * We'll try to get something pretty, so we
 * have some strange css to have the scroll bar on
 * the left with fix button on the top right of the tooltip
 */
@-moz-keyframes fadeOut {
  from {
    opacity: 1;
  }
  to {
    opacity: 0;
  }
}
@-webkit-keyframes fadeOut {
  from {
    opacity: 1;
  }
  to {
    opacity: 0;
  }
}
@-moz-keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
@-webkit-keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
/*properties of tooltip after "expand"*/
.bigtooltip {
  overflow: auto;
  height: 200px;
  -webkit-transition-property: height;
  -webkit-transition-duration: 500ms;
  -moz-transition-property: height;
  -moz-transition-duration: 500ms;
  transition-property: height;
  transition-duration: 500ms;
}
/*properties of tooltip before "expand"*/
.smalltooltip {
  -webkit-transition-property: height;
  -webkit-transition-duration: 500ms;
  -moz-transition-property: height;
  -moz-transition-duration: 500ms;
  transition-property: height;
  transition-duration: 500ms;
  text-overflow: ellipsis;
  overflow: hidden;
  height: 80px;
}
.tooltipbuttons {
  position: absolute;
  padding-right: 15px;
  top: 0px;
  right: 0px;
}
.tooltiptext {
  /*avoid the button to overlap on some docstring*/
  padding-right: 30px;
}
.ipython_tooltip {
  max-width: 700px;
  /*fade-in animation when inserted*/
  -webkit-animation: fadeOut 400ms;
  -moz-animation: fadeOut 400ms;
  animation: fadeOut 400ms;
  -webkit-animation: fadeIn 400ms;
  -moz-animation: fadeIn 400ms;
  animation: fadeIn 400ms;
  vertical-align: middle;
  background-color: #f7f7f7;
  overflow: visible;
  border: #ababab 1px solid;
  outline: none;
  padding: 3px;
  margin: 0px;
  padding-left: 7px;
  font-family: monospace;
  min-height: 50px;
  -moz-box-shadow: 0px 6px 10px -1px #adadad;
  -webkit-box-shadow: 0px 6px 10px -1px #adadad;
  box-shadow: 0px 6px 10px -1px #adadad;
  border-radius: 2px;
  position: absolute;
  z-index: 1000;
}
.ipython_tooltip a {
  float: right;
}
.ipython_tooltip .tooltiptext pre {
  border: 0;
  border-radius: 0;
  font-size: 100%;
  background-color: #f7f7f7;
}
.pretooltiparrow {
  left: 0px;
  margin: 0px;
  top: -16px;
  width: 40px;
  height: 16px;
  overflow: hidden;
  position: absolute;
}
.pretooltiparrow:before {
  background-color: #f7f7f7;
  border: 1px #ababab solid;
  z-index: 11;
  content: "";
  position: absolute;
  left: 15px;
  top: 10px;
  width: 25px;
  height: 25px;
  -webkit-transform: rotate(45deg);
  -moz-transform: rotate(45deg);
  -ms-transform: rotate(45deg);
  -o-transform: rotate(45deg);
}
ul.typeahead-list i {
  margin-left: -10px;
  width: 18px;
}
ul.typeahead-list {
  max-height: 80vh;
  overflow: auto;
}
ul.typeahead-list > li > a {
  /** Firefox bug **/
  /* see https://github.com/jupyter/notebook/issues/559 */
  white-space: normal;
}
.cmd-palette .modal-body {
  padding: 7px;
}
.cmd-palette form {
  background: white;
}
.cmd-palette input {
  outline: none;
}
.no-shortcut {
  display: none;
}
.command-shortcut:before {
  content: "(command)";
  padding-right: 3px;
  color: #777777;
}
.edit-shortcut:before {
  content: "(edit)";
  padding-right: 3px;
  color: #777777;
}
#find-and-replace #replace-preview .match,
#find-and-replace #replace-preview .insert {
  background-color: #BBDEFB;
  border-color: #90CAF9;
  border-style: solid;
  border-width: 1px;
  border-radius: 0px;
}
#find-and-replace #replace-preview .replace .match {
  background-color: #FFCDD2;
  border-color: #EF9A9A;
  border-radius: 0px;
}
#find-and-replace #replace-preview .replace .insert {
  background-color: #C8E6C9;
  border-color: #A5D6A7;
  border-radius: 0px;
}
#find-and-replace #replace-preview {
  max-height: 60vh;
  overflow: auto;
}
#find-and-replace #replace-preview pre {
  padding: 5px 10px;
}
.terminal-app {
  background: #EEE;
}
.terminal-app #header {
  background: #fff;
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
}
.terminal-app .terminal {
  width: 100%;
  float: left;
  font-family: monospace;
  color: white;
  background: black;
  padding: 0.4em;
  border-radius: 2px;
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.4);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.4);
}
.terminal-app .terminal,
.terminal-app .terminal dummy-screen {
  line-height: 1em;
  font-size: 14px;
}
.terminal-app .terminal .xterm-rows {
  padding: 10px;
}
.terminal-app .terminal-cursor {
  color: black;
  background: white;
}
.terminal-app #terminado-container {
  margin-top: 20px;
}
/*# sourceMappingURL=style.min.css.map */
    </style>
<style type="text/css">
    .highlight .hll { background-color: #ffffcc }
.highlight  { background: #f8f8f8; }
.highlight .c { color: #408080; font-style: italic } /* Comment */
.highlight .err { border: 1px solid #FF0000 } /* Error */
.highlight .k { color: #008000; font-weight: bold } /* Keyword */
.highlight .o { color: #666666 } /* Operator */
.highlight .ch { color: #408080; font-style: italic } /* Comment.Hashbang */
.highlight .cm { color: #408080; font-style: italic } /* Comment.Multiline */
.highlight .cp { color: #BC7A00 } /* Comment.Preproc */
.highlight .cpf { color: #408080; font-style: italic } /* Comment.PreprocFile */
.highlight .c1 { color: #408080; font-style: italic } /* Comment.Single */
.highlight .cs { color: #408080; font-style: italic } /* Comment.Special */
.highlight .gd { color: #A00000 } /* Generic.Deleted */
.highlight .ge { font-style: italic } /* Generic.Emph */
.highlight .gr { color: #FF0000 } /* Generic.Error */
.highlight .gh { color: #000080; font-weight: bold } /* Generic.Heading */
.highlight .gi { color: #00A000 } /* Generic.Inserted */
.highlight .go { color: #888888 } /* Generic.Output */
.highlight .gp { color: #000080; font-weight: bold } /* Generic.Prompt */
.highlight .gs { font-weight: bold } /* Generic.Strong */
.highlight .gu { color: #800080; font-weight: bold } /* Generic.Subheading */
.highlight .gt { color: #0044DD } /* Generic.Traceback */
.highlight .kc { color: #008000; font-weight: bold } /* Keyword.Constant */
.highlight .kd { color: #008000; font-weight: bold } /* Keyword.Declaration */
.highlight .kn { color: #008000; font-weight: bold } /* Keyword.Namespace */
.highlight .kp { color: #008000 } /* Keyword.Pseudo */
.highlight .kr { color: #008000; font-weight: bold } /* Keyword.Reserved */
.highlight .kt { color: #B00040 } /* Keyword.Type */
.highlight .m { color: #666666 } /* Literal.Number */
.highlight .s { color: #BA2121 } /* Literal.String */
.highlight .na { color: #7D9029 } /* Name.Attribute */
.highlight .nb { color: #008000 } /* Name.Builtin */
.highlight .nc { color: #0000FF; font-weight: bold } /* Name.Class */
.highlight .no { color: #880000 } /* Name.Constant */
.highlight .nd { color: #AA22FF } /* Name.Decorator */
.highlight .ni { color: #999999; font-weight: bold } /* Name.Entity */
.highlight .ne { color: #D2413A; font-weight: bold } /* Name.Exception */
.highlight .nf { color: #0000FF } /* Name.Function */
.highlight .nl { color: #A0A000 } /* Name.Label */
.highlight .nn { color: #0000FF; font-weight: bold } /* Name.Namespace */
.highlight .nt { color: #008000; font-weight: bold } /* Name.Tag */
.highlight .nv { color: #19177C } /* Name.Variable */
.highlight .ow { color: #AA22FF; font-weight: bold } /* Operator.Word */
.highlight .w { color: #bbbbbb } /* Text.Whitespace */
.highlight .mb { color: #666666 } /* Literal.Number.Bin */
.highlight .mf { color: #666666 } /* Literal.Number.Float */
.highlight .mh { color: #666666 } /* Literal.Number.Hex */
.highlight .mi { color: #666666 } /* Literal.Number.Integer */
.highlight .mo { color: #666666 } /* Literal.Number.Oct */
.highlight .sa { color: #BA2121 } /* Literal.String.Affix */
.highlight .sb { color: #BA2121 } /* Literal.String.Backtick */
.highlight .sc { color: #BA2121 } /* Literal.String.Char */
.highlight .dl { color: #BA2121 } /* Literal.String.Delimiter */
.highlight .sd { color: #BA2121; font-style: italic } /* Literal.String.Doc */
.highlight .s2 { color: #BA2121 } /* Literal.String.Double */
.highlight .se { color: #BB6622; font-weight: bold } /* Literal.String.Escape */
.highlight .sh { color: #BA2121 } /* Literal.String.Heredoc */
.highlight .si { color: #BB6688; font-weight: bold } /* Literal.String.Interpol */
.highlight .sx { color: #008000 } /* Literal.String.Other */
.highlight .sr { color: #BB6688 } /* Literal.String.Regex */
.highlight .s1 { color: #BA2121 } /* Literal.String.Single */
.highlight .ss { color: #19177C } /* Literal.String.Symbol */
.highlight .bp { color: #008000 } /* Name.Builtin.Pseudo */
.highlight .fm { color: #0000FF } /* Name.Function.Magic */
.highlight .vc { color: #19177C } /* Name.Variable.Class */
.highlight .vg { color: #19177C } /* Name.Variable.Global */
.highlight .vi { color: #19177C } /* Name.Variable.Instance */
.highlight .vm { color: #19177C } /* Name.Variable.Magic */
.highlight .il { color: #666666 } /* Literal.Number.Integer.Long */
    </style>
<style type="text/css">
    
/* Temporary definitions which will become obsolete with Notebook release 5.0 */
.ansi-black-fg { color: #3E424D; }
.ansi-black-bg { background-color: #3E424D; }
.ansi-black-intense-fg { color: #282C36; }
.ansi-black-intense-bg { background-color: #282C36; }
.ansi-red-fg { color: #E75C58; }
.ansi-red-bg { background-color: #E75C58; }
.ansi-red-intense-fg { color: #B22B31; }
.ansi-red-intense-bg { background-color: #B22B31; }
.ansi-green-fg { color: #00A250; }
.ansi-green-bg { background-color: #00A250; }
.ansi-green-intense-fg { color: #007427; }
.ansi-green-intense-bg { background-color: #007427; }
.ansi-yellow-fg { color: #DDB62B; }
.ansi-yellow-bg { background-color: #DDB62B; }
.ansi-yellow-intense-fg { color: #B27D12; }
.ansi-yellow-intense-bg { background-color: #B27D12; }
.ansi-blue-fg { color: #208FFB; }
.ansi-blue-bg { background-color: #208FFB; }
.ansi-blue-intense-fg { color: #0065CA; }
.ansi-blue-intense-bg { background-color: #0065CA; }
.ansi-magenta-fg { color: #D160C4; }
.ansi-magenta-bg { background-color: #D160C4; }
.ansi-magenta-intense-fg { color: #A03196; }
.ansi-magenta-intense-bg { background-color: #A03196; }
.ansi-cyan-fg { color: #60C6C8; }
.ansi-cyan-bg { background-color: #60C6C8; }
.ansi-cyan-intense-fg { color: #258F8F; }
.ansi-cyan-intense-bg { background-color: #258F8F; }
.ansi-white-fg { color: #C5C1B4; }
.ansi-white-bg { background-color: #C5C1B4; }
.ansi-white-intense-fg { color: #A1A6B2; }
.ansi-white-intense-bg { background-color: #A1A6B2; }

.ansi-bold { font-weight: bold; }

    </style>


<style type="text/css">
/* Overrides of notebook CSS for static HTML export */
body {
  overflow: visible;
  padding: 8px;
}

div#notebook {
  overflow: visible;
  border-top: none;
}@media print {
  div.cell {
    display: block;
    page-break-inside: avoid;
  } 
  div.output_wrapper { 
    display: block;
    page-break-inside: avoid; 
  }
  div.output { 
    display: block;
    page-break-inside: avoid; 
  }
}
</style>

<!-- Custom stylesheet, it must be in the same directory as the html file -->
<link rel="stylesheet" href="custom.css">

<!-- Loading mathjax macro -->
<!-- Load mathjax -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.1/MathJax.js?config=TeX-AMS_HTML"></script>
    <!-- MathJax configuration -->
    <script type="text/x-mathjax-config;executed=true">
    MathJax.Hub.Config({
        tex2jax: {
            inlineMath: [ ['$','$'], ["\\(","\\)"] ],
            displayMath: [ ['$$','$$'], ["\\[","\\]"] ],
            processEscapes: true,
            processEnvironments: true
        },
        // Center justify equations in code and markdown cells. Elsewhere
        // we use CSS to left justify single line equations in code cells.
        displayAlign: 'center',
        "HTML-CSS": {
            styles: {'.MathJax_Display': {"margin": 0}},
            linebreaks: { automatic: true }
        }
    });
    </script>
    <!-- End of mathjax configuration --><style type="text/css">.MathJax_Hover_Frame {border-radius: .25em; -webkit-border-radius: .25em; -moz-border-radius: .25em; -khtml-border-radius: .25em; box-shadow: 0px 0px 15px #83A; -webkit-box-shadow: 0px 0px 15px #83A; -moz-box-shadow: 0px 0px 15px #83A; -khtml-box-shadow: 0px 0px 15px #83A; border: 1px solid #A6D ! important; display: inline-block; position: absolute}
.MathJax_Menu_Button .MathJax_Hover_Arrow {position: absolute; cursor: pointer; display: inline-block; border: 2px solid #AAA; border-radius: 4px; -webkit-border-radius: 4px; -moz-border-radius: 4px; -khtml-border-radius: 4px; font-family: 'Courier New',Courier; font-size: 9px; color: #F0F0F0}
.MathJax_Menu_Button .MathJax_Hover_Arrow span {display: block; background-color: #AAA; border: 1px solid; border-radius: 3px; line-height: 0; padding: 4px}
.MathJax_Hover_Arrow:hover {color: white!important; border: 2px solid #CCC!important}
.MathJax_Hover_Arrow:hover span {background-color: #CCC!important}
</style><style type="text/css">#MathJax_About {position: fixed; left: 50%; width: auto; text-align: center; border: 3px outset; padding: 1em 2em; background-color: #DDDDDD; color: black; cursor: default; font-family: message-box; font-size: 120%; font-style: normal; text-indent: 0; text-transform: none; line-height: normal; letter-spacing: normal; word-spacing: normal; word-wrap: normal; white-space: nowrap; float: none; z-index: 201; border-radius: 15px; -webkit-border-radius: 15px; -moz-border-radius: 15px; -khtml-border-radius: 15px; box-shadow: 0px 10px 20px #808080; -webkit-box-shadow: 0px 10px 20px #808080; -moz-box-shadow: 0px 10px 20px #808080; -khtml-box-shadow: 0px 10px 20px #808080; filter: progid:DXImageTransform.Microsoft.dropshadow(OffX=2, OffY=2, Color='gray', Positive='true')}
#MathJax_About.MathJax_MousePost {outline: none}
.MathJax_Menu {position: absolute; background-color: white; color: black; width: auto; padding: 2px; border: 1px solid #CCCCCC; margin: 0; cursor: default; font: menu; text-align: left; text-indent: 0; text-transform: none; line-height: normal; letter-spacing: normal; word-spacing: normal; word-wrap: normal; white-space: nowrap; float: none; z-index: 201; box-shadow: 0px 10px 20px #808080; -webkit-box-shadow: 0px 10px 20px #808080; -moz-box-shadow: 0px 10px 20px #808080; -khtml-box-shadow: 0px 10px 20px #808080; filter: progid:DXImageTransform.Microsoft.dropshadow(OffX=2, OffY=2, Color='gray', Positive='true')}
.MathJax_MenuItem {padding: 2px 2em; background: transparent}
.MathJax_MenuArrow {position: absolute; right: .5em; padding-top: .25em; color: #666666; font-size: .75em}
.MathJax_MenuActive .MathJax_MenuArrow {color: white}
.MathJax_MenuArrow.RTL {left: .5em; right: auto}
.MathJax_MenuCheck {position: absolute; left: .7em}
.MathJax_MenuCheck.RTL {right: .7em; left: auto}
.MathJax_MenuRadioCheck {position: absolute; left: 1em}
.MathJax_MenuRadioCheck.RTL {right: 1em; left: auto}
.MathJax_MenuLabel {padding: 2px 2em 4px 1.33em; font-style: italic}
.MathJax_MenuRule {border-top: 1px solid #CCCCCC; margin: 4px 1px 0px}
.MathJax_MenuDisabled {color: GrayText}
.MathJax_MenuActive {background-color: Highlight; color: HighlightText}
.MathJax_MenuDisabled:focus, .MathJax_MenuLabel:focus {background-color: #E8E8E8}
.MathJax_ContextMenu:focus {outline: none}
.MathJax_ContextMenu .MathJax_MenuItem:focus {outline: none}
#MathJax_AboutClose {top: .2em; right: .2em}
.MathJax_Menu .MathJax_MenuClose {top: -10px; left: -10px}
.MathJax_MenuClose {position: absolute; cursor: pointer; display: inline-block; border: 2px solid #AAA; border-radius: 18px; -webkit-border-radius: 18px; -moz-border-radius: 18px; -khtml-border-radius: 18px; font-family: 'Courier New',Courier; font-size: 24px; color: #F0F0F0}
.MathJax_MenuClose span {display: block; background-color: #AAA; border: 1.5px solid; border-radius: 18px; -webkit-border-radius: 18px; -moz-border-radius: 18px; -khtml-border-radius: 18px; line-height: 0; padding: 8px 0 6px}
.MathJax_MenuClose:hover {color: white!important; border: 2px solid #CCC!important}
.MathJax_MenuClose:hover span {background-color: #CCC!important}
.MathJax_MenuClose:hover:focus {outline: none}
</style><style type="text/css">.MathJax_Preview .MJXf-math {color: inherit!important}
</style><style type="text/css">.MJX_Assistive_MathML {position: absolute!important; top: 0; left: 0; clip: rect(1px, 1px, 1px, 1px); padding: 1px 0 0 0!important; border: 0!important; height: 1px!important; width: 1px!important; overflow: hidden!important; display: block!important; -webkit-touch-callout: none; -webkit-user-select: none; -khtml-user-select: none; -moz-user-select: none; -ms-user-select: none; user-select: none}
.MJX_Assistive_MathML.MJX_Assistive_MathML_Block {width: 100%!important}
</style><style type="text/css">#MathJax_Zoom {position: absolute; background-color: #F0F0F0; overflow: auto; display: block; z-index: 301; padding: .5em; border: 1px solid black; margin: 0; font-weight: normal; font-style: normal; text-align: left; text-indent: 0; text-transform: none; line-height: normal; letter-spacing: normal; word-spacing: normal; word-wrap: normal; white-space: nowrap; float: none; -webkit-box-sizing: content-box; -moz-box-sizing: content-box; box-sizing: content-box; box-shadow: 5px 5px 15px #AAAAAA; -webkit-box-shadow: 5px 5px 15px #AAAAAA; -moz-box-shadow: 5px 5px 15px #AAAAAA; -khtml-box-shadow: 5px 5px 15px #AAAAAA; filter: progid:DXImageTransform.Microsoft.dropshadow(OffX=2, OffY=2, Color='gray', Positive='true')}
#MathJax_ZoomOverlay {position: absolute; left: 0; top: 0; z-index: 300; display: inline-block; width: 100%; height: 100%; border: 0; padding: 0; margin: 0; background-color: white; opacity: 0; filter: alpha(opacity=0)}
#MathJax_ZoomFrame {position: relative; display: inline-block; height: 0; width: 0}
#MathJax_ZoomEventTrap {position: absolute; left: 0; top: 0; z-index: 302; display: inline-block; border: 0; padding: 0; margin: 0; background-color: white; opacity: 0; filter: alpha(opacity=0)}
</style><style type="text/css">.MathJax_Preview {color: #888}
#MathJax_Message {position: fixed; left: 1em; bottom: 1.5em; background-color: #E6E6E6; border: 1px solid #959595; margin: 0px; padding: 2px 8px; z-index: 102; color: black; font-size: 80%; width: auto; white-space: nowrap}
#MathJax_MSIE_Frame {position: absolute; top: 0; left: 0; width: 0px; z-index: 101; border: 0px; margin: 0px; padding: 0px}
.MathJax_Error {color: #CC0000; font-style: italic}
</style><style type="text/css">.MJXp-script {font-size: .8em}
.MJXp-right {-webkit-transform-origin: right; -moz-transform-origin: right; -ms-transform-origin: right; -o-transform-origin: right; transform-origin: right}
.MJXp-bold {font-weight: bold}
.MJXp-italic {font-style: italic}
.MJXp-scr {font-family: MathJax_Script,'Times New Roman',Times,STIXGeneral,serif}
.MJXp-frak {font-family: MathJax_Fraktur,'Times New Roman',Times,STIXGeneral,serif}
.MJXp-sf {font-family: MathJax_SansSerif,'Times New Roman',Times,STIXGeneral,serif}
.MJXp-cal {font-family: MathJax_Caligraphic,'Times New Roman',Times,STIXGeneral,serif}
.MJXp-mono {font-family: MathJax_Typewriter,'Times New Roman',Times,STIXGeneral,serif}
.MJXp-largeop {font-size: 150%}
.MJXp-largeop.MJXp-int {vertical-align: -.2em}
.MJXp-math {display: inline-block; line-height: 1.2; text-indent: 0; font-family: 'Times New Roman',Times,STIXGeneral,serif; white-space: nowrap; border-collapse: collapse}
.MJXp-display {display: block; text-align: center; margin: 1em 0}
.MJXp-math span {display: inline-block}
.MJXp-box {display: block!important; text-align: center}
.MJXp-box:after {content: " "}
.MJXp-rule {display: block!important; margin-top: .1em}
.MJXp-char {display: block!important}
.MJXp-mo {margin: 0 .15em}
.MJXp-mfrac {margin: 0 .125em; vertical-align: .25em}
.MJXp-denom {display: inline-table!important; width: 100%}
.MJXp-denom > * {display: table-row!important}
.MJXp-surd {vertical-align: top}
.MJXp-surd > * {display: block!important}
.MJXp-script-box > *  {display: table!important; height: 50%}
.MJXp-script-box > * > * {display: table-cell!important; vertical-align: top}
.MJXp-script-box > *:last-child > * {vertical-align: bottom}
.MJXp-script-box > * > * > * {display: block!important}
.MJXp-mphantom {visibility: hidden}
.MJXp-munderover {display: inline-table!important}
.MJXp-over {display: inline-block!important; text-align: center}
.MJXp-over > * {display: block!important}
.MJXp-munderover > * {display: table-row!important}
.MJXp-mtable {vertical-align: .25em; margin: 0 .125em}
.MJXp-mtable > * {display: inline-table!important; vertical-align: middle}
.MJXp-mtr {display: table-row!important}
.MJXp-mtd {display: table-cell!important; text-align: center; padding: .5em 0 0 .5em}
.MJXp-mtr > .MJXp-mtd:first-child {padding-left: 0}
.MJXp-mtr:first-child > .MJXp-mtd {padding-top: 0}
.MJXp-mlabeledtr {display: table-row!important}
.MJXp-mlabeledtr > .MJXp-mtd:first-child {padding-left: 0}
.MJXp-mlabeledtr:first-child > .MJXp-mtd {padding-top: 0}
.MJXp-merror {background-color: #FFFF88; color: #CC0000; border: 1px solid #CC0000; padding: 1px 3px; font-style: normal; font-size: 90%}
.MJXp-scale0 {-webkit-transform: scaleX(.0); -moz-transform: scaleX(.0); -ms-transform: scaleX(.0); -o-transform: scaleX(.0); transform: scaleX(.0)}
.MJXp-scale1 {-webkit-transform: scaleX(.1); -moz-transform: scaleX(.1); -ms-transform: scaleX(.1); -o-transform: scaleX(.1); transform: scaleX(.1)}
.MJXp-scale2 {-webkit-transform: scaleX(.2); -moz-transform: scaleX(.2); -ms-transform: scaleX(.2); -o-transform: scaleX(.2); transform: scaleX(.2)}
.MJXp-scale3 {-webkit-transform: scaleX(.3); -moz-transform: scaleX(.3); -ms-transform: scaleX(.3); -o-transform: scaleX(.3); transform: scaleX(.3)}
.MJXp-scale4 {-webkit-transform: scaleX(.4); -moz-transform: scaleX(.4); -ms-transform: scaleX(.4); -o-transform: scaleX(.4); transform: scaleX(.4)}
.MJXp-scale5 {-webkit-transform: scaleX(.5); -moz-transform: scaleX(.5); -ms-transform: scaleX(.5); -o-transform: scaleX(.5); transform: scaleX(.5)}
.MJXp-scale6 {-webkit-transform: scaleX(.6); -moz-transform: scaleX(.6); -ms-transform: scaleX(.6); -o-transform: scaleX(.6); transform: scaleX(.6)}
.MJXp-scale7 {-webkit-transform: scaleX(.7); -moz-transform: scaleX(.7); -ms-transform: scaleX(.7); -o-transform: scaleX(.7); transform: scaleX(.7)}
.MJXp-scale8 {-webkit-transform: scaleX(.8); -moz-transform: scaleX(.8); -ms-transform: scaleX(.8); -o-transform: scaleX(.8); transform: scaleX(.8)}
.MJXp-scale9 {-webkit-transform: scaleX(.9); -moz-transform: scaleX(.9); -ms-transform: scaleX(.9); -o-transform: scaleX(.9); transform: scaleX(.9)}
.MathJax_PHTML .noError {vertical-align: ; font-size: 90%; text-align: left; color: black; padding: 1px 3px; border: 1px solid}
</style></head>
<body style=""><div id="MathJax_Message" style="display: none;"></div>
  <div tabindex="-1" id="notebook" class="border-box-sizing">
    <div class="container" id="notebook-container">

<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="1.-Dataset-Information:">1. Dataset Information:<a class="anchor-link" href="#1.-Dataset-Information:">¶</a></h1><p>The dataset contains cases from a study that was conducted between 1958 and 1970 at the University of Chicago's Billings Hospital on the survival of patients who had undergone surgery for breast cancer.</p>
<p>Number of Instances: 306 <br>
 Number of Attributes: 4 (including the class attribute)<br>
 Attribute Information:<br>
 Age of patient at time of operation (numerical)<br>
 Patient's year of operation (year - 1900, numerical)<br>
 Number of positive axillary nodes detected (numerical)<br>
 Survival status (class attribute)<br></p>
<blockquote><p>1 = the patient survived 5 years or longer<br>
 2 = the patient died within 5 year<br></p>
</blockquote>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="2.-Importing-necessary-library">2. Importing necessary library<a class="anchor-link" href="#2.-Importing-necessary-library">¶</a></h1><h3 id="Pandas---to-read-.csv-file">Pandas - to read .csv file<a class="anchor-link" href="#Pandas---to-read-.csv-file">¶</a></h3><h3 id="Seaborn-and-Matlab---to-plot-various-kinds-of-data">Seaborn and Matlab - to plot various kinds of data<a class="anchor-link" href="#Seaborn-and-Matlab---to-plot-various-kinds-of-data">¶</a></h3><h3 id="Numpy---to-calculate-cumulative-distribution-function">Numpy - to calculate cumulative distribution function<a class="anchor-link" href="#Numpy---to-calculate-cumulative-distribution-function">¶</a></h3>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[1]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">pandas</span> <span class="k">as</span> <span class="nn">pd</span>
<span class="kn">import</span> <span class="nn">seaborn</span> <span class="k">as</span> <span class="nn">sns</span>
<span class="kn">import</span> <span class="nn">matplotlib.pyplot</span> <span class="k">as</span> <span class="nn">plt</span>
<span class="kn">import</span> <span class="nn">numpy</span> <span class="k">as</span> <span class="nn">np</span>
<span class="c1">#reading the csv file</span>
<span class="n">df</span> <span class="o">=</span> <span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">'haberman.csv'</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="3.-High-level-statistics-of-the-dataset">3. High level statistics of the dataset<a class="anchor-link" href="#3.-High-level-statistics-of-the-dataset">¶</a></h1>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[2]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span><span class="o">.</span><span class="n">shape</span>  <span class="c1">#print the number of rows and colums</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt output_prompt">Out[2]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>(306, 4)</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[3]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span><span class="o">.</span><span class="n">head</span><span class="p">()</span><span class="c1">#Prints the first 5 entries of df</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt output_prompt">Out[3]:</div>



<div class="output_html rendered_html output_subarea output_execute_result">
<div>
<style scoped="">
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>age</th>
      <th>year</th>
      <th>nodes</th>
      <th>status</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>30</td>
      <td>64</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>1</th>
      <td>30</td>
      <td>62</td>
      <td>3</td>
      <td>1</td>
    </tr>
    <tr>
      <th>2</th>
      <td>30</td>
      <td>65</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>3</th>
      <td>31</td>
      <td>59</td>
      <td>2</td>
      <td>1</td>
    </tr>
    <tr>
      <th>4</th>
      <td>31</td>
      <td>65</td>
      <td>4</td>
      <td>1</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[4]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span><span class="o">.</span><span class="n">columns</span> <span class="c1">#printing the columns</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt output_prompt">Out[4]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>Index(['age', 'year', 'nodes', 'status'], dtype='object')</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[5]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="nb">print</span><span class="p">(</span><span class="n">df</span><span class="o">.</span><span class="n">info</span><span class="p">())</span> <span class="c1">#info about the dataset</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>&lt;class 'pandas.core.frame.DataFrame'&gt;
RangeIndex: 306 entries, 0 to 305
Data columns (total 4 columns):
age       306 non-null int64
year      306 non-null int64
nodes     306 non-null int64
status    306 non-null int64
dtypes: int64(4)
memory usage: 9.6 KB
None
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[6]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span><span class="o">.</span><span class="n">describe</span><span class="p">(</span><span class="n">percentiles</span><span class="o">=</span><span class="p">[</span><span class="mf">0.25</span><span class="p">,</span><span class="mf">0.5</span><span class="p">,</span><span class="mf">0.75</span><span class="p">,</span><span class="mf">0.9</span><span class="p">,</span><span class="mf">0.99</span><span class="p">],</span><span class="n">include</span><span class="o">=</span><span class="s1">'all'</span><span class="p">)</span> <span class="c1">#describes the dataset</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt output_prompt">Out[6]:</div>



<div class="output_html rendered_html output_subarea output_execute_result">
<div>
<style scoped="">
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>age</th>
      <th>year</th>
      <th>nodes</th>
      <th>status</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>count</th>
      <td>306.000000</td>
      <td>306.000000</td>
      <td>306.000000</td>
      <td>306.000000</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>52.457516</td>
      <td>62.852941</td>
      <td>4.026144</td>
      <td>1.264706</td>
    </tr>
    <tr>
      <th>std</th>
      <td>10.803452</td>
      <td>3.249405</td>
      <td>7.189654</td>
      <td>0.441899</td>
    </tr>
    <tr>
      <th>min</th>
      <td>30.000000</td>
      <td>58.000000</td>
      <td>0.000000</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>44.000000</td>
      <td>60.000000</td>
      <td>0.000000</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>52.000000</td>
      <td>63.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>60.750000</td>
      <td>65.750000</td>
      <td>4.000000</td>
      <td>2.000000</td>
    </tr>
    <tr>
      <th>90%</th>
      <td>67.000000</td>
      <td>67.000000</td>
      <td>13.000000</td>
      <td>2.000000</td>
    </tr>
    <tr>
      <th>99%</th>
      <td>75.950000</td>
      <td>69.000000</td>
      <td>29.900000</td>
      <td>2.000000</td>
    </tr>
    <tr>
      <th>max</th>
      <td>83.000000</td>
      <td>69.000000</td>
      <td>52.000000</td>
      <td>2.000000</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="Observation:">Observation:<a class="anchor-link" href="#Observation:">¶</a></h1><ol>
<li>The given data has a total of 306 rows and 4 columns</li>
<li>The column names are 'age', 'year', 'nodes', 'status'</li>
<li>The given dataset has no empty values</li>
<li>After seeing the description and evaluating the data, the status column has only 2 values (1 or 2). This is a categorical feature.</li>
</ol>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="4.-OBJECTIVE:">4. OBJECTIVE:<a class="anchor-link" href="#4.-OBJECTIVE:">¶</a></h1><h3 id="The-new-value-must-be-categorised-as-a-survivor-or-not-after-5-years-of-the-operation">The new value must be categorised as a survivor or not after 5 years of the operation<a class="anchor-link" href="#The-new-value-must-be-categorised-as-a-survivor-or-not-after-5-years-of-the-operation">¶</a></h3>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="5.-Data-preprocessing">5. Data preprocessing<a class="anchor-link" href="#5.-Data-preprocessing">¶</a></h1>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[7]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span><span class="p">[</span><span class="s1">'status'</span><span class="p">]</span> <span class="o">=</span> <span class="n">df</span><span class="p">[</span><span class="s1">'status'</span><span class="p">]</span><span class="o">.</span><span class="n">map</span><span class="p">({</span><span class="mi">1</span><span class="p">:</span><span class="s1">'Yes'</span><span class="p">,</span> <span class="mi">2</span><span class="p">:</span><span class="s1">'No'</span><span class="p">})</span>
<span class="n">df</span><span class="o">.</span><span class="n">head</span><span class="p">()</span> 
<span class="c1">#mapping the values of 1 and 2 to yes and no respectively and #printing the first 5 records from the dataset.</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt output_prompt">Out[7]:</div>



<div class="output_html rendered_html output_subarea output_execute_result">
<div>
<style scoped="">
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>age</th>
      <th>year</th>
      <th>nodes</th>
      <th>status</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>30</td>
      <td>64</td>
      <td>1</td>
      <td>Yes</td>
    </tr>
    <tr>
      <th>1</th>
      <td>30</td>
      <td>62</td>
      <td>3</td>
      <td>Yes</td>
    </tr>
    <tr>
      <th>2</th>
      <td>30</td>
      <td>65</td>
      <td>0</td>
      <td>Yes</td>
    </tr>
    <tr>
      <th>3</th>
      <td>31</td>
      <td>59</td>
      <td>2</td>
      <td>Yes</td>
    </tr>
    <tr>
      <th>4</th>
      <td>31</td>
      <td>65</td>
      <td>4</td>
      <td>Yes</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[8]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span><span class="p">[</span><span class="s2">"status"</span><span class="p">]</span><span class="o">.</span><span class="n">value_counts</span><span class="p">()</span> <span class="c1">#gives each count of the status type</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt output_prompt">Out[8]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>Yes    225
No      81
Name: status, dtype: int64</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[9]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="p">(</span><span class="n">df</span><span class="p">[[</span><span class="s1">'age'</span><span class="p">,</span><span class="s1">'year'</span><span class="p">,</span><span class="s1">'nodes'</span><span class="p">]]</span> <span class="o">==</span> <span class="mi">0</span><span class="p">)</span><span class="o">.</span><span class="n">all</span><span class="p">()</span> <span class="c1">#return True if all values are 0 otherwise it will return false</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt output_prompt">Out[9]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>age      False
year     False
nodes    False
dtype: bool</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[10]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">survived</span> <span class="o">=</span> <span class="n">df</span><span class="p">[</span><span class="n">df</span><span class="p">[</span><span class="s1">'status'</span><span class="p">]</span><span class="o">==</span><span class="s1">'Yes'</span><span class="p">]</span>
<span class="n">survived</span><span class="o">.</span><span class="n">describe</span><span class="p">()</span>
<span class="c1">#survived dataframe stores all the records where status is yes</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt output_prompt">Out[10]:</div>



<div class="output_html rendered_html output_subarea output_execute_result">
<div>
<style scoped="">
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>age</th>
      <th>year</th>
      <th>nodes</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>count</th>
      <td>225.000000</td>
      <td>225.000000</td>
      <td>225.000000</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>52.017778</td>
      <td>62.862222</td>
      <td>2.791111</td>
    </tr>
    <tr>
      <th>std</th>
      <td>11.012154</td>
      <td>3.222915</td>
      <td>5.870318</td>
    </tr>
    <tr>
      <th>min</th>
      <td>30.000000</td>
      <td>58.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>43.000000</td>
      <td>60.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>52.000000</td>
      <td>63.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>60.000000</td>
      <td>66.000000</td>
      <td>3.000000</td>
    </tr>
    <tr>
      <th>max</th>
      <td>77.000000</td>
      <td>69.000000</td>
      <td>46.000000</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[11]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">not_survived</span> <span class="o">=</span> <span class="n">df</span><span class="p">[</span><span class="n">df</span><span class="p">[</span><span class="s1">'status'</span><span class="p">]</span><span class="o">==</span><span class="s1">'No'</span><span class="p">]</span>
<span class="n">not_survived</span><span class="o">.</span><span class="n">describe</span><span class="p">()</span>
<span class="c1">#not_survived dataframe stores all the records where status is no</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt output_prompt">Out[11]:</div>



<div class="output_html rendered_html output_subarea output_execute_result">
<div>
<style scoped="">
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>age</th>
      <th>year</th>
      <th>nodes</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>count</th>
      <td>81.000000</td>
      <td>81.000000</td>
      <td>81.000000</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>53.679012</td>
      <td>62.827160</td>
      <td>7.456790</td>
    </tr>
    <tr>
      <th>std</th>
      <td>10.167137</td>
      <td>3.342118</td>
      <td>9.185654</td>
    </tr>
    <tr>
      <th>min</th>
      <td>34.000000</td>
      <td>58.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>46.000000</td>
      <td>59.000000</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>53.000000</td>
      <td>63.000000</td>
      <td>4.000000</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>61.000000</td>
      <td>65.000000</td>
      <td>11.000000</td>
    </tr>
    <tr>
      <th>max</th>
      <td>83.000000</td>
      <td>69.000000</td>
      <td>52.000000</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="Observation">Observation<a class="anchor-link" href="#Observation">¶</a></h1><ol>
<li>The categorical data has been changed from integer (1 &amp; 2) to object (Yes &amp; No)</li>
<li>The given dataset had 225 Yes and 81 No as status type which is considered as an unbalanced dataset.</li>
</ol>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="6.-Univaraite-analysis">6. Univaraite analysis<a class="anchor-link" href="#6.-Univaraite-analysis">¶</a></h1>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="6a.-Probability-Density-Function-(PDF)">6a. Probability Density Function (PDF)<a class="anchor-link" href="#6a.-Probability-Density-Function-(PDF)">¶</a></h2>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[12]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">sns</span><span class="o">.</span><span class="n">FacetGrid</span><span class="p">(</span><span class="n">df</span><span class="p">,</span><span class="n">hue</span><span class="o">=</span><span class="s1">'status'</span><span class="p">,</span><span class="n">size</span> <span class="o">=</span> <span class="mi">5</span><span class="p">)</span><span class="o">.</span><span class="n">map</span><span class="p">(</span><span class="n">sns</span><span class="o">.</span><span class="n">distplot</span><span class="p">,</span><span class="s2">"age"</span><span class="p">)</span><span class="o">.</span><span class="n">add_legend</span><span class="p">();</span>
<span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>


<div class="output_subarea output_stream output_stderr output_text">
<pre>C:\Anaconda3\lib\site-packages\matplotlib\axes\_axes.py:6462: UserWarning: The 'normed' kwarg is deprecated, and has been replaced by the 'density' kwarg.
  warnings.warn("The 'normed' kwarg is deprecated, and has been "
C:\Anaconda3\lib\site-packages\matplotlib\axes\_axes.py:6462: UserWarning: The 'normed' kwarg is deprecated, and has been replaced by the 'density' kwarg.
  warnings.warn("The 'normed' kwarg is deprecated, and has been "
</pre>
</div>
</div>

<div class="output_area">

<div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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y//+7/++uKenx/yhD31o8dlnn70Y4KabbipfsWLFspqamuVf/OIXFwE89NBDBVPLpaamnjlR7+OPP559zTXXVAL813/9V3Ztbe3yJUuW1NXX1y8JR9xBLX2vtd6Mf9jv5GMPTHruAq6b5rqHgIdOUec2punkEeHnGPPQYxtjzXTbBk8y0Uk/klZJiqvntGXF7K3O9rBlYDUfGG6gq/hSkClaYhrPPvustaioyL1ly5YmgP7+fuNTTz2V98YbbxwqLi72AHznO985VlhY6PV4PHzgAx9YsnXr1pSvfOUrPY888kjh5HKn8o1vfKP4lVd8UMP4AAAgAElEQVReOVRVVeXu6+s79QieEMT7WGkRhKP9/sl2VXlppy1ntR8BkDuVCKtKHeMNVU+Gb4QM58z734jEtHbt2tE333zTetddd5W89NJL6bm5ud6pZZ544omcurq6ZXV1dXWHDx9O3r17d0hbtdbX19tvuummyv/4j//I83hOm3+CJkklARzpc2AyKEqyTj+iy+o4gleZcKQsmqfIEpNSYLfWMqqTyByWJjAxvVWrVo3t2LHjwMqVK0e//OUvl9x7773Fk883NjYm/eAHPyh84403Dh06dOjARRddNOxyuab9Tp+8gsbo6OiJF08++WTbQw891Nne3p60Zs2a5d3d3XO+W5GkkgBa+52U5aSetj8FJkZ+VaANsiFopK3KdvOabw1Zww2gZeVicbLW1lZzRkaG77Of/ezAF77wheO7du1KTUtL8w4PDxsABgcHjSkpKb6cnBxve3u7acuWLZkT104uB5Cbm+vesWNHstfr5fnnn8+eOL5//37LRRdd5PjP//zPzuzsbE9LS0vSXOOWb48FzuX20jk0yoVLC2Ysa3UcYSS9eh6iEssynDyj1/Mx37tYnUelyVGcZPv27Sn3339/qcFgwGQy6Ycffvjom2++mX7ZZZfVFhQUuLdu3XpoxYoVztra2uXl5eVj69ats09ce8stt/RNLvcv//IvxzZu3FhTXFzsXrp06ajD4TAAfPGLXyxtbW21aK3V+eefP3LOOeeMzjVupeNorHx9fb3etm1btMOIaVP3TD/YbeOJP7dy2/lVp12eRfncfOKV9TRU3cLuJV+IyDIl4v1+2pLDD5xfYiD3TNqLN8x+j/r6W8MbmAg3BbB79+7W1atX90U7mHDavXt33urVqysnH5PmrwWutd+BQUFZ9unnp6SPHsOgPfIX8zxalT3Om76VZAwfkomQYsGQpLLAHelzUJqdSpLp9L/qv4z8qpyHqATAaquD13xryfAOkeo6Hu1whAgLSSoL2LjHx7HBUSpzTz+UGCbNUUmvjGxQ4oRko6Y7bSk+rciyHYx2OEKEhSSVBax90IlXa6ryTt/0Bf6RX6NJObjNmTOWFeFTm63YrmtJHz4U7VCECAtJKgvYkT4HCqgI6k7liCwkGQXrMu286l1H9ngXOAeiHY4QcyZJZQFr7XNQnJVMsnnm+UxWe6t00kdBltnLQUtgtaLj+6IbjBBhIEllgfL4fLQNOKkK4i7lxEKSsjpxVBRlpdHkW8RYpyQVETk+n49169Ytefrpp60Txx599NHsCy64oDac7yOTHxeoY4OjeHyayhnW+4L3LyQp5t9ZWXZe6annzsHfw7gTkmbuAxPx7yd/bM4LZ313fLD6tHNgDAYDP/rRj45+4hOfqL788ssPeDwe9a//+q8lmzdvPhzOOOROZYFq7fMvIhlsfwogfSpRUpI8znbjKgz4oEfWAhORc9ZZZ7kuvfTS4a9+9atF//AP/7Dor//6r/uXL18+9v3vfz935cqVy5YuXVr3yU9+stzr9eJ2u7nqqquqFi9eXFdbW7v8oYcemnlZDuROZcFq7XeSn2Eh3TLzrzjD0YpXmbCnlMxDZGIqpSDFWkDPSBY5XfswldZHOySxgH3rW9/qXLVqVV1SUpJv9+7dDe+9917y888/n7Vjx44Gs9nMDTfcUPHTn/40Z/HixWMDAwOmQ4cOHQAIdml8SSoLkE9r2gacLF9knbkw/omP9tRyWUgyitZlO3h1cC1/3fs2eD1glN+FiAyr1eq76qqrBtLT070pKSn6xRdftO7Zsydt5cqVdQAul8tQWlo6ftVVVw23tLQk33rrrWWXX3758NVXXz0STP3S/LUA9dnHGHV7Z9w6eEKmvYXh9DMiHJU4nSXpo/zJsBaTbwz6Zc6KiCyDwYDB4P/611pzww039DU2Nh5obGw80Nrauu/b3/52V1FRkXf//v37L7jgAvv3v//9gptuuqkiqLojGrmIivYBJ0BQScXgHSfd2c6IJJWoMipILazBqS34umUUmJg/l112me3555/P6erqMgF0d3cbDx8+nNTZ2Wny+Xx85jOfGXzwwQc79+7dG9RfqXKPvQC1DThJNhvIy7DMWDbDeRQDPrlTiQEfLtG83b2CC44fJFlr2WZYzIv169eP3nfffZ0XXnjhYp/Ph9ls1g8//PBRo9HI7bffXqm1RinF1772tY5g6pOksgC1DTgpz0nFEMSXktXeAsBImiSVaPtg4Tjf1qu4ZGw7OHogvTDaIYkImmkIcCR95zvf6Zz8+s477xy48847T1rSoaGhIeThiNL8tcC43F56RsYoC6E/RaNkIckYkG7W2LPrANDHG6IcjRCzI0llgWkfcKIJrj8FINPRgiNlEV7j6fevF/PjzNIMmnyLcHY1RjsUIWZFksoC0zbgRDHzplwTrDLyK6ZcvGicLb7VJA81gWcs2uEIETJJKgtM24CTQmtwi0gq7cXqaGVY9qWPGUUpPtpSV2DEA/1N0Q5HiJBJUllAfD5N+6Az6P6UNOcxjL5x6aSPMYUllTi1RZrARFySpLKANPfacbl9IU16BGR14hhzUYmPP/nq8B1vkL3rRdyRpLKA7GgbBILvpLc6/ElF+lRiy9JML7tMq0h394GjN9rhiAVEKbXu9ttvL514/cADDxTec889i8L5HjJPZQHZfnSQFLORvPSkoMpn2ptxWvJxm4NbI0zMD6XAVLgUumG8u4GkmqAWhxXx5u3vhXXpe877uxnnvSQlJenNmzdnd3V1dRcXF3vC+v4BcqeygOxoG6I8JxUV5Exsq/2ILM8So84qs9LsK2ak82C0QxELiNFo1DfffHPv17/+9ZNm1h46dCjp3HPPXbx48eK6c889d/Hhw4eD++t0CkkqC8Sw001Tj53y3CA3eNJaFpKMYevz3fyJVWSOHAbveLTDEQvIl770pZ5nn302p7+//31DRO+8887yG2+8sf/QoUMHPvGJT/TfddddZbOpX5LKArGzPbT+lBTXccxeh4z8ilFmA9iyl2PGjbdPhhaL8MnJyfFdd911/d/4xjfe1666c+fOtDvuuGMA4K677hrYvn17+mzqDyqpKKU2KKUOKqWalFL3TXPeopT6VeD8VqVUZeB4rlLqdaWUXSn1gynXbAnUuSvwIw3Hc7CjbQiDgtLs4GbGZ0onfcwrL69kVCfR1y5NYCK87r///uNPPvlknsPhCPuNxYwVKqWMwA+By4A64AalVN2UYrcBg1rrGuC7wDcDx13AV4F7T1H9TVrrNYGfntl8AOG3s22QJUVWLKagNmfDavdvISx9KrHrg4s07/jqMPfJOmAivAoLC71XXHHF4JNPPnlisMCZZ57pePTRR7MBfvzjH+fU19fbZ1N3MFlqPdCktW7RWo8DTwEbp5TZCDwReP4M8BGllNJaO7TWb+FPLiJCvD7NzrYh1pZnBX1Npr2FMbMVV1JuBCMTc2E1a9pTl5Pj6QFnf7TDEQvMl7/85e6hoaETI4AfeeSRtp///Od5ixcvrvvlL3+Z+/DDD7fPpt5ghhSXAJMr7wDOPlUZrbVHKTUM5AIzDXF7XCnlBX4DPKT1yTO9lFJ3AHcAlJeXBxFu4jncY8M+5mFteTZjHl9Q11jtzf7+FNmzI6ZlLFoMR6C3/RD5S86NdjginIIYAhxuTqdz58TzsrIyz+jo6InXS5YsGX/nnXfmvO1oMHcq033rTP3yD6bMVDdprVcCFwR+PjVdIa31T7TW9Vrr+vz8/BmDTUQ7jg4BsK4iO+hrMh1HZM2vOHBWRRYdOg+7DC0WcSKYpNIBTB5aVgp0nqqMUsoEZAInbfgymdb6WODRBjyJv5lNzMKOtkFy0pKoCHI4sWV8kOTxAVmeJQ6Upmv2mFZQ6GgEnzfa4Qgxo2CSyntArVKqSimVBFwPbJpSZhNwS+D5tcBr0zVlTVBKmZRSeYHnZuByQDbmnqUdbYOsLc8KYdKjjPyKJ57cZaTiYrjnaLRDEWJGMyYVrbUHuBt4GWgAntZa71dKPaiUujJQ7DEgVynVBNwDnBh2rJRqBb4DfFop1REYOWYBXlZK7QF2AceAn4bvYyWOQcc4Lb0OziwPvunrL0lFmr/iQU3VGXi0gWNHD0c7FDE3Pp/Pt2A6MQOf5aRO3KDW/tJabwY2Tzn2wKTnLuC6U1xbeYpq1wXz3uL0JiY9rg0hqWQ6WvAYU3AmF0UqLBFGy/LM7FE1ZA40AB+Ndjhi9vb19vbW5efnDxsMhrheftrn86ne3t5MpmlhkgUl49yOo0MYDYrVZZlBX2O1H2EkrRKULKgQD5SCvoxlrBzZhGvUTnLKrCY6iyjzeDx/093d/Wh3d/cK4n81Ex+wz+Px/M3UE5JU4tyOtkGWFWeQmhT8rzLT3kxPjtwoxpPskiUYbJrmlmaWL18d7XDELKxbt64HuHLGgnEu3rNlQvP6NLvbh0Jq+jK7R0hzdTOUXhvByES4La8sYkin4+qWocUitklSiWMHu204xr0hJZUsm39xwuEMSSrxxGIy0GSpo3z0AD5fXDfHiwVOkkoc2942i056m38E0VDG4ojEJCLHULCEfIY42CHL5InYJUklju08OkheehJlOcGtTAyQZT/MuCkDZ/JJe/SIGFd9Rg0Ax9tlaLGIXZJU4ph/0mN20JMeAbJshxnKqJE1v+JQpjWTNkMp1qED0Q5FiFOSpBKn+u1jtPY7WRvCel9oTZbtMMPSSR+3hjOXsdx3iLbhiGwvLsScSVKJUzvb/ItIhtKfkuI6TpLHxpB00setwrJaLMrDgebWaIcixLQkqcSpHW2DmAyKVaXBT3rMsk900ktSiVcFJVW4SEL3ytBiEZskqcSp7UcHqVtkJdkc3E6P4O9PAfx9KiI+Gc10pixm8dg+hsalX0zEHkkqccjj9bGnYzikpi/wz1FxJBfiNgd/dyNij6VwCdWGLt45aot2KEKcRJZpiUON3TZG3d7QOunxz1EZTpe7lFi19chptyA6wWIs8G+12tLAVlM1zd62952/8WzZIVVEj9ypxKEdJyY9Br8nvfK5yXS0yKTHBWDMkke/yqZi7CDuhbOSulggJKnEoR1HBynIsFCSFfykR6ujFaNvnEHrkghGJuaFUhxPreEcdYADI5ZoRyPE+0hSiUM72oZCnvSYPdIIwGDG0kiFJeaRyqrEqpwMDPRFOxQh3keSSpzptY3RNuBkbUXwTV/gTyoeQzK29MrIBCbmlSOjEh+KHEczp9m5W4h5J0klzkz0p6wLsZM+23aQoYxatAp+CLKIXV5jCl3mctazj84hV7TDEeIESSpxZkfbIGajYvmiEIYFa032SKP0pywwLmsVq1QLbcfaox2KECfIkOIY8eTWtpkLAS/v66bImsyzO44FXXeq6zgW97D0pywwLusZGPq3kNn1NqyQUX0iNsidShzx+jQdg6OU56SGdN1EJ/2Q3KksKPaURThVKqtc2xl0jkc7HCEASSpxpWt4FI9PUxZqUrE1olEyR2WhUQYGU6v4oHEPDZ3D0Y5GCECSSlxpG3AChHynkjVyEFtaBR5TaNeJ2DeWeQZFahDXsf3RDkUIQJJKXGkbcJKZYiYrNSmk67JHGhnMkKavhWg4vRqAqpF3cLm9UY5GCEkqcaVtwBly05fZbSNjtINBq3TSL0TjZiu9KVVcoPZw8LgsMCmiT5JKnBhxuRlyukNu+soZ8W89O5BZF4mwRAzoKzifsw2NNHf2RDsUISSpxIu2/tn1p+QM+9vaB6zLwx6TiA1d+edjUW6yet7D65PZ9SK6JKnEiaP9DkwGxaLM5JCuyxnejy2llPEk2UNloerNWYtbJXGu3s2RPke0wxEJTpJKnGjt9/enmIyh/cpyh/czkCl3KQuZ15hMT049HzLuoaFrJNrhiAQnSSUOjLm9dA6NUpmbFtJ1SeNDpI8ek6SSALrzz6NGHWOwSxaYFNElSSUOHB1wooHKvND6U3ID/Sn9klQWvM78CwCoH3+Phi4ZBSaiJ6ikopTaoJQ6qJRqUkrdN815i1LqV4HzW5VSlYHjuUqp15VSdqXUD6Zcs04ptTdwzfdUKJuDJJjWfgcGNZdOehn5tdDZ0qsYSqngEsN2Xm04Hu1wRAKbMakopYzAD4HLgDrgBqXU1G+p24BBrXUN8F3gm4HjLuCrwL3TVP0IcAdQG/jZMJsPkAha+5wsykrBYgpt2fqckf0Mp1XiMadHKDIRSzqLLuQDxgO8te9ItEMRCSyYO5X1QJPWukVrPQ48BWycUmYj8ETg+TPAR5RSSmvt0Fq/hT+5nKCUKgasWus/a38D8M+Aq+byQRYqj9dHx6Az5P4U8N+pSH9K4jhWcCFmPOQdf5Ou4dFohyMSVDBJpQSYvGFDR+DYtGW01h5gGMidoc6OGeoEQCl1h1Jqm1JqW29vbxDhLiwdg/5FJENNKsljfaS5jsv8lATSl70apymLS4zbebVBJkKK6AgmqUzX1zF1eEkwZWZVXmv9E611vda6Pj8//zRVLkyt/f55B5W5ofWn5A3tBqA/a2XYYxKxSSsjXYUf4mLjLl7fH/x+O0KEUzBJpQMom/S6FOg8VRmllAnIBAZmqLN0hjoF/qRSkGEh1RLafmp5g7vxKhMD1mURikzEomMFF5KBA/eRP2FzuaMdjkhAwSSV94BapVSVUioJuB7YNKXMJuCWwPNrgdf0aQbLa627AJtS6pzAqK+bgedDjn6B82nN0X4nlXmh96fkDe1m0FqHz2iJQGQiVnXlnYvPkMSFvMdrjdIEJubfjEkl0EdyN/Ay0AA8rbXer5R6UCl1ZaDYY0CuUqoJuAc4MexYKdUKfAf4tFKqY9LIsbuAR4EmoBl4MTwfaeHoGnYx5vGF3J+ifG5yhvfTl70qQpGJWOU1paKqL+Sjph28tLcr2uGIBBRUm4rWejOwecqxByY9dwHXneLaylMc3wasCDbQRNTaN7v+lOyRg5h8Y/RlrY5EWCLGqaV/Rcnhlzl2aAfO8TWkJoXWdCrEXMiM+hjW2u8gOzX0TbkmOul7s9ZEIiwR6xb7p3x90PcubxxMvBGTIrokqcQorTWtfY5ZzU/JG9qNI7mQ0ZSiCEQmYl5GEbqkng3mnby4rzva0YgEI0klRvXZx3GMe2edVKTpK7GpJZexgib2NjbKNsNiXklSiVEtfXaAkEd+Jbt6SR/tlKSS6JZ+DIDzPFt563BflIMRiUSSSoxq7rGTmWImLz20/pT8wR0AklQSXf5SdG4tV5jfkyYwMa8kqcQgn9Y09zqozk8j1MWbCwe24TamyJ70iU4p1PKrOYsDbD/QyLjHF+2IRIKQpBKDuoZdjLq9VOeHvrpwwcA2+rLWoA3mCEQm4sryqzDg43z3n/lzS3+0oxEJQpJKDGru8fenhJpULOODZNmbOJ57ViTCEvGmoA5fbi1Xmrby0j6ZCCnmhySVGNTca6cgw4I1JbS7jfwBf39KT059JMIS8UYpDCs+Tr1qYNu+RjxeaQITkSdTbWOMx+ujtd9BfUVOUOWr23594nl518t4lYms4YNk2poiFaKIJ8uvxvDGNzl37C3eabmI82vzoh2RWODkTiXGtA04cXs1NQWh96dYnUexp5aiDaHtECkWsIJl+PKX8XHTn/ndblkIXESeJJUY09xrRwFVIc5PMXpHSXV1Y0utiExgIm4ZVn+CNeoQ+/btklFgIuIkqcSYph47pdkpJJtDu9vIcLahgJE0SSpiipXXoVF8xP0GbzfJREgRWdKnEkNcbi/Hhkb54OLQd7jMtB/Bq0zYU0pnLiwWtCe3tp107MKcej7e/xZffPUQXcOuoOq58ezycIcmEoDcqcSQI30OfBpqZjE/JdPejC2tEm2QvxPEyY6WXEGl6sbUvQO3jAITESRJJYY09doxGxXlOaHtn5I0PkTKeD/D6WdEKDIR79oKL8GtkriCP3LouC3a4YgFTJJKDGnusVOZm4bJGNqvJdPRAsBwWnUkwhILgMecTkfRxVxlfJvGdtlmWESOJJUYMeJy02Mbm9XSLJn2FsZNGYxaZA6COLXmsmuxKidVPa/KKDARMZJUYkTTcf/SLCHPT9E+Mh0tDKVXQ4iLT4rE0pNTz4CllOsMr9HYPRLtcMQCJUklRhw8biMj2URxZnJI16WNdmHyuqQ/RcxMKVorruVsQyP9R/dHOxqxQElSiQEer4/DPTYWF2aEvNR9lr0JDYykVUUmOLGgtJZuxIOR9YO/Z3RcdoQU4SdJJQbsaBvC5faxpDAj5GuzbIewp5TiMYW+7bBIPC5LHs05H+JawxYa249HOxyxAElSiQGvH+zBoELvT0kZ7Sbd1cVgxuIIRSYWoraaT5Kt7OS3bop2KGIBkqQSA15v7KEyNy3kpVlKev8IwKB1SSTCEgtUb0497UnVXOHaRL8tuNn1QgRLkkqUdQ2P0thtY0lR6E1fpcdfw5WUgytJhhKLEChFU9VNLDO0M3r4jWhHIxYYSSpR9mqDfyJaqP0pJo+Dwv53/U1fMpRYhKin4gqGVQZnHf8VWutohyMWEEkqUfbK/m7OyEujwBraUOLivj9h1G4GM6TpS4TOa0zm3byPcyHv4Tgmw4tF+EhSiaIRl5t3Wvq5pK4w5GvLul9lzJyJLbUsApGJRNBb92mc2sLiw49FOxSxgEhSiaItB3txezWXLg8tqRi9Lkp6ttBedDEo+RWKWUrN4w+pl3H+6GtYbCcvly/EbMg3UhT94cBx8tKTWFOWHdJ1i3rfxOx1crRoQ4QiE4miueZWfChKGn4a7VDEAiFJJUrGPT62NPZw8bJCjIbQOtorul5kNCmXntyzIhSdSBQFJVU8ry5kbf/vSR2VPezF3AWVVJRSG5RSB5VSTUqp+6Y5b1FK/SpwfqtSqnLSufsDxw8qpT466XirUmqvUmqXUmpbOD5MPHm7qQ/bmCfkpi+Tx8minjdpL7oErUKb1yLEVAal+NOiW9FasbTxB9EORywAMyYVpZQR+CFwGVAH3KCUqptS7DZgUGtdA3wX+Gbg2jrgemA5sAF4OFDfhAu11mu01vVz/iRx5vd7ushINnF+TWhbB5f0bMHkc3G0WJq+RHhU1yzlZ95LWdz9Apm2pmiHI+JcMHcq64EmrXWL1noceArYOKXMRuCJwPNngI8o/8qIG4GntNZjWusjQFOgvoQ25vHyyoFuPrq8iCRTaC2QlZ0v4LQU0Jt9ZoSiE4kmJy2Jl7JvwIGFVYe+F+1wRJwL5hutBGif9LojcGzaMlprDzAM5M5wrQZeUUptV0rdcao3V0rdoZTappTa1tvbG0S4se+tw33YXB4+tqo4pOtSXD0U977FkZIrZdSXCKu66ip+5L6Csp7XKex7J9rhiDgWzDfTdL3IU6fgnqrM6a49T2u9Fn+z2ueUUh+c7s211j/RWtdrrevz80NrKopVL+zpwpps4rzq0JZXqTz2Owz4aCm9KkKRiUS1uDCDX5uvpEsVUn/g3zD43NEOScSpYJJKBzB5hl0pMHWYyIkySikTkAkMnO5arfXEYw/wHAnSLOZye/nDgeOhN31pTfWx39KTvRZbWkXkAhQJyWhQrKws4stjnyLT0cLi1v+JdkgiTgXzrfYeUKuUqlJKJeHveJ+6ZvYm4JbA82uB17R/QaFNwPWB0WFVQC3wrlIqTSmVAaCUSgMuBfbN/ePEvtcae7CNebhi9aKQrssb2oXV0Upz6dURikwkuvrKHLbotexMPoeVTY/AUPvMFwkxxYxJJdBHcjfwMtAAPK213q+UelApdWWg2GNArlKqCbgHuC9w7X7gaeAA8BLwOa21FygE3lJK7QbeBV7QWr8U3o8Wm57d0UFBhoXzakJr+qpufxa3MZX2oksjFJlIdJkpZpYWWfkH503+A5vuBp8vukGJuGMKppDWejOwecqxByY9dwHXneLarwFfm3KsBVgdarDxrs8+xpaDvdx2flVIEx6Txoeo6HqJ1pKP4TGlRjBCkejWV+Xw310j/K70s3y85d9h22Ow/vZohyXiiAwhmke/292Jx6f5+NrSkK6r7ngWk8/FwYobIxSZEH41BenkpCXx/4bOg+qL4A8PQN/haIcl4ogklXn07I5jLF9kDWlDLuXzsPjoU3TnrGdYtg0WEWZQinPPyOXowCgHzvo6mJLh6Zth3Bnt0EScCKr5S8xdQ9cIe48N89XLpy5GcHqlPa+T5upie90/RigyEe+q234d1vqKjQZeM1Tz8KsH+MHK6+Ddn8DProTVN859Q7j6W8MTpIhZcqcyT57c2kaSycA1a6fOGz29Ja2/wJ6yiGMFH45MYEJMkWr0cXH+EC8es9CRthxqL4WO96D1zWiHJuKAJJV54Bjz8NzOY1y+spis1KSgr8sf2EHB4A4OVnxSFo8U82pDwSAAjzelwuKPQuEK2P8cdCfEyH8xB5JU5sHvdndiH/Nw49nlIV23vPknuJJyaCq7JkKRCTG9vCQPV5aN8WRLCgPjRjjzU5BZCjt/BoOt0Q5PxDBJKhGmteZ/traxpDCDdRXBb8aVPbyfRX1v01j5KbwyjFhEweeWOnB54bHDqWCywPo7wJIBW38kEyPFKUlSibDtRwfZe2yYT55Tjgqhk3NF808ZN2VwqPz6CEYnxKnVWL38VekYTzSlMDyu/Anl3LvBnApbH4FhSSziZJJUIuynb7aQlWrmmnXBz03JGdpH2fH/5WDlTXjM6RGMTojT+9xSJ3aPgcebUvwHUrLh3M/571z+/AOZwyJOIkklgo70OXjlwHE+eXYFqUlBjt7WmjUHv4vLnE1D5S0zlxciguqyPFy6aIzHDqUyMBa4007NhQ/8H3+CefdH0LkzukGKmCJJJYIee6sFs8HAzR8IflXh4r63KBp4l321d8pdiogJ9y63Y/coHmlM+8vBlCw49/OQVQE7noCDL4KWdcKEJJWI6bG5eGZ7B1eduYiCjOSgrlE+D2sOfqWX71IAABCaSURBVBdbahlNZdMupSbEvFuc6eXjFS6eaE6h0znpKyMpDc7+LJSth8Mv+9cJG3dEL1AREySpRMiPtrTg9mo+++GaoK+pbfsV2bbD7Fr8BXwGcwSjEyI0X6jzJ4v/2J/2/hNGE6y6AZZfA72N8MdvST9LgpOkEgHHR1z8YutRrllbQmVe2swX4N8qePWh79OZdx7tRZdEOEIhQlOW5uPWGie/OZrCjv4p/YNKQdUFcN4XwZgE7zwMBzeDzxudYEVUSVKJgIdfb8Ln03z+otqgr1nb+G0M2s22ui/PfX0lISLg88ucFCR7+eddGfimbigO/smRF9wLZWfB4VfgT98D+/F5j1NElySVMDvS5+DJd9u4rr6MspwgJy02bqai6yX2V9+OPa1s5vJCREG6WXP/Sjt7Bs386sgp+glNFv/Ck2feDI5e+OO3oekPcteSQCSphNm//v4AFpORL14S5F2KvQc2fZ4B6zIOnHFbZIMTYo6uKh9jfd44X9+bTvfoab4+StbCh++HwuXQ+AK89f/bu/foquorgePfnRvIOwQIZMJLIkRRUZ7ydLT4GMViLYgVtR3NsMq4gCqdjlMd33UtHGe1FnyUVetzfBRFwTKsqYg8asWCBJTIWyQYApGAQEIghJDs+eN3ojFNyCXce07C3Z+1zrr3nnvuOTvnnJt9z+O3f7+FsmL/AjWBsaQSQcu3lrJsSyl3XtE3vDu+VGHhz6DqMB9d9JhdnDetngg8PuQwx2uE+9aloY2dBquTkAZD8txw7BB8+AQsvg+qKnyL1/jPkkqEHKuu4Vf/u4mczBRuH5UT3odWzYFt78KVD1Oe1ieq8RkTKTlpNdzdv4KlJQnMLwrjx1P2AHfU0mOYa4X/zDDY9CdOnpFMW2VJJUJ+895WCvcf4dHr+9M+PozVWvgBvHc/9BsHw++IfoDGRFBebiXDMo/zwLpUvjgcRrcM7VNgwCSYvASSOrneJF+bCAd2RD9Y4ytLKhGQv/MAz31YyK3De3FJbmbzHzhUBPPyoHMf+OEciLPNYNqWkMDsYeUkhGDaqnSOhXsdvucwmLICrn4MilbBMyNgxeNQfSyK0Ro/2X+z01R2tJp/e3M93TOS+M9rz2v+A0f2wyvjoaYaJr0OienRD9KYKMhOruWJi8vZUtaOe9emh382KxQPI6fC9DXQ7/uwYibMGQnbl0Y1XuMPSyqnobZWmfHGJ5SUVTJ70iBSEpopGll1GF670d0Fc8tcyAy/HYsxrdGY7OP8+wUVLChKZPbmU+z3J70b3Pgi/GQBIPDqBJh7KxwojEqsxh+WVE7DrPe3sXzrPh687oLmO+CqPOiOUErWw40vwVmjfInRmGib1u8oE8+qZNamVOY21X7lZPpcDlP/BpffD18sdxfylzwIx8ojH6yJOksqLfTyRzt5ctl2fjS0Bz9urpvgw3vhpXEuofzoZTh3rD9BGuMDEZg55DCXZVVxz9r0phtGnkx8Alx6N/xsLfSfCCtnw1ODIf8Fd6rYtBmWVFpgXv4uHlq4kavOz2Lm+AtP3qPj7nXwhzHuLpdb3oDzrvMvUGN80j4Ofj+qjMuyqvjl2nSe/zypZXcMp2fD+Dnw0+XQuS8s+jk8fTGsf8Na5bcRllROgaoyZ8UX3P1WAZf0zeSpmwcRH2piFapC/ovwwjUgcZD3Z3eYb8wZKjHkEsvV3Y7x6Po07v8kleqWdrHSfbD7ztzyJrRPhQVTYM5o2PiOJZdWzpJKmI4eP8Ev3y7g8Xe3cN2Abjx/+1AS2zVxf35ZMbx6AyyaAWeNhCl/gW4D/Q3YmAAkhmDOyHLuOPcIr+1IZuLyjuwIpx1LY0TgnKvhXz+AiS9CbTXMuw2eGgKrn7W+W1opSyphWL/rEOOe+pB5a4uZPqYvs28aSEJ8I1+UqgpYPtMdrhf9Da79Nfx4AaR09j9oYwISJ3DPhUeYM6KMnRUhvv9+J363JZmqlh5gxMVB/wkwdbW7ySW5M/z5bnjifFjykPXf0sqE2XF6bCopq+Q3723jrbXFZKUn8Nrk4Yzq20jjxiP7Yc1z8PGzcPRruGACXPkQdOzte8zGtBZje1QxqHM1D3ySxn9vSGVuYRLT43bxw0Hdw6s60VAoHi4Y74ai1a7ky0dPwspZ0G0wXHQT9L8BUrtE/o8xYRNtQ/V3hg4dqvn5+VFdRm2tsq7oIK+u+pJFBSXEiZB3SW+mjelLemK9go9Vh+GLZVDwJmxb7A7NzxkL//gL15/EKXp9dVGL4u1TNK9FnzOmOcNzOkVsXn/d247HPktl06F2ZKUnMHFIDyYM7kGfLqmnN+PyEtjwNhS8AV8VuOuX3YfA2WOgzxjocTGEAi/UGlMdJIWVVETkGmA2EAKeU9X/avB+AvA/wBDga+AmVd3pvXcvMBmoAe5U1cXhzLMx0UoqpeXHWFd0kJXbv2bZllJ2H6okpX2Imy7uRd7o3vTsmASHv4K9G6B4DXz5kSsxUVsNKV3hwhthyG3Q5dwWx2BJxbQ2kUwq4O5d+aDDOF5cWcgH2/ZRq3B2lxQuO6cLA3tm0L97B3I6pxAX18L/waWbYcN892NvzzrQWneRv9sg+IcLIau/e8zMhXZJEf3bmmFJ5TsTiISAbcBVQDGwBrhZVTfVm2YqcJGq3iEik4DxqnqTiJwP/BEYBnQD3gfO8T520nk25lSTSkXVCb78+ghHqmqoqKqmoqqGsspq9hyq/GaI27eF+MpSUjlGx/gq+meGGNxVyU2qoF1FCZTvgbIiOFbm/bFx0PUC9yso9yroNcodlp8mSyqmtYl0UgFgaB7gutz+v89KWLallNWFBzh+wt0mltI+RG5WGt0zkshKTyS7QyKZae1JaR9PSkI8ye1DJLYLEYoT4gREhKR2IbplNEgSlQdh54ewY4VrH7Z3I1Qf/fb95EzXU2VGT0jLhsQMSMpwj4npEJ/ojnBCCa6L5LpmAxm9ICWM+n7fFVNJJZz/hsOA7aq6A0BE5gLXA/UTwPXAw97zt4CnxTXeuB6Yq6pVQKGIbPfmRxjzPG2rd3zN5Jf/PgnFxwnZGYl065DEzISX6VPz6bdvHvCG5ExXRqJDd1cEr0s/6Hqeu4srIS2SYRoTc7LSE8kbnUPe6Byqa2rZXlrBZ7vL2Li7jG17K9hcUs7yraUcPd781f3BvTKYP3X0d0cmdXRtwurahdXWuLZiXxW4x7JiOLQL9m1zFcOPlQNhXAq4bjYMuf2U/95YEk5S6Q7sqve6GBje1DSqekJEyoDO3vhVDT7b3Xve3DwBEJEpwBTvZYWIbA0j5mZ94R4y34T9jU9RDvhaljuTJmPxncXStNYUTxuM5V8ivuAvAZnWklha4JE8IO9UPpEJvKuq10QlnlYonKTS2KFbw5Te1DRNjW/s1o9Gfyao6rPAsycLsKVEJF9Vh0Zj3qfKYmlca4oFWlc8FkvjWmEsMZNQILx2KsVAz3qvewB7mppGROKBDriTSE19Npx5GmOMaWPCSSprgFwRyRGR9sAkYGGDaRYCt3nPJwLL1N0BsBCYJCIJIpID5AIfhzlPY4wxbUyzp7+8ayTTgcW4239fUNWNIvIrIF9VFwLPA694F+IP4JIE3nRv4i7AnwCmqWoNQGPzjPyf16yonFZrIYulca0pFmhd8VgsjbNYAtSmGj8aY4xp3az2lzHGmIixpGKMMSZiYiKpiEhPEVkuIptFZKOI3OWN7yQiS0Tkc++xmT6BIxZPooh8LCLrvXge8cbniMhqL543vJsY/IgnJCKfiMiiIOPwlr1TRD4TkU9FJN8bF9R2yhCRt0Rki7fvjAwiFhE511sfdUO5iMwIcL383NtvN4jIH739Oah99y4vjo0iMsMb59t6EZEXRKRURDbUG9fo8sV5UkS2i0iBiAyOVlxBiomkgrtJ4Beqeh4wApgmroTMPcBSVc0Flnqv/VAFXK6qA4CBwDUiMgJ4HPitF89BXM00P9wFbK73Oqg46oxR1YH12hoEtZ1m4xqu9QMG4NaR77Go6lZvfQzE1dc7CiwIIhYR6Q7cCQxV1f64G20mEcA+IyL9gZ/iqnQMAMaJSC7+rpeXgIbtUJpa/ljcHbC5uAbdc6IYV3BUNeYG4E+4umNbgWxvXDawNYBYkoF1uIoC+4F4b/xIYLEPy++B2/EvBxbhGqz6Hke9eHYCmQ3G+b6dgHSgEO9mliBjabD8fwJWBrhe6qpndMLdPboIuDqgffdGXDHautcPAP/h93oBegMbmttHgN/jahz+3XRn0hArRyrfEJHewCBgNZClqiUA3mNXH+MIicinQCmwBFc55pCqnvAmqV/SJppm4b6IdR2/dg4ojjoKvCcia8WV6IFgttPZwD7gRe/U4HMikhJQLPVNwhVpJYhYVHU38GugCCgByoC1BLPPbAAuFZHOIpIMXItrVB30Nmpq+Y2VvPLzu+WLmEoqIpIKvA3MUNXyIGNR1Rp1pzN64A7fz2tssmjGICLjgFJVXVt/tN9xNDBaVQfjThVME5FLfVx2ffHAYGCOqg4CjuDfabdGedcpfgAEVprauz5wPZCDqzyegttWDUV9n1HVzbjTbkuAd4H1uFPdrVXQ3y1fxExSEZF2uITymqrO90bvFZFs7/1s3FGDr1T1ELACd60nQ1yZG/CndM1o4AcishOYizsFNiuAOL6hqnu8x1LcdYNhBLOdioFiVV3tvX4Ll2SC3GfGAutUda/3OohYrgQKVXWfqlYD84FRBLTPqOrzqjpYVS/FNbz+nOC/100tPybKU8VEUhERwbX636yqT9R7q355mdtw11r8iKeLiGR4z5NwX9TNwHJcmRtf4lHVe1W1h6r2xp1WWaaqt/odRx0RSRGRtLrnuOsHGwhgO6nqV8AuEanree0KXGWIQPYZz818e+qLgGIpAkaISLL3vapbL0HtM129x17ABNz6CXIbcZLlLwT+2bsLbARQVnea7IwS9EUdPwbgEtxhZgHwqTdci7t+sBT362Yp0MmneC4CPvHi2QA86I0/G1cbbTvuFEeCj+voe8CiIOPwlrveGzYC93njg9pOA4F8bzu9A3QMMJZkXK+qHeqNCyqWR4At3r77CpAQ4D7zV1xSWw9c4fd6wSWxEqAadyQyuanl405/PYO7fvoZ7g66qK8jvwcr02KMMSZiYuL0lzHGGH9YUjHGGBMxllSMMcZEjCUVY4wxEWNJxRhjTMRYUjHGGBMxllSMMcZEjCUVExNE5B2vSOXGukKVIjJZRLaJyAoR+YOIPO2N7yIib4vIGm8YHWz0xrQd1vjRxAQR6aSqB7yyOGtw5dpX4up5HQaWAetVdbqIvA78TlU/9Mp/LFbXF48xphnxzU9izBnhThEZ7z3vCfwE+IuqHgAQkXnAOd77VwLnu9JWAKSLSJqqHvYzYGPaIksq5ownIt/DJYqRqnpURFbgOkhq6ugjzpu20p8IjTlz2DUVEws6AAe9hNIP181AMnCZiHT0SrbfUG/694DpdS9EZKCv0RrThllSMbHgXSBeRAqAR4FVwG5gJq4H0PdxlW7LvOnvBIaKSIGIbALu8D9kY9omu1BvYpaIpKpqhXeksgB4QVUXBB2XMW2ZHamYWPawiHyK6xekENdnijHmNNiRijHGmIixIxVjjDERY0nFGGNMxFhSMcYYEzGWVIwxxkSMJRVjjDER8/+d0UQzWvSA6QAAAABJRU5ErkJggg==
">
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="OBSERVATION:">OBSERVATION:<a class="anchor-link" href="#OBSERVATION:">¶</a></h1><ol>
<li>The survival chance is high when people who age is in range 30-40</li>
<li>People whose age is in the range 40-60 have higher chance of not surviving.</li>
<li>People whose age is in the range 60–75 have equal chances of surviving and not surviving.</li>
<li>Overall. we cannot separate the data based on the age alone.</li>
</ol>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[13]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">sns</span><span class="o">.</span><span class="n">FacetGrid</span><span class="p">(</span><span class="n">df</span><span class="p">,</span><span class="n">hue</span><span class="o">=</span><span class="s1">'status'</span><span class="p">,</span><span class="n">size</span> <span class="o">=</span> <span class="mi">5</span><span class="p">)</span><span class="o">.</span><span class="n">map</span><span class="p">(</span><span class="n">sns</span><span class="o">.</span><span class="n">distplot</span><span class="p">,</span><span class="s2">"year"</span><span class="p">)</span><span class="o">.</span> <span class="n">add_legend</span><span class="p">();</span>
<span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>


<div class="output_subarea output_stream output_stderr output_text">
<pre>C:\Anaconda3\lib\site-packages\matplotlib\axes\_axes.py:6462: UserWarning: The 'normed' kwarg is deprecated, and has been replaced by the 'density' kwarg.
  warnings.warn("The 'normed' kwarg is deprecated, and has been "
C:\Anaconda3\lib\site-packages\matplotlib\axes\_axes.py:6462: UserWarning: The 'normed' kwarg is deprecated, and has been replaced by the 'density' kwarg.
  warnings.warn("The 'normed' kwarg is deprecated, and has been "
</pre>
</div>
</div>

<div class="output_area">

<div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
">
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="Observation">Observation<a class="anchor-link" href="#Observation">¶</a></h1><ol>
<li>From 1958 to 1960, the operated patients survival rate is higher.</li>
<li>From 1960 to 1965, the operated patients not survived is high.</li>
<li>Overall, this plot gets overlapped</li>
</ol>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[14]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">sns</span><span class="o">.</span><span class="n">FacetGrid</span><span class="p">(</span><span class="n">df</span><span class="p">,</span><span class="n">hue</span><span class="o">=</span><span class="s1">'status'</span><span class="p">,</span><span class="n">size</span> <span class="o">=</span> <span class="mi">5</span><span class="p">)</span><span class="o">.</span><span class="n">map</span><span class="p">(</span><span class="n">sns</span><span class="o">.</span><span class="n">distplot</span><span class="p">,</span><span class="s2">"nodes"</span><span class="p">)</span><span class="o">.</span> <span class="n">add_legend</span><span class="p">();</span>
<span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>


<div class="output_subarea output_stream output_stderr output_text">
<pre>C:\Anaconda3\lib\site-packages\matplotlib\axes\_axes.py:6462: UserWarning: The 'normed' kwarg is deprecated, and has been replaced by the 'density' kwarg.
  warnings.warn("The 'normed' kwarg is deprecated, and has been "
C:\Anaconda3\lib\site-packages\matplotlib\axes\_axes.py:6462: UserWarning: The 'normed' kwarg is deprecated, and has been replaced by the 'density' kwarg.
  warnings.warn("The 'normed' kwarg is deprecated, and has been "
</pre>
</div>
</div>

<div class="output_area">

<div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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BzBu3LjYypUrixOJBE8++eTY9PY1a9ZEzj333Pbvfve728aOHRvfuHFjUS41a4zFJ23ROOWREAEztVhExDevvPJKyc033zwtEAgQCoXcPffcs/n3v/99+eLFi+dPmDAhtmzZsnVHH310x/z584+aMWNG16JFi/amX3vllVfuztzvH/7hH7Z+7GMfmzd58uTYEUcc0dne3h4AuPHGG6dt2rQp4pyzM844o/WUU07pzKVmc8O0YGJdXZ1bsWLFsHzvofCVn65i2cYmPn/OPB78w7t0xhJcf/Y8Lj95xnCXJiL5wQBWr1696bjjjts93MX4afXq1eOPO+64WenH6grzSWtnnIpirwEYUYtFRAqYgsUnbdEYlcXeyZHFGmMRkQKmYPFJWzROZYnXYtEYi4gUMgWLT9q6YlSkWiyRUIDuRFIX/BKRgqRg8UnmGEtx2JsCrlaLiBQiBYsPnHPs7coYvA95b6vGWUSkEClYfNDRnSCRdPsG7yNqsYhInkomkyxatGjhT3/608r0tvvvv3/smWeeOd+v76ETJH2QvshXeoylOOzldZdaLCLSj/teeGe8n8e75v1z+zxHJhAI8MMf/nDzJZdcMveCCy54Mx6P29e//vWpS5cu9e2S8goWH6TXCasoDtEWjVMc8losWohSRPLRiSeeGP3Qhz7U8nd/93eT2tvbg5/61KcajzrqqK677rpr3H333TchFotZXV3d3oceeui9ZDLJxRdfPPvNN98scc7ZlVde2XDrrbfu6uv4ChYfpFc2riwJ0xaNZ4yxqCtMRPLTnXfeue3YY4+tLSoqSq5evXrt8uXLi5988skxK1euXBsOh7nssstm/uhHP6pesGBBV1NTU2jdunVvAmSzrL6CxQfpa7FoVpiIjBSVlZXJiy66qKm8vDxRUlLifvGLX1S+9tprZcccc0wtQDQaDUybNq37oosuatm4cWPxVVddNf2CCy5o+fjHP97a37EVLD5Ij7FU7lvSRWMsIpL/AoEAgYD3eeWc47LLLtv9ve99b1vP/dasWbPmZz/7WdVdd9014fHHHx/7yCOPbO7zuENUb0HZP8biDd4XBQMYGmMRkZFj8eLFbU8++WT19u3bQwA7duwIrl+/vmjbtm2hZDLJX/zFXzTffvvt215//fXS/o6lFosPOrq9YCkt8rrAzIxIOKAxFhEZMU466aTOm266ads555yzIJlMEg6H3T333LM5GAxy9dVXz3LOYWb84z/+Y31/x1Kw+CCaGkspCe8f0yoOab0wEelff9ODh9K3v/3tA7q9rr322qZrr722qed+a9eufXMgx1VXmA86YwlCASMU3P92RsK67r2IFCYFiw+iscS+mWBpxaGgBu9FpCApWHwQjSUPCpZIOECXxlhEpAApWHzQFUvsW8YlLRIKqitMRAqSgsUHnb11hYUDGrwXkYKkYPFB9BAtlq6EgkVECo+CxQfRWPKAqcYARaEAsXiSZFJXkRSR/GJmi66++upp6ce33XbbxK985StT/Dq+zmPxQTSeoDxy4FtZFAzgUs+VFultFpFD+MO/+bpsPqd/sd/zYoqKitzSpUvHbt++fcfkyZPjvn5/1GLxRWd3gkjo4BYLQHuXBvBFJL8Eg0H36U9/uuGf/umfJvZ8bt26dUWnnnrqggULFtSeeuqpC9avX1800OMrWHzQFU8eNMaSDpb0ci8iIvnka1/72q4nnniiurGx8YC/iq+99toZl19+eeO6devevOSSSxqvu+666QM9toLFB9FY4uAxlqBaLCKSv6qrq5MXX3xx4x133DEhc/urr75ads011zQBXHfddU2vvPJK+UCPrWDxQW9n3kfUYhGRPHfzzTfvXLJkyfj29nZfs0DB4oPOXqYb7+8KU4tFRPLTxIkTEx/96EeblyxZsm8CwQknnNB+//33jwW49957q+vq6vYO9LgKlhw553pd0kVjLCIyEtxyyy079uzZs2/q6g9+8IP3Hn744fELFiyofeSRR8bdc889WwZ6TM2DzVF6PbCDu8K8xxpjEZE+ZTE92G8dHR2vpu9Pnz493tnZue/xwoULu19++eV1uRxfLZYcpZdtUYtFRMSjYMlRZ2qhyYPGWNKzwjTGIiIFRsGSo/QKxsU9TpAMBw0DOrrUYhGRwqJgyVE0dTGvkqIDg8XMKAoF1GIRkZ6SyWTShrsIv6R+lgNW3FWw5Ci6b4zl4LeyKBTQGIuI9PRGQ0ND1WgIl2QyaQ0NDVXAG5nbNSssR53dvXeFgTfOollhIpIpHo9/bseOHffv2LHjaEb+H/dJ4I14PP65zI0Klhylu8Ii4YODJaIWi4j0sGjRol3AhcNdx1DKKi3N7Dwze9vMNpjZTb08/xUze9PMXjOz35jZTP9LzU9dqcH7nmuFgdcVphaLiBSafoPFzILA3cBioBa4zMxqe+z2KlDnnDsWeBy40+9C85XGWEREDpRNi+UkYINzbqNzrht4FPhY5g7Oud855zpSD18GplEg9p/H0luLJahZYSJScLIJlqlA5lox9alth/JZ4Be9PWFm15jZCjNb0dDQkH2VeSzaR1dYJBjQeSwiUnCyCZbepsT1eiF3M/szoA74Zm/PO+fuc87VOefqampqsq8yj0UPsaQLoPNYRKQgZTMrrB7IvILYNGBbz53M7APALcBZzrkuf8rLf+kWS/r6K5k0xiIihSibFstyYL6ZzTazIuBS4KnMHczsBOBe4ELn3C7/y8xf0ViColCAQODghl1RKEAs4eiOJ3t5pYjI6NRvsDjn4sANwLPAWuCnzrk1Zna7maXnYn8TKAceM7NVZvbUIQ436vR2WeK09EKUarWISCHJ6gRJ59xSYGmPbbdl3P+Az3WNGN5FvnrP53T3WHt3gjGlh7MqEZHhM9KXExh20fjB17tP23dNFs0ME5EComDJUWd3otd1wmB/sGhmmIgUEgVLjqLxJMVFarGIiKQpWHIUjSUo7mWqMUAkmLruvVosIlJAFCw56oplMcaiWWEiUkAULDnqjCUOOSts3xiLVjgWkQKiYMlRNJY85HksEbVYRKQAKVhyFO2jKyycOkFyrwbvRaSAKFhy1FewBANGcThAu4JFRAqIgiVH0ViSyCHGWAAqisO0RRUsIlI4FCw5SCQd3YlDj7EAVBSHFCwiUlAULDnoih/66pFpFcVhWqOxw1WSiMiwU7DkYN9Fvg5xgiRApVosIlJgFCw56Ot692leV5haLCJSOBQsOdh3vftDrBUGUFkcplUtFhEpIAqWHOy/LLFaLCIiaQqWHOwbY+lnunE0liSW0OWJRaQwKFhyEM1yjAXQAL6IFAwFSw72jbH0M90YUHeYiBQMBUsO9neFqcUiIpKmYMnB/q6wvsZYvGDRSZIiUigULDnI5jyW/9vQCMDS17azZNl7h6UuEZHhpGDJQTaD9+nn0t1mIiKjnYIlB13x/qcbp5d7SbduRERGOwVLDqKxBGZQFDz02xhJt1jiChYRKQwKlhx0dicoDgUxs0PuEwwY4aDRpa4wESkQCpYcROOJPtcJSysOB/eNx4iIjHYKlhxEY8k+l8xPKw4pWESkcChYctDX9e4zFYcDROPqChORwqBgyUE0ltg3ON8XdYWJSCFRsOQgGktS0sdU4zQvWNRiEZHCoGDJwYC6wtRiEZECoWDJQTSeZbBo8F5ECoiCJQed3Yk+z7pPi4SDxJOOeFLdYSIy+ilYchCNJbPuCkvvLyIy2ilYctCVZVdY+kJgnd3qDhOR0U/BkgPvBMn+gyV9Fcm9XbrYl4iMfgqWHHTGshtjKY94F/tSsIhIIQgNdwEjVSyRJJF0B13vfu57jx20b00sCMwnsn05rFjR/8HrrvKpShGRw08tlkHK5iJfaeWhBAEcLbH+9xURGekULIOUnuGVTVdYwKAqHGdPTA1EERn9FCyDlG6xZLNWGEBVKEFLXMEiIqOfgmWQ0sHSc4zlUMaE4+xRV5iIFAAFyyDt7wrLssUSjtOirjARKQAKlkFKX8M+mzEWgDHhBHviIZwbyqpERIZfVp+KZnaemb1tZhvM7KZenn+/ma00s7iZfdL/MvNP+iz6rFssoTgJZ7TEbCjLEhEZdv0Gi5kFgbuBxUAtcJmZ1fbY7T3gM8ASvwvMV4MZYwFoiKqRKCKjWzafcicBG5xzG51z3cCjwMcyd3DObXLOvQYUzCqL6UsND6QrDBQsIjL6ZfMpNxXYkvG4PrVtwMzsGjNbYWYrGhoaBnOIvLFvunEWa4WB1xUGChYRGf2y+ZTrbVBgUEPQzrn7nHN1zrm6mpqawRwibwzkzHtQV5iIFI5sPuXqgekZj6cB24amnJFj3xhLUXbBUhZMErIku7sULCIyumXzKbccmG9ms82sCLgUeGpoy8p/+85jCWUXFGbe2fdqsYjIaNfvp5xzLg7cADwLrAV+6pxbY2a3m9mFAGZ2opnVAxcD95rZmqEsOh9EYwlCASMUzD4oxoTj7FKwiMgol9Wp4M65pcDSHttuy7i/HK+LrGB412IZ2BItEyIx3ttbOkQViYjkB/35PEjZXu8+05Tibra0B4nqCsUiMoopWAapK8urR2aaWtxFEmPzXi1GKSKjl4JlkNq745RmOSMsbUpxNwDvtGkxShEZvRQsg9QWjVNRHB7QayZHvGDZ2KYWi4iMXgqWQdrbFaeieGAtj+KgY2ppQi0WERnVFCyD1BaNUx4ZeEDMKU/wjlosIjKKKVgGqS0aG3BXGMDcyjjvtAV1XRYRGbUULIPUGo1TOcCuMIC5FQna4wF26kRJERml9Ok2CF3xBN3x5IDHWADmVniLUb7Tqu4wERmdFCyD0Bb1wmEwXWELq7zXrm4e+GtFREYCBcsg7A+WgbdYxkUcCyvjvLSryO+yRETygoJlENqiMWBwLRaAUyd0s7wxTJeWdhGRUUjBMgh7B9hiCcU7KInupKxjK6+tfYua5G6iCWPJms6hLFNEZFjoTL1BaE0FS1/nsVgyzoTmlVS3vklFxxYs46KbtYEIR4aPZHNjHbhaMOW7iIweCpZBSHeFVR6iK6yqbT2zdjxDcXczHZEJbK05k47iiSQtRDjRSXnHFo5qfpdz21fBczWw8CMw+TjvamAiIiOcgmUQDjl4n0wwc/szTGr6I51F41g7889oLZ9z0Ot3jzmWnyTHEmvYyHfKnyC08j+g5kg45pNQOu4w/AQiIkNHfTCDkA6W8sxg6e6An/w5k5r+yPbqk3l97l/2Gippp49r5+fJU3lw0i1Q+3Fo2ggvfBO2vTrU5YuIDCm1WAahLRqjJBwknL4scSwKSz4Fm15k06QPs3Pcyf0eY1pJNwvKOnhwQwnH1B5DZM505tX/jIqVD0EgCOfdAaHIEP8kIiL+U4tlELwl81OZnEzAE1fDpt/Dx+/NKlTSzhnfwrZohHXtJXQXjWHt7M/AnHNhxQPw4PnQum1ofgARkSGkYBmEA5bM/8Vfw9qn4MP/BMddMqDjnDa2leJAgl83jAHAWRBqL4RPPQwNb8G9Z8Hml/wuX0RkSClYBqE1GqO8OAyvPATL74dTb4BTPz/g4xQHHWePa+EPzZU0xzLWDqu9ED73G4hUwEMXwB9/hJZDFpGRQsEyCG3ROMcFNsLSv4I5Z8MHbx/0sRZPbCbp4NldYw98YsIRcM3vYN4HvO/z5Oe9sRwRkTynYBmMzia+1Ph1KJ8In3jAG2wfpEmRGHVj9vKrhrF0JXucx1JcBZc+AmfdBKv+Cx48D/ZsybF4EZGhpWAZKOf4QvvdVCUa4VMPQVnu552cP6GJvYkgLzdXHPxkIADn3OwFTOM7cN9Z8O4LOX9PEZGhomAZqFVL+BP3Es9PuQamLvLlkEeWdzIl0sVvGsaw7N0mlix7b99tnyPOh6t/651A+eOL4KW7Ne4iInlJwTIQTRtxv/hrXk4eyZpZV/p2WDM4d3wLb7eXUt/Zx3L64+d7g/oLF8Ozfwv/+QlNSRaRvKNgyVYiDk9cg7MgN3ZfT3mJvycvvn9cC0Fz/Hb3mL53LK6ES/4TPvIteO8luOcUb3ZaMulrPSIig6VgydYL34T65TSd8y9sZ9ygLvLVl6pwgkVVe3mxqZJEsp8uLjM48XNw7Ysw4Sj4+RfhgQ/DtlW+1iQiMhgKlmy8twxeuBOOu4ydM84HBnf1yP6cUd1KSzzEu7vbs3vBuLlw1VK46AfQlBrYf/yz3rpjIiLDRMHSn2irt2RL1XRYfGdO17vvzwlVeykJJHitfk/2LzKD4y+HL6yEM78Kb/0v3FXnBcyO132vUUSkPwqW/vzib6BlC/zpj6C4kp2t3kmKEyr8XyCyKOCoG7OXN7a1EB/omEnJGPiT2+BLq+DU62HdM/DDM+D+D8LKh6Frr+/1ioj0RsHSlzeegNVL4P1fgxne4pL1zd7lhKeOLRmSb3l6dSvRWJL1OwcZBBWT4EPfgBvfgA9+HaJ74Kkb4FsL4akvwOb/8xbOFBEZIlo2/1CaN8PTX4ZpJ8L7/3rf5vrmTqrLiigtGpq37pjKdipDcd5+6w0uiG2FYPXgD3b6F+G0L8CWZV6r5fXHYeWPoawGjvgIHPFRmP1+CPUxxVlEZIAULL2Jd8NjnwGH1wUW3P821Td3MG2IWisAIYMzq1t5pmEsrfHBLxWzjxnMOMW7Lb4D1v8S1j7thcwr/wGRKljwITjyozD3TyBSnvv3FJGCpmDpza/+Drat9M4XqZ59wFNbmzs5YnIvS6/46OzxLfzvrmpebKzkg/N9PHCkAo7+hHeLRWHjc/DWz+GtpfD6YxCMwOwzYcF53m3MdB+/uYgUCgVLT68/Dst+CCdf5/0VnyGZdNTv6eQDtROHtIQZJV3MKe3kd41V/L1rxaz/1/RqxYP97zO1Diaf4E1R3vmGdy7Mhl97KypXToHjr4AFi2HKCd66ZSIi/VCwZKpfAf9zPcw4rdel8Hfv7aI7nhzSrrC0D9bs4d7Nk3m6vouPTu/qdR/nYOm6VrqTxphwgtLggTPJTp6d5fhMIOgtFzN+PtReBO27YOca7/bCv3onh0YqYUItTDwKxi8Y+GWT664a2P4iMmIpWNJatsKjl3uzqi55uNcB7fo93oywwxEsZ49r4VcNY/j66nLOntRNRdg7G985WNkU4rFNJfxqW4TGrgn7XnPimDYunrybmaW9B1FWzLzLAZRPhLnnQnc77FoLu9bA9lWw5WUIhLxwmXiUd+Z/ST/L0IhIQVGwALTvhoc/Dt0d8OknoWx8r7ulpxpPG1s65CUFDD47Yye3vjWTq/+viusWdlDfEeCxTSWsagpTGkzywSndjGMPpcEkW6IRftUwhldbZnL9rO2cXt3mTyFFZTCtzrslE94Z/unWzK43gcegdDyMmwfj5kD1PCjNYSabiIx4CpbOZm8Z+j3vwZ/9DCYcechd65s7AJg6ZuhbLADzyqJ8/YQ2/nVNOVe+6LUKJka6+YvpOzhrXAvFwQPXFPvoxEb+9Z1p/Nu7U2mL7+Dk2b0dNQeBoNdSGb/A6zLbuxMa1nrXidnxmtfr4buwAAAOiklEQVSaAW+SQMVk71Y5BconQdsOb5pzDhdFE5GRobCDZe8u+K+LYffbcNkjMOv0Pnevb+5kbGmYssjhe9v+bG6Ui2Z08YddYeZXJtjV0HDIwfyKUJJb5m/h396dwoNbJjF7XBufntc5NIWZed2GFZNgzjngkl54NG6Alnpo2546GTPm7f+H74AFoGwCVEz0WjmRCm+15kild/+gW+WBX4vKNYFAZAQo3GDZvd67nsneXd604nkf6Pcl9c2dh6UbrKfysOPDU7sBaNjd975FAceXZ2/lOxunctuqCnZFA3zlqHYCg51ZlmHZu00HPD5gcoAFvNZJ5ZT921zS62bcuxMm1nrBk751NnlL5XS1ebfubFYaMG88p6xm/618IoyZ4XXZZUsTCUSGVGEGy9qfw5M3QDAMV/1v1leC3NzYTu3kyiEuLnehANw4ZytPNc/k+2+V8WpTmFuPbePIMYd5KRcLQPkE79bfh3kysT9kDri17r//7vPQ3gjtDbD1FYhH97++rAbGzoIxM6F6jteSMrVuRIZDYQVLtBV+eSusfAgmHw8X/8dBJ0AeyrqdbWxu7OAzp80a0hL9EgrAHYvaOGZsjDvfKOf8X1dzxsRuPjkzyoendlE8gKGOnZ0BHttUzG/rS2nqDjGjpIvjq/ZywkwoyvazO5tzavpSVAYLz9//2DlvxlrbNm/5nT2bvdlr9cu958Nl3mUFxs3zbgoakcOmMIIlEffC5Ll/9rpmzrgRzv7bAa2R9T+vbiUYMC44dkr/O/uoZ/fTQPxxUxPzA/Cd2gBLd1XzfGMVX9pZRUkgwWnVrVx3NJwwLkawl24y5+C15hAPbijl6S0REg6mFndTHY6zurWMF5qq+Mn2BH8+t5PL53RSHenn4mQ+6LUrLpKaTJAuurPJm0zQuMGbwbbjNe+5cGkqZOZ6679NqNV4jcgQGd3B0t4Irz4My/8dWt7zTny8/CdZd32lJZOOJ1dt44x546kZguXyh1p5KMmnpuzmk5N38+beUp7fXcWLTVX85rkAleEkx1XHmFaapDTkiCdhZzTAq41hdkaDlIeS/PncTj4zr5MdDQ0AJB2sbi3jD20T+Nc15dy1toyLZkT505lR3jcuRjiLz+u2mLF5b5CupLc+WmXYMakkQUkv/yKdg7dbg/yhqYLWeIjJkW7mlfUyKcEMSsd5t+kneds6mqBpgxc06dlra/4bSsbCzNNh1pkw6wwFjYiPzLn+/9I0s/OA7wFB4H7n3B09no8APwYWAY3AJc65TX0ds66uzq1YsWKQZR9CIu6dyLf5JXh7KWz+AyTj3ofHKdfDwsUMZn2UZRsbueS+l/nuJcdz0QlT+973sW8NtvrDqjMRYGVLGa+3lrG5M8Lu7jDdSSNgMCYcZ2ZJF8dUtnPq2LaDzujPVN9ZxC92jeWFxiq6XYCSQIJjK9uprejgw3MilAYde+PGO20hXqyPszVaxLZoEU2x3i+UNr4oxpRIN+OKYkwfU8TWjiCvNYdoiB7YdxeyJOdP6+aKOZ2cND7W66/1t+v3EE0GCJrjQ/OrvH06mrwJBptehM0vQvMmALpDFTSXzWFnZBa7S2Yz/+g6AmNnEqqcTLi0kkeXb6ErnqQ7niQSDvCX759LSVFhTJ1esuw9ABJJx96uOB86aiLjyoqoKgljg15vqCAVzJvVb7CYWRBYB3wQqAeWA5c5597M2Od64Fjn3LVmdinwcefcJX0dd1DB0t3u/dXZ3gAdjV63Vsdu2LMFGtdDwzqIpS7rO36BtzT8MRd7Z4jn4JvPvsUDL25ixa0f6Heq8UgJFr91JAK83lrKqtZyVrWU9RocJYEEU4q7mVrczZTiLqYUdxMJOBIO2hNBGrrDbEsFT3MsRIIgk0uSHDkmzmkTurGO3VSGEtRHI6zYU86LzWNoiwWYXR7nhOoYYyOOtpixaW+QjW0hdnftb4GUBB2zK+LMKU8wZ+ExTK4qpiuWoG3nu0S2vsSYxlXMSG5hnm1lvLUe+LO5CA2uit1U0eEiRIkQpYiiknLGlhd7H7LFIcqKjFDACJrzLnTkEt6khH1fkz0eJ7wVH0j9HwyEvHGgQMg738dSXwPB/dsCYe9+MPU1EPJWSAhFIFSc+pp5P/U1GPFeYwZYL18D++53Jxx7OrvZ0dzOxl0tPP3qZnbs2UtzawdGgjAJQiQYW2zMH1/MvPHFzK0OM3tMiKr65yAZZ09nkjDdTI50e3/cpW+JWO/3049xUDHFq8UCqfcjmPoa9n6GYFHqa/p+UY/tPbflcN+CB9aYjHvbB7fahIJl3w5mpwJ/75z7cOrxzQDOuX/O2OfZ1D4vmVkI2AHUuD4OPqhgeed38PBFPQoMen+BjpsHNUekzhI/EcbOHNix++Cco765k+nV/U81LtRgyeQcNMVClFeNJ5aEkpBjTkWCTdt3D6jB2HOts55jLMdOr+bp+mKW1kdY2xKiLWaUhRwzyhLMrUgQjrVRGkoQSxpEKnk3FTj1HUGSqX+ZkVCAuTXlhIPGhMpiasojVCb3cFZ1M8G2rYQ6dlLUuZuuPduoTOyh2EUJJrsooRti7SQScRLOcBhJjGTq2nkudT9JgERfX52RIIDhCJEgTJwiixMmvu+xd0tQRIwI3QRt6MezhoYdHIrB1Nd0YFrAm0LukqlbRiAnE5DoTt1iB99PnzM11N73abjwrsG8smCCJZsxlqnAlozH9cDJh9rHORc3sxZgHHDAWRdmdg1wTerhXjN7exA1j+95XGgG1gBPDuJwvuulvrwy6utbPsD91w38W4z693CI5Xt90GeN30/dBuwZ59x5gy9p5MgmWHpL2Z5/MmWzD865+4D7sviehy7GbIVzri6XYwwl1ZebfK8P8r9G1Ze7kVBjPstmGkw9kHnFp2nAtkPtk+oKqwIGP09WRERGrGyCZTkw38xmm1kRcCnwVI99ngKuTN3/JPDbvsZXRERk9Oq3Kyw1ZnID8CzedOMHnHNrzOx2YIVz7ing34GHzWwDXkvl0iGsOaeutMNA9eUm3+uD/K9R9eVuJNSYt7I6j0VERCRbOtVYRER8pWARERFfjYhgMbOLzWyNmSXNrK7Hczeb2QYze9vMPjyMNZ6XqmGDmd00XHVkMrMHzGyXmb2Rsa3azH5lZutTX8cOY33Tzex3ZrY29fv9Uj7VaGbFZvZHM1udqu8fUttnm9myVH0/SU1qGTZmFjSzV83s6Tytb5OZvW5mq8xsRWpbXvyOU7WMMbPHzeyt1L/FU/OpvpFoRAQL8Abwp8ALmRvNrBZvosBRwHnAPaklaA6r1Pe8G1gM1AKXpWobbv+B975kugn4jXNuPvCb1OPhEge+6pw7EjgF+HzqfcuXGruAc51zxwHHA+eZ2SnAvwDfSdXXDHx2mOpL+xKwNuNxvtUHcI5z7viMc0Py5XcM3jqIzzjnjgCOw3sv86m+kcc5N2JuwHNAXcbjm4GbMx4/C5w6DHWdCjx7qLqG+T2bBbyR8fhtYHLq/mTg7eGuMaO2J/HWpMu7GoFSYCXeqhO7gVBvv/thqGsa3gffucDTeCcr5019qRo2AeN7bMuL3zFQCbxLaiJTvtU3Um8jpcVyKL0tN9P38sOju45sTHTObQdIfZ0wzPUAYGazgBOAZeRRjaluplXALuBXwDvAHudcPLXLcP+uvwv8NZBegnoc+VUfeKtw/NLMXkkt6wT58zueAzQAD6a6E+83s7I8qm9EypvrsZjZr4FJvTx1i3PuUIuAZbWUzGGQL3WMSGZWDvwM+LJzrjWflmJ3ziWA481sDPDfwJG97XZ4q/KY2QXALufcK2Z2dnpzL7sO97/F051z28xsAvArM3trmOvJFALeB3zBObfMzL6Hur1yljfB4pz7wCBels1yM4dDvtSRjZ1mNtk5t93MJuP9JT5szCyMFyr/5Zx7IrU5r2oEcM7tMbPn8MaCxphZKNUqGM7f9enAhWZ2PlCM163z3TyqDwDn3LbU111m9t/ASeTP77geqHfOLUs9fhwvWPKlvhFppHeFPQVcamYRM5sNzAf+OAx1ZLPsTb7IXH7nSoZxSWjzmib/Dqx1zn0746m8qNHMalItFcysBPgA3sDu7/CWLhrW+pxzNzvnpjnnZuH9m/utc+6KfKkPwMzKzKwifR/4EN5knLz4HTvndgBbzGxhatOfAG+SJ/WNWMM9yJPNDfg43l8WXcBODhwovwWv3/ttYPEw1ng+3grs7+B13+XD+/YIsB2Ipd6/z+L1wf8GWJ/6Wj2M9Z2B103zGrAqdTs/X2oEjgVeTdX3BnBbavscvD9gNgCPAZE8+F2fDTydb/Wlalmduq1J/9/Il99xqpbjgRWp3/P/AGPzqb6ReNOSLiIi4quR3hUmIiJ5RsEiIiK+UrCIiIivFCwiIuIrBYuIiPhKwSIFx8xmZa74LCL+UrCIiIivFCwyIqVaHWvN7Eepa6X80sxKzOx4M3vZzF4zs/9OX0fDzBalrqvyEvD5jOMEzeybZrY89Zq/TG2fbGYvpK4h8oaZnTlMP6rIiKNgkZFsPnC3c+4oYA/wCeDHwN84544FXgf+X2rfB4EvOudO7XGMzwItzrkTgROBq1PLA12Ot8LD8XjX6Fg15D+NyCiRN4tQigzCu8659Af+K8BcYIxz7vnUtoeAx8ysqsf2h/Euygbe2lXHmll6ba0qvMBaDjyQWiTzfzK+j4j0Q8EiI1lXxv0EMOYQ+xmHXjre8JZMf/agJ8zeD3wEeNjMvumc+3EuxYoUCnWFyWjSAjRnjIf8OfC8c24P0GJmZ6S2X5HxmmeB61ItE8xsQWpF3pl41zr5Ed4KzO87PD+CyMinFouMNlcCPzSzUmAjcFVq+1V4XVsdeGGSdj/e5ZtXppbxbwAuwlst+GtmFgP2Ap8+LNWLjAJa3VhERHylrjAREfGVgkVERHylYBEREV8pWERExFcKFhER8ZWCRUREfKVgERERX/1/Xyqvju5zufMAAAAASUVORK5CYII=
">
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="Observation">Observation<a class="anchor-link" href="#Observation">¶</a></h1><ol>
<li>Patients having 0 or 1 node are more likely to survive.</li>
<li>Patients having more than 20 nodes are less likely to survive.</li>
</ol>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="6b.-Cumulative-Distribution-Function-(CDF)">6b. Cumulative Distribution Function (CDF)<a class="anchor-link" href="#6b.-Cumulative-Distribution-Function-(CDF)">¶</a></h1>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[15]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># For survived people</span>
<span class="n">counts1</span><span class="p">,</span> <span class="n">bin_edges1</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">histogram</span><span class="p">(</span><span class="n">survived</span><span class="p">[</span><span class="s1">'nodes'</span><span class="p">],</span> <span class="n">bins</span><span class="o">=</span><span class="mi">10</span><span class="p">,</span> <span class="n">density</span> <span class="o">=</span> <span class="kc">True</span><span class="p">)</span>
<span class="n">pdf1</span> <span class="o">=</span> <span class="n">counts1</span><span class="o">/</span><span class="p">(</span><span class="nb">sum</span><span class="p">(</span><span class="n">counts1</span><span class="p">))</span>
<span class="nb">print</span><span class="p">(</span><span class="n">pdf1</span><span class="p">);</span>
<span class="nb">print</span><span class="p">(</span><span class="n">bin_edges1</span><span class="p">)</span>
<span class="n">cdf1</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">cumsum</span><span class="p">(</span><span class="n">pdf1</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">bin_edges1</span><span class="p">[</span><span class="mi">1</span><span class="p">:],</span> <span class="n">pdf1</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">bin_edges1</span><span class="p">[</span><span class="mi">1</span><span class="p">:],</span> <span class="n">cdf1</span><span class="p">,</span> <span class="n">label</span> <span class="o">=</span> <span class="s1">'Yes'</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">xlabel</span><span class="p">(</span><span class="s1">'nodes'</span><span class="p">)</span>

<span class="nb">print</span><span class="p">(</span><span class="s2">"***********************************************************"</span><span class="p">)</span>

<span class="c1">#For not survived people</span>
<span class="n">counts2</span><span class="p">,</span> <span class="n">bin_edges2</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">histogram</span><span class="p">(</span><span class="n">not_survived</span><span class="p">[</span><span class="s1">'nodes'</span><span class="p">],</span> <span class="n">bins</span><span class="o">=</span><span class="mi">10</span><span class="p">,</span> <span class="n">density</span> <span class="o">=</span> <span class="kc">True</span><span class="p">)</span>
<span class="n">pdf2</span> <span class="o">=</span> <span class="n">counts2</span><span class="o">/</span><span class="p">(</span><span class="nb">sum</span><span class="p">(</span><span class="n">counts2</span><span class="p">))</span>
<span class="nb">print</span><span class="p">(</span><span class="n">pdf2</span><span class="p">);</span>
<span class="nb">print</span><span class="p">(</span><span class="n">bin_edges2</span><span class="p">)</span>
<span class="n">cdf2</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">cumsum</span><span class="p">(</span><span class="n">pdf2</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">bin_edges2</span><span class="p">[</span><span class="mi">1</span><span class="p">:],</span> <span class="n">pdf2</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">bin_edges2</span><span class="p">[</span><span class="mi">1</span><span class="p">:],</span> <span class="n">cdf2</span><span class="p">,</span> <span class="n">label</span> <span class="o">=</span> <span class="s1">'No'</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">xlabel</span><span class="p">(</span><span class="s1">'nodes'</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">legend</span><span class="p">()</span>
<span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>[0.83555556 0.08       0.02222222 0.02666667 0.01777778 0.00444444
 0.00888889 0.         0.         0.00444444]
[ 0.   4.6  9.2 13.8 18.4 23.  27.6 32.2 36.8 41.4 46. ]
***********************************************************
[0.56790123 0.14814815 0.13580247 0.04938272 0.07407407 0.
 0.01234568 0.         0.         0.01234568]
[ 0.   5.2 10.4 15.6 20.8 26.  31.2 36.4 41.6 46.8 52. ]
</pre>
</div>
</div>

<div class="output_area">

<div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
">
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="Observation:">Observation:<a class="anchor-link" href="#Observation:">¶</a></h1><ol>
<li>82% of people have survived with node in range of 0-4.5</li>
<li>Nearly 100% of people will not survive when the node is greater than 40</li>
</ol>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="6c.-Box-plot-with-whiskers">6c. Box plot with whiskers<a class="anchor-link" href="#6c.-Box-plot-with-whiskers">¶</a></h1>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[16]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">sns</span><span class="o">.</span><span class="n">boxplot</span><span class="p">(</span><span class="n">x</span><span class="o">=</span><span class="s1">'status'</span><span class="p">,</span><span class="n">y</span><span class="o">=</span><span class="s1">'age'</span><span class="p">,</span><span class="n">data</span><span class="o">=</span><span class="n">df</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
<span class="n">sns</span><span class="o">.</span><span class="n">boxplot</span><span class="p">(</span><span class="n">x</span><span class="o">=</span><span class="s1">'status'</span><span class="p">,</span><span class="n">y</span><span class="o">=</span><span class="s1">'year'</span><span class="p">,</span><span class="n">data</span><span class="o">=</span><span class="n">df</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
<span class="n">sns</span><span class="o">.</span><span class="n">boxplot</span><span class="p">(</span><span class="n">x</span><span class="o">=</span><span class="s1">'status'</span><span class="p">,</span><span class="n">y</span><span class="o">=</span><span class="s1">'nodes'</span><span class="p">,</span><span class="n">data</span><span class="o">=</span><span class="n">df</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
">
</div>

</div>

<div class="output_area">

<div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAYIAAAEKCAYAAAAfGVI8AAAABHNCSVQICAgIfAhkiAAAAAlwSFlzAAALEgAACxIB0t1+/AAAADl0RVh0U29mdHdhcmUAbWF0cGxvdGxpYiB2ZXJzaW9uIDIuMi4yLCBodHRwOi8vbWF0cGxvdGxpYi5vcmcvhp/UCwAAEXlJREFUeJzt3X2QXXV9x/H3h6Q8agg2gWo0RgyCrYLEpRVbUcC2io6KItMZO4NozWjbJeKgolaUP6QtatuYttRUwCc6U0x96AOgyDjj0FY0CUGBpLKiQALBIMpTgAh8+8e9kZBJdpck595Nfu/XDJO95557zmd3DvvZ8/hLVSFJatdeww4gSRoui0CSGmcRSFLjLAJJapxFIEmNswgkqXEWgSQ1ziKQpMZZBJLUuOnDDjAZs2bNqnnz5g07hiTtVlasWHFXVc2eaL7dogjmzZvH8uXLhx1DknYrSW6ZzHweGpKkxlkEktQ4i0CSGmcRSFLjLAJJapxFIEmNswgkqXG7xX0Ee4IlS5YwNjY27BisW7cOgDlz5gw1x/z58xkdHR1qBj1uKmyfU2XbhPa2T4ugMQ8++OCwI0jb5LY5PNkdBq8fGRkp7yzeNRYtWgTA4sWLh5xEeiK3zV0vyYqqGploPs8RSFLjLAJJapxFIEmNswgkqXEWgSQ1ziKQpMZZBJLUOItAkhpnEUhS4ywCSWqcRSBJjbMIJKlxFoEkNa7TIkgyM8myJGuSrE5ybJIXJflOklVJlif57S4zSJLG1/V4BIuBK6rqlCR7A/sDlwLnVtXlSU4Czgde0XEOSdJ2dFYESWYAxwFvBaiqTcCmJAXM6M92IHB7VxkkSRPrco/gUGADcHGSo4AVwCLg3cDXk3yC3qGpl27rw0kWAgsB5s6d22FMSWpbl+cIpgMLgAuq6mjgAeBs4F3AmVX1LOBM4MJtfbiqllbVSFWNzJ49u8OYktS2LotgLbC2qq7pv15GrxhOA77cn/YlwJPFkjREnRVBVa0HbktyeH/SicCN9M4JvLw/7QTgpq4ySJIm1vVVQ6PAJf0rhm4GTge+BixOMh14iP55AEnScHRaBFW1ChjZavLVwIu7XK8kafK8s1iSGmcRSFLjLAJJapxFIEmNswgkqXEWgSQ1ziKQpMZZBJLUOItAkhpnEUhS4ywCSWqcRSBJjbMIJKlxFoEkNc4ikKTGWQSS1DiLQJIaZxFIUuMsAklqnEUgSY2zCCSpcRaBJDXOIpCkxlkEktQ4i0CSGmcRSFLjOi2CJDOTLEuyJsnqJMf2p48m+b8kNyQ5v8sMkqTxTe94+YuBK6rqlCR7A/snOR54PXBkVT2c5OCOM0iSxtFZESSZARwHvBWgqjYBm5K8C/irqnq4P/2nXWWQJE2syz2CQ4ENwMVJjgJWAIuA5wEvS/Ix4CHgrKr6Xoc5WLJkCWNjY12uYrex+eewaNGiISeZGubPn8/o6OiwY0hD1WURTAcWAKNVdU2SxcDZ/ekHAS8BjgEuTXJoVdWWH06yEFgIMHfu3J0KMjY2xqrrV/Po/k/bqeXsCfba1Psxr7j5ziEnGb5pG+8edgRpSuiyCNYCa6vqmv7rZfSKYC3w5f4v/u8meQyYRW/v4VeqaimwFGBkZOQJJbEjHt3/aTx4xEk7uxjtQfZbc9mwI0hTQmdXDVXVeuC2JIf3J50I3Ah8FTgBIMnzgL2Bu7rKIUkaX9dXDY0Cl/SvGLoZOB14ALgoyfXAJuC0rQ8LSZIGp9MiqKpVwMg23vrjLtcrSZo87yyWpMZZBJLUOItAkhpnEUhS4ywCSWqcRSBJjbMIJKlxFoEkNc4ikKTGWQSS1DiLQJIaZxFIUuO6fvqopHE4et7jHD3viQY5ep5FIA3R2NgYN91wLXOf8uiwowzd3r/sHaB4+JblQ04yfLfeP22g67MIpCGb+5RH+eCCe4cdQ1PIeStnDHR9niOQpMZZBJLUOItAkhpnEUhS4ywCSWqcRSBJjbMIJKlxFoEkNc4ikKTGWQSS1DiLQJIaZxFIUuM6LYIkM5MsS7Imyeokx27x3llJKsmsLjNIksbX9dNHFwNXVNUpSfYG9gdI8izg94FbO16/JGkCne0RJJkBHAdcCFBVm6rqF/23/xZ4H1BdrV+SNDldHho6FNgAXJzk2iSfSXJAktcB66rqug7XLUmapHGLIMleSV66g8ueDiwALqiqo4EHgI8CHwLOmejDSRYmWZ5k+YYNG3YwgiRpIuMWQVU9BnxyB5e9FlhbVdf0Xy+jVwzPAa5L8hPgmcDKJL+xjXUvraqRqhqZPXv2DkaQJE1kMoeGvpHkTUnyZBZcVeuB25Ic3p90IrCyqg6uqnlVNY9eWSzozytJGoLJXDX0HuAA4JEkDwEBqqomM6jmKHBJ/4qhm4HTdzipJKkTExZBVT11RxdeVauAkXHen7ejy5Yk7RqTuo8gyUHAYcC+m6dV1be7CiVJGpwJiyDJnwCL6J3YXQW8BPhf4IRuo0mSBmEyJ4sXAccAt1TV8cDR9O4PkCTtASZTBA9V1UMASfapqjXA4RN8RpK0m5jMOYK1SWYCXwWuTPJz4PZuY0mSBmUyVw2d3P/yo0m+BRwIXNFpKknSwEz2qqHfAw6rqouTzAbmAD/uNJkkaSAmPEeQ5CPA+4EP9Cf9GvDFLkNJkgZnMieLTwZeR++hcVTV7cAO32QmSZpaJlMEm6qq6I8dkOSAbiNJkgZpMkVwaZJPAzOTvAP4JvDP3caSJA3KZE4WP0zvl/+99O4fOKeqruw0lSRpYCZTBIfQu7t4JXARvVLYraxbt45pG+9hvzWXDTuKppBpG3/GunWPDDXDunXreOC+aZy3cjIP81UrbrlvGgesWzew9U14aKiq/oLeA+cuBN4K3JTkvCTP7TibJGkAJnUfQVVVkvXAeuAR4CBgWZIrq+p9XQbcFebMmcP6h6fz4BEnDTuKppD91lzGnDmHDDXDnDlzePiRO/jggnuHmkNTy3krZ7DPnDkDW99knj56BnAacBfwGeC9VfXLJHsBNwFTvggkSds3mT2CWcAbq+qWLSdW1WNJXttNLEnSoEzmWUPnjPPe6l0bR5I0aJO5j0CStAezCCSpcRaBJDXOIpCkxlkEktQ4i0CSGmcRSFLjLAJJapxFIEmN67QIksxMsizJmiSrkxyb5OP9199P8pUkM7vMIEkaX9d7BIuBK6rqCOAoYDVwJfCCqjoS+CHwgY4zSJLG0VkRJJkBHEdvHAOqalNV/aKqvlFVm0cD+Q7wzK4ySJIm1uUewaHABuDiJNcm+cw2Br5/G3B5hxkkSRPosgimAwuAC6rqaOAB4OzNbyb5EL1Bbi7Z1oeTLEyyPMnyDRs2dBhTktrWZRGsBdZW1TX918voFQNJTgNeC7ylqmpbH66qpVU1UlUjs2fP7jCmJLWtsyKoqvXAbUkO7086EbgxyauA9wOvq6qNXa1fkjQ5kxqzeCeMApck2Ru4GTgd+B6wD3BlEoDvVNU7O84hSdqOTougqlYBI1tNnt/lOiVJT453FktS4ywCSWqcRSBJjbMIJKlxFoEkNc4ikKTGWQSS1DiLQJIaZxFIUuMsAklqnEUgSY2zCCSpcRaBJDXOIpCkxlkEktQ4i0CSGmcRSFLjLAJJapxFIEmNswgkqXEWgSQ1ziKQpMZZBJLUOItAkhpnEUhS4ywCSWqcRSBJjeu0CJLMTLIsyZokq5Mcm+RpSa5MclP/34O6zCBJGl/XewSLgSuq6gjgKGA1cDZwVVUdBlzVfy1JGpLOiiDJDOA44EKAqtpUVb8AXg98rj/b54A3dJVBkjSx6R0u+1BgA3BxkqOAFcAi4JCqugOgqu5IcnCHGX5l2sa72W/NZYNY1ZS210P3AvDYvjOGnGT4pm28Gzhk2DGkoeuyCKYDC4DRqromyWKexGGgJAuBhQBz587dqSDz58/fqc/vScbG7gNg/qH+AoRD3DYkui2CtcDaqrqm/3oZvSK4M8nT+3sDTwd+uq0PV9VSYCnAyMhI7UyQ0dHRnfn4HmXRokUALF68eMhJJE0VnZ0jqKr1wG1JDu9POhG4Efh34LT+tNOAr3WVQZI0sS73CABGgUuS7A3cDJxOr3wuTfJ24FbgzR1nkCSNo9MiqKpVwMg23jqxy/VKkibPO4slqXEWgSQ1ziKQpMZZBJLUOItAkhpnEUhS4ywCSWqcRSBJjbMIJKlxFoEkNc4ikKTGWQSS1Liunz4qaQK33j+N81Y6YtydG3t/lx6y/2NDTjJ8t94/jcMGuD6LQBoiR0h73KaxMQD2ebY/k8MY7LZhEUhD5Oh5j3P0vOHxHIEkNc4ikKTGWQSS1DiLQJIaZxFIUuMsAklqnEUgSY2zCCSpcRaBJDXOIpCkxlkEktQ4i0CSGtfpQ+eS/AS4D3gUeKSqRpK8CPgnYF/gEeBPq+q7XeaQJG3fIJ4+enxV3bXF6/OBc6vq8iQn9V+/YgA5JEnbMIxDQwVsHoXjQOD2IWSQJPWlqrpbePJj4Of0fvl/uqqWJnk+8HUg9IropVV1y3jLGRkZqeXLl3eWcxCWLFnCWH/gjWHanGHYA6LMnz/fZ/FPIVNh+5wq2+bmDHvC9plkRVWNTDRf14eGfreqbk9yMHBlkjXAKcCZVfVvSU4FLgReufUHkywEFgLMnTu345jt2G+//YYdQdomt83h6XSP4AkrSj4K3A98GJhZVZUkwD1VNe6ArXvCHoEkDdpk9wg6O0eQ5IAkT938NfAHwPX0zgm8vD/bCcBNXWWQJE2sy0NDhwBf6f3Rz3TgX6rqiiT3A4uTTAceon/4R5I0HJ0VQVXdDBy1jelXAy/uar2SpCfHO4slqXEWgSQ1ziKQpMZZBJLUOItAkho3sBvKdkaSDcC4j6HQkzILuGvCuaTBc9vctZ5dVbMnmmm3KALtWkmWT+ZuQ2nQ3DaHw0NDktQ4i0CSGmcRtGnpsANI2+G2OQSeI5CkxrlHIEmNswj2MOm5Osmrt5h2apIrhplL2lKSSvLJLV6f1R+zRENgEexhqnes753A3yTZtz8WxMeAPxtuMukJHgbemGTWsIPIItgjVdX1wH8A7wc+Any+qn6U5LQk302yKsk/JtkryfQkX0jygyTXJzljuOnViEfonRg+c+s3kjw7yVVJvt//17FqO9b1mMUannOBlcAmYCTJC4CTgZdW1SNJlgJ/BPwImFVVLwRIMnNYgdWcfwC+n+T8rab/Pb0/Xj6X5G3Ap4A3DDxdQyyCPVRVPZDkX4H7q+rhJK8EjgGW90eN2w+4Dfg6cHiSxcBlwDeGlVltqap7k3weOAN4cIu3jgXe2P/6C8DWRaFdzCLYsz3W/w8gwEVV9eGtZ0pyJPBqev9DvgmHD9Xg/B29PdeLx5nHa9w75jmCdnwTOHXzybkkv55kbpLZ9O4n+RK98wkLhhlSbamqu4FLgbdvMfl/6B22BHgLcPWgc7XGPYJGVNUPkpwLfDPJXsAv6V1d9ChwYXrHi4reCWZpkD4J/PkWr88ALkryXmADcPpQUjXEO4slqXEeGpKkxlkEktQ4i0CSGmcRSFLjLAJJapxFIG1Hkncn2X9XzSdNVV4+Km1Hkp8AI1V1166YT5qq3COQgCQHJPmvJNf1n8L6EeAZwLeSfKs/zwVJlie5oX9zHv2ntW493/1bLPeUJJ/tf/3m/rKvS/LtAX+L0nZ5Z7HU8yrg9qp6DUCSA+nd0Xr8Fn/pf6iq7k4yDbgqyZFV9akk79lqvu05B/jDqlrnU141lbhHIPX8AHhlkr9O8rKqumcb85yaZCVwLfBbwG8+yXX8N/DZJO8Apu1cXGnXcY9AAqrqh0leDJwE/GWSJzyOO8lzgLOAY6rq5/3DPftub3FbfP2rearqnUl+B3gNsCrJi6rqZ7vy+5B2hHsEEpDkGcDGqvoi8Al6T2G9D3hqf5YZwAPAPUkOoffY7s22nA/gziTP7z/c7+Qt1vHcqrqmqs4B7gKe1dk3JD0J7hFIPS8EPp7kMXpPZn0XvQFSLk9yR1Udn+Ra4AbgZnqHeTZbuuV8wNnAf9Ib+Od64Cn9+T6e5DB6Y0NcBVw3gO9LmpCXj0pS4zw0JEmNswgkqXEWgSQ1ziKQpMZZBJLUOItAkhpnEUhS4ywCSWrc/wOVyWMLu9hTzQAAAABJRU5ErkJggg==
">
</div>

</div>

<div class="output_area">

<div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
">
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="Observation">Observation<a class="anchor-link" href="#Observation">¶</a></h1><ol>
<li>Patients with 1 nodes or less than 1 node are likely to survive. </li>
<li>Chances of survival reduces when the number of node increase.</li>
</ol>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="6d.-Violin-Plot">6d. Violin Plot<a class="anchor-link" href="#6d.-Violin-Plot">¶</a></h1>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[17]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">sns</span><span class="o">.</span><span class="n">violinplot</span><span class="p">(</span><span class="n">x</span><span class="o">=</span><span class="s2">"status"</span><span class="p">,</span><span class="n">y</span><span class="o">=</span><span class="s2">"age"</span><span class="p">,</span><span class="n">data</span> <span class="o">=</span> <span class="n">df</span><span class="p">,</span><span class="n">height</span> <span class="o">=</span> <span class="mi">10</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
<span class="n">sns</span><span class="o">.</span><span class="n">violinplot</span><span class="p">(</span><span class="n">x</span><span class="o">=</span><span class="s2">"status"</span><span class="p">,</span><span class="n">y</span><span class="o">=</span><span class="s2">"year"</span><span class="p">,</span><span class="n">data</span> <span class="o">=</span> <span class="n">df</span><span class="p">,</span><span class="n">height</span> <span class="o">=</span> <span class="mi">10</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
<span class="n">sns</span><span class="o">.</span><span class="n">violinplot</span><span class="p">(</span><span class="n">x</span><span class="o">=</span><span class="s2">"status"</span><span class="p">,</span><span class="n">y</span><span class="o">=</span><span class="s2">"nodes"</span><span class="p">,</span><span class="n">data</span> <span class="o">=</span> <span class="n">df</span><span class="p">,</span><span class="n">height</span> <span class="o">=</span> <span class="mi">10</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
">
</div>

</div>

<div class="output_area">

<div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
">
</div>

</div>

<div class="output_area">

<div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
">
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="Observation">Observation<a class="anchor-link" href="#Observation">¶</a></h1><ol>
<li>People who got operated in the year 1965 did not survive for more than 5 years comparatively.</li>
<li>Comparatively, more people survived more than 5 years when they have node less than 1 but there are people who were not survived as well. This means that people having no nodes can also not survive more than 5 years.</li>
<li>People at the age of 50 has higher chance of not surviving fo rmore than 5 years.</li>
</ol>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="7.-Bi-variate-analysis">7. Bi-variate analysis<a class="anchor-link" href="#7.-Bi-variate-analysis">¶</a></h1>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="7a.-Scatter-plot">7a. Scatter plot<a class="anchor-link" href="#7a.-Scatter-plot">¶</a></h2>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[18]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">sns</span><span class="o">.</span><span class="n">set_style</span><span class="p">(</span><span class="s2">"whitegrid"</span><span class="p">)</span>
<span class="n">sns</span><span class="o">.</span><span class="n">FacetGrid</span><span class="p">(</span><span class="n">df</span><span class="p">,</span> <span class="n">hue</span> <span class="o">=</span> <span class="s2">"status"</span> <span class="p">,</span> <span class="n">size</span> <span class="o">=</span> <span class="mi">6</span><span class="p">)</span>\
 <span class="o">.</span><span class="n">map</span><span class="p">(</span><span class="n">plt</span><span class="o">.</span><span class="n">scatter</span><span class="p">,</span><span class="s2">"age"</span><span class="p">,</span><span class="s2">"year"</span><span class="p">)</span>\
 <span class="o">.</span><span class="n">add_legend</span><span class="p">()</span>
<span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
">
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="7b.-Pair-plot">7b. Pair plot<a class="anchor-link" href="#7b.-Pair-plot">¶</a></h1>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[19]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">sns</span><span class="o">.</span><span class="n">set_style</span><span class="p">(</span><span class="s2">"whitegrid"</span><span class="p">)</span>
<span class="n">sns</span><span class="o">.</span><span class="n">pairplot</span><span class="p">(</span><span class="n">df</span><span class="p">,</span> <span class="n">hue</span><span class="o">=</span><span class="s2">"status"</span><span class="p">,</span> <span class="n">size</span> <span class="o">=</span> <span class="mi">5</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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UnIe6oOBitvc7Llmxyr3XEvnctjzU1mbm5UhE6ivar9W2iatlj9WiTJ9Rw9GKj6XZv232r5O9ik3BpheDz44jtk1n+sLdhN1rHLjgN1td+RY8lwPoo4j8liirgcZ+xIREZHThGdrevvtt6HrOpYtW4ZTTjml4DnV/gZ3KNtSKDD0aCWTh1m2JlVVoGkakIofyTgTjgIozSxjPLd0H5qml2S8AUoz7gSDKrKZbFXZmqAoptlxtGymMFtTyMgCYbbfastglq2p7H4B08w/lbajqpqfB9MsQwpMy2X23HLnx8pzza4bXTPPdGTWNjqUistQLoOSWbYkTS/dr5W2EZmtqVz/LddX7VJLnxpUPe6ajAGqybciqyXqOGbXvN1ZjUQfy2x8sTv7VI5s14Oo44g8lqjrQca+ZBfGnLGGMWf8h/XzL5nr5gfCFmcqYddkJetFJWu9ANbNj2StFyB33Ypx3DUnW30A1skvZKuTbPWxAxdnrOHijP+wfv4lc938wLsfKxARERERERER1QBhAYGJiIiIiIjIxKJjXDims98QIiJr+M0ZIiIiIiIiIiIX8ZszREREREREOQ5/i4URPYjIDBdniIiIiIjIkyYMPCX8mK4EISaimsefNRERERERERERuYiLM0RERERERERELuLiDBERERERERGRixhzhoiIiIiIaBDj3BCRG7g4Q0RERERE5CJXFoSEH5GIhsOfNRERERERERERuYjfnCEiIiIiIqoxE+54zsG97zbdumf5Zx08JpG/cXGGiIiIiIiInLfoGBeO+Tfhh3R24cucHXGLJlt9gQttKzNF13Xd7ULkvPHGG24XgYjIU8466yxH989xl4ioEMddIiKxnB53/cJTizNERERERERERLWGAYGJiIiIiIiIiFzExRkiIiIiIiIiIhf5PiBwNpvFwoUL8ac//QmBQAD33nsvdF3HHXfcAUVRcNppp+Gee+6BqvpzHaqnpwef//zn8b3vfQ/BYFCael122WUYPXo0AOCEE07Av/7rv2Lp0qUIBAI4//zzceONN7pcwpH77ne/i//93/9FOp1GZ2cnzjnnHN+ft2eeeQY/+tGPAADJZBLbt2/H2rVrpThn6XQad9xxB959912oqorFixdL1decUtyHp0+fjgceeADBYBDt7e245ZZbXC6hNTL22+I6nXHGGVi8eDECgQDC4TBWrFiBcePGuV1MS4rrdMUVVwAAnn32Waxbtw5PP/20yyW0prg+H//4x7Fw4UIcOnQI2WwW9913H8aPH+92MS0xu+7uueceBAIBTJgwAUuXLvVdX/ISTdOwaNEi7Ny5E+FwGEuWLMFJJ53kdrFs8dvf/hYPPPAA1q5di7179/p+DM5Jp9O466678O677yKVSuHLX/4yTj31VGnqJ/t7MUDe92OA3O/JfEn3uRdeeEG/4447dF3X9VdffVWfN2+efv311+uvvvqqruu6fvfdd+s///nP3SziiKVSKf0rX/mKfvHFF+u7du2Spl4DAwP6pZdeWrDtc5/7nL53715d0zT9uuuu0//whz+4VLrqvPrqq/r111+vZ7NZPRaL6StXrpTmvOUsWrRI7+7uluacvfDCC/r8+fN1Xdf1V155Rb/xxhulO2d2M+vDl156qf7OO+/omqbpHR0d+o4dO1wqnXUy9luzOn3hC1/Q//jHP+q6rutdXV36smXLXC6lNWZ10nVd/+Mf/6jPnj1bv+KKK1wuoTVm9bn99tv15557Ttd1Xd+8ebP+y1/+0t1CWmRWp6985Sv6Sy+9pOu6rt966636iy++6HIp/e1nP/uZfvvtt+u6rutvvvmmPm/ePJdLZI/HH39c/5d/+Zehfuz3MTjfhg0b9CVLlui6ruu9vb36xz72ManqJ/N7MV2X9/2Yrsv9nsyv/LvMN+iTn/wkFi9eDAB47733MG7cOGzbtg3nnHMOAODCCy/Eb37zGzeLOGIrVqxAR0cHjj32WACQpl47duxAf38/rr32WsyePRtbtmxBKpXC+PHjoSgKzj//fGzevNntYo7IK6+8gokTJ+KGG27AvHnzcNFFF0lz3gDg97//PXbt2oXPfvaz0pyzk08+GdlsFpqmIRaLIRgMSnXOnFDch9966y1MnjwZH374IdLpNJLJJAKBgNvFrJiM/dasTg8++CAmTzaSZGazWdTV1blcSmvM6tTX14cHHngAd911l9vFs8ysPlu3bsX777+Pa665Bs8+++zQNegXZnXKjQ26riMejyMY9P2Xtl31xhtv4IILLgAATJkyBX/4wx9cLpE9xo8fj0ceeWTob7+Pwfk+9alP4aabbhr6OxAISFU/md+LAfK+HwPkfk/mV1LMkMFgELfffjteeOEFrFy5Er/85S+hKAoAIBqN4vDhwy6X0LpnnnkGTU1NuOCCC/D4448DAHRd9329AGDUqFGYM2cOrrjiCuzZswdz585FY2Pj0L9Ho1H8+c9/drGEI9fX14f33nsPjz32GPbv348vf/nL0pw3wPi6+g033IBYLIaGhoah7X4+Z5FIBO+++y4+/elPo6+vD4899hi2bNkizTlzglkf7ujowLx58zBmzBhMmjQJra2tbhezYjL2W7M6/fSnPwUAbN26FevWrcP69etdLqU1xXWaN28eTjnlFNx1112+W2gCzM/Ru+++i8bGRnz/+9/Ht7/9bTzxxBMFb+q8zqxO//7v/45vfvObePTRRzF69Gice+65bhfT14rn30AggEwm4/tFr0suuQT79+8f+tvvY3C+aDQKwDh38+fPx80334wVK1ZIUz9AzvdigNzvxwC535P5lb9H8jwrVqzA1772NVx55ZVIJpND2+PxeMFF5hcbN26EoijYvHkztm/fjttvvx29vb1D/+7XegHGNxVOOukkKIqCk08+GaNHj8aHH3449O9+rtuYMWPQ2tqKcDiM1tZW1NXV4a9//evQv/u5bocOHcLu3btx3nnnIRaLIR6PD/2bn+v1/e9/H+effz6++tWv4i9/+QuuvvpqpNPpoX/3c92cUtyHA4EA7r//fmzatAnHHXcc7rvvPnzve9/Ddddd53ZRKyJjvzWrU29vL1577TU8+uijePzxx9HU1OR2MS0prtNf//pXBAIBLFq0CMlkErt27cLSpUuxYMECt4taEbNzlM1m8fGPfxwA8PGPfxwPPfSQy6W0xqxOX/va1/Dss8/itNNOw/r167F8+XLcc889bhfVtxoaGgrmX03TfL8wYyY/hocfx+Bif/nLX3DDDTdg1qxZmD59Ou6///6hf5OhfoB878UAud+PAXK/J/Mr3/+s6b/+67/w3e9+FwBQX18PRVFwxhln4LXXXgMAbNq0CWeffbabRRyR9evXY926dVi7di0mT56MFStW4MILL/R9vQBgw4YNWL58OQDg/fffR39/PyKRCPbt2wdd1/HKK6/4tm5nnXUWXn75Zei6PlS39vZ2Kc7bli1b8I//+I8AjJvDUCgkxTlrbGwcCoR2zDHHIJPJ4PTTT5finDmluA+n02mccMIJiEQiAIBjjz0Whw4dcrOIlsjYb83qtGnTpqF55cQTT3S7iJYV1+m4447Dj3/8Y6xduxYPPvggTj31VN8szADm5+gTn/gEfvWrXwEwxtxTTz3V5VJaY1an8ePHD33Tw29jgxedeeaZ2LRpEwDgrbfewsSJE10ukTNkmocPHjyIa6+9FrfddhtmzpwJQK76yfpeDJD7/Rgg93syv1J0XdfdLkQ1EokE7rzzThw8eBCZTAZz587FKaecgrvvvhvpdBqtra1YsmSJr+IfFPviF7+IRYsWQVVVKeqVSqVw55134r333oOiKPja174GVVWxbNkyZLNZnH/++b7L9JLvvvvuw2uvvQZd13HLLbfghBNOkOK8rVq1CsFgENdccw0A46ZQhnMWj8dx11134cCBA0in05g9ezbOOOMMKc6ZU8z6cE9PDx5//HHU1dVh9OjRWL58OY455hi3i1oxGfttcZ2++tWv4vjjjx/6FGzatGmYP3++y6W0prhOudgb+/fvx6233oof/OAHLpfQmuL6tLa2YuHChejv70dDQwO+9a1v+aofAaV1qq+vH8rkFgqFsHjxYpxwwgluF9O3ctma3n77bei6jmXLluGUU05xu1i2yO/Hf/rTn3w/BucsWbIEzz//fMHPfRcsWIAlS5ZIUb9aeC8GyPd+DJD/PZkf+X5xhoiIiIiIiIjIz3z/syYiIiIiIiIiIj/j4gwRERERERERkYu4OENERERERERE5CIuzhARERERERERuYiLM0RERERERERELuLiDBERERERUQ268sorsX//freLQUTg4gwRERERERERkauCbheAyA2xWAwLFizA4cOH0dfXhyuuuAJnnHEGvvGNbyAajaK5uRl1dXVYvnw51q5dix//+MdQFAWf+cxnMHv2bLeLT0TkG1/96lcxffp0XHTRRfi///s/rFixAuPGjcPevXuhaRpuvvlmnHvuufjpT3+K9evXD73u4YcfxjvvvIMHHngAoVAIV155JS677DIXa0JE5F3PPPMMfvWrX2FgYAD79u3D3Llz0dbWhsWLFyMQCKCurg6LFy/G3/3d3+Ghhx7Cyy+/jI985CPo6+sDABw+fBgLFiwY+nvhwoWYNGkS7rjjDuzbtw/JZBJz5szBZz7zGTerSSQ1Ls5QTdq7dy8++9nP4uKLL8b777+PL37xi4hGo7jvvvtw2mmn4aGHHsL777+PXbt24Sc/+QmeeuopKIqCa665Bueffz5aW1vdrgIRkS9cccUV6OrqwkUXXYQNGzZg6tSpiMViWLZsGfr6+nDVVVfhueeew549e/D444+jvr4eX//61/HKK6/guOOOQzKZxA9/+EO3q0FE5HmxWAyrV6/Gnj17MG/ePEQiESxduhSTJ0/GL37xCyxfvhw33ngjtmzZgg0bNiCRSODiiy8GADz22GM477zzMGvWLOzZswd33nknnnjiCbz22mvYuHEjAODXv/61m9Ujkh4XZ6gmjRs3DmvWrMHPRSzOdQAAA0pJREFUf/5zNDQ0IJPJ4IMPPsBpp50GADjrrLPwk5/8BG+//Tbee+89XHPNNQCAv/3tb9i3bx8XZ4iIKnTuuedi6dKl6Onpwa9//WtMnToVW7duxe9+9zsAQCaTQV9fH5qbm3H77bcjGo1i9+7dmDJlCgDg5JNPdrP4RES+0dbWBgA4/vjjkUqlEIvFMHnyZADAtGnT8K1vfQu7du3CGWecAVVV0dDQgIkTJwIA3n77bbz66qt4/vnnAQCHDh1CQ0MD7r77btx9992IxWL43Oc+507FiGoEF2eoJn3ve9/DlClTMGvWLLz66qv41a9+hY985CPYtWsXTj31VPz2t78FALS2tuLUU0/FqlWroCgKvv/97w9NYkREdHSKomD69OlYunQp/t//+384/vjjcfzxx2PevHkYGBjAo48+imAwiJUrV+Kll14CAPzbv/0bdF0HAKgqw+MREVVCUZSCv4899ljs2LEDbW1t2LJlCyZMmICTTz4ZTz75JDRNw8DAAHbt2gXAuOf93Oc+h+nTp6Onpwc//OEP8cEHH2Dbtm34z//8TySTSXzsYx/DpZdeimCQbyGJnMCeRTXpn/7pn7Bo0SI8++yzGDNmDAKBAL7+9a/jrrvuQiQSQSgUwnHHHYe2tja0t7ejs7MTqVQKH/3oR3Hccce5XXwiIl/5/Oc/j4suugj//d//jRNPPBELFy7EVVddhVgshlmzZqGhoQFnnnkmLr/8ckQiETQ2NuKDDz7ACSec4HbRiYh8a8mSJVi8eDF0XUcgEMCyZctw4okn4lOf+hRmzpyJY489Fs3NzQCAefPmYcGCBfjBD36AWCyGG2+8ES0tLThw4AAuu+wyRCIRXHvttVyYIXKQouc+miKqcevXr8enP/1pNDU14aGHHkIoFMKNN97odrGIiHzv/fffx3/8x39gzZo1bheFiIiIyJO49Ek0qLm5Gddeey0ikQhGjx6N5cuXu10kIiLf+9nPfoZvf/vbWLp0qdtFISIiIvIsfnOGiIiIiIiIiMhFjLJHREREREREROQiLs4QEREREREREbmIizNERERERERERC7i4gwRERERERERkYu4OENERERERERE5CIuzhARERERERERuej/B+SujbeMjCgIAAAAAElFTkSuQmCC
">
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="Observation">Observation<a class="anchor-link" href="#Observation">¶</a></h1><ol>
<li>Amongst all the pair plots, age vs nodes can able to distinguish between survivors and non-survivors when compared with others. </li>
</ol>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="8.-Multivariate-Analysis">8. Multivariate Analysis<a class="anchor-link" href="#8.-Multivariate-Analysis">¶</a></h1><h2 id="8a.-Contour-Plot">8a. Contour Plot<a class="anchor-link" href="#8a.-Contour-Plot">¶</a></h2>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[20]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">sns</span><span class="o">.</span><span class="n">jointplot</span><span class="p">(</span><span class="n">x</span> <span class="o">=</span> <span class="s1">'age'</span><span class="p">,</span> <span class="n">y</span> <span class="o">=</span> <span class="s1">'year'</span><span class="p">,</span> <span class="n">data</span> <span class="o">=</span> <span class="n">df</span><span class="p">,</span> <span class="n">kind</span> <span class="o">=</span> <span class="s2">"kde"</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
">
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="Observation">Observation<a class="anchor-link" href="#Observation">¶</a></h1><ol>
<li>People who got operated from 1960 to 1964 are at the age between 45 and 55</li>
</ol>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="Overall-Conclusion:">Overall Conclusion:<a class="anchor-link" href="#Overall-Conclusion:">¶</a></h1><ol>
<li>Survival chance is inversely proportional to the number of nodes. The absence of nodes cannot always guarantee survival. [Violin plot {node vs status}]</li>
<li>People less than 35 years have more chance of survival but Patient’s age and operation year alone are not deciding factors for his/her survival.[PDF{age},Scatter plot{age vs year}]</li>
<li>Age vs nodes might able to distinguish between survivors and non-survivors when compared with others but not perfectly. [Pair plot {ave vs nodes}]</li>
<li>Since the data is imbalance, the objective of classifying the survival status of a new patient based on the given features is a difficult task.</li>
</ol>

</div>
</div>
</div>
    </div>
  </div>


 



</body></html>
