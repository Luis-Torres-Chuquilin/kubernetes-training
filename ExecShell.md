<!-- @format -->

# Acces to Shell in the Pod

k exec -ti <podName> -- <pathToShell>

k exec -ti blue -- /bin/sh -> This case will be an error, because the image does not has the shell, it is for a size email and protection

k exec -ti nginx -- /bin/sh

We can write commands in the shell -> ls , curl localhost

We can update the package, to have wget ->
apt update
apt install wget

<!-- Information about wget https://www.labnol.org/software/wget-command-examples/28750/ -->

[debianDistribution]
