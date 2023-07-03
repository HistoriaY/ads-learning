# Control

This directory comprises methodologies of Control module, responsible for executing the trajectory or path generated by the planning module. In essence, it's the component of the autonomous driving system that directly interfaces with the vehicle's actuators — steering, brakes, and throttle — to ensure that the vehicle behaves as desired.

There are two primary forms of control in this context: longitudinal and lateral. Longitudinal control pertains to controlling the vehicle's speed and acceleration, which includes accelerating, decelerating, and maintaining a certain speed. On the other hand, lateral control involves steering the vehicle and maintaining its position within a lane.

## Table of Contents

* [PID Control](PID.md)
* [LQR Control](LQR.md)
* [Model Predictive Control](MPC.md)
* [NN-based Control](NN_based.md)

---

For more detailed knowledge, you can refer to [Optimal Control](https://books.google.com/books?hl=en&lr=lang_en|lang_ja&id=U3Gtlot_hYEC&oi=fnd&pg=PR11&dq=optimal+control&ots=wcdrD5CAkr&sig=NFYzg6q7k3TUau_IoWGLIWUG7yc), or [Modelling and Control Strategies in Path Tracking Control for Autonomous Ground Vehicles: A Review of State of the Art and Challenges](https://pdf.sciencedirectassets.com/271438/1-s2.0-S0022489822X00062/1-s2.0-S0022489822000714/main.pdf?X-Amz-Security-Token=IQoJb3JpZ2luX2VjEID%2F%2F%2F%2F%2F%2F%2F%2F%2F%2FwEaCXVzLWVhc3QtMSJHMEUCIQD2rCWTYTQTUVLzeOBFJyevA3Yz2A%2BB6N%2FMBsu5%2BGS0AwIgdK2TphZJ2fPcagCqLAcoCjWcZ%2BZioUlMdWVZ18WBWj4qvAUI6f%2F%2F%2F%2F%2F%2F%2F%2F%2F%2FARAFGgwwNTkwMDM1NDY4NjUiDJkKwIrCqfkjoSG34yqQBQdY9cpBJ%2BZiN3CrNq%2BvhriRBuUigv2Pvg%2BkRCk05ZYH4OJUbDXw4hbA9eN%2FtxO73jA0kfCkAJfySYglGL%2FFUaLnwhsKeV%2FqH64iAlRVwFMrDoj2Qq4MiI7vwHxNkGhyldaaQRH3F2npUAYMR8%2Ffp%2FyOyaAEHUT2dXEfbkRix3IVDnj9HnW5ulObn41T4SrubAI%2F7oMbfhZkfW8Ky6ih0LgFODTPJlG0FOcfuYJK09ydCLzA3KoEF%2Bx%2B9ZMkvaJaki6q%2Fb09cl2JJ0BXm%2B%2FYZ8jo3trIboyT%2FMqdhifynw%2F5UtfmpgQiUvqPipQeLi8i69isNEMLN2pLrr3ooU40lfW55hYciborB939kGHZ3%2Fge5by8MhHNHl75vXj8dVgIJwbd7RydEm7oyxem5%2FIWdIU4nlCgWFLlGVeejTEWXHqr7aWoQLWoz%2BRgJb4rFibAc%2Fnz8p7Rxl6ahwaEsUzymZvJdkJEMmXiJU9GnFbMBMICR3a4xFKyBrzxkGUh3Kl2aO6WoGItBSgRC3XP6iCfrE7pPcD6NcwSoQlRPb39ESLKIBkD52onLBp04n1DUNSXuCFDF27unArVGTLsNVrD23kKOEE8sY1CG%2FArXg6A0ec0oliXVzQtc1mCj978ld1wdaFb4Kmnuoj0m4Yw1XG20OZRSSzTwUSLK%2B3Pun6Uc%2BOTlfAIrMvgAorRpuXdPZLnR7oMRm6481jZ9D%2FEIpAUIIJrVqz3QsIUKPjTtfkh3qNfkQWqy95cDFOdqyUI1LPKMi2QrUzG4AWmfE0QelnZaBTA8OQY%2BfMDTsV5CmSRvapCgBfkOz6snh6eikvGvAtFM3adGTEHPnX%2BfxNwTl0odp%2Bvubpa%2Fxbstiu8h5QbZbg%2BMNDziaUGOrEBBXx73LDXuYWo5O23orU%2BUC2FaJbXpoKb4Ms1S6g5H88xgCFLqgmxtw4HRvHuKReam%2FryvI%2FyrNgsuezjswc%2BAtkeT3Bw0aGSiUbgztuB6h2wnuk8egJG%2BQ9aG8kAOzuo%2BvS8tiDQsSce%2B%2F9Jh06eS7kjwCqnhx5e6P39jWjrQOBGn%2BhK3kXE4KL3nVt6arZHjsUqrwkOUiklwQcxMMWhcyxErNIb5JjSz9ahmkuCSX4F&X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Date=20230703T081926Z&X-Amz-SignedHeaders=host&X-Amz-Expires=299&X-Amz-Credential=ASIAQ3PHCVTY2IONEZ46%2F20230703%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Signature=9f7b15999f2836539376ec585a34f62bbf66573b84e8d9873709405bbc8401b4&hash=37618c346934e70483f5dbb1d8c306b5a2cd17cbbc98b6e19d7d712aee8dfee6&host=68042c943591013ac2b2430a89b270f6af2c76d8dfd086a07176afe7c76c2c61&pii=S0022489822000714&tid=spdf-13513de0-f29f-4643-a99e-0a8842ca8be0&sid=f555142d355c7841a438864088602d45b919gxrqa&type=client&tsoh=d3d3LnNjaWVuY2VkaXJlY3QuY29t&ua=0f16520a540603515003&rr=7e0db41a9d982089&cc=jp).