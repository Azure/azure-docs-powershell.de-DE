---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: CED38886-2DC9-450E-91FF-8209602C76CD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabasecopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseCopy.md
ms.openlocfilehash: 7019fc7345b4296d9c35f11c6acec5bf5a42d966
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502869"
---
# <span data-ttu-id="29acf-101">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="29acf-101">New-AzureRmSqlDatabaseCopy</span></span>

## <span data-ttu-id="29acf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="29acf-102">SYNOPSIS</span></span>
<span data-ttu-id="29acf-103">Erstellt eine Kopie einer SQL-Datenbank, die den Snapshot zum aktuellen Zeitpunkt verwendet.</span><span class="sxs-lookup"><span data-stu-id="29acf-103">Creates a copy of a SQL Database that uses the snapshot at the current time.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29acf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="29acf-104">SYNTAX</span></span>

### <span data-ttu-id="29acf-105">DtuBasedDatabase (Standard)</span><span class="sxs-lookup"><span data-stu-id="29acf-105">DtuBasedDatabase (Default)</span></span>
```
New-AzureRmSqlDatabaseCopy [-DatabaseName] <String> [-ServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-Tags <Hashtable>] [-CopyResourceGroupName <String>] [-CopyServerName <String>]
 -CopyDatabaseName <String> [-AsJob] [-LicenseType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="29acf-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="29acf-106">VcoreBasedDatabase</span></span>
```
New-AzureRmSqlDatabaseCopy [-DatabaseName] <String> [-Tags <Hashtable>] [-CopyResourceGroupName <String>]
 [-CopyServerName <String>] -CopyDatabaseName <String> [-AsJob] -ComputeGeneration <String> -VCore <Int32>
 [-LicenseType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29acf-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="29acf-107">DESCRIPTION</span></span>
<span data-ttu-id="29acf-108">Das Cmdlet **New-AzureRmSqlDatabaseCopy** erstellt eine Kopie einer Azure SQL-Datenbank, in der die Momentaufnahme der Daten zur aktuellen Zeit verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="29acf-108">The **New-AzureRmSqlDatabaseCopy** cmdlet creates a copy of an Azure SQL Database that uses the snapshot of the data at the current time.</span></span> <span data-ttu-id="29acf-109">Verwenden Sie dieses Cmdlet anstelle des Start-AzureSqlDatabaseCopy-Cmdlets, um eine einmalige Datenbankkopie zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="29acf-109">Use this cmdlet instead of the Start-AzureSqlDatabaseCopy cmdlet to create a one-time database copy.</span></span> <span data-ttu-id="29acf-110">Dieses Cmdlet gibt das **Daten Bank** Objekt der Kopie zurück.</span><span class="sxs-lookup"><span data-stu-id="29acf-110">This cmdlet returns the **Database** object of the copy.</span></span>
<span data-ttu-id="29acf-111">Hinweis: Verwenden Sie das New-AzureRmSqlDatabaseSecondary-Cmdlet, um die Geo-Replikation für eine Datenbank zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="29acf-111">Note: Use the New-AzureRmSqlDatabaseSecondary cmdlet to configure geo-replication for a database.</span></span>
<span data-ttu-id="29acf-112">Dieses Cmdlet wird auch vom SQL Server Stretch-Datenbankdienst auf Azure unterstützt.</span><span class="sxs-lookup"><span data-stu-id="29acf-112">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="29acf-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="29acf-113">EXAMPLES</span></span>

## <span data-ttu-id="29acf-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="29acf-114">PARAMETERS</span></span>

### <span data-ttu-id="29acf-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="29acf-115">-AsJob</span></span>
<span data-ttu-id="29acf-116">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="29acf-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="29acf-117">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="29acf-117">-ComputeGeneration</span></span>
<span data-ttu-id="29acf-118">Die COMPUTE-Generierung, die der neuen Kopie zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="29acf-118">The compute generation to assign to the new copy.</span></span>

```yaml
Type: System.String
Parameter Sets: VcoreBasedDatabase
Aliases: Family

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29acf-119">-CopyDatabaseName</span><span class="sxs-lookup"><span data-stu-id="29acf-119">-CopyDatabaseName</span></span>
<span data-ttu-id="29acf-120">Gibt den Namen der SQL-Datenbankkopie an.</span><span class="sxs-lookup"><span data-stu-id="29acf-120">Specifies the name of the SQL Database copy.</span></span>

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

### <span data-ttu-id="29acf-121">-CopyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29acf-121">-CopyResourceGroupName</span></span>
<span data-ttu-id="29acf-122">Gibt den Namen der Azure-Ressourcengruppe an, in der die Kopie zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="29acf-122">Specifies the name of the Azure Resource Group in which to assign the copy.</span></span>

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

### <span data-ttu-id="29acf-123">-CopyServerName</span><span class="sxs-lookup"><span data-stu-id="29acf-123">-CopyServerName</span></span>
<span data-ttu-id="29acf-124">Gibt den Namen des SQL-Servers an, der die Kopie hostet.</span><span class="sxs-lookup"><span data-stu-id="29acf-124">Specifies the name of the SQL Server which hosts the copy.</span></span>

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

### <span data-ttu-id="29acf-125">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="29acf-125">-DatabaseName</span></span>
<span data-ttu-id="29acf-126">Gibt den Namen der SQL-Datenbank an, die kopiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="29acf-126">Specifies the name of the SQL Database to copy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29acf-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29acf-127">-DefaultProfile</span></span>
<span data-ttu-id="29acf-128">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="29acf-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29acf-129">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="29acf-129">-ElasticPoolName</span></span>
<span data-ttu-id="29acf-130">Gibt den Namen des elastischen Pools an, in dem die Kopie zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="29acf-130">Specifies the name of the elastic pool in which to assign the copy.</span></span>

```yaml
Type: System.String
Parameter Sets: DtuBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29acf-131">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="29acf-131">-LicenseType</span></span>
<span data-ttu-id="29acf-132">Der Lizenztyp für die Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="29acf-132">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="29acf-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29acf-133">-ResourceGroupName</span></span>
<span data-ttu-id="29acf-134">Gibt den Namen der Ressourcengruppe an, die die zu kopierende Datenbank enthält.</span><span class="sxs-lookup"><span data-stu-id="29acf-134">Specifies the name of the Resource Group that contains the database to copy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29acf-135">-Servername</span><span class="sxs-lookup"><span data-stu-id="29acf-135">-ServerName</span></span>
<span data-ttu-id="29acf-136">Gibt den Namen des SQL-Servers an, der die zu kopierende Datenbank enthält.</span><span class="sxs-lookup"><span data-stu-id="29acf-136">Specifies the name of the  SQL Server that contains the database to copy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29acf-137">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="29acf-137">-ServiceObjectiveName</span></span>
<span data-ttu-id="29acf-138">Gibt den Namen des Dienst Ziels an, das der Kopie zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="29acf-138">Specifies the name of the service objective to assign to the copy.</span></span>

```yaml
Type: System.String
Parameter Sets: DtuBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29acf-139">-Tags</span><span class="sxs-lookup"><span data-stu-id="29acf-139">-Tags</span></span>
<span data-ttu-id="29acf-140">Gibt die Schlüssel-Wert-Paare in Form einer Hashtabelle an, die der Azure SQL-Datenbankkopie zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="29acf-140">Specifies the Key-value pairs in the form of a hash table to associate with the Azure SQL Database copy.</span></span> <span data-ttu-id="29acf-141">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="29acf-141">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29acf-142">-VCore</span><span class="sxs-lookup"><span data-stu-id="29acf-142">-VCore</span></span>
<span data-ttu-id="29acf-143">Die Vcore-Nummern der Azure SQL-Datenbankkopie.</span><span class="sxs-lookup"><span data-stu-id="29acf-143">The Vcore numbers of the Azure Sql Database copy.</span></span>

```yaml
Type: System.Int32
Parameter Sets: VcoreBasedDatabase
Aliases: Capacity

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29acf-144">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="29acf-144">-Confirm</span></span>
<span data-ttu-id="29acf-145">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="29acf-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29acf-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29acf-146">-WhatIf</span></span>
<span data-ttu-id="29acf-147">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="29acf-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29acf-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="29acf-148">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29acf-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29acf-149">CommonParameters</span></span>
<span data-ttu-id="29acf-150">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29acf-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29acf-151">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29acf-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29acf-152">Eingaben</span><span class="sxs-lookup"><span data-stu-id="29acf-152">INPUTS</span></span>

### <span data-ttu-id="29acf-153">System. String</span><span class="sxs-lookup"><span data-stu-id="29acf-153">System.String</span></span>

## <span data-ttu-id="29acf-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="29acf-154">OUTPUTS</span></span>

### <span data-ttu-id="29acf-155">Microsoft. Azure. Commands. SQL. Replication. Model. AzureSqlDatabaseCopyModel</span><span class="sxs-lookup"><span data-stu-id="29acf-155">Microsoft.Azure.Commands.Sql.Replication.Model.AzureSqlDatabaseCopyModel</span></span>

## <span data-ttu-id="29acf-156">Notizen</span><span class="sxs-lookup"><span data-stu-id="29acf-156">NOTES</span></span>

## <span data-ttu-id="29acf-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="29acf-157">RELATED LINKS</span></span>

[<span data-ttu-id="29acf-158">Neu – AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="29acf-158">New-AzureRmSqlDatabaseSecondary</span></span>](./New-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="29acf-159">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="29acf-159">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
