FOR Ver r.

Sampling method: DPM++ 2M Karras or DPM++ SDE Karras are recommended.

(2M is faster and easy to handle the lighting effects. SDE can provide much more realistic image, so you can choose what you want.)

When you use SDE Karras for sampling, Sampling step size should be more than twice the CFG scale(and it means it will takes more time to generate images).

Upscaler: ESRGAN_4x or SwinlR_4x

Dynamic Thresholding is STRONGLY RECOMMENDED. Here's my setting about DT;

When you use 2M Karras - CFG Scale: 20~30, Mimic CFG Scale: 10, Top percentile of latents to clamp: 99~100, Mimic Scale Scheduler: Half cosine up, Mimic Scale Schedule: 0, CFG Scale Scheduler: Half cosine up, CFG Scale Schedule: 10

When you use SDE Karras - CFG Scale: 20 or 25 or 30 or more(I recommend a multiple of five), Sampling steps: 50 Mimic CFG Scale: ~10, Top percentile of latents to clamp: 99~100, Mimic Scale Scheduler: Half cosine up, Mimic Scale Schedule: 0, CFG Scale Scheduler: Half cosine up, CFG Scale Schedule: 10
If you raise CFG Scale Scheduler, you can get more realistic images, but girl's face would get older. For me, CFG schedule 7~10 was satisfying. Of course, you can try other options for your best shot.
