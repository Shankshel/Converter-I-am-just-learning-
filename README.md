# Converter (# I am just learning)

# Write currency converter rubles-dollars: program,
# that asks a course, then asks the user,
# how many rubles he has, and then gives the result in dollars

puts "# converter"

currency = [
	"рубли",
	"доллары",
	"евро"
]

puts "Соотношение каких валют Вы хотите узнать?
1. рубль к доллару
2. рубль к евро
3. доллар к рублю
4. евро к рублю"

currency_ratio = [
	"рубль к доллару",
	"рубль к евро",
	"доллар к рублю",
	"евро к рублю",
] 

puts

user = gets.to_i

puts

if user == '' || user <= 0 || user > 4
	user = 1
end

arr = ""
arr << currency_ratio[user - 1].split.join(', ')

if arr[0] == "р" && arr[-1] == "у"
	puts "Вы хотите узнать соотношение рубля к доллару?"
	print "Введите пожалуйста сегодняшний курс доллара: "
	dol = gets.to_f
	print "Какая сумма в рублях у Вас на руках? "
	rub = gets.to_f
	puts "Благодарю!"
	sleep 2
	puts "Считаю... считаю..."
	sleep 3
	puts "Эм..."
	sleep 4
	puts "Вы еще тут? Простите за столь длительное ожидание... Я посчитал, у Вас сейчас #{(rub / dol).round(2)} $"
elsif arr[0] == "р" && arr[-1] == "о"
	puts "Вы хотите узнать соотношение рубля к евро?"
	print "Введите пожалуйста сегодняшний курс евро: "
	eur = gets.to_f
	print "Какая сумма в рублях у Вас на руках? "
	rub = gets.to_f
	puts "Благодарю!"
	sleep 2
	puts "Считаю... считаю... считаю..."
	sleep 3
	puts "Эм... Вроде, что-то похожее на доллар... но... О, да!"
	sleep 4
	puts "Вы еще тут? Простите за столь длительное ожидание... Я посчитал, у Вас сейчас #{(rub / eur).round(2)} евро"
elsif arr[0] == "д" && arr[-1] == "ю"
	puts "Вы хотите узнать соотношение доллара к рублю?"
	print "Введите пожалуйста сегодняшний курс рубля: "
	dol = gets.to_f
	print "Какая сумма в долларах у Вас на руках? "
	rub = gets.to_f
	puts "Благодарю! Эту валюту считать почему-то мне проще =)"
	puts "Я посчитал, у Вас сейчас #{(dol * rub).round(2)} руб"
elsif arr[0] == "е" && arr[-1] == "ю"
	puts "Вы хотите узнать соотношение евро к рублю?"
	print "Введите пожалуйста сегодняшний курс рубля: "
	eur = gets.to_f
	print "Какая сумма в евро у Вас на руках? "
	rub = gets.to_f
	puts "Благодарю! Эту валюту считать почему-то мне проще =)"
	puts "Я посчитал, у Вас сейчас #{(eur * rub).round(2)} руб"
end
