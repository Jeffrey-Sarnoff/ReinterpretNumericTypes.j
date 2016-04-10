## ReinterpretNumericTypes.jl
extends reinterpret to work with targets that are abstract numeric types 

####Use
```julia

using ReinterpretNumericTypes

anInt     = Int32(1)                                      # 1

aFloatType = reinterpret(AbstractFloat, typeof(anInt))    # Float32
anIntType  = reinterpret(Signed  , aFloatType)            # Int32
aUIntType  = reinterpret(Unsigned, aFloatType)            # UInt32
aUIntType  = reinterpret(Unsigned, anIntType)             # UInt32

aFloat = reinterpret(AbstractFloat, anInt)                # 1.0f-45
aUInt  = reinterpret(Unsigned, aFloat)                    # 0x00000001
anInt  = reinterpret(Signed, aFloat)                      # 1

```
