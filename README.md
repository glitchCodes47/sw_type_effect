# sw_type_effect

Create MorebBlok 
typerString("Text")setTextTo(textview)delayfor(delay);

s = ""; 

n = 0;

t = new TimerTask() {

 @Override

 public void run() {

  runOnUiThread(new Runnable() {

   @Override

   public void run() {

    if (!(n == _Text.length())) {

     String jg = ""+_Text;

     char ug = jg.charAt((int) n);

     s = s+""+ug;

     _textview.setText(s);

     n++;

    }

    else {

     t.cancel();

    }

   }

  });

 }

};

_timer.scheduleAtFixedRate(t, (int)(_delay), (int)(_delay));

