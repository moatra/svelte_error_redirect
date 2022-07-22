<script context="module">
    export const load = function ({ url, status}) {
        if (status === 401) {
            return {
                redirect: `/login?from=${encodeURIComponent(url.pathname + url.search)}`,
                status: 302,
            };
        }
        return {
            props: {
                status_code: status,
            },
        };
    };
</script>
<script>
    export let status_code;
</script>

<h3>{status_code} Error Page</h3>