#[Capybara](https://github.com/jnicklas/capybara)

Capybara 是个 Ruby gem，可以模拟用户在浏览器中的交互动作，方便 Rails 等应用程序进行集成测试。可以与 Cucumber 和 RSpec 很好的结合使用。

##用法

###和 Cucumber 一起使用
[cucumber-rails][cr] 集成了对 Capybara 的支持，按照常规执行以下命令即可：

```bash
rails generate cucumber:install
```

###和 RSpec 一起使用

将以下代码添加到 `spec/spec_helper.rb`：

```ruby
require 'capybara/rspec'
```

##Capybara API/DSL

```ruby
# 访问
visit '/home'
visit root_path

# 当前地址
current_path.should == root_path

# 点击链接、按钮
click_link 'id-of-link'
click_link 'Link Text'
click_button 'Save'
click_on 'Link Text' # 点击链接或按钮
click_on 'Button Value'

# 表格交互
fill_in 'First Name', :with => 'John'
fill_in 'Password', :with => 'passwd'
fill_in 'Description', :with => 'Really Long Text...'
choose('A Radio Button')
check('A Checkbox')
uncheck('A Checkbox')
attach_file('Image', '/path/to/image.jpg')
select('Option', :from => 'Select Box')

#查询
page.has_selector?('table tr')
page.has_selector?(:xpath, '//table/tr')
page.has_no_selector?(:content)
page.has_xpath?('//table/tr')
page.has_css?('table tr.foo')
page.has_content?('foo')

#查找
find_field('First Name').value
find_link('Hello').visible?
find_button('Send').click
find(:xpath, "//table/tr").click
find("#overlay").find("h1").click
all('a').each { |a| a[:href] }

find('#navigation').click_link('Home')
find('#navigation').should have_button('Sign out')

#作用域
#  作用在找到的第一个元素上
within("li#employee") do
  fill_in 'Name', :with => 'Jimmy'
end

within(:xpath, "//li[@id='employee']") do
  fill_in 'Name', :with => 'Jimmy'
end

within_fieldset('Employee') do
  fill_in 'Name', :with => 'Jimmy'
end

within_table('Employee') do
  fill_in 'Name', :with => 'Jimmy'
end

#执行脚本
#  在特定的 driver 中可用
page.execute_script("$('body').empty()")
result = page.evaluate_script('4 + 4');

#Debug
save_and_open_page
```

[cc]:https://github.com/cucumber/cucumber "Cucumber"
[cr]:https://github.com/cucumber/cucumber-rails "cucumber-rails"
