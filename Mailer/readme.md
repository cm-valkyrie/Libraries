# Mailer para Valkyrie Platform

### Use

Copy the repository to the libraries folder.
You can use in controller or model.

	$mail = new Mailer(true);
	try {
		// Recipients
		$mail->setFrom('EMAIL FROM', 'Mailer');
		$mail->addAddress('EMAIL TO', 'Joe User'); // Add a recipient

		// Content
		$mail->Subject = 'Here is the subject';
		$mail->Body    = 'This is the HTML message body <b>in bold!</b>';
		$mail->AltBody = 'This is the body in plain text for non-HTML mail clients';

		$mail->send();
		echo 'Message has been sent';
	} catch (Exception $e) {
		echo "Message could not be sent. Mailer Error: {$mail->ErrorInfo}";
	}

### End
