<script setup lang="ts">
  import { ref } from 'vue'
  import Sidebar from "@/components/Sidebar.vue";
  import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome';
  import { faBars, faExclamationTriangle, faMessage, faUser, faCopy, faEnvelope, faPhone, faLocationPin, faPlus, faChartBar } from '@fortawesome/free-solid-svg-icons';
  import { faTelegram } from '@fortawesome/free-brands-svg-icons'

  const isSidebarOpen = ref(false)
</script>

<template>
  <div class="flex min-h-screen">
    <Sidebar :isOpen="isSidebarOpen" @toggle="isSidebarOpen = !isSidebarOpen" />
    <div class="flex-1 flex flex-col lg:ml-64 lg:w-[calc(100%-16rem)]">
      <header class="bg-indigo-200 shadow p-4 flex justify-between items-center">
        <button @click="isSidebarOpen = !isSidebarOpen" class="lg:hidden ">
          <FontAwesomeIcon :icon="faBars" size="2x" class="text-indigo-600" />
        </button>
        <div class="hidden lg:flex items-center justify-between w-full">
          <div></div>
          <h1 class="text-indigo-900 font-semibold">Our Virtual assistance tool will offer guidance along the way. Please address the yellow and red tasks.</h1>
          <button class="bg-indigo-500 text-white py-1 px-3 rounded">Close</button>
        </div>
      </header>
      <main class="p-4 flex flex-col lg:flex-row gap-4">
        <div class="bg-indigo-200 p-4 flex flex-col gap-4 lg:w-[350px] rounded-md">
          <h1 class="text-xl font-semibold text-center">Virtual Assistance</h1>
          <div class="bg-white flex items-center p-2 gap-4 justify-center border border-gray-400">
            <FontAwesomeIcon :icon="faExclamationTriangle" size="2x" class=" text-red-600" />
            <p>Email Address not verified.</p>
          </div>
          <div class="bg-indigo-500 flex items-center justify-center p-2 gap-4 text-white rounded">
            <FontAwesomeIcon :icon="faTelegram" size="2x" class="" />
            <p>Send Email Confirmation</p>
          </div>
          <div class="bg-white flex items-center justify-center p-2 gap-4 border border-gray-400">
            <FontAwesomeIcon :icon="faExclamationTriangle" size="2x" class=" text-red-600" />
            <p>Text Message not verified.</p>
          </div>
          <div class="bg-indigo-500 flex items-center justify-center p-2 gap-4 text-white rounded">
            <FontAwesomeIcon :icon="faMessage" size="2x" class="" />
            <p>Send SMS Confirmation</p>
          </div>
          <div class="bg-white rounded p-4">
            <p>Notification of offers are sent in real-time via email and SMS. We recommend you to verify you are receiving our notifications.</p>
            <p class="my-4">Select the confirmation button in the body of the email and 2 digit verification number to complete this task.</p>
          </div>
          <div class="bg-white flex items-center justify-center p-2 gap-4 border border-gray-400">
            <FontAwesomeIcon :icon="faExclamationTriangle" size="2x" class=" text-red-600" />
            <p>Missing Mail Address.</p>
          </div>
          <div class="bg-white rounded p-4">
            <p>Should we submit an agreement to Disney and the Title Company, a complete mailing address is required.</p>
            <button class="bg-indigo-500 p-2 text-white rounded w-full mt-2">Edit Mailing Address</button>
          </div>
          <button class="border-indigo-500 bg-white border-2 p-2 text-indigo-500 rounded w-full mt-2">Edit Mailing Address</button>
        </div>
        <div class="bg-gray-200 rounded-md border p-4 border-gray-300">
          <div class=" w-full flex flex-col md:flex-row items-center gap-4 h-fit border-b-4 pb-10 border-white">
            <div class="bg-white flex flex-col gap-1 p-3">
              <div class="flex justify-between gap-4 items-center">
                <div class="text-indigo-900 flex items-center gap-2">
                  <FontAwesomeIcon :icon="faUser" class="" />
                  <p class="font-semibold">Paolo Joe Di Battista</p>
                </div>
                <div class="flex gap-3 items-center text-indigo-900">
                  <FontAwesomeIcon :icon="faCopy" class="border p-1 border-indigo-900 rounded" />
                  <p class="px-2 border rounded border-indigo-900 ">Edit</p>
                </div>
              </div>
              <div class="flex justify-between items-center gap-4">
                <div class="text-indigo-900 flex items-center gap-2">
                  <FontAwesomeIcon :icon="faEnvelope" class="" />
                  <p class="">paolo@attrius.ca</p>
                </div>
                <FontAwesomeIcon :icon="faCopy" class="border p-1 rounded text-indigo-900 border-indigo-900" />
              </div>
              <div class="flex justify-between gap-4 items-center">
                <div class="text-indigo-900 flex items-center gap-2">
                  <FontAwesomeIcon :icon="faPhone" class="" />
                  <p>+1 (647) 880-4288</p>
                </div>
                <div class="flex gap-2 items-center bg-indigo-500 px-2 rounded">
                  <FontAwesomeIcon :icon="faExclamationTriangle" class=" text-red-600" />
                  <p class="text-white">Verify</p>
                </div>
                <div class="flex gap-3 items-center text-indigo-900">
                  <FontAwesomeIcon :icon="faMessage" class="bg-green-700 text-white p-1 rounded" />
                  <FontAwesomeIcon :icon="faCopy" class="border p-1 border-indigo-900 rounded" />
                </div>
              </div>
              <div class="flex justify-between items-center gap-4">
                <div class="text-indigo-900 flex items-center gap-2">
                  <FontAwesomeIcon :icon="faLocationPin" class="" />
                  <p class="">16 Josephine Rd, Vaughan, ON L4H 0M4, Canada</p>
                </div>
                <FontAwesomeIcon :icon="faCopy" class="border p-1 rounded text-indigo-900 border-indigo-900" />
              </div>
            </div>
  
            <div class="bg-white flex flex-col gap-1 p-3">
              <div class="flex justify-between gap-4 items-center">
                <div class="text-indigo-900 flex items-center gap-2">
                  <FontAwesomeIcon :icon="faUser" class="" />
                  <p class="font-semibold">Jo-Ann D'Addio</p>
                </div>
                <div class="flex gap-3 items-center text-indigo-900">
                  <FontAwesomeIcon :icon="faCopy" class="border p-1 border-indigo-900 rounded" />
                  <p class="px-2 border rounded border-indigo-900 ">Edit</p>
                </div>
              </div>
              <div class="flex justify-between items-center gap-4">
                <div class="text-indigo-900 flex items-center gap-2">
                  <FontAwesomeIcon :icon="faEnvelope" class="" />
                  <p class="">paolo@attrius.ca</p>
                </div>
                <FontAwesomeIcon :icon="faCopy" class="border p-1 rounded text-indigo-900 border-indigo-900" />
              </div>
              <div class="flex justify-between gap-4 items-center">
                <div class="text-indigo-900 flex items-center gap-2">
                  <FontAwesomeIcon :icon="faPhone" class="" />
                  <p>+1 (647) 880-4288</p>
                </div>
                <div class="flex gap-3 items-center text-indigo-900">
                  <FontAwesomeIcon :icon="faMessage" class="bg-green-700 text-white p-1 rounded" />
                  <FontAwesomeIcon :icon="faCopy" class="border p-1 border-indigo-900 rounded" />
                </div>
              </div>
              <div class="flex justify-between items-center gap-4">
                <div class="text-indigo-900 flex items-center gap-2">
                  <FontAwesomeIcon :icon="faLocationPin" class="" />
                  <p class="">16 Josephine Rd, Vaughan, ON L4H 0M4, Canada</p>
                </div>
                <FontAwesomeIcon :icon="faCopy" class="border p-1 rounded text-indigo-900 border-indigo-900" />
              </div>
            </div>
  
            <div class=" text-indigo-900 w-full lg:w-[100px] bg-white rounded-lg text-center h-fit">
              <FontAwesomeIcon :icon="faPlus" size="2x" class="" />
              <p>Add Additional Seller</p>
            </div>
          </div>

          <div class="py-4">
            <form action="">
              <label for="Salutation">Salutation</label>
              <input type="text" value="Paolo and Jo-Ann" class="border ml-4 p-1 text-sm">

              <label for="lock" class="ml-2">Lock</label>
              <input type="checkbox" class="ml-4">

              <label for="usresident" class="ml-10">US Resident</label>
              <input type="checkbox" class="ml-4">

              <div class="mt-2">
                <label for="">First Sentence of the Contract</label>
                <input type="text" value="Paolo and Jo-Ann" class="border ml-4 p-1 text-sm ">

                <label for="lock" class="ml-2">Lock</label>
                <input type="checkbox" class="ml-4">
              </div>

              <div class="mt-2 border-b-4 pb-6 border-white">
                <label for="email notification" class="">Receive Email Notifications</label>
                <input type="checkbox" class="ml-4">

                <label for="email notification" class="ml-6">Receive Email Notifications</label>
                <input type="checkbox" class="ml-4">
              </div>

              <div class="py-4">
                <label for="Password">Password</label>
                <input type="password" value="Paolo and Jo-Ann" class="border ml-4 p-1 text-sm">

                <button class="text-white bg-indigo-500 py-1 px-2 ml-10">Reset Password</button>
              </div>
            </form>
          </div>

          <div class="bg-yellow-50 px-4 py-2 space-y-4">
            <div class="flex items-center gap-3 mb-4">
              <p class="text-white bg-indigo-900 p-1 italic">INVENTORY FOR SALE</p>
              <p class="text-white bg-green-700 p-1 italic">ADD INVENTORY TO SELL</p>
            </div>

            <div class="min-w-full w-4 overflow-x-auto">
              <table class="min-w-full text-sm text-indigo-900">
                <thead>
                  <tr class="text-center">
                    <th class="font-normal p-2 min-w-28">
                      <p>ID Number</p>
                      <p>Resort Name</p>
                    </th>
                    <th></th>
                    <th class="font-normal p-2 min-w-28">
                      <p>Yearly Points</p>
                      <p>Contact Num</p>
                    </th>
                    <th class="font-normal p-2">Status</th>
                    <th class="font-normal p-2 min-w-28">
                      <p>Traffic</p>
                      <p>Analytics</p>
                    </th>
                    <th class="font-normal p-2 min-w-28">
                      <p>Copy of</p>
                      <p>the Deed</p>
                    </th>
                    <th class="font-normal p-2 min-w-28">
                      <p>Available points</p>
                      <p>Statement</p>
                    </th>
                    <th class="font-normal p-2 min-w-28">
                      <p>More</p>
                      <p>Information</p>
                    </th>
                  </tr>
                </thead>

                <tbody>
                  <tr class="text-center bg-indigo-100 border-2 border-indigo-500">
                    <td class="p-2">Old Key West</td>
                    <td class="p-2"></td>
                    <td  class="p-2">50</td>
                    <td  class="p-2">
                      <p class="border border-indigo-700 rounded p-1 bg-white text-indigo-700">Available</p>
                    </td>
                    <td class="p-2">
                      <FontAwesomeIcon :icon="faChartBar" class="text-indigo-700" />
                    </td>
                    <td class="p-2">Upload</td>
                    <td class="p-2">Upload</td>
                    <td  class="p-2">
                      <p class="border bg-white border-indigo-900 p-1 rounded text-indigo-900 italic text-sm">VIEW DETAILS</p>
                    </td>
                  </tr>
                </tbody>
              </table>
            </div>


            <p class="text-white bg-indigo-900 p-1 italic w-fit">ACTIVE OFFERS</p>

            <div class="min-w-full w-4 overflow-x-auto">
              <table class="min-w-full text-sm text-indigo-900">
                <thead>
                  <tr class="text-center">
                    <th class="font-semibold p-2 min-w-28">
                      <p>ID Number</p>
                      <p>Resort Name</p>
                    </th>
                    <th></th>
                    <th class="font-semibold p-2 min-w-28">
                      <p>Yearly Points</p>
                      <p>Contact Num</p>
                    </th>
                    <th class="font-semibold p-2 min-w-28">Status</th>
                    <th class="font-semibold p-2 min-w-28">
                      <p>Offer</p>
                      <p>Date</p>
                    </th>
                    <th class="font-semibold p-2 min-w-28">
                      <p>Asking Price</p>
                      <p>Offer Price</p>
                    </th>
                    <th class="font-semibold p-2 min-w-28">
                      <p>Available points</p>
                      <p>Statement</p>
                    </th>
                    <th class="font-semibold p-2 min-w-28">
                      Buyer
                    </th>
                  </tr>
                </thead>

                <tbody>
                  <tr class="text-center bg-indigo-100 border-2 border-indigo-500">
                    <td class="p-2">Old Key West</td>
                    <td class="p-2"></td>
                    <td  class="p-2">50</td>
                    <td  class="p-2">
                      <p class="border border-indigo-700 rounded p-1 bg-white text-indigo-700">Counter offer</p>
                    </td>
                    <td class="p-2">
                      <p>02/02/2025</p>
                      <p>09:58pm</p>
                    </td>
                    <td class="p-2">
                      <p>$119.00</p>
                      <p>$108.00</p>
                    </td>
                    <td class="p-2">Holly Ann</td>
                    <td  class="p-2">
                      <p class="border bg-white border-indigo-900 p-1 rounded text-indigo-900 italic text-sm">VIEW DETAILS</p>
                    </td>
                  </tr>
                </tbody>
              </table>
            </div>
          </div>
        </div>
        
      </main>
    </div>
    
  </div>
</template>