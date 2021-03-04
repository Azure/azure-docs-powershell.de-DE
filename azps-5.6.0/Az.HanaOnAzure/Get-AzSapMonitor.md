---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/powershell/module/az.hanaonazure/get-azsapmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Get-AzSapMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Get-AzSapMonitor.md
ms.openlocfilehash: 0de9aa6dd623efa379a6123570e766d30c850ab8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101949304"
---
# Get-AzSapMonitor

## SYNOPSIS
Ruft Eigenschaften eines SAP-Monitors für das angegebene Abonnement, die Ressourcengruppe und den Ressourcennamen ab.

## SYNTAX

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

## BESCHREIBUNG
Ruft Eigenschaften eines SAP-Monitors für das angegebene Abonnement, die Ressourcengruppe und den Ressourcennamen ab.

## BEISPIELE

### Beispiel 1: Alle SAP-Monitore unter einem Abonnement erhalten
```powershell
PS C:\> Get-AzSapMonitor

Location Name              Type
-------- ----              ----
westus2  ps-sapmonitor-t01 Microsoft.HanaOnAzure/sapMonitors
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

Dieser Befehl ruft SAP-Monitore unter einem Abonnement ab.

### Beispiel 2: Benennen eines SAP-Monitors
```powershell
PS C:\> Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-spamonitor-t01

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

Dieser Befehl ruft einen SAP-Monitor namens ab.

### Beispiel 3: Erstellen eines SAP-Monitors nach Objekt
```powershell
PS C:\> $sap = Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-spamonitor-t01
PS C:\> Get-AzSapMonitor -InputObject $sap

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

Dieser Befehl ruft einen SAP-Monitor nach Objekt ab.

### Beispiel 4: Erhalten eines SAP-Monitors per Pipeline
```powershell
PS C:\> @{Id='/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/nancyc-hn1/providers/Microsoft.HanaOnAzure/sapMonitors/ps-spamonitor-t01'} | Get-AzSapMonitor

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

Dieser Befehl ruft einen SAP-Monitor per Pipeline ab.

## PARAMETER

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

### -InputObject
Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.

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
Name der SAP-Monitorressource.

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
Name der Ressourcengruppe.

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

### -SubscriptionId
Abonnement-ID, mit der Microsoft Azure-Abonnement eindeutig identifiziert wird.
Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.

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
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## EINGABEN

### Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity

## AUSGABEN

### Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.ISapMonitor

## NOTIZEN

ALIASE

KOMPLEXE PARAMETEREIGENSCHAFTEN

Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält. Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.


INPUTOBJECT <IHanaOnAzureIdentity> : Identitätsparameter
  - `[Id <String>]`: Ressourcenidentitätspfad
  - `[Location <String>]`: Der Speicherort des gelöschten Tresors.
  - `[OperationKind <AccessPolicyUpdateKind?>]`: Name des Vorgangs
  - `[ProviderInstanceName <String>]`: Name der Anbieterinstanz.
  - `[ResourceGroupName <String>]`: Name der Ressourcengruppe.
  - `[ResourceName <String>]`: Der Name der Identitätsressource.
  - `[SapMonitorName <String>]`: Name der SAP-Monitorressource.
  - `[Scope <String>]`: Der Ressourcenanbieterbereich der Ressource. Übergeordnete Ressource, die durch verwaltete Identitäten erweitert wird.
  - `[SubscriptionId <String>]`: Abonnement-ID, mit der Microsoft Azure-Abonnement eindeutig identifiziert wird. Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.
  - `[VaultName <String>]`: Name des Tresors

## VERWANDTE LINKS

