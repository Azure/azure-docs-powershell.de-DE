---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstanceDatabase.md
ms.openlocfilehash: 6c8fdc5b54ca802c8c23df577fc0e0e39de0ba16
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98460699"
---
# New-AzSqlInstanceDatabase

## SYNOPSIS
Erstellt eine Azure SQL Verwaltete Instanzdatenbank.

## SYNTAX

### CreateNewInstanceDatabaseFromInputParameters (Standard)
```
New-AzSqlInstanceDatabase [-Name] <String> [-InstanceName] <String> [-ResourceGroupName] <String>
 [-Collation <String>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### CreateNewInstanceDatabaseFromAzureSqlManagedInstanceModelInstanceDefinition
```
New-AzSqlInstanceDatabase [-Name] <String> [-Collation <String>] [-Tag <Hashtable>]
 [-InstanceObject] <AzureSqlManagedInstanceModel> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### CreateNewInstanceDatabaseFromAzureSqlInstanceResourceId
```
New-AzSqlInstanceDatabase [-Name] <String> [-Collation <String>] [-Tag <Hashtable>]
 [-InstanceResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "New-AzSqlInstanceDatabase"** erstellt eine Azure SQL Verwaltete Instanzdatenbank.

## BEISPIELE

### Beispiel 1: Erstellen einer Datenbank für eine bestimmte Instanz
```
PS C:\>New-AzSqlInstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/databases/Database01
Name                     : Database01
Tags                     :
Collation                : SQL_Latin1_General_CP1_CI_AS
Status                   : Online
CreationDate             : 4/27/2018 2:30:07 PM
EarliestRestorePoint     : 4/27/2018 2:40:47 PM
RestorePointInTime       :
DefaultSecondaryLocation : West US 2
CatalogCollation         :
CreateMode               :
StorageContainerUri      :
StorageContainerSasToken :
SourceDatabaseId         :
FailoverGroupId          :
```

Mit diesem Befehl wird eine Instanzdatenbank namens "Database01" für "managedInstance1" erstellt.

## PARAMETERS

### -AsJob
Ausführen des Cmdlets im Hintergrund

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

### -Collation
Die Sortierung der Azure SQL Zu verwendende Instanzdatenbanksortierung.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -InstanceName
Der Instanzname.

```yaml
Type: System.String
Parameter Sets: CreateNewInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InstanceObject
Das Instanzobjekt

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: CreateNewInstanceDatabaseFromAzureSqlManagedInstanceModelInstanceDefinition
Aliases: ParentObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -InstanceResourceId
Die Instanzressourcen-ID

```yaml
Type: System.String
Parameter Sets: CreateNewInstanceDatabaseFromAzureSqlInstanceResourceId
Aliases: ParentResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Der Name der Azure SQL Instanzdatenbank, die erstellt werden soll.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: InstanceDatabaseName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Der Name der Ressourcengruppe.

```yaml
Type: System.String
Parameter Sets: CreateNewInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tag
Die Tags, die der Azure Sql-Instanzdatenbank zugeordnet werden sollen

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
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

### Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel

### System.String

## AUSGABEN

### Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN
