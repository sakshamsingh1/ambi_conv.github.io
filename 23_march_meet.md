## Train full model
- architec : unet
- sampling rate : 44.1kHz //Is it fine to quote results in a rate different from original rate?
- data duration : ~1 sec
- data : train 49152 ; val 7168
- lr = 3e-4 //Should I train more with lesser lr?
- patience : 20 
- #epochs : 175
- time : ~10min/epoch
- Loss : 
 <img width="423" alt="Screenshot 2022-03-23 at 12 53 49 PM" src="https://user-images.githubusercontent.com/31805612/159753893-a0e61df9-c6f5-457d-a435-8aee54c0bf8b.png">
- ex.
<img width="350" alt="Screenshot 2022-03-23 at 12 54 54 PM" src="https://user-images.githubusercontent.com/31805612/159753949-3ffa4098-a781-4671-a766-dfb277694d52.png">
<img width="338" alt="Screenshot 2022-03-23 at 12 56 06 PM" src="https://user-images.githubusercontent.com/31805612/159754058-6cd4e7cd-5608-4c8e-882a-2778fb14be34.png">


## Appendix:
Verification 
<img width="417" alt="Screenshot 2022-03-23 at 1 21 08 PM" src="https://user-images.githubusercontent.com/31805612/159760907-6a82a3b4-644a-45d7-b8cc-8e25641c8a44.png">

<img width="507" alt="Screenshot 2022-03-23 at 1 20 38 PM" src="https://user-images.githubusercontent.com/31805612/159760918-91adff1f-5795-4fdb-80c7-a91dc92c45f8.png">

<img width="513" alt="Screenshot 2022-03-23 at 1 20 45 PM" src="https://user-images.githubusercontent.com/31805612/159760931-20e06d67-4558-4f5a-8624-2f5c87bf7b1e.png">

### Next steps

* Reduce lr to make learning continue from where the best model is
* Train with more data
* Train with a more complex loss, to improve phase error
* Include another baseline in the Table of results
* Use the model for a downstream task (SEDL)
* Dynamic filter convolutions
