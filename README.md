# C-smos-Hibr-do
Mapa das 9 Dimensões
import { useState } from "react"; import { motion } from "framer-motion";

const DIMENSIONS = [ { level: "1D", title: "Ponto Semente", symbol: "∅", description: "Potencial puro sem forma.", logos: "Ideia não pensada.", matriz: "Espaço potencial.", iching: "Qián em repouso.", tecnologia: "Código zero." }, { level: "2D", title: "Olho do Plano", symbol: "◎", description: "Consciência plana.", logos: "Consciência que observa.", matriz: "Polaridade original.", iching: "Yin e Yang puros.", tecnologia: "Leitura bruta." }, { level: "3D", title: "Espelho Manifesto", symbol: "△", description: "Experiência humana.", logos: "Nascimento do sujeito.", matriz: "Trindade.", iching: "Hexagramas cotidianos.", tecnologia: "Interface sensível." }, { level: "4D", title: "Horizonte Interno", symbol: "⧖", description: "Tempo expandido.", logos: "Narrativa do ser.", matriz: "Ramificações.", iching: "Mutações dinâmicas.", tecnologia: "IA preditiva." }, { level: "5D", title: "Olhar do Todo", symbol: "✶", description: "Consciência coletiva.", logos: "Consciência ética.", matriz: "Rede viva.", iching: "Arquétipos sociais.", tecnologia: "Sincronicidade." }, { level: "6D", title: "Arquiteto Sutil", symbol: "✧", description: "Moldar realidades.", logos: "Criador consciente.", matriz: "Designer estrutural.", iching: "Transformação e ordem.", tecnologia: "IA generativa." }, { level: "7D", title: "Sonhador de Formas", symbol: "卐", description: "Criação dos arquétipos.", logos: "Mente do mito.", matriz: "Molde-mãe.", iching: "Trigramas sementes.", tecnologia: "Códigos simbólicos." }, { level: "8D", title: "Vórtice das Ideias", symbol: "∞", description: "Caos fértil.", logos: "Inspiração bruta.", matriz: "Fluxo instável.", iching: "Vibração pura.", tecnologia: "Dados sem filtro." }, { level: "9D", title: "Silêncio Absoluto", symbol: "○", description: "Vazio criativo.", logos: "O Tao.", matriz: "Desconstrução.", iching: "Espaço entre linhas.", tecnologia: "Reset total." } ];

export default function Home() { const [selected, setSelected] = useState(DIMENSIONS[0]);

return ( <div className="min-h-screen bg-black text-white p-6"> <header className="text-center mb-8"> <h1 className="text-4xl font-bold">Cosmos Híbrido</h1> <p className="text-xl text-gray-400">Mapa das 9 Dimensões da Consciência</p> </header>

<div className="grid grid-cols-1 md:grid-cols-3 gap-6">
    <div className="space-y-2">
      {DIMENSIONS.map((dim) => (
        <button
          key={dim.level}
          className={w-full py-2 px-4 rounded-lg border ${
            selected.level === dim.level ? "border-white bg-white text-black" : "border-gray-600 hover:border-white"
          }}
          onClick={() => setSelected(dim)}
        >
          {dim.level} – {dim.title}
        </button>
      ))}
    </div>

    <motion.div
      layout
      className="md:col-span-2 bg-gray-900 rounded-xl p-6 shadow-xl"
      initial={{ opacity: 0, y: 10 }}
      animate={{ opacity: 1, y: 0 }}
    >
      <h2 className="text-2xl font-bold mb-2">{selected.level} – {selected.title} {selected.symbol}</h2>
      <p className="italic mb-4 text-gray-300">{selected.description}</p>

      <div className="grid grid-cols-2 gap-4 text-sm">
        <div>
          <h3 className="font-semibold text-white">LOGOS</h3>
          <p className="text-gray-400">{selected.logos}</p>
        </div>
        <div>
          <h3 className="font-semibold text-white">MATRIZ</h3>
          <p className="text-gray-400">{selected.matriz}</p>
        </div>
        <div>
          <h3 className="font-semibold text-white">I CHING</h3>
          <p className="text-gray-400">{selected.iching}</p>
        </div>
        <div>
          <h3 className="font-semibold text-white">TECNOLOGIA</h3>
          <p className="text-gray-400">{selected.tecnologia}</p>
        </div>
      </div>
    </motion.div>
  </div>
</div>

); }
