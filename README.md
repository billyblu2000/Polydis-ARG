# AccoMontage2 and Beyond

> A useful tool to generate chord progressions and accompaniment according to melody MIDIs.
> 
> Work in progress build upon AccoMontage2: https://dclibrary.mbzuai.ac.ae/mlfp/258/



### Archive
Try out our previous version from https://github.com/JohnnyHHU/Chorderator with the demo below.

### Demo

```python
import chorderator as cdt

if __name__ == '__main__':

    demo_name = 'hpps30'
    input_melody_path = 'MIDI demos/inputs/' + demo_name + '/melody.mid'

    cdt.set_melody(input_melody_path)
    cdt.set_meta(tonic=cdt.Key.A)
    cdt.set_segmentation('A8B8A8B8')
    cdt.set_texture_prefilter((0, 2))
    cdt.set_note_shift(16)
    cdt.set_output_style(cdt.Style.POP_STANDARD)
    cdt.generate_save(demo_name + '_output_results')
    
```

### Run GUI

Please check all the requirements in ``backend/requirments.txt`` are satisfied, and run

```
python backend/app.py
```

You can interact with the GUI at http://127.0.0.1:5000.