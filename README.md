# Conectando Nodejs com MongoDB

No projeto de NodeJS, precisamos de uma biblioteca que consegue falar com o MongoDB.

É muito comum ver tutoriais na internet que utilizam o Mongoose.

Porém, o Mongoose não é a implementação oficial do MongoDB, e sim o próprio driver chamado MongoDB.

Mongoose tem algumas validações de schema e um certo padrão para construir as collections.

Exemplo de query para criação de registro:

await mensagens.insertOne(mensagem);
Exemplo de query para visualização de registros:

await collection.find().toArray()
Exemplo de query para visualizar apenas um registro:

await mensagens.findOne({ _id: ObjectId(id) });
Exemplo de query para atualização de registros:

await mensagens.updateOne(
    { _id: ObjectId(id) },
    { $set: mensagem }
);
Exemplo de query para remoção de registros:

await mensagens.deleteOne({ _id: ObjectId(id) });