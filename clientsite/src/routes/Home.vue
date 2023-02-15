<template>
    <main>
        <header>
            <div class="top-header">
                <div class="logo">
                    KEA-COMMERCE
                </div>
                <div class="info-links">
                    <div class="info-links-wrapper">
                        <div class="content flex-row">
                            <div class="left-content"><i class="fa-solid fa-phone"></i></div>
                            <div class="right-content">
                                <a href="/">+237682449347</a>

                            </div>
                        </div>
                        <div class="content flex-column">
                            <div class="content-flex"><i class="fa-solid fa-envelope"></i><a
                                    href="/">codingherald@gmail.com</a></div>
                            <div class="content-flex"><i class="fa-brands fa-whatsapp"></i><a href="/">codingherald</a>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            <div class="bottom-header">
                <div class="left-bottom-header">My account<i class="fa-solid fa-caret-down"></i></div>
                <div class="bottom-header-routes">
                    <div class="routes-wrapper">
                        <router-link to="/">Home</router-link>
                        <router-link to="/">shop</router-link>
                        <router-link to="/">pages</router-link>
                        <router-link to="/">cart</router-link>
                        <router-link to="/">about</router-link>
                    </div>
                </div>
                <div class="right-bottom-header">
                    <div class="content-wrapper">
                        <div class="search-box-wrapper">
                            <input type="search" name="search" id="search" placeholder="search item">
                            <button><i class="fa-solid fa-magnifying-glass"></i></button>
                        </div>
                    </div>
                </div>
                <div class="cart">
                    <div class="cart-wrapper">
                        <button>
                            <i class="fa-solid fa-cart-shopping"></i> 10 items ~ $210
                        </button>

                    </div>
                </div>
            </div>
        </header>
        <div class="landing-page">
            <div class="main-wrapper">
                <div class="main-wrapper-content">
                    <h3>kea-commerce at your sercice daily daily</h3>
                    <h1>Get new arrivals from all around the world at one click. </h1>
                    <router-link to="/">start shopping</router-link>
                </div>
                <div class="carousel-wrapper">
                    <carousel :images="images" />
                </div>
            </div>
        </div>
        <div class="main-section-1">
            <div class="main-section-1-wrapper">
                <div class="main-section-1-wrapper-left-content">
                    <div class="hot-deals">
                        <div class="hot-deals-wrapper">
                            <div class="hot-deals-header">
                                <nav>
                                    <div class="nav-left-content">
                                        <h1>hot deals this week</h1>
                                    </div>
                                    <div class="nav-right-content">
                                        <button>25</button>
                                        <p>view all</p>
                                    </div>

                                </nav>
                            </div>
                            <div class="hot-deals-body">
                                <div class="hot-deals-body-wrapper">
                                    <div class="hot-deals-body-wrapper-content">
                                        <div class="img">
                                            <img src="data:image/jpeg;base64,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"
                                                alt="">
                                        </div>
                                    </div>
                                    <div class="hot-deals-body-wrapper-content">
                                        <div class="img"><img
                                                src="data:image/jpeg;base64,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"
                                                alt=""></div>
                                    </div>
                                    <div class="hot-deals-body-wrapper-content">
                                        <div class="img"><img
                                                src="data:image/jpeg;base64,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"
                                                alt=""></div>
                                    </div>
                                    <div class="hot-deals-body-wrapper-content">
                                        <div class="img"><img
                                                src="data:image/jpeg;base64,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"
                                                alt=""></div>
                                    </div>
                                    <div class="hot-deals-body-wrapper-content">
                                        <div class="img"><img
                                                src="data:image/jpeg;base64,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"
                                                alt=""></div>
                                    </div>
                                    <div class="hot-deals-body-wrapper-content">
                                        <div class="img"><img
                                                src="data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wCEAAkGBwgHBgkIBwgKCgkLDRYPDQwMDRsUFRAWIB0iIiAdHx8kKDQsJCYxJx8fLT0tMTU3Ojo6Iys/RD84QzQ5OjcBCgoKDQwNGg8PGjclHyU3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3N//AABEIAHsAwwMBIgACEQEDEQH/xAAcAAAABwEBAAAAAAAAAAAAAAAAAgMEBQYHAQj/xABLEAABAwMCAwUEBQcJBgcBAAABAgMEAAURBiESMUEHEyJRYTJCcYEUI2KRsRUkM1KhwdEWNDVDcqKy0vAlU1SCg+FEc5KTlMLiF//EABoBAAEFAQAAAAAAAAAAAAAAAAABAgMEBQb/xAAqEQACAgIBAgYBBAMAAAAAAAAAAQIDBBESITETFCJBUVJhBTJCkXGB8f/aAAwDAQACEQMRAD8AmLXbJF0e7qP4Uj2nCMhP/f0rR7Vb49tjIjx0YxupXVSupPrScGMzEaDTDYbSOQTT1Jq9lZUr3+CnjYsaF+Q6hwkrHLqKHGAM5GMZzRH5DUZlb0hxLbaE8SlqOAkDqaxfW2vnL6FQ7K6GtPklqbLHElxRPupxuNtxseLrsDVNItll1T2jKZnqh6eLLhhugzXn9kcOeSfMZ2J9RjOauFlu8O/Wxq429fE0vIKTsUKHMEV59VHR3MZMgOpjNKDTCUePvwRlC1Eb436cx7OMGrFpO+TtOXQOcQeQtI+lIQv6hDYOMJI2yOW3Xbc5wy/HhdW4sVPRtortIQZca4wmpkJwOMOp4kkfhjpS1cndTKmbhImT2doUK5UQHaFcrtAAoVw+Q51C2zUsK43SRAZJC2lFLajydxzx8DnbqN6khVOabiuwE3QrmaI8nvGlIyRkcxUYDaXc4cXIefSFfqjc1V9Q6kQtkGIwVKQdlL2/ZTG5xXIklTbmTvsT1qOdTxoKT1GK0MNqm2Ni9iG6PiQcWMJd2myc97IUEn3UbCkYzyVoMZ1SUhSstuK5IV6+h6/I02WCklJ5g4NNnl4rtXqaMeG4S2hlqK+m3yF2q2FSJQOJDzmxyPaSD546/DHSo7Sd1ZgrXDnrEm3S0K7/ACg+JvkFf2k9fTrkCnt2iC5smUhINwiIyrw8RebA2UB1Wjb4p/s7wXASFJWp7gSsd4sKDaGlJAwR5JO3w22zis+cWno1oT5rZqdqH0o/yQvsnjdGJFjnqzlxCRsM53UkZB80k1ns+3fkSS7b5TceN3SsJ41lRZkEZ6+5jBBO2MHxEYqc07IF6iIscuSmHPZV3sGQHQVxpGSeD4HHLfbI6CrJPaVrOyPyFMKY1JaklmfDawFOYHhUnPXmpB6bgc6QcZq9NsUd5bN0hzHZqFEPrad7tKl9Tw8Q/AZ50KfJudygJERFrfmpa8IkEKPeDz2SfxJ8980KTQHo9Cts0S4XGJa4Ls24SEMRmk8S3FHGBUdfL1BsNteuNxeDTDYyepWfJI6msQ1fqKXqqVxXYd1aFr/2c0yVfWKxlJX6EHc4yOnWnMRC2t9bTNauFttxy36aQ5wZI8UhQ33+7OOQ5nPKoplpUcx2nmgw4oORxHRhxlGMELc358ifgFbDIoqSttQ9lqQtvgLiCkxoykK2yNwlWw88KUCM8VH4kMpW8pSo0VTqfpLwTxtzUkHYJ6J5nHLCj7wCaNgOWXVt99ISvuXShCn5qE940+CeSUgfsGM4UPAKnbDapN3mtxILBS1xlaQ04VtqQtOy3d/Z2GP1hsMEE0npTTM6+zENoabZbY7xt0oXxsMpIyOME5Uo5BweeyjgjBfap1pFtUV6xaLdShsf0heNsuHGDwEc1evIchS8tAWe5agt2grSu12+Qmfd1HLxUcNtKwBkjkkAckD59TXdKdoke5tBFxSlDgxl1r2fQlPl8M1gNwnmSe7QSWxueJR4lZ5lRPM70eyXV2A+nhUQAfDn9oPpVe7HrvWpocm0etWH2pDSXWHEuNq9lSTkH50es67OWZ07ubpHddj29wZUlQx3x8gOWPtfdWi1zeXRGizipbJE9kZJvsKJJ7iWpbKuhUnY/OnkabFlDMaQ07/YUDTDUVoRdIakjAeSMoVWfMQZX0xUcoKFoPjURy9abVV4vSPcG9Fq7TtTDTGln32lgTJH1MYE+8eavkMn7q83C/3BC4xYkraMZQW0pOxChyNarrS0xNWW5TNuuCn7ha8+FbhUPEASMeR4diNsisXUkoJCgQQcEHmK6HDx/Ar17sjctnp7s211G1fbAl5SGrswn85YG3F9tPofLoflVzrx1ZLtMstyYuFueUzJZVlKhyPmCOoPUV6f0HrCHrC0CSxwtTGsJlRs5LavMeaTvg1l/qGFwbsr7D4yJO+21M6MSkYcTuDVDeQptakLGFA4NafVX1RaSpBlsJ3HtAdaoVT10YrRnlyR3cgnorf+NRrozU5c28s8fVP4VDqT0rs8C3xKF+OhkXx4zYyStbD6HWllDjZ4kqHNJHI0zvMBlaUXCJHY7lZ7pxhbigltxRyU+iVblJ2wQRucU/dRXIr5iuKygracSUPIBwVIPPB6EHBB6EA1PZDkhabOD/BBR3CFJcYW44Wh32Y8cJ71CThKckbKSeW22NgTWhwp0yU0zqW1oUu+2xsInM8HD+UI+BnYclDy5gjHlVKuEMxpCQtbj0ZZS5HdL/AjgHJ0gYweLwrG2DyJJFL2O5O2We1OYVGbdaV9ckFRCXF9NtuAgfAdOIgZq6NFdVs05jS+mNSMpvUF6Q2xO+uCWJq20gn2vCFDB4s59c0KgX9F6Vvb7lzReH7f9JUVripdCA2v3hwnl4sn51ym6ApN8vsy+3lD91dBlniTDjNkqYDahkcaeg9eZzvgCmaFlCnH2ZBZU62hT1xbPG0lYJHAhI5HbbG/MDwnNSOq9MPaWuaXGZKmLZIc4jOJ4nFHn3Z25/iNz5VHhshxtKo6WlOcbSIjQ42Ek7hSxn4H1ACtgMUgCmUMd2pbaosZThT3DILiJfEPCogHYciMDkfBuk4tOjdJP3gruMxbcKGy0W5Mxp1JaaShQPAgcuIAbqHhScEZVml9I6YZVCc1HqOWiHbS2hT0tLhb+kEHkgYGEk4HEPaPs4B3gtd66XqEJgwmzB0/HIDMNsBCn8cisDkn7PLqaAJDWuuGJcRdk0tmBYGyrvpLY4VzFE5OOvCTuTzV8KzeVMLuG2x3bKD4UDbh/iaRkyFPL8RCQnZKQMcPoKRSlSylCAVE4CUgZOenzoA6TsD0x9x9a1Xsx7MF3JTV51KyUwtlMRFbF/yUsdE9cdfhzQ0PpOPapDFy1FGTJkAhbcJR2a9XPt/Z5DrvsNutt1iXFPFHdHGBu2rZSflVb9Q8xRTzjF6fuR13VTnx31HjaEttpQhAQhIwlKRgAUahmmrj5cUUMkgDZTg6eg9fwrm66rL56j1ZabSDvvYJQhQBHtKPJArIO0fW7cgvWbTn1jiAFSHtwX0YPEG1Dnt1HTlyq09qMW8qsSFWh1Cbeji/KTPAVLdaxvjG5HPI59c4zWLQ4/cBqRlKYg+st8mQcKZXnISofInPIe1yyK6LGxIY8encicuQ4tE1ywSG346220oHA2t53JKiQVNOAbAD+7z64p9rSxR7xEd1HYknZRE6NjBQpPM4P7fPnTF9sNofcS3/ADcYmtttbrdOcKRnkATnpjmBhQpay3WTY5yCSt1PAlv693hEgE5KSDyUMnGeXInlVsaUTepjS2oZ+mbwzcra4A4jZaCfC6nqlXoamtZ6eYLf5dsR7y3vEl1Cf6led9ugz06VTeRpGk1pinrrSepIGqbO1crevZXhcaUfE0vG6T/rcb1MLQFoKVDII5GvKOhdWTNJXlM2LlbCvDIj52dRn/EOh/jXqCx3iFfbYxcba6HY7ycg9UnqCOhHUVzudiOl849iSMt9Cm6mtBiOOFI+pcGPhmqWoEEpPMHBrbZ8RuZHW04AQRWS6jtzlsuKm1jwr8ST51pfomR6nWylmQ6KRCuJpo8nAp8rem7yMiujZRQlGW2+wuBKcQ02slTT7ichhZGN/sqHhV6b9Kb93JYfLPdSA62V8MYIDYCR4e7UR1HQ+WMHlXXE4pzhNyi8C2+8mMJBwCeJ9tIOMY5rQM8tynI6VBOHuW6Lf4sKxMlsspbjR/pLSR4XVPDJ+ODjbl8uZ50KZd+0rxLip4juS2yFJPqD5HnQqEuGgRnmFNfki8fXW1/CGXXN1R1+6M9Bn2VdDtSVh0DC0wZ1x1BLQbfHcDwWXCFP43Bc9MnZHUjfOcUV8tBhwvcPdcJ4+IZGOtUXVt4m3GMzl99cGMS20ytfEGz7qj55BIyTtj1rQz8WMHziZeBkyn6JCOu9aStTzg46FMW5n+ZwM4CenEvGxV+HIdapzrynVFSjuedEf4islSuLPU9acWu2y7rNbhwGVOvL5AcgOpJ6AdSayvc1O3cJGYflyG48Zpbrzh4UNoGST5CtU0ppVjT4EqUUP3Uj2huiN6I81eaunTzpzpnT8XTkYhpQenrTh6UByHVDfkn15q+G1S1bOFgfzsX+jHy87for/sHPn1oyHFtrDja1JWOSknBFFoVsOKa0zKT09otOn71JuKn4UhxJU0hKiobLUCSMfDbnVgawEgAbDkKzQ960+1KiL7uUz+jV0I6pV9k9avVhuzd3h98hJQ6hXA80ebawOXw8j1zXOZWDDHm5Vx0n8G7h5Piw4t9UTIwRggEHbBGaxztG0cuxTHbxZ4qZEGW4DMQ4rP0XyUkHYAc8n2eWMVr/AHnQc+vpRlNNPtLZdQFtLSUrSoZBB51UaLyPNralZjrYfMhbG8KY6vCH1qPsYPXmMZz0V4cU1ktx0x1vNhsRmT9eeErU1IVkApz7vhODsNjnJwasOvNHr0bcDJYaL+npSyUjhKvobp2Bxnf0zsobHkKjW3HlPIWhRky2k5QskBuZxnOOhUcfNXD0KaYOOWK6yLZIXHktrfjqAbeQ5gJfB340g81Y3I5kc8EVDat06m3LTcLaQ9a5PiaWjfgz0Pp5GnMuOy2yl1pbZjpOUvuOFZakHcp9RtnOMHHFnpT2yXEMh63XJtT0ReG32+DCUqPNaeuDzP8A6thQBRNxVz7N9cSdH3Lx8btskEfSWAfuWn7Q/aNvhD6osDlmljuyXYTviZeG4I8ifP8AGoQcxTZxUk4y7AezIUyNPiMy4byXo7yQttxJyFD0qE1naU3C394E/WtnY+hrIuxrVlwtLzlvkJW9Z1HiUr/hlHmU+eeZT8x670e7lRzwKC23EZSpJyCDyIrDdcsHJjZ/Hf8A0WxeJW0Ya8hTLim1jCknBpNW4q3aptBUDIaT9Yj2hVOJrsf8djEi9obvJpKGzKdnNpt6XDJSoKQUc0kHY+lWG02CRcyFqBaY6rUNz8BV2tlsiWxnuorYTn2lHmr40KGxJXKPYUtrS2oDDbzURl0IHG2014Qrrj512l6FL5eAnnrvkyvUdwU+8IEXxAHx8PU+VHgWAphyTIT3jjyP0XMHG+Pidx86fWi0IiJDrw431bkmpXrzxWrKnxIvn7lSNvhtOPsZenSUmfOQzbcFpZ4i64fC0nzUfw89h8dEs9ogWKGYltScqx30lf6R8+vknyT9+TTtpCWWy2yhLaCriKU9T5n/AFtXarYuDGt8p9WWcrOdvph0QKFdrlaRngoV2uUACjRpEiBL+mweHvQnhcbUSEup8j+49KLQ2PrTJwjOPGQ6E3B8kXyz3Bi4w0PxuIA7KSoYUhQ5gjzqSbVVDsEO4KmmVbUhIB+u4jhDw8j6+R6VcoclEhvjbyDkpWgjBSocwfUVzeTT4VnFPZ0ONkeNDfZjmdDjXKC9DnMoejPJ4HG1DZQrAdV6YXoycIspx2Rb3nibY8QSGFnB8ePXHhHPGehFegkKzTa7WyLe7e7CmIyw4D40nCknoUnoRzzVZospnngF0Lewyp+TH8MqIhoIbfcJ/SDzI2Ocb4yMJzUbPihrgcbe75tsfm8p54ELWT4kEdSP+52Iqf1DYpemJ7dum44Y2Ta5SnD+cKJ94dBuMjbhOBkgmoi2fTLjNbgwbbxqUvgk29DY4mXf96M+vnsMcJ2IpBw4sdxjSmjZLkkOR1KS0lGDltfp9nOwPQ+lCP2Z3W4XgtQGVrt+cmRtlI/V3xvWuaN7NINlQmZeFpn3RScLc3CU+mM7/HrV6QhKEhKEhKUjASkYArOy8+NPpj1Y6Mdme2fs7XGiojqeaiMpHsNDjUfieWfvq7Wi2t2qCiIy684hJJy8oE7/AA2A9BT6mN1uka1xy9KVgckpHNVY92Xdf6ZPoSKKRG3dhIkrCh4HBn+NV1GnISZZkKTxb5CD7NS6tSWm4cAdccjkH30Z/aKlYyrYGVPtOtLQhJUpfHnA8z5V12Bk7xo811RgZFMlc1EiHS3EirfdIajtDKlY2A/efQU301dIt+efZSFR3GvEG1qCitHmP3jfG3nVB1rrhV4uncwQDa45IQk7d8f1/T09PjTe0XRTEtqXCc4ZDSuIJP4HzBG1SyyJN9CzXgw8P1dzahb4+Bso+vFQptb9RWybCZkmWyypxOVNuLAUg9R99dpPFl8lby0vgoNN581q3xFypCHVtowOFoAq3OOpAqJ/lIjpG/vUnJu6J8Z2IWeDvk8HEVcieX7cV0FtvofF9SjVX61zXQLJ11aYpT3sKfhWeRRTVXaLZ/dt08/FxA/dVDvue+QDthPKousB52Rv9xu+Rx/qaae0e1+7a5h/66P8tEV2kwfdtElXxlJH/wBKzWhTfO5H2F8nR9TRf/6Uxnaxq+c3/wDFA9prePDYm/8AmlqP4AVnVCk85f8Adi+Vo+qNAV2mO+5Y4f8AzPOH8CKc2ztAkz5ncG1W5oFJIOXjkj/qVm1PrI6WrrGVnmsJ+/b99N8zc3+5irGp+qPRHZ9qW4XuZIhyGYKI8ZgL/N21IKSThI3UeeFfdVhuTTlvfXcowUthQH0tkDJwP6xI8wOY6j1qvdk8EM2+fMKRxPvJb4vMIGfxWavRFHfuVbZcLdxG0dSXm0uIWlTahkFJ2UP4U8SfLaq++lVgdLze9qcVl1IH81J6j7BPPy58qmkOZAIIIIyCOVNaLcJqa2hnqWxRdRWtcOV4VgEsPpSCtleCOJOeu9Rui9JQtLRBwkSbktAQ/NUkcS8dB5AcvPbflVi4iRQFI4ckRWZHHpEMDXaJnFJypbMRhT0hQQhIySa53K/Tba25R6onpy4z6PowlznsW6Kt+QrCUjOOp9KzG73N+7TFPvEhO4QjokUrfru9eJfESUsJP1aP3mo47UzExnKaRLZZxjs62krWAASScBIqv6rvSUJcs9vdBOeGa8g5Cj/ugfIHmepGOQ3NrHUKbHGVBhr/ANqvI8akneKgj/GofcPU1TNPw1qBeV+j6IJ9uulSSXFFeqD/AHSJWG0QoKUMe9lfLFOw2AoLbylQ3/161wbDiT033HT/AFypF99SVdwwvgc4eIqVuG0dSfWgnJEXqM0O7fXFLidlcZGfnQotusmoJsJqTaNLrlQXAS0+paQXBndW++5zQo2BJTtOuIPFDXxj9RXP5GoVxLsdZQ6hSFDmFDFX6kpMViUjgkNJWOmRy+B6V1EqU+xy0bX7mP6p/pRRxhK0JWk+ed/xyPlUNW1Ruz6x3tqTMudykQ2ISu7KgpAABwrdShy8W1NXuzXQ6gFM61SgKWEJ41tL38tsb1zN0OFjidJTPnWpGP0K1tvs50KVISrXSCpay2kJSjxKGMgb89x99KN9n3Z2ru8a2cX3hIRwBHiI542qElMgoVsrPZ/2cLS2U6nuboWFFJbQCCBnP9WfI0onQHZwCgi835wKSpQAYO4AOeTO3I/dS6AxalY6+7fQv9VQV9xrbY+iuzRpxJWb4+ODj4XGXgCNx0QN9uXP0qw2fSfZzLktQotldcdUgqBfbdGQPMnr6UaYFi0TEEPS8FGMFxJeOftqKvwIqcriG0MoS22kJQgBKUgbADYCu1OjHm9ybOKSFAggEEYIPWmcC3NwUFppxZYBy22rH1foDzx5DpT2hQCk12BQoVwkAEk8qUacccS0grWQEgZJNZrqm/KusgssEiKg7fbIp5rPUffrVb4i/qxs4oHn6VU0H501k0I/Iu0SPhTLUN+a0/CD2EuT3gTFYIzjp3qh+qCDgdT6ClJ8+NaLeu4ThxtpPC0yDgvudEjyHUnoPUisylPzb/dlyZbmVuHKjjwtp5AAdAOQFRcYxe0upcqg5dWCDGeu0tyTKUpaSoredUclZJ338zVmASBwJSnhA4eFP6vl8POkWG0R2kNtApQjYee/n6muyH0xmStwkD2ceZ6AClXQsnZD/dABCQ46o4bTn2vU+lSuhNIr1dcXGluqRZoqgufLzjvjz7tJ/HyFRemLFcdWXtNugnhcWMypOMpjN/xPQdT+zZWoMZ9A0jp1KotmtqkpuDwQD9JJGS0D1JyCs4OxxSN7EYujV8hhCWNN6Wfm2lpIbiyGHm0NrSkY8IJBwCCPlQq0x2m47DbMdlDTTaQlDaNkpSOQABoUCbGEHS9pfhR3XI6ytxpKlYdWNyB60t/JKzf8Ov8A95f8ak7V/RkP/wAhH+EU7qTzF33f9kPlqfqiC/knZzCmQvo7ncTP0wDywTsBsc5GyRypgOznTIGBFkjw8O057b19vn686teK7UUpOT2yaMVFaRUx2d6bGcR5g4khJxcH+mPt7Hwjeuns806QsFmbhSQkj8oyOQxj3/QVa6FIKVJ3s50y6hxDsWUtLgSFcU5854eXv0R/s00o8l8O291QkKCncy3tyM4971NXChRsCgK0vogvykuRHgp1XfuKU6/hZTxZI36b7D0p7Z7dpa3zkS4LEhmUrJT3nfEnix7pz+t+PlVpMCGoYVEjkZzgtJ55z5ee9BMKIhQKIrCSORDYBHL+A+6l2w0R4utrJ3ccAJGCWl+LIB22+0PntRm7jblx+/4lBHGtHsqJBQSFbDyx+7nT38nwsAfQ4+AMAd0nlyxyrv0KIpPCqKwRnOO7Hlj8KNsZ4cPgZx59tkrUll1RKRk5QtO3zFFkz4MVxSJHeIKSRuDvhIJI+8D1JqRbjMNEFphtBAwOFAGBRVwoi1qWuKwpSt1KLYJO2N/ltRth4cPgjBdrepK1JS6pKTgqAyCeEqHXqB+HQiifTrdcI+EtvqaUlRyDwbDIO+Rj2VD5GpVUKItKUrisKSn2QWwQNsbfLagIEMEERI+Rkg90nbIwenltRth4cPgrELR+m5ZWRb5KCnGe8kOcyM49rnuM/Gnf8hdPD/wbn/yXP81WNKUpzwpAycnA5mjUbYvCPwVC59mulbqtpc+3uOlpHA2PpToCR6AKx6nzpBnsp0ayCGrY6kE5wJj3+ertQpNjl0KYnsu0ikYFvexjH89e/wA9FX2VaOcKSu2ukp5fnr+39+rrQoAg7JpOzWG3SIFojKisyCVOFDq+NRIxnjJ4v27U7tVkt9pt7MC3sBmKynDbYUTjfOck5zknf1qRoUAImK1n2SPgSKFLUKA0f//Z"
                                                alt=""></div>
                                    </div>
                                </div>
                            </div>
                            <div class="hot-deals-body">
                                <div class="hot-deals-body-wrapper">
                                    <div class="hot-deals-body-wrapper-content">
                                        <div class="img">
                                            <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcR8Qss7hwkA5vcJSWhaXNBFurgQpbUvT0mynQ&usqp=CAU"
                                                alt="">
                                        </div>
                                    </div>
                                    <div class="hot-deals-body-wrapper-content">
                                        <div class="img"><img
                                                src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSeYthTPmBG-mLIvOUlrXnc-qcZx3TUJx6irQ&usqp=CAU"
                                                alt=""></div>
                                    </div>
                                    <div class="hot-deals-body-wrapper-content">
                                        <div class="img"><img
                                                src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcS9EkT0nSXA1hfywRFYHLR8MNkdxhqSnCr5iQ&usqp=CAU"
                                                alt=""></div>
                                    </div>
                                </div>
                            </div>
                            <div class="hot-deals-body">
                                <div class="hot-deals-body-wrapper">
                                    <div class="hot-deals-body-wrapper-content">
                                        <div class="img">
                                            <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQwtXpjdCXEiPUpuXb2Skmu7Gl66zR0jh-y8g&usqp=CAU"
                                                alt="">
                                        </div>
                                    </div>
                                    <div class="hot-deals-body-wrapper-content">
                                        <div class="img"><img
                                                src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQjLthA5V0h60K5o6F2HiSy6NMdJkiyfQGgcw&usqp=CAU"
                                                alt=""></div>
                                    </div>
                                    <div class="hot-deals-body-wrapper-content">
                                        <div class="img"><img
                                                src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQrc8LoLYUKsBIkLSd3zSYJes5ZHanNKXttEQ&usqp=CAU"
                                                alt=""></div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="main-section-1-wrapper-right-content">
                    <div class="right-content-wrapper">
                        <div class="right-content-wrapper-header">
                            <div class="right-content-wrapper-left-header">
                                <h1>new arrivals...</h1>
                            </div>
                            <div class="right-content-wrapper-right-header">
                                <nav>
                                    <div class="nav-routes">
                                        <div class="route"><button>all</button></div>
                                        <div class="route"><button>shoes</button></div>
                                        <div class="route"><button>clothing</button></div>
                                        <div class="route"><button>machines</button></div>
                                        <div class="route"><button>spare parts</button></div>
                                    </div>
                                </nav>
                                <div class="nav-options">
                                    <button><i class="fa-solid fa-ellipsis"></i></button>
                                </div>
                            </div>
                        </div>
                        <div class="right-content-wrapper-body">
                            <div class="body-wrapper">
                                <div class="body-wrapper-container">
                                    <div class="img"><img
                                            src="data:image/jpeg;base64,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"
                                            alt=""></div>
                                    <div class="body-wrapper-container-detail">

                                        <p>product name</p>
                                        <button>view more...</button>
                                    </div>
                                </div>
                                <div class="body-wrapper-container">
                                    <div class="img"><img
                                            src="data:image/jpeg;base64,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"
                                            alt=""></div>
                                    <div class="body-wrapper-container-detail">

                                        <p>product name</p>
                                        <button>view more...</button>
                                    </div>
                                </div>
                                <div class="body-wrapper-container">
                                    <div class="img"><img
                                            src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRu1wcILBG4LXkOguTFqi8J6keq1j-Ghf-LzQ&usqp=CAU"
                                            alt=""></div>
                                    <div class="body-wrapper-container-detail">

                                        <p>product name</p>
                                        <button>view more...</button>
                                    </div>
                                </div>
                                <div class="body-wrapper-container">
                                    <div class="img"><img
                                            src="data:image/jpeg;base64,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"
                                            alt=""></div>
                                    <div class="body-wrapper-container-detail">

                                        <p>product name</p>
                                        <button>view more...</button>
                                    </div>
                                </div>
                                <div class="body-wrapper-container">
                                    <div class="img"><img
                                            src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRjHR7blawscfM_x3S7IjwYPaUL7-pHJaNnbw&usqp=CAU"
                                            alt=""></div>
                                    <div class="body-wrapper-container-detail">

                                        <p>product name</p>
                                        <button>view more...</button>
                                    </div>
                                </div>
                                <div class="body-wrapper-container">
                                    <div class="img"><img
                                            src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcREUNVxZJbftRH11qSq22KB2LmoIX9mnCjtKg&usqp=CAU"
                                            alt=""></div>
                                    <div class="body-wrapper-container-detail">

                                        <p>product name</p>
                                        <button>view more...</button>
                                    </div>
                                </div>
                                <div class="body-wrapper-container">
                                    <div class="img"><img
                                            src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRrO86WJNe3W4i68ddvTij_RRc6SmJkeM-ZYg&usqp=CAU"
                                            alt=""></div>
                                    <div class="body-wrapper-container-detail">

                                        <p>product name</p>
                                        <button>view more...</button>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="main-section-2">
            <div class="main-section-2-wrapper">
                <div class="main-section-2-wrapper-content">

                    <div class="img"><img
                            src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSThzoaY0MNgzJ4EQM5hAT9X0B66VLg5vpepw&usqp=CAU"
                            alt=""></div>
                    <div class="details">
                        <p>$20 - $500</p>
                        <h3>product name</h3>
                    </div>
                </div>
                <div class="main-section-2-wrapper-content">

                    <div class="img"><img
                            src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSAsFtq4u1iBrnEKLTKTyNyJZvAxEMe2S-nnQ&usqp=CAU"
                            alt=""></div>
                    <div class="details">
                        <p>$20 - $500</p>
                        <h3>product name</h3>
                    </div>
                </div>
                <div class="main-section-2-wrapper-content">

                    <div class="img"><img
                            src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTGmP_8Fubw0yNAn0HF3c_HEoWk-R6XPVUPIA&usqp=CAU"
                            alt=""></div>
                    <div class="details">
                        <p>$20 - $500</p>
                        <h3>product name</h3>
                    </div>
                </div>
                <div class="main-section-2-wrapper-content">

                    <div class="img"><img
                            src="data:image/jpeg;base64,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"
                            alt=""></div>
                    <div class="details">
                        <p>$20 - $500</p>
                        <h3>product name</h3>
                    </div>
                </div>
                <div class="main-section-2-wrapper-content">

                    <div class="img"><img
                            src="data:image/jpeg;base64,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"
                            alt=""></div>
                    <div class="details">
                        <p>$20 - $500</p>
                        <h3>product name</h3>
                    </div>
                </div>
                <div class="main-section-2-wrapper-content">

                    <div class="img"><img
                            src="data:image/jpeg;base64,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"
                            alt=""></div>
                    <div class="details">
                        <p>$20 - $500</p>
                        <h3>product name</h3>
                    </div>
                </div>
                <div class="main-section-2-wrapper-content">

                    <div class="img"><img
                            src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcS2ZhXpfr0NEqkuKnPjtaxFLS1n-KuwyoFcSw&usqp=CAU"
                            alt=""></div>
                    <div class="details">
                        <p>$20 - $500</p>
                        <h3>product name</h3>
                    </div>
                </div>
                <div class="main-section-2-wrapper-content">

                    <div class="img"><img
                            src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRClkj4xBfHa7tCDxC6Bp4fDstk_dKpq3LKaQ&usqp=CAU"
                            alt=""></div>
                    <div class="details">
                        <p>$20 - $500</p>
                        <h3>product name</h3>
                    </div>
                </div>
                <div class="main-section-2-wrapper-content">

                    <div class="img"><img
                            src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT7R2gAMn4FQWkB0iI88wHlJb1seuPvtMPsUQ&usqp=CAU"
                            alt=""></div>
                    <div class="details">
                        <p>$20 - $500</p>
                        <h3>product name</h3>
                    </div>
                </div>
                <div class="main-section-2-wrapper-content">

                    <div class="img"><img
                            src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT3uOirD0lukBjQWe_9SN_RWUxSemd5m6J7zw&usqp=CAU"
                            alt=""></div>
                    <div class="details">
                        <p>$20 - $500</p>
                        <h3>product name</h3>
                    </div>
                </div>
            </div>
        </div>
    </main>
</template>

<script >
import carousel from '../components/carousel.vue'
import { ref } from 'vue'

export default {
    name: 'carousel',

    components: {
        carousel
    }, setup() {
        const images = ref([
            "https://s3.envato.com/files/379243010/Retail%20Shopping%20(8).JPG", "https://c8.alamy.com/comp/2J5A49J/e-commerce-ecommerce-web-banner-on-violet-background-various-shopping-icons-online-shopping-concept-2J5A49J.jpg", "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSBFNc5TzSEqnmcPGsXg13507uO5VX4OGXUqw&usqp=CAU", "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSiqYLK3MWQ6OFSTi1cyi2vC0rXw_9NF0nGnw&usqp=CAU"
        ])
        return { images }
    }
}

</script>

<style lang="scss" scoped>
$prime-color: rgb(209, 59, 0);

main {
    width: 100vw;
    height: fit-content;

    header {
        max-width: 100%;
        height: 23vh;
        padding: 0;
        margin: 0;

        .top-header {
            width: 100%;
            height: 35%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            background: rgb(30, 30, 38);


            .logo {
                width: 20%;
                height: 90%;
                display: flex;
                justify-content: center;
                align-items: center;
                font-size: 20px;
                font-weight: 600;
                color: white;
                font-family: "Poppins", sans-serif;

            }

            .info-links {
                width: 35%;
                height: 100%;
                display: flex;
                justify-content: center;
                align-items: center;

                .info-links-wrapper {
                    height: 60%;
                    width: 100%;
                    display: flex;
                    justify-content: space-evenly;
                    align-items: center;

                    .content {
                        width: 30%;
                        height: 100%;
                        display: flex;
                        align-items: center;
                        justify-content: center;


                        i {
                            color: rgb(236, 235, 235);
                            font-size: 12px;
                        }

                        a {
                            color: rgb(224, 224, 224);
                            font-size: 11px;
                            font-family: "Nunito Sans", sans-serif;
                            letter-spacing: 1px;
                        }

                        .left-content {
                            width: fit-content;
                            height: 100%;
                            display: flex;
                            justify-content: flex-end;
                            align-items: center;

                            i {
                                font-size: 19px;
                            }
                        }

                        .right-content {
                            min-width: 80%;

                            display: flex;
                            justify-content: flex-start;
                            align-items: center;
                            flex-direction: column;
                        }

                        .content-flex {
                            width: 100%;
                            display: flex;
                            justify-content: space-between;
                            align-items: center;


                            i {
                                font-size: 15px;
                                width: 25%;
                                display: flex;
                                justify-content: center;
                                align-items: center;

                            }

                            a {
                                width: 75%;
                                display: flex;
                                font-size: 11px;
                                justify-content: flex-start;
                                align-items: center;
                            }
                        }
                    }

                    .flex-row {
                        width: 30%;
                        flex-direction: row;
                    }

                    .flex-column {
                        width: 50%;
                        flex-direction: column;
                    }
                }
            }
        }

        .bottom-header {
            width: 100%;
            height: 65%;
            display: flex;
            justify-content: space-around;
            align-items: center;
            box-shadow: 0 5px 5px 7px rgb(30, 30, 38);


            .left-bottom-header {
                width: 15%;
                height: 100%;
                cursor: pointer;
                display: flex;
                justify-content: center;
                align-items: center;
                // border-right:1px solid rgb(30,30,38);
                font-size: 20px;
                font-weight: 600;
                box-shadow: -5px 0 5px 3px rgb(30, 30, 38);

                i {
                    font-size: 20px;
                }
            }

            .bottom-header-routes {
                width: 50%;
                height: 100%;
                display: flex;
                justify-content: center;
                align-items: center;

                .routes-wrapper {
                    width: 100%;
                    height: 100%;
                    display: flex;
                    justify-content: space-evenly;
                    align-items: center;

                    a {
                        color: rgb(32, 32, 32);
                        text-transform: capitalize;
                        font-size: 18px;
                        font-weight: 600;
                    }
                }
            }

            .right-bottom-header {
                width: 22%;
                height: 100%;
                display: flex;
                justify-content: space-evenly;
                align-items: center;

                .content-wrapper {
                    width: 100%;
                    height: 100%;
                    display: flex;
                    justify-content: space-evenly;
                    align-items: center;

                    .search-box-wrapper {
                        width: 100%;
                        display: flex;
                        justify-content: center;
                        align-items: center;
                        border: 1px solid $prime-color;

                        input {
                            width: 75%;
                            height: 40px;
                            padding: 2px 5px;
                            padding-left: 15px;
                            outline: none;
                            border: none;
                        }

                        button {
                            width: 25%;
                            height: 40px;
                            padding: 2px 5px;
                            outline: none;
                            border: none;
                            display: flex;
                            justify-content: center;
                            align-items: center;
                            background: rgb(209, 59, 0);
                            border-radius: 0;

                            i {
                                font-size: 22px;
                                color: rgb(235, 235, 235);
                            }


                        }
                    }
                }
            }

            .cart {
                width: 10%;
                height: 100%;
                display: flex;
                justify-content: center;
                align-items: center;

                .cart-wrapper {
                    width: 100%;
                    height: 40px;
                    display: flex;
                    justify-content: center;
                    align-items: center;
                    border: 1px solid $prime-color;
                    background: $prime-color;

                    button {
                        width: 100%;
                        height: 100%;
                        display: flex;
                        justify-content: center;
                        align-items: center;
                        outline: none;
                        border: none;
                        background: none;
                        color: white;
                        font-size: 12px;

                        i {
                            color: white;
                            font-size: 19px;
                        }
                    }
                }
            }
        }
    }

    .landing-page {
        width: 100vw;
        height: 70vh;
        background: rgb(240, 240, 240);

        .main-wrapper {
            width: 100%;
            height: 100%;
            display: flex;
            justify-content: flex-start;
            align-items: center;
            position: relative;

            .main-wrapper-content {
                width: 55%;
                height: fit-content;
                position: relative;
                z-index: 1;

                margin-left: 10%;
                padding: 10px;

                h3 {
                    font-size: 13px;
                    font-weight: 500;
                    padding: 0;
                    margin: 0;
                    color: rgb(235, 234, 234);
                    font-family: "Nunito Sans", sans-serif;
                    word-spacing: 10px;
                }

                h1 {
                    font-size: 55px;
                    font-weight: 600;
                    text-transform: capitalize;
                    font-family: "Nunito Sans", sans-serif;
                    margin: 0;
                    margin: 35px 0;
                    margin-top: 10px;
                    padding: 0;
                    color: rgb(219, 219, 219);
                    word-spacing: 7px;
                    line-height: 70px;
                }

                a {
                    width: 200px;
                    height: 50px;
                    font-size: 15px;
                    display: flex;
                    justify-content: center;
                    align-items: center;
                    border-radius: 3px;
                    background: $prime-color;
                    color: white;
                    text-transform: uppercase;
                    margin: 0;
                }
            }

            .carousel-wrapper {
                width: 100%;
                height: 100%;
                position: absolute;
                top: 0;
                left: 0;
            }
        }
    }

    .main-section-1 {
        width: 100vw;
        height: fit-content;
        padding: 10px 1%;
        padding-top: 3%;
        margin: 0;
        background: rgb(236, 235, 235);

        .main-section-1-wrapper {
            width: 100%;
            height: 100%;
            display: flex;
            justify-content: space-evenly;
            align-items: center;

            .main-section-1-wrapper-left-content {
                width: 30%;
                height: fit-content;


                .hot-deals {
                    width: 100%;
                    height: fit-content;

                    .hot-deals-wrapper {
                        width: 100%;
                        height: fit-content;

                        .hot-deals-header {
                            width: 100%;
                            height: 90px;
                            background: white;

                            nav {
                                width: 100%;
                                height: 100%;
                                display: flex;
                                justify-content: space-between;
                                align-items: center;

                                .nav-left-content {
                                    width: 60%;
                                    height: 100%;
                                    display: flex;
                                    justify-content: center;
                                    align-items: center;

                                    h1 {
                                        font-size: 22px;
                                        text-transform: uppercase;
                                        font-family: "Nunito Sans", sans-serif;
                                        font-weight: 900;
                                    }
                                }

                                .nav-right-content {
                                    width: 40%;
                                    height: 100%;

                                    display: flex;
                                    justify-content: space-evenly;
                                    align-items: center;

                                    button {
                                        width: 40px;
                                        height: 40px;
                                        background: $prime-color;
                                        border-radius: 100%;
                                        color: white;
                                        display: flex;
                                        justify-content: center;
                                        align-items: center;
                                    }

                                    p {
                                        font-weight: 600;
                                    }
                                }
                            }
                        }

                        .hot-deals-body {
                            width: 100%;
                            height: fit-content;
                            margin-top: 25px;
                            padding: 10px;
                            background: white;

                            .hot-deals-body-wrapper {
                                width: 100%;
                                height: 100%;
                                display: flex;
                                justify-content: space-evenly;
                                align-items: center;
                                flex-wrap: wrap;

                                .hot-deals-body-wrapper-content {
                                    width: 150px;
                                    height: 150px;

                                    .img {
                                        width: 100%;
                                        height: 100%;
                                        overflow: hidden;
                                        display: flex;
                                        justify-content: center;
                                        align-items: center;
                                        cursor: pointer;

                                        img {
                                            width: auto;
                                            height: 100%;
                                            object-fit: cover;
                                        }
                                    }

                                    &:hover {
                                        .img img {
                                            transform: scale(1.1);
                                        }
                                    }
                                }
                            }
                        }
                    }
                }
            }

            .main-section-1-wrapper-right-content {
                width: 60%;
                height: fit-content;
                background: white;
                border-radius: 3px;

                .right-content-wrapper {
                    width: 100%;
                    height: 100%;

                    .right-content-wrapper-header {
                        width: 100%;
                        height: 110px;
                        display: flex;
                        justify-content: space-between;
                        align-items: center;

                        .right-content-wrapper-left-header {
                            width: 30%;
                            height: 100%;
                            display: flex;
                            justify-content: center;
                            align-items: center;

                            h1 {
                                font-size: 25px;
                                font-weight: 700;
                                text-transform: uppercase;
                            }
                        }

                        .right-content-wrapper-right-header {
                            width: 65%;
                            height: 100%;
                            display: flex;
                            justify-content: space-evenly;
                            align-items: center;

                            nav {
                                width: 100%;
                                height: 100%;

                                .nav-routes {
                                    width: 100%;
                                    height: 100%;
                                    display: flex;
                                    justify-content: space-evenly;
                                    align-items: center;

                                    .route {
                                        width: max-content;

                                        button {
                                            border: none;
                                            background: transparent;
                                            text-transform: capitalize;

                                        }
                                    }

                                }
                            }

                            .nav-options {
                                width: 7%;
                                height: 100%;
                                display: flex;
                                justify-content: center;
                                align-items: center;

                                button {
                                    background: transparent;
                                    border: none;
                                    outline: none;
                                }
                            }
                        }
                    }

                    .right-content-wrapper-body {
                        width: 100%;
                        height: fit-content;

                        .body-wrapper {
                            width: 100%;
                            height: 100%;
                            display: flex;
                            justify-content: space-evenly;
                            align-items: flex-start;
                            flex-wrap: wrap;
                            gap: 10px;

                            .body-wrapper-container {
                                width: fit-content;
                                height: 300px;
                                padding: 10px;
                                margin-bottom: 30px;
                                transition: all 0.4s ease;

                                .img {
                                    width: 100%;
                                    height: 60%;
                                    overflow: hidden;
                                    cursor: pointer;

                                    img {
                                        width: auto;
                                        height: 100%;
                                        object-fit: cover;
                                    }
                                }

                                .body-wrapper-container-detail {
                                    width: 90%;
                                    margin: 0 auto;


                                    p {
                                        font-size: 14px;
                                        text-transform: capitalize;
                                        font-weight: 600;
                                    }

                                    button {
                                        width: 90%;
                                        height: 40px;
                                        border-radius: 0;
                                        font-size: 13px;
                                        outline: none;

                                        &:hover {
                                            background: $prime-color;
                                            color: white;
                                            border-radius: 3px;
                                            border: none;

                                        }
                                    }
                                }

                                &:hover {
                                    transform: scale(1.1);
                                    box-shadow: 0 0 10px 6px rgb(233, 232, 232);
                                }

                            }
                        }
                    }
                }
            }
        }
    }

    .main-section-2 {
        width: 100vw;
        height: fit-content;
        background: rgb(236, 235, 235);
        border-top: 2px solid white;
        display: flex;
        justify-content: center;
        align-items: flex-start;

        .main-section-2-wrapper {
            width: 90%;
            height: 100%;
            padding-top: 3%;
            // margin:0 auto;
            display: flex;
            justify-content: flex-start;
            align-items: flex-start;
            flex-wrap: wrap;
            gap: 0;

            .main-section-2-wrapper-content {
                width: fit-content;
                height: fit-content;
                position: relative;
                margin: 0;
                box-shadow: 0 0 1px 1px rgb(235, 233, 233);
                .details {
                    width: 100%;
                    position: absolute;
                    top: 0;
                    left: 0;

                }

                .img {
                    position: relative;
                    width: 280px;
                    height: 300px;
                    cursor: pointer;
                    overflow: hidden;

                    img {
                        width: auto;
                        height: 100%;
                        object-fit: cover;
                    }
                }
            }

        }
    }
}
</style>
