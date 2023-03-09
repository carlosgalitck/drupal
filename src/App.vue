<script>
import { Buffer } from 'buffer';

export const restConfig = {
    headers: {
        'Content-Type': 'application/json',
        'X-CSRF-Token': '1tGwx9lOVnalvErUZeC750a2uOMzeLGhSASnkz9goXc',
        'Authorization': 'Basic ' + Buffer.from('usuariodemo:usuariodemo', 'utf8').toString('base64'),
    },
    params: {
        '_format': 'json',
    }
};

export const siteDomain = 'http://localhost:8001'

export default {
    name: 'App',
}

</script>