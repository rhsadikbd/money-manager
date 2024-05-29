<template>
    <div class="bg-gray-200 h-screen">
        <!-- Page Header -->
        <div class="bg-white shadow-sm">
            <div class="max-w-[992px] mx-auto px-5">
                <div class="flex items-center justify-between py-6">
                    <h3 class="font-sans font-bold text-xl">Good Afternoon, <span class="text-xl text-cyan-500">Chandan
                            Bahadur</span></h3>
                    <div class="flex items-center gap-2">
                        <button class="active:bg-slate-100 btn" @click="addIncome">Add Income</button>
                        <button class="active:bg-cyan-700 btn bg-cyan-600 border-cyan-600 text-white" @click="addExpense">Add
                            Expense</button>
                    </div>
                </div>
            </div>
        </div>
        <!-- @@@ End Page Header -->

        <div class="max-w-[992px] mx-auto px-5">
            <!-- Overview Card -->
            <h5 class="font-sans text-xl font-bold pb-2 pt-12">Overview</h5>
            <div class="flex items-center justify-between gap-5">
                <div class="shadow-md p-5 flex items-center gap-5 bg-yellow-100 rounded-md w-full">
                    <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5"
                        stroke="currentColor" class="size-6">
                        <path stroke-linecap="round" stroke-linejoin="round"
                            d="M12 3v17.25m0 0c-1.472 0-2.882.265-4.185.75M12 20.25c1.472 0 2.882.265 4.185.75M18.75 4.97A48.416 48.416 0 0 0 12 4.5c-2.291 0-4.545.16-6.75.47m13.5 0c1.01.143 2.01.317 3 .52m-3-.52 2.62 10.726c.122.499-.106 1.028-.589 1.202a5.988 5.988 0 0 1-2.031.352 5.988 5.988 0 0 1-2.031-.352c-.483-.174-.711-.703-.59-1.202L18.75 4.971Zm-16.5.52c.99-.203 1.99-.377 3-.52m0 0 2.62 10.726c.122.499-.106 1.028-.589 1.202a5.989 5.989 0 0 1-2.031.352 5.989 5.989 0 0 1-2.031-.352c-.483-.174-.711-.703-.59-1.202L5.25 4.971Z" />
                    </svg>
                    <div>
                        <span class="text-gray-500">Total Income</span>
                        <h3 class="font-bold text-xl">Tk 50,000</h3>
                    </div>
                </div>
                <div class="shadow-md p-5 flex items-center gap-5 bg-red-100 rounded-md w-full">
                    <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5"
                        stroke="currentColor" class="size-6">
                        <path stroke-linecap="round" stroke-linejoin="round"
                            d="M12 3v17.25m0 0c-1.472 0-2.882.265-4.185.75M12 20.25c1.472 0 2.882.265 4.185.75M18.75 4.97A48.416 48.416 0 0 0 12 4.5c-2.291 0-4.545.16-6.75.47m13.5 0c1.01.143 2.01.317 3 .52m-3-.52 2.62 10.726c.122.499-.106 1.028-.589 1.202a5.988 5.988 0 0 1-2.031.352 5.988 5.988 0 0 1-2.031-.352c-.483-.174-.711-.703-.59-1.202L18.75 4.971Zm-16.5.52c.99-.203 1.99-.377 3-.52m0 0 2.62 10.726c.122.499-.106 1.028-.589 1.202a5.989 5.989 0 0 1-2.031.352 5.989 5.989 0 0 1-2.031-.352c-.483-.174-.711-.703-.59-1.202L5.25 4.971Z" />
                    </svg>
                    <div>
                        <span class="text-gray-500">Total Expense</span>
                        <h3 class="font-bold text-xl">Tk 35,000</h3>
                    </div>
                </div>
                <div class="shadow-md p-5 flex items-center gap-5 bg-green-100 rounded-md w-full">
                    <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5"
                        stroke="currentColor" class="size-6">
                        <path stroke-linecap="round" stroke-linejoin="round"
                            d="M12 3v17.25m0 0c-1.472 0-2.882.265-4.185.75M12 20.25c1.472 0 2.882.265 4.185.75M18.75 4.97A48.416 48.416 0 0 0 12 4.5c-2.291 0-4.545.16-6.75.47m13.5 0c1.01.143 2.01.317 3 .52m-3-.52 2.62 10.726c.122.499-.106 1.028-.589 1.202a5.988 5.988 0 0 1-2.031.352 5.988 5.988 0 0 1-2.031-.352c-.483-.174-.711-.703-.59-1.202L18.75 4.971Zm-16.5.52c.99-.203 1.99-.377 3-.52m0 0 2.62 10.726c.122.499-.106 1.028-.589 1.202a5.989 5.989 0 0 1-2.031.352 5.989 5.989 0 0 1-2.031-.352c-.483-.174-.711-.703-.59-1.202L5.25 4.971Z" />
                    </svg>
                    <div>
                        <span class="text-gray-500">Current Balance</span>
                        <h3 class="font-bold text-xl">Tk 15,000</h3>
                    </div>
                </div>
            </div>
            <!-- @@@ End Overview Card -->


            <!-- Activity Table -->
            <div class="mt-9">
                <div class="flex items-center justify-between mb-3">
                    <h5 class="font-sans text-xl font-bold">Recent Activity</h5>
                    <div>
                        <label for="table-search" class="sr-only">Search</label>
                        <div class="relative">
                            <div class="absolute inset-y-0 left-0 rtl:inset-r-0 rtl:right-0 flex items-center ps-3 pointer-events-none">
                                <svg class="w-5 h-5 text-gray-500 dark:text-gray-400" aria-hidden="true" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M8 4a4 4 0 100 8 4 4 0 000-8zM2 8a6 6 0 1110.89 3.476l4.817 4.817a1 1 0 01-1.414 1.414l-4.816-4.816A6 6 0 012 8z" clip-rule="evenodd"></path></svg>
                            </div>
                            <input type="text" id="table-search" class="mt-1 pe-3 ps-9 py-2 bg-white border shadow-sm border-slate-300 placeholder-slate-400 focus:outline-none focus:border-gray-300 focus:ring-gray-300 block w-full rounded-md text-sm focus:ring-1" placeholder="Search an item">
                        </div>
                    </div>
                </div>
                <div class="inline-block min-w-full shadow-md rounded-lg overflow-hidden">
                    <table class="w-full">
                        <thead class="bg-gray-100 border-b">
                            <tr>
                                <th class="text-center py-3 px-2 w-[15%]">Date</th>
                                <th class="text-left py-3 px-2">Transaction Details</th>
                                <th class="text-right py-3 px-2 w-[15%]">Amount</th>
                            </tr>
                        </thead>
                        <tbody class="bg-white">
                            <tr v-for="item in allTransaction" :key="item.id" class="border-b">
                                <td class="text-center py-2 px-2">{{ item.date }}</td>
                                <td class="text-left py-2 px-2">{{ item.des }}</td>
                                <td class="text-right py-2 px-2">{{ item.amount }}</td>
                            </tr>
                        </tbody>
                    </table>
                </div>
            </div>
            <!-- @@@ End Activity Table -->

        </div>




        <!-- Add Income Modal -->
        <div v-if="openIncomeModal" class="fixed top-0 left-0 bg-black bg-opacity-40 w-screen h-screen overflow-hidden flex items-center justify-center">
            <div class="bg-white min-w-[500px] rounded-md shadow-md" @click="handleClick">
                <!-- Modal Header  -->
                <div class="flex items-center justify-between py-2 px-3 border-b bg-gray-200 rounded-t-md">
                    <h5 class="text-md font-semibold font-sans">Add Income</h5>
                    <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5"
                        stroke="currentColor" class="size-6 cursor-pointer" @click="openIncomeModal = false">
                        <path stroke-linecap="round" stroke-linejoin="round" d="M6 18 18 6M6 6l12 12" />
                    </svg>
                </div>
                <!-- @@@ End Modal Header -->

                <!-- Modal Body -->
                <div class="px-3 py-2">
                    <div class="p-5">
                        <label for="income-date" class="after:content-['*'] after:ml-0.5 after:text-red-500 block text-sm font-medium text-slate-700">Income Date</label>
                        <input v-model="incomeDate" type="date" name="income-date" id="income-date" class="mt-1 px-3 py-2 bg-white border shadow-sm border-slate-300 placeholder-slate-400 focus:outline-none focus:border-gray-300 focus:ring-gray-300 block w-full rounded-md text-sm focus:ring-1">
                    </div>
                    <div class="px-5">
                        <label for="income-description" class="after:content-['*'] after:ml-0.5 after:text-red-500 block text-sm font-medium text-slate-700">Income Description</label>
                        <input v-model="incomeDes" placeholder="Enter details" type="text" name="income-description" id="income-description" class="mt-1 px-3 py-2 bg-white border shadow-sm border-slate-300 placeholder-slate-400 focus:outline-none focus:border-gray-300 focus:ring-gray-300 block w-full rounded-md text-sm focus:ring-1">
                    </div>
                    <div class="p-5">
                        <label for="income-amount" class="after:content-['*'] after:ml-0.5 after:text-red-500 block text-sm font-medium text-slate-700">Income Amount</label>
                        <input v-model="incomeAmount" placeholder="Enter amount in taka" type="number" name="income-amount" id="income-amount" class="mt-1 px-3 py-2 bg-white border shadow-sm border-slate-300 placeholder-slate-400 focus:outline-none focus:border-gray-300 focus:ring-gray-300 block w-full rounded-md text-sm focus:ring-1">
                    </div>
                </div>
                <!-- @ End Modal Body -->

                <!-- Modal Footer -->
                <div class="flex gap-2 border-t py-3 justify-center">
                    <button class="btn w-[100px] border-red-600 text-red-600 active:bg-red-100" @click="openIncomeModal = false">Cancel</button>
                    <button @click="saveIncome()" class="btn w-[100px] bg-green-600 border border-green-600 text-white active:bg-green-700">Save</button>
                </div>
                <!-- @@@ End Modal Footer -->
            </div>
        </div>
        <!-- @@@ End Add Income Modal -->



        <!-- Add Expense Modal -->
        <div v-if="openExpenseModal" class="fixed top-0 left-0 bg-black bg-opacity-40 w-screen h-screen overflow-hidden flex items-center justify-center">
            <div class="bg-white min-w-[500px] rounded-md shadow-md" @click="handleClick">
                <!-- Modal Header  -->
                <div class="flex items-center justify-between py-2 px-3 border-b bg-gray-200 rounded-t-md">
                    <h5 class="text-md font-semibold font-sans">Add Expense</h5>
                    <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5"
                        stroke="currentColor" class="size-6 cursor-pointer" @click="openExpenseModal = false">
                        <path stroke-linecap="round" stroke-linejoin="round" d="M6 18 18 6M6 6l12 12" />
                    </svg>
                </div>
                <!-- @@@ End Modal Header -->

                <!-- Modal Body -->
                <div class="px-3 py-2">
                    <div class="p-5">
                        <label for="income-date" class="after:content-['*'] after:ml-0.5 after:text-red-500 block text-sm font-medium text-slate-700">Expense Date</label>
                        <input type="date" name="income-date" id="income-date" class="mt-1 px-3 py-2 bg-white border shadow-sm border-slate-300 placeholder-slate-400 focus:outline-none focus:border-gray-300 focus:ring-gray-300 block w-full rounded-md text-sm focus:ring-1">
                    </div>
                    <div class="px-5">
                        <label for="income-description" class="after:content-['*'] after:ml-0.5 after:text-red-500 block text-sm font-medium text-slate-700">Expense Description</label>
                        <input placeholder="Enter details" type="text" name="income-description" id="income-description" class="mt-1 px-3 py-2 bg-white border shadow-sm border-slate-300 placeholder-slate-400 focus:outline-none focus:border-gray-300 focus:ring-gray-300 block w-full rounded-md text-sm focus:ring-1">
                    </div>
                    <div class="p-5">
                        <label for="income-amount" class="after:content-['*'] after:ml-0.5 after:text-red-500 block text-sm font-medium text-slate-700">Expense Amount</label>
                        <input placeholder="Enter amount in taka" type="number" name="income-amount" id="income-amount" class="mt-1 px-3 py-2 bg-white border shadow-sm border-slate-300 placeholder-slate-400 focus:outline-none focus:border-gray-300 focus:ring-gray-300 block w-full rounded-md text-sm focus:ring-1">
                    </div>
                </div>
                <!-- @ End Modal Body -->

                <!-- Modal Footer -->
                <div class="flex gap-2 border-t py-3 justify-center">
                    <button class="btn w-[100px] border-red-600 text-red-600 active:bg-red-100 py-2" @click="openExpenseModal = false">Cancel</button>
                    <button class="btn w-[100px] bg-green-600 border border-green-600 text-white active:bg-green-700">Save</button>
                </div>
                <!-- @@@ End Modal Footer -->
            </div>
        </div>
        <!-- @@@ End Add Expense Modal -->
    </div>
</template>





<script setup>
    import { ref } from 'vue';
    let openIncomeModal = ref(false);
    let openExpenseModal = ref(false);
    let incomeDate = ref()
    let incomeDes = ref()
    let incomeAmount = ref()
    let allTransaction = ref([
        {
            id: 1,
            date: '28/05/2024',
            des: 'MI 22" Monitor Black',
            amount: '12000'
        },
        {
            id: 2,
            date: '27/05/2024',
            des: 'ASUS CPU',
            amount: '40000'
        },
        {
            id: 3,
            date: '26/05/2024',
            des: 'Mouse Pad',
            amount: '1000'
        }
    ])


    function handleClick(event) {
        event.stopImmediatePropagation();
    }
    
    function addIncome(){
        openIncomeModal.value = true
    }
    
    function addExpense(){
        openExpenseModal.value = true
    }

    function saveIncome(){
        allTransaction.value.push({
            id: Math.random(),
            date: incomeDate,
            des: incomeDes,
            amount: incomeAmount
        });
    }
</script>





<style lang="">

</style>