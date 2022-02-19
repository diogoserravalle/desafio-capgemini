# desafio-capgemini

Desafio 1 de criação da escada

Scanner entrada = new Scanner(System.in);
List<String> degraus = new ArrayList<>();

 

System.out.print("Digite a quantidade de vezes: ");
int qtdDegraus = entrada.nextInt();

 

for (int i = 0; i < qtdDegraus; i++) {
degraus.add(" ".repeat(qtdDegraus - i) + "*".repeat(i + 1));
}

 

for (String d : degraus ) {
System.out.println(d);
}

______________________________________________________________________
                                                 
 Desafio 2 de criação da senha
                                                 
   public static boolean validaSenha(String senha) {

        String regex = "^(?=.*[0-9])"
                + "(?=.*[a-z])(?=.*[A-Z])"
                + "(?=.*[!@#$%^&*()-+])"
                + "(?=\\S+$).{6}$";

        Pattern p = Pattern.compile(regex);


        if (senha == null) {
            return false;
        }



        Matcher m = p.matcher(senha);

        return m.matches();
    }

    public static void main(String[] args) {

        Scanner scanner = new Scanner(System.in);

        System.out.println("Nome");
        String nome = scanner.next();
        System.out.println("Senha");
        String senha = scanner.next();



        System.out.println(validaSenha(senha));
    }


}
