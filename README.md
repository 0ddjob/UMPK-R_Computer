# УМПК-Р (UMPK-R) Computer
Information about the Soviet Ukrainian computer based on the Soviet homebrew computer called the [РАДИО-86РК](https://github.com/skiselev/radio-86rk) (RADIO-86RK).  I'll refer to it as the "RK" (Radio Computer) for the rest of this description.  This computer utilised the Soviet equivalent of the Intel 8080A called the КР580ВМ80А.<br>

My computer doesn't work so I need to troubleshoot, hence this translation work.  The Soviets were very good in including schematics & documentation how the computer works.<br>

There were quite a few industrially produced clones of the RK design so understanding how it works can help with troubleshooting other machines.<br>

![Image of my УМПК-Р 32](UMPK-R_32.jpg)

## My YouTube Videos (As of 9-Mar-2025)
- [УМПК-Р (UMPK-R): Part 1 (First Look)](https://youtu.be/Kr2Yl7z__qQ)
- [УМПК-Р (UMPK-R): Part 2 (Trying to get video output)](https://youtu.be/anAznSh7gso)
- [УМПК-Р (UMPK-R): Part 3 (Video output troubleshooting continues)](https://youtu.be/vZf2vCqavNA)
- [УМПК-Р (UMPK-R): Part 4 (Faulty DRAM?)](https://youtu.be/Y1xS1cXXh0Q)

## English Documentation
I have done a partial translation (thanks to Grok) of the Operation Manual - original scanned Russian, my cleaned-up Russian and the translated English manuals can be found here.  There are four file types:
- Apple Pages (native)
- PDF
- Rich Text Format
- MS Word

Note that there may be errors in my cleaned-up Russian copy ... some words in the scanned manual disappeared into the page binding!<br>

Question: what on earth is "foiled lavsan" (фольгированный лавсан)?<br>

_"Lavsan" is a Russian trade name for a type of polyester film, chemically known as polyethylene terephthalate (PET). It is similar to materials like Mylar in Western terminology. "Фольгированный" means "foiled" or "coated with foil," indicating that the lavsan film has a thin layer of metal foil (often aluminium) applied to it. In the context of the УМПК-Р keyboard device, this refers to a metallised polyester film used in the membrane keyboard construction, where the foil provides conductive tracks or contacts for key operation._<br>

_So, in technical terms, it could be described as "metallised polyester film" or simply "foiled PET film", depending on the context._

In the English translation I have kept the Soviet/Russian part identifiers rather than transliterate them, but I have included Western equivalent part identifiers as well.<br>

The scanned Russian manual includes the tables & diagrams referred to in the translation.  It also includes a map of the parts on the motherboard.<br>

I have also included some very-roughly machine translated (Google image) pages from the original Soviet RADIO magazine that explain the RK's functionality - I hope to come back and do better translations.<br>

## Memory Layout
![RAM layout](УМПК-Р_Memory_Layout_ENG.jpg)

## Map of ICs
![Main ICs on the motherboard](UMPK-R_circuit_layout.jpg)
```
- D1    КР580ГФ24   8224    Clock generator
- D2    КР580ВТ57   8257    DMA controller
- D3    К155ИЕ4     74LS92  Divide-by-12 counter
- D4    К155ЛИ1     74LS08  Quad 2IN AND
- D5    КР580ВМ80А  8080A   CPU
- D6    К155ЛП5     74LS86  Quad 2IN XOR
- D7    К589ИР12    8212    8-bit I/O port
- D8    КР580ВГ75   8275    CRT controller
- D9    К555ИД7     74LS138 1-of-8 decoder/demultiplexer
- D10   К155ЛА8     74LS01  Quad 2IN NAND
- D11   К155ЛН1     74LS04  Hex inverter
- D12   К573РФ2     2716    EPROM (for character data)
- D13   К155ТМ2     74LS74  Dual D-type flip flop
- D14   КР580ВВ55А  8255    Programmable peripheral adaptor
- D15   К155ИР1     74LS95  4-bit shift register
- D16   К155ИР13    74LS198 8-bit shift register
- D17   К555КП11    74LS257 Quad 2IN multiplexer
- D18   К555КП11    74LS257 Quad 2IN multiplexer
- D19   К573РФ5     2716    EPROM (for MONITOR)
- D20   КР565РУ5Д1          32K x 1bit DRAM
- D21   КР565РУ5Д1          32K x 1bit DRAM
- D22   КР565РУ5Д1          32K x 1bit DRAM
- D23   КР565РУ5Д1          32K x 1bit DRAM
- D24   КР580ВВ55А  8255    Programmable peripheral adaptor
- D25   КР565РУ5Д1          32K x 1bit DRAM
- D26   КР565РУ5Д1          32K x 1bit DRAM
- D27   КР565РУ5Д1          32K x 1bit DRAM
- D28   КР565РУ5Д1          32K x 1bit DRAM
- D29   К553УД2     LM301   Op. Amp.
```
