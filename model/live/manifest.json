/// <reference path="./online-streaming-provider.d.ts" />
 
class Provider {

    getSettings(): Settings {
        return {
            episodeServers: ["server1", "server2"],
            supportsDub: true,
        }
    }

    async search(query: SearchOptions): Promise<SearchResult[]> {
        return [{
            id: "1",
            title: "ONE PIECE FILM: RED",
            url: "https://ophim17.cc/phim/one-piece-film-red",
            subOrDub: "both",
        }]
    }
    async findEpisodes(id: string): Promise<EpisodeDetails[]> {
        return [{
            id: "1",
            number: 1,
            url: "https://vip.opstream14.com/share/a96683574013404fbdc72bcb5f4c80e7",
            title: "Vietsub",
        }]
    }
    async findEpisodeServer(episode: EpisodeDetails, _server: string): Promise<EpisodeServer> {
        let server = "server1"
        if (_server !== "default") server = _server
        
        return {
            server: server,
            headers: {},
            videoSources: [{
                url: "https://example.com/.../stream.m3u8",
                type: "m3u8",
                quality: "1080p",
                subtitles: [{
                    id: "1",
                    url: "https://example.com/.../subs.vtt",
                    language: "en",
                    isDefault: true,
                }],
            }],
        }
    }
}
