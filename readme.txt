traefik --configFile=traefik.yml --api.dashboard.entrypoints=dashboard




७ — گواهی محلی (mkcert توصیه میشه)
گزینه الف) استفاده از mkcert (راحت و بدون هشدار در مرورگر)

پیشنهاد می‌کنم از mkcert استفاده کنی چون در macOS مرورگرها هشدار نمیدن.

نصب mkcert:

brew install mkcert
mkcert -install
mkcert localhost laravel.test
# خروجی: localhost+1-key.pem localhost+1.pem
# rename them:
mv localhost+1.pem traefik/certs/localhost.crt
mv localhost+1-key.pem traefik/certs/localhost.key




/etc/hosts اضافه کن

برای دسترسی به laravel.test لوکالی:

ویرایش کن /etc/hosts و خط زیر اضافه کن (با دسترسی sudo):

127.0.0.1 laravel.test


