# -e--learning-management
import React from "react";
import { Button } from "@/components/ui/button";
import { Card, CardContent } from "@/components/ui/card";
import { motion } from "framer-motion";

export default function Home() {
  return (
    <div className="min-h-screen bg-gray-100 flex flex-col items-center p-6">
      <motion.h1
        className="text-4xl font-bold text-gray-900 mb-6"
        initial={{ opacity: 0, y: -20 }}
        animate={{ opacity: 1, y: 0 }}
      >
        Welcome to E-Learning Platform
      </motion.h1>
      <p className="text-lg text-gray-600 mb-6">
        Learn anytime, anywhere with our curated courses.
      </p>
      <Button className="bg-blue-600 text-white px-4 py-2 rounded-lg hover:bg-blue-700">
        Explore Courses
      </Button>
      <div className="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6 mt-10">
        {[1, 2, 3].map((course) => (
          <Card key={course} className="w-80 p-4">
            <CardContent>
              <h2 className="text-xl font-semibold">Course {course}</h2>
              <p className="text-gray-600">Introduction to Next.js & Tailwind CSS</p>
              <Button className="mt-4 bg-green-600 text-white px-4 py-2 rounded-lg hover:bg-green-700">
                Enroll Now
              </Button>
            </CardContent>
          </Card>
        ))}
      </div>
      <div className="mt-10">
        <h2 className="text-2xl font-bold text-gray-900">Role-Based Access</h2>
        <p className="text-lg text-gray-600">Students and instructors have different access levels.</p>
      </div>
    </div>
  );
}
