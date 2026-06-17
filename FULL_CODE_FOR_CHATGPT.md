# 📝 সম্পূর্ণ Home.tsx কোড - ChatGPT এর জন্য

এই কোডটি সম্পূর্ণভাবে কপি করুন এবং ChatGPT কে এই প্রম্পট দিয়ে দিন:

---

## 📌 ChatGPT প্রম্পট

```
আমার একটি গ্রাফিক্স ডিজাইন পোর্টফোলিও ওয়েবসাইট আছে। নিচের কোডে আমার তথ্য দিয়ে কাস্টমাইজ করে দাও:

1. নাম: মোঃ আল-আমিন (যেখানে "Al-Amin" আছে সেখানে আমার নাম দাও)
2. ইমেইল: আমার-ইমেইল@gmail.com (যেখানে "al-amin@example.com" আছে)
3. ফোন: +880 1761399365 (ইতিমধ্যে আছে, ঠিক রাখো)
4. লোকেশন: নরসিংদী বাংলাদেশ (ইতিমধ্যে আছে, ঠিক রাখো)
5. পোর্টফোলিও আইটেম: 
   - আইটেম ১: আমার লোগো ডিজাইন (বর্ণনা: আমার ডিজাইন করা লোগো এবং ব্র্যান্ডিং)
   - আইটেম ২: ব্র্যান্ডিং প্রজেক্ট (বর্ণনা: সম্পূর্ণ ব্র্যান্ড আইডেন্টিটি সিস্টেম)
   - আইটেম ৩: ওয়েব ডিজাইন (বর্ণনা: আধুনিক এবং প্রতিক্রিয়াশীল ওয়েব ডিজাইন)
   - আইটেম ৪: ডিজিটাল মার্কেটিং (বর্ণনা: সোশ্যাল মিডিয়া এবং মার্কেটিং ডিজাইন)
6. সেবা: লোগো ডিজাইন, ব্র্যান্ডিং, ওয়েব ডিজাইন, ডিজিটাল মার্কেটিং
7. সম্পর্কে: আমি একজন পেশাদার গ্রাফিক্স ডিজাইনার যার ৫ বছরের অভিজ্ঞতা আছে। আমি ব্র্যান্ড আইডেন্টিটি, ডিজিটাল ডিজাইন এবং ভিজ্যুয়াল সিস্টেম তৈরিতে বিশেষজ্ঞ।

কোডটি সম্পূর্ণভাবে কাস্টমাইজ করে দাও এবং শুধু আপডেট করা কোড দাও।
```

---

## 🔗 সম্পূর্ণ কোড (কপি করুন)

```typescript
import { Button } from "@/components/ui/button";
import { Mail, Phone, MapPin, ExternalLink, ArrowRight } from "lucide-react";
import { useState } from "react";

/**
 * Premium Graphics Design Portfolio
 * Design Philosophy: Sophisticated Premium
 * - Deep navy-black background with gold accents
 * - Elegant typography (Playfair Display + Poppins)
 * - Smooth animations and micro-interactions
 * - Masonry gallery layout for portfolio items
 */

export default function Home() {
  const [hoveredCard, setHoveredCard] = useState<number | null>(null);

  // Portfolio items
  const portfolioItems = [
    {
      id: 1,
      title: "Brand Identity Design",
      category: "Branding",
      image: "https://d2xsxph8kpxj0f.cloudfront.net/310519663768943686/UGB6ac5HCnWgVAJgER7E7v/sample-work-1-bKupwGLkAUretmNDg4gowr.webp",
      description: "Complete brand identity system including logo, color palette, and guidelines",
    },
    {
      id: 2,
      title: "Digital UI/UX Design",
      category: "Web Design",
      image: "https://d2xsxph8kpxj0f.cloudfront.net/310519663768943686/UGB6ac5HCnWgVAJgER7E7v/sample-work-2-miYPVxhQ2oh2DXH2R2bKz3.webp",
      description: "Modern interface design with focus on user experience and aesthetics",
    },
    {
      id: 3,
      title: "Marketing Collateral",
      category: "Print Design",
      image: "https://d2xsxph8kpxj0f.cloudfront.net/310519663768943686/UGB6ac5HCnWgVAJgER7E7v/sample-work-1-bKupwGLkAUretmNDg4gowr.webp",
      description: "Business cards, brochures, and promotional materials",
    },
    {
      id: 4,
      title: "Social Media Campaign",
      category: "Digital Marketing",
      image: "https://d2xsxph8kpxj0f.cloudfront.net/310519663768943686/UGB6ac5HCnWgVAJgER7E7v/sample-work-2-miYPVxhQ2oh2DXH2R2bKz3.webp",
      description: "Engaging social media graphics and campaign designs",
    },
  ];

  // Services
  const services = [
    {
      icon: "🎨",
      title: "Logo & Branding",
      description: "Create memorable brand identities that stand out",
    },
    {
      icon: "💻",
      title: "Web Design",
      description: "Modern, responsive web designs for digital presence",
    },
    {
      icon: "📱",
      title: "UI/UX Design",
      description: "User-centered interface and experience design",
    },
    {
      icon: "📊",
      title: "Marketing Design",
      description: "Eye-catching materials for your campaigns",
    },
  ];

  return (
    <div className="min-h-screen bg-background">
      {/* Navigation */}
      <nav className="sticky top-0 z-50 bg-white/95 backdrop-blur-md border-b border-border">
        <div className="container flex items-center justify-between h-16">
          <div className="flex items-center gap-2">
            <img
              src="https://d2xsxph8kpxj0f.cloudfront.net/310519663768943686/UGB6ac5HCnWgVAJgER7E7v/logo-XtJStq2X44buohK4YJznRb.webp"
              alt="Logo"
              className="w-8 h-8"
            />
            <span style={{ fontFamily: "'Playfair Display', serif" }} className="text-xl font-bold text-primary">Al-Amin</span>
          </div>
          <div className="hidden md:flex items-center gap-8">
            <a href="#portfolio" className="text-foreground hover:text-[#d4a574] transition-colors">
              Portfolio
            </a>
            <a href="#services" className="text-foreground hover:text-[#d4a574] transition-colors">
              Services
            </a>
            <a href="#about" className="text-foreground hover:text-[#d4a574] transition-colors">
              About
            </a>
            <a href="#contact" className="text-foreground hover:text-[#d4a574] transition-colors">
              Contact
            </a>
          </div>
          <Button className="bg-[#d4a574] text-primary hover:bg-[#d4a574]-dark">
            Get Started
          </Button>
        </div>
      </nav>

      {/* Hero Section */}
      <section
        className="relative min-h-screen flex items-center justify-center overflow-hidden"
        style={{
          backgroundImage: `url('https://d2xsxph8kpxj0f.cloudfront.net/310519663768943686/UGB6ac5HCnWgVAJgER7E7v/hero-bg-DyeGdc88kBzf4GzSqtFZpJ.webp')`,
          backgroundSize: "cover",
          backgroundPosition: "center",
        }}
      >
        <div className="absolute inset-0 bg-black/40"></div>
        <div className="container relative z-10 text-center text-white">
          <div className="mb-6 inline-block">
            <span style={{ fontFamily: "'Poppins', sans-serif" }} className="text-[#d4a574] text-sm font-semibold tracking-widest">
              WELCOME TO MY STUDIO
            </span>
          </div>
          <h1 style={{ fontFamily: "'Playfair Display', serif" }} className="text-5xl md:text-7xl font-bold mb-6 leading-tight">
            Creative Design Solutions
          </h1>
          <p style={{ fontFamily: "'Poppins', sans-serif" }} className="text-lg md:text-xl text-gray-200 mb-8 max-w-2xl mx-auto">
            Transforming ideas into stunning visual experiences. Specializing in branding, UI/UX, and digital design.
          </p>
          <div className="flex gap-4 justify-center">
            <Button
              size="lg"
              className="bg-[#d4a574] text-primary hover:bg-[#d4a574]-dark"
              style={{ fontFamily: "'Poppins', sans-serif" }}
            >
              View আমার কাজ
              <ArrowRight className="ml-2 w-5 h-5" />
            </Button>
            <Button
              size="lg"
              variant="outline"
              className="border-white text-white hover:bg-white/10"
              style={{ fontFamily: "'Poppins', sans-serif" }}
            >
              Get In Touch
            </Button>
          </div>
        </div>
      </section>

      {/* Portfolio Section */}
      <section id="portfolio" className="py-20 bg-white">
        <div className="container">
          <div className="text-center mb-16">
            <span style={{ fontFamily: "'Poppins', sans-serif" }} className="text-[#d4a574] text-sm font-semibold tracking-widest">
              SELECTED WORK
            </span>
            <h2 style={{ fontFamily: "'Playfair Display', serif" }} className="text-4xl md:text-5xl font-bold text-primary mt-4 mb-4">
              Portfolio Showcase
            </h2>
            <div className="w-16 h-1 bg-gradient-to-r from-transparent via-accent-gold to-transparent mx-auto"></div>
          </div>

          <div className="grid grid-cols-1 md:grid-cols-2 gap-8">
            {portfolioItems.map((item, index) => (
              <div
                key={item.id}
                className="group relative overflow-hidden rounded-lg shadow-lg hover:shadow-lg-hover transition-all duration-300 cursor-pointer"
                onMouseEnter={() => setHoveredCard(index)}
                onMouseLeave={() => setHoveredCard(null)}
              >
                <div className="relative h-80 overflow-hidden">
                  <img
                    src={item.image}
                    alt={item.title}
                    className="w-full h-full object-cover group-hover:scale-110 transition-transform duration-500"
                  />
                  <div className="absolute inset-0 bg-black/40 group-hover:bg-black/60 transition-all duration-300"></div>
                </div>

                <div className="absolute inset-0 flex flex-col justify-end p-6 text-white">
                  <span style={{ fontFamily: "'Poppins', sans-serif" }} className="text-[#d4a574] text-sm font-semibold mb-2">
                    {item.category}
                  </span>
                  <h3 style={{ fontFamily: "'Playfair Display', serif" }} className="text-2xl font-bold mb-2">{item.title}</h3>
                  <p style={{ fontFamily: "'Poppins', sans-serif" }} className="text-gray-200 text-sm opacity-0 group-hover:opacity-100 transition-opacity duration-300">
                    {item.description}
                  </p>
                </div>
              </div>
            ))}
          </div>

          <div className="text-center mt-12">
            <Button
              size="lg"
              className="bg-[#d4a574] text-primary hover:bg-[#d4a574]-dark"
              style={{ fontFamily: "'Poppins', sans-serif" }}
            >
              View All Projects
              <ArrowRight className="ml-2 w-5 h-5" />
            </Button>
          </div>
        </div>
      </section>

      {/* Services Section */}
      <section id="services" className="py-20 bg-primary text-white">
        <div className="container">
          <div className="text-center mb-16">
            <span style={{ fontFamily: "'Poppins', sans-serif" }} className="text-[#d4a574] text-sm font-semibold tracking-widest">
              WHAT I OFFER
            </span>
            <h2 style={{ fontFamily: "'Playfair Display', serif" }} className="text-4xl md:text-5xl font-bold mt-4 mb-4">
              My Services
            </h2>
            <div className="w-16 h-1 bg-gradient-to-r from-transparent via-accent-gold to-transparent mx-auto"></div>
          </div>

          <div className="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
            {services.map((service, index) => (
              <div
                key={index}
                className="group p-6 bg-white/10 backdrop-blur-sm rounded-lg border border-white/20 hover:border-[#d4a574]/50 hover:bg-white/20 transition-all duration-300"
              >
                <div className="text-4xl mb-4">{service.icon}</div>
                <h3 style={{ fontFamily: "'Playfair Display', serif" }} className="text-xl font-bold mb-3">{service.title}</h3>
                <p style={{ fontFamily: "'Poppins', sans-serif" }} className="text-gray-300 text-sm">{service.description}</p>
              </div>
            ))}
          </div>
        </div>
      </section>

      {/* About Section */}
      <section id="about" className="py-20 bg-white">
        <div className="container">
          <div className="grid grid-cols-1 md:grid-cols-2 gap-12 items-center">
            <div>
              <span style={{ fontFamily: "'Poppins', sans-serif" }} className="text-[#d4a574] text-sm font-semibold tracking-widest">
                ABOUT ME
              </span>
              <h2 style={{ fontFamily: "'Playfair Display', serif" }} className="text-4xl font-bold text-primary mt-4 mb-6">
                Professional Designer & Creative Thinker
              </h2>
              <p style={{ fontFamily: "'Poppins', sans-serif" }} className="text-foreground text-lg mb-4 leading-relaxed">
                With years of experience in graphic design, I help brands tell their stories through compelling visual design. My passion is creating designs that not only look beautiful but also drive results.
              </p>
              <p style={{ fontFamily: "'Poppins', sans-serif" }} className="text-foreground text-lg mb-8 leading-relaxed">
                I specialize in brand identity, digital design, and creating cohesive visual systems that elevate your brand presence.
              </p>
              <Button className="bg-[#d4a574] text-primary hover:bg-[#d4a574]-dark">
                Learn More
              </Button>
            </div>
            <div className="relative">
              <div className="aspect-square rounded-lg overflow-hidden shadow-lg">
                <img
                  src="https://d2xsxph8kpxj0f.cloudfront.net/310519663768943686/UGB6ac5HCnWgVAJgER7E7v/portfolio-bg-GYctz4dhEx2CZa3UFReB9.webp"
                  alt="About"
                  className="w-full h-full object-cover"
                />
              </div>
              <div className="absolute -bottom-4 -right-4 w-32 h-32 bg-[#d4a574]/20 rounded-full blur-3xl"></div>
            </div>
          </div>
        </div>
      </section>

      {/* Contact Section */}
      <section id="contact" className="py-20 bg-primary text-white">
        <div className="container">
          <div className="max-w-3xl mx-auto">
            <div className="text-center mb-12">
              <span style={{ fontFamily: "'Poppins', sans-serif" }} className="text-[#d4a574] text-sm font-semibold tracking-widest">
                GET IN TOUCH
              </span>
              <h2 style={{ fontFamily: "'Playfair Display', serif" }} className="text-4xl md:text-5xl font-bold mt-4 mb-4">
                Let's Work Together
              </h2>
              <p style={{ fontFamily: "'Poppins', sans-serif" }} className="text-gray-300 text-lg">
                Have a project in mind? I'd love to hear about it. Get in touch and let's create something amazing together.
              </p>
            </div>

            <div className="grid grid-cols-1 md:grid-cols-3 gap-8 mb-12">
              <div className="text-center">
                <div className="w-12 h-12 bg-[#d4a574]/20 rounded-full flex items-center justify-center mx-auto mb-4">
                  <Mail className="w-6 h-6 text-[#d4a574]" />
                </div>
                <h3 style={{ fontFamily: "'Playfair Display', serif" }} className="font-bold mb-2">Email</h3>
                <a href="mailto:al-amin@example.com" className="text-gray-300 hover:text-[#d4a574] transition-colors">
                  al-amin@example.com
                </a>
              </div>
              <div className="text-center">
                <div className="w-12 h-12 bg-[#d4a574]/20 rounded-full flex items-center justify-center mx-auto mb-4">
                  <Phone className="w-6 h-6 text-[#d4a574]" />
                </div>
                <h3 style={{ fontFamily: "'Playfair Display', serif" }} className="font-bold mb-2">Phone</h3>
                <a href="tel:+880123456789" className="text-gray-300 hover:text-[#d4a574] transition-colors">
                  +880 1761399365
                </a>
              </div>
              <div className="text-center">
                <div className="w-12 h-12 bg-[#d4a574]/20 rounded-full flex items-center justify-center mx-auto mb-4">
                  <MapPin className="w-6 h-6 text-[#d4a574]" />
                </div>
                <h3 style={{ fontFamily: "'Playfair Display', serif" }} className="font-bold mb-2">Location</h3>
                <p className="text-gray-300">নরসিংদী বাংলাদেশ</p>
              </div>
            </div>

            <form className="space-y-6 bg-white/10 backdrop-blur-sm p-8 rounded-lg border border-white/20">
              <div className="grid grid-cols-1 md:grid-cols-2 gap-6">
                <input
                  type="text"
                  placeholder="Your Name"
                  className="bg-white/10 border border-white/20 rounded-lg px-4 py-3 text-white placeholder-gray-400 focus:outline-none focus:border-[#d4a574] transition-colors"
                />
                <input
                  type="email"
                  placeholder="Your Email"
                  className="bg-white/10 border border-white/20 rounded-lg px-4 py-3 text-white placeholder-gray-400 focus:outline-none focus:border-[#d4a574] transition-colors"
                />
              </div>
              <input
                type="text"
                placeholder="Project Title"
                className="w-full bg-white/10 border border-white/20 rounded-lg px-4 py-3 text-white placeholder-gray-400 focus:outline-none focus:border-[#d4a574] transition-colors"
              />
              <textarea
                placeholder="Tell me about your project..."
                rows={5}
                className="w-full bg-white/10 border border-white/20 rounded-lg px-4 py-3 text-white placeholder-gray-400 focus:outline-none focus:border-[#d4a574] transition-colors resize-none"
              ></textarea>
              <Button className="w-full bg-[#d4a574] text-primary hover:bg-[#d4a574]-dark">
                Send Message
              </Button>
            </form>
          </div>
        </div>
      </section>

      {/* Footer */}
      <footer className="bg-black/50 text-gray-400 py-8 border-t border-white/10">
        <div className="container flex flex-col md:flex-row items-center justify-between">
          <div className="flex items-center gap-2 mb-4 md:mb-0">
            <img
              src="https://d2xsxph8kpxj0f.cloudfront.net/310519663768943686/UGB6ac5HCnWgVAJgER7E7v/logo-XtJStq2X44buohK4YJznRb.webp"
              alt="Logo"
              className="w-6 h-6"
            />
            <span style={{ fontFamily: "'Playfair Display', serif" }} className="font-bold text-white">Al-Amin Design Studio</span>
          </div>
          <div className="flex gap-6">
            <a href="#" className="hover:text-[#d4a574] transition-colors">
              Twitter
            </a>
            <a href="#" className="hover:text-[#d4a574] transition-colors">
              LinkedIn
            </a>
            <a href="#" className="hover:text-[#d4a574] transition-colors">
              Instagram
            </a>
            <a href="#" className="hover:text-[#d4a574] transition-colors">
              Dribbble
            </a>
          </div>
          <p className="text-sm mt-4 md:mt-0">
            © 2024 Al-Amin Graphics Design. All rights reserved.
          </p>
        </div>
      </footer>
    </div>
  );
}
```

---

## 🎯 ব্যবহারের ধাপ

1. **উপরের প্রম্পট কপি করুন** - "ChatGPT প্রম্পট" সেকশন থেকে
2. **ChatGPT খুলুন** - https://chat.openai.com
3. **প্রম্পট পেস্ট করুন** - ChatGPT এ
4. **কোড পেস্ট করুন** - উপরের সম্পূর্ণ কোড কপি করে প্রম্পটের পরে পেস্ট করুন
5. **এন্টার চাপুন** - ChatGPT কাস্টমাইজ করা কোড দেবে
6. **কাস্টমাইজড কোড কপি করুন** - ChatGPT থেকে
7. **আপনার ওয়েবসাইটে পেস্ট করুন** - Code প্যানেলে Home.tsx এ

---

## 💡 টিপস

- ChatGPT আপনার সব তথ্য দিয়ে কোড কাস্টমাইজ করবে
- আপনি চাইলে আরও বিস্তারিত নির্দেশনা দিতে পারেন
- ChatGPT এর কাছ থেকে পাওয়া কোড সরাসরি ব্যবহার করতে পারবেন

---

## ❓ সমস্যা হলে

- ChatGPT এর কাছে আরও বিস্তারিত বলুন
- বা আমাকে বলুন, আমি সাহায্য করব!
