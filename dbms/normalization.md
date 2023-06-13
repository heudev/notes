# Second Normal Form

### Proper Subset

Örnek: 
* **ADE** candidate key olsun
* Bu durumda 6 tane proper subset vardır. **(AD, DE, AE, A, D, E)**

### Prime Atributes

Candidate key'in bir parçasıdır. \
Örnek: 
* **R(A, B, C, D, E, F)** ilişkisi var.
* Varsayalım **ADE** ve **BC** candidate key olsun.
* Bu durumda **A, B, C, D, E** prime attrubutes olur.
* **F** non-prime atrubute olur.

### Partial Dependency 
**Proper subset of any candidate key** -> (must determine) **non-prime atribute** 

Not: Normalizasyon işleminde **candidate key** olmadan hiçbir şey yapalımaz. \
Not: Candidate key super key'in minimal halidir.

Örnek:
* **R(A, B, C, D, E, F)** ikişikisi var.
* FD = **{A→B, B→C, C→D, D→E}**
* İlk önce Super Key bulunur. Tüm attribute'lar closer şeklinde yazılır.
* **ABCDEF⁺ = {ABCDEF}** (Super Key)
* **BCDE** attribute'larına **A**'dan ulaşılabilir. Bu yüzden silinir.
* Candidate Key'in bulunabilmesi için en minimal hâle getiririlir.
* **AF⁺ = {ABCDEF}** (Super Key)
* Proper Subset'lere bakılır.
* **A⁺ = {ABCDE}** (Super Key değil)
* **F⁺ = {F}** (Super Key değil)

Not: Eğer proper subset ayrıca super key ise candidate key olmaz.


* Bu durumda **AF** Candidate key olur.
* Ayrıca **A** ve **F** prime atributes olur.
* Non-prime atributes **B, C, D, E** olur.

Not: Eğer prime attribute'lar, hehangi bir FD'nin sağ tarafında mevcutsa, o ilişkide daha fazla candidate key vardır. Eğer yoksa, sadece bir tane Candidate Key vardır. 

* Bu ilişikide sadece 1 tane Candidate Key vardır.

2NF olabilmesi için, 1NF olmalıdır ve İlişkide Partial Dependency olmamalıdır. 

* **A** ve **F** candidate key'in proper subset'leri olur.
* **A → B** (Proper Subset, non-prime attribute'u belirliyor)
* **F → x** (Proper Subset, herhangi bir attribute'u belirlemiyor)
* Bu ilişkinin 2NF olabilmesi için Candaite key'in proper subset'leri **(A ve F)**, non-prime attribute'ları belirlememesi gerekir. 
* Eğer belirliyorsa partial dependency olur.
* Ancak, 2NF'de partial dependenct olmamalıdır.
* Bu yüzden, bu ilişki 2NF değildir.
