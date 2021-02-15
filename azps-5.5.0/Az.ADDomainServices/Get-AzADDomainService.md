---
external help file: ''
Module Name: Az.ADDomainServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.addomainservices/get-azaddomainservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/Get-AzADDomainService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/Get-AzADDomainService.md
ms.openlocfilehash: ec52bea37eed3bb785da80beb8dfba02d0a426cc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100143836"
---
# Get-AzADDomainService

## SYNOPSIS
Der Get Domain Service-Vorgang ruft eine json-Darstellung des Domain Service ab.

## SYNTAX

### Liste (Standard)
```
Get-AzADDomainService [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### Erhalten
```
Get-AzADDomainService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzADDomainService -InputObject <IAdDomainServicesIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### Liste1
```
Get-AzADDomainService -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## BESCHREIBUNG
Der Get Domain Service-Vorgang ruft eine json-Darstellung des Domain Service ab.

## BEISPIELE

### Beispiel 1: Standardmäßiges "Get All ADDomainService"
```powershell
PS C:\> Get-AzADDomainService

Name          Domain Name       Location Sku
----          -----------       -------- ---
youriADdomain youriAddomain.com westus   Enterprise
```

Standardmäßiges "Get All ADDomainService"

### Beispiel 2: "ADDomainService by ResourceGroup" und den Namen
```powershell
PS C:\> Get-AzADDomainService -Name youriADdomain -ResourceGroupName youriADdomain

Name          Domain Name       Location Sku
----          -----------       -------- ---
youriADdomain youriAddomain.com westus   Enterprise
```

ADDomainService nach ResourceGroup und Name

### Beispiel 3: "Get all ADDomainService By ResourceGroup"
```powershell
PS C:\> Get-AzADDomainService -ResourceGroupName youriADdomain

Name          Domain Name       Location Sku
----          -----------       -------- ---
youriADdomain youriAddomain.com westus   Enterprise
```

"Get all ADDomainService By ResourceGroup"

### Beispiel 4: Erhalten von ADDomainService von InputObject
```powershell
PS C:\> $getAzAddomain = Get-AzADDomainService -Name youriADdomain -ResourceGroupName youriADdomain
Get-AzADDomainService -InputObject $getAzAddomain

Name          Domain Name       Location Sku
----          -----------       -------- ---
youriADdomain youriAddomain.com westus   Enterprise
```

ADDomainService von InputObject erhalten

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

### -InputObject
Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.IAdDomainServicesIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Der Name des Domänendiensts.

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DomainServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Der Name der Ressourcengruppe im Abonnement des Benutzers.
Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Ruft Abonnementanmeldeinformationen ab, mit denen das Microsoft Azure-Abonnement eindeutig identifiziert wird.
Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.IAdDomainServicesIdentity

## AUSGABEN

### Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IDomainService

## HINWEISE

ALIASE

KOMPLEXE PARAMETEREIGENSCHAFTEN

Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften. Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.


INPUTOBJECT <IAdDomainServicesIdentity> : Identity Parameter
  - `[DomainServiceName <String>]`: Der Name des Domänendiensts.
  - `[Id <String>]`: Ressourcenidentitätspfad
  - `[ResourceGroupName <String>]`: Der Name der Ressourcengruppe im Abonnement des Benutzers. Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.
  - `[SubscriptionId <String>]`: Ruft Abonnementanmeldeinformationen ab, mit denen das Microsoft Azure-Abonnement eindeutig identifiziert wird. Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.

## LINKS ZU VERWANDTEN THEMEN

