import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { Truck, Phone, MapPin } from "lucide-react";
import { motion } from "framer-motion";

export default function AggregateDepotWebsite() {
  return (
    <div className="min-h-screen bg-gray-50 text-gray-800">
      {/* Hero Section */}
      <section className="bg-gradient-to-r from-gray-900 to-gray-700 text-white py-16 px-6">
        <motion.div initial={{ opacity: 0, y: 20 }} animate={{ opacity: 1, y: 0 }}>
          <h1 className="text-4xl font-bold mb-4">Abhishek Basumatary Enterprise</h1>
          <p className="text-lg mb-6">Aggregate, Sand, GSB & River Stone Sale Depot</p>
          <Button className="rounded-2xl shadow-lg">Get a Quote</Button>
        </motion.div>
      </section>

      {/* Products Section */}
      <section className="py-12 px-6 grid md:grid-cols-2 lg:grid-cols-4 gap-6">
        {["Aggregates", "Sand", "GSB (Granular Sub Base)", "River Stone"].map((item) => (
          <Card key={item} className="rounded-2xl shadow-md">
            <CardContent className="p-6">
              <h3 className="text-xl font-semibold mb-2">{item}</h3>
              <p className="text-sm">High quality materials suitable for construction and road works.</p>
            </CardContent>
          </Card>
        ))}
      </section>

      {/* Services Section */}
      <section className="bg-white py-12 px-6">
        <h2 className="text-2xl font-bold mb-6">Our Services</h2>
        <ul className="space-y-3">
          <li className="flex items-center gap-2"><Truck size={18}/> Bulk supply & dumper delivery</li>
          <li className="flex items-center gap-2"><Truck size={18}/> On-site delivery</li>
          <li className="flex items-center gap-2"><Truck size={18}/> Government & private projects</li>
        </ul>
      </section>

      {/* Contact Section */}
      <section className="bg-gray-100 py-12 px-6">
        <h2 className="text-2xl font-bold mb-4">Contact Us</h2>
        <p className="flex items-center gap-2"><Phone size={18}/> +91 XXXXX XXXXX</p>
        <p className="flex items-center gap-2"><MapPin size={18}/> Kokrajhar, Assam</p>
      </section>

      {/* Footer */}
      <footer className="bg-gray-900 text-white text-center py-4">
        © {new Date().getFullYear()} Abhishek Basumatary Enterprise. All rights reserved.
      </footer>
    </div>
  );
}
