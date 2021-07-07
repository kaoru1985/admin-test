<template>
    <div>
        <Header />
        <div class="content_wrapper">
            <Sidebar />
            <Nuxt />
        </div>
    </div>
</template>
<style>
    button.green {
        color: #fff;
        background-color: #00cd81;
        border: none;
        border-radius: 20px;
        padding: .5rem 2rem;
    }
    button:disabled {
        background-color: #B1CCC2;
    }
    button:hover {
        opacity: .8;
    }
    .content_wrapper {
        display: flex;
    }
</style>
