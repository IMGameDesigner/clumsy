# clumsy

__clumsy makes your network condition on Windows significantly worse, but in a managed and interactive manner.__

Leveraging the awesome [WinDivert](http://reqrypt.org/windivert.html), clumsy stops living network packets and capture them, lag/drop/tamper/.. the packets on demand, then send them away. Whether you want to track down weird bugs related to broken network, or evaluate your application on poor connections, clumsy will come in handy:

* No installation.
* No need for proxy setup or code change in your application.
* System wide network capturing means it works on any application.
* Works even if you're offline (ie, connecting from localhost to localhost).
* Your application keeps running, while clumsy can start and stop anytime.
* Interactive control how bad the network can be, with enough visual feedback to tell you what's going on.

See [this page](http://jagt.github.io/clumsy) for more info and build instructions.

## License

MIT


捕获数据包后，可以选择启用提供的功能以恶化透视网络状况：

1 滞后，将数据包保留一小段时间以模拟网络滞后。
2 丢弃，随机丢弃数据包。
3 节流阀，在给定的时间段内阻塞流量，然后分批发送。
4 复制，然后将克隆的数据包立即发送到原始数据包。
5 乱序，重新排列数据包的顺序。
6 篡改，微调数据包内容的位。
