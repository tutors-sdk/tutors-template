# Panel Note

The current track-mongo-model is partially complete:

~~~javascript
import { Track } from "./track.js";

export const trackMongoStore = {
  async getTracksByPlaylistId(id) {
    const tracks = await Track.find({ playlistid: id }).lean();
    return tracks;
  },
};
~~~

Complete this now, but do so in conjunction with a set of Track model tests. You can base these tests on the existing playlist tests.
