---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/get-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Get-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Get-AzAppConfigurationStore.md
ms.openlocfilehash: 88847cbb128f5545a235eb2c5c02043231ff1078
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100171755"
---
# Get-AzAppConfigurationStore

## SYNOPSIS
Laden Sie Konfigurationsspeicher für Apps herunter, oder listen Sie sie auf.

## SYNTAX

### Liste (Standard)
```
Get-AzAppConfigurationStore [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### Erhalten
```
Get-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzAppConfigurationStore -InputObject <IAppConfigurationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### Liste1
```
Get-AzAppConfigurationStore -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## BESCHREIBUNG
Laden Sie Konfigurationsspeicher für Apps herunter, oder listen Sie sie auf.

## BEISPIELE

### Beispiel 1: Auflisten aller App-Konfigurationsspeicher unter einem Abonnement
```powershell
PS C:\> Get-AzAppConfigurationStore

Location Name               Type
-------- ----               ----
eastus   appconfig-test01   Microsoft.AppConfiguration/configurationStores
eastus   contoso-app-config Microsoft.AppConfiguration/configurationStores
```

Mit diesem Befehl werden alle App-Konfigurationsspeicher unter einem Abonnement aufgeführt.

### Beispiel 2: Auflisten aller App-Konfigurationsspeicher unter einer Ressourcengruppe
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
eastus   appconfig-test02 Microsoft.AppConfiguration/configurationStores
```

Mit diesem Befehl werden alle App-Konfigurationsspeicher unter einer Ressourcengruppe aufgeführt.

### Beispiel 3: Erstellen eines App-Konfigurationsspeichers nach Name
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test01

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
```

Dieser Befehl ruft einen App-Konfigurationsspeicher nach Name ab.

### Beispiel 4: Herunterladen eines App-Konfigurationsspeichers per Pipeline
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test01 | Get-AzAppConfigurationStore

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
```

Dieser Befehl ruft einen App-Konfigurationsspeicher per Pipeline ab.

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
Type: Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Der Name des Konfigurationsspeichers.

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

### -ResourceGroupName
Der Name der Ressourcengruppe, zu der die Containerregistrierung gehört.

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
Die Microsoft Azure-Abonnement-ID.

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

### Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity

## AUSGABEN

### Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IConfigurationStore

## HINWEISE

ALIASE

KOMPLEXE PARAMETEREIGENSCHAFTEN

Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften. Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.


INPUTOBJECT <IAppConfigurationIdentity> : Identity Parameter
  - `[ConfigStoreName <String>]`: Der Name des Konfigurationsspeichers.
  - `[GroupName <String>]`: Der Name der Ressourcengruppe für private Verknüpfungen.
  - `[Id <String>]`: Ressourcenidentitätspfad
  - `[PrivateEndpointConnectionName <String>]`: Name der Verbindung für den privaten Endpunkt
  - `[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, zu der die Containerregistrierung gehört.
  - `[SubscriptionId <String>]`: Die Microsoft Azure-Abonnement-ID.

## LINKS ZU VERWANDTEN THEMEN

