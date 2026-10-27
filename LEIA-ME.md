# ZoneFy APK

## Jeito fácil (sem instalar nada) - GitHub Actions
1. Crie um repositório no GitHub e suba TODO o conteúdo desta pasta (inclusive a pasta .github).
2. Vá na aba Actions, abra "Build APK" e clique em Run workflow (ou só faça o push).
3. Quando terminar (uns 4-6 min), baixe o artefato ZoneFy-apk, extraia e instale o app-debug.apk no celular.

## Jeito local (precisa de Node 20, JDK 17 e Android SDK)
npm install && npx cap add android && npx cap sync android
cd android && ./gradlew assembleDebug
APK em android/app/build/outputs/apk/debug/app-debug.apk

Para mudar o app, edite www/index.html. O plugin CapacitorHttp já está ligado, então não há problema de CORS no celular.
