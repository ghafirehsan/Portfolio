import React from "react";
import { motion } from "framer-motion";

export default function Portfolio() {
  return (
    <div className="min-h-screen bg-gradient-to-b from-gray-950 to-black text-white font-sans">
      {/* Header */}
      <header className="p-6 border-b border-gray-800 flex justify-between items-center">
        <h1 className="text-2xl font-bold">Ghafir Ehsan</h1>
        <a href="mailto:ghafirehsan97@gmail.com" className="bg-white text-black px-4 py-2 rounded-lg font-semibold">Hire Me</a>
      </header>

      {/* Hero */}
      <motion.section
        initial={{ opacity: 0, y: 40 }}
        animate={{ opacity: 1, y: 0 }}
        transition={{ duration: 0.6 }}
        className="p-16 text-center max-w-5xl mx-auto"
      >
        <h2 className="text-5xl font-extrabold leading-tight mb-6">
          I Turn Content Into Traffic, Rankings, and Growth
        </h2>
        <p className="text-gray-400 text-lg max-w-2xl mx-auto">
          SEO content built on strategy, backed by data, and designed to perform.
        </p>
      </motion.section>

      {/* About */}
      <motion.section
        initial={{ opacity: 0 }}
        whileInView={{ opacity: 1 }}
        transition={{ duration: 0.6 }}
        className="p-10 max-w-4xl mx-auto"
      >
        <h2 className="text-3xl font-semibold mb-4">About Me</h2>
        <p className="text-gray-300 leading-relaxed">
          I don’t write content just to fill pages. I create content that ranks, attracts traffic, and converts readers into results. If content doesn’t perform, it’s useless.
        </p>
      </motion.section>

      {/* Services */}
      <section className="p-10 bg-gray-900">
        <div className="max-w-5xl mx-auto">
          <h2 className="text-3xl font-semibold mb-6">Services</h2>
          <div className="grid md:grid-cols-3 gap-6">
            {["Blog Writing","SEO Strategy","Keyword Research","Content Audits","Website Content","On-Page SEO"].map((s,i)=>(
              <motion.div
                key={i}
                whileHover={{ scale: 1.05 }}
                className="p-5 bg-gray-800 rounded-2xl shadow-lg"
              >
                {s}
              </motion.div>
            ))}
          </div>
        </div>
      </section>

      {/* Portfolio */}
      <section className="p-10 max-w-5xl mx-auto">
        <h2 className="text-3xl font-semibold mb-6">Portfolio</h2>
        <div className="grid md:grid-cols-2 gap-6">
          {[
            {title:"Prince Ea",link:"https://princeea.com/scientists-develop-tiny-nanobots-that-could-clear-cholesterol-blockages-without-surgery/",desc:"High-authority SEO article"},
            {title:"Birds Advice",link:"https://www.birdsadvice.com/scientists-say-the-songs-you-loved-as-a-teenager-may-stay-with-you-forever/",desc:"Psychology-driven engagement content"},
            {title:"Spirit Science",link:"https://spiritsciencecentral.com/people-are-sharing-videos-of-their-cats-attacking-lugers-at-the-olympics-and-its-pure-gold/",desc:"Viral and shareable content"},
            {title:"Ask Dr Nandi",link:"https://askdrnandi.com/blog/",desc:"Health SEO blog writing"}
          ].map((item,i)=>(
            <motion.a
              key={i}
              href={item.link}
              target="_blank"
              whileHover={{ scale: 1.03 }}
              className="p-6 bg-gray-900 rounded-2xl hover:bg-gray-800 transition"
            >
              <h3 className="text-xl font-bold">{item.title}</h3>
              <p className="text-gray-400 mt-2">{item.desc}</p>
            </motion.a>
          ))}
        </div>
      </section>

      {/* Stats */}
      <section className="p-12 bg-gray-900 text-center">
        <h2 className="text-3xl font-semibold mb-6">SEO Results</h2>
        <p className="text-gray-400 mb-6">Real performance snapshot from content-driven SEO work</p>

        {/* IMPORTANT: Place your image in public folder as stats.png */}
        <motion.img
          src={require("../assets/stats.png")}
          alt="SEO Stats"
          initial={{ opacity: 0, scale: 0.9 }}
          whileInView={{ opacity: 1, scale: 1 }}
          transition={{ duration: 0.6 }}
          className="mx-auto rounded-xl shadow-2xl border border-gray-700"
        />
      </section>

      {/* Why Me */}
      <section className="p-12 max-w-4xl mx-auto text-center">
        <h2 className="text-3xl font-semibold mb-4">Why Choose Me</h2>
        <p className="text-gray-400">
          Most writers focus on words. I focus on results. Every piece of content is built to rank, attract traffic, and contribute to long-term growth.
        </p>
      </section>

      {/* CTA */}
      <section className="p-16 text-center">
        <h2 className="text-4xl font-bold mb-4">Let’s Build Something That Ranks</h2>
        <p className="text-gray-400 mb-6">Your content should work for you. Let’s make it happen.</p>
        <a href="mailto:ghafirehsan97@gmail.com" className="bg-white text-black px-8 py-3 rounded-xl font-semibold">Contact Me</a>
      </section>

      {/* Footer */}
      <footer className="p-6 text-center text-gray-500 border-t border-gray-800">
        © {new Date().getFullYear()} Ghafir Ehsan
      </footer>
    </div>
  );
}
