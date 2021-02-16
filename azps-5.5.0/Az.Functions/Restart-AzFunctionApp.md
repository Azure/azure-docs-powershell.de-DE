---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/restart-azfunctionapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Restart-AzFunctionApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Restart-AzFunctionApp.md
ms.openlocfilehash: 408adc74257e1260e97c47b24d91cf437b915a5f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100154916"
---
# Restart-AzFunctionApp

## SYNOPSIS
Startet eine Funktions-App neu.

## SYNTAX

### RestartByName (Standard)
```
Restart-AzFunctionApp -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Force]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### ByObjectInput
```
Restart-AzFunctionApp -InputObject <ISite> [-Force] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## BESCHREIBUNG
Startet eine Funktions-App neu.

## BEISPIELE

### Beispiel 1: Benennen Sie eine Funktions-App, und starten Sie sie neu.
```powershell
PS C:\> Get-AzFunctionApp -Name MyAppName -ResourceGroupName MyResourceGroupName | Restart-AzFunctionApp -Force
```

Dieser Befehl ruft eine Funktions-App nach Name ab und wird neu gestartet.

### Beispiel 2: Starten Sie eine Funktions-App nach Name neu.
```powershell
PS C:\> Restart-AzFunctionApp -Name MyAppName -ResourceGroupName MyResourceGroupName -Force
```

Mit diesem Befehl wird eine Funktions-App nach Name neu gestartet.

## PARAMETERS

### -DefaultProfile
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

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

### -Force
Erzwingt das Cmdlet, die Funktions-App ohne Bestätigungsaufforderung neu zu starten.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Informationen zum Erstellen finden Sie im Abschnitt NOTES zu #A0 und zum Erstellen einer Hashtabelle.

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
Der Name der Funktions-App.

```yaml
Type: System.String
Parameter Sets: RestartByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Gibt "true" zurück, wenn der Befehl erfolgreich ist.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName


```yaml
Type: System.String
Parameter Sets: RestartByName
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
Type: System.String
Parameter Sets: RestartByName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
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

### -Waswenn
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.
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
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite

## AUSGABEN

### System.Boolean

## HINWEISE

ALIASE

KOMPLEXE PARAMETEREIGENSCHAFTEN

Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften. Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.


INPUTOBJECT <ISite> : 
  - `Location <String>`: Ressourcenspeicherort.
  - `CloningInfoSourceWebAppId <String>`: ARM Ressourcen-ID der Quell-App. Die App-Ressourcen-ID hat das Format /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} für Produktionsslots und /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} für andere Slots.
  - `[Kind <String>]`: Ressourcentyp.
  - `[Tag <IResourceTags>]`: Ressourcentags.
    - `[(Any) <String>]`: Dies gibt an, dass diesem Objekt beliebige Eigenschaften hinzugefügt werden können.
  - `[ClientAffinityEnabled <Boolean?>]`: <code>true</code> zum Aktivieren der Clientaffinität, zum Beenden des Sendens von Sitzungsaffinitätscookies, die Clientanforderungen in derselben Sitzung an dieselbe Instanz weiter <code>false</code> routen. Der Standardwert ist <code>true</code> .
  - `[ClientCertEnabled <Boolean?>]`: <code>true</code> zum Aktivieren der Clientzertifikatauthentifizierung (TLS-gegenseitige Authentifizierung). Andernfalls. <code>false</code> Der Standardwert ist <code>false</code> .
  - `[ClientCertExclusionPath <String>]`: Durch Kommas getrennte Ausschlusspfade für Clientzertifikate
  - `[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: Anwendungseinstellungsüberschreibungen für geklonte Apps. Falls angegeben, setzen diese Einstellungen die Einstellungen außer Kraft, die aus der Quell-App geklont werden. Andernfalls bleiben die Anwendungseinstellungen der Quell-App erhalten.
    - `[(Any) <String>]`: Dies gibt an, dass diesem Objekt beliebige Eigenschaften hinzugefügt werden können.
  - `[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> um benutzerdefinierte Hostnamen aus der #A0 zu klonen. Andernfalls <code>false</code> .
  - `[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> um das Quellsteuerelement aus der #A0 zu klonen. Andernfalls <code>false</code> .
  - `[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> zum Konfigurieren des Lastenausgleichs für die Quell- und Ziel-App.
  - `[CloningInfoCorrelationId <String>]`: Korrelations-ID des Klonvorgangs. Diese ID bindet mehrere Klonvorgänge zusammen, um dieselbe Momentaufnahme zu verwenden.
  - `[CloningInfoHostingEnvironment <String>]`: App-Dienstumgebung.
  - `[CloningInfoOverwrite <Boolean?>]`: <code>true</code> um die #A0 zu überschreiben. Andernfalls <code>false</code> .
  - `[CloningInfoSourceWebAppLocation <String>]`: Speicherort der Quell-App, beispiel: USA, Westen oder Europa, Norden
  - `[CloningInfoTrafficManagerProfileId <String>]`: ARM Ressourcen-ID des zu verwendende Datenverkehrs-Manager-Profils, sofern vorhanden. Die Ressourcen-ID des Datenverkehrs-Managers liegt im Format "/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}" vor.
  - `[CloningInfoTrafficManagerProfileName <String>]`: Name des zu erstellende Traffic-Manager-Profils. Dies ist nur erforderlich, wenn das Profil von Traffic Manager noch nicht vorhanden ist.
  - `[Config <ISiteConfig>]`: Konfiguration der App.
    - `IsPushEnabled <Boolean>`: Ruft ein Kennzeichen ab oder legt es fest, das angibt, ob der Pushendpunkt aktiviert ist.
    - `[ActionMinProcessExecutionTime <String>]`: Mindestzeit, die der Prozess ausgeführt werden muss, bevor die Aktion ausgeführt wird
    - `[ActionType <AutoHealActionType?>]`: Vordefinierte Aktion, die sie ergreifen soll.
    - `[AlwaysOn <Boolean?>]`: <code>true</code> wenn "Immer aktiviert" aktiviert ist; andernfalls. <code>false</code>
    - `[ApiDefinitionUrl <String>]`: Die URL der API-Definition.
    - `[ApiManagementConfigId <String>]`: APIM-Api-ID.
    - `[AppCommandLine <String>]`: Startbefehlszeile der App.
    - `[AppSetting <INameValuePair[]>]`: Anwendungseinstellungen.
      - `[Name <String>]`: Name des Koppelns
      - `[Value <String>]`: Paarwert.
    - `[AutoHealEnabled <Boolean?>]`: <code>true</code> wenn die automatische Umergnung aktiviert ist. Andernfalls. <code>false</code>
    - `[AutoSwapSlotName <String>]`: Name des automatischen Tauschs von Slot.
    - `[ConnectionString <IConnStringInfo[]>]`: Verbindungszeichenfolgen.
      - `[ConnectionString <String>]`: Wert der Verbindungszeichenfolge.
      - `[Name <String>]`: Name der Verbindungszeichenfolge.
      - `[Type <ConnectionStringType?>]`: Datenbanktyp.
    - `[CorAllowedOrigin <String[]>]`: Ruft die Liste der Ursprünge ab oder legt sie fest, für die cross-origin-Aufrufe zulässig sein sollen (z. http://example.com:12345) B.: Verwenden Sie "*", um alle zu erlauben.
    - `[CorSupportCredentials <Boolean?>]`: Ruft ab oder legt fest, ob CORS-Anforderungen mit Anmeldeinformationen zulässig sind. Weitere         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         Details finden Sie hier.
    - `[CustomActionExe <String>]`: Ausführbare Datei, die ausgeführt werden soll.
    - `[CustomActionParameter <String>]`: Parameter für die ausführbare Datei.
    - `[DefaultDocument <String[]>]`: Standarddokumente.
    - `[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> wenn die detaillierte Fehlerprotokollierung aktiviert ist. Andernfalls. <code>false</code>
    - `[DocumentRoot <String>]`: Dokumentstamm
    - `[DynamicTagsJson <String>]`: Ruft eine JSON-Zeichenfolge ab oder legt sie fest, die eine Liste von dynamischen Tags enthält, die von Denkwerten im Pushregistrierungsendpunkt ausgewertet werden.
    - `[ExperimentRampUpRule <IRampUpRule[]>]`: Liste der Regeln für die Einlaufung.
      - `[ActionHostName <String>]`: Hostname eines Slot, an das der Datenverkehr umgeleitet wird, wenn dies entschieden ist. Beispiel: myapp-stage.azurewebsites.net.
      - `[ChangeDecisionCallbackUrl <String>]`: Benutzerdefinierter Entscheidungsalgorithmus kann in der TiPCallback-Websiteerweiterung bereitgestellt werden, welche URL angegeben werden kann. Informationen zum Gerüst und zu Verträgen finden Sie unter "TiPCallback-Websiteerweiterung".         https://www.siteextensions.net/packages/TiPCallback/
      - `[ChangeIntervalInMinute <Int32?>]`: Gibt das Intervall in Minuten an, um "ReroutePercentage" neu zu bewerten.
      - `[ChangeStep <Double?>]`: Im Szenario für die automatische Erstrecherhung ist dies der Schritt zum Hinzufügen/Entfernen von, bis <code>ReroutePercentage</code> \n oder <code>MinReroutePercentage</code> erreicht         <code>MaxReroutePercentage</code> ist. Websitemetriken werden alle N Minuten überprüft, die im ".\nCustom"-Entscheidungsalgorithmus angegeben sind, können in der TiPCallback-Websiteerweiterung bereitgestellt werden, in der <code>ChangeIntervalInMinutes</code> die URL angegeben werden <code>ChangeDecisionCallbackUrl</code> kann.
      - `[MaxReroutePercentage <Double?>]`: Gibt die obere Grenze an, unter der "ReroutePercentage" bleiben soll.
      - `[MinReroutePercentage <Double?>]`: Gibt die untere Grenze an, über der "ReroutePercentage" bleiben soll.
      - `[Name <String>]`: Name der Routingregel. Der empfohlene Name ist, auf den Platz zu verweisen, der den Datenverkehr im Experiment erhält.
      - `[ReroutePercentage <Double?>]`: Prozentsatz des Datenverkehrs, der umgeleitet <code>ActionHostName</code> wird.
    - `[FtpsState <FtpsState?>]`: Status des FTP/FTPS-Diensts
    - `[HandlerMapping <IHandlerMapping[]>]`: Handlerzuordnungen.
      - `[Argument <String>]`: Befehlszeilenargumente, die an den Skriptprozessor übergeben werden sollen.
      - `[Extension <String>]`: Anforderungen mit dieser Erweiterung werden mit der angegebenen Anwendung FastCGI verarbeitet.
      - `[ScriptProcessor <String>]`: Der absolute Pfad zur FastCGI-Anwendung.
    - `[HealthCheckPath <String>]`: Pfad der Integritätsprüfung
    - `[Http20Enabled <Boolean?>]`: Http20Enabled: Konfiguriert eine Website, damit Clients die Verbindung über http2.0 herstellen können.
    - `[HttpLoggingEnabled <Boolean?>]`: <code>true</code> wenn die #A0 aktiviert ist. Andernfalls . <code>false</code>
    - `[IPSecurityRestriction <IIPSecurityRestriction[]>]`: IP-Sicherheitseinschränkungen für "main".
      - `[Action <String>]`: Zugriff für diesen IP-Bereich zulassen oder verweigern.
      - `[Description <String>]`: Beschreibung der IP-Einschränkungsregel.
      - `[IPAddress <String>]`: IP-Adresse, für die die Sicherheitseinschränkung gültig ist.         Sie kann in Form einer reinen ipv4-Adresse (erforderliche Subnetzmask-Eigenschaft) oder einer CIDR-Notation wie "ipv4/mask" (führende Bit-Übereinstimmung) liegen. Bei CIDR darf die Eigenschaft "SubnetMask" nicht angegeben werden.
      - `[Name <String>]`: Name der IP-Einschränkungsregel.
      - `[Priority <Int32?>]`: Priorität der IP-Einschränkungsregel.
      - `[SubnetMask <String>]`: Subnetzformat für den Bereich der IP-Adressen, für den die Einschränkung gültig ist.
      - `[SubnetTrafficTag <Int32?>]`: (intern) Tag für Den Subnetzdatenverkehr
      - `[Tag <IPFilterTag?>]`: Definiert, wofür dieser IP-Filter verwendet wird. Dies ist die Unterstützung der IP-Filterung auf Proxys.
      - `[VnetSubnetResourceId <String>]`: Id der virtuellen Netzwerkressource
      - `[VnetTrafficTag <Int32?>]`: (intern) Vnet-Datenverkehrstag
    - `[JavaContainer <String>]`: Java Container.
    - `[JavaContainerVersion <String>]`: Java Containerversion.
    - `[JavaVersion <String>]`: Java Version.
    - `[LimitMaxDiskSizeInMb <Int64?>]`: Maximal zulässige Datenträgergröße in MB.
    - `[LimitMaxMemoryInMb <Int64?>]`: Maximal zulässige Speicherauslastung in MB.
    - `[LimitMaxPercentageCpu <Double?>]`: Maximal zulässiger Prozentsatz der CPU-Nutzung.
    - `[LinuxFxVersion <String>]`: Linux-App-Framework und -Version
    - `[LoadBalancing <SiteLoadBalancing?>]`: Lastenausgleich der Website.
    - `[LocalMySqlEnabled <Boolean?>]`: <code>true</code> zum Aktivieren des lokalen MySQL. Andernfalls <code>false</code> .
    - `[LogsDirectorySizeLimit <Int32?>]`: Beschränkung der Größe des HTTP-Verzeichnisses.
    - `[MachineKeyDecryption <String>]`: Algorithmus, der für die Entschlüsselung verwendet wird.
    - `[MachineKeyDecryptionKey <String>]`: Entschlüsselungsschlüssel.
    - `[MachineKeyValidation <String>]`: MachineKey-Überprüfung.
    - `[MachineKeyValidationKey <String>]`: Überprüfungsschlüssel.
    - `[ManagedPipelineMode <ManagedPipelineMode?>]`: Verwalteter Pipelinemodus.
    - `[ManagedServiceIdentityId <Int32?>]`: Verwaltete Dienstidentitäts-ID
    - `[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: Konfiguriert die mindestversion von TLS, die für -SSL-Anforderungen erforderlich ist.
    - `[NetFrameworkVersion <String>]`: .NET Framework-Version.
    - `[NodeVersion <String>]`: Version Node.js.
    - `[NumberOfWorker <Int32?>]`: Anzahl der Arbeitskräfte.
    - `[PhpVersion <String>]`: Version von PHP.
    - `[PowerShellVersion <String>]`: Version von PowerShell.
    - `[PreWarmedInstanceCount <Int32?>]`: Anzahl der vorab angezeigten Instanzen.         Diese Einstellung gilt nur für die Verbrauchs- und Plänen
    - `[PublishingUsername <String>]`: Veröffentlichen des Benutzernamens
    - `[PushKind <String>]`: Ressourcentyp.
    - `[PythonVersion <String>]`: Version von Python.
    - `[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> wenn remote debuggen aktiviert ist. Andernfalls. <code>false</code>
    - `[RemoteDebuggingVersion <String>]`: Remotedebugversion.
    - `[RequestCount <Int32?>]`: Anzahl anfragen.
    - `[RequestTimeInterval <String>]`: Zeitintervall.
    - `[RequestTracingEnabled <Boolean?>]`: <code>true</code> wenn die Anforderungsablaufverfolgung aktiviert ist. Andernfalls <code>false</code> .
    - `[RequestTracingExpirationTime <DateTime?>]`: Ablaufzeit der Ablaufverfolgung anfordern.
    - `[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: IP-Sicherheitseinschränkungen für SCM.
    - `[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: IP-Sicherheitseinschränkungen für SCM zur Verwendung des Haupts.
    - `[ScmType <ScmType?>]`: SCM-Typ.
    - `[SlowRequestCount <Int32?>]`: Anzahl anfragen.
    - `[SlowRequestTimeInterval <String>]`: Zeitintervall.
    - `[SlowRequestTimeTaken <String>]`: Genommene Zeit.
    - `[TagWhitelistJson <String>]`: Ruft eine JSON-Zeichenfolge ab oder legt sie fest, die eine Liste der Tags enthält, die für die Verwendung durch den Pushregistrierungsendpunkt auf der Whiteliste aufgeführt sind.
    - `[TagsRequiringAuth <String>]`: Ruft eine JSON-Zeichenfolge ab oder legt sie fest, die eine Liste von Tags enthält, die die Verwendung der Benutzerauthentifizierung am Pushregistrierungsendpunkt erfordern.         Tags können aus alphanumerischen Zeichen bestehen und folgendes: '_', '@', '#', '.', ':', '-'.         Die Überprüfung sollte im PushRequestHandler durchgeführt werden.
    - `[TracingOption <String>]`: Ablaufverfolgungsoptionen.
    - `[TriggerPrivateBytesInKb <Int32?>]`: Eine Regel basierend auf privaten Bytes.
    - `[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: Eine Regel, die auf Statuscodes basiert.
      - `[Count <Int32?>]`: Anzahl anfragen.
      - `[Status <Int32?>]`: HTTP-Statuscode.
      - `[SubStatus <Int32?>]`: Unterstatus anfordern.
      - `[TimeInterval <String>]`: Zeitintervall.
      - `[Win32Status <Int32?>]`: Win32-Fehlercode.
    - `[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> um den 32-Bit-Workerprozess zu verwenden. <code>false</code> Andernfalls.
    - `[VirtualApplication <IVirtualApplication[]>]`: Virtuelle Anwendungen.
      - `[PhysicalPath <String>]`: Physischer Pfad.
      - `[PreloadEnabled <Boolean?>]`: <code>true</code> wenn das Vorabladen aktiviert ist; andernfalls <code>false</code> .
      - `[VirtualDirectory <IVirtualDirectory[]>]`: Virtuelle Verzeichnisse für virtuelle Anwendungen.
        - `[PhysicalPath <String>]`: Physischer Pfad.
        - `[VirtualPath <String>]`: Pfad zu virtueller Anwendung.
      - `[VirtualPath <String>]`: Virtueller Pfad.
    - `[VnetName <String>]`: Name des virtuellen Netzwerks.
    - `[WebSocketsEnabled <Boolean?>]`: <code>true</code> wenn WebSocket aktiviert ist. Andernfalls. <code>false</code>
    - `[WindowsFxVersion <String>]`: Xenon-App-Framework und -Version
    - `[XManagedServiceIdentityId <Int32?>]`: Explizite Identitäts-ID für verwaltete Dienste
  - `[ContainerSize <Int32?>]`: Größe des Funktionscontainers.
  - `[DailyMemoryTimeQuota <Int32?>]`: Maximal zulässiges tägliches Speicherzeitkontingent (gilt nur für dynamische Apps).
  - `[Enabled <Boolean?>]`: <code>true</code> wenn die App aktiviert ist. Andernfalls <code>false</code> . Wenn Sie diesen Wert auf "false" festlegen, wird die App deaktiviert (die App wird offline geschaltet).
  - `[HostNameSslState <IHostNameSslState[]>]`: Hostname SSL-Zustände werden verwendet, um die SSL-Bindungen für die Hostnamen der App zu verwalten.
    - `[HostType <HostType?>]`: Gibt an, ob der Hostname ein Standard- oder Repositoryhostname ist.
    - `[Name <String>]`: Hostname.
    - `[SslState <SslState?>]`: SSL-Typ.
    - `[Thumbprint <String>]`: FINGERABDRUCK DES SSL-Zertifikats.
    - `[ToUpdate <Boolean?>]`: Wird so <code>true</code> festgelegt, dass der vorhandene Hostname aktualisiert wird.
    - `[VirtualIP <String>]`: Virtuelle IP-Adresse, die dem Hostnamen zugewiesen ist, wenn IP-basiertes SSL aktiviert ist.
  - `[HostNamesDisabled <Boolean?>]`: <code>true</code> um die öffentlichen Hostnamen der App zu deaktivieren. Andernfalls. <code>false</code>          Wenn, <code>true</code> kann auf die App nur über die API-Verwaltungsprozesse zugegriffen werden.
  - `[HostingEnvironmentProfileId <String>]`: Ressourcen-ID der App-Dienstumgebung.
  - `[HttpsOnly <Boolean?>]`: HttpsOnly: Konfiguriert eine Website so, dass nur https-Anfragen akzeptiert werden. Problemumleitung für http-Anforderungen
  - `[HyperV <Boolean?>]`: Hyper-V Sandbox.
  - `[IdentityType <ManagedServiceIdentityType?>]`: Typ der verwalteten Dienstidentität.
  - `[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: Die Liste der benutzer zugewiesenen Identitäten, die der Ressource zugeordnet sind. Die Verweise auf benutzeridentitätswörterbücher sind ARM Ressourcen-IDs im Format '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}
    - `[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: Dies gibt an, dass diesem Objekt beliebige Eigenschaften hinzugefügt werden können.
  - `[IsXenon <Boolean?>]`: Veraltet: Hyper-V-Sandbox.
  - `[RedundancyMode <RedundancyMode?>]`: Modus "Websiteredundanz"
  - `[Reserved <Boolean?>]`: <code>true</code> falls reserviert; andernfalls <code>false</code> .
  - `[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> zum Beenden der #A0 (KUDU), wenn die App beendet wird. Andernfalls. <code>false</code> Die Standardeinstellung ist <code>false</code> .
  - `[ServerFarmId <String>]`: Ressourcen-ID des zugeordneten App-Serviceplans, formatiert mit: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".

## LINKS ZU VERWANDTEN THEMEN

