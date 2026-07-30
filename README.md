# GoldDrop - Сайт для открытия кейсов standoff 2 открывай-заробатывай-выводи

Полнофункциональный сайт для открытия кейсов CS:GO с авторизацией через Steam, системой платежей и админ-панелью.

## 🚀 Функционал

### Основные возможности:
- ✅ Авторизация через Steam
- ✅ Пополнение баланса (карты, СБП, криптовалюта)
- ✅ Вывод скинов через Steam
- ✅ Открытие кейсов (обычное и быстрое)
- ✅ Live-лента и топ-дроп на главной
- ✅ Апгрейды и контракты
- ✅ Бонусы: промокоды, розыгрыши
- ✅ Реферальная программа (до 30%)
- ✅ VIP-система + кешбэк (1–5%)
- ✅ Инвентарь: продажа, вывод, апгрейд
- ✅ Адаптивный дизайн для мобильных устройств

### Админ-панель:
- ✅ Управление кейсами и шансами
- ✅ Управление пользователями
- ✅ Финансовая статистика
- ✅ Управление бонусами и промокодами
- ✅ Логи действий

## 🛠 Технологический стек

- **Frontend**: Next.js 14 + TypeScript + Tailwind CSS
- **Backend**: Next.js API Routes + Prisma ORM
- **База данных**: PostgreSQL
- **Аутентификация**: NextAuth.js + Steam OpenID
- **Платежи**: Юмани API + СБП
- **Хостинг**: Vercel (бесплатно)

## 📦 Установка

1. **Клонируйте репозиторий:**
```bash
git clone https://github.com/yourusername/casecsgo.git
cd casecsgo
```

2. **Установите зависимости:**
```bash
npm install
```

3. **Настройте переменные окружения:**
```bash
cp env.example .env.local
```

Заполните `.env.local`:
```env
# Database
DATABASE_URL="postgresql://username:password@localhost:5432/casecsgo"

# NextAuth
NEXTAUTH_URL="http://localhost:3000"
NEXTAUTH_SECRET="your-secret-key-here"

# Steam API
STEAM_API_KEY="your-steam-api-key"

# Payment Systems
YUMAONEY_SHOP_ID="your-yumoney-shop-id"
YUMAONEY_SECRET_KEY="your-yumoney-secret"

# SBP
SBP_MERCHANT_ID="your-sbp-merchant-id"
SBP_SECRET_KEY="your-sbp-secret"

# Admin
ADMIN_STEAM_ID="your-steam-id-for-admin-access"
```

4. **Настройте базу данных:**
```bash
# Создайте базу данных PostgreSQL
createdb casecsgo

# Примените миграции
npx prisma db push

# Заполните тестовыми данными
npm run db:seed
```

5. **Запустите проект:**
```bash
npm run dev
```

Откройте [http://localhost:3000](http://localhost:3000) в браузере.

## 🔧 Получение Steam API ключа

1. Перейдите на [Steam Web API](https://steamcommunity.com/dev/apikey)
2. Войдите в свой Steam аккаунт
3. Введите домен (например: `localhost:3000`)
4. Скопируйте полученный ключ в `.env.local`

## 💳 Настройка платежей

### Юмани:
1. Зарегистрируйтесь на [Юмани](https://yoomoney.ru/)
2. Создайте магазин
3. Получите Shop ID и Secret Key

### СБП:
1. Обратитесь в банк для подключения СБП
2. Получите Merchant ID и Secret Key

## 🎮 Тестовые данные

После запуска `npm run db:seed` будут созданы:
- 2 тестовых кейса с 10 предметами каждый
- 3 промокода для тестирования
- RTP настроен на 85%

## 📱 Адаптивность

Сайт полностью адаптивен и работает на:
- 📱 Мобильных устройствах
- 📱 Планшетах
- 💻 Десктопах
- 🖥 Больших экранах

## 🚀 Деплой на Vercel

1. **Подключите GitHub репозиторий к Vercel**
2. **Настройте переменные окружения в Vercel:**
   - `DATABASE_URL` - ссылка на PostgreSQL (например, от Supabase)
   - `NEXTAUTH_SECRET` - случайная строка
   - `STEAM_API_KEY` - ваш Steam API ключ
   - Остальные переменные для платежей

3. **Деплой произойдет автоматически**

## 🔒 Безопасность

- Все транзакции защищены
- Steam OpenID для безопасной авторизации
- Валидация всех входных данных
- Защита от CSRF атак
- Логирование всех действий

## 📊 RTP (Return to Player)

- **RTP: 85%** - один из самых высоких показателей
- Прозрачные алгоритмы генерации
- Все шансы видны пользователям
- Аудит кода доступен

## 🤝 Поддержка

Если у вас есть вопросы или проблемы:
- Создайте Issue в GitHub
- Напишите в Telegram: @yourusername
- Email: support@casecsgo.com

## 📄 Лицензия

MIT License - используйте свободно для коммерческих и некоммерческих проектов.

## 🎯 Roadmap

- [ ] Интеграция с криптовалютами
- [ ] Мобильное приложение
- [ ] Турниры и соревнования
- [ ] Система достижений
- [ ] API для партнеров

---

**Сделано с ❤️ для сообщества CS:GO**