---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/update-azfunctionappsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppSetting.md
ms.openlocfilehash: 4255940b9cf17420fe0b522d81c6a974e9cf9324
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175609"
---
# Update-AzFunctionAppSetting

## Synopsis
Fügt App-Einstellungen in einer Funktions-APP hinzu oder aktualisiert sie.

## Syntax

### ByName (Standard)
```
Update-AzFunctionAppSetting -Name <String> -ResourceGroupName <String> -AppSetting <Hashtable>
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### ByObjectInput
```
Update-AzFunctionAppSetting -AppSetting <Hashtable> -InputObject <ISite> [-Force] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## Beschreibung
Fügt App-Einstellungen in einer Funktions-APP hinzu oder aktualisiert sie.

## Beispiele

### Beispiel 1: Hinzufügen einer neuen App-Einstellung in einer Funktions-APP.
```powershell
PS C:\> Update-AzFunctionAppSetting -Name MyAppName -ResourceGroupName MyResourceGroupName -AppSetting @{"Name1" = "Value1"}
```

Dieser Befehl fügt eine neue APP-Einstellung in einer Funktions-APP hinzu.

## Parameter

### -AppSetting
Hashtable mit Schlüsseln und Werten beschreibt die App-Einstellungen, die in der Funktions-APP hinzugefügt oder aktualisiert werden sollen.
Beispiel: @ {"myappsetting" = "123"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -Force
Erzwingt das Cmdlet zum Aktualisieren der Funktion-app-Einstellung ohne Aufforderung zur Bestätigung.

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

### -Inputobject
Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für Inputobject-Eigenschaften und Erstellen einer Hashtabelle.

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
Der Name der Funktions-APP.

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
Der Name der Ressourcengruppe, zu der die Ressource gehört.

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

### -Abonnement-Nr
Die Azure-Abonnement-ID.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### -Bestätigen
Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### Microsoft. Azure. PowerShell. Cmdlets. Functions. Models. Api20190801. ISite

## Ausgaben

### Microsoft. Azure. PowerShell. Cmdlets. Functions. Models. Api20190801. IStringDictionary

## Notizen

Aliase

komplexe Parameter Eigenschaften

Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften. Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.


Inputobject <ISite> : 
  - `Location <String>`: Ressourcen Standort.
  - `CloningInfoSourceWebAppId <String>`: Arm-Ressourcen-ID der Quell-app. Die APP-Ressourcen-ID hat das Format/Subscriptions/{subId}/resourceGroups/{resourceGroupName}/Providers/Microsoft.Web/Sites/{Sitename} für Produktions Steckplätze und/Subscriptions/{subId}/resourceGroups/{resourceGroupName}/Providers/Microsoft.Web/Sites/{Sitename}/Slots/{slotName} für andere Slots.
  - `[Kind <String>]`: Art der Ressource.
  - `[Tag <IResourceTags>]`: Ressourcenkategorien.
    - `[(Any) <String>]`: Gibt an, dass einer Eigenschaft dieses Objekt hinzugefügt werden kann.
  - `[ClientAffinityEnabled <Boolean?>]`: <code>true</code> um die Clientaffinität zu <code>false</code> aktivieren, können Sie das Senden von Sitzungs Affinitäts Cookies beenden, die Clientanforderungen in derselben Sitzung an dieselbe Instanz weiterleiten. Standardwert ist <code>true</code> .
  - `[ClientCertEnabled <Boolean?>]`: <code>true</code> um die Clientzertifikatauthentifizierung (MTLS-gegenseitige Authentifizierung) zu aktivieren, andernfalls <code>false</code> . Standardwert ist <code>false</code> .
  - `[ClientCertExclusionPath <String>]`: Clientzertifikatauthentifizierung durch Kommas getrennte Ausschluss Pfade
  - `[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: Anwendungseinstellung Außerkraftsetzungen für geklonte app. Wenn diese Einstellungen angegeben sind, überschreiben Sie die von der Quell-App geklonten Einstellungen. Andernfalls bleiben die Anwendungseinstellungen aus der Quell-APP erhalten.
    - `[(Any) <String>]`: Gibt an, dass einer Eigenschaft dieses Objekt hinzugefügt werden kann.
  - `[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> zum Klonen von benutzerdefinierten Hostnamen aus der Quell-App; andernfalls <code>false</code> .
  - `[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> zum Klonen der Quellcodeverwaltung aus der Quell-App; andernfalls <code>false</code> .
  - `[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> zum Konfigurieren des Lastenausgleichs für die Quell-und Ziel-app.
  - `[CloningInfoCorrelationId <String>]`: Korrelations-ID des Cloning-Vorgangs. Diese ID bindet mehrere Cloning-Vorgänge zusammen, um denselben Snapshot zu verwenden.
  - `[CloningInfoHostingEnvironment <String>]`: App-Dienstumgebung.
  - `[CloningInfoOverwrite <Boolean?>]`: <code>true</code> zum Überschreiben der Ziel-App; andernfalls <code>false</code> .
  - `[CloningInfoSourceWebAppLocation <String>]`: Standort der Quell-App Ex: West-und Nordeuropa
  - `[CloningInfoTrafficManagerProfileId <String>]`: Arm-Ressourcen-ID des zu verwendenden Traffic Manager-Profils, falls vorhanden. Die Datenverkehrs-Manager-Ressourcen-ID hat das Format/Subscriptions/{subId}/resourceGroups/{resourceGroupName}/Providers/Microsoft.Network/trafficManagerProfiles/{ProfileName}.
  - `[CloningInfoTrafficManagerProfileName <String>]`: Name des zu erstellenden Traffic Manager-Profils. Dies ist nur erforderlich, wenn das Traffic Manager-Profil noch nicht vorhanden ist.
  - `[Config <ISiteConfig>]`: Konfiguration der app.
    - `IsPushEnabled <Boolean>`: Ruft ein Flag ab, das angibt, ob der Push-Endpunkt aktiviert ist, oder legt dieses fest.
    - `[ActionMinProcessExecutionTime <String>]`: Minimale Zeitdauer, die der Prozess ausführen muss, bevor die Aktion ausgeführt wird
    - `[ActionType <AutoHealActionType?>]`: Vordefinierte Aktion, die ausgeführt werden soll.
    - `[AlwaysOn <Boolean?>]`: <code>true</code> Wenn immer aktiviert ist; andernfalls <code>false</code> .
    - `[ApiDefinitionUrl <String>]`: Die URL der API-Definition.
    - `[ApiManagementConfigId <String>]`: APIM-Api-Bezeichner.
    - `[AppCommandLine <String>]`: App-Befehlszeile zum Starten.
    - `[AppSetting <INameValuePair[]>]`: Anwendungseinstellungen.
      - `[Name <String>]`: Pair-Name.
      - `[Value <String>]`: Pair-Wert.
    - `[AutoHealEnabled <Boolean?>]`: <code>true</code> Wenn Auto Heal aktiviert ist; andernfalls <code>false</code> .
    - `[AutoSwapSlotName <String>]`: Automatisches austauschen des Steckplatz namens.
    - `[ConnectionString <IConnStringInfo[]>]`: Verbindungszeichenfolgen
      - `[ConnectionString <String>]`: Wert der Verbindungszeichenfolge.
      - `[Name <String>]`: Name der Verbindungszeichenfolge.
      - `[Type <ConnectionStringType?>]`: Typ der Datenbank.
    - `[CorAllowedOrigin <String[]>]`: Ruft die Liste der Ursprünge ab, die für die über-Origin-Aufrufe zulässig sein sollen (beispielsweise: http://example.com:12345) . Verwenden Sie "*", um alle zu ermöglichen.
    - `[CorSupportCredentials <Boolean?>]`: Ruft ab oder legt fest, ob CORS-Anforderungen mit Anmeldeinformationen zulässig sind. Weitere Informationen finden Sie unter         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         .
    - `[CustomActionExe <String>]`: Ausführbare Datei, die ausgeführt werden soll.
    - `[CustomActionParameter <String>]`: Parameter für die ausführbare Datei.
    - `[DefaultDocument <String[]>]`: Standarddokumente.
    - `[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> Wenn die detaillierte Fehlerprotokollierung aktiviert ist, andernfalls <code>false</code> .
    - `[DocumentRoot <String>]`: Dokumentstamm.
    - `[DynamicTagsJson <String>]`: Ruft eine JSON-Zeichenfolge ab, die eine Liste der dynamischen Tags enthält, die aus benutzeransprüchen im Push-Registrierungs Endpunkt ausgewertet werden.
    - `[ExperimentRampUpRule <IRampUpRule[]>]`: Liste der Weiterverfolgungs Regeln.
      - `[ActionHostName <String>]`: Hostname eines Slots, in den der Datenverkehr umgeleitet wird, wenn entschieden wird. Z.b.. MyApp-Stage.azurewebsites.net.
      - `[ChangeDecisionCallbackUrl <String>]`: Benutzerdefinierter Entscheidungs Algorithmus kann in TiPCallback Site Extension bereitgestellt werden, die URL angegeben werden kann. Informationen finden Sie unter TiPCallback Site Extension für das Gerüst und die Verträge.         https://www.siteextensions.net/packages/TiPCallback/
      - `[ChangeIntervalInMinute <Int32?>]`: Gibt das Intervall in Minuten an, um ReroutePercentage neu auszuwerten.
      - `[ChangeStep <Double?>]`: Im Szenario für das automatische Hochfahren ist dies der Schritt zum hinzufügen/entfernen, <code>ReroutePercentage</code> bis er \n <code>MinReroutePercentage</code> oder erreicht         <code>MaxReroutePercentage</code> . Website Metriken werden überprüft alle N Minuten <code>ChangeIntervalInMinutes</code> , die im .\nCustom-Entscheidungs Algorithmus angegeben sind, können in TiPCallback Site Extension bereitgestellt werden, in der URL angegeben werden kann <code>ChangeDecisionCallbackUrl</code> .
      - `[MaxReroutePercentage <Double?>]`: Gibt die obere Grenze an, unter der ReroutePercentage bleibt.
      - `[MinReroutePercentage <Double?>]`: Gibt die untere Grenze an, über der ReroutePercentage bleibt.
      - `[Name <String>]`: Name der Routingregel Der empfohlene Name lautet, auf den Steckplatz zu zeigen, der den Datenverkehr im Experiment empfängt.
      - `[ReroutePercentage <Double?>]`: Prozentsatz des Datenverkehrs, zu dem umgeleitet wird <code>ActionHostName</code> .
    - `[FtpsState <FtpsState?>]`: Zustand des FTP/FTP-Diensts
    - `[HandlerMapping <IHandlerMapping[]>]`: Handler-Zuordnungen.
      - `[Argument <String>]`: Befehlszeilenargumente, die an den Skriptprozessor übergeben werden.
      - `[Extension <String>]`: Anforderungen mit dieser Erweiterung werden mithilfe der angegebenen FastCGI-Anwendung verarbeitet.
      - `[ScriptProcessor <String>]`: Der absolute Pfad zur FastCGI-Anwendung.
    - `[HealthCheckPath <String>]`: Pfad für Integritätsprüfung
    - `[Http20Enabled <Boolean?>]`: Http20Enabled: konfiguriert eine Website, um Clients die Verbindung über http 2.0 zu ermöglichen.
    - `[HttpLoggingEnabled <Boolean?>]`: <code>true</code> Wenn die HTTP-Protokollierung aktiviert ist, andernfalls <code>false</code> .
    - `[IPSecurityRestriction <IIPSecurityRestriction[]>]`: IP-Sicherheitseinschränkungen für Main.
      - `[Action <String>]`: Gewähren oder Verweigern des Zugriffs für diesen IP-Bereich.
      - `[Description <String>]`: Beschreibung der IP-Einschränkungs Regel
      - `[IPAddress <String>]`: IP-Adresse die Sicherheitsbeschränkung ist gültig für.         Sie kann in Form einer reinen IPv4-Adresse (erforderliche Subnetzmaske-Eigenschaft) oder CIDR-Notation wie IPv4/Mask (Leading Bit Match) erfolgen. Für CIDR darf keine Subnetzmaske-Eigenschaft angegeben werden.
      - `[Name <String>]`: Name der IP-Einschränkungs Regel
      - `[Priority <Int32?>]`: Priorität der IP-Einschränkungs Regel
      - `[SubnetMask <String>]`: Subnetzmaske für den Bereich der IP-Adressen, für die die Einschränkung gültig ist.
      - `[SubnetTrafficTag <Int32?>]`: (interner) Subnet Traffic-Tag
      - `[Tag <IPFilterTag?>]`: Definiert, wofür dieser IP-Filter verwendet wird. Dadurch wird die IP-Filterung für Proxys unterstützt.
      - `[VnetSubnetResourceId <String>]`: Virtuelle Netzwerk-Ressourcen-ID
      - `[VnetTrafficTag <Int32?>]`: (intern) vnet Traffic-Tag
    - `[JavaContainer <String>]`: Java-Container.
    - `[JavaContainerVersion <String>]`: Java-Container Version.
    - `[JavaVersion <String>]`: Java-Version.
    - `[LimitMaxDiskSizeInMb <Int64?>]`: Maximal zulässige Datenträgergröße in MB.
    - `[LimitMaxMemoryInMb <Int64?>]`: Maximal zulässige Speicherauslastung in MB.
    - `[LimitMaxPercentageCpu <Double?>]`: Maximal zulässige CPU-Auslastung Prozentsatz.
    - `[LinuxFxVersion <String>]`: Linux-App-Framework und-Version
    - `[LoadBalancing <SiteLoadBalancing?>]`: Lastenausgleich für Websites.
    - `[LocalMySqlEnabled <Boolean?>]`: <code>true</code> um lokales MySQL zu aktivieren, andernfalls <code>false</code> .
    - `[LogsDirectorySizeLimit <Int32?>]`: Maximale Größe des http-Logs-Verzeichnisses.
    - `[MachineKeyDecryption <String>]`: Algorithmus, der für die Entschlüsselung verwendet wird.
    - `[MachineKeyDecryptionKey <String>]`: Entschlüsselungsschlüssel.
    - `[MachineKeyValidation <String>]`: MachineKey-Validierung.
    - `[MachineKeyValidationKey <String>]`: Gültigkeits Taste.
    - `[ManagedPipelineMode <ManagedPipelineMode?>]`: Verwalteter Pipelinemodus.
    - `[ManagedServiceIdentityId <Int32?>]`: Verwaltete Dienst Identitäts-ID
    - `[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: konfiguriert die für SSL-Anforderungen erforderliche minimale Version von TLS
    - `[NetFrameworkVersion <String>]`: .NET Framework-Version.
    - `[NodeVersion <String>]`: Version von Node.js.
    - `[NumberOfWorker <Int32?>]`: Anzahl der Mitarbeiter.
    - `[PhpVersion <String>]`: PHP-Version.
    - `[PowerShellVersion <String>]`: PowerShell-Version.
    - `[PreWarmedInstanceCount <Int32?>]`: Anzahl der vorgewärmten Instanzen.         Diese Einstellung gilt nur für den Verbrauch und die elastischen Pläne.
    - `[PublishingUsername <String>]`: Veröffentlichungs Benutzername.
    - `[PushKind <String>]`: Art der Ressource.
    - `[PythonVersion <String>]`: Version von Python.
    - `[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> Wenn das Remotedebuggen aktiviert ist, andernfalls <code>false</code> .
    - `[RemoteDebuggingVersion <String>]`: Remote Debugging-Version.
    - `[RequestCount <Int32?>]`: Anzahl anfordern.
    - `[RequestTimeInterval <String>]`: Zeitintervall.
    - `[RequestTracingEnabled <Boolean?>]`: <code>true</code> Wenn die Anforderungs Ablaufverfolgung aktiviert ist, andernfalls <code>false</code> .
    - `[RequestTracingExpirationTime <DateTime?>]`: Ablaufzeit der Ablaufverfolgung anfordern.
    - `[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: IP-Sicherheitseinschränkungen für SCM.
    - `[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: IP-Sicherheitseinschränkungen für SCM, um Main zu verwenden.
    - `[ScmType <ScmType?>]`: SCM-Typ.
    - `[SlowRequestCount <Int32?>]`: Anzahl anfordern.
    - `[SlowRequestTimeInterval <String>]`: Zeitintervall.
    - `[SlowRequestTimeTaken <String>]`: Zeitaufwand.
    - `[TagWhitelistJson <String>]`: Ruft eine JSON-Zeichenfolge mit einer Liste von Tags ab, die für die Verwendung durch den Push-Registrierungs Endpunkt whitelisted sind, oder legt diese fest.
    - `[TagsRequiringAuth <String>]`: Ruft eine JSON-Zeichenfolge mit einer Liste von Tags ab, für die die Benutzerauthentifizierung im Push-Registrierungs Endpunkt verwendet werden muss, oder legt diese fest.         Tags können aus alphanumerischen Zeichen und folgendem bestehen: "_"; "@"; "#"; "."; ":"; "-".         Die Validierung sollte am PushRequestHandler durchgeführt werden.
    - `[TracingOption <String>]`: Ablaufverfolgungsoptionen.
    - `[TriggerPrivateBytesInKb <Int32?>]`: Eine Regel, die auf privaten Bytes basiert.
    - `[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: Eine Regel, die auf Statuscodes basiert.
      - `[Count <Int32?>]`: Anzahl anfordern.
      - `[Status <Int32?>]`: HTTP-Statuscode.
      - `[SubStatus <Int32?>]`: Untergeordneten Status anfordern.
      - `[TimeInterval <String>]`: Zeitintervall.
      - `[Win32Status <Int32?>]`: Win32-Fehlercode.
    - `[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> So verwenden Sie den 32-Bit-Workerprozess; andernfalls <code>false</code> .
    - `[VirtualApplication <IVirtualApplication[]>]`: Virtuelle Anwendungen.
      - `[PhysicalPath <String>]`: Physikalischer Pfad.
      - `[PreloadEnabled <Boolean?>]`: <code>true</code> Wenn das Vorabladen aktiviert ist, andernfalls <code>false</code> .
      - `[VirtualDirectory <IVirtualDirectory[]>]`: Virtuelle Verzeichnisse für virtuelle Anwendungen.
        - `[PhysicalPath <String>]`: Physikalischer Pfad.
        - `[VirtualPath <String>]`: Pfad zur virtuellen Anwendung.
      - `[VirtualPath <String>]`: Virtueller Pfad.
    - `[VnetName <String>]`: Virtueller Netzwerkname.
    - `[WebSocketsEnabled <Boolean?>]`: <code>true</code> Wenn WebSocket aktiviert ist; andernfalls <code>false</code> .
    - `[WindowsFxVersion <String>]`: Xenon-App-Framework und-Version
    - `[XManagedServiceIdentityId <Int32?>]`: Explizite verwaltete Dienst Identitäts-ID
  - `[ContainerSize <Int32?>]`: Größe des Funktions Containers.
  - `[DailyMemoryTimeQuota <Int32?>]`: Maximal zulässige tägliche Speicherzeit Kontingent (gilt nur für dynamische Apps).
  - `[Enabled <Boolean?>]`: <code>true</code> Wenn die App aktiviert ist, andernfalls <code>false</code> . Wenn dieser Wert auf "false" festgelegt wird, wird die APP deaktiviert (übernimmt die APP offline).
  - `[HostNameSslState <IHostNameSslState[]>]`: Hostname SSL-Status werden verwendet, um die SSL-Bindungen für die Hostnamen der APP zu verwalten.
    - `[HostType <HostType?>]`: Gibt an, ob der Hostname ein Standard-oder Repository-Hostname ist.
    - `[Name <String>]`Hostname.
    - `[SslState <SslState?>]`: SSL-Typ.
    - `[Thumbprint <String>]`: Fingerabdruck des SSL-Zertifikats.
    - `[ToUpdate <Boolean?>]`: Auf <code>true</code> , um vorhandenen Hostnamen zu aktualisieren.
    - `[VirtualIP <String>]`: Virtuelle IP-Adresse, die dem Hostnamen zugewiesen ist, wenn IP-basiertes SSL aktiviert ist.
  - `[HostNamesDisabled <Boolean?>]`: <code>true</code> zum Deaktivieren der öffentlichen hostnames der APP; andernfalls <code>false</code> .          Wenn <code>true</code> die app nur über API-Verwaltungsprozess zugänglich ist.
  - `[HostingEnvironmentProfileId <String>]`: Ressourcen-ID der APP-Dienstumgebung.
  - `[HttpsOnly <Boolean?>]`: HttpsOnly: konfiguriert eine Website so, dass nur HTTPS-Anforderungen akzeptiert werden. Probleme beim Umleiten für HTTP-Anforderungen
  - `[HyperV <Boolean?>]`: Hyper-V-Sandbox.
  - `[IdentityType <ManagedServiceIdentityType?>]`: Typ der verwalteten Dienstidentität.
  - `[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: Die Liste der Benutzer zugewiesenen Identitäten, die der Ressource zugeordnet sind. Die Schlüssel Verweise für das Benutzer-ID-Wörterbuch sind arm-Ressourcen-IDs im folgenden Format: "/Subscriptions/{SubscriptionId}/resourceGroups/{resourceGroupName}/Providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}
    - `[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: Gibt an, dass einer Eigenschaft dieses Objekt hinzugefügt werden kann.
  - `[IsXenon <Boolean?>]`: Veraltet: Hyper-V-Sandbox.
  - `[RedundancyMode <RedundancyMode?>]`: Website Redundanzmodus
  - `[Reserved <Boolean?>]`: <code>true</code> Wenn reserviert; andernfalls; <code>false</code>
  - `[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> um die SCM-Website (KUDU) zu beenden, wenn die APP angehalten wird, andernfalls <code>false</code> . Der Standardwert ist <code>false</code> .
  - `[ServerFarmId <String>]`: Ressourcen-ID des zugehörigen App-Service Plans, formatiert als: "/Subscriptions/{subscriptionID}/resourceGroups/{GroupName}/Providers/Microsoft.Web/Serverfarms/{appServicePlanName}"

## Verwandte Links

