# Ruch harmoniczny i drgania układu masa-sprężyna

## Układ masa-sprężyna jest klasycznym przykładem oscylatora harmonicznego. Gdy ciało zostaje wychylone od położenia równowagi, sprężyna wywołuje siłę przywracającą, która jest proporcjonalna do wychylenia i działa przeciwnie do jego kierunku. W rezultacie masa wykonuje drgania okresowe, a jej położenie, prędkość i przyspieszenie zmieniają się sinusoidalnie w czasie. Częstotliwość drgań zależy od masy ciała oraz stałej sprężystości, zgodnie z zależnością $\omega = \sqrt{k/m}$. To proste, ale bardzo ważne zjawisko opisuje wiele procesów mechanicznych i jest fundamentem analizy drgań w fizyce.

### Energia i rezonans w drganiach

W ruchu harmonicznym energia układu jest nieustannie zamieniana między energię potencjalną sprężyny a energię kinetyczną ciała. W położeniu skrajnym energia potencjalna osiąga maksimum, natomiast w położeniu równowagi maksymalna jest energia kinetyczna. Przy odpowiednio dobranej częstotliwości wymuszenia może wystąpić rezonans, polegający na gwałtownym wzroście amplitudy drgań. To zjawisko jest kluczowe w wielu zastosowaniach technicznych, od konstrukcji mostów po układy pomiarowe i urządzenia mechaniczne.


# Oscylator harmoniczny

## Wprowadzenie

Układ masa-sprężyna jest jednym z najważniejszych modeli w mechanice. Gdy ciało zostaje wychylone od położenia równowagi, sprężyna wywiera siłę przywracającą, która przeciwdziała odchyleniu. W efekcie ciało wykonuje drgania okresowe, a jego położenie zmienia się w czasie zgodnie z prawem harmonicznym. Dla takiego układu możemy zapisać zależność $x(t)=A\cos(\omega t+\phi)$, gdzie $A$ jest amplitudą, a $\omega$ częstotliwością kołową.

Warto zauważyć, że w ruchu harmonicznym energia nie znika, lecz zamienia się między energią potencjalną a kinetyczną. To zjawisko można analizować zarówno teoretycznie, jak i eksperymentalnie, co czyni ten model bardzo użytecznym do opisu różnych układów fizycznych.

## Energia i rezonans

W układzie sprężynowym energia potencjalna wyraża się wzorem $E_p=\frac{1}{2}kx^2$, a energia kinetyczna jako $E_k=\frac{1}{2}mv^2$. Wartość całkowita zależy od stanu układu, ale przy braku tłumienia pozostaje stała. W praktyce jednak w rzeczywistych układach występują opory, które rozpraszają energię i prowadzą do zaniku amplitudy drgań.

Jeśli częstość wymuszenia zbliży się do częstotliwości własnej układu, pojawia się **rezonans**. W takim stanie amplituda drgań może gwałtownie wzrosnąć, co ma duże znaczenie w technice i fizyce. Przeanalizowanie tego zjawiska jest kluczowe dla bezpieczeństwa konstrukcji mechanicznych.

- masa ciała wpływa na częstotliwość drgań,
- stała sprężystości określa sztywność układu,
- amplituda zależy od warunków początkowych,
- rezonans pojawia się przy dopasowanej częstotliwości wymuszenia.

1. Zmierz masę ciała.
2. Określ stałą sprężystości.
3. Wychyl ciało od równowagi.
4. Obserwuj zmiany położenia i prędkości.
5. Porównaj wyniki z modelem teoretycznym.

- [x] przygotowano opis modelu fizycznego,
- [x] zapisano zależności matematyczne,
- [x] wyróżniono podstawowe zjawiska,
- [ ] sprawdzono wyniki eksperymentalne.

| Wielkość | Symbol | Jednostka |
| --- | --- | --- |
| masa | $m$ | kg |
| stała sprężystości | $k$ | N/m |
| wychylenie | $x$ | m |
| częstotliwość | $f$ | Hz |
| energia | $E$ | J |

Link do Google Colab: [Google Colab](http://colab.research.google.com)

![Wykres drgań układu masa-sprężyna](wykres.png)

```python
import numpy as np
import matplotlib.pyplot as plt

m = 0.5
k = 20.0
omega = np.sqrt(k / m)

t = np.linspace(0, 5, 500)
x = 0.1 * np.cos(omega * t)

plt.plot(t, x, label="x(t)")
plt.xlabel("Czas [s]")
plt.ylabel("Wychylenie [m]")
plt.title("Ruch harmoniczny")
plt.grid(True)
plt.legend()
plt.show()
