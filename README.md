# Base_Flutter

assets : 
         - fonts
         - icons
         - jsons: config data
lib: 
     - base:
             + presenter: Tất cả các màn hình đều phải có class presenter và đc kế ừa từ base
             + contract: abstract (void updateState();)
             + const: config toàn bộ app
             + utils: methob đc xử dụng nhiều
             + data_store: singleton (dùng cho project nhỏ và có tính cục bộ)
             + api_client: Tất cả các api_client dùng để giao tiếp hay xử lý data và đc kế thừa từ base
     - model
     - core: 
             + api: các methob request (get, post, put, del)
             + api_config: config các api host
     - helper
     - pages: cái view màn chính ( chi tiết screens)
     - screens: MVP
              + bloc (khi xử lý, update dữ liệu phức tạp)
              + model
              + views: nhiều view nhỏ thì tạo folder
              * example:
                        1. login_view: chỉ có view ko có biến
                        2. login_presenter: các biến + phương thức
                        3. login_api_client: xử lý request api
              * Lưu ý: 
                       1. Hàm ko đc viết trong view bao gồm cả builder item
                       2. item phải viết class riêng
                       3. Hạn chế tối đa việc tách class ko cần thiết
                       4. Tóm lại k có hàm hoặc biến bên view
     - views: các view chung cho nếu trùng nhau
     - main.dart
