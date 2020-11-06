---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: CED38886-2DC9-450E-91FF-8209602C76CD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabasecopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseCopy.md
ms.openlocfilehash: 4e9d33691cfd09681bb115c89d0eaf351ef14f13
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476470"
---
# <span data-ttu-id="6233c-101">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="6233c-101">New-AzureRmSqlDatabaseCopy</span></span>

## <span data-ttu-id="6233c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6233c-102">SYNOPSIS</span></span>
<span data-ttu-id="6233c-103">Erstellt eine Kopie einer SQL-Datenbank, die den Snapshot zum aktuellen Zeitpunkt verwendet.</span><span class="sxs-lookup"><span data-stu-id="6233c-103">Creates a copy of a SQL Database that uses the snapshot at the current time.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6233c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6233c-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseCopy [-DatabaseName] <String> [-ServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-Tags <Hashtable>] [-CopyResourceGroupName <String>] [-CopyServerName <String>]
 -CopyDatabaseName <String> [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6233c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6233c-105">DESCRIPTION</span></span>
<span data-ttu-id="6233c-106">Das Cmdlet **New-AzureRmSqlDatabaseCopy** erstellt eine Kopie einer Azure SQL-Datenbank, in der die Momentaufnahme der Daten zur aktuellen Zeit verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6233c-106">The **New-AzureRmSqlDatabaseCopy** cmdlet creates a copy of an Azure SQL Database that uses the snapshot of the data at the current time.</span></span> <span data-ttu-id="6233c-107">Verwenden Sie dieses Cmdlet anstelle des Start-AzureSqlDatabaseCopy-Cmdlets, um eine einmalige Datenbankkopie zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="6233c-107">Use this cmdlet instead of the Start-AzureSqlDatabaseCopy cmdlet to create a one-time database copy.</span></span> <span data-ttu-id="6233c-108">Dieses Cmdlet gibt das **Daten Bank** Objekt der Kopie zurück.</span><span class="sxs-lookup"><span data-stu-id="6233c-108">This cmdlet returns the **Database** object of the copy.</span></span>

<span data-ttu-id="6233c-109">Hinweis: Verwenden Sie das New-AzureRmSqlDatabaseSecondary-Cmdlet, um die Geo-Replikation für eine Datenbank zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="6233c-109">Note: Use the New-AzureRmSqlDatabaseSecondary cmdlet to configure geo-replication for a database.</span></span>

<span data-ttu-id="6233c-110">Dieses Cmdlet wird auch vom SQL Server Stretch-Datenbankdienst auf Azure unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6233c-110">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="6233c-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6233c-111">EXAMPLES</span></span>

## <span data-ttu-id="6233c-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="6233c-112">PARAMETERS</span></span>

### <span data-ttu-id="6233c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6233c-113">-AsJob</span></span>
<span data-ttu-id="6233c-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="6233c-114">Run cmdlet in the background</span></span>
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

### <span data-ttu-id="6233c-115">-CopyDatabaseName</span><span class="sxs-lookup"><span data-stu-id="6233c-115">-CopyDatabaseName</span></span>
<span data-ttu-id="6233c-116">Gibt den Namen der SQL-Datenbankkopie an.</span><span class="sxs-lookup"><span data-stu-id="6233c-116">Specifies the name of the SQL Database copy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6233c-117">-CopyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6233c-117">-CopyResourceGroupName</span></span>
<span data-ttu-id="6233c-118">Gibt den Namen der Azure-Ressourcengruppe an, in der die Kopie zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="6233c-118">Specifies the name of the Azure Resource Group in which to assign the copy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6233c-119">-CopyServerName</span><span class="sxs-lookup"><span data-stu-id="6233c-119">-CopyServerName</span></span>
<span data-ttu-id="6233c-120">Gibt den Namen des SQL-Servers an, der die Kopie hostet.</span><span class="sxs-lookup"><span data-stu-id="6233c-120">Specifies the name of the SQL Server which hosts the copy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6233c-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6233c-121">-DatabaseName</span></span>
<span data-ttu-id="6233c-122">Gibt den Namen der SQL-Datenbank an, die kopiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="6233c-122">Specifies the name of the SQL Database to copy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6233c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6233c-123">-DefaultProfile</span></span>
<span data-ttu-id="6233c-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="6233c-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6233c-125">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="6233c-125">-ElasticPoolName</span></span>
<span data-ttu-id="6233c-126">Gibt den Namen des elastischen Pools an, in dem die Kopie zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="6233c-126">Specifies the name of the elastic pool in which to assign the copy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6233c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6233c-127">-ResourceGroupName</span></span>
<span data-ttu-id="6233c-128">Gibt den Namen der Ressourcengruppe an, die die zu kopierende Datenbank enthält.</span><span class="sxs-lookup"><span data-stu-id="6233c-128">Specifies the name of the Resource Group that contains the database to copy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6233c-129">-Servername</span><span class="sxs-lookup"><span data-stu-id="6233c-129">-ServerName</span></span>
<span data-ttu-id="6233c-130">Gibt den Namen des SQL-Servers an, der die zu kopierende Datenbank enthält.</span><span class="sxs-lookup"><span data-stu-id="6233c-130">Specifies the name of the  SQL Server that contains the database to copy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6233c-131">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="6233c-131">-ServiceObjectiveName</span></span>
<span data-ttu-id="6233c-132">Gibt den Namen des Dienst Ziels an, das der Kopie zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="6233c-132">Specifies the name of the service objective to assign to the copy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6233c-133">-Tags</span><span class="sxs-lookup"><span data-stu-id="6233c-133">-Tags</span></span>
<span data-ttu-id="6233c-134">Gibt die Schlüssel-Wert-Paare in Form einer Hashtabelle an, die der Azure SQL-Datenbankkopie zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="6233c-134">Specifies the Key-value pairs in the form of a hash table to associate with the Azure SQL Database copy.</span></span> <span data-ttu-id="6233c-135">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="6233c-135">For example:</span></span>

<span data-ttu-id="6233c-136">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="6233c-136">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6233c-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6233c-137">-Confirm</span></span>
<span data-ttu-id="6233c-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6233c-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6233c-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6233c-139">-WhatIf</span></span>
<span data-ttu-id="6233c-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6233c-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6233c-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6233c-141">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6233c-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6233c-142">CommonParameters</span></span>
<span data-ttu-id="6233c-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6233c-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6233c-144">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6233c-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6233c-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6233c-145">INPUTS</span></span>

### <span data-ttu-id="6233c-146">Keine</span><span class="sxs-lookup"><span data-stu-id="6233c-146">None</span></span>
<span data-ttu-id="6233c-147">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="6233c-147">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6233c-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6233c-148">OUTPUTS</span></span>

### <span data-ttu-id="6233c-149">Microsoft. Azure. Commands. SQL. Replication. Model. AzureSqlDatabaseCopyModel</span><span class="sxs-lookup"><span data-stu-id="6233c-149">Microsoft.Azure.Commands.Sql.Replication.Model.AzureSqlDatabaseCopyModel</span></span>
<span data-ttu-id="6233c-150">Dieses Cmdlet gibt ein **Daten Bank** Objekt zurück, das die kopierte Datenbank darstellt.</span><span class="sxs-lookup"><span data-stu-id="6233c-150">This cmdlet returns a **Database** object that represents the copied database.</span></span>

## <span data-ttu-id="6233c-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="6233c-151">NOTES</span></span>

## <span data-ttu-id="6233c-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6233c-152">RELATED LINKS</span></span>

[<span data-ttu-id="6233c-153">Neu – AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="6233c-153">New-AzureRmSqlDatabaseSecondary</span></span>](./New-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="6233c-154">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="6233c-154">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
