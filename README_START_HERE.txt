VOCAL SUITE  -  all-in-one vocal plugin (VST3) for FL Studio
=============================================================

You do NOT install JUCE or Visual Studio. GitHub builds the plugin for you.

STEP 1  Unzip this folder on your PC.
STEP 2  Make a free account at https://github.com
STEP 3  Click "+" (top right) > "New repository". Name it VocalSuite, set it to
        PUBLIC (free build minutes), click "Create repository".
STEP 4  On the empty repo page click "uploading an existing file".
        Open the unzipped folder, select EVERYTHING inside it
        (CMakeLists.txt, Source folder, .github folder, etc.) and drag it into the browser.
        Click "Commit changes".

        !! If the ".github" folder did not upload (you can't see it in the repo):
           In the repo click "Add file" > "Create new file".
           In the name box type exactly:   .github/workflows/build.yml
           Open WORKFLOW_COPY_PASTE.txt, copy all of it, paste it in the big box,
           click "Commit changes".

STEP 5  Click the "Actions" tab. A build called "Build VST3" starts by itself
        (5-10 minutes). Wait for the green check mark.
        (If nothing starts: Actions > Build VST3 > "Run workflow".)
STEP 6  Click the finished build, scroll to "Artifacts" at the bottom, download
        "VocalSuite-VST3". Unzip it. You get a folder called  "Vocal Suite.vst3".
STEP 7  Copy that whole "Vocal Suite.vst3" folder into:
            C:\Program Files\Common Files\VST3
STEP 8  FL Studio: Options > Manage plugins > "Find installed plugins" (verify/rescan).
        Then add it on a mixer insert: click an FX slot > "Vocal Suite".

If the build fails (red X): click it, open the failed step, copy the red error
text and send it to me.

HOW TO USE
----------
* Pick a preset at the top (arrows < > or the dropdown). FL's own preset menu works too.
* For the pitch-correction presets, SET THE KEY AND SCALE to your song's key.
  Notes get pulled to the nearest note in that scale.
* Retune Speed: 0 ms = hard "T-Pain" tuning, 100+ ms = subtle/natural.
* Chain: Input > Low Cut > Gate > Pitch Correct > EQ > De-esser > Compressor
         > Saturation > Delay > Reverb > Output + limiter.
* Double-click any knob to reset it.
* The plugin reports ~512 samples (about 11 ms) of latency. FL compensates automatically.
* Works best on a single mono vocal (one voice, no harmonies in the same track).
