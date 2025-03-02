# hems-osgi-backend



Run: brew install openjdk@17 (install Homebrew first with /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)" if needed).


For the system Java wrappers to find this JDK, symlink it with
  sudo ln -sfn /opt/homebrew/opt/openjdk@17/libexec/openjdk.jdk /Library/Java/JavaVirtualMachines/openjdk-17.jdk

openjdk@17 is keg-only, which means it was not symlinked into /opt/homebrew,
because this is an alternate version of another formula.

If you need to have openjdk@17 first in your PATH, run:
  echo 'export PATH="/opt/homebrew/opt/openjdk@17/bin:$PATH"' >> /Users/mme/.zshrc

For compilers to find openjdk@17 you may need to set:
  export CPPFLAGS="-I/opt/homebrew/opt/openjdk@17/include"


mvn archetype:generate -DarchetypeArtifactId=maven-archetype-quickstart -DgroupId=com.hems -DartifactId=modbus-bundle -Dversion=1.0-SNAPSHOT -DinteractiveMode=false

mvn clean install