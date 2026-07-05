<template>
  <!-- Loader initial -->
  <div v-if="isLoading" class="fixed inset-0 z-50 flex flex-col items-center justify-center">

<div class="svg-frame relative flex items-center justify-center">
	<svg style="--i:0;--j:0;">
		<g id="out1">
			<path d="M72 172C72 116.772 116.772 72 172 72C227.228 72 272 116.772 272 172C272 227.228 227.228 272 172 272C116.772 272 72 227.228 72 172ZM197.322 172C197.322 158.015 185.985 146.678 172 146.678C158.015 146.678 146.678 158.015 146.678 172C146.678 185.985 158.015 197.322 172 197.322C185.985 197.322 197.322 185.985 197.322 172Z"></path>
			<path mask="url(#path-1-inside-1_111_3212)" stroke-miterlimit="16" stroke-width="2" stroke="#00FFFF" d="M72 172C72 116.772 116.772 72 172 72C227.228 72 272 116.772 272 172C272 227.228 227.228 272 172 272C116.772 272 72 227.228 72 172ZM197.322 172C197.322 158.015 185.985 146.678 172 146.678C158.015 146.678 146.678 158.015 146.678 172C146.678 185.985 158.015 197.322 172 197.322C185.985 197.322 197.322 185.985 197.322 172Z"></path>
		</g>
	</svg>

	<svg style="--i:1;--j:1;">
		<g id="out2">
			<mask fill="white" id="path-2-inside-2_111_3212">
				<path d="M102.892 127.966C93.3733 142.905 88.9517 160.527 90.2897 178.19L94.3752 177.88C93.1041 161.1 97.3046 144.36 106.347 130.168L102.892 127.966Z"></path>
				<path d="M93.3401 194.968C98.3049 211.971 108.646 226.908 122.814 237.541L125.273 234.264C111.814 224.163 101.99 209.973 97.2731 193.819L93.3401 194.968Z"></path>
				<path d="M152.707 92.3592C140.33 95.3575 128.822 101.199 119.097 109.421L121.742 112.55C130.981 104.739 141.914 99.1897 153.672 96.3413L152.707 92.3592Z"></path>
				<path d="M253.294 161.699C255.099 175.937 253.132 190.4 247.59 203.639L243.811 202.057C249.075 189.48 250.944 175.74 249.23 162.214L253.294 161.699Z"></path>
				<path d="M172 90.0557C184.677 90.0557 197.18 92.9967 208.528 98.6474C219.875 104.298 229.757 112.505 237.396 122.621L234.126 125.09C226.869 115.479 217.481 107.683 206.701 102.315C195.921 96.9469 184.043 94.1529 172 94.1529V90.0557Z"></path>
				<path d="M244.195 133.235C246.991 138.442 249.216 143.937 250.83 149.623L246.888 150.742C245.355 145.34 243.242 140.12 240.586 135.174L244.195 133.235Z"></path>
				<path d="M234.238 225.304C223.932 237.338 210.358 246.126 195.159 250.604C179.961 255.082 163.79 255.058 148.606 250.534L149.775 246.607C164.201 250.905 179.563 250.928 194.001 246.674C208.44 242.42 221.335 234.071 231.126 222.639L234.238 225.304Z"></path>
			</mask>
			<path mask="url(#path-2-inside-2_111_3212)" fill="#00FFFF" d="M102.892 127.966L105.579 123.75L101.362 121.063L98.6752 125.28L102.892 127.966ZM90.2897 178.19L85.304 178.567L85.6817 183.553L90.6674 183.175L90.2897 178.19ZM94.3752 177.88L94.7529 182.866L99.7386 182.488L99.3609 177.503L94.3752 177.88ZM106.347 130.168L110.564 132.855L113.251 128.638L109.034 125.951L106.347 130.168ZM93.3401 194.968L91.9387 190.168L87.1391 191.569L88.5405 196.369L93.3401 194.968ZM122.814 237.541L119.813 241.54L123.812 244.541L126.813 240.542L122.814 237.541ZM125.273 234.264L129.272 237.265L132.273 233.266L128.274 230.265L125.273 234.264ZM97.2731 193.819L102.073 192.418L100.671 187.618L95.8717 189.02L97.2731 193.819ZM152.707 92.3592L157.567 91.182L156.389 86.3226L151.53 87.4998L152.707 92.3592ZM119.097 109.421L115.869 105.603L112.05 108.831L115.278 112.649L119.097 109.421ZM121.742 112.55L117.924 115.778L121.152 119.596L124.97 116.368L121.742 112.55ZM153.672 96.3413L154.849 101.201L159.708 100.023L158.531 95.1641L153.672 96.3413ZM253.294 161.699L258.255 161.07L257.626 156.11L252.666 156.738L253.294 161.699ZM247.59 203.639L245.66 208.251L250.272 210.182L252.203 205.569L247.59 203.639ZM243.811 202.057L239.198 200.126L237.268 204.739L241.88 206.669L243.811 202.057ZM249.23 162.214L248.601 157.253L243.641 157.882L244.269 162.842L249.23 162.214ZM172 90.0557V85.0557H167V90.0557H172ZM208.528 98.6474L206.299 103.123L206.299 103.123L208.528 98.6474ZM237.396 122.621L240.409 126.611L244.399 123.598L241.386 119.608L237.396 122.621ZM234.126 125.09L230.136 128.103L233.149 132.093L237.139 129.08L234.126 125.09ZM206.701 102.315L204.473 106.791L204.473 106.791L206.701 102.315ZM172 94.1529H167V99.1529H172V94.1529ZM244.195 133.235L248.601 130.87L246.235 126.465L241.83 128.83L244.195 133.235ZM250.83 149.623L252.195 154.433L257.005 153.067L255.64 148.257L250.83 149.623ZM246.888 150.742L242.078 152.107L243.444 156.917L248.254 155.552L246.888 150.742ZM240.586 135.174L238.22 130.768L233.815 133.134L236.181 137.539L240.586 135.174ZM234.238 225.304L238.036 228.556L241.288 224.759L237.491 221.506L234.238 225.304ZM195.159 250.604L196.572 255.4L196.572 255.4L195.159 250.604ZM148.606 250.534L143.814 249.107L142.386 253.899L147.178 255.326L148.606 250.534ZM149.775 246.607L151.203 241.816L146.411 240.388L144.983 245.18L149.775 246.607ZM194.001 246.674L195.415 251.47L195.415 251.47L194.001 246.674ZM231.126 222.639L234.379 218.841L230.581 215.589L227.329 219.386L231.126 222.639ZM98.6752 125.28C88.5757 141.13 83.8844 159.826 85.304 178.567L95.2754 177.812C94.0191 161.227 98.1709 144.681 107.109 130.653L98.6752 125.28ZM90.6674 183.175L94.7529 182.866L93.9976 172.895L89.912 173.204L90.6674 183.175ZM99.3609 177.503C98.1715 161.8 102.102 146.135 110.564 132.855L102.131 127.481C92.5071 142.585 88.0368 160.4 89.3895 178.258L99.3609 177.503ZM109.034 125.951L105.579 123.75L100.205 132.183L103.661 134.385L109.034 125.951ZM88.5405 196.369C93.8083 214.41 104.78 230.259 119.813 241.54L125.815 233.542C112.512 223.558 102.802 209.532 98.1397 193.566L88.5405 196.369ZM126.813 240.542L129.272 237.265L121.274 231.263L118.815 234.54L126.813 240.542ZM128.274 230.265C115.679 220.813 106.486 207.534 102.073 192.418L92.4735 195.221C97.493 212.412 107.948 227.513 122.272 238.263L128.274 230.265ZM95.8717 189.02L91.9387 190.168L94.7415 199.767L98.6745 198.619L95.8717 189.02ZM151.53 87.4998C138.398 90.681 126.188 96.8793 115.869 105.603L122.325 113.239C131.457 105.519 142.262 100.034 153.884 97.2187L151.53 87.4998ZM115.278 112.649L117.924 115.778L125.56 109.322L122.915 106.193L115.278 112.649ZM124.97 116.368C133.616 109.059 143.846 103.866 154.849 101.201L152.495 91.4818C139.981 94.5132 128.347 100.419 118.514 108.732L124.97 116.368ZM158.531 95.1641L157.567 91.182L147.848 93.5364L148.812 97.5185L158.531 95.1641ZM248.334 162.327C250.028 175.697 248.181 189.277 242.978 201.708L252.203 205.569C258.082 191.522 260.169 176.177 258.255 161.07L248.334 162.327ZM249.521 199.027L245.741 197.445L241.88 206.669L245.66 208.251L249.521 199.027ZM248.423 203.987C254.025 190.602 256.014 175.98 254.19 161.585L244.269 162.842C245.873 175.5 244.125 188.357 239.198 200.126L248.423 203.987ZM249.858 167.174L253.923 166.659L252.666 156.738L248.601 157.253L249.858 167.174ZM172 95.0557C183.903 95.0557 195.644 97.8172 206.299 103.123L210.757 94.1717C198.717 88.1761 185.45 85.0557 172 85.0557V95.0557ZM206.299 103.123C216.954 108.429 226.233 116.135 233.406 125.634L241.386 119.608C233.281 108.874 222.796 100.167 210.757 94.1717L206.299 103.123ZM234.383 118.631L231.113 121.1L237.139 129.08L240.409 126.611L234.383 118.631ZM238.116 122.077C230.393 111.849 220.403 103.552 208.93 97.8393L204.473 106.791C214.56 111.814 223.345 119.11 230.136 128.103L238.116 122.077ZM208.93 97.8393C197.458 92.1263 184.816 89.1529 172 89.1529V99.1529C183.269 99.1529 194.385 101.767 204.473 106.791L208.93 97.8393ZM177 94.1529V90.0557H167V94.1529H177ZM239.79 135.601C242.416 140.49 244.504 145.649 246.02 150.988L255.64 148.257C253.927 142.225 251.567 136.395 248.601 130.87L239.79 135.601ZM249.464 144.813L245.523 145.932L248.254 155.552L252.195 154.433L249.464 144.813ZM251.698 149.376C250.067 143.628 247.818 138.073 244.991 132.808L236.181 137.539C238.666 142.168 240.644 147.052 242.078 152.107L251.698 149.376ZM242.951 139.579L246.561 137.64L241.83 128.83L238.22 130.768L242.951 139.579ZM230.441 222.051C220.763 233.351 208.017 241.603 193.746 245.808L196.572 255.4C212.698 250.649 227.101 241.325 238.036 228.556L230.441 222.051ZM193.746 245.808C179.475 250.012 164.291 249.99 150.033 245.742L147.178 255.326C163.289 260.125 180.447 260.151 196.572 255.4L193.746 245.808ZM153.397 251.962L154.567 248.035L144.983 245.18L143.814 249.107L153.397 251.962ZM148.348 251.399C163.7 255.973 180.049 255.997 195.415 251.47L192.588 241.877C179.077 245.858 164.702 245.837 151.203 241.816L148.348 251.399ZM195.415 251.47C210.78 246.942 224.504 238.058 234.924 225.891L227.329 219.386C218.167 230.084 206.099 237.897 192.588 241.877L195.415 251.47ZM227.874 226.436L230.986 229.101L237.491 221.506L234.379 218.841L227.874 226.436Z"></path>
		</g>
	</svg>

	<svg style="--i:0;--j:2;">
		<g id="inner3">
			<path d="M195.136 135.689C188.115 131.215 179.948 128.873 171.624 128.946C163.299 129.019 155.174 131.503 148.232 136.099L148.42 136.382C155.307 131.823 163.368 129.358 171.627 129.286C179.886 129.213 187.988 131.537 194.954 135.975L195.136 135.689Z"></path>
			<path d="M195.136 208.311C188.115 212.784 179.948 215.127 171.624 215.054C163.299 214.981 155.174 212.496 148.232 207.901L148.42 207.618C155.307 212.177 163.368 214.642 171.627 214.714C179.886 214.786 187.988 212.463 194.954 208.025L195.136 208.311Z"></path>
			<path mask="url(#path-5-inside-3_111_3212)" fill="#00FFFF" d="M195.136 135.689L195.474 135.904L195.689 135.566L195.351 135.352L195.136 135.689ZM171.624 128.946L171.627 129.346L171.624 128.946ZM148.232 136.099L148.011 135.765L147.678 135.986L147.899 136.32L148.232 136.099ZM148.42 136.382L148.086 136.603L148.307 136.936L148.641 136.716L148.42 136.382ZM171.627 129.286L171.63 129.686L171.627 129.286ZM194.954 135.975L194.739 136.313L195.076 136.528L195.291 136.19L194.954 135.975ZM195.136 208.311L195.351 208.648L195.689 208.433L195.474 208.096L195.136 208.311ZM171.624 215.054L171.627 214.654L171.624 215.054ZM148.232 207.901L147.899 207.68L147.678 208.014L148.011 208.234L148.232 207.901ZM148.42 207.618L148.641 207.284L148.307 207.063L148.086 207.397L148.42 207.618ZM171.627 214.714L171.63 214.314L171.627 214.714ZM194.954 208.025L195.291 207.81L195.076 207.472L194.739 207.687L194.954 208.025ZM195.351 135.352C188.265 130.836 180.022 128.473 171.62 128.546L171.627 129.346C179.874 129.274 187.966 131.594 194.921 136.026L195.351 135.352ZM171.62 128.546C163.218 128.619 155.018 131.127 148.011 135.765L148.453 136.432C155.33 131.88 163.38 129.418 171.627 129.346L171.62 128.546ZM147.899 136.32L148.086 136.603L148.753 136.161L148.566 135.878L147.899 136.32ZM148.641 136.716C155.463 132.199 163.448 129.757 171.63 129.686L171.623 128.886C163.287 128.958 155.15 131.447 148.199 136.049L148.641 136.716ZM171.63 129.686C179.812 129.614 187.839 131.916 194.739 136.313L195.169 135.638C188.138 131.158 179.959 128.813 171.623 128.886L171.63 129.686ZM195.291 136.19L195.474 135.904L194.799 135.474L194.617 135.76L195.291 136.19ZM194.921 207.974C187.966 212.406 179.874 214.726 171.627 214.654L171.62 215.454C180.022 215.527 188.265 213.163 195.351 208.648L194.921 207.974ZM171.627 214.654C163.38 214.582 155.33 212.12 148.453 207.567L148.011 208.234C155.018 212.873 163.218 215.38 171.62 215.454L171.627 214.654ZM148.566 208.122L148.753 207.838L148.086 207.397L147.899 207.68L148.566 208.122ZM148.199 207.951C155.15 212.553 163.287 215.041 171.623 215.114L171.63 214.314C163.448 214.243 155.463 211.801 148.641 207.284L148.199 207.951ZM171.623 215.114C179.959 215.187 188.138 212.842 195.169 208.362L194.739 207.687C187.839 212.084 179.812 214.386 171.63 214.314L171.623 215.114ZM194.617 208.239L194.799 208.526L195.474 208.096L195.291 207.81L194.617 208.239Z"></path>
		</g>
		<path stroke="#00FFFF" d="M240.944 172C240.944 187.951 235.414 203.408 225.295 215.738C215.176 228.068 201.095 236.508 185.45 239.62C169.806 242.732 153.567 240.323 139.5 232.804C125.433 225.285 114.408 213.12 108.304 198.384C102.2 183.648 101.394 167.25 106.024 151.987C110.654 136.723 120.434 123.537 133.696 114.675C146.959 105.813 162.884 101.824 178.758 103.388C194.632 104.951 209.472 111.97 220.751 123.249" id="out3"></path>
	</svg>

	<svg style="--i:1;--j:3;">
		<g id="inner1">
			<path fill="#00FFFF" d="M145.949 124.51L148.554 129.259C156.575 124.859 165.672 122.804 174.806 123.331C183.94 123.858 192.741 126.944 200.203 132.236C207.665 137.529 213.488 144.815 217.004 153.261C220.521 161.707 221.59 170.972 220.09 179.997L224.108 180.665L224.102 180.699L229.537 181.607C230.521 175.715 230.594 169.708 229.753 163.795L225.628 164.381C224.987 159.867 223.775 155.429 222.005 151.179C218.097 141.795 211.628 133.699 203.337 127.818C195.045 121.937 185.266 118.508 175.118 117.923C165.302 117.357 155.525 119.474 146.83 124.037C146.535 124.192 146.241 124.349 145.949 124.51ZM224.638 164.522C224.009 160.091 222.819 155.735 221.082 151.563C217.246 142.352 210.897 134.406 202.758 128.634C194.62 122.862 185.021 119.496 175.06 118.922C165.432 118.367 155.841 120.441 147.311 124.914L148.954 127.91C156.922 123.745 165.876 121.814 174.864 122.333C184.185 122.87 193.166 126.019 200.782 131.421C208.397 136.822 214.339 144.257 217.928 152.877C221.388 161.188 222.526 170.276 221.23 179.173L224.262 179.677C224.998 174.671 225.35 169.535 224.638 164.522Z" clip-rule="evenodd" fill-rule="evenodd"></path>
			<path fill="#00FFFF" d="M139.91 220.713C134.922 217.428 130.469 213.395 126.705 208.758L130.983 205.286L130.985 205.288L134.148 202.721C141.342 211.584 151.417 217.642 162.619 219.839C173.821 222.036 185.438 220.232 195.446 214.742L198.051 219.491C197.759 219.651 197.465 219.809 197.17 219.963C186.252 225.693 173.696 227.531 161.577 225.154C154.613 223.789 148.041 221.08 142.202 217.234L139.91 220.713ZM142.752 216.399C148.483 220.174 154.934 222.833 161.769 224.173C173.658 226.504 185.977 224.704 196.689 219.087L195.046 216.09C185.035 221.323 173.531 222.998 162.427 220.82C151.323 218.643 141.303 212.747 134.01 204.122L131.182 206.5C134.451 210.376 138.515 213.607 142.752 216.399Z" clip-rule="evenodd" fill-rule="evenodd"></path>
		</g>
	</svg>

	<svg style="--i:2;--j:4;">
		<path fill="#00FFFF" d="M180.956 186.056C183.849 184.212 186.103 181.521 187.41 178.349C188.717 175.177 189.013 171.679 188.258 168.332C187.503 164.986 185.734 161.954 183.192 159.65C180.649 157.346 177.458 155.883 174.054 155.46C170.649 155.038 167.197 155.676 164.169 157.288C161.14 158.9 158.683 161.407 157.133 164.468C155.582 167.528 155.014 170.992 155.505 174.388C155.997 177.783 157.524 180.944 159.879 183.439L161.129 182.259C159.018 180.021 157.648 177.186 157.207 174.141C156.766 171.096 157.276 167.989 158.667 165.245C160.057 162.5 162.261 160.252 164.977 158.806C167.693 157.36 170.788 156.788 173.842 157.167C176.895 157.546 179.757 158.858 182.037 160.924C184.317 162.99 185.904 165.709 186.581 168.711C187.258 171.712 186.992 174.849 185.82 177.694C184.648 180.539 182.627 182.952 180.032 184.606L180.956 186.056Z" id="center1"></path>
		<path fill="#00FFFF" d="M172 166.445C175.068 166.445 177.556 168.932 177.556 172C177.556 175.068 175.068 177.556 172 177.556C168.932 177.556 166.444 175.068 166.444 172C166.444 168.932 168.932 166.445 172 166.445ZM172 177.021C174.773 177.021 177.021 174.773 177.021 172C177.021 169.227 174.773 166.979 172 166.979C169.227 166.979 166.979 169.227 166.979 172C166.979 174.773 169.227 177.021 172 177.021Z" id="center"></path>
	</svg>

</div>
    <h2 class="text-xl text-[#00e5ff] font-bold tracking-wider mt-6 animate-pulse">
    veuillez patientez...
  </h2>

  </div>
  <div v-else class="overflow-hidden flex h-screen text-body">

    <!-- Sidebar -->
  <aside :class="[
    'fixed md:static inset-y-0 left-0 z-30',
    'w-[280px] md:max-lg:w-[200px] lg:w-[300px]', /* ← Applique 200px UNIQUEMENT sur tablette */
    'bg-surface border-r border-custom flex flex-col transition-transform duration-300',
    sidebarOpen ? 'translate-x-0' : '-translate-x-full md:translate-x-0'
]">
  <!-- Logo -->
  <div class="header relative pb-4 border-b-2 border-r border-custom rounded-xl stars shrink-0 w-[280px] md:max-lg:w-[200px] lg:w-[300px]
">
    <div class="max-w-7xl pt-4">
      <div
        class="profile-container mx-auto mb-2 bg-cover bg-center h-28 w-28 sm:h-36 sm:w-36 rounded-full"
        :style="{ backgroundImage: 'url(/cv_kouli.png)' }"
      ></div>

      <h1 class="text-2xl font-semibold text-[#00e5ff] text-center">Judicael Kouli</h1>
      <div class="typewriter-line">
        <span class="text-green-900 text-center pl-5 text-xs mt-5">{{ typedText }}</span><span class="cursor"></span>
      </div>
    </div>
  </div>

  <!-- Navigation -->
  <div class="flex-1 overflow-y-auto py-6 px-4 flex flex-col gap-1">
    <a @click="switchTab('about')" :class="['nav-item', activeTab === 'about' ? 'active' : '']">
      <Icon icon="mdi:user-settings-variant" :ssr="true" width="24" />
      <span>À propos</span>
    </a>

    <a @click="switchTab('capacites')" :class="['nav-item', activeTab === 'capacites' ? 'active' : '']">
      <Icon icon="lucide:cpu" :ssr="true" width="24" />

      <span>Capacités</span>
    </a>
    <a @click="switchTab('realisations')" :class="['nav-item', activeTab === 'realisations' ? 'active' : '']">
      <Icon icon="iconamoon:certificate-badge" :ssr="true" width="24" />
      <span>Réalisations</span>
    </a>
    <a @click="switchTab('contact')" :class="['nav-item', activeTab === 'contact' ? 'active' : '']">
      <Icon icon="mynaui:telephone" :ssr="true" width="24" />
      <span>Contact</span>
    </a>
  </div>

  <!-- User Profile -->
  <div class="p-5 border-t border-custom shrink-0 bg-[var(--bg)] m-4 rounded-xl">
    <div class="flex items-center gap-3">
      <div
        class="w-10 h-10 rounded-full flex items-center justify-center font-bold text-primary-custom border-2 border-surface shadow-sm"
        style="background-color: var(--primary-light);"
      >
        JK
      </div>
    </div>
  </div>
</aside>

    <!-- Overlay mobile -->
    <div
      v-if="sidebarOpen"
      class="fixed inset-0  bg-[var(--bg)] backdrop-blur-sm z-20 md:hidden"
      @click="toggleSidebar"
    ></div>

    <main class="flex-1 flex flex-col min-w-0 bg-[var(--bg)]">

  <header class="h-[80px] bg-surface border-b border-custom flex items-center justify-between px-6 shrink-0 z-10 sticky top-0 rounded-3xl">
    <div class="flex items-center gap-4">
      <button class="btn-icon md:!hidden text-[var(--text-main)]" @click="toggleSidebar">
        <Icon icon="hugeicons:menu-03" width="26" />
      </button>
    </div>

    <div class="flex items-center gap-3 sm:gap-5">
      <!-- Theme Toggle -->
      <button class="btn-icon bg-[var(--bg)] rounded-full hover:bg-[var(--border)]" @click="toggleTheme">
        <Icon :icon="isDark? 'solar:sun-bold-duotone' : 'solar:moon-bold-duotone'" width="22" :class="isDark? 'text-[#FFC107]' : 'text-[var(--text-main)]'" />
      </button>
    </div>
  </header>

  <!-- Un seul conteneur scrollable pour tout le contenu -->
  <div class="flex-1 overflow-y-auto p-5 sm:p-8" ref="scrollArea">
    <div class="max-w-[1400px] mx-auto">

      <!-- About content -->
       <div v-show="activeTab === 'about'" class="view-fade">
        <div class="">
          <!-- From Uiverse.io by pharmacist-sabot -->
<div class="nhost-card w-full mx-auto py-12 px-4 sm:px-6 lg:py-16 lg:px-8 z-20">
  <div class="card-glow"></div>
  <div class="card-grid"></div>

  <div class="card-header">
    <div class="brand-wrapper">
      <div class="logo-container">

        <Icon icon="material-icon-theme:vscode" width="25"/>
      </div>
      <span class="brand-text">Développeur Full-Stack</span>
    </div>

    <div class="action-buttons">

      <a class="btn-icon" aria-label="View on GitHub" href="https://github.com/judicaelkouly">
        <svg
          class="icon github"
          viewBox="0 0 16 16"
          version="1.1"
          aria-hidden="true"
        >
          <path
            fill-rule="evenodd"
            d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.013 8.013 0 0016 8c0-4.42-3.58-8-8-8z"
          ></path>
        </svg>
      </a>
    </div>
  </div>

  <div class="card-body">
    <div class="repo-title ">{{ typedWel }}<span class="blinking-cursor"></span></div>

    <div class="tag-wrapper">

      <a href="mailto:judicael.kouli@epitech.eu"><span class="badge badge-ts"><Icon icon="ic:outline-email" width="25"/></span></a>
      <a href="https://www.linkedin.com/in/kouli"><span class="badge badge-ts"><Icon icon="mdi:linkedin" width="25"/></span></a>

    </div>
  </div>
</div>

    <div class=" w-full mx-auto py-12 px-4 sm:px-6 lg:py-16 lg:px-8 z-20">
        <h1 class="">
            <span class="text-xs ">Je suis </span> <br><span class="text-[#00e5ff] text-4xl md:text-6xl font-bold mb-4"> Judicael Kouli</span>
        </h1>

    </div>
</div>
        <AboutView />
       </div>


      <!-- Capacites content -->
      <div v-show="activeTab === 'capacites'" class="view-fade">
        <CapaciteView />
      </div>

      <!-- Realisations content -->
      <div v-show="activeTab === 'realisations'" class="view-fade">
        <RealisationView/>
      </div>

      <!-- Contact content -->
      <div v-show="activeTab === 'contact'" class="view-fade">
        <ContactView/>
      </div>

    </div>
  </div>
</main>
  </div>
</template>

<script setup>
import { ref, onMounted, onBeforeUnmount, nextTick } from 'vue'
import { Icon } from '@iconify/vue'
import { Chart, registerables } from 'chart.js'
import AboutView from './AboutView.vue'
import CapaciteView from './CapaciteView.vue'
import ContactView from './ContactView.vue'
import RealisationView from './RealisationView.vue'

Chart.register(...registerables)

// ─── Loader initial ──────────────────────────────────────
const isLoading = ref(true)
const LOADER_DURATION = 3500 // entre 3000 et 4000 ms

// ─── State ───────────────────────────────────────────────
const activeTab = ref('about')
const isDark = ref(false)
const sidebarOpen = ref(false)
const scrollArea = ref(null)
const chartTrenRef = ref(null)
const chartStatusRef = ref(null)

let chart1 = null
let chart2 = null

// ─── Typewriter (composable inline) ──────────────────────
function useTypewriter(phrases) {
  const text = ref('')
  let phraseIndex = 0, charIndex = 0, deleting = false, timer = null

  function type() {
    const current = phrases[phraseIndex]
    if (!deleting) {
      text.value = current.slice(0, ++charIndex)
      if (charIndex === current.length) {
        deleting = true
        timer = setTimeout(type, 2200)
        return
      }
    } else {
      text.value = current.slice(0, --charIndex)
      if (charIndex === 0) {
        deleting = false
        phraseIndex = (phraseIndex + 1) % phrases.length
      }
    }
    timer = setTimeout(type, deleting ? 28 : 52)
  }

  onMounted(() => type())
  onBeforeUnmount(() => clearTimeout(timer))
  return text
}

const typedText = useTypewriter([
  'Développeur Full-Stack Junior',
  'Concepteur d’Applications Web'
])

const typedWel = useTypewriter([
  'Bienvenue sur mon porfolio',
  'Propulsez votre présence digitale',
  'Allier stratégie métier et excellence technique',
  'Architecte de vos ambitions numériques',
  'Concevoir des produits à forte valeur ajoutée'
])

// ─── Theme ───────────────────────────────────────────────
function toggleTheme() {
  isDark.value = !isDark.value
  document.documentElement.classList.toggle('dark', isDark.value)
  localStorage.setItem('theme', isDark.value ? 'dark' : 'light')
  updateChartsTheme()
}

// ─── Sidebar ─────────────────────────────────────────────
function toggleSidebar() {
  sidebarOpen.value = !sidebarOpen.value
}

// ─── Navigation ──────────────────────────────────────────
function switchTab(tab) {
  activeTab.value = tab
  if (window.innerWidth < 768) sidebarOpen.value = false
  if (scrollArea.value) scrollArea.value.scrollTop = 0
  if (tab === 'about') {
    nextTick(() => {
      chart1?.resize()
      chart2?.resize()
    })
  }
}

// ─── Charts ──────────────────────────────────────────────
function initCharts() {
  if (!chartTrenRef.value || !chartStatusRef.value) return

  const dark        = isDark.value
  const primaryColor = dark ? '#634bea' : '#190182'
  const gridColor    = dark ? '#2A3645' : '#E9ECEF'
  const textColor    = dark ? '#94A3B8' : '#6C757D'
  const areaBgColor  = dark ? 'rgba(99,75,234,0.1)' : 'rgba(25,1,130,0.08)'
  const tooltipBg    = dark ? '#2A3645' : '#212529'

  chart1 = new Chart(chartTrenRef.value, {
    type: 'line',
    data: {
      labels: ['1 Mar', '5 Mar', '10 Mar', '15 Mar', '20 Mar', '25 Mar', '30 Mar'],
      datasets: [{
        label: 'Pendaftar Harian',
        data: [120, 190, 250, 210, 380, 420, 560],
        borderColor: primaryColor,
        backgroundColor: areaBgColor,
        borderWidth: 3,
        fill: true,
        tension: 0.4,
        pointBackgroundColor: dark ? '#1E1E1E' : '#FFFFFF',
        pointBorderColor: primaryColor,
        pointBorderWidth: 2,
        pointRadius: 4,
        pointHoverRadius: 6,
      }],
    },
    options: {
      responsive: true,
      maintainAspectRatio: false,
      layout: { padding: { top: 10 } },
      plugins: {
        legend: { display: false },
        tooltip: {
          backgroundColor: tooltipBg,
          titleColor: '#FFF',
          bodyColor: '#FFF',
          padding: 12,
          cornerRadius: 8,
          displayColors: false,
          callbacks: { label: ctx => ctx.parsed.y + ' Pendaftar Baru' },
        },
      },
      scales: {
        y: {
          beginAtZero: true,
          grid: { color: gridColor, drawBorder: false, borderDash: [5, 5] },
          ticks: { color: textColor, font: { family: "'Plus Jakarta Sans', sans-serif", size: 11 }, padding: 10 },
        },
        x: {
          grid: { display: false },
          ticks: { color: textColor, font: { family: "'Plus Jakarta Sans', sans-serif", size: 11 }, padding: 10 },
        },
      },
    },
  })

  chart2 = new Chart(chartStatusRef.value, {
    type: 'doughnut',
    data: {
      labels: ['Diterima', 'Cadangan', 'Ditolak'],
      datasets: [{
        data: [320, 80, 120],
        backgroundColor: ['#28A745', '#6F42C1', '#DC3545'],
        borderWidth: 0,
        hoverOffset: 6,
      }],
    },
    options: {
      responsive: true,
      maintainAspectRatio: false,
      cutout: '75%',
      plugins: {
        legend: { display: false },
        tooltip: {
          backgroundColor: tooltipBg,
          bodyFont: { family: "'Plus Jakarta Sans', sans-serif", size: 13 },
          padding: 12,
          cornerRadius: 8,
        },
      },
    },
  })
}

function updateChartsTheme() {
  chart1?.destroy()
  chart2?.destroy()
  chart1 = null
  chart2 = null
  nextTick(() => initCharts())
}

// ─── Lifecycle ───────────────────────────────────────────
onMounted(() => {
  // Applique le thème immédiatement (pas de flash visuel), même pendant le loader
  const saved = localStorage.getItem('theme')
  if (saved === 'dark' || (!saved && window.matchMedia('(prefers-color-scheme: dark)').matches)) {
    isDark.value = true
    document.documentElement.classList.add('dark')
  }

  // Affiche le loader pendant LOADER_DURATION, puis bascule sur l'app
  setTimeout(() => {
    isLoading.value = false
    // Les canvas des charts ne sont montés dans le DOM qu'une fois isLoading = false,
    // donc on initialise les charts juste après, au prochain tick
    nextTick(() => {
      if (chartTrenRef.value || chartStatusRef.value) {
        initCharts()
      }
    })
  }, LOADER_DURATION)
})

onBeforeUnmount(() => {
  chart1?.destroy()
  chart2?.destroy()
})
</script>


<style lang="scss">
/* ── CSS Variables ── */

@import 'https://fonts.googleapis.com/icon?family=Material+Icons';
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@200;300;400&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Playwrite+AU+VIC+Guides&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Sail&display=swap');


/*----Card presentation------*/
/* From Uiverse.io by pharmacist-sabot */
@keyframes blink {
  0%,
  100% {
    opacity: 1;
  }
  50% {
    opacity: 0;
  }
}

@keyframes grid-move {
  0% {
    background-position: 0 0;
  }
  100% {
    background-position: 30px 30px;
  }
}

@keyframes float {
  0%,
  100% {
    transform: translateY(0);
  }
  50% {
    transform: translateY(-4px);
  }
}

/* Component Styles */
.nhost-card {
  --bg-color: #0c111d;
  --card-border: #1f2937;
  --text-primary: #f3f4f6;
  --text-secondary: #9ca3af;
  --accent-color: #0052cc;
  --accent-glow: rgba(0, 82, 204, 0.35);
  --brand-gradient: linear-gradient(135deg, #0052cc, #2684ff);

  font-family: "Inter", system-ui, sans-serif;
  width: 100%;
  max-width: 400px;
  background-color: var(--bg-color);
  border: 1px solid var(--card-border);
  border-radius: 16px;
  padding: 24px;
  position: relative;
  overflow: hidden;
  box-shadow: 0 4px 24px -1px rgba(0, 0, 0, 0.2);
  transition:
    transform 0.3s cubic-bezier(0.34, 1.56, 0.64, 1),
    box-shadow 0.3s ease,
    border-color 0.3s ease;
  z-index: 1;
}

.nhost-card:hover {
  transform: translateY(-4px) scale(1.01);
  box-shadow:
    0 20px 40px -5px rgba(0, 0, 0, 0.4),
    0 0 0 1px rgba(38, 132, 255, 0.3);
  border-color: rgba(38, 132, 255, 0.5);
}

.card-grid {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-image: linear-gradient(
      rgba(255, 255, 255, 0.05) 1px,
      transparent 1px
    ),
    linear-gradient(90deg, rgba(255, 255, 255, 0.05) 1px, transparent 1px);
  background-size: 30px 30px;
  mask-image: linear-gradient(to bottom, black 40%, transparent 100%);
  pointer-events: none;
  z-index: -2;
  transition: opacity 0.5s ease;
  opacity: 0.5;
}

.nhost-card:hover .card-grid {
  animation: grid-move 20s linear infinite;
  opacity: 0.8;
}

.card-glow {
  position: absolute;
  top: -50px;
  right: -50px;
  width: 150px;
  height: 150px;
  background: radial-gradient(
    circle,
    var(--accent-glow) 0%,
    rgba(0, 0, 0, 0) 70%
  );
  filter: blur(40px);
  z-index: -1;
  transition: all 0.5s ease;
}

.nhost-card:hover .card-glow {
  transform: scale(1.5);
  background: radial-gradient(
    circle,
    rgba(38, 132, 255, 0.4) 0%,
    rgba(0, 0, 0, 0) 70%
  );
}

/* Header Section */
.card-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 24px;
}

.brand-wrapper {
  display: flex;
  align-items: center;
  gap: 12px;
}

.logo-container {
  width: 40px;
  height: 40px;
  display: flex;
  align-items: center;
  justify-content: center;
  background: rgba(255, 255, 255, 0.03);
  border-radius: 8px;
  border: 1px solid rgba(255, 255, 255, 0.1);
  transition: background 0.3s ease;
}

.nhost-logo {
  width: 24px;
  height: 24px;
  color: #fff;
  filter: drop-shadow(0 0 2px rgba(255, 255, 255, 0.3));
}

.brand-text {
  font-size: 18px;
  font-weight: 700;
  letter-spacing: 0.5px;
  color: var(--text-primary);
}

/* Actions */
.action-buttons {
  display: flex;
  gap: 8px;
}

.btn-icon {
  background: transparent;
  border: none;
  cursor: pointer;
  padding: 8px;
  border-radius: 8px;
  color: var(--text-secondary);
  transition: all 0.2s ease;
  display: flex;
  align-items: center;
  justify-content: center;
}

.btn-icon:hover {
  background: rgba(255, 255, 255, 0.1);
  color: #fff;
  transform: translateY(-2px);
}

.icon {
  width: 20px;
  height: 20px;
  fill: currentColor;
}

.icon.star {
  transition: color 0.2s;
}

.btn-icon:hover .icon.star {
  color: #fbbf24;
  filter: drop-shadow(0 0 6px rgba(251, 191, 36, 0.5));
}

/* Body Section */
.card-body {
  position: relative;
}

.repo-title {
  font-family: "JetBrains Mono", monospace;
  font-size: 20px;
  font-weight: 500;
  color: var(--accent-color);
  margin: 0 0 12px 0;
  display: flex;
  align-items: center;
}

.blinking-cursor {
  display: inline-block;
  width: 10px;
  height: 3px;
  background-color: var(--accent-color);
  margin-left: 6px;
  animation: blink 1s step-end infinite;
  box-shadow: 0 0 8px var(--accent-color);
}

.repo-description {
  font-size: 15px;
  line-height: 1.6;
  color: var(--text-secondary);
  margin: 0 0 24px 0;
}

/* Tags */
.tag-wrapper {
  display: flex;
  gap: 10px;
}

.badge {
  font-family: "JetBrains Mono", monospace;
  font-size: 12px;
  font-weight: 600;
  padding: 4px 10px;
  border-radius: 6px;
  transition: all 0.3s ease;
  cursor: default;
  position: relative;
  overflow: hidden;
}

/* JS Tag */
.badge-js {
  background-color: rgba(247, 223, 30, 0.1);
  color: #f7df1e;
  border: 1px solid rgba(247, 223, 30, 0.2);
}

.badge-js:hover {
  background-color: rgba(247, 223, 30, 0.2);
  box-shadow: 0 0 12px rgba(247, 223, 30, 0.2);
  transform: translateY(-1px);
}

/* TS Tag */
.badge-ts {
  background-color: rgba(49, 120, 198, 0.1);
  color: #3178c6;
  border: 1px solid rgba(49, 120, 198, 0.2);
}

.badge-ts:hover {
  background-color: rgba(49, 120, 198, 0.2);
  box-shadow: 0 0 12px rgba(49, 120, 198, 0.3);
  transform: translateY(-1px);
}



/* ── Loader ── */

.svg-frame {
  position: relative;
  width: 300px;
  height: 300px;
  transform-style: preserve-3d;
  display: flex;
  justify-content: center;
  align-items: center;
}

.svg-frame svg {
  position: absolute;
  transition: .5s;
  z-index: calc(1 - (0.2 * var(--j)));
  transform-origin: center;
  width: 344px;
  height: 344px;
  fill: none;
}

.svg-frame:hover svg {
  transform: rotate(-80deg) skew(30deg) translateX(calc(45px * var(--i))) translateY(calc(-35px * var(--i)));
}

.svg-frame svg #center {
  transition: .5s;
  transform-origin: center;
}

.svg-frame:hover svg #center {
  transform: rotate(-30deg) translateX(45px) translateY(-3px);
}

#out2 {
  animation: rotate16 7s ease-in-out infinite alternate;
  transform-origin: center;
}

#out3 {
  animation: rotate16 3s ease-in-out infinite alternate;
  transform-origin: center;
  stroke: #ff0;
}

#inner3,
#inner1 {
  animation: rotate16 4s ease-in-out infinite alternate;
  transform-origin: center;
}

#center1 {
  fill: #ff0;
  animation: rotate16 2s ease-in-out infinite alternate;
  transform-origin: center;
}

@keyframes rotate16 {
  to {
    transform: rotate(360deg);
  }
}
/*.loader-screen {
  position: fixed;
  inset: 0;
  z-index: 100;
  display: flex;
  align-items: center;
  justify-content: center;
  background: var(--bg);
}

.loader-content {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 1rem;
}

.loader-spinner {
  width: 48px;
  height: 48px;
  border: 3px solid var(--border);
  border-top-color: var(--cyan);
  border-radius: 50%;
  animation: loader-spin 0.8s linear infinite;
}

@keyframes loader-spin {
  to { transform: rotate(360deg); }
}

.loader-text {
  font-family: 'JetBrains Mono', monospace;
  color: var(--cyan);
  font-size: 0.9rem;
  letter-spacing: 0.1em;
  text-transform: uppercase;
}*/

 @keyframes neon-pulse {
            0%, 100% { text-shadow: 0 0 5px #fff, 0 0 10px #fff, 0 0 15px #fff, 0 0 20px #00ffff, 0 0 35px #00ffff, 0 0 40px #00ffff, 0 0 50px #00ffff, 0 0 75px #00ffff; }
            50% { text-shadow: 0 0 2px #fff, 0 0 5px #fff, 0 0 7px #fff, 0 0 10px #00ffff, 0 0 17px #00ffff, 0 0 20px #00ffff, 0 0 25px #00ffff, 0 0 37px #00ffff; }
        }
        /* Test font */
        .playwrite-au-vic-guides-regular {
          font-family: "Playwrite AU VIC Guides", cursive;
          font-weight: 400;
          font-style: normal;
        }
        .sail-regular {
          font-family: "Sail", system-ui;
          font-weight: 400;
          font-style: normal;
        }
        .neon-text {
            animation: neon-pulse 1.5s infinite alternate;
        }

         .bg-animated {
            background-size: 400% 400%;
            animation: gradient 15s ease infinite;
        }

        @keyframes gradient {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        @keyframes cyber-grid-move {
            0% { background-position: 0 0; }
            100% { background-position: 20px 20px; }
        }

        .feature-card {
            backdrop-filter: blur(10px);
            background-color: rgba(0, 0, 0, 0.1);
            border: 1px solid rgba(0, 255, 255, 0.1);
            transition: all 0.3s ease;
        }

        .feature-card:hover {
            transform: translateY(-10px) scale(1.05);
            box-shadow: 0 0 20px rgba(0, 255, 255, 0.5);
        }

        .feature-icon {
            transition: all 0.3s ease;
        }

        .feature-card:hover .feature-icon {
            transform: rotate(360deg) scale(1.2);
        }

        @keyframes float {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-20px); }
        }

        .floating {
            animation: float 6s ease-in-out infinite;
        }

        .glitch-effect {
            position: relative;
            overflow: hidden;
        }

        .glitch-effect::before,
        .glitch-effect::after {
            content: attr(data-text);
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.5);
        }

        .glitch-effect::before {
            left: 2px;
            text-shadow: -2px 0 #ff00de;
            clip: rect(24px, 550px, 90px, 0);
            animation: glitch-anim 3s infinite linear alternate-reverse;
        }

        .glitch-effect::after {
            left: -2px;
            text-shadow: -2px 0 #00ffff;
            clip: rect(85px, 550px, 140px, 0);
            animation: glitch-anim 2s infinite linear alternate-reverse;
        }

        @keyframes glitch-anim {
            0% { clip: rect(39px, 9999px, 71px, 0); }
            20% { clip: rect(3px, 9999px, 5px, 0); }
            40% { clip: rect(6px, 9999px, 38px, 0); }
            60% { clip: rect(13px, 9999px, 43px, 0); }
            80% { clip: rect(44px, 9999px, 93px, 0); }
            100% { clip: rect(54px, 9999px, 47px, 0); }
        }

@keyframes move-background {
  from {
		-webkit-transform: translate3d(0px, 0px, 0px);
	}
	to {
		-webkit-transform: translate3d(1000px, 0px, 0px);
	}
}
@-webkit-keyframes move-background {
  from {
		-webkit-transform: translate3d(0px, 0px, 0px);
	}
	to {
		-webkit-transform: translate3d(1000px, 0px, 0px);
	}
}

@-moz-keyframes move-background {
	from {
		-webkit-transform: translate3d(0px, 0px, 0px);
	}
	to {
		-webkit-transform: translate3d(1000px, 0px, 0px);
	}
}

    @-webkit-keyframes move-background {
	from {
		-webkit-transform: translate3d(0px, 0px, 0px);
	}
	to {
		-webkit-transform: translate3d(1000px, 0px, 0px);
	}
}

.stars {
 background: url(https://s3-us-west-2.amazonaws.com/s.cdpn.io/1231630/stars.png) repeat;

}

.hr-text {
  line-height: 1em;
  position: relative;
  outline: 0;
  border: 0;
  color: black;
  text-align: center;
  height: 1.5em;
  opacity: 0.5;
}
.hr-text:before {
  content: "";
  background: linear-gradient(to right, transparent, #818078, transparent);
  position: absolute;
  left: 0;
  top: 50%;
  width: 100%;
  height: 1px;
}
.hr-text:after {
  content: attr(data-content);
  position: relative;
  display: inline-block;
  color: black;
  padding: 0 0.5em;
  line-height: 1.5em;
  color: #818078;
  background-color: #fcfcfa;
}


 /* HERO */
  .hero {
    padding: 7rem 2rem 5rem;
    max-width: 900px;
    margin: 0 auto;
  }

  .hero-eyebrow {
    font-family: var(--font-mono);
    font-size: 12px;
    color: var(--accent);
    letter-spacing: 0.12em;
    text-transform: uppercase;
    margin-bottom: 1.5rem;
    display: flex;
    align-items: center;
    gap: 8px;
  }

  .hero-eyebrow::before {
    content: '';
    display: inline-block;
    width: 24px;
    height: 1px;
    background: var(--accent);
  }

  .hero-title {
    font-family: var(--font-display);
    font-size: clamp(2.4rem, 5vw, 3.8rem);
    font-weight: 700;
    line-height: 1.1;
    letter-spacing: -0.02em;
    margin-bottom: 1.5rem;
  }

  .hero-title .name { display: block; color: var(--text); }
  .hero-title .role { display: block; color: var(--muted); font-weight: 400; }

  .typewriter-line {
    font-family: var(--font-mono);
    font-size: clamp(1rem, 2.5vw, 1.4rem);
    color: var(--accent);
    display: flex;
    align-items: center;
    gap: 2px;
    margin-bottom: 2rem;
    min-height: 2rem;
  }

  .cursor {
    display: inline-block;
    width: 2px;
    height: 1.2em;
    background: var(--accent);
    animation: blink 1s step-end infinite;
    vertical-align: middle;
  }

  @keyframes blink { 50% { opacity: 0; } }

  .hero-desc {
    color: var(--muted);
    font-size: 15px;
    max-width: 540px;
    line-height: 1.8;
    margin-bottom: 2.5rem;
  }

  .hero-cta { display: flex; gap: 1rem; flex-wrap: wrap; }

  .btn-primary {
    font-family: var(--font-display);
    font-size: 13px;
    font-weight: 500;
    letter-spacing: 0.04em;
    padding: 10px 24px;
    background: var(--accent);
    color: #0A0A0F;
    border: none;
    border-radius: 4px;
    cursor: pointer;
    transition: background 0.2s, transform 0.15s;
    text-decoration: none;
    display: inline-block;
  }

  .btn-primary:hover { background: #6FFFD4; transform: translateY(-1px); }

  .btn-secondary {
    font-family: var(--font-display);
    font-size: 13px;
    font-weight: 500;
    letter-spacing: 0.04em;
    padding: 10px 24px;
    background: transparent;
    color: var(--text);
    border: 1px solid var(--border);
    border-radius: 4px;
    cursor: pointer;
    transition: border-color 0.2s, transform 0.15s;
    text-decoration: none;
    display: inline-block;
  }

  .btn-secondary:hover { border-color: rgba(255,255,255,0.25); transform: translateY(-1px); }

:root {
  --cyan:#00e5ff;
  --primary: #190182;
  --primary-dark: #12015c;
  --primary-light: rgba(25, 1, 130, 0.08);
  --bg: #080d28;
  --surface: #FFFFFF;
  --text-main: #FFFFFF;
  --text-secondary: #FFFFFF;
  --text-tertiary: #FFFFFF;
  --border: rgba(0,229,255,0.18);
  --border-light: #F1F3F5;
  --success: #28A745;
  --success-light: rgba(40, 167, 69, 0.12);
  --danger: #DC3545;
  --danger-light: rgba(220, 53, 69, 0.12);
  --warning: #FFC107;
  --warning-dark: #D39E00;
  --warning-light: rgba(255, 193, 7, 0.15);
  --info: #17A2B8;
  --info-light: rgba(23, 162, 184, 0.12);
  --purple: #6F42C1;
  --purple-light: rgba(111, 66, 193, 0.12);
  --shadow-sm: 0 2px 4px rgba(25,1,130,0.02), 0 4px 12px rgba(25,1,130,0.04);
  --shadow-md: 0 4px 12px rgba(25,1,130,0.05), 0 12px 24px rgba(25,1,130,0.08);
}
.dark {
  --primary: #634bea;
  --primary-dark: #190182;
  --primary-light: rgba(99, 75, 234, 0.15);
  --bg: #121212;
  --surface: #1E1E1E;
  --text-main: #F8FAFC;
  --text-secondary: #CBD5E1;
  --text-tertiary: #94A3B8;
  --border: #334155;
  --border-light: #2A3645;
  --warning-dark: #FFC107;
  --shadow-sm: 0 4px 6px -1px rgba(0,0,0,0.4);
  --shadow-md: 0 10px 20px -5px rgba(0,0,0,0.5);
}

body {
  font-family: 'Plus Jakarta Sans', sans-serif;
  background-color: var(--bg);
  color: var(--text-secondary);
  transition: background-color 0.3s, color 0.3s;
}
.font-mono { font-family: 'JetBrains Mono', monospace; }

h3 { font-size: 1.25rem; font-weight: 700; color: var(--cyan); }
h4 { font-size: 1.125rem; font-weight: 600; color: var(--text-main); }
.text-body { font-size: 0.9375rem; font-weight: 400; color: var(--text-secondary); line-height: 1.6; }
.text-caption { font-size: 0.75rem; font-weight: 600; text-transform: uppercase; letter-spacing: 0.05em; color: var(--text-tertiary); }
.text-data { font-size: 1.5rem; font-weight: 700; color: var(--text-main); font-family: 'JetBrains Mono', monospace; line-height: 1.2; }

.card-panel {
  background-color: var(--surface);
  border-radius: 16px;
  box-shadow: var(--shadow-sm);
  border: 1px solid var(--border-light);
  transition: box-shadow 0.3s ease, transform 0.3s ease;
}
.card-panel:hover { box-shadow: var(--shadow-md); }

.stat-card {
  background-color: var(--surface);
  border-left: 4px solid var(--primary);
  border-right: 1px solid var(--border-light);
  border-top: 1px solid var(--border-light);
  border-bottom: 1px solid var(--border-light);
  border-radius: 12px;
  padding: 16px 20px;
  box-shadow: var(--shadow-sm);
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  min-height: 110px;
  transition: transform 0.2s;
}
.stat-card:hover { transform: translateY(-2px); box-shadow: var(--shadow-md); }

.btn-primary {
  background-color: var(--primary);
  color: #FFF;
  padding: 8px 18px;
  border-radius: 8px;
  font-weight: 600;
  font-size: 0.875rem;
  transition: all 0.2s;
  border: none;
  cursor: pointer;
  display: inline-flex; align-items: center; justify-content: center; gap: 8px;
}
.btn-primary:hover { background-color: var(--primary-dark); transform: translateY(-1px); }

.btn-outline {
  border: 1px solid var(--border);
  color: var(--text-main);
  background: var(--surface);
  padding: 8px 18px;
  border-radius: 8px;
  font-weight: 600;
  font-size: 0.875rem;
  transition: all 0.2s;
  cursor: pointer;
  display: inline-flex; align-items: center; justify-content: center; gap: 8px;
}
.btn-outline:hover { background-color: var(--bg); border-color: var(--text-tertiary); }

.btn-icon {
  width: 36px; height: 36px;
  border-radius: 8px;
  display: inline-flex; justify-content: center; align-items: center;
  transition: all 0.2s;
  color: var(--text-tertiary);
  background: transparent;
  border: none;
  cursor: pointer;
}
.btn-icon:hover { background-color: var(--primary-light); color: var(--primary); }

.badge {
  padding: 4px 10px;
  border-radius: 6px;
  font-size: 0.75rem;
  font-weight: 600;
  display: inline-flex; align-items: center; gap: 6px;
  letter-spacing: 0.02em;
}
.badge-success { background-color: var(--success-light); color: var(--success); }
.badge-warning { background-color: var(--warning-light); color: var(--warning-dark); }
.badge-danger  { background-color: var(--danger-light);  color: var(--danger); }
.badge-info    { background-color: var(--info-light);    color: var(--info); }
.badge-purple  { background-color: var(--purple-light);  color: var(--purple); }

.input-solid {
  background-color: var(--bg);
  border: 1px solid var(--border);
  color: var(--text-main);
  border-radius: 8px;
  padding: 10px 16px;
  width: 100%;
  font-size: 0.875rem;
  font-weight: 500;
  transition: all 0.2s;
  font-family: inherit;
}
.input-solid:focus {
  outline: none;
  border-color: var(--primary);
  background-color: var(--surface);
  box-shadow: 0 0 0 3px var(--primary-light);
}

.table-custom { width: 100%; border-collapse: separate; border-spacing: 0; }
.table-custom th {
  background-color: var(--bg);
  color: var(--text-tertiary);
  font-weight: 600;
  font-size: 0.75rem;
  text-transform: uppercase;
  letter-spacing: 0.05em;
  padding: 14px 20px;
  text-align: left;
  border-bottom: 1px solid var(--border);
}
.table-custom td {
  padding: 16px 20px;
  border-bottom: 1px solid var(--border-light);
  color: var(--text-secondary);
  font-size: 0.875rem;
  vertical-align: middle;
  transition: background-color 0.2s;
}
.table-custom tbody tr:hover td { background-color: var(--primary-light); }
.table-custom tbody tr:last-child td { border-bottom: none; }

.nav-item {
  display: flex; align-items: center; gap: 14px;
  padding: 12px 18px;
  color: var(--text-secondary);
  border-radius: 10px;
  margin-bottom: 4px;
  font-weight: 600;
  font-size: 0.9375rem;
  transition: all 0.2s;
  cursor: pointer;
  text-decoration: none;
}
.nav-item:hover { background-color: var(--primary-light); color: var(--primary); }
.nav-item.active { background-color: var(--primary); color: #FFF; box-shadow: 0 4px 12px var(--primary-light); }

.timeline-item { position: relative; padding-left: 28px; padding-bottom: 20px; }
.timeline-item::before {
  content: ''; position: absolute; left: 7px; top: 4px; bottom: 0;
  width: 2px; background-color: var(--border);
}
.timeline-item:last-child::before { display: none; }
.timeline-dot {
  position: absolute; left: 0; top: 4px;
  width: 16px; height: 16px;
  border-radius: 50%;
  background-color: var(--primary);
  border: 3px solid var(--surface);
  z-index: 1;
}


.text-primary-custom { color: var(--primary); }
.border-custom { border-color: var(--border); }

/* View fade animation */
.view-fade { animation: fadeIn 0.35s cubic-bezier(0.4, 0, 0.2, 1) forwards; }
@keyframes fadeIn { from { opacity: 0; transform: translateY(8px); } to { opacity: 1; transform: translateY(0); } }

::-webkit-scrollbar { width: 6px; height: 6px; }
::-webkit-scrollbar-track { background: transparent; }
::-webkit-scrollbar-thumb { background: var(--text-tertiary); border-radius: 10px; }
::-webkit-scrollbar-thumb:hover { background: var(--primary); }
</style>
