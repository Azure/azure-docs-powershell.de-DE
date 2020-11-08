---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/get-azsapmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Get-AzSapMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Get-AzSapMonitor.md
ms.openlocfilehash: 1ec82e745c7f6521a62db80ca109078bb1681172
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166693"
---
# Get-AzSapMonitor

## Synopsis
Ruft Eigenschaften eines SAP-Monitors für das angegebene Abonnement, die Ressourcengruppe und den Ressourcennamen ab.

## Syntax

### Liste (Standard)
```
Get-AzSapMonitor [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### Erhalten
```
Get-AzSapMonitor -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzSapMonitor -InputObject <IHanaOnAzureIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## Beschreibung
Ruft Eigenschaften eines SAP-Monitors für das angegebene Abonnement, die Ressourcengruppe und den Ressourcennamen ab.

## Beispiele

### Beispiel 1: Abrufen aller SAP-Monitore unter einem Abonnement
```powershell
PS C:\> Get-AzSapMonitor

Location Name              Type
-------- ----              ----
westus2  ps-sapmonitor-t01 Microsoft.HanaOnAzure/sapMonitors
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

Dieser Befehl ruft SAP-Monitore unter einem Abonnement ab.

### Beispiel 2: Abrufen eines SAP-Monitors nach Name
```powershell
PS C:\> Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-spamonitor-t01

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

Dieser Befehl ruft einen SAP-Monitor nach Name ab.

### Beispiel 3: Abrufen eines SAP-Monitors nach Objekt
```powershell
PS C:\> $sap = Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-spamonitor-t01
PS C:\> Get-AzSapMonitor -InputObject $sap

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

Mit diesem Befehl wird ein SAP-Monitor nach Objekt abgerufen.

### Beispiel 4: Abrufen eines SAP-Monitors nach Pipeline
```powershell
PS C:\> @{Id='/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/nancyc-hn1/providers/Microsoft.HanaOnAzure/sapMonitors/ps-spamonitor-t01'} | Get-AzSapMonitor

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

Dieser Befehl ruft einen SAP-Monitor nach Pipeline ab.

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
Type: Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Der Name der SAP-Monitor Ressource.

```yaml
Type: System.String
Parameter Sets: Get
Aliases: SapMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Der Name der Ressourcengruppe.

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Abonnement-Nr
Abonnement-ID, die das Microsoft Azure-Abonnement eindeutig identifiziert.
Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### Microsoft. Azure. PowerShell. Cmdlets. HanaOnAzure. Models. IHanaOnAzureIdentity

## Ausgaben

### Microsoft. Azure. PowerShell. Cmdlets. HanaOnAzure. Models. Api20200207Preview. ISapMonitor

## Notizen

Aliase

komplexe Parameter Eigenschaften

Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften. Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.


Inputobject <IHanaOnAzureIdentity> : Identity-Parameter
  - `[Id <String>]`: Ressourcen Identitäts Pfad
  - `[Location <String>]`: Der Speicherort des gelöschten Tresors.
  - `[OperationKind <AccessPolicyUpdateKind?>]`: Name des Vorgangs
  - `[ProviderInstanceName <String>]`: Name der Anbieterinstanz.
  - `[ResourceGroupName <String>]`: Name der Ressourcengruppe.
  - `[ResourceName <String>]`: Der Name der Identitäts Ressource.
  - `[SapMonitorName <String>]`: Name der SAP-Monitor Ressource.
  - `[Scope <String>]`: Der Ressourcenanbieter Bereich der Ressource. Übergeordnete Ressource, die durch verwaltete Identitäten erweitert wird.
  - `[SubscriptionId <String>]`: Abonnement-ID, die das Microsoft Azure-Abonnement eindeutig identifiziert. Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.
  - `[VaultName <String>]`: Name des Tresors

## Verwandte Links

