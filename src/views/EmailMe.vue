<template>
  <section class="mx-auto mt-20 w-5/6 max-w-6xl lg:w-3/4">
    <article
      class="flex flex-col items-center justify-between rounded-3xl bg-yellow-500 p-8 md:flex-row md:py-16 md:px-16 lg:px-20"
    >
      <h2 class="text-white font-md text-5xl font-medium">
        Interested<br />
        working<br />
        with me?
      </h2>
      <div
        class="mt-14 flex flex-col items-center justify-between gap-6 md:mt-0 xl:flex-row xl:gap-12"
      >
        <button
          class="text-2xl flex items-center justify-between gap-4 rounded-md font-medium bg-white py-5 px-8"
        >
          <svg
            stroke="currentColor"
            fill="currentColor"
            stroke-width="0.5"
            viewBox="0 0 16 16"
            height="24"
            width="24"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              d="M0 4a2 2 0 0 1 2-2h12a2 2 0 0 1 2 2v8a2 2 0 0 1-2 2H2a2 2 0 0 1-2-2V4Zm2-1a1 1 0 0 0-1 1v.217l7 4.2 7-4.2V4a1 1 0 0 0-1-1H2Zm13 2.383-4.708 2.825L15 11.105V5.383Zm-.034 6.876-5.64-3.471L8 9.583l-1.326-.795-5.64 3.47A1 1 0 0 0 2 13h12a1 1 0 0 0 .966-.741ZM1 11.105l4.708-2.897L1 5.383v5.722Z"
            ></path></svg
          >Email Me</button
        ><button
          class="button-outline border border-white py-4 px-5 text-2xl rounded-md font-medium text-white"
        >
          See More Projects
        </button>
      </div>
    </article>
  </section>
</template>

<script>
export default {
  name: 'EmailMeView',
}
</script>
