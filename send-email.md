# SendEmail Wordpress, Ajax & PHPMailer!

Simples código para envio de mensagens via formulários em temas Wordpress, utilizando Ajax para captação e validação de dados e PHPMailer para envio do e-mail.


# Instalação

A instalação é muito simples:

 1. Adicione o seguinte código no rodapé (**footer.php**) do site: <br>
  `<script src="http://ajax.aspnetcdn.com/ajax/jquery.validate/1.11.1/jquery.validate.min.js"></script>` <br>
	`<?php bs_SetJS(array('js/contact-form-script.js')) ?>`

 2. Adicione o seguinte código no `style.css` principal do template: <br>
	 3. ` #form-result {
    width: 100%;
    margin-top: 15px;
    clear: both;
}
form label.error {
    color: #fe403f !important;
    font-size: 0.93333rem;
    font-weight: normal;
    margin: 5px 0 0 0;
}
#form-result.alert-success,
#form-result.alert-error {
    width: 100%;
    color: #fff;
    padding: 5px 10px;
    font-size: 16px;
    text-align: center;
    display: none;
}
@media (max-width: 767px) {
    #form-result .alert-success,
    #form-result .alert-error {
        font-size: 15px;
    }
}
#form-result.alert-success {
    background-color: #4fd050;
    border-left: 5px solid #4fd050;
    margin-bottom: 5px;
}
#form-result.alert-error {
    background-color: #fe403f;
    border-left: 5px solid #fe403f;
}`

 3. Adicione o seguinte atributo à tag do botão de envio do formulário: <br>
  `<button ... data-loading-text="Aguarde..." ...></button`
  
 4. Sincronize cada formulário `<form id="contact-form" ...>`e seus campos `<input name="name" id="name" ... >` com o arquivo `js/contact-form-script.js`:

 5. Configure o arquivo de envio `//dominio/api/email/envio-email.php` com as informações STMP dos e-mails.

 6.  E é isso.
