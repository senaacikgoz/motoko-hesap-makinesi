Motoko Playground İle Hesap Makinesi Projesi

Bu proje, Motoko Playground ile yazılmış bir hesap makinesi projesidir. Projeye şu adresten ulaşabilirsiniz:

Projenin Linki:   [(https://m7sm4-2iaaa-aaaab-qabra-cai.raw.ic0.app/?tag=2003710119)]
Bu proje ile basit matematiksel işlemleri yapabilirsiniz.


Ayrıca projenin kodlarına da aşağıda ulaşabilirsiniz.


```motoko
// hesap makinesi
// değişkenler (let -> immutable, var -> mutable)
// operatörler
// async metodu
// if condition

// canister => akıllı sözleşme

actor hesap_makinesi {
    var hucre: Int = 0;
    
    // toplama
    public func toplama(s: Int) : async Int {
        hucre += s;
        hucre
    };
    
    // çıkarma
    public func cikarma(s: Int) : async Int {
        hucre -= s;
        hucre
    };
    
    // çarpma
    public func carpma(s: Int) : async Int {
        hucre *= s;
        hucre
    };
    
    // bölme
    public func bolme(s: Int) : async ?Int {
        if (s == 0) {
            null
        } else {
            hucre /= s;
            ?hucre
        }
    };
    
    // temizle
    public func temizle() : async () {
        hucre := 0;
    };
};
