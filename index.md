## A-B format conversion

- #### Experiment 1 
  Dataset : DCASE task 3 2021\
  Train set : 400\
  val set : 100\
  exp size : 4 x 1000 (trimmed)\
  actual size : 4 x 1440000\
  architecture : 1 CNN - 4 Linear, L1 loss\
  criterion = nn.L1Loss()\
optimizer = optim.SGD(net.parameters(), lr=0.001, momentum=0.9)\
  EDA : 
  <img width="456" alt="eda" src="https://user-images.githubusercontent.com/31805612/151916423-861cfa43-44f9-4d9e-8aa3-56139489a656.png">

  result: 
  

<img width="445" alt="exp1_result" src="https://user-images.githubusercontent.com/31805612/151916442-79449c99-3e47-467f-bab2-52189a48d0d7.png">

- #### Experiment 2
  Everything same except
  exp size : 4 x 24000 (trimmed)\
  Network :
<img width="856" alt="Screenshot 2022-02-03 at 7 12 41 PM" src="https://user-images.githubusercontent.com/31805612/152450663-ec9ed767-c781-4a65-bd89-846c379a7f5b.png">
  Results:
  <img width="458" alt="Screenshot 2022-02-03 at 7 12 32 PM" src="https://user-images.githubusercontent.com/31805612/152450692-d570de24-66a0-4879-a598-2f88413eb1bd.png">

- #### Experiment 3 : exp2 + more epochs + plots

<img width="432" alt="Screenshot 2022-02-04 at 4 16 34 PM" src="https://user-images.githubusercontent.com/31805612/152609221-e0fdbf7c-a3e6-4cfc-8491-0e73c20d2170.png">

<img width="458" alt="Screenshot 2022-02-04 at 4 40 07 PM" src="https://user-images.githubusercontent.com/31805612/152609229-e159ecbb-eb92-464e-8cf5-0a1108c63a51.png">

- #### Experiment 4 : try to overfit on smaller dataset (10 datapoints)
  Exp3 +\
  optim.Adam(net.parameters(), lr=0.01)\
  epochs = 200
<img width="638" alt="Screenshot 2022-02-07 at 7 12 57 PM" src="https://user-images.githubusercontent.com/31805612/152893580-e702ee64-15fa-42f5-a4f1-163f0d67b6ad.png">

file = 'fold3_room2_mix010.wav'
<img width="449" alt="Screenshot 2022-02-07 at 7 15 06 PM" src="https://user-images.githubusercontent.com/31805612/152893787-4dc16e8c-d8dc-4f7f-b8d2-4696b19a3607.png">

- #### Experiment 5 : Trying to overfit on small dataset(10 points) + CNNs 
  <img width="838" alt="Screenshot 2022-02-07 at 7 18 31 PM" src="https://user-images.githubusercontent.com/31805612/152894262-ec5a9a51-6257-48c3-a331-c23a51b62d5e.png">
<img width="446" alt="Screenshot 2022-02-07 at 7 18 46 PM" src="https://user-images.githubusercontent.com/31805612/152894266-e2d204f7-f776-43bd-8bcf-050fd81fbd80.png">

<img width="605" alt="Screenshot 2022-02-07 at 7 18 57 PM" src="https://user-images.githubusercontent.com/31805612/152894276-a75ec629-9a8f-444b-8496-8960f8c4925e.png">

<img width="463" alt="Screenshot 2022-02-07 at 7 19 07 PM" src="https://user-images.githubusercontent.com/31805612/152894277-9b1c6017-3d56-4676-83a9-73a3cfec4236.png">

--------------------------------------- Till Now (8th Feb) --------------------------------------------------------------------------------

- #### Experiment 5 : Normalize + (L1->L2 loss) + Kernel size change(3,333)
  Normalization {normalized = arr/max(|arr|)}
  
  Note: max is globally chosen(i.e. across all the channels) and not channel wise

<img width="483" alt="Screenshot 2022-02-10 at 3 04 06 PM" src="https://user-images.githubusercontent.com/31805612/153487787-639c854b-6601-4fe3-b50b-9926399ca507.png">

<img width="447" alt="Screenshot 2022-02-10 at 3 04 12 PM" src="https://user-images.githubusercontent.com/31805612/153487796-c46b7d90-4e39-4f40-bc35-b20153bcc425.png">

<img width="824" alt="Screenshot 2022-02-10 at 4 26 21 PM" src="https://user-images.githubusercontent.com/31805612/153499428-687ab26f-d5ee-41a8-a1b3-88cbeff194ea.png">

<img width="461" alt="Screenshot 2022-02-10 at 4 26 29 PM" src="https://user-images.githubusercontent.com/31805612/153499442-eec91244-bae5-4227-8349-0b5c67400a8b.png">

<img width="480" alt="Screenshot 2022-02-10 at 4 26 55 PM" src="https://user-images.githubusercontent.com/31805612/153499453-a2189903-fdc1-4f4c-8b2a-305e48f95697.png">



Comaprisons:
- L1 vs L2 Loss
- Kernel sizes

