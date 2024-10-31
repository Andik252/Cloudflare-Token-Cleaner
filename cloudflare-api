const axios = require('axios');

const email = 'Isi Email'; // Ganti dengan email akun Cloudflare kamu
const apiKey = 'Isi Token'; // Ganti dengan Global API Key Cloudflare kamu
const exceptions = ['Isi Nama']; // Token yang tidak akan dihapus jika ada

const deleteApiToken = async (tokenId) => {
    try {
        await axios.delete(`https://api.cloudflare.com/client/v4/user/tokens/${tokenId}`, {
            headers: {
                'X-Auth-Email': email,
                'X-Auth-Key': apiKey,
                'Content-Type': 'application/json',
            },
        });
        console.log(`Deleted token ID: ${tokenId}`);
    } catch (error) {
        console.error(`Failed to delete token ID: ${tokenId}`, error.response.data);
    }
};

const fetchAndDeleteTokens = async () => {
    try {
        const response = await axios.get('https://api.cloudflare.com/client/v4/user/tokens', {
            headers: {
                'X-Auth-Email': email,
                'X-Auth-Key': apiKey,
                'Content-Type': 'application/json',
            },
        });

        const tokens = response.data.result;
        if (tokens.length === 0) {
            console.log('No API tokens found.');
            return;
        }

        for (const token of tokens) {
            if (!exceptions.includes(token.name)) {
                await deleteApiToken(token.id);
            } else {
                console.log(`Skipped token: ${token.name}`);
            }
        }
    } catch (error) {
        console.error('Error fetching API tokens:', error.response.data);
    }
};

fetchAndDeleteTokens();
