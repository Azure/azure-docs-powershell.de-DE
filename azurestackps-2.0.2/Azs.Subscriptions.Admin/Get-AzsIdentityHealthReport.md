---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsidentityhealthreport
schema: 2.0.0
ms.openlocfilehash: 995ddf191f870fee9d27438ebea6d29729ca4c9f
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94007323"
---
# Get-AzsIdentityHealthReport

## Synopsis
Überprüft den Identitätsstatus

## Syntax

### Überprüfen (Standard)
```
Get-AzsIdentityHealthReport [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### CheckViaIdentity
```
Get-AzsIdentityHealthReport -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## Beschreibung
Überprüft den Identitätsstatus

## Beispiele

### Beispiel 1
```powershell
PS C:\> Get-AzsIdentityHealthReport

ReportEndTimeUtc      ReportStartTimeUtc    Status 
----------------      ------------------    ------ 
3/12/2020 11:41:08 PM 3/12/2020 11:40:50 PM Healthy
```

Abrufen des Status des Identitäts Zustands.

## Parameter

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

### -Inputobject
Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity
Parameter Sets: CheckViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### -Abonnement-Nr
Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren. Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.

```yaml
Type: System.String[]
Parameter Sets: Check
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

### Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity

## Ausgaben

### Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. Api20151101. IIdentityHealthCheckReportDefinition

Aliase

## Notizen

Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften. Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.

Inputobject <ISubscriptionsAdminIdentity> : Identity-Parameter
  - `[DelegatedProvider <String>]`: DelegatedProvider-Bezeichner.
  - `[DelegatedProviderSubscriptionId <String>]`: Bezeichner des Delegierten Anbieter Abonnements.
  - `[Id <String>]`: Ressourcen Identitäts Pfad
  - `[Location <String>]`: Der AzureStack-Speicherort.
  - `[ManifestName <String>]`: Der Name des Manifests.
  - `[Offer <String>]`: Name eines Angebots.
  - `[OfferDelegationName <String>]`: Name einer Angebots Delegation.
  - `[OperationsStatusName <String>]`: Der Name des Vorgangsstatus.
  - `[Plan <String>]`: Name des Plans.
  - `[PlanAcquisitionId <String>]`: Der Plan Erfassung-Bezeichner
  - `[Quota <String>]`: Name des Kontingents.
  - `[ResourceGroupName <String>]`: Die Ressourcengruppe, unter der sich die Ressource befindet.
  - `[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren. Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.
  - `[TargetSubscriptionId <String>]`: Die zielabonnement-ID.
  - `[Tenant <String>]`: Name des Verzeichnis Mandanten.

## Verwandte Links

