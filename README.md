*, *:before, *:after {
-moz-box-sizing: border-box; -webkit-box-sizing: border-box; box-sizing: border-box;
}

body {
 overflow: hidden;
 font-family: 'HelveticaNeue-UltraLight', 'Helvetica Neue UltraLight', 'Helvetica Neue', Arial, Helvetica, sans-serif;
 font-weight: 100;
 color: rgba(255, 255, 255, 1);
 margin: 0;
 padding: 0;
 background: #4A4A4A;
 -webkit-touch-callout: none;
 -webkit-user-select: none;
 -khtml-user-select: none;
 -moz-user-select: none;
 -ms-user-select: none;
 user-select: none;
}

#calendar {
  -webkit-transform: translate3d(0, 0, 0);
  -moz-transform: translate3d(0, 0, 0);
  transform: translate3d(0, 0, 0);
  width: 420px;
  margin: 0 auto;
  height: 570px;
  overflow: hidden;
}

.header {
  height: 50px;
  width: 420px;
  background: rgba(66, 66, 66, 1);
  text-align: center;
  position:relative;
  z-index: 100;
}

.header h1 {
  margin: 0;
  padding: 0;
  font-size: 20px;
  line-height: 50px;
  font-weight: 100;
  letter-spacing: 1px;
}

.left, .right {
  position: absolute;
  width: 0px;
  height: 0px;
  border-style: solid;
  top: 50%;
  margin-top: -7.5px;
  cursor: pointer;
}

.left {
  border-width: 7.5px 10px 7.5px 0;
  border-color: transparent rgba(160, 159, 160, 1) transparent transparent;
  left: 20px;
}

.right {
  border-width: 7.5px 0 7.5px 10px;
  border-color: transparent transparent transparent rgba(160, 159, 160, 1);
  right: 20px;
}

.month {
  /*overflow: hidden;*/
  opacity: 0;
}

.month.new {
  -webkit-animation: fadeIn 1s ease-out;
  opacity: 1;
}

.month.in.next {
  -webkit-animation: moveFromTopFadeMonth .4s ease-out;
  -moz-animation: moveFromTopFadeMonth .4s ease-out;
  animation: moveFromTopFadeMonth .4s ease-out;
  opacity: 1;
}

.month.out.next {
  -webkit-animation: moveToTopFadeMonth .4s ease-in;
  -moz-animation: moveToTopFadeMonth .4s ease-in;
  animation: moveToTopFadeMonth .4s ease-in;
  opacity: 1;
}

.month.in.prev {
  -webkit-animation: moveFromBottomFadeMonth .4s ease-out;
  -moz-animation: moveFromBottomFadeMonth .4s ease-out;
  animation: moveFromBottomFadeMonth .4s ease-out;
  opacity: 1;
}

.month.out.prev {
  -webkit-animation: moveToBottomFadeMonth .4s ease-in;
  -moz-animation: moveToBottomFadeMonth .4s ease-in;
  animation: moveToBottomFadeMonth .4s ease-in;
  opacity: 1;
}

.week {
 background: #4A4A4A;
}

.day {
  display: inline-block;
  width: 60px;
  padding: 10px;
  text-align: center;
  vertical-align: top;
  cursor: pointer;
  background: #4A4A4A;
  position: relative;
  z-index: 100;
}

.day.other {
 color: rgba(255, 255, 255, .3);
}

.day.today {
  color: rgba(156, 202, 235, 1);
}

.day-name {
  font-size: 9px;
  text-transform: uppercase;
  margin-bottom: 5px;
  color: rgba(255, 255, 255, .5);
  letter-spacing: .7px;
}

.day-number {
  font-size: 24px;
  letter-spacing: 1.5px;
}


.day .day-events {
  list-style: none;
  margin-top: 3px;
  text-align: center;
  height: 12px;
  line-height: 6px;
  overflow: hidden;
}

.day .day-events span {
  vertical-align: top;
  display: inline-block;
  padding: 0;
  margin: 0;
  width: 5px;
  height: 5px;
  line-height: 5px;
  margin: 0 1px;
}

.blue { background: rgba(156, 202, 235, 1); }
.orange { background: rgba(247, 167, 0, 1); }
.green { background: rgba(153, 198, 109, 1); }
.yellow { background: rgba(249, 233, 0, 1); }

.details {
  position: relative;
  width: 420px;
  height: 75px;
  background: rgba(164, 164, 164, 1);
  margin-top: 5px;
  border-radius: 4px;
}

.details.in {
  -webkit-animation: moveFromTopFade .5s ease both;
  -moz-animation: moveFromTopFade .5s ease both;
  animation: moveFromTopFade .5s ease both;
}

.details.out {
  -webkit-animation: moveToTopFade .5s ease both;
  -moz-animation: moveToTopFade .5s ease both;
  animation: moveToTopFade .5s ease both;
}

.arrow {
  position: absolute;
  top: -5px;
  left: 50%;
  margin-left: -2px;
  width: 0px;
  height: 0px;
  border-style: solid;
  border-width: 0 5px 5px 5px;
  border-color: transparent transparent rgba(164, 164, 164, 1) transparent;
  transition: all 0.7s ease;
}

.events {
  height: 75px;
  padding: 7px 0;
  overflow-y: auto;
  overflow-x: hidden;
}

.events.in {
  -webkit-animation: fadeIn .3s ease both;
  -moz-animation: fadeIn .3s ease both;
  animation: fadeIn .3s ease both;
}

.events.in {
  -webkit-animation-delay: .3s;
  -moz-animation-delay: .3s;
  animation-delay: .3s;
}

.details.out .events {
  -webkit-animation: fadeOutShrink .4s ease both;
  -moz-animation: fadeOutShink .4s ease both;
  animation: fadeOutShink .4s ease both;
}

.events.out {
  -webkit-animation: fadeOut .3s ease both;
  -moz-animation: fadeOut .3s ease both;
  animation: fadeOut .3s ease both;
}

.event {
  font-size: 16px;
  line-height: 22px;
  letter-spacing: .5px;
  padding: 2px 16px;
  vertical-align: top;
}

.event.empty {
  color: #eee;
}

.event-category {
  height: 10px;
  width: 10px;
  display: inline-block;
  margin: 6px 0 0;
  vertical-align: top;
}

.event span {
  display: inline-block;
  padding: 0 0 0 7px;
}

.legend {
  position: absolute;
  bottom: 0;
  width: 100%;
  height: 30px;
  background: rgba(60, 60, 60, 1);
  line-height: 30px;

}

.entry {
  position: relative;
  padding: 0 0 0 25px;
  font-size: 13px;
  display: inline-block;
  line-height: 30px;
  background: transparent;
}

.entry:after {
  position: absolute;
  content: '';
  height: 5px;
  width: 5px;
  top: 12px;
  left: 14px;
}

.entry.blue:after { background: rgba(156, 202, 235, 1); }
.entry.orange:after { background: rgba(247, 167, 0, 1); }
.entry.green:after { background: rgba(153, 198, 109, 1); }
.entry.yellow:after { background: rgba(249, 233, 0, 1); }

/* Animations are cool!  */
@-webkit-keyframes moveFromTopFade {
  from { opacity: .3; height:0px; margin-top:0px; -webkit-transform: translateY(-100%); }
}
@-moz-keyframes moveFromTopFade {
  from { height:0px; margin-top:0px; -moz-transform: translateY(-100%); }
}
@keyframes moveFromTopFade {
  from { height:0px; margin-top:0px; transform: translateY(-100%); }
}

@-webkit-keyframes moveToTopFade {
  to { opacity: .3; height:0px; margin-top:0px; opacity: 0.3; -webkit-transform: translateY(-100%); }
}
@-moz-keyframes moveToTopFade {
  to { height:0px; -moz-transform: translateY(-100%); }
}
@keyframes moveToTopFade {
  to { height:0px; transform: translateY(-100%); }
}

@-webkit-keyframes moveToTopFadeMonth {
  to { opacity: 0; -webkit-transform: translateY(-30%) scale(.95); }
}
@-moz-keyframes moveToTopFadeMonth {
  to { opacity: 0; -moz-transform: translateY(-30%); }
}
@keyframes moveToTopFadeMonth {
  to { opacity: 0; -moz-transform: translateY(-30%); }
}

@-webkit-keyframes moveFromTopFadeMonth {
  from { opacity: 0; -webkit-transform: translateY(30%) scale(.95); }
}
@-moz-keyframes moveFromTopFadeMonth {
  from { opacity: 0; -moz-transform: translateY(30%); }
}
@keyframes moveFromTopFadeMonth {
  from { opacity: 0; -moz-transform: translateY(30%); }
}

@-webkit-keyframes moveToBottomFadeMonth {
  to { opacity: 0; -webkit-transform: translateY(30%) scale(.95); }
}
@-moz-keyframes moveToBottomFadeMonth {
  to { opacity: 0; -webkit-transform: translateY(30%); }
}
@keyframes moveToBottomFadeMonth {
  to { opacity: 0; -webkit-transform: translateY(30%); }
}

@-webkit-keyframes moveFromBottomFadeMonth {
  from { opacity: 0; -webkit-transform: translateY(-30%) scale(.95); }
}
@-moz-keyframes moveFromBottomFadeMonth {
  from { opacity: 0; -webkit-transform: translateY(-30%); }
}
@keyframes moveFromBottomFadeMonth {
  from { opacity: 0; -webkit-transform: translateY(-30%); }
}

@-webkit-keyframes fadeIn  {
  from { opacity: 0; }
}
@-moz-keyframes fadeIn  {
  from { opacity: 0; }
}
@keyframes fadeIn  {
  from { opacity: 0; }
}

@-webkit-keyframes fadeOut  {
  to { opacity: 0; }
}
@-moz-keyframes fadeOut  {
  to { opacity: 0; }
}
@keyframes fadeOut  {
  to { opacity: 0; }
}

@-webkit-keyframes fadeOutShink  {
  to { opacity: 0; padding: 0px; height: 0px; }
}
@-moz-keyframes fadeOutShink  {
  to { opacity: 0; padding: 0px; height: 0px; }
}
@keyframes fadeOutShink  {
  to { opacity: 0; padding: 0px; height: 0px; }
}
