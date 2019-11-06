---
title: 'Public Member Functions'

layout: nil
---

### Public Member Functions 

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
    }
    table tr td:nth-child(2) {
        width: 80%;
        vertical-align: top;
    }
</style>

<table>
	<tr>
		<td>void</td>
		<td>
			init()<br>
			Initialize or reset sounds of ppmSynth
		</td>

	</tr>
	<tr>
		<td>void</td>
		<td>
			loadInstruments(StringRef instName, bool isPattern) {<br>
			Load specific instruments
		</td>

	</tr>
	<tr>
		<td>void</td>
		<td>
			modify()<br>
			Modify current pattern based on initSegmentPos, segmentPos and pitches
		</td>

	</tr>
	<tr>
		<td>void</td>
		<td>
			threadModify()<br>
			Wrapper for function modify() running in back-thread
		</td>

	</tr>
	<tr>
		<td>StringArray</td>
		<td>
			getSampleFileNames()<br>
			Return currently selected sample file names
		</td>

	</tr>
	<tr>
		<td>XmlElement*</td>
		<td>
			getMetaData()<br>
			Return metadata of current pattern
		</td>

	</tr>
	<tr>
		<td>int*</td>
		<td>
			getSelectedFiles()<br>
			Return selected pattern files in GUI
		</td>

	</tr>
	<tr>
		<td>int</td>
		<td>
			getCurrentNote()<br>
			Return currently or recently played note
		</td>

	</tr>
	<tr>
		<td>int</td>
		<td>
			getPatternSelectionNote()<br>
			Return currently selected pattern selection note
		</td>

	</tr>
	<tr>
		<td>double</td>
		<td>
			getLength()<br>
			Return length of current sample in seconds
		</td>

	</tr>
	<tr>
		<td>double</td>
		<td>
			getHostSampleRate()<br>
			Return host sampling rate
		</td>

	</tr>
	<tr>
		<td>AudioSampleBuffer</td>
		<td>
			getCurrentSampleBuffer()<br>
			Return currently loaded sample buffer
		</td>

	</tr>
	<tr>
		<td>AudioSampleBuffer</td>
		<td>
			getTempBuffer()<br>
			Return temporary buffer for audio thumbnail when modifying sample
		</td>

	</tr>
	<tr>
		<td>double</td>
		<td>
			getCurrentPosition()<br>
			Return currently playing sample position ratio relative to entire sample
		</td>

	</tr>
	<tr>
		<td>File</td>
		<td>
			getCurrentPattern()<br>
			Return currently loaded pattern file (or file name)
		</td>

	</tr>
	<tr>
		<td>bool</td>
		<td>
			getPlayingState()<br>
			Return current playing state
		</td>

	</tr>
	<tr>
		<td>bool</td>
		<td>
			getBufferChangeState()<br>
			Return buffer change state whether pointer of current buffer is changed or not
		</td>

	</tr>
	<tr>
		<td>bool</td>
		<td>
			getModifyingState()<br>
			Return whether sample is modifying or not
		</td>

	</tr>
	<tr>
		<td>bool</td>
		<td>
			getDeleteState()<br>
			Return whether segment is deleting
		</td>

	</tr>
	<tr>
		<td>int</td>
		<td>
			getDeleteIndex()<br>
			Return index of currently deleting segment
		</td>

	</tr>
	<tr>
		<td>Array<double></td>
		<td>
			getPitches()<br>
			Return pitch values of segments
		</td>

	</tr>
	<tr>
		<td>Array<double></td>
		<td>
			getInitSegmentPos()<br>
			Return relative segment positions before the sample is modified
		</td>

	</tr>
	<tr>
		<td>Array<double></td>
		<td>
			getSegmentPos()<br>
			segmentPos is equal to initSegmentPos before the sample is modified
		</td>

	</tr>
	<tr>
		<td>Array<int></td>
		<td>
			getSliceIndices()<br>
			Return the array of slice indices among segments
		</td>

	</tr>
	<tr>
		<td>Array<double></td>
		<td>
			getSlicePos()<br>
			slicePos is similar to segmentPos and it is optained based on sliceIndices
		</td>

	</tr>
	<tr>
		<td>ScopedPointer<AudioSampleBuffer></td>
		<td>
			getSamples(ScopedPointer<AudioSampleBuffer> sourceBuffer, double startPos, double destPos)<br>
			Returns specific audioSampleBuffer from startPos to destPos proportion of entire number of samples.
		</td>

	</tr>
	<tr>
		<td>void</td>
		<td>
			setPitches(Array<double> getPitches)<br>
			Set class variable pitches, pitches of segments
		</td>

	</tr>
	<tr>
		<td>void</td>
		<td>
			setInitSegmentPos(Array<double> getInitSegmentPos)<br>
			Set class variable initSegmentPos, initial segment position array when sample is loaded
		</td>

	</tr>
	<tr>
		<td>void</td>
		<td>
			setSegmentPos(Array<double> getSegmentPos)<br>
			Set class variable segmentPos, current segment position array
		</td>

	</tr>
	<tr>
		<td>void</td>
		<td>
			setPrevSegmentPos()<br>
			Set class variable prevSegmentPos, previous, before any changes, segment position array
		</td>

	</tr>
	<tr>
		<td>void</td>
		<td>
			setSlicePos(Array<double> getSlicePos)<br>
			Set class variable slicePos, position array of slices
		</td>

	</tr>
	<tr>
		<td>void</td>
		<td>
			setSliceIndices(Array<int> getSliceIndices)<br>
			Set class variable sliceIndices, indices of segments that are slice
		</td>

	</tr>
	<tr>
		<td>void</td>
		<td>
			insertSliceIndex(int getIndex)<br>
			Insert new slice and its index to sliceIndices
		</td>

	</tr>
	<tr>
		<td>void</td>
		<td>
			deleteSliceIndex(int getIndex)<br>
			Delete a slice and its index in sliceIndices
		</td>

	</tr>
	<tr>
		<td>void</td>
		<td>
			setThumbnail(DrawAudioThumbnail* thumbnail)<br>
			DrawAudioThumbnail class uses _thumbnail to draw audio thumbnail
		</td>

	</tr>
	<tr>
		<td>void</td>
		<td>
			setPosInfo(DrawPosInfo* posInfo)<br>
			DrawPosInfo class uses _posInfo to draw beat information
		</td>

	</tr>
	<tr>
		<td>void</td>
		<td>
			setCurrentNote(int getCurrentNote)<br>
			Set class variable currentNote, currently playing note
		</td>

	</tr>
	<tr>
		<td>void</td>
		<td>
			setReader(File file)<br>
			This function is used for initializing pattern sample for audioSampleBuffer
		</td>

	</tr>
	<tr>
		<td>void</td>
		<td>
			setBPM(double getHostBPM)<br>
			Set class variable hostBPM
		</td>

	</tr>
	<tr>
		<td>void</td>
		<td>
			setUsingSingleNote()<br>
			Load single note using PPM_SamplerSound
		</td>

	</tr>
	<tr>
		<td>void</td>
		<td>
			setUsingPattern()<br>
			Load pattern sample to wsola and set wsola parameters
		</td>

	</tr>
	<tr>
		<td>void</td>
		<td>
			setUsingModified(ScopedPointer<AudioSampleBuffer> getData) {<br>
			Load modified pattern sample to wsola and set wsola parameters
		</td>

	</tr>
	<tr>
		<td>void</td>
		<td>
			setModeState(int midiNoteNumber)<br>
			Switch between single note and pattern
		</td>

	</tr>
	<tr>
		<td>void</td>
		<td>
			loadAudioFile(String filePath)<br>
			Load file to currentSampleBuffer and wsola from given filePath
		</td>

	</tr>
	<tr>
		<td>void</td>
		<td>
			readSegmentInfo(File xmlFile, bool loadFile)<br>
			Read segment/slice information from given XML file path
		</td>

	</tr>
	<tr>
		<td>void</td>
		<td>
			setPatternSelectionNote(int getPatternSelectionNote)<br>
			Set class variable, patternSelectionNote, from midi keyboard
		</td>

	</tr>
	<tr>
		<td>void</td>
		<td>
			setHostSampleRate(double sampleRate)<br>
			Set class variable, hostSampleRate, from host sample rate
		</td>

	</tr>
	<tr>
		<td>void</td>
		<td>
			setStartPosition(double startPosition)<br>
			Set start position of current buffer
		</td>

	</tr>
	<tr>
		<td>void</td>
		<td>
			setCurrentPosition(double currentPosition)<br>
			Set current playing position of current buffer
		</td>

	</tr>
	<tr>
		<td>void</td>
		<td>
			setEndPosition(double endPosition)<br>
			Set stop position of current buffer
		</td>

	</tr>
	<tr>
		<td>void</td>
		<td>
			setPlayingState(bool getPlayingState)<br>
			Set audio playing state
		</td>

	</tr>
	<tr>
		<td>void</td>
		<td>
			setBufferChangeState(bool getBufferChangeState)<br>
			Set recent state whether audio buffer is changed
		</td>

	</tr>
	<tr>
		<td>void</td>
		<td>
			setModifyingState(bool getModifyingState)<br>
			Set recent state whether user is modifying the pattern
		</td>

	</tr>
	<tr>
		<td>void</td>
		<td>
			setDeleteState(bool getDeleteState)<br>
			Set recent state whether user is deleting a segment
		</td>

	</tr>
	<tr>
		<td>void</td>
		<td>
			setDeleteIndex(int getDeleteIndex)<br>
			Set recently deleted segment index
		</td>

	</tr>
	<tr>
		<td>void</td>
		<td>
			setTempBuffer(int segmentIndex)<br>
			Set temporary audioSampleBuffer to tempBuffer
		</td>

	</tr>
	<tr>
		<td>void</td>
		<td>
			setTempSegmentPos()<br>
			Set temporary segment position when segment is draged on GUI
		</td>

	</tr>
	<tr>
		<td>void</td>
		<td>
			transportPlay()<br>
			start transport and playing sound
		</td>

	</tr>
	<tr>
		<td>void</td>
		<td>
			transportStop()<br>
			stop transport and playing sound
		</td>

	</tr>
	<tr>
		<td>double</td>
		<td>
			midi2hz(double getDeltaMIDI)<br>
			Simple midi difference to hertz scale difference conversion function
		</td>

	</tr>
	<tr>
		<td>Array<File>*</td>
		<td>
			getPatterns()<br>
			Get patterns selected on the GUI
		</td>

	</tr>
</table>
