---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/powershell/module/az.functions/get-azfunctionappsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppSetting.md
ms.openlocfilehash: 5aff9382cbeac47c8d4423769d6256d34d5d109a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927152"
---
# Get-AzFunctionAppSetting

## SYNOPSIS
Ruft App-Einstellungen für eine Funktions-App ab.

## SYNTAX

### ByName (Standard)
```
Get-AzFunctionAppSetting -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### ByObjectInput
```
Get-AzFunctionAppSetting -InputObject <ISite> [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## BESCHREIBUNG
Ruft App-Einstellungen für eine Funktions-App ab.

## BEISPIELE

### Beispiel 1: Herunterladen der App-Einstellungen einer Funktions-App.
```powershell
PS C:\> Get-AzFunctionAppSetting -Name MyAppName -ResourceGroupName MyResourceGroupName
```

Dieser Befehl ruft die App-Einstellungen einer Funktions-App ab.

## PARAMETER

### -DefaultProfile


```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Informationen zum Erstellen finden Sie im Abschnitt NOTIZEN zu INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite
Parameter Sets: ByObjectInput
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Name der Funktions-App.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Name der Ressourcengruppe, zu der die Ressource gehört.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Die Azure-Abonnement-ID.

```yaml
Type: System.String[]
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### -Bestätigen
Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.
Das Cmdlet wird nicht ausgeführt.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## EINGABEN

### Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite

## AUSGABEN

### Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IStringDictionary

## NOTIZEN

ALIASE

KOMPLEXE PARAMETEREIGENSCHAFTEN

Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält. Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.


INPUTOBJECT <ISite> : 
  - `Location <String>`: Ressourcenspeicherort.
  - `CloningInfoSourceWebAppId <String>`: ARM Ressourcen-ID der Quell-App. Die App-Ressourcen-ID ist das Formular /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} für Produktionsplätze und /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName}.
  - `[Kind <String>]`: Art der Ressource.
  - `[Tag <IResourceTags>]`: Ressourcentags.
    - `[(Any) <String>]`: Dies gibt an, dass diesem Objekt eine beliebige Eigenschaft hinzugefügt werden kann.
  - `[ClientAffinityEnabled <Boolean?>]`: zum Aktivieren der Clientaffinität; zum Beenden des Sendens von Sitzungsaffinitätscookies, die Clientanforderungen in derselben Sitzung an <code>true</code> <code>false</code> dieselbe Instanz weiterrouten. Standard ist <code>true</code> .
  - `[ClientCertEnabled <Boolean?>]`: <code>true</code> zum Aktivieren der Clientzertifikatauthentifizierung (TLS Mutual Authentication); andernfalls <code>false</code> . Standard ist <code>false</code> .
  - `[ClientCertExclusionPath <String>]`: Durch Kommas getrennte Ausschlusspfade für Clientzertifikate
  - `[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: Anwendungseinstellung außer Kraft für geklonte Apps. Wenn angegeben, setzen diese Einstellungen die aus der Quell-App geklonten Einstellungen außer Kraft. Andernfalls bleiben die Anwendungseinstellungen aus der Quell-App erhalten.
    - `[(Any) <String>]`: Dies gibt an, dass diesem Objekt eine beliebige Eigenschaft hinzugefügt werden kann.
  - `[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> zum Klonen von benutzerdefinierten Hostnamen aus der Quell-App; andernfalls <code>false</code> .
  - `[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> zum Klonen der Quellcodeverwaltung aus der Quell-App; andernfalls <code>false</code> .
  - `[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> so konfigurieren Sie den Lastenausgleich für die Quell- und Ziel-App.
  - `[CloningInfoCorrelationId <String>]`: Korrelations-ID des Klonvorgangs. Diese ID bindet mehrere Klonvorgänge zusammen, um dieselbe Momentaufnahme zu verwenden.
  - `[CloningInfoHostingEnvironment <String>]`: App-Dienstumgebung.
  - `[CloningInfoOverwrite <Boolean?>]`: <code>true</code> zum Überschreiben der Ziel-App; andernfalls <code>false</code> .
  - `[CloningInfoSourceWebAppLocation <String>]`: Speicherort der Quell-App ex: West US oder North Europe
  - `[CloningInfoTrafficManagerProfileId <String>]`: ARM ressourcen-ID des Traffic Manager-Profils, das verwendet werden soll, wenn es vorhanden ist. Die Traffic Manager-Ressourcen-ID ist das Formular /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.
  - `[CloningInfoTrafficManagerProfileName <String>]`: Name des zu erstellende Traffic Manager-Profils. Dies ist nur erforderlich, wenn das Traffic Manager-Profil noch nicht vorhanden ist.
  - `[Config <ISiteConfig>]`: Konfiguration der App.
    - `IsPushEnabled <Boolean>`: Ruft ein Kennzeichen ab oder legt fest, ob der Pushendpunkt aktiviert ist.
    - `[ActionMinProcessExecutionTime <String>]`: Mindestzeit, die der Prozess ausführen muss, bevor die Aktion ausgeführt wird
    - `[ActionType <AutoHealActionType?>]`: Vordefinierte Aktion, die sie ergreifen soll.
    - `[AlwaysOn <Boolean?>]`: <code>true</code> wenn Immer ein aktiviert ist; andernfalls <code>false</code> .
    - `[ApiDefinitionUrl <String>]`: Die URL der API-Definition.
    - `[ApiManagementConfigId <String>]`: APIM-Api Identifier.
    - `[AppCommandLine <String>]`: Startbefehlzeile der App.
    - `[AppSetting <INameValuePair[]>]`: Anwendungseinstellungen.
      - `[Name <String>]`: Name des Paares.
      - `[Value <String>]`: Koppelwert.
    - `[AutoHealEnabled <Boolean?>]`: <code>true</code> wenn Automatisches Verheilen aktiviert ist; andernfalls <code>false</code> .
    - `[AutoSwapSlotName <String>]`: Name des automatischen Tauschplatzes.
    - `[ConnectionString <IConnStringInfo[]>]`: Verbindungszeichenfolgen.
      - `[ConnectionString <String>]`: Wert der Verbindungszeichenfolge.
      - `[Name <String>]`: Name der Verbindungszeichenfolge.
      - `[Type <ConnectionStringType?>]`: Datenbanktyp.
    - `[CorAllowedOrigin <String[]>]`: Ruft die Liste der Ursprünge ab, die originsübergreifende Aufrufe (z. B. dürfen) zulässig sein sollen, oder legt sie http://example.com:12345) fest. Verwenden Sie "*", um alle zu erlauben.
    - `[CorSupportCredentials <Boolean?>]`: Ruft ab oder legt fest, ob CORS-Anforderungen mit Anmeldeinformationen zulässig sind. Weitere         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         Details finden Sie unter.
    - `[CustomActionExe <String>]`: Ausführbare Datei, die ausgeführt werden soll.
    - `[CustomActionParameter <String>]`: Parameter für die ausführbare Datei.
    - `[DefaultDocument <String[]>]`: Standarddokumente.
    - `[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> wenn die detaillierte Fehlerprotokollierung aktiviert ist; andernfalls <code>false</code> .
    - `[DocumentRoot <String>]`: Dokumentstamm.
    - `[DynamicTagsJson <String>]`: Ruft eine JSON-Zeichenfolge ab oder legt sie fest, die eine Liste dynamischer Tags enthält, die aus Benutzeransprüchen im Pushregistrierungsendpunkt ausgewertet werden.
    - `[ExperimentRampUpRule <IRampUpRule[]>]`: Liste der Anlaufregeln.
      - `[ActionHostName <String>]`: Hostname eines Slot, an den der Datenverkehr umgeleitet wird, wenn dies entschieden ist. Beispiel: myapp-stage.azurewebsites.net.
      - `[ChangeDecisionCallbackUrl <String>]`: Benutzerdefinierter Entscheidungsalgorithmus kann in der TiPCallback-Websiteerweiterung bereitgestellt werden, deren URL angegeben werden kann. Informationen zum Gerüst und den Verträgen finden Sie unter TiPCallback-Websiteerweiterung.         https://www.siteextensions.net/packages/TiPCallback/
      - `[ChangeIntervalInMinute <Int32?>]`: Gibt das Intervall in Minuten an, um den Umleitungsprozentwert neu zu bewerten.
      - `[ChangeStep <Double?>]`: Im Szenario für automatisches Hochfahren ist dies der Schritt zum Hinzufügen/Entfernen von, bis <code>ReroutePercentage</code> \n oder <code>MinReroutePercentage</code> erreicht         <code>MaxReroutePercentage</code> wird. Websitemetriken werden alle N Minuten überprüft, die im .\nCustom-Entscheidungsalgorithmus angegeben sind, kann in der TiPCallback-Websiteerweiterung bereitgestellt werden, in der <code>ChangeIntervalInMinutes</code> die URL angegeben werden <code>ChangeDecisionCallbackUrl</code> kann.
      - `[MaxReroutePercentage <Double?>]`: Gibt die obere Grenze an, unter der "Umleitungsprozent" bleiben soll.
      - `[MinReroutePercentage <Double?>]`: Gibt die untere Grenze an, über der die Umleitungslinie bleiben soll.
      - `[Name <String>]`: Name der Routingregel. Der empfohlene Name wäre, auf den Slot zu verweisen, der den Datenverkehr im Experiment erhält.
      - `[ReroutePercentage <Double?>]`: Prozentsatz des Datenverkehrs, der an umgeleitet <code>ActionHostName</code> wird.
    - `[FtpsState <FtpsState?>]`: Status des FTP/FTPS-Diensts
    - `[HandlerMapping <IHandlerMapping[]>]`: Handlerzuordnungen.
      - `[Argument <String>]`: Befehlszeilenargumente, die an den Skriptprozessor übergeben werden sollen.
      - `[Extension <String>]`: Anforderungen mit dieser Erweiterung werden mit der angegebenen FastCGI-Anwendung behandelt.
      - `[ScriptProcessor <String>]`: Der absolute Pfad zur FastCGI-Anwendung.
    - `[HealthCheckPath <String>]`: Integritätsprüfungspfad
    - `[Http20Enabled <Boolean?>]`: Http20Enabled: Konfiguriert eine Website so, dass Clients eine Verbindung über http2.0 herstellen können
    - `[HttpLoggingEnabled <Boolean?>]`: <code>true</code> wenn die #A0 aktiviert ist; andernfalls <code>false</code> .
    - `[IPSecurityRestriction <IIPSecurityRestriction[]>]`: IP-Sicherheitseinschränkungen für Main.
      - `[Action <String>]`: Zulassen oder Verweigern des Zugriffs für diesen IP-Bereich.
      - `[Description <String>]`: Beschreibung der IP-Einschränkungsregel.
      - `[IPAddress <String>]`: IP-Adresse, für die die Sicherheitseinschränkung gültig ist.         Sie kann in Form einer reinen ipv4-Adresse (erforderliche SubnetMask-Eigenschaft) oder cidr-Notation wie ipv4/mask (leading bit match) verwendet werden. Für CIDR darf keine Subnetzmask-Eigenschaft angegeben werden.
      - `[Name <String>]`: Name der IP-Einschränkungsregel.
      - `[Priority <Int32?>]`: Priorität der Regel für DIE IP-Einschränkung.
      - `[SubnetMask <String>]`: Subnetzformat für den Bereich der IP-Adressen, für den die Einschränkung gültig ist.
      - `[SubnetTrafficTag <Int32?>]`: (internes) Subnetzverkehrstag
      - `[Tag <IPFilterTag?>]`: Definiert, wofür dieser IP-Filter verwendet wird. Dies soll die IP-Filterung für Proxys unterstützen.
      - `[VnetSubnetResourceId <String>]`: Virtuelle Netzwerkressourcen-ID
      - `[VnetTrafficTag <Int32?>]`: (internes) Vnet-Verkehrstag
    - `[JavaContainer <String>]`: Java Container.
    - `[JavaContainerVersion <String>]`: Java Containerversion.
    - `[JavaVersion <String>]`: Java Version.
    - `[LimitMaxDiskSizeInMb <Int64?>]`: Maximal zulässige Datenträgergröße in MB.
    - `[LimitMaxMemoryInMb <Int64?>]`: Maximal zulässige Speicherauslastung in MB.
    - `[LimitMaxPercentageCpu <Double?>]`: Maximal zulässiger Prozentsatz der CPU-Nutzung.
    - `[LinuxFxVersion <String>]`: Linux App Framework und Version
    - `[LoadBalancing <SiteLoadBalancing?>]`: Lastenausgleich der Website.
    - `[LocalMySqlEnabled <Boolean?>]`: <code>true</code> um lokales MySQL zu aktivieren; andernfalls <code>false</code> .
    - `[LogsDirectorySizeLimit <Int32?>]`: HTTP protokolliert das Verzeichnisgrößenlimit.
    - `[MachineKeyDecryption <String>]`: Algorithmus, der für die Entschlüsselung verwendet wird.
    - `[MachineKeyDecryptionKey <String>]`: Entschlüsselungsschlüssel.
    - `[MachineKeyValidation <String>]`: MachineKey-Überprüfung.
    - `[MachineKeyValidationKey <String>]`: Überprüfungsschlüssel.
    - `[ManagedPipelineMode <ManagedPipelineMode?>]`: Verwalteter Pipelinemodus.
    - `[ManagedServiceIdentityId <Int32?>]`: Id für verwaltete Dienstidentität
    - `[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: Konfiguriert die für SSL-Anforderungen erforderliche Mindestversion von TLS
    - `[NetFrameworkVersion <String>]`: .NET Framework Version.
    - `[NodeVersion <String>]`: Version von Node.js.
    - `[NumberOfWorker <Int32?>]`: Anzahl der Arbeitskräfte.
    - `[PhpVersion <String>]`: Version von PHP.
    - `[PowerShellVersion <String>]`: Version von PowerShell.
    - `[PreWarmedInstanceCount <Int32?>]`: Anzahl der vordefinierten Instanzen.         Diese Einstellung gilt nur für die Pläne "Verbrauch" und "Flexible Pläne".
    - `[PublishingUsername <String>]`: Veröffentlichen des Benutzernamens.
    - `[PushKind <String>]`: Art der Ressource.
    - `[PythonVersion <String>]`: Version von Python.
    - `[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> wenn das Remotedebuding aktiviert ist; andernfalls <code>false</code> .
    - `[RemoteDebuggingVersion <String>]`: Remotedebugversion.
    - `[RequestCount <Int32?>]`: Anzahl anfordern.
    - `[RequestTimeInterval <String>]`: Zeitintervall.
    - `[RequestTracingEnabled <Boolean?>]`: <code>true</code> wenn die Anforderungsablaufverfolgung aktiviert ist; andernfalls <code>false</code> .
    - `[RequestTracingExpirationTime <DateTime?>]`: Ablaufzeit der Ablaufverfolgung anfordern.
    - `[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: IP-Sicherheitseinschränkungen für scm.
    - `[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: IP-Sicherheitseinschränkungen für scm für die Verwendung von Main.
    - `[ScmType <ScmType?>]`: SCM-Typ.
    - `[SlowRequestCount <Int32?>]`: Anzahl anfordern.
    - `[SlowRequestTimeInterval <String>]`: Zeitintervall.
    - `[SlowRequestTimeTaken <String>]`: Zeit, die sie sich genommen hat.
    - `[TagWhitelistJson <String>]`: Ruft eine JSON-Zeichenfolge ab oder legt sie fest, die eine Liste der Tags enthält, die auf der Whitelist für die Verwendung durch den Pushregistrierungsendpunkt stehen.
    - `[TagsRequiringAuth <String>]`: Ruft eine JSON-Zeichenfolge ab oder legt sie fest, die eine Liste der Tags enthält, für die die Benutzerauthentifizierung im Pushregistrierungsendpunkt verwendet werden muss.         Tags können aus alphanumerischen Zeichen und den folgenden Zeichen bestehen: '_', '@', '#', '.', ':', '-'.         Die Überprüfung sollte im PushRequestHandler ausgeführt werden.
    - `[TracingOption <String>]`: Ablaufverfolgungsoptionen.
    - `[TriggerPrivateBytesInKb <Int32?>]`: Eine Regel, die auf privaten Bytes basiert.
    - `[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: Eine Regel, die auf Statuscodes basiert.
      - `[Count <Int32?>]`: Anzahl anfordern.
      - `[Status <Int32?>]`: HTTP-Statuscode.
      - `[SubStatus <Int32?>]`: Unterstatus anfordern.
      - `[TimeInterval <String>]`: Zeitintervall.
      - `[Win32Status <Int32?>]`: Win32-Fehlercode.
    - `[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> zum Verwenden des 32-Bit-Workerprozesses; andernfalls <code>false</code> .
    - `[VirtualApplication <IVirtualApplication[]>]`: Virtuelle Anwendungen.
      - `[PhysicalPath <String>]`: Physischer Pfad.
      - `[PreloadEnabled <Boolean?>]`: <code>true</code> wenn das Vorabladen aktiviert ist; andernfalls <code>false</code> .
      - `[VirtualDirectory <IVirtualDirectory[]>]`: Virtuelle Verzeichnisse für virtuelle Anwendungen.
        - `[PhysicalPath <String>]`: Physischer Pfad.
        - `[VirtualPath <String>]`: Pfad zur virtuellen Anwendung.
      - `[VirtualPath <String>]`: Virtueller Pfad.
    - `[VnetName <String>]`: Name des virtuellen Netzwerks.
    - `[WebSocketsEnabled <Boolean?>]`: <code>true</code> wenn WebSocket aktiviert ist; andernfalls <code>false</code> .
    - `[WindowsFxVersion <String>]`: Xenon App Framework und Version
    - `[XManagedServiceIdentityId <Int32?>]`: Explizite Identitäts-ID für verwaltete Dienste
  - `[ContainerSize <Int32?>]`: Größe des Funktionscontainers.
  - `[DailyMemoryTimeQuota <Int32?>]`: Maximal zulässiges tägliches Speicher-Zeitkontingent (gilt nur für dynamische Apps).
  - `[Enabled <Boolean?>]`: <code>true</code> wenn die App aktiviert ist; andernfalls <code>false</code> . Wenn Sie diesen Wert auf false festlegen, wird die App deaktiviert (die App wird offline geschaltet).
  - `[HostNameSslState <IHostNameSslState[]>]`: Hostname SSL-Zustände werden verwendet, um die SSL-Bindungen für die Hostnamen der App zu verwalten.
    - `[HostType <HostType?>]`: Gibt an, ob der Hostname ein Standard- oder Repositoryhostname ist.
    - `[Name <String>]`: Hostname.
    - `[SslState <SslState?>]`: SSL-Typ.
    - `[Thumbprint <String>]`: Fingerabdruck des SSL-Zertifikats.
    - `[ToUpdate <Boolean?>]`: So wird <code>true</code> festgelegt, dass der vorhandene Hostname aktualisiert wird.
    - `[VirtualIP <String>]`: Virtuelle IP-Adresse, die dem Hostnamen zugewiesen ist, wenn IP-basiertes SSL aktiviert ist.
  - `[HostNamesDisabled <Boolean?>]`: <code>true</code> um die öffentlichen Hostnamen der App zu deaktivieren; andernfalls <code>false</code> .          Wenn <code>true</code> , kann auf die App nur über den API-Verwaltungsvorgang zugegriffen werden.
  - `[HostingEnvironmentProfileId <String>]`: Ressourcen-ID der App-Dienstumgebung.
  - `[HttpsOnly <Boolean?>]`: HttpsOnly: konfiguriert eine Website so, dass nur https-Anforderungen akzeptiert werden. Umleitung von Problemen bei Http-Anforderungen
  - `[HyperV <Boolean?>]`: Hyper-V-Sandkasten.
  - `[IdentityType <ManagedServiceIdentityType?>]`: Typ der verwalteten Dienstidentität.
  - `[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: Die Liste der benutzer zugewiesenen Identitäten, die der Ressource zugeordnet sind. Die Schlüsselverweise für benutzeridentitätswörterbücher werden ARM Ressourcen-ID im Formular angezeigt: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}
    - `[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: Dies gibt an, dass diesem Objekt eine beliebige Eigenschaft hinzugefügt werden kann.
  - `[IsXenon <Boolean?>]`: Veraltet: Hyper-V-Sandkasten.
  - `[RedundancyMode <RedundancyMode?>]`: Websiteredundanzmodus
  - `[Reserved <Boolean?>]`: <code>true</code> falls reserviert; andernfalls <code>false</code> .
  - `[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> um die #A0 (KUDU) zu beenden, wenn die App beendet wird; andernfalls <code>false</code> . Die Standardeinstellung ist <code>false</code> .
  - `[ServerFarmId <String>]`: Ressourcen-ID des zugeordneten App Service-Plans, formatiert als: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".

## VERWANDTE LINKS

