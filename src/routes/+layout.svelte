<nav>
    <div class="nav-container">
        <a href="/" class="nav-logo" title="Back to Homepage">Maxim Spiridonov</a>
        <div class="nav-links">
            {#each nav as link}
            {#if link.isShow}
            <a href={link.href} class="link">{link.title}</a>
            {/if}
            {/each}
        </div>
    </div>
</nav>
<div class="container">
    <!-- Pages will be injected below -->
    <slot></slot>
</div>
<script>
    const nav = [
    {
    title: 'Обо мне',
    isShow: true,
    href: '/about'
    },
    {
    title: 'Блог',
    isShow: true,
    href: '/blog'
    },
    {
    title: 'Портфолио',
    isShow: true,
    href: '/project'
    },
    {
    title: 'Контакты',
    isShow: true,
    href: '/contact'
    },
    {
    title: 'temp',
    isShow: false,
    href: '/temp'
    }
    ]
    </script>
<style>
    .container {
    max-width: 1400px;
    margin: 50px auto;
    }
</style>