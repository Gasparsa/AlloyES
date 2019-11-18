sig Usuario {
	submissoes: set Submissao,
	amigos: set Usuario
}

sig Submissao {
	arquivo: one Arquivo,
	questao: one Questao
}

sig Arquivo { }

sig Questao { }

// Todo arquivo deve fazer parte de exatamente uma submissao
fact arquivoSubmissao {
	all a: Arquivo | one s : Submissao | a in s.arquivo
}

// Toda submissao deve ter sido enviada por exatamente um usuario
fact submissaoUsuario {
	all s: Submissao | one u : Usuario | s in u.submissoes
}

// Nenhum usuario pode ser amigo dele mesmo
fact amigoRecursivo {
	all u: Usuario | u not in u.amigos
}
