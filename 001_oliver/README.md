Oliver's contribution
============================

**Date:** 23 May 2023

**Name:** Oliver

**Location:** N/A

**Device(s):** Personal Apple MacBook Pro Apple M1 Chip

**Steps taken:**
1. Downloaded the [`new challenge`](https://pse-trusted-setup-ppot.s3.eu-central-1.amazonaws.com/challenge_0075) file from [`perpetualpowersoftau`](https://github.com/privacy-scaling-explorations/perpetualpowersoftau) 
2. Used the [`zkbnb-setup`](
   https://github.com/bnb-chain/zkbnb-setup/releases/tag/v1.0.0-ceremony) tool to transform the challenge file above into gnark circuits format using this command:    
`zkbnb-setup p1t challenge_0075 challenge_0075_26 28 26`
3. Cloned the [`zkbnb-crypto`](https://github.com/bnb-chain/zkbnb-crypto) repository based on commit `e4ad33260f18e09d68a19ff6a1827d6996d1856a`
4. Ran command `go test -run TestExportSol -timeout 600m -create_pkvk=false`
5. Used the [`zkbnb-setup`](
   https://github.com/bnb-chain/zkbnb-setup/releases/tag/v1.0.0-ceremony) tool to create phase 2 initial files for each circuit using this command:    
``` 
zkbnb-setup p2np challenge_26.ph1 zkbnb8 start_8.ph2 2509735 1738492 100000
zkbnb-setup p2np challenge_26.ph1 zkbnb16 start_16.ph2 4263876 3374751 100000
zkbnb-setup p2np challenge_26.ph1 zkbnb32 start_32.ph2 7746400 6664384 100000
zkbnb-setup p2np challenge_26.ph1 zkbnb64 start_64.ph2 14636612 13211981 100000
```
phase 2 initial files: [`block size 8`](https://d3i6h4yib3miee.cloudfront.net/zkbnb-mpc/initial/start_8.ph2), [`block size 16`](https://d3i6h4yib3miee.cloudfront.net/zkbnb-mpc/initial/start_16.ph2), [`block size 32`](https://d3i6h4yib3miee.cloudfront.net/zkbnb-mpc/initial/start_32.ph2), [`block size 64`](https://d3i6h4yib3miee.cloudfront.net/zkbnb-mpc/initial/start_64.ph2)
7. Made contributions to each of the initial files using the [`zkbnb-setup`](
   https://github.com/bnb-chain/zkbnb-setup/releases/tag/v1.0.0-ceremony) tool with the following commands:    
```
zkbnb-setup p2c start_8.ph2 output_8.ph2
zkbnb-setup p2c start_16.ph2 output_16.ph2
zkbnb-setup p2c start_32.ph2 output_32.ph2
zkbnb-setup p2c start_64.ph2 output_64.ph2
```

**Hash:**   
Hashes of the [`new challenge`]() files for verification:
```
output_16.ph2 := e287693e2f87ec198ada0d6629d82424183e023b81aeab3b6900a7b8bbd34344
output_32.ph2 := b9b0643bae7463a7e7d2b459f1299bd9e43ad135195acc07bae60cc670ffd544
output_64.ph2 := 3a09e751bc95f8c040faa1022a285a3aae25b8da197b012ace5dd509d18bb4fc
output_8.ph2 := e651c16ae00fe2526f7caf66065c62a70b3e13756ee661d7370bd4402158d161
```

**New challenge files:**   
[`link for block size 8`](https://d3i6h4yib3miee.cloudfront.net/zkbnb-mpc/oliver_1/output_8.ph2)    
[`link for block size 16`](https://d3i6h4yib3miee.cloudfront.net/zkbnb-mpc/oliver_1/output_16.ph2)    
[`link for block size 32`](https://d3i6h4yib3miee.cloudfront.net/zkbnb-mpc/oliver_1/output_32.ph2)    
[`link for block size 64`](https://d3i6h4yib3miee.cloudfront.net/zkbnb-mpc/oliver_1/output_64.ph2)







