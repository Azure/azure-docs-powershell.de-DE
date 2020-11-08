---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstancedatabaselongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: c52b0a9cafbb5a3e61af3a044ef834e499e88bc5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003016"
---
# <span data-ttu-id="588b7-101">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="588b7-101">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="588b7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="588b7-102">SYNOPSIS</span></span>
<span data-ttu-id="588b7-103">Löscht eine langfristige Aufbewahrungs Sicherung.</span><span class="sxs-lookup"><span data-stu-id="588b7-103">Deletes a long term retention backup.</span></span>

## <span data-ttu-id="588b7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="588b7-104">SYNTAX</span></span>

### <span data-ttu-id="588b7-105">RemoveBackupDefault (Standard)</span><span class="sxs-lookup"><span data-stu-id="588b7-105">RemoveBackupDefault (Default)</span></span>
```
Remove-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-BackupName] <String> [-ResourceGroupName <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="588b7-106">RemoveBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="588b7-106">RemoveBackupByInputObject</span></span>
```
Remove-AzSqlInstanceDatabaseLongTermRetentionBackup
 [-InputObject] <AzureSqlManagedDatabaseLongTermRetentionBackupModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="588b7-107">RemoveBackupByResourceId</span><span class="sxs-lookup"><span data-stu-id="588b7-107">RemoveBackupByResourceId</span></span>
```
Remove-AzSqlInstanceDatabaseLongTermRetentionBackup [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="588b7-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="588b7-108">DESCRIPTION</span></span>
<span data-ttu-id="588b7-109">Das Cmdlet **Remove-AzSqlInstanceDatabaseLongTermRetentionBackup** löscht die angegebene Sicherung.</span><span class="sxs-lookup"><span data-stu-id="588b7-109">The **Remove-AzSqlInstanceDatabaseLongTermRetentionBackup** cmdlet deletes the backup specified.</span></span>

## <span data-ttu-id="588b7-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="588b7-110">EXAMPLES</span></span>

### <span data-ttu-id="588b7-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="588b7-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSqlInstanceDatabaseLongTermRetentionBackup -Location southeastasia -ResourceGroupName testResourceGroup -InstanceName testInstance -DatabaseName test -BackupName 15be823c-7e2c-49d8-819f-a3fdcad92215;132268250550000000
```

<span data-ttu-id="588b7-112">Löscht die Sicherung mit dem Namen 15be823c-7e2c-49d8-819f-a3fdcad92215; 132268250550000000</span><span class="sxs-lookup"><span data-stu-id="588b7-112">Deletes the backup with name 15be823c-7e2c-49d8-819f-a3fdcad92215;132268250550000000</span></span>

## <span data-ttu-id="588b7-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="588b7-113">PARAMETERS</span></span>

### <span data-ttu-id="588b7-114">-BackupName</span><span class="sxs-lookup"><span data-stu-id="588b7-114">-BackupName</span></span>
<span data-ttu-id="588b7-115">Der Name der Sicherung.</span><span class="sxs-lookup"><span data-stu-id="588b7-115">The name of the backup.</span></span>

```yaml
Type: String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="588b7-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="588b7-116">-DatabaseName</span></span>
<span data-ttu-id="588b7-117">Der Name der verwalteten Datenbank, aus der die Sicherung erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="588b7-117">The name of the Managed Database the backup is from.</span></span>

```yaml
Type: String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="588b7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="588b7-118">-DefaultProfile</span></span>
<span data-ttu-id="588b7-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="588b7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="588b7-120">-Force</span><span class="sxs-lookup"><span data-stu-id="588b7-120">-Force</span></span>
<span data-ttu-id="588b7-121">Bestätigungsmeldung zum Durchführen der Aktion überspringen</span><span class="sxs-lookup"><span data-stu-id="588b7-121">Skip confirmation message for performing the action</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="588b7-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="588b7-122">-InputObject</span></span>
<span data-ttu-id="588b7-123">Das zu entfernende Datenbank-Backup-Objekt für langfristige Aufbewahrung.</span><span class="sxs-lookup"><span data-stu-id="588b7-123">The Database Long Term Retention Backup object to remove.</span></span>

```yaml
Type: AzureSqlManagedDatabaseLongTermRetentionBackupModel
Parameter Sets: RemoveBackupByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="588b7-124">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="588b7-124">-InstanceName</span></span>
<span data-ttu-id="588b7-125">Der Name der verwalteten Instanz, unter der sich die Sicherung befindet.</span><span class="sxs-lookup"><span data-stu-id="588b7-125">The name of the Managed Instance the backup is under.</span></span>

```yaml
Type: String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="588b7-126">-Standort</span><span class="sxs-lookup"><span data-stu-id="588b7-126">-Location</span></span>
<span data-ttu-id="588b7-127">Der Speicherort der verwalteten Quellinstanz der Sicherung.</span><span class="sxs-lookup"><span data-stu-id="588b7-127">The location of the backups' source Managed Instance.</span></span>

```yaml
Type: String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="588b7-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="588b7-128">-ResourceGroupName</span></span>
<span data-ttu-id="588b7-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="588b7-129">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="588b7-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="588b7-130">-ResourceId</span></span>
<span data-ttu-id="588b7-131">Die Ressourcen-ID der zu entfernenden Datenbank-Backup-Aufbewahrungsdauer.</span><span class="sxs-lookup"><span data-stu-id="588b7-131">The Resource ID of the Database Long Term Retention Backup to remove.</span></span>

```yaml
Type: String
Parameter Sets: RemoveBackupByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="588b7-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="588b7-132">-Confirm</span></span>
<span data-ttu-id="588b7-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="588b7-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="588b7-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="588b7-134">-WhatIf</span></span>
<span data-ttu-id="588b7-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="588b7-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="588b7-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="588b7-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="588b7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="588b7-137">CommonParameters</span></span>
<span data-ttu-id="588b7-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="588b7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="588b7-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="588b7-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="588b7-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="588b7-140">INPUTS</span></span>

### <span data-ttu-id="588b7-141">Microsoft. Azure. Commands. SQL. ManagedDatabaseBackup. Model. AzureSqlManagedDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="588b7-141">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel</span></span>

### <span data-ttu-id="588b7-142">System. String</span><span class="sxs-lookup"><span data-stu-id="588b7-142">System.String</span></span>

## <span data-ttu-id="588b7-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="588b7-143">OUTPUTS</span></span>

### <span data-ttu-id="588b7-144">Microsoft. Azure. Commands. SQL. ManagedDatabaseBackup. Model. AzureSqlManagedDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="588b7-144">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="588b7-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="588b7-145">NOTES</span></span>

## <span data-ttu-id="588b7-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="588b7-146">RELATED LINKS</span></span>

[<span data-ttu-id="588b7-147">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="588b7-147">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="588b7-148">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="588b7-148">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="588b7-149">Satz-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="588b7-149">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="588b7-150">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="588b7-150">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)