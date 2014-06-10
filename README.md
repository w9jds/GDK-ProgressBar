GDK-ProgressBar
===============

ProgressBar for Glass GDK Menu Cards that look and work exactly like the ones Google Use.

Examples:

Indeterminate

![Indeterminate Progress](http://1.bp.blogspot.com/-WlmMyIIZEv8/Us4n2PsEmoI/AAAAAAAAKZ8/IVUXtQ8NdSg/s1600/device-2014-01-08-212834.png)

Progress

![Indeterminate Progress](http://2.bp.blogspot.com/-S8urgDIJ690/Us4n2NpOFEI/AAAAAAAAKZ4/Snewld6WnKo/s1600/device-2014-01-08-222839.png)


To show the indeterminate progressbar:

```

    mSliderView.startIndeterminate();

```

To get the setting time create a call like this:

```

    mSliderView.startProgress(1000, new Animator.AnimatorListener()
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
