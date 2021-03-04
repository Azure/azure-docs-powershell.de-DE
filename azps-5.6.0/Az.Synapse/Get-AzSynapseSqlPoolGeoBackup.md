---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesqlpoolgeobackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolGeoBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolGeoBackup.md
ms.openlocfilehash: d1c0b6439b148d51506861a6bfffc6a6681343ef
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921547"
---
# Get-AzSynapseSqlPoolGeoBackup

## SYNOPSIS
Ruft eine georedundant gesicherte Sicherung eines Sql-Pools ab.

## SYNTAX

### GetByNameParameterSet (Standard)
```
Get-AzSynapseSqlPoolGeoBackup [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SqlPoolGeoBackupResourceId
```
Get-AzSynapseSqlPoolGeoBackup [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## BESCHREIBUNG
Das **Get-AzSynapseSqlPoolGeoBackup-Cmdlet** ruft eine angegebene georedundierte Sicherung eines SQL-Pools oder alle verfügbaren georedundierten Sicherungen in einem angegebenen Arbeitsbereich ab.
Eine georedundant gesicherte Ressource ist eine restorable Ressource, die Datendateien von einem separaten geografischen Speicherort verwendet.
Sie können Geo-Restore verwenden, um eine georedundant gesicherte Sicherung im Fall eines regionalen Ausfalls wiederherzustellen, um Ihren Sql Pool in einer neuen Region wiederherzustellen.

## BEISPIELE

### Beispiel 1: Erhalten einer angegebenen geo redundanten Sicherung
```powershell
PS C:\> Get-AzSynapseSqlPoolGeoBackup -ResourceGroupName ContosoResourceGroup -WorkspaceName "ContosoWorkspace" -Name "ContosoSqlPool"
```
Das Cmdlet ruft Die Geosicherung für einen SQL-Pool ab.

### Beispiel 2: Erhalten aller georedundanter Sicherungen in einem Arbeitsbereich
```
PS C:\>Get-AzSynapseSqlPoolGeoBackup -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```
Mit diesem Befehl werden alle verfügbaren georedundanziellen Sicherungen in einem angegebenen Arbeitsbereich angezeigt.

### Beispiel 3: Erhalten aller georedundanter Sicherungen in einem Arbeitsbereich mithilfe von Filtern
```
PS C:\>Get-AzSynapseSqlPoolGeoBackup -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -Name "Contoso*"
```
Mit diesem Befehl werden alle verfügbaren georedundanziellen Sicherungen für einen angegebenen Arbeitsbereich, der mit "Contoso" beginnt, angezeigt.

## PARAMETER

### -DefaultProfile
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Der Synapse Sql-Pool.

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: The Synapse Sql pool.

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Geben Sie eine Sql Pool Geo Backup Resource ID ein.

```yaml
Type: System.String
Parameter Sets: SqlPoolGeoBackupResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Name der Ressourcengruppe.

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WorkspaceName
Name des Synapse-Arbeitsbereichs.

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## EINGABEN

### Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace

### Microsoft.Azure.Commands.Synapse.Models.PSSynapseResourceGroup

## AUSGABEN

### Microsoft.Azure.Commands.Synapse.Models.PSBackupModel

## NOTIZEN

## VERWANDTE LINKS
