---
external help file: ''
Module Name: Azs.InfrastructureInsights.Admin
online version: https://docs.microsoft.com/powershell/module/azs.infrastructureinsights.admin/close-azsalert
schema: 2.0.0
ms.openlocfilehash: 885ffca453cd7a13e9ec137da89a402375eeec55
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842572"
---
# Close-AzsAlert

## Synopsis
Schließt die angegebene Benachrichtigung.

## Syntax

### CloseExpanded (Standard)
```
Close-AzsAlert -Name <String> -User <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-AlertId <String>] [-AlertProperty <Hashtable>] [-ClosedByUserAlias <String>]
 [-ClosedTimestamp <String>] [-CreatedTimestamp <String>] [-Description <IDictionary[]>] [-FaultId <String>]
 [-FaultTypeId <String>] [-HasValidRemediationAction] [-ImpactedResourceDisplayName <String>]
 [-ImpactedResourceId <String>] [-LastUpdatedTimestamp <String>] [-Location1 <String>]
 [-Remediation <IDictionary[]>] [-ResourceProviderRegistrationId <String>] [-ResourceRegistrationId <String>]
 [-Severity <String>] [-State <String>] [-Tag <Hashtable>] [-Title <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### Schließen
```
Close-AzsAlert -Name <String> -User <String> -Alert <IAlert> [-Location <String>]
 [-ResourceGroupName <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### CloseViaIdentity
```
Close-AzsAlert -InputObject <IInfrastructureInsightsAdminIdentity> -User <String> -Alert <IAlert>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### CloseViaIdentityExpanded
```
Close-AzsAlert -InputObject <IInfrastructureInsightsAdminIdentity> -User <String> [-Location <String>]
 [-AlertId <String>] [-AlertProperty <Hashtable>] [-ClosedByUserAlias <String>] [-ClosedTimestamp <String>]
 [-CreatedTimestamp <String>] [-Description <IDictionary[]>] [-FaultId <String>] [-FaultTypeId <String>]
 [-HasValidRemediationAction] [-ImpactedResourceDisplayName <String>] [-ImpactedResourceId <String>]
 [-LastUpdatedTimestamp <String>] [-Remediation <IDictionary[]>] [-ResourceProviderRegistrationId <String>]
 [-ResourceRegistrationId <String>] [-Severity <String>] [-State <String>] [-Tag <Hashtable>]
 [-Title <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## Beschreibung
Schließt die angegebene Benachrichtigung.

## Beispiele

### Beispiel 1:
```powershell
PS C:\> Close-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0
```

Schließen Sie eine Benachrichtigung nach Namen.

### Beispiel 2:
```powershell
PS C:\> Get-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0 | Close-AzsAlert
```

Schließen Sie eine Benachrichtigung über Piping.

## Parameter

### -Alert
Dieses Objekt stellt eine Warnungs Ressource dar.
Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für Warnungseigenschaften und Erstellen einer Hashtabelle.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IAlert
Parameter Sets: Close, CloseViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### -Warnungs-Nr.
Ruft die ID der Benachrichtigung ab oder legt diese fest.

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -Alertproperty
Eigenschaften der Benachrichtigung.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -ClosedByUserAlias
Benutzer-Alias, der die Benachrichtigung geschlossen hat.

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -ClosedTimestamp
Timestamp, wenn die Benachrichtigung geschlossen wurde.

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -CreatedTimestamp
Timestamp, wenn die Benachrichtigung erstellt wurde.

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

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

### -Beschreibung
Beschreibung der Benachrichtigung.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IDictionary[]
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -Fehler-Nr
Ruft die Fehler-ID der Benachrichtigung ab oder legt diese fest.

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -FaultTypeId
Ruft die Fault Type-ID der Benachrichtigung ab oder legt diese fest.

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -HasValidRemediationAction
Gibt an, ob die Benachrichtigung wiederhergestellt werden kann.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -ImpactedResourceDisplayName
Anzeigename für das betroffene Element

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -ImpactedResourceId
Ruft die Ressourcen-ID für das betroffene Element ab oder legt diese fest.

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -Inputobject
Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity
Parameter Sets: CloseViaIdentity, CloseViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### -LastUpdatedTimestamp
Timestamp, wenn die Benachrichtigung zuletzt aktualisiert wurde.

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -Standort
Name der Region

```yaml
Type: System.String
Parameter Sets: Close, CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### -Location1
Der Azure-Bereich, in dem die Ressource wohnt

```yaml
Type: System.String
Parameter Sets: CloseExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -Name
Der Name der Benachrichtigung.

```yaml
Type: System.String
Parameter Sets: Close, CloseExpanded
Aliases: AlertName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -Behebung
Ruft die Administrator freundlichen Behebungsanweisungen für die Benachrichtigung ab oder legt diese fest.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IDictionary[]
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -ResourceGroupName
Der Name der Ressourcengruppe.

```yaml
Type: System.String
Parameter Sets: Close, CloseExpanded
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### -ResourceProviderRegistrationId
Ruft die Registrierungs-ID des Diensts ab, zu dem die Benachrichtigung gehört, oder legt diese fest.

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -ResourceRegistrationId
Ruft die Registrierungs-ID der Ressource ab, die der Benachrichtigung zugeordnet ist, oder legt diese fest.
Wenn die Benachrichtigung keiner Ressource zugeordnet ist, ist die Ressourcen Registrierungs-ID NULL.

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -Schweregrad
Schweregrad der Benachrichtigung

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -Bundesland
Status der Benachrichtigung.

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -Abonnement-Nr
Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.
Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.

```yaml
Type: System.String
Parameter Sets: Close, CloseExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### -Tag
Ressourcenkategorien.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -Title
Ruft die Ressourcen-ID für das betroffene Element ab oder legt diese fest.

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -User
Der zum Ausführen des Vorgangs verwendete Benutzername.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
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

### Microsoft. Azure. PowerShell. Cmdlets. InfrastructureInsightsAdmin. Models. Api20160501. IAlert

### Microsoft. Azure. PowerShell. Cmdlets. InfrastructureInsightsAdmin. Models. IInfrastructureInsightsAdminIdentity

## Ausgaben

### Microsoft. Azure. PowerShell. Cmdlets. InfrastructureInsightsAdmin. Models. Api20160501. IAlert



## Notizen

Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften. Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.

Warnung <IAlert> : dieses Objekt stellt eine Warnungs Ressource dar.
  - `[Location <String>]`: Der Azure-Bereich, in dem die Ressource wohnt
  - `[Tag <ITrackedResourceTags>]`: Ressourcenkategorien.
    - `[(Any) <String>]`: Gibt an, dass einer Eigenschaft dieses Objekt hinzugefügt werden kann.
  - `[AlertId <String>]`: Ruft die ID der Benachrichtigung ab oder legt diese fest.
  - `[AlertProperty <IAlertModelAlertProperties>]`: Eigenschaften der Benachrichtigung.
    - `[(Any) <String>]`: Gibt an, dass einer Eigenschaft dieses Objekt hinzugefügt werden kann.
  - `[ClosedByUserAlias <String>]`: Benutzer-Alias, der die Benachrichtigung geschlossen hat.
  - `[ClosedTimestamp <String>]`: Timestamp, wenn die Benachrichtigung geschlossen wurde.
  - `[CreatedTimestamp <String>]`: Timestamp, wenn die Benachrichtigung erstellt wurde.
  - `[Description <IDictionary[]>]`: Beschreibung der Benachrichtigung.
  - `[FaultId <String>]`: Ruft die Fehler-ID der Benachrichtigung ab oder legt diese fest.
  - `[FaultTypeId <String>]`: Ruft die Fault Type-ID der Benachrichtigung ab oder legt diese fest.
  - `[HasValidRemediationAction <Boolean?>]`: Gibt an, ob die Benachrichtigung wiederhergestellt werden kann.
  - `[ImpactedResourceDisplayName <String>]`: Anzeigename für das betroffene Element
  - `[ImpactedResourceId <String>]`: Ruft die Ressourcen-ID für das betroffene Element ab oder legt diese fest.
  - `[LastUpdatedTimestamp <String>]`: Timestamp, wenn die Benachrichtigung zuletzt aktualisiert wurde.
  - `[Remediation <IDictionary[]>]`: Ruft die Administrator freundlichen Behebungsanweisungen für die Benachrichtigung ab oder legt diese fest.
  - `[ResourceProviderRegistrationId <String>]`: Ruft die Registrierungs-ID des Diensts ab, zu dem die Benachrichtigung gehört, oder legt diese fest.
  - `[ResourceRegistrationId <String>]`: Ruft die Registrierungs-ID der Ressource ab, die der Benachrichtigung zugeordnet ist, oder legt diese fest. Wenn die Benachrichtigung keiner Ressource zugeordnet ist, ist die Ressourcen Registrierungs-ID NULL.
  - `[Severity <String>]`: Schweregrad der Benachrichtigung.
  - `[State <String>]`: Zustand der Benachrichtigung.
  - `[Title <String>]`: Ruft die Ressourcen-ID für das betroffene Element ab oder legt diese fest.

Inputobject <IInfrastructureInsightsAdminIdentity> : Identity-Parameter
  - `[AlertName <String>]`: Name der Benachrichtigung.
  - `[Id <String>]`: Ressourcen Identitäts Pfad
  - `[Location <String>]`: Name der Region
  - `[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.
  - `[ResourceRegistrationId <String>]`: Ressourcen Registrierungs-ID.
  - `[ServiceHealth <String>]`: Name des Dienststatus.
  - `[ServiceRegistrationId <String>]`: Dienst Registrierungs-ID.
  - `[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren. Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.

## Verwandte Links

