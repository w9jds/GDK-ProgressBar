GDK-ProgressBar
===============

ProgressBar for Glass GDK Menu Cards that look and work exactly like the ones Google Use.

Examples:

Indeterminate

![Indeterminate Progress](https://lh6.googleusercontent.com/bqVm9ysRT2ukdy34nkZRoo5xXWEG0pbu7ohWubOz597WfCD7emmGg4kklvIkhF9vxOhfF_tarUI)

Progress

![Indeterminate Progress](https://lh4.googleusercontent.com/ZulMxJoxh_hIdIJVwYQ_I87iyUjJ4Fdrn-pM2dSzrBa0aitOAzEOr1xeRNIxNzLdNYE0mBYO_1c)


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
