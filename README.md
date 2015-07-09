# AnimationDemo
EasingAnimationDemo
This is a demo 
for using esing animation for nineoldandroids.animation

##How to
```
AnimatorSet set = new AnimatorSet();
set.playTogether(
		ObjectAnimator.ofFloat(tv, "translationY", 0, dipToPixels(this, -(160 - 3))),
		MyAnimator.Build(ObjectAnimator.ofFloat(tv, "translationY", 0, dipToPixels(this, -(160 - 3))),
				new EvaluatorHolder.BackEaseOut(1200),
				new BaseEvaluator.AnimListener() {
					@Override
					public void on(float time, float value, float start, float end, float duration) {
						System.out.println("time: -> " + time + "-value: -> " + value);
					}
				})
);
set.setDuration(1200);
set.start();
```