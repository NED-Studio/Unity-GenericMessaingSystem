# Generic Event Syste 
------
**Generic Event System** adalah Event System yang menggunakan **generic class** untuk penyimpanannya, 
yang pada umumnya memanfaatkan collecntio seperti list atau array yang selanjutnya akan di-loop.

## How to use
------
1. Download *.unitypackage release from [Release Page](../../releases)
2. Import to your Unity project
3. Create New Class which extending BaseMessagingManager class
4. Overite abstract method **BaseMessagingManager.CreateAllStorage()** and **BaseMessagingManager.DestroyAllStorage()** using method :
```
	BaseMessagingManager.CreateStorage<D, I>() where D : IMessageDomain where I : IMessageListener
	
	BaseMessagingManager.DestroyStorage<D, I>() where D : IMessageDomain where I : IMessageListener
```
5. Create Interface which extending IMessageListener
6. Create Interface which extending IMessageDomain or use GlobalDomain
7. Create new class which extend IMessageListener and Add or Remove its instrance using :

```
	BaseMessagingManager.Add<D, I>(I handler) where D : IMessageDomain where I : IMessageListener
	
	BaseMessagingManager.Remove<D, I>(I handler) where D : IMessageDomain where I : IMessageListener
```

Please look at Sample for more detail 

## Contribution
------
Please read [CONTRIBUTION.md](./CONTRIBUTION.md) file for deatail about contribution.

## Licenses
------
Please read [LICENSE](./LICENSE) file for deatail about lincese.

