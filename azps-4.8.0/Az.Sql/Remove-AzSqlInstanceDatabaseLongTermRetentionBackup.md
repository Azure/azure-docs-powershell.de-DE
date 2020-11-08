---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstancedatabaselongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: 3dbcbed2466f9bb6b229a6dcfa710d6745a72eac
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166015"
---
# <span data-ttu-id="aa0cf-101">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="aa0cf-101">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="aa0cf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="aa0cf-102">SYNOPSIS</span></span>
<span data-ttu-id="aa0cf-103">Löscht eine langfristige Aufbewahrungs Sicherung.</span><span class="sxs-lookup"><span data-stu-id="aa0cf-103">Deletes a long term retention backup.</span></span>

## <span data-ttu-id="aa0cf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="aa0cf-104">SYNTAX</span></span>

### <span data-ttu-id="aa0cf-105">RemoveBackupDefault (Standard)</span><span class="sxs-lookup"><span data-stu-id="aa0cf-105">RemoveBackupDefault (Default)</span></span>
```
Remove-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-BackupName] <String> [-ResourceGroupName <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa0cf-106">RemoveBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="aa0cf-106">RemoveBackupByInputObject</span></span>
```
Remove-AzSqlInstanceDatabaseLongTermRetentionBackup
 [-InputObject] <AzureSqlManagedDatabaseLongTermRetentionBackupModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa0cf-107">RemoveBackupByResourceId</span><span class="sxs-lookup"><span data-stu-id="aa0cf-107">RemoveBackupByResourceId</span></span>
```
Remove-AzSqlInstanceDatabaseLongTermRetentionBackup [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa0cf-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aa0cf-108">DESCRIPTION</span></span>
<span data-ttu-id="aa0cf-109">Das Cmdlet **Remove-AzSqlInstanceDatabaseLongTermRetentionBackup** löscht die angegebene Sicherung.</span><span class="sxs-lookup"><span data-stu-id="aa0cf-109">The **Remove-AzSqlInstanceDatabaseLongTermRetentionBackup** cmdlet deletes the backup specified.</span></span>

## <span data-ttu-id="aa0cf-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="aa0cf-110">EXAMPLES</span></span>

### <span data-ttu-id="aa0cf-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="aa0cf-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSqlInstanceDatabaseLongTermRetentionBackup -Location southeastasia -ResourceGroupName testResourceGroup -InstanceName testInstance -DatabaseName test -BackupName 15be823c-7e2c-49d8-819f-a3fdcad92215;132268250550000000
```

<span data-ttu-id="aa0cf-112">Löscht die Sicherung mit dem Namen 15be823c-7e2c-49d8-819f-a3fdcad92215; 132268250550000000</span><span class="sxs-lookup"><span data-stu-id="aa0cf-112">Deletes the backup with name 15be823c-7e2c-49d8-819f-a3fdcad92215;132268250550000000</span></span>

## <span data-ttu-id="aa0cf-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="aa0cf-113">PARAMETERS</span></span>

### <span data-ttu-id="aa0cf-114">-BackupName</span><span class="sxs-lookup"><span data-stu-id="aa0cf-114">-BackupName</span></span>
<span data-ttu-id="aa0cf-115">Der Name der Sicherung.</span><span class="sxs-lookup"><span data-stu-id="aa0cf-115">The name of the backup.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa0cf-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="aa0cf-116">-DatabaseName</span></span>
<span data-ttu-id="aa0cf-117">Der Name der verwalteten Datenbank, aus der die Sicherung erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="aa0cf-117">The name of the Managed Database the backup is from.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa0cf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa0cf-118">-DefaultProfile</span></span>
<span data-ttu-id="aa0cf-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="aa0cf-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa0cf-120">-Force</span><span class="sxs-lookup"><span data-stu-id="aa0cf-120">-Force</span></span>
<span data-ttu-id="aa0cf-121">Bestätigungsmeldung zum Durchführen der Aktion überspringen</span><span class="sxs-lookup"><span data-stu-id="aa0cf-121">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="aa0cf-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="aa0cf-122">-InputObject</span></span>
<span data-ttu-id="aa0cf-123">Das zu entfernende Datenbank-Backup-Objekt für langfristige Aufbewahrung.</span><span class="sxs-lookup"><span data-stu-id="aa0cf-123">The Database Long Term Retention Backup object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel
Parameter Sets: RemoveBackupByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aa0cf-124">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="aa0cf-124">-InstanceName</span></span>
<span data-ttu-id="aa0cf-125">Der Name der verwalteten Instanz, unter der sich die Sicherung befindet.</span><span class="sxs-lookup"><span data-stu-id="aa0cf-125">The name of the Managed Instance the backup is under.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa0cf-126">-Standort</span><span class="sxs-lookup"><span data-stu-id="aa0cf-126">-Location</span></span>
<span data-ttu-id="aa0cf-127">Der Speicherort der verwalteten Quellinstanz der Sicherung.</span><span class="sxs-lookup"><span data-stu-id="aa0cf-127">The location of the backups' source Managed Instance.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa0cf-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa0cf-128">-ResourceGroupName</span></span>
<span data-ttu-id="aa0cf-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="aa0cf-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa0cf-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="aa0cf-130">-ResourceId</span></span>
<span data-ttu-id="aa0cf-131">Die Ressourcen-ID der zu entfernenden Datenbank-Backup-Aufbewahrungsdauer.</span><span class="sxs-lookup"><span data-stu-id="aa0cf-131">The Resource ID of the Database Long Term Retention Backup to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa0cf-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="aa0cf-132">-Confirm</span></span>
<span data-ttu-id="aa0cf-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="aa0cf-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa0cf-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa0cf-134">-WhatIf</span></span>
<span data-ttu-id="aa0cf-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="aa0cf-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa0cf-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="aa0cf-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa0cf-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa0cf-137">CommonParameters</span></span>
<span data-ttu-id="aa0cf-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa0cf-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa0cf-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aa0cf-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa0cf-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="aa0cf-140">INPUTS</span></span>

### <span data-ttu-id="aa0cf-141">Microsoft. Azure. Commands. SQL. ManagedDatabaseBackup. Model. AzureSqlManagedDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="aa0cf-141">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel</span></span>

### <span data-ttu-id="aa0cf-142">System. String</span><span class="sxs-lookup"><span data-stu-id="aa0cf-142">System.String</span></span>

## <span data-ttu-id="aa0cf-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="aa0cf-143">OUTPUTS</span></span>

### <span data-ttu-id="aa0cf-144">Microsoft. Azure. Commands. SQL. ManagedDatabaseBackup. Model. AzureSqlManagedDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="aa0cf-144">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="aa0cf-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="aa0cf-145">NOTES</span></span>

## <span data-ttu-id="aa0cf-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="aa0cf-146">RELATED LINKS</span></span>

[<span data-ttu-id="aa0cf-147">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="aa0cf-147">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="aa0cf-148">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="aa0cf-148">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="aa0cf-149">Satz-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="aa0cf-149">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="aa0cf-150">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="aa0cf-150">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)