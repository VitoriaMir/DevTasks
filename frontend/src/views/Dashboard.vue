<template>
  <div class="min-h-screen bg-gray-50">
    <!-- Navigation -->
    <nav class="bg-white shadow">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="flex justify-between h-16">
          <div class="flex items-center">
            <h1 class="text-xl font-bold text-gray-900">DevTasks</h1>
          </div>
          <div class="flex items-center space-x-4">
            <span class="text-gray-700">Usuário</span>
            <button @click="logout" class="btn-secondary">Sair</button>
          </div>
        </div>
      </div>
    </nav>

    <!-- Main Content -->
    <div class="max-w-7xl mx-auto py-6 sm:px-6 lg:px-8">
      <!-- Header -->
      <div class="mb-8">
        <h1 class="text-2xl font-bold text-gray-900">Dashboard</h1>
        <p class="text-gray-600">Bem-vindo ao DevTasks!</p>
      </div>

      <!-- Stats Cards -->
      <div class="grid grid-cols-1 md:grid-cols-4 gap-6 mb-8">
        <div class="card p-6">
          <div class="flex items-center">
            <div class="flex-shrink-0">
              <div class="w-8 h-8 bg-blue-500 rounded-md flex items-center justify-center">
                <svg class="w-5 h-5 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5H7a2 2 0 00-2 2v10a2 2 0 002 2h8a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path>
                </svg>
              </div>
            </div>
            <div class="ml-5 w-0 flex-1">
              <dl>
                <dt class="text-sm font-medium text-gray-500 truncate">Total de Tarefas</dt>
                <dd class="text-lg font-medium text-gray-900">{{ totalTasks }}</dd>
              </dl>
            </div>
          </div>
        </div>

        <div class="card p-6">
          <div class="flex items-center">
            <div class="flex-shrink-0">
              <div class="w-8 h-8 bg-green-500 rounded-md flex items-center justify-center">
                <svg class="w-5 h-5 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"></path>
                </svg>
              </div>
            </div>
            <div class="ml-5 w-0 flex-1">
              <dl>
                <dt class="text-sm font-medium text-gray-500 truncate">Concluídas</dt>
                <dd class="text-lg font-medium text-gray-900">{{ completedTasks }}</dd>
              </dl>
            </div>
          </div>
        </div>

        <div class="card p-6">
          <div class="flex items-center">
            <div class="flex-shrink-0">
              <div class="w-8 h-8 bg-yellow-500 rounded-md flex items-center justify-center">
                <svg class="w-5 h-5 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z"></path>
                </svg>
              </div>
            </div>
            <div class="ml-5 w-0 flex-1">
              <dl>
                <dt class="text-sm font-medium text-gray-500 truncate">Em Progresso</dt>
                <dd class="text-lg font-medium text-gray-900">{{ inProgressTasks }}</dd>
              </dl>
            </div>
          </div>
        </div>

        <div class="card p-6">
          <div class="flex items-center">
            <div class="flex-shrink-0">
              <div class="w-8 h-8 bg-red-500 rounded-md flex items-center justify-center">
                <svg class="w-5 h-5 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 9v2m0 4h.01m-6.938 4h13.856c1.54 0 2.502-1.667 1.732-2.5L13.732 4c-.77-.833-1.964-.833-2.732 0L3.732 16.5c-.77.833.192 2.5 1.732 2.5z"></path>
                </svg>
              </div>
            </div>
            <div class="ml-5 w-0 flex-1">
              <dl>
                <dt class="text-sm font-medium text-gray-500 truncate">Atrasadas</dt>
                <dd class="text-lg font-medium text-gray-900">{{ overdueTasks }}</dd>
              </dl>
            </div>
          </div>
        </div>
      </div>

      <!-- Quick Actions -->
      <div class="mb-8">
        <h2 class="text-lg font-medium text-gray-900 mb-4">Ações Rápidas</h2>
        <div class="flex space-x-4">
          <button class="btn-primary">
            <svg class="w-4 h-4 mr-2" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 4v16m8-8H4"></path>
            </svg>
            Nova Tarefa
          </button>
          <button class="btn-secondary">
            <svg class="w-4 h-4 mr-2" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 11H5m14 0a2 2 0 012 2v6a2 2 0 01-2 2H5a2 2 0 01-2-2v-6a2 2 0 012-2m14 0V9a2 2 0 00-2-2M5 11V9a2 2 0 012-2m0 0V5a2 2 0 012-2h6a2 2 0 012 2v2M7 7h10"></path>
            </svg>
            Ver Quadro Kanban
          </button>
          <button class="btn-secondary">
            <svg class="w-4 h-4 mr-2" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 7V3m8 4V3m-9 8h10M5 21h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v12a2 2 0 002 2z"></path>
            </svg>
            Calendário
          </button>
        </div>
      </div>

      <!-- Recent Tasks -->
      <div class="card">
        <div class="px-4 py-5 sm:p-6">
          <h3 class="text-lg leading-6 font-medium text-gray-900 mb-4">Tarefas Recentes</h3>
          <div class="space-y-3">
            <div v-if="recentTasks.length === 0" class="text-gray-500 text-center py-8">
              Nenhuma tarefa encontrada. Crie sua primeira tarefa!
            </div>
            <div v-for="task in recentTasks" :key="task.id" class="flex items-center justify-between py-3 border-b border-gray-200 last:border-b-0">
              <div class="flex items-center">
                <div class="flex-shrink-0">
                  <div class="w-3 h-3 rounded-full" :class="{
                    'bg-green-400': task.status === 'done',
                    'bg-blue-400': task.status === 'in-progress',
                    'bg-yellow-400': task.status === 'review',
                    'bg-gray-400': task.status === 'todo'
                  }"></div>
                </div>
                <div class="ml-4">
                  <p class="text-sm font-medium text-gray-900">{{ task.title }}</p>
                  <p class="text-sm text-gray-500">{{ task.description || 'Sem descrição' }}</p>
                </div>
              </div>
              <div class="flex items-center space-x-2">
                <span class="inline-flex items-center px-2.5 py-0.5 rounded-full text-xs font-medium" :class="{
                  'bg-green-100 text-green-800': task.status === 'done',
                  'bg-blue-100 text-blue-800': task.status === 'in-progress',
                  'bg-yellow-100 text-yellow-800': task.status === 'review',
                  'bg-gray-100 text-gray-800': task.status === 'todo'
                }">
                  {{ getStatusLabel(task.status) }}
                </span>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref, computed } from 'vue'
import { useRouter } from 'vue-router'

const router = useRouter()

// Mock data para demonstração
const tasks = ref([
  {
    id: 1,
    title: 'Implementar autenticação',
    description: 'Criar sistema de login e registro',
    status: 'in-progress',
    created_at: new Date()
  },
  {
    id: 2,
    title: 'Design do dashboard',
    description: 'Criar interface do painel principal',
    status: 'done',
    created_at: new Date()
  },
  {
    id: 3,
    title: 'Testes unitários',
    description: 'Escrever testes para componentes',
    status: 'todo',
    created_at: new Date()
  }
])

// Computed properties para estatísticas
const totalTasks = computed(() => tasks.value.length)
const completedTasks = computed(() => tasks.value.filter(t => t.status === 'done').length)
const inProgressTasks = computed(() => tasks.value.filter(t => t.status === 'in-progress').length)
const overdueTasks = computed(() => 0) // Implementar lógica de vencimento

const recentTasks = computed(() => {
  return tasks.value
    .sort((a, b) => new Date(b.created_at) - new Date(a.created_at))
    .slice(0, 5)
})

const getStatusLabel = (status) => {
  const labels = {
    'todo': 'A Fazer',
    'in-progress': 'Em Progresso', 
    'review': 'Em Revisão',
    'done': 'Concluído'
  }
  return labels[status] || status
}

const logout = () => {
  router.push('/login')
}
</script>