TF-IDF kya hai?

Machine learning models sirf numbers samajhte hain, text nahi. Toh humein text ko numbers mein convert karna padta hai. TF-IDF ek tarika hai isko karne ka.

TF-IDF = Term Frequency × Inverse Document Frequency

. TF (Term Frequency) — "Ye word is document mein kitni baar aaya?"
Agar ek review mein "React" word 5 baar aaya hai, to uski TF high hai us review ke liye.

Simple example se samjho

Maano humare paas 3 reviews hain:

"great culture great team"
"bad management bad culture"
"great salary good benefits"

TF (Term Frequency) — har review mein kaunsa word kitni baar aaya

Review 1 mein "great" 2 baar aaya → uska TF zyada hoga
Yeh idea hai: jo word kisi review mein baar-baar aata hai, woh us review ke liye important hai

IDF (Inverse Document Frequency) — koi word kitne reviews mein common hai
IDF (Inverse Document Frequency) — "Ye word kitna RARE/SPECIAL hai poore dataset mein?"

Yahan ulta logic hai:

Agar koi word har document mein hai (jaise "the", "is", "course") → IDF kam (ye word useless hai, kyunki har jagah hai, kuch distinguish nahi karta)
Agar koi word sirf kuch documents mein hai (jaise "Flexbox", "TensorFlow") → IDF high (ye word bahut specific/meaningful hai)

Agar "culture" word saare reviews mein baar-baar aa raha hai, to woh itna useful nahi hai differentiate karne ke liye
Lekin agar "salary" sirf ek hi review mein aaya hai, to woh word us review ko unique banata hai — usko zyada importance milegi

TF-IDF dono ko combine karta hai: jo word ek particular review mein zyada baar aaya ho, LEKIN baaki reviews mein kam common ho — usko sabse zyada score milta hai.
