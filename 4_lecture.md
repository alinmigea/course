# 4. Агляд Action Controller. REST. HTTP

## Першыя вынікі працы

Мы ўжо шмат чаго зрабілі цягам першых заняткаў:

* пазнаёміліся з інструментамі распрацоўкі;
* навучыліся працаваць з сістэмай кантроля версій ;
* навучыліся кіраваць Ruby-бібліятэкамі з дапамогай Bundler;
* даведаліся, як уладкавана Rails application;
* пазнаёміліся з архітэктурай MVC і іншымі патэрнамі распрацоўкі;
* стварылі Rails прыкладанне
* папрактыкаваліся ў працы з статычнымі web-старонкамі
* і нават разгарнулі прыкладанне ў production

Дзякуючы таму, што наш курс - гэта не толькі набор канспектаў на Github, але і
непасрэдны кантакт на [лекцыях](http://vk.com/rubyway), я магу зрабіць пэўныя
высновы і рэкамендацыі для студэнтаў ужо на гэтым этапе. Нейкія рэкамендацыі ўжо
даваліся раней, але практыка паказвае, што варта звярнуць на іх асаблівую увагу зноў.

#### Памылкі

Звяртайце увагу на паведамленні памылак (server log, старонка з памылкай у
development mode, памылкі у тэрмінале). Гэтыя паведамленні - ключ да разумення
праблем вашага прыкладання і часцей за ўсё з іх можна выцягнуць усю неабходную
інфармацыю для вырашэння праблемы. З цягам часу вы таксама навучыцеся працаваць
з Rails кансолью, метадамі дэбагінга і JavaScript кансолью. Падрабязней пра
адладку Rails прыкладанняў можна пазнаёміцца на
[Rails Guides](http://guides.rubyonrails.org/debugging_rails_applications.html).

#### Пошук інфармацыі

На значную колькасць пытанняў ад студэнтаў можна было знайсці адказ па першых жа
спасылках ў Google. Гэта значыць, што такія пытанні можна вырашыць *самастойна*
без прафесійнай экспертызы. З іншага боку, самастойнасць - гэта і ёсць адна з
галоўных прыкмет прафесіяналізма. І, каб стаць прафесіяналам, трэба вучыцца
працаваць самастойна. Першым крокам да гэтага можа стаць пісменны падыход да
пошука інфармацыі. Калі вы шукаеце інфармацыю пра памылку, спачатку прааналізуйце
яе. Ці спецыфічна яна менавіта да вашага прыкладання, ці да бібліятэк, якія вы
выкарыстоўваеце, ці да версій бібліятэк? Пры якіх умовах адбываецца памылка? Калі
вы зразумееце саму праблему, тады значна прасцей будзе знайсці інфармацыю пра яе
вырашэнне ці чотка сфармуляваць яе, каб атрымаць адказ на
[Stack Overflow](http://stackoverflow.com/).

З вопытам вы заўважыце, што добрае разуменне праблемы і добрае бачанне агульнай
сутнасці працы web-прыкладанняў дапаможа вам хутка знаходзіць адказы і шляхі
вырашэнняў нават у тых тэхналогіях, з якімі не даводзілася раней працаваць.

#### Падыход да вучобы

Курс разлічаны ў тым ліку на людзей без бэкграўнду у web-тэхналогіях. Але, як
высветлілася, такія студэнты чамусці менш працуюць. Магчыма, студэнты-навічкі не
разумеюць спецыфікі працы ў IT. Справа ў тым, што web-тэхналогіі вельмі імкліва
развіваюцца. І, каб не страціць кампетэнцыі, канкурэнтаздольнасць і досвед, нават
вопытныя распрацоўшчыкі павінны пастаянна вучыцца і працаваць з новымі тэхналогіямі.
Я ужо не кажу пра навічкоў, якія проста абавязаны вучыцца, чытаць і практыкавацца
*кожны* дзень. Прафессія Software Engineer абавязвае чалавека пастаянна развівацца.
Варта гэта зразумець з самага пачатку.

#### Дакументацыя і codestyle

Сучаснае web-прыкладанне ствараецца з дапамогай цэлага ансамбля інструментаў на
стыку вялікай колькасці тэхналогій. І, каб эфектыўна выкарыстоўваць гэтыя
інструменты і тэхналогіі, трэба чытаць дакументацыю і вывучаць API. Не грэбуйце
дакументацыяй, бо добрая арыентацыя ў прадмеце вашай працы дазволіць вам
сэканоміць шмат часу.

Іншае пытанне - дакументацыя і стыль кода вашага прыкладання. Калі вы працуеце ў
камандзе ці публікуеце прыкладанне для code-review, важна напісаць хаця б README
і інструкцыі па выконванню сецыфічных каманд. Таксама важна пісаць каменты у
кодзе, асабліва ў кодзе з высокай ступеню абстракцыі. Назвы метадаў, кантроллераў
і г.д павінны казаць самі за сябе. Важна, таксама, рабіць інфарматыўныя
паведамленні камітаў, каб прасцей было знайсці пэўныя змяненні. Пачытайце добрыя
рэкамендацыі [Rails Style Guide](https://github.com/bbatsov/rails-style-guide).

Мы не выпадкова зрабілі прамежкавыя вынікі. Зараз мы пераходзім да другога этапа
нашага курса - пабудовы дынамічнага web-прыкладання. Гэта значыць, што мы будзем
працаваць з дадзенымі з дапамогай Ruby DSL і падрабязней пазнаёмімся з магутнымі
магчымасцямі Rails і лаканічнасцю мовы Ruby.

## Падрабязней пра кантроллеры

Падмурак Rails-прыкладанняў - гэта Action Pack. Ён складаецца з трох Ruby-модуляў:
Action Dispatch, Action Controller і Action View. Action Dispatch займаецца маршрутызацыяй
знешніх запытаў да кантроллераў. Action Controller пераўтварае запыты ў адказы.
Action Controller можа выкарыстоўваць  Action View для фармавання гэтых адказаў.

На прыкладзе нашага прыкладання гэта рэалізуецца такім чынам: мы робім запыт, напрыклад */*.
Action Dispatcher накіроўвае гэты знешні запыт да дзеяння *home* кантроллера Pages.
Action Controller вяртае нам візуалізаванае з дапамогай Action View прадстаўленне
файла **app/views/pages/home.html.erb**.

#### Наследаванне кантроллераў

Звярніце увагу на радок `class PagesController < ApplicationController` у нашым
Pages кантроллеры. Такі запіс азначае, што Ruby клас *PagesController*
ўспадкоўваецца ад класа *ApplicationController*. Паглядзіце файл Application кантроллера:

    # app/controllers/application_controller.rb
    class ApplicationController < ActionController::Base
      protect_from_forgery with: :exception
    end

Тут мы бачым, што *ApplicationController* ўспадкоўваецца ад
*ActionController::Base* - гэта базавы клас кантроллераў Rails. Такім чынам,
метады і правілы з класа *ActionController::Base* дасяжныя для *ApplicationController*.
У сваю чаргу метады *ApplicationController* дасяжныя ў нашым Pages кантроллеры
(і ў кантроллеры Testimonials, які мы створым неўзабаве). Больш за тое, яны
дасяжныя ў actions нашага кантроллера. Нават калі гэтыя дзеянні пустыя. Калі мы
наведваем старонку */course*, Rails накіроўвае наш запыт да дзеяння *course*
Pages кантроллера, пасля гэтага рэндэрыцца View для гэтага дзеяння ў выглядзе
старонкі **app/views/pages/home.html.erb**. Rails ведае, што трэба аддаць
менавіта гэтую старонку, дзякуючы пагаджэнням іменавання кантроллераў і файлаў,
а таксама размяшчэнню іх ў адпаведных каталогах. Кантроллеры прынята называць ў
множным ліку: *PagesController*. Файлы кантроллераў прынята іменаваць у фармаце
*snake_case*: **app/controllers/pages_controller.rb**. Views павінны ляжаць у
адпаведным каталогу: **app/views/pages/**. Калі следаваць гэтым пагаджэнням, то
Rails-прыкладанне само знойдзе патрэбныя файлы і метады, без дадатковай
канфігурацыі. Гэта і ёсць падыход *Convention over configuration* у дзеянні.

Іншы прыклад наследавання: метад `protect_from_forgery`, які абараняе прыкладанне
ад CSRF-атак. І на кожнай старонцы, якая мае форму з інпутамі і належыць да
actions кантроллера Pages інпуты аўтаматычна атрымаюць *authenticity_token*,
які ўскладняе задачу злачынцам атакаваць наша прыкладанне. Падрабязней можна
пачытаць у [артыкуле](http://blog.nvisium.com/2014/09/understanding-protectfromforgery.html).

Насдедаванне - адзін з галоўных прынцыпаў Аб'ектна-Арыенаванага Праграмавання.
Мы абавязкова вернемся да гэтага пытання ў будучыні.

#### RESTful кантроллеры

Давайце зробім магчымасць дадаваць водгукі на сайце. Відавочна, што старонкі
водгукаў павінны быць дынамічнымі, бо прадугледжваецца праца з дадзенымі і
ўзаемадзеянне з кліентам. Таму, варта стварыць асобны кантроллер Testimonials.
Водгук - гэта рэсурс. Рэсурс - гэта ключавы панятак ў REST-архітэктуры.

[REpresentational State Transfer](http://en.wikipedia.org/wiki/Representational_state_transfer) -
гэта архітэктурны стыль для стварэння web-прыкладанняў. Пры праектаванні
Rails-прыкладанняў прынята мадэляваць значную колькасць рэсурсаў
(напрыклад, водгукі у нашым прыкладанні) з магчымасцю стварэння, чытання,
абнаўлення і выдалення. Гэтыя аперацыі (Create, Read, Update і  Destroy)
адпавядаюць аперацыям CRUD рэляцыйных баз дадзеных і чатыром галоўным HTTP
метадам (пра іх даведаемся ніжэй).

RESTful стыль дапамагае вызначыцца, якія дзеянні дадаваць у кантроллер. На
прыкладзе рэсурса водгукаў лёгка зразумець, што з дапамогай гэтых дзеянняў мы
можам стварыць рэсурс (напісаць водгук), прачытаць рэсурс (убачыць водгук),
абнавіць рэсурс (змяніць тэкст водгука) і выдаліць рэсурс (водгук).

Зараз мы створым рэсурс Testimonial, выкарыстоўваючы скафолд (мы генеруем не
толькі кантроллер, але і мадэль з міграцыямі базы дадзеных і шмат чаго яшчэ).
Гэта проста дэманстрацыя магчымасцяў Rails, таму, пакуль не будзем падрабязна
спыняцца на змесціве файлаў.

    $ rails generate scaffold Testimonial user:string feedback:text

Каб усё працавала, трэба выканаць міграцыю базы дадзеных:

    $ rake db:migrate

Калі перайсці на старонку */testimonials/new*, мы убачым форму для дадання водгука.
Праз гэтую форму можна стварыць водгук, які будзе бачны  па адрасе */testimonials/1*.
Можна адразу адрэдагаваць гэты водгук: */testimonials/1/edit*. Увесь спіс водгукаў
будзе бачны тут */testimonials*. З гэтай жа старонкі можна выдаліць водгукі.

Як гэта ўсё працуе? Паглядзіце Testimonials кантроллер, які мы толькі што згенеравалі.
Там ёсць наступныя дзеянні: *index, show, new, edit, create, update, destroy*
(можна пакуль не звяртаць увагу на код гэтых дзеянняў). Усе гэтыя дзеянні
характэрны для рэсурса. Але, мы бачым (**app/views/pages/testimonials/**), што
не для кожнага дзеяння ёсць адпаведнае прадстаўленне, а толькі для чатырох: *index, show, new, edit*.

Давайце разбярэмся, што робяць гэтыя дзеянні.

* *index* вяртае спіс нашых рэсурсаў (водгукаў)
* *new* стварае рэсурс і перадае яго кліенту (у выглядзе формы для запаўнення)
* *create* стварае новы водгук (з дадзенымі формы) і захоўвае яго
* *show* паказвае нам кантрэтны водгук
* *update* абнаўляе водгук
* *edit* дазваляе адрэдагаваць водгук у форме
* *destroy* выдаляе водгук

Мы атрымліваем доступ да рэсурсаў праз выкарыстанне URL. REST
адрознівае змест рэсурсаў ад прадстаўлення зместа. REST падтрымлівае высокую
маштабаванасць падчас апрацўкі дадзеных і дазваляе захоўваць натуральныя сувязі
у прыкладанні. Але Rails не робіць жорсткіх абмежаванняў у выкарыстанні гэтага
стылю (напрыклад у Pages кантроллеры такі падыход быў бы недарэчны).

## HTTP

Адкуль бяруцца маршруты для дзеянняў Testimonials кантроллера? Калі паглядзець
файл маршрутаў, то можна убачыць такі радок  `resources :testimonials`. Давайце
праверым, якія маршруты стварае гэты метад:

    $ rake routes

![REST routes](https://github.com/micrum/course/blob/master/assets/rest-routes.png)

Мы бачым, што сямі нашым дзеянням адпавядае чатыры URL. Гэта значыць, што аднаму
і таму ж URL (напрыклад */testimonials/1*) можа адпавядаць адразу 3 дзеяння:
*show, update і destroy*. І толькі адно з іх мае прадстаўленне -
**app/views/testimonials/pages/show.html.erb**. Як такое магчыма? Справа ў тым,
што аднолькавым URI могуць адпавядаць розныя метады HTTP. *show* дзеянню
адпавядае GET метад, *update* - PATCH (альбо PUT), *destroy* - DELETE. Звярніце
увагу, што толькі дзеянні з GET метадамі маюць прадстаўленні. Справа ў тым, што
з дапамогай GET метада можна толькі прачытаць дадзеныя з сервера (то бок, атрымаць старонку).

[Hyper Text Transfer Protocol](http://en.wikipedia.org/wiki/Hypertext_Transfer_Protocol)
вызначае 4 асноўныя аперацыі: GET (атрымаць), POST (адправіць), PATCH (выправіць)
і DELETE (выдвліць). Браўзеры ўзаемадзейнічаюць з Rails, калі робяць запыт па URL,
выкарыстоўваючы адзін з HTTP метадаў (GET, POST, PATCH, PUT і DELETE). Кожны метад
прыводзіць да пэўнай аперацыі з нашым рэсурсам (у дадзеным выпадку гэта водгук).
Рэсурсны маршрут `resources :testimonials` злучае метады HTTP і URL з дзеяннямі
ў адным кантроллеры (Testimonials). GET - самая распаўсюджаная аперацыя. З яе
дапамогай можна проста атрымаць старонку. GET маршруты мы дадавалі ў Router для
дзеянняў Pages кантроллера. Каб атрымаць статычную старонку (напрыклад */course*),
браўзер дасылае менавіта GET запыт. З дапамогай POST аперацыі мы можам пакласці
дадзеныя на сервер (стварыць водгук праз *create* дзеянне з дадзенымі запоўненай
формы. PATCH і DELETE аперацыі абнаўляюць ці выдаляюць рэсурсы на серверы
(*update і destroy* дзеянні Testimonials кантроллера). Дзеянні адпавядаюць не
толькі HTTP запытам і URL, але і запытам да рэляцыйнай базы дадзеных (CRUD).
Маршрутызацыя Rails адлюстроўвае URL-адрасы на дзеянні праз сам ідэнтыфікатар URI,
а таксама праз HTTP-метад запыта.

## Працягваем распрацоўку

Мы стварылі рэсурс водгукаў з дапамогай скафолда. Выкарыстоўвайце scaffold
толькі калі дакладна ведаеце будучую структуру прыкладання і разумееце, што
кожны згенераваны файл вам спатрэбіцца. Злоўжыванне генератарамі прыводзіць да
з'яўлення "мёртвага" кода і ускладнення падтрымкі прыкладання. Таму, на гэты раз
створым кантроллер ўручную. Але спачатку трэба адкаціць базу дадзеных:

    $ rake db:rollback

Зараз можна выдаліць згенераваны код:

    $ rails destroy scaffold Testimonial

Магчыма, нейкія файлы давядзецца выдаліць уручную. Пасля гэтага проста стварыце
файл кантроллера з адным дзеяннем index:

    # app/controllers/testimonials_controller.rb
    class TestimonialsController < ApplicationController
      def index
      end
    end

Дзеянне `testimonials` зараз можна выдаліць з кантроллера Pages. Таксама варта
перамясціць Testimonials view у асобны каталог, каб не парушаць пагаджэнні Rails:

    # app/views/testimonials/index.html.erb
    <div class="page-header">
        <h1>Testimonials</h1>
    </div>

Засталося толькі абнавіць маршруты, каб атрымаць нашую старонку ад новага
кантроллера. Для гэтага выдалім стары маршрут `get 'testimonials' => 'pages#testimonials'`
і дададзім рэсурсны маршрут:

    # config/routes.rb
    resources :testimonials

Але мы зараз маем толькі адзін экшн, таму трэба абмяжаваць маршруты гэтым дзеяннем:

    # config/routes.rb
    resources :testimonials, only: [:index]

Зараз наша старонка Testimonials (**app/views/testimonials/index.html.erb**)
суадносіцца з *index* дзеяннем кантроллера Testimonials. Пасля таго, як Router
вызначае, што для апрацоўкі запыта */testimonials* трэба выкарыстоўваць
Testimonials кантроллер, гэты кантроллер апрацоўвае гэты запыт, адрасуе яго
*index* дзеянню і вяртае адказ у выглядзе View. Гэта значыць, што кантроллер
накіроўвае знешнія запыты ўнутраным дзеянням.

[<< папярэдні занятак](3_lecture.md)
[наступны занятак >>](5_lecture.md)