<script>
  import Step from "./Step.svelte";

  let steps = [
    { name: "TrackLift CRUD", icon: "fa-solid fa-dumbbell" },
    { name: "Capstone Project", icon: "fa-solid fa-book" },
    { name: "Servicing System", icon: "fa-solid fa-folder-open" },
  ];

  let benefits = [
    {
      name: "NAIT Software Dev. graduate (honours)",
      description:
        "I obtained a diploma in Digital Media and IT - Computer Software Development Specialization at NAIT, where I gained a strong foundation in programming, working with languages such as C#, HTML/CSS, JavaScript, Dart, Java, and SvelteKit. I quickly developed a passion for the entire development process—analyzing frameworks, designing databases and backend systems, and crafting intuitive UI/UX experiences. I thrive on bringing ideas to life, ensuring both functionality and user satisfaction in every project.",
    },
    {
      name: "An excellent communicator and great soft skills",
      description:
        "I believe communication and leadership skills are just as important—if not more—than technical expertise. Transparency and constructive communication are core values of mine, helping me build strong relationships and foster collaboration. These principles enhance my effectiveness and productivity in any team or workspace.",
    },
    {
      name: "A product design & UX fanatic",
      description:
        "Carefully crafting and designing applications from backend to frontend has become a true passion of mine. It allows me to blend creativity with technical expertise to bring ideas to life—whether its a simple to-do list or a fully responsive website. I also enjoy the challenge of learning new design concepts and emerging technologies to continuously improve my skills and build more efficient, high-quality applications.",
    },
  ];
</script>

<main class="flex flex-col flex-1 p-4">
  <section
    id="introPage"
    class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14"
  >
    <div
      class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8 lg:gap-10"
    >
      <h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl">
        Hi! I'm <span class="poppins text-violet-400">Andres</span> Garcia
        <br />Full Stack
        <span class="poppins text-violet-400"> Developer</span>
      </h2>
      <p class="text-base sm:text-lg md:text-xl">
        My <span class="text-violet-400">favorite tech</span> includes Javascript
        (SvelteKit), Flutter, TailwindCss, Node.js & Next.js, Firebase/FireStore,
        Supabase, SQL, React, Bootstrap, and Blazor
      </p>
      <a
        class="blueShadow mx-auto lg:mr-auto text-base sm:text-lg md:text-lg poppins relative overflow-hidden px-6 py-3 group rounded-full
            bg-white text-slate-950 cursor-pointer"
        href="https://x.com/elBulletzzz"
        target="_blank"
      >
        <div
          class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20 group-hover:translate-x-full z-0 duration-200"
        ></div>
        <h4 class="relative z-9">Get in touch &rarr;</h4>
      </a>
    </div>
    <div class="relative shadow-2xl grid place-items-center">
      <img
        src={"images/profile.jpg"}
        alt="profile img"
        class="object-cover z-[2] max-h-[70vh]"
      />
    </div>
  </section>

  <section id="projects" class="py-20 lg:py-32 flex flex-col gap-24">
    <div class="flex flex-col gap-2 text-center">
      <h6 class="text-lg sm:text-xl md:text-2xl">
        A few of my creative endeavors.
      </h6>
      <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
        Coriuos to <span class="poppins text-violet-400">know about</span> my work?
      </h3>
    </div>
    <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
      <Step step={steps[0]}>
        <p>
          TrackLift is a Full Stack mobile CRUD app developed using <strong
            class="text-violet-400">Dart, Flutter and Firebase/Firestore</strong
          > User's can register and sign in and it's designed to help users track
          their personal exercises. It allows users to log details such as the name
          of the workout, the number of sets, and the number of reps completed for
          each exercise. Users can then view exercise reports filtered by the date
          they were completed. All exercises are organized and grouped by the day
          of the week, providing a clear and structured overview of their workout
          progress. users can also update workouts and delete workouts from the list.
        </p>
      </Step>
      <Step step={steps[1]}>
        <p>
          My capstone project was a web application developed using <strong
            class="text-violet-400">SvelteKit, JavaScript, and Supabase.</strong
          > We implemented an add-on to an existing website to create a voting system
          where all players in the sports league were presented in a 1v1 format,
          displaying the mugshots of two players on the screen along with their current
          season stats, which were updated daily using the official sports API. Users
          had to vote for one of the two players. We processed all votes in our backend
          to generate player rankings based on user votes. Additionally, we created
          two types of user profiles: fans and official players, with results displayed
          separately for each group. Some key business rules included prioritizing
          a signed-in player’s team when displaying matchups, ensuring that the signed-in
          player did not appear in the voting game, and displaying the signed-in
          player's information (such as name, team, and jersey number) in the navbar,
          whereas for a logged-in fan, only their username was shown. This approach
          ensured a personalized experience while maintaining fair voting rules.
        </p>
      </Step>
      <Step step={steps[2]}>
        <p>
          The Servicing System was part of a group project in which we developed
          a full web application for a motorcycle shop, and my role focused on
          the Servicing System. This system was developed using <strong
            class="text-violet-400">C#, Blazor, and SQL.</strong
          > I was responsible for ensuring that the VIN number and customer information
          existed in our database. If a new VIN was entered, we needed to register
          the vehicle and create a new work order. Additionally, I had to verify
          the shop rates and apply them to the order based on the estimated job duration,
          which was determined by our shop rates and the hours required for the specific
          service performed on the vehicle. I also implemented a system to process
          customer coupons, ensuring they were valid and not expired before applying
          them to the order.
        </p>
      </Step>
    </div>
  </section>
  <section
    id="about"
    class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative"
  >
    <div
      class="flex flex-col gap-2 text-center relative before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-violet-700 after:absolute after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-violet-700 py-4"
    >
      <h6 class="text-lg sm:text-xl md:text-2xl">Want to know more?</h6>
      <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
        A bit <span class="poppins text-violet-400">about</span>me.
      </h3>
    </div>
    <p class="mx-auto poppins font-semibold text-lg sm:text-xl md:text-2xl">
      I am ...
    </p>
    <div class="flex flex-col gap-20 w-full mx-auto max-w-[800px]">
      {#each benefits as benefit, index}
        <div class="flex gap-6 sm:gap-8">
          <p
            class="poppins text-4xl sm:text-5xl md:text-6xl text-slate-500 font-semibold"
          >
            0{index + 1}
          </p>
          <div class="flex flex-col gap-6 sm:gap-8">
            <h3 class="text-2xl sm:text-3xl md:text-5xl">
              {benefit.name}
            </h3>
            <p>{benefit.description}</p>
          </div>
        </div>
      {/each}
    </div>
    <h5 class="mx-auto text-2xl sm:text-3xl md:text-5xl">The <span class="text-violet-400">Complete</span> Package:</h5>
    <div
      class="flex flex-col overflow-x-scroll gap-10 max-w-[800px] mx-auto w-full"
    >
      <table class="bg-white text-slate-700 rounded text-center">
        <thead class="border-b border-solid border-slate-200">
          <tr class="">
            <th/>
            <th class="whitespace-nowrap p-2 px-4">Candidate #1</th>
            <th class="whitespace-nowrap p-2 px-4">Candidate #2</th>
            <th class="whitespace-nowrap p-2 px-4">Candidate #3</th>
            <th class="whitespace-nowrap bg-violet-700 text-white p-4 px-8"
              >Me
            </th>
          </tr>
        </thead>
        <tbody>
          <tr class="border-b border-solid border-slate-200">
            <td
              class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm whitespace-nowrap"
              >Dedication</td
            >
            <td><i class="fa-solid fa-check text-slate-500"></i></td>
            <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
            <td><i class="fa-solid fa-check text-slate-500"></i></td>
            <td><i class="fa-solid fa-check text-green-500"></i></td>
          </tr>
          <tr class="border-b border-solid border-slate-200">
            <td
              class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm whitespace-nowrap"
              >Soft-Skills</td
            >
            <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
            <td><i class="fa-solid fa-check text-slate-500"></i></td>
            <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
            <td><i class="fa-solid fa-check text-green-500"></i></td>
          </tr>
          <tr class="border-b border-solid border-slate-200">
            <td
              class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm whitespace-nowrap"
              >Critical Thinking</td
            >
            <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
            <td><i class="fa-solid fa-check text-slate-500"></i></td>
            <td><i class="fa-solid fa-check text-slate-500"></i></td>
            <td><i class="fa-solid fa-check text-green-500"></i></td>
          </tr>
          <tr class="border-b border-solid border-slate-200">
            <td
              class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm whitespace-nowrap"
              >Programing Ability</td
            >
            <td><i class="fa-solid fa-check text-slate-500"></i></td>
            <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
            <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
            <td><i class="fa-solid fa-check text-green-500"></i></td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="mx-auto -mt-12 italic sm:hidden opacity-50">
        <p>Scroll to see more &rarr;</p>
    </div>
  </section>
</main>
