<div>
  <h1>User info</h1>
  <p><%= attachment_image_tag @user, :profile_image, :fill, 100, 100, format: 'jpeg', fallback: "no_image.jpg" %></p>
  <h3>name</h3>
    <%= @user.name %>
  <h3>introduction</h3>
    <%= @user.introduction %>
  <% if @user.id == current_user.id %>
    <p><%= link_to "プロフィール編集", edit_user_path(@user) %></p>
  <% end %>
</div>

<h1>New book</h1>
<%= form_with model: @book, local:true do |f| %>
<h4>Title</h4>
<%= f.text_field :title %>
<h4>Opinion</h4>
<%= f.text_field :body %>
  <p><%= f.submit 'Create Book' %></p>
<% end %>

新規投稿画面の部分テンプレート
使用ファイル一覧
book: index,show
user: index,show