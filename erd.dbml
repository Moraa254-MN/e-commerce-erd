Table product {
  product_id int [pk, increment]
  name varchar
  brand_id int [ref: > brand.brand_id]
  category_id int [ref: > product_category.category_id]
  base_price decimal
  description text
}

Table brand {
  brand_id int [pk, increment]
  name varchar
  description text
}

Table product_category {
  category_id int [pk, increment]
  name varchar
  description text
}

Table product_image {
  image_id int [pk, increment]
  product_id int [ref: > product.product_id]
  image_url varchar
  alt_text varchar
}

Table color {
  color_id int [pk, increment]
  name varchar
  hex_value varchar
}

Table size_category {
  size_category_id int [pk, increment]
  name varchar
}

Table size_option {
  size_id int [pk, increment]
  size_category_id int [ref: > size_category.size_category_id]
  label varchar
}

Table product_variation {
  variation_id int [pk, increment]
  product_id int [ref: > product.product_id]
  color_id int [ref: > color.color_id]
  size_id int [ref: > size_option.size_id]
}

Table product_item {
  item_id int [pk, increment]
  variation_id int [ref: > product_variation.variation_id]
  sku varchar
  stock_quantity int
  price_override decimal
}

Table attribute_type {
  type_id int [pk, increment]
  name varchar
}

Table attribute_category {
  attribute_category_id int [pk, increment]
  name varchar
}

Table product_attribute {
  attribute_id int [pk, increment]
  product_id int [ref: > product.product_id]
  name varchar
  value varchar
  type_id int [ref: > attribute_type.type_id]
  category_id int [ref: > attribute_category.attribute_category_id]
}
