import React from "react";

// Pieter King - Single-file React component (TailwindCSS classes assumed)
// Usage: drop into a CRA / Vite / Next.js / standalone React app and ensure Tailwind is configured.
// Replace placeholders (images, text, embed URIs) with your real assets.

export default function PieterKingSite() {
  const spotifyEmbed = "https://open.spotify.com/embed/artist/3Edr8uYXrdKWq3DQaTlKjp"; // your artist embed
  const youtubeEmbed = "https://www.youtube.com/embed/VIDEO_ID"; // replace VIDEO_ID with a YouTube video id

  return (
    <div className="min-h-screen bg-gray-50 text-gray-900 antialiased">
      <header className="bg-gradient-to-r from-indigo-700 via-purple-700 to-pink-600 text-white">
        <div className="max-w-5xl mx-auto px-6 py-10 flex items-center gap-6">
          <img src="/profile.jpg" alt="Pieter King" className="w-24 h-24 rounded-full object-cover ring-4 ring-white shadow-lg" />
          <div>
            <h1 className="text-3xl font-extrabold">Pieter King</h1>
            <p className="mt-1 text-sm opacity-90">Johannesburg-based singer-songwriter • Afrikaans & English pop</p>
            <div className="mt-3 flex items-center gap-3">
              <a href="https://open.spotify.com/artist/3Edr8uYXrdKWq3DQaTlKjp" target="_blank" rel="noopener noreferrer" className="px-3 py-1 rounded-md bg-white text-indigo-700 font-semibold shadow-sm text-sm">Listen on Spotify</a>
              <a href="#music" className="px-3 py-1 rounded-md border border-white/30 text-sm">Latest music</a>
            </div>
          </div>
        </div>
      </header>

      <main className="max-w-5xl mx-auto px-6 py-12">
        {/* About / Bio */}
        <section className="grid md:grid-cols-3 gap-8 items-start">
          <div className="md:col-span-2">
            <h2 className="text-2xl font-bold">About</h2>
            <p className="mt-3 text-gray-700 leading-relaxed">Hi — I’m Pieter King. I write and record songs in Afrikaans and English, blending intimate storytelling with modern pop production. My music is DIY-first: recorded at home, produced with collaborators across South Africa, and shared directly with listeners.
            </p>

            <div className="mt-6">
              <h3 className="font-semibold">Connect</h3>
              <div className="mt-3 flex gap-3 flex-wrap">
                <a href="https://instagram.com/yourhandle" target="_blank" rel="noopener noreferrer" className="text-sm underline">Instagram</a>
                <a href="https://youtube.com/yourchannel" target="_blank" rel="noopener noreferrer" className="text-sm underline">YouTube</a>
                <a href="https://facebook.com/yourpage" target="_blank" rel="noopener noreferrer" className="text-sm underline">Facebook</a>
                <a href="https://pieterking.bandcamp.com" target="_blank" rel="noopener noreferrer" className="text-sm underline">Bandcamp</a>
              </div>
            </div>
          </div>

          <aside className="bg-white rounded-2xl shadow p-5">
            <h4 className="font-semibold">Join the mailing list</h4>
            <p className="mt-2 text-sm text-gray-600">Get new songs & show announcements. No spam.</p>
            <form action="https://formspree.io/f/yourformid" method="POST" className="mt-4 flex flex-col gap-3">
              <input name="email" type="email" placeholder="Your email" required className="w-full px-3 py-2 rounded border" />
              <input name="name" type="text" placeholder="Your name (optional)" className="w-full px-3 py-2 rounded border" />
              <button type="submit" className="w-full py-2 rounded bg-indigo-600 text-white font-semibold">Subscribe</button>
            </form>
          </aside>
        </section>

        {/* Music section */}
        <section id="music" className="mt-12">
          <h2 className="text-2xl font-bold">Music</h2>
          <p className="mt-2 text-sm text-gray-600">Stream or save on your platform of choice. New singles every few weeks.</p>

          <div className="mt-6 grid md:grid-cols-2 gap-6">
            <div className="bg-white p-4 rounded-lg shadow">
              <h3 className="font-semibold">Spotify</h3>
              <div className="mt-3">
                <iframe title="Spotify" src={spotifyEmbed} width="100%" height="380" frameBorder="0" allowtransparency="true" allow="encrypted-media"></iframe>
              </div>
            </div>

            <div className="bg-white p-4 rounded-lg shadow">
              <h3 className="font-semibold">Featured video</h3>
              <div className="mt-3 aspect-video">
                <iframe className="w-full h-full rounded" src={youtubeEmbed} title="YouTube video player" frameBorder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowFullScreen></iframe>
              </div>
            </div>
          </div>

          <div className="mt-6 bg-white p-4 rounded-lg shadow">
            <h4 className="font-semibold">Latest releases</h4>
            <ul className="mt-3 space-y-2 text-sm text-gray-700">
              <li>
                <strong>Single Title — 2025</strong>
                <div className="text-xs text-gray-500">Acoustic / pop • 3:12</div>
              </li>
              <li>
                <strong>Another Song — 2024</strong>
                <div className="text-xs text-gray-500">Collab • 2:54</div>
              </li>
            </ul>
          </div>
        </section>

        {/* Shows & Merch */}
        <section className="mt-12 grid md:grid-cols-2 gap-6">
          <div className="bg-white p-4 rounded-lg shadow">
            <h3 className="font-semibold">Shows</h3>
            <p className="mt-2 text-sm text-gray-600">No shows currently - check back soon.</p>
            <ul className="mt-3 space-y-2 text-sm">
              <li className="flex justify-between items-center">
                <div>
                  <div className="font-medium">Jun 28, 2025 — The Jazz Cafe, Johannesburg</div>
                  <div className="text-xs text-gray-500">Tickets available on link</div>
                </div>
                <a href="#" className="text-indigo-600 underline text-sm">Buy</a>
              </li>
            </ul>
          </div>

          <div className="bg-white p-4 rounded-lg shadow">
            <h3 className="font-semibold">Merch / Store</h3>
            <p className="mt-2 text-sm text-gray-600">T-shirts, vinyl, and limited-run bundles available on Bandcamp / Shopify.</p>
            <div className="mt-4 grid grid-cols-2 gap-3">
              <a href="#" className="block rounded overflow-hidden border">
                <img src="/merch1.jpg" alt="Merch 1" className="w-full h-32 object-cover" />
                <div className="p-2 text-xs">T-shirt — R250</div>
              </a>
              <a href="#" className="block rounded overflow-hidden border">
                <img src="/merch2.jpg" alt="Merch 2" className="w-full h-32 object-cover" />
                <div className="p-2 text-xs">Vinyl — R350</div>
              </a>
            </div>
          </div>
        </section>

        {/* Contact */}
        <section className="mt-12 bg-white p-6 rounded-lg shadow">
          <h3 className="font-semibold">Contact</h3>
          <p className="mt-2 text-sm text-gray-600">For bookings and press: <a href="mailto:booking@pieterking.com" className="underline">booking@pieterking.com</a></p>
          <p className="mt-2 text-sm text-gray-600">Socials: <span className="italic">@yourhandle</span></p>
        </section>

        <footer className="mt-12 text-center text-sm text-gray-500 pb-12">
          © {new Date().getFullYear()} Pieter King — All rights reserved.
        </footer>
      </main>
    </div>
  );
}
