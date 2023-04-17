## How to use
1. Install Node.js and Docker.

2. Clone the repository to your local machine.
```
git clone https://github.com/Hatrison/mtsd_lab3.git
```

3. Navigate to the project directory in your terminal.

4. Execute: 

```
docker build . -t js:1.0
````

5. Run command

```
docker run -p 8080:8080 --ti js:1.0
```
