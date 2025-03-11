import React from "react";
import { motion } from "framer-motion";

const ChocolateGift = () => {
  return (
    <div className="min-h-screen bg-black text-white flex items-center justify-center p-4 relative overflow-hidden">
      <div className="text-center space-y-6 relative z-10">
        <h1 className="text-4xl font-bold">Bu sizga konkrus sovg'asi!</h1>
        <p className="text-xl">Shokolad sizga 12.03.2025 kuni beriladi.</p>
        <div className="relative inline-block">
          <img 
            src="https://upload.wikimedia.org/wikipedia/commons/7/70/Chocolate_%28blue_background%29.jpg" 
            alt="Shokolad"
            className="w-64 h-auto rounded-lg shadow-lg"
          />
        </div>
        <a
          href="/gift"
          className="mt-4 inline-block bg-blue-500 text-white px-6 py-2 rounded-lg shadow-lg hover:bg-blue-600 transition"
        >
          Loyihani ochish
        </a>
      </div>
      {/* Galaktika foni */}
      <motion.div
        className="absolute top-0 left-0 w-full h-full bg-cover bg-center"
        style={{ backgroundImage: "url('https://images.unsplash.com/photo-1447433819943-74a20887a81e')" }}
        animate={{ scale: [1, 1.1, 1] }}
        transition={{ duration: 15, repeat: Infinity, ease: "linear" }}
      ></motion.div>
      
      {/* Yulduzlarning porlashi */}
      <motion.div
        className="absolute inset-0 z-0"
        initial={{ opacity: 0 }}
        animate={{ opacity: [0.2, 0.5, 0.2] }}
        transition={{ duration: 6, repeat: Infinity, ease: "easeInOut" }}
      >
        <div className="absolute w-full h-full bg-black opacity-30"></div>
      </motion.div>
    </div>
  );
};

export default ChocolateGift;
