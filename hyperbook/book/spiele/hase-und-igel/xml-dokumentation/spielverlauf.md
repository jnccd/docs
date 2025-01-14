# Spielverlauf

Der Server startet (StandardIp: localhost 13050).

Nun gibt es zwei Varianten ein Spiel zu starten, eine durch einen
Administratorclient die andere durch hinzufügen der Spieler zu einen
Spieltyp:

## Variante 1 (AdminClient [???](#mit-reservierungscode))

Ein Client registriert sich als Administrator mit dem in
server.properties festgelegten Passwort p:

    <protocol><authenticate passphrase="p"/>

Dann kann ein Spiel angelegt werden:

    <prepare gameType="swc_2018_hase_und_igel">
      <slot displayName="p1" canTimeout="false" shouldBePaused="true"/>
      <slot displayName="p2" canTimeout="false" shouldBePaused="true"/>
    </prepare>

Der Server antwortet darauf mit einer Nachricht, die die ROOM\_ID und
Reservierungscodes für die beiden Clients enthält:

    <protocol>
      <prepared roomId="871faccb-5190-4e44-82fc-6cdcbb493726">
        <reservation>RC1</reservation>
        <reservation>RC2</reservation>
      </prepared>

Der Administratorclient kann nur ebenfalls als Observer des Spiels
genutzt werden, indem ein entsprechender Request gesendet wird. Dadurch
wird das derzeitge Spielfeld ([???](#memento)) ebenfalls an den
Administratorclient gesendet.

    <observe roomId="871faccb-5190-4e44-82fc-6cdcbb493726"/>

Clients die auf dem Serverport (localhost 13050) gestartet werden können
so über diesen Code joinen.

    <protocol>
      <joinPrepared reservationCode="RC1"/>

    <protocol>
      <joinPrepared reservationCode="RC2"/>

## Variante 2 ((eventuell) ohne AdminClient [???](#ohne-reservierungscode))

Die Clients wurden auf dem Serverport (Standard: localhost 13050)
gestartet.

Sie können sich mit folgender Anfrage einen bereits offenen Spiel
gleichen Typs beitreten oder, falls kein Spiel des Typs vorhanden selbst
eines starten:

    <protocol>
      <join gameType="swc_2018_hase_und_igel"/>

Der Server antwortet mit:

    <protocol>
      <joined roomId="871faccb-5190-4e44-82fc-6cdcbb493726"/>

## Weiterer Spielverlauf

Der Server antwortet jeweils mit der WelcomeMessage
([???](#welcome-message)) und dem ersten GameState ([???](#memento))
sobald beide Spieler verbunden sind.

    <room roomId="871faccb-5190-4e44-82fc-6cdcbb493726">
      <data class="welcomeMessage" color="red"/>
    </room>
    <room roomId="871faccb-5190-4e44-82fc-6cdcbb493726">
      <data class="memento">
        <state class="state" turn="0" startPlayer="RED" currentPlayer="RED">
          <red displayName="Unknown" color="RED" index="0" carrots="68" salads="5">
            <cards>
              <type>TAKE_OR_DROP_CARROTS</type>
              <type>EAT_SALAD</type>
              <type>HURRY_AHEAD</type>
              <type>FALL_BACK</type>
            </cards>
          </red>
          <blue displayName="Unknown" color="BLUE" index="0" carrots="68" salads="5">
            <cards>
              <type>TAKE_OR_DROP_CARROTS</type>
              <type>EAT_SALAD</type>
              <type>HURRY_AHEAD</type>
              <type>FALL_BACK</type>
            </cards>
          </blue>
          <board>
            <fields index="0" type="START"/>
            <fields index="1" type="CARROT"/>
            <fields index="2" type="HARE"/>
            <fields index="3" type="HARE"/>
            <fields index="4" type="POSITION_2"/>
            <fields index="5" type="POSITION_1"/>
            <fields index="6" type="CARROT"/>
            <fields index="7" type="CARROT"/>
            <fields index="8" type="HARE"/>
            <fields index="9" type="CARROT"/>
            <fields index="10" type="SALAD"/>
            <fields index="11" type="HEDGEHOG"/>
            <fields index="12" type="HARE"/>
            <fields index="13" type="CARROT"/>
            <fields index="14" type="CARROT"/>
            <fields index="15" type="HEDGEHOG"/>
            <fields index="16" type="POSITION_1"/>
            <fields index="17" type="CARROT"/>
            <fields index="18" type="POSITION_2"/>
            <fields index="19" type="HEDGEHOG"/>
            <fields index="20" type="CARROT"/>
            ...
            <fields index="57" type="SALAD"/>
            <fields index="58" type="CARROT"/>
            <fields index="59" type="POSITION_1"/>
            <fields index="60" type="HARE"/>
            <fields index="61" type="CARROT"/>
            <fields index="62" type="HARE"/>
            <fields index="63" type="CARROT"/>
            <fields index="64" type="GOAL"/>
          </board>
        </state>
      </data>
    </room>

Der erste Spieler erhält dann eine Zugaufforderung
([???](#move-request)), falls in server.properties paused auf false
gesetzt wurde. Falls das Spiel pausiert ist, muss das Spiel durch einen
Administratorclient gestartet werden:

Verbinden des Administratorclients (falls es sich um die erste
Kontaktaufnahme zum Server handelt, ansonsten &lt;protocol&gt;
weglassen).

    <protocol>
      <authenticate passphrase="examplepassword"/>

Pausierung aufheben:

    <pause roomId="871faccb-5190-4e44-82fc-6cdcbb493726" pause="false" />

Daraufhin wird der erste Spieler aufgefordert einen Zug zu senden:

    <room roomId="871faccb-5190-4e44-82fc-6cdcbb493726">
      <data class="sc.framework.plugins.protocol.MoveRequest"/>
    </room>

Der Client des CurrentPlayer sendet nun einen Zug ([???](#zug)):

    <room roomId="871faccb-5190-4e44-82fc-6cdcbb493726">
      <data class="move">
        <advance order="0" distance="6">
      </data>
    </room>

So geht es abwechselnd weiter, bis zum Spielende ([???](#spielende)).
Die letzte Nachricht des Servers endet mit:

    </protocol>

Danach wird die Verbindung geschlossen.
