# VM Lifecycle on GCP and OCI — Tutorial

## Video
Loom for GCP
  <https://www.loom.com/share/08146a2e7cfe472d825d7a90ce2e19a0>

Loom for OCI
  <https://www.loom.com/share/56d2d247fd4440449c22d80159333c67>

Loom for Similarities/Differences and Preference 
  <https://www.loom.com/share/4bf0e0d6417e4ebeac7ecf633df389af>

## Prereqs
- Cloud access to GCP and OCI
- No PHI/PII; smallest/free-tier shapes

---

## Google Cloud (GCP)
### Create
1. Go to Compute Engine → Create instance (or create VM)
2. Name instance
3. Select region and zone of your choice
4. Choose machine type: smallest - E2 micro for cost
5. Choose operating system: Ubuntu LTS 
6. Boot disk: default minimal
7. Keep network as default VPC and choose ephemeral public IP

Below is a screenshot of instance being created
<img width="700" height="700" alt="GCPcreateVM" src="https://github.com/user-attachments/assets/5649cce2-1ed9-4fa2-82e7-8d04666483b1" />


### Start/Stop
- Start: Instance should now be running
- Stop:  Stop instance to ensure 

<img width="700" height="700" alt="Screenshot 2025-12-08 115945" src="https://github.com/user-attachments/assets/5359ee4d-122e-444a-b7b2-2847994e23f0" />
<img width="700" height="700" alt="Screenshot 2025-12-08 120245" src="https://github.com/user-attachments/assets/dc749da0-bd1c-4242-a99e-c56120f2e84a" />


### Delete
- Delete instance and verify no disks/IPs remain

<img width="500" height="500" alt="Screenshot 2025-12-08 120450" src="https://github.com/user-attachments/assets/3756b88d-7aa6-476d-9018-da59eddf77f0" />


---

## Oracle Cloud (OCI)
### Create
1. Compartment: AD 1 
2. Networking: VCN with Internet Connectivity (defaults)
3. Shape: E2 micro
4. Image: Ubuntu
5. Public IP: ephemeral
6. Boot volume: default minimal

<img width="700" height="450" alt="Screenshot 2025-12-08 195731" src="https://github.com/user-attachments/assets/95178086-fd71-400c-8ff9-e89d59733967" />


### Start/Stop
- Instance should be running
- Click stop to stop instance from continuing to run

<img width="700" height="600" alt="Screenshot 2025-12-08 190559" src="https://github.com/user-attachments/assets/4cb6dee3-dd01-406b-97ae-9694a9c13763" />


### Terminate
- Click on Actions to Terminate the Instance and delete boot volume
- Verify cleanup 

<img width="700" height="270" alt="image" src="https://github.com/user-attachments/assets/89f6b275-9902-4b97-899f-05d5aadb8fa0" />


---

## Reflections
### Similarities
- Same VM lifecycle: Create -> Running -> Stop -> Terminate
- Name instance
- Pick a region/domain
- Choose OS image
- Choose machine type/shape

### Differences
- OCI's settings are broken into sections, will GCP is on one page
- GCP is simpler to use, OCP is more detailed
- GCP is faster than OCI depending on shape
- Terminology is different: Machine types vs shapes, Projects vs compartments

### Preference (OCI vs GCP) and Why
- I prefer using Google Cloud Platform because the interface is more intuitive and easier to navigate, with all the key VM settings presented on a single straightforward page. Provisioning and deleting instances also feels faster and more seamless compared to OCI. In addition, GCP’s terminology such as project, zone, and machine type is clearer for beginners, while OCI’s compartment and shape structure can feel more complex at first.
