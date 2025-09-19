# Mannu.cmsimport { Sidebar } from "./components/Sidebar";
import { Topbar } from "./components/Topbar";
import { DashboardCards } from "./components/DashboardCards";

export default function App() {
  return (
    <div class="flex h-screen bg-gray-100">
      <Sidebar />
      <div class="flex-1 flex flex-col">
        <Topbar />
        <main class="flex-1 p-6 overflow-y-auto">
          <DashboardCards />
          <div class="bg-white rounded shadow p-6 mt-6">
            <h2 class="text-xl font-semibold mb-4">Overview</h2>
            <p class="text-gray-600">Welcome to your dashboard. Here you can monitor all key metrics and manage your content.</p>
          </div>
        </main>
      </div>
    </div>
  );
}
export function Sidebar() {
  return (
    <aside class="w-64 bg-white shadow-md hidden md:block">
      <div class="p-4 font-bold text-xl border-b">Mannu CMS</div>
      <nav class="mt-6 space-y-2">
        <a href="#" class="flex items-center px-4 py-2 text-gray-700 hover:bg-gray-100 rounded">Dashboard</a>
        <a href="#" class="flex items-center px-4 py-2 text-gray-700 hover:bg-gray-100 rounded">Users</a>
        <a href="#" class="flex items-center px-4 py-2 text-gray-700 hover:bg-gray-100 rounded">Settings</a>
        <a href="#" class="flex items-center px-4 py-2 text-gray-700 hover:bg-gray-100 rounded">Analytics</a>
      </nav>
    </aside>
  );
}
export function Topbar() {
  return (
    <header class="bg-white shadow flex items-center justify-between px-6 py-4">
      <div class="text-lg font-semibold">Dashboard</div>
      <div class="flex items-center space-x-4">
        <span class="text-gray-600">Hello, Admin</span>
        <img class="w-8 h-8 rounded-full" src="https://i.pravatar.cc/40" alt="User avatar" />
      </div>
    </header>
  );
}
export function DashboardCards() {
  return (
    <div class="grid grid-cols-1 md:grid-cols-3 gap-6 mb-6">
      <div class="bg-white rounded shadow p-4">
        <div class="text-gray-500">Users</div>
        <div class="text-2xl font-bold">1,234</div>
      </div>
      <div class="bg-white rounded shadow p-4">
        <div class="text-gray-500">Posts</div>
        <div class="text-2xl font-bold">567</div>
      </div>
      <div class="bg-white rounded shadow p-4">
        <div class="text-gray-500">Revenue</div>
        <div class="text-2xl font-bold">$3,456</div>
      </div>
    </div>
  );
}
