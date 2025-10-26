traefik --configFile=traefik.yml --api.dashboard.entrypoints=dashboard




७ — گواهی محلی (mkcert توصیه میشه)
گزینه الف) استفاده از mkcert (راحت و بدون هشدار در مرورگر)

پیشنهاد می‌کنم از mkcert استفاده کنی چون در macOS مرورگرها هشدار نمیدن.

نصب mkcert:

brew install mkcert
mkcert -install
mkcert laravel.localhost


laravel.localhost.pem        # گواهی
laravel.localhost-key.pem    # کلید خصوصی





/etc/hosts اضافه کن

برای دسترسی به laravel.localhost لوکالی:

ویرایش کن /etc/hosts و خط زیر اضافه کن (با دسترسی sudo):

127.0.0.1 laravel.localhost




