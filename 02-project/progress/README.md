# Progress notes

One note per hour of the window, named `NN-HHMM.md`: the hour number, then
the time you wrote it. Example: `03-1145.md` is the note for hour 3.

Start from `templates/hourly-note.md`. Each note needs at least one
screenshot from `02-project/images/`, listed on the `Images:` line

    Images: h3-tests-green.png, h3-agent-plan.png

or linked:

    ![tests passing](../images/h3-tests-green.png)

Example note:

    ## Hour 3 · 11:00

    Stage:     Build → starting Test
    Done:      the first feature end to end, with tests
    AI did:    the first version of the code and its tests
    I fixed:   the AI skipped a rule from my design; I found it in review,
               rewrote the function and added a test
    Blocked:   nothing
    Images:    h3-tests-green.png
