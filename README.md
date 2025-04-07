Cósmos Híbrido 
O que é a Realidade no Cosmos Híbrido?
No contexto do Mapa das 9 Dimensões da Consciência – Cosmos Híbrido, a realidade é um constructo multidimensional que evolui com a consciência do usuário. Ela é:

Fluida e Relativa: A realidade muda dependendo da dimensão (ex.: potencial puro no 1D, caos criativo no 8D).
Sincrônica e Simbólica: O I Ching revela a realidade atual do usuário e oferece orientação para moldá-la, conectando eventos de forma significativa.
Interativa e Imersiva: A cena 3D permite que o usuário experimente, visualize e ajuste a realidade, tornando-a tangível e moldável.
Co-Criada: A realidade é um processo colaborativo entre o usuário, a dimensão, o I Ching, e a cena 3D, onde a intenção e a ação do usuário têm um papel ativo.
Em resumo, a realidade no "Cosmos Híbrido" é um estado de ser que reflete o nível de consciência do usuário, podendo ser percebida, interpretada e transformada através das ferramentas do Mapa (dimensões, I Ching, cena 3D). É uma realidade que transcende o material e se torna um espaço de criação consciente e conexão universal

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
