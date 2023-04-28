<template>
      <!-- Sidebar -->
      <div class="flex-none w-64 bg-slate-300 shadow">
        <div class="flex items-center justify-center h-16 bg-slate-600 text-white font-semibold text-2xl">
          <span>Admin Panel</span>
        </div>
        <nav class="mt-8">
          <a href="#" class="flex items-center py-2 px-4 bg-indigo-100 text-indigo-700 bg-opacity-25 font-medium">
            <i class="fas fa-box mr-3"></i>
            <span>Products</span>
          </a>
          <a href="#" class="flex items-center py-2 px-4 hover:bg-indigo-100 hover:text-indigo-700 font-medium">
            <i class="fas fa-users mr-3"></i>
            <span>Users</span>
          </a>
          <a href="#" class="flex items-center py-2 px-4 hover:bg-indigo-100 hover:text-indigo-700 font-medium">
            <i class="fas fa-shopping-cart mr-3"></i>
            <span>Orders</span>
          </a>
        </nav>
      </div>
  </template>
  
  <script>
  export default {
    // Insert component logic here
  }
  </script>
  
  <style>
  @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap');
  
  /* Styling for fontawesome icons */
  @import url('https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.3/css/all.min.css');
  
  /* Styling for the sidebar */
  a {
    transition: background-color 0.2s ease, color 0.2s ease;
  }
  
  a.active {
    background-color: rgba(55, 125, 255, 0.25);
    color: #3b82f6;
  }
  </style>