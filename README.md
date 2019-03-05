YesPoWer miner for Yenten
cli version

Brief instructions for miner

Miner is configured under 4 basic processor instructions
AVX
AVX2
SSE4
SSE2

Miner automatically switches to the new algorithm at the time of the hardfork.
You can now start to mine using the new miner.
No intervention is required in the work of the miner during the algorithm change.

A list of supported arguments is available when you run the miner with the --help switch.

The miner is started by the command:

miner-sse4.exe --password <PASSWORD> --threads <THREADS> - url <URL> --username <USER>
  
for example (the pool administrator account yenten.luckypool.org):

miner-sse4.exe -o stratum://yenten.luckypool.org:3344 -u admin.u -p x -t 10

or you can run miner with config file
miner-sse4.exe -c conf.jsom

conf.json example:

{"host": "yenten.luckypool.org", "port": 3344, "username": "admin.u", "password": "x"}

or

{"host": "yenten.luckypool.org", "port": 9996, "username": "admin.u", "password": "x", "threads": 10} - with number of threads

If you do not specify the number of cores, the miner himself determines what number of physical cores you have and starts to mine them
After hardfork on logical cores it is not recommended to mine.
A total hash value when booting on physical cores is higher than when starting on physical + logical cores.

You can download miner(Windows, Linux, MacOS versions) on release page

https://github.com/cranepay/cli-miner-for-yenten/releases/tag/1.0
