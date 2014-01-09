GDK-ProgressBar
===============

ProgressBar for Glass GDK Menu Cards that look and work exactly like the ones Google Use.

To have the indeterminate progressbar:

```

    ProgressBar.startIndeterminate();

```

To get the setting time create a call like this:

```

    ProgressBar.startProgress(1000, new Animator.AnimatorListener()
    {
        @Override
        public void onAnimationStart(Animator animation)
        { 
            //Create listener for swipe down
        }
    
        @Override
        public void onAnimationEnd(Animator animation)
        {
            setContentView(R.layout.menu_layout);
            ((ImageView)findViewById(R.id.icon)).setImageResource(R.drawable.ic_done_50);
            ((TextView)findViewById(R.id.label)).setText("Deleted");
    
            maManager.playSoundEffect(Sounds.SUCCESS);
    
            new Handler().postDelayed(new Runnable()
            {
                public void run()
                {
                    CreatePictureView();
                }
            }, 1000);
        }
    
        @Override
        public void onAnimationCancel(Animator animation)
        {
    
        }
    
        @Override
        public void onAnimationRepeat(Animator animation)
        {
    
        }
    });

```

Looks like this
