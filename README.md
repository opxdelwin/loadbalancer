# Traefik Load Balancer

This project sets up a Traefik load balancer to distribute traffic between two backend servers using a round-robin algorithm. The load balancer is accessible via the hostname `loadbalancer.plansync.in`.

## Project Structure

- `traefik.yml`: Main configuration file for Traefik.
- `dynamic.yml`: Dynamic configuration file specifying backend servers and header management.
- `README.md`: Documentation for the project.

## Setup Instructions

1. **Install Traefik**: Follow the official Traefik installation guide to set up Traefik on your server.

2. **Configuration Files**:
   - Place the `traefik.yml` and `dynamic.yml` files in the appropriate directory as per your Traefik setup.

3. **Start Traefik**: Run Traefik using the command that points to your `traefik.yml` configuration file.

## Configuration Details

### traefik.yml

This file defines the entry points and the load balancer settings. It specifies the host for the load balancer and the routing algorithm.

### dynamic.yml

This file contains the backend server definitions:
- `s1.server.plansync.in`
- `s2.server.plansync.in`

It ensures that all headers are passed as is to the backend servers.

## Usage Examples

Once the load balancer is running, you can access it via `http://loadbalancer.plansync.in`. Traefik will distribute incoming requests to the backend servers using the round-robin method.

## Additional Information

For more details on Traefik configuration and advanced features, refer to the [Traefik documentation](https://doc.traefik.io/traefik/).