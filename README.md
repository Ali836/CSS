# CSS
html, body {
  font-family: Helvetica, sans-serif; }

.wrapper {
  position: absolute;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  margin: auto; }

input {
  position: absolute; }

input.grow {
  -webkit-animation: grow 0.8s cubic-bezier(0.175, 0.885, 0.32, 1.275);
  -moz-animation: grow 0.8s cubic-bezier(0.175, 0.885, 0.32, 1.275);
  animation: grow 0.8s cubic-bezier(0.175, 0.885, 0.32, 1.275); }

@-webkit-keyframes grow {
  0% {
    -webkit-transform: scale(1); }
  30% {
    -webkit-transform: scale(2.5); }
  100% {
    -webkit-transform: scale(1); } }

@-moz-keyframes grow {
  0% {
    -moz-transform: scale(1); }
  30% {
    -moz-transform: scale(2.5); }
  100% {
    -moz-transform: scale(1); } }

@keyframes grow {
  0% {
    transform: scale(1); }
  30% {
    transform: scale(2.5); }
  100% {
    transform: scale(1); } }
Contact GitHub API Training Shop Blog About
