# Artemis
Artemis leaked get rekt lmfao. Coming out at 30 github stars. 

Update: wasnt expecting it to be so fast. gimme 1 week to clean up the mess i made

Update 2: Lmfaooooooo this dumfuc thinks its fake bro i dumped classes from ur source why you capping so hard

## Proof:

ac/artemis/anticheat/engine/v2/EngineInjector.java
```java
package ac.artemis.anticheat.engine.v2;

import ac.artemis.core.inject.Injectable;
import ac.artemis.core.v4.Artemis;
import ac.artemis.core.v4.utils.chat.Chat;
import ac.artemis.core.v5.emulator.Emulator;
import ac.artemis.core.v5.emulator.EmulatorManager;


public class EngineInjector implements Injectable {
    @Override
    public void begin() {
        Chat.sendConsoleMessage("&r[&a✓&r] &aHooking into Predictions 2.0!");
        final EmulatorProvider provider = new EmulatorManager.EmulatorProvider()
                        .setNames("v2", "version2", "modern", "upgraded")
                        .setFactory(new EmulatorManager.EmulatorFactory() {
                            @Override
                            public Emulator build() {
                                assert data != null : "PlayerData cannot be null! (0x03-A)";
                                return new ArtemisData(data);
                            }
                        }
        );
        Artemis.INSTANCE.getApi().getEmulatorManager().inject(provider);
    }

    @Override
    public void end() {
      // Do nothing
    }
}
```

![Proof](https://i.imgur.com/yzJcTPm.png)

