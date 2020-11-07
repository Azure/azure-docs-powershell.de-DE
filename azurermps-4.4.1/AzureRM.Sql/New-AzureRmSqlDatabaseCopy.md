---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: CED38886-2DC9-450E-91FF-8209602C76CD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseCopy.md
ms.openlocfilehash: a962ca86c3d65cd11da4169626ed932bb78653b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664963"
---
# <span data-ttu-id="7d19d-101">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="7d19d-101">New-AzureRmSqlDatabaseCopy</span></span>

## <span data-ttu-id="7d19d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7d19d-102">SYNOPSIS</span></span>
<span data-ttu-id="7d19d-103">Erstellt eine Kopie einer SQL-Datenbank, die den Snapshot zum aktuellen Zeitpunkt verwendet.</span><span class="sxs-lookup"><span data-stu-id="7d19d-103">Creates a copy of a SQL Database that uses the snapshot at the current time.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d19d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7d19d-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseCopy [-DatabaseName] <String> [-ServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-Tags <Hashtable>] [-CopyResourceGroupName <String>] [-CopyServerName <String>]
 -CopyDatabaseName <String> [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d19d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7d19d-105">DESCRIPTION</span></span>
<span data-ttu-id="7d19d-106">Das Cmdlet **New-AzureRmSqlDatabaseCopy** erstellt eine Kopie einer Azure SQL-Datenbank, in der die Momentaufnahme der Daten zur aktuellen Zeit verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7d19d-106">The **New-AzureRmSqlDatabaseCopy** cmdlet creates a copy of an Azure SQL Database that uses the snapshot of the data at the current time.</span></span> <span data-ttu-id="7d19d-107">Verwenden Sie dieses Cmdlet anstelle des Start-AzureSqlDatabaseCopy-Cmdlets, um eine einmalige Datenbankkopie zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="7d19d-107">Use this cmdlet instead of the Start-AzureSqlDatabaseCopy cmdlet to create a one-time database copy.</span></span> <span data-ttu-id="7d19d-108">Dieses Cmdlet gibt das **Daten Bank** Objekt der Kopie zurück.</span><span class="sxs-lookup"><span data-stu-id="7d19d-108">This cmdlet returns the **Database** object of the copy.</span></span>

<span data-ttu-id="7d19d-109">Hinweis: Verwenden Sie das New-AzureRmSqlDatabaseSecondary-Cmdlet, um die Geo-Replikation für eine Datenbank zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="7d19d-109">Note: Use the New-AzureRmSqlDatabaseSecondary cmdlet to configure geo-replication for a database.</span></span>

<span data-ttu-id="7d19d-110">Dieses Cmdlet wird auch vom SQL Server Stretch-Datenbankdienst auf Azure unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7d19d-110">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="7d19d-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7d19d-111">EXAMPLES</span></span>

## <span data-ttu-id="7d19d-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="7d19d-112">PARAMETERS</span></span>

### <span data-ttu-id="7d19d-113">-CopyDatabaseName</span><span class="sxs-lookup"><span data-stu-id="7d19d-113">-CopyDatabaseName</span></span>
<span data-ttu-id="7d19d-114">Gibt den Namen der SQL-Datenbankkopie an.</span><span class="sxs-lookup"><span data-stu-id="7d19d-114">Specifies the name of the SQL Database copy.</span></span>

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

### <span data-ttu-id="7d19d-115">-CopyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d19d-115">-CopyResourceGroupName</span></span>
<span data-ttu-id="7d19d-116">Gibt den Namen der Azure-Ressourcengruppe an, in der die Kopie zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="7d19d-116">Specifies the name of the Azure Resource Group in which to assign the copy.</span></span>

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

### <span data-ttu-id="7d19d-117">-CopyServerName</span><span class="sxs-lookup"><span data-stu-id="7d19d-117">-CopyServerName</span></span>
<span data-ttu-id="7d19d-118">Gibt den Namen des SQL-Servers an, der die Kopie hostet.</span><span class="sxs-lookup"><span data-stu-id="7d19d-118">Specifies the name of the SQL Server which hosts the copy.</span></span>

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

### <span data-ttu-id="7d19d-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7d19d-119">-DatabaseName</span></span>
<span data-ttu-id="7d19d-120">Gibt den Namen der SQL-Datenbank an, die kopiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="7d19d-120">Specifies the name of the SQL Database to copy.</span></span>

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

### <span data-ttu-id="7d19d-121">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="7d19d-121">-ElasticPoolName</span></span>
<span data-ttu-id="7d19d-122">Gibt den Namen des elastischen Pools an, in dem die Kopie zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="7d19d-122">Specifies the name of the elastic pool in which to assign the copy.</span></span>

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

### <span data-ttu-id="7d19d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d19d-123">-ResourceGroupName</span></span>
<span data-ttu-id="7d19d-124">Gibt den Namen der Ressourcengruppe an, der das Cmdlet die kopierte Datenbank zuweist.</span><span class="sxs-lookup"><span data-stu-id="7d19d-124">Specifies the name of the  Resource Group to which this cmdlet assigns the copied database.</span></span>

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

### <span data-ttu-id="7d19d-125">-Servername</span><span class="sxs-lookup"><span data-stu-id="7d19d-125">-ServerName</span></span>
<span data-ttu-id="7d19d-126">Gibt den Namen des SQL-Servers an, der die zu kopierende Datenbank enthält.</span><span class="sxs-lookup"><span data-stu-id="7d19d-126">Specifies the name of the  SQL Server that contains the database to copy.</span></span>

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

### <span data-ttu-id="7d19d-127">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="7d19d-127">-ServiceObjectiveName</span></span>
<span data-ttu-id="7d19d-128">Gibt den Namen des Dienst Ziels an, das der Kopie zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="7d19d-128">Specifies the name of the service objective to assign to the copy.</span></span>

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

### <span data-ttu-id="7d19d-129">-Tags</span><span class="sxs-lookup"><span data-stu-id="7d19d-129">-Tags</span></span>
<span data-ttu-id="7d19d-130">Gibt die Schlüssel-Wert-Paare in Form einer Hashtabelle an, die der Azure SQL-Datenbankkopie zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7d19d-130">Specifies the Key-value pairs in the form of a hash table to associate with the Azure SQL Database copy.</span></span> <span data-ttu-id="7d19d-131">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="7d19d-131">For example:</span></span>

<span data-ttu-id="7d19d-132">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="7d19d-132">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="7d19d-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7d19d-133">-Confirm</span></span>
<span data-ttu-id="7d19d-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7d19d-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d19d-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d19d-135">-WhatIf</span></span>
<span data-ttu-id="7d19d-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7d19d-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d19d-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7d19d-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d19d-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d19d-138">-DefaultProfile</span></span>
<span data-ttu-id="7d19d-139">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7d19d-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d19d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d19d-140">CommonParameters</span></span>
<span data-ttu-id="7d19d-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d19d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d19d-142">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d19d-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d19d-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7d19d-143">INPUTS</span></span>

## <span data-ttu-id="7d19d-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7d19d-144">OUTPUTS</span></span>

### <span data-ttu-id="7d19d-145">Microsoft. Azure. Commands. SQL. Replication. Model. AzureSqlDatabaseCopyModel</span><span class="sxs-lookup"><span data-stu-id="7d19d-145">Microsoft.Azure.Commands.Sql.Replication.Model.AzureSqlDatabaseCopyModel</span></span>
<span data-ttu-id="7d19d-146">Dieses Cmdlet gibt ein **Daten Bank** Objekt zurück, das die kopierte Datenbank darstellt.</span><span class="sxs-lookup"><span data-stu-id="7d19d-146">This cmdlet returns a **Database** object that represents the copied database.</span></span>

## <span data-ttu-id="7d19d-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="7d19d-147">NOTES</span></span>

## <span data-ttu-id="7d19d-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7d19d-148">RELATED LINKS</span></span>

[<span data-ttu-id="7d19d-149">Neu – AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="7d19d-149">New-AzureRmSqlDatabaseSecondary</span></span>](./New-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="7d19d-150">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="7d19d-150">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
