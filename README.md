# Meu-portifolio
✨ Portfólio criado com React, Tailwind e Framer Motion, unindo tecnologia e estética soft. 🌸 Visual clean, tons pastéis e animações suaves refletem minha personalidade criativa e organizada. 💻 Apresenta meus projetos com carinho, clareza e um toque único de vibes aesthetic.
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { Github, Mail, Linkedin } from "lucide-react";
import { motion } from "framer-motion";

export default function Portfolio() {
  return (
    <main className="min-h-screen bg-gradient-to-b from-pink-100 via-white to-blue-100 text-gray-800 p-6 font-sans">
      <section className="max-w-4xl mx-auto text-center space-y-4">
        <motion.h1
          initial={{ opacity: 0, y: -20 }}
          animate={{ opacity: 1, y: 0 }}
          transition={{ duration: 0.6 }}
          className="text-4xl md:text-5xl font-bold text-pink-600"
        >
          Olá, eu sou a Luna ✨
        </motion.h1>
        <p className="text-lg md:text-xl text-gray-600">
          Estudante apaixonada por design, tecnologia e vibes aesthetic 🌸
        </p>
        <div className="flex justify-center gap-4 mt-4">
          <Button variant="outline" className="gap-2">
            <Github size={18} /> GitHub
          </Button>
          <Button variant="outline" className="gap-2">
            <Linkedin size={18} /> LinkedIn
          </Button>
          <Button variant="outline" className="gap-2">
            <Mail size={18} /> E-mail
          </Button>
        </div>
      </section>

      <section className="mt-10 grid grid-cols-1 md:grid-cols-2 gap-6">
        <motion.div
          whileHover={{ scale: 1.02 }}
          className="transition-transform"
        >
          <Card className="bg-white/70 shadow-xl rounded-2xl p-4">
            <CardContent>
              <h2 className="text-2xl font-semibold mb-2 text-pink-500">
                ✨ Projeto 1
              </h2>
              <p className="text-gray-700">
                Um site para mostrar minha arte digital com interface clean e suave.
              </p>
            </CardContent>
          </Card>
        </motion.div>

        <motion.div
          whileHover={{ scale: 1.02 }}
          className="transition-transform"
        >
          <Card className="bg-white/70 shadow-xl rounded-2xl p-4">
            <CardContent>
              <h2 className="text-2xl font-semibold mb-2 text-blue-500">
                🌿 Projeto 2
              </h2>
              <p className="text-gray-700">
                App de rotina para autocuidado com tons pastéis e animações suaves.
              </p>
            </CardContent>
          </Card>
        </motion.div>
      </section>

      <footer className="text-center mt-16 text-sm text-gray-500">
        Feito com amor por mim 💖 — 2025
      </footer>
    </main>
  );
}
