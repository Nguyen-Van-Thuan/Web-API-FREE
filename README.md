# Các trang web có API miễn phí

Dưới đây là danh sách các trang web có API miễn phí để sử dụng trong các dự án của bạn:

1. [OpenWeatherMap API](https://openweathermap.org/api) - API để truy xuất dữ liệu thời tiết
2. [The Movie Database (TMDb) API](https://www.themoviedb.org/documentation/api) - API để truy xuất dữ liệu phim và chương trình truyền hình
3. [NASA Open APIs](https://api.nasa.gov/) - API để truy xuất dữ liệu về vũ trụ, khoa học và giáo dục
4. [Google Maps Platform API](https://developers.google.com/maps/documentation) - API để truy xuất dữ liệu bản đồ và địa điểm
5. [Twitter API](https://developer.twitter.com/en/docs) - API để truy xuất dữ liệu và thực hiện các thao tác trên trang web Twitter.
6. [Facebook API](https://developers.facebook.com/docs/apis-and-sdks) - API để truy xuất dữ liệu và thực hiện các thao tác trên trang web Facebook.
7. [YouTube API](https://developers.google.com/youtube/v3) - API để truy xuất dữ liệu và thực hiện các thao tác trên trang web YouTube.
8. [SoundCloud API](https://developers.soundcloud.com/docs/api/reference) - API để truy xuất dữ liệu và thực hiện các thao tác trên trang web SoundCloud.
9. [Spotify API](https://developer.spotify.com/documentation/web-api/) - API để truy xuất dữ liệu và thực hiện các thao tác trên trang web Spotify.
10. [GitHub API](https://docs.github.com/en/rest) - API để truy xuất dữ liệu và thực hiện các thao tác trên trang web GitHub.
11. [Stripe API](https://stripe.com/docs/api) - API để thực hiện các thao tác thanh toán trực tuyến.
12. [Twilio API](https://www.twilio.com/docs/usage/api) - API để thực hiện các thao tác gửi tin nhắn SMS và điện thoại.
13. [Mailchimp API](https://mailchimp.com/developer/) - API để thực hiện các thao tác quản lý email marketing.
14. [Google Translate API](https://developers.google.com/translate) - API để thực hiện các thao tác dịch văn bản.
15. [Bing Maps API](https://www.microsoft.com/en-us/maps/choose-your-bing-maps-api) - API để truy xuất dữ liệu bản đồ và địa điểm.
16. [Reddit API](https://www.reddit.com/dev/api/) - API để truy xuất dữ liệu và thực hiện các thao tác trên trang web Reddit.
17. [OpenAI API](https://beta.openai.com/docs/api-reference) - API để sử dụng các công cụ trí tuệ nhân tạo từ OpenAI.
18. [CoinGecko API](https://www.coingecko.com/api/documentations/v3) - API để truy xuất thông tin về tiền điện tử và thị trường.
19. [OpenFoodFacts API](https://world.openfoodfacts.org/data) - API để truy xuất thông tin về các sản phẩm thực phẩm trên toàn thế giới.
20. [Wikipedia API](https://www.mediawiki.org/wiki/API:Main_page) - API để truy xuất dữ liệu từ trang web Wikipedia.
21. [PokéAPI](https://pokeapi.co/) - API để truy xuất thông tin về các loài Pokémon.
22. [RandomUser API](https://randomuser.me/documentation) - API để tạo ra dữ liệu người dùng giả định.
23. [JokeAPI](https://sv443.net/jokeapi/v2/) - API để lấy ra các câu chuyện cười và truyện ngắn.
24. [Covid19APIs](https://covid19api.com/) - API để truy xuất thông tin về dịch bệnh Covid-19.
25. [Open Exchange Rates API](https://openexchangerates.org/) - API để truy xuất thông tin về tỷ giá hối đoái.

## Cách sử dụng

Để sử dụng một API, truy cập vào trang web của API đó để đăng ký và lấy API Key. Sau đó, thực hiện các cuộc gọi API từ mã bằng cách sử dụng các thư viện API hoặc giao thức HTTP.

Ví dụ về sử dụng API với axios:

```axios
const axios = require('axios');

// Tạo một request để truy xuất người dùng ứng với ID cho sẵn:
axios.get('/user?ID=12345')
  .then(function (response) {
    // xử trí khi thành công
    console.log(response);
  })
  .catch(function (error) {
    // xử trí khi bị lỗi
    console.log(error);
  })
  .finally(function () {
    // luôn luôn được thực thi
  });

// Cái request bên trên cũng có thể được làm bằng cách sau, tùy ý
axios.get('/user', {
    params: {
      ID: 12345
    }
  })
  .then(function (response) {
    console.log(response);
  })
  .catch(function (error) {
    console.log(error);
  })
  .finally(function () {
    // luôn luôn được thực thi
  });  

// Nếu muốn sử dụng async/await thì viết như sau
async function getUser() {
  try {
    const response = await axios.get('/user?ID=12345');
    console.log(response);
  } catch (error) {
    console.error(error);
  }
}