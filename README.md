# Floating-Static-Routes

Understanding Floating Static Routes: The Network Safety Net

Overview

In network engineering, redundancy is everything. A Floating Static Route is a backup static route with a higher Administrative Distance (AD) than the primary route. It "floats" above the routing table and only appears when the primary path fails.

1. The Core Concept: Administrative Distance
To understand how these work, you have to understand how a router chooses between two different paths to the same destination. It uses Administrative Distance (AD)—the "trustworthiness" of a route.

Standard Static Route: AD of 1 (Very trustworthy).

EIGRP: AD of 90.

OSPF: AD of 110.

If you create a static route but manually set the AD to something higher (like 210), the router will ignore it as long as the primary route (AD 1 or a dynamic protocol) is active. If the primary link goes down, the primary route is removed from the routing table, and the "floating" route—now the best remaining option—is installed.

2. Why Use Them?
Redundancy: Provides a backup path if a primary ISP or leased line fails.

Low Overhead: Unlike dynamic protocols, static routes don't consume bandwidth with "Hello" packets or updates.

Predictability: You know exactly which path traffic will take during a failure.

LAB
<img width="1491" height="1102" alt="image" src="https://github.com/user-attachments/assets/7f07bc3a-3639-4336-a9a9-f5bb8134e73d" />

step-1

it is using OSPF routing protocol

<img width="900" height="818" alt="image" src="https://github.com/user-attachments/assets/602de71c-4650-4889-aef0-093a739d77e3" />

<img width="793" height="304" alt="image" src="https://github.com/user-attachments/assets/b48e667b-2544-4b1d-ab8c-e33a99046623" />

step-2

<img width="899" height="61" alt="image" src="https://github.com/user-attachments/assets/b42e56ad-b91c-4d9d-acc1-4cb1bf324085" />

<img width="957" height="76" alt="image" src="https://github.com/user-attachments/assets/eb4f799a-317d-4d4b-9c6f-c57267f4fcc4" />

<img width="1241" height="672" alt="image" src="https://github.com/user-attachments/assets/6f669362-3e99-48df-b68e-cfaafb30ecef" />

<img width="1016" height="213" alt="image" src="https://github.com/user-attachments/assets/d320e7b6-2ca1-47ee-84a5-26b9cdc11657" />

<img width="1005" height="177" alt="image" src="https://github.com/user-attachments/assets/61f857c4-8817-4812-8c4d-db5e49a2bf61" />

<img width="1057" height="91" alt="image" src="https://github.com/user-attachments/assets/b733a03e-e758-4114-85df-d5c00815a952" />

<img width="985" height="195" alt="image" src="https://github.com/user-attachments/assets/9033731c-aed7-4090-b713-d9af2ec4b546" />

step-3
<img width="830" height="342" alt="image" src="https://github.com/user-attachments/assets/5023ac7b-fa44-4a1a-839e-323436738cec" />
here we can say that we made sure with that  network is down we have the backup floating static route is enable so that you can sure around the internet without problem
