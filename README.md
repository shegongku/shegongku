source table
{
  type              = mysql
  sql_host          = localhost
  sql_user          = username
  sql_pass          = password
  sql_db            = sgk
  sql_port          = 3306
  sql_query_pre     = SET NAMES utf8
  sql_query         = SELECT id,name,pwd FROM table
  sql_query_info    = SELECT * FROM table WHERE id=$id
}
index table
{
  source            = table
  path              = /home/sphinx/table/
  docinfo           = none
  mlock             = 0
  morphology        = none
  min_word_len      = 1
  html_strip        = 0
  ngram_len         = 1
  min_infix_len     = 1
  enable_star       = 1
  ondisk_dict       = 1
  charset_type      = utf-8
  ngram_chars = U+3000..U+2FA1F
}
