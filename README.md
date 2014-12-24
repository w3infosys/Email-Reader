Email Reader Library
===================================
It is a codeigniter email library to check connection, count and read emails from mailbox and it’s contents, specially this library is designed to get attachments from emails and check attachment types etc.

This is a basic version of email reader.
@package 	Codeignitor, IMAP
@author 	Kakesh Narayan Pradhan
@since 	1.0

Class Name: Email_Reader
Properties: 
$success, $error, $connection, $server, $username, $password, $ctype, $port, $inbox, $message_count, $attachment_type, $attachment_folder, $checks

Methods:
__construct()
mail_connect()
list_mailboxes() // get all mailboxes available in the mail server
check_mailbox() // 
switch_mailbox() // reopen mailbox other than inbox using same connection
get_mailbox_detail() // check current mailbox details like total message
read_mailbox($mailbox = 'INBOX', $search = null, $check = array()) // default inbox
count_emails($type = 'all') // count total messages or recent messages in the current mailbox
get_email_detail($message_id = null)
move_email($message_id, $folder='INBOX.Processed') // message index no and the folder to which the message needs to move
set_attachment_type($type = array()) // it will merge the default attachment type array
is_valid_attachment($filename)
check_attachment($message_id)
get_attachments($message_id)
save_attachment($attachment, $filename)
get_errors($type = 'all')
check_connection()
mail_close()
