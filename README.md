import React from 'react';
import { motion } from 'framer-motion';
import { Link } from 'react-router-dom';
import { ArrowRight } from 'lucide-react';

const ABOUT_IMAGE = 'https://media.base44.com/images/public/69f13723c78729b543cb7618/edfcb0fa0_generated_5aeafd74.png';

export default function About() {
  return (
    <div>
      {/* Hero */}
      <section className="relative h-[60vh] lg:h-[70vh] overflow-hidden">
        <img
          src={ABOUT_IMAGE}
          alt="Industrial studio environment with dramatic moody lighting"
          className="w-full h-full object-cover"
        />
        <div className="absolute inset-0 bg-black/50" />
        <div className="absolute inset-0 flex items-center justify-center">
          <motion.div
            initial={{ opacity: 0, y: 20 }}
            animate={{ opacity: 1, y: 0 }}
            transition={{ duration: 0.7 }}
            className="text-center"
          >
            <h1 className="text-4xl md:text-5xl font-bold text-white tracking-tight">Our Story</h1>
          </motion.div>
        </div>
      </section>

      {/* Content */}
      <section className="py-20 lg:py-28">
        <div className="max-w-3xl mx-auto px-6 lg:px-8">
          <motion.div
            initial={{ opacity: 0, y: 20 }}
            whileInView={{ opacity: 1, y: 0 }}
            viewport={{ once: true }}
            transition={{ duration: 0.6 }}
            className="space-y-8"
          >
            <div>
              <p className="text-[11px] font-semibold tracking-[0.3em] uppercase text-muted-foreground mb-4">The Mission</p>
              <h2 className="text-2xl md:text-3xl font-bold tracking-tight mb-6">
                One product. Perfected.
              </h2>
              <p className="text-muted-foreground leading-relaxed">
                Vanguard was born from a simple frustration — finding a shirt that actually fits, feels premium, and transitions seamlessly from the gym to everyday life. We stopped looking and started making.
              </p>
            </div>

            <div>
              <p className="text-[11px] font-semibold tracking-[0.3em] uppercase text-muted-foreground mb-4">The Craft</p>
              <p className="text-muted-foreground leading-relaxed">
                Every Vanguard shirt starts with 200gsm premium cotton — thick enough to drape properly, light enough to train in. We obsess over the details: reinforced seams, pre-shrunk fabric, and a cut that flatters without restricting. No logos screaming for attention. Just clean, intentional design.
              </p>
            </div>

            <div>
              <p className="text-[11px] font-semibold tracking-[0.3em] uppercase text-muted-foreground mb-4">The Standard</p>
              <p className="text-muted-foreground leading-relaxed">
                We don't do seasonal drops or trend-chasing. We do essentials — refined over time, available when you need them. Buy once, wear everywhere. That's the Vanguard standard.
              </p>
            </div>
          </motion.div>

          <motion.div
            initial={{ opacity: 0, y: 20 }}
            whileInView={{ opacity: 1, y: 0 }}
            viewport={{ once: true }}
            transition={{ duration: 0.6, delay: 0.2 }}
            className="mt-16 pt-10 border-t border-border"
          >
            <div className="grid grid-cols-3 gap-8 text-center">
              <div>
                <p className="text-3xl font-bold tracking-tight">200</p>
                <p className="text-xs text-muted-foreground tracking-wider uppercase mt-1">GSM Cotton</p>
              </div>
              <div>
                <p className="text-3xl font-bold tracking-tight">6</p>
                <p className="text-xs text-muted-foreground tracking-wider uppercase mt-1">Colorways</p>
              </div>
              <div>
                <p className="text-3xl font-bold tracking-tight">30</p>
                <p className="text-xs text-muted-foreground tracking-wider uppercase mt-1">Day Returns</p>
              </div>
            </div>
          </motion.div>

          <motion.div
            initial={{ opacity: 0, y: 20 }}
            whileInView={{ opacity: 1, y: 0 }}
            viewport={{ once: true }}
            transition={{ duration: 0.6 }}
            className="mt-16 text-center"
          >
            <Link
              to="/shop"
              className="inline-flex items-center gap-3 bg-foreground text-background px-8 py-4 text-[13px] font-semibold tracking-[0.15em] uppercase hover:opacity-90 transition-colors rounded-sm"
            >
              Shop the Collection
              <ArrowRight className="w-4 h-4" />
            </Link>
          </motion.div>
        </div>
      </section>
    </div>
  );
}
