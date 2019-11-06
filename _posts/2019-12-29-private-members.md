---
title: 'Private Members'

layout: nil
---

<style>
    table {
        width: 100%;
    }
    tr {
        border-top: 1px solid black;
        border-bottom: 1px solid black;
    }
    table tr td:nth-child(1) {
        width: 20%;
        vertical-align: top;
        text-align: right;
    }
    table tr td:nth-child(2) {
        width: 80%;
        vertical-align: top;
        padding-left: 20px;
    }
    table tr td:nth-child(2)::first-line {
        font-weight: bold;
        font-size: 110%;
    }
</style>

### Private Members
<table>
    <tr>
        <td> int </td>
        <td> currentNote <br>
        Currently or recently played note.
        </td>
    </tr>
    <tr>
        <td> int </td>
        <td> patternSelectionNote <br>
        Currently or recently selected pattern selection note.
        </td>
    </tr>
    <tr>
        <td> int </td>
        <td> selectedFiles <br>
        Currently selected pattern files on GUI.
        </td>
    </tr>
    <tr>
        <td> double </td>
        <td> length <br>
        Length in seconds of current sample buffer.
        </td>
    </tr>
    <tr>
        <td> double </td>
        <td> sourceSampleRate <br>
        Sampling rate of original sample file.
        </td>
    </tr>
    <tr>
        <td> double </td>
        <td> hostSampleRate <br>
        Sampling rate of host or DAW.
        </td>
    </tr>
    <tr>
        <td> double </td>
        <td> pitchRatio <br>
        Global pitch ratio compared to original sample for pitch bending.
        </td>
    </tr>
    <tr>
        <td> double </td>
        <td> lengthRatio <br>
        Global length ratio compared to original sample to adjust to host BPM.
        </td>
    </tr>
    <tr>
        <td> bool </td>
        <td> modeState <br>
        Playing mode whether current mode is single note or pattern.
        <br> True - pattern
        <br> False - single note
        </td>
    </tr>
    <tr>
        <td> bool </td>
        <td> playingState <br>
        Playing state whether sample is currently playing or not.
        </td>
    </tr>
    <tr>
        <td> bool </td>
        <td> transportState <br>
        </td>
    </tr>
    <tr>
        <td> bool </td>
        <td> fileLoadState <br>
        State whether a file is loaded to sampler. This become true when using setUsingSingleNote(), setUsingPattern() or setUsingModified().
        </td>
    </tr>
    <tr>
        <td> bool </td>
        <td> bufferChangeState <br>
        State whether buffer is changed compared to previous sample. 
        </td>
    </tr>
    <tr>
        <td> bool </td>
        <td> modifyingState <br>
        State whether user is trying to modify pattern sample or using modify().
        </td>
    </tr>
    <tr>
        <td> bool </td>
        <td> deleteState <br>
        State whether user is trying to delete segment or slice.
        </td>
    </tr>
    <tr>
        <td> int </td>
        <td> deleteIndex <br>
        Index of currently deleting segment or slice.
        </td>
    </tr>
    <tr>
        <td> Array&lt;double&gt; </td>
        <td> tempos <br>
        Tempo or BPM of currently selected files or selectedFiles.
        </td>
    </tr>
    <tr>
        <td> Array&lt;double&gt; </td>
        <td> pitches <br>
        Array of pitch changes of segments. Default values are 0.0 for each segments.
        </td>
    </tr>
    <tr>
        <td> Array&lt;double&gt; </td>
        <td> initSegmentPos <br>
        Array of segment positions when pattern sample is initialized or setUsingPattern() is used.
        </td>
    </tr>
    <tr>
        <td> Array&lt;double&gt; </td>
        <td> segmentPos <br>
        Array of current segment positions.
        </td>
    </tr>
    <tr>
        <td> Array&lt;double&gt; </td>
        <td> prevSegmentPos <br>
        Array of previous segment positions after pattern sample is modified or setUsingModified() is used.
        </td>
    </tr>
    <tr>
        <td> Array&lt;double&gt; </td>
        <td> tempSegmentPos <br>
        Array of temporary segment positions when pattern sample is modifying or user is modifying segments on GUI.
        </td>
    </tr>
    <tr>
        <td> Array&lt;double&gt; </td>
        <td> slicePos <br>
        Array of current slice positions.
        </td>
    </tr>
    <tr>
        <td> Array&lt;double&gt; </td>
        <td> sliceIndices <br>
        Indices of segments that are slice.
        </td>
    </tr>
    <tr>
        <td> StringArray </td>
        <td> sampleFileNames <br>
        Base file name of currently selected pattern files.
        </td>
    </tr>
    <tr>
        <td> File </td>
        <td> currentPattern <br>
        Full path or file of current pattern sample. 
        </td>
    </tr>
    <tr>
        <td> File </td>
        <td> patternInfo <br>
        Full path or file of pattern metadata file.
        </td>
    </tr>
    <tr>
        <td> File </td>
        <td> singleInfo <br>
        Full path or file of single metadata file.
        </td>
    </tr>
    <tr>
        <td> ScopedPointer&lt;XmlElement&gt; </td>
        <td> singleParsed <br>
        Parsed XML information of single metadata file. 
        </td>
    </tr>
    <tr>
        <td> ScopedPointer&lt;XmlElement&gt; </td>
        <td> patternParsed <br>
        Parsed XML information of pattern metadata file. 
        </td>
    </tr>
    <tr>
        <td> ScopedPointer&lt;AudioFormatReader&gt; </td>
        <td> reader <br>
        </td>
    </tr>
    <tr>
        <td> ScopedPointer&lt;AudioFormatManager&gt; </td>
        <td> formatManager <br>
        </td>
    </tr>
    <tr>
        <td> ScopedPointer&lt;AudioSampleBuffer&gt; </td>
        <td> currentSampleBuffer <br>
        Currently or recently using audio sample buffer.
        </td>
    </tr>
    <tr>
        <td> ScopedPointer&lt;AudioSampleBuffer&gt; </td>
        <td> tempBuffer <br>
        Audio sample buffer when modifying pattern sample to draw modifying audio thumbnail.
        </td>
    </tr>
    <tr>
        <td> std::thread </td>
        <td> timeModThread <br>
        Object to initialize back-threading for modify().
        </td>
    </tr>
    <tr>
        <td> WsolaSamplerSound* </td>
        <td> wsola <br>
        Pointer of object for time-pitch modification or DSP.
        </td>
    </tr>
    <tr>
        <td> ScopedPointer&lt;PPM_Resampler&gt; </td>
        <td> wsola <br>
        Pointer of object for high quality resampling.
        </td>
    </tr>
</table>