# My media server setup
Running on MacBook Pro M2 Pro

## How to run?
1. Create .env file according to example.env

2. Create ssl certificates for each of domain used
   example:
   ```sh
   cd ssl/
   mkcert <your-domain> localhost 127.0.0.1 ::1
   ```

3. Add domains to /etc/hosts file
   example:
   ```sh
   sudo vim /etc/hosts
   ```

   And add each domain, below other entries, according to this example
   ```
   127.0.0.1 <your-domain>
   ```

4. Boot docker containers
   ```sh
   docker compose up -d
   ```