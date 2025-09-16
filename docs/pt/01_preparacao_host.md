# Passo 2: Iniciar o Serviço de Virtualização

Com as ferramentas instaladas, precisamos ligar o "motor" delas. O serviço `libvirtd` é o daemon (processo de fundo) que gerencia as VMs, redes e armazenamentos virtuais. Sem ele, o `virt-manager` não tem a quem se conectar.

# Passo 3: Conceder Permissões ao Criador

Por padrão, apenas o usuário `root` pode gerenciar VMs. Para facilitar o processo e seguir boas práticas de segurança, adicionamos nosso usuário normal aos grupos de controle. Isso nos dá o poder de criar, deletar e gerenciar VMs sem precisar ser o superusuário para cada clique.

**Atenção**: É crucial fazer logout e login novamente na sua sessão do *Sistema Operacional* após este passo. Sem isso, o sistema não reconhecerá suas novas permissões.

# Passo 4: Obter a "Semente" do Ouroboros

Precisamos da matéria-prima, a partir do qual os **nós** do nosso cluster serão criados. Faremos o download da imagem de instalação do **Rocky Linux 9**.

Acesse o site oficial de downloads: ![OS](https://img.shields.io/badge/Guest_OS-Rocky_Linux_9-green?style=for-the-badge&logo=rockylinux)

Baixe a imagem Minimal da ISO do Rocky Linux 9 para a arquitetura x86_64 (escolha sua arquitetura). A imagem "Minimal" é a escolha profissional para servidores, pois contém apenas o sistema operacional essencial, sem interfaces gráficas ou pacotes desnecessários. Isso resulta em VMs mais leves, seguras e com uma superfície de ataque menor.

Com o ambiente preparado e a semente em mãos, estamos prontos para iniciar a criação.
