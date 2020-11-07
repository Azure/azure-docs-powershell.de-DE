---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 4695AFEA-D244-4FCB-AF36-D8CDEBFB392C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 02a6090a98a80300f886e8bbbd8e2622aa7981d4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845796"
---
# <span data-ttu-id="ffbc2-101">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="ffbc2-101">Remove-AzSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="ffbc2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ffbc2-102">SYNOPSIS</span></span>
<span data-ttu-id="ffbc2-103">Entfernt eine Daten Maskierungs Regel aus einer Datenbank.</span><span class="sxs-lookup"><span data-stu-id="ffbc2-103">Removes a data masking rule from a database.</span></span>

## <span data-ttu-id="ffbc2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ffbc2-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseDataMaskingRule [-PassThru] [-Force] -SchemaName <String> -TableName <String>
 -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ffbc2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ffbc2-105">DESCRIPTION</span></span>
<span data-ttu-id="ffbc2-106">Das Cmdlet " **Remove-AzSqlDatabaseDataMaskingRule** " entfernt eine bestimmte Daten Maskierungs Regel aus einer Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="ffbc2-106">The **Remove-AzSqlDatabaseDataMaskingRule** cmdlet removes a specific data masking rule from an Azure SQL database.</span></span>
<span data-ttu-id="ffbc2-107">Sie können eine Daten Maskierungs Regel entfernen, indem Sie die *ResourceGroupName* -, *Servername* -, *DatabaseName* -und *Rules* -Parameter verwenden, um die Regel zu identifizieren, die dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="ffbc2-107">You can remove a data masking rule by using the *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleId* parameters to identify the rule that this cmdlet removes.</span></span>
<span data-ttu-id="ffbc2-108">Dieses Cmdlet wird auch vom SQL Server Stretch-Datenbankdienst auf Azure unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ffbc2-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="ffbc2-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ffbc2-109">EXAMPLES</span></span>

### <span data-ttu-id="ffbc2-110">Beispiel 1: Entfernen einer Datenbankdaten-Maskierungs Regel</span><span class="sxs-lookup"><span data-stu-id="ffbc2-110">Example 1: Remove a database data masking rule</span></span>
```
PS C:\>Remove-AzSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SchemaName "dbo" -TableName  "table1" -ColumnName "column1"
```

<span data-ttu-id="ffbc2-111">Dieser Befehl entfernt die für die Datenbank-database01 definierten Regelnamen Rule01.</span><span class="sxs-lookup"><span data-stu-id="ffbc2-111">This command removes rule name Rule01 defined for the database Database01.</span></span>
<span data-ttu-id="ffbc2-112">Die Datenbank befindet sich auf Server01 und ist der Ressourcengruppe ResourceGroup01 zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="ffbc2-112">The database is located on Server01 and assigned to resource group ResourceGroup01.</span></span>

## <span data-ttu-id="ffbc2-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="ffbc2-113">PARAMETERS</span></span>

### <span data-ttu-id="ffbc2-114">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="ffbc2-114">-ColumnName</span></span>
<span data-ttu-id="ffbc2-115">Gibt den Namen der Spalte an, auf die die Maskierungs Regel ausgerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="ffbc2-115">Specifies the name of the column targeted by the masking rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffbc2-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ffbc2-116">-DatabaseName</span></span>
<span data-ttu-id="ffbc2-117">Gibt den Namen der Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="ffbc2-117">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="ffbc2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffbc2-118">-DefaultProfile</span></span>
<span data-ttu-id="ffbc2-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="ffbc2-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ffbc2-120">-Force</span><span class="sxs-lookup"><span data-stu-id="ffbc2-120">-Force</span></span>
<span data-ttu-id="ffbc2-121">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="ffbc2-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ffbc2-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ffbc2-122">-PassThru</span></span>
<span data-ttu-id="ffbc2-123">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="ffbc2-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ffbc2-124">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="ffbc2-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ffbc2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffbc2-125">-ResourceGroupName</span></span>
<span data-ttu-id="ffbc2-126">Gibt den Namen der Ressourcengruppe an, der die Datenbank zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="ffbc2-126">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="ffbc2-127">-Schemaname</span><span class="sxs-lookup"><span data-stu-id="ffbc2-127">-SchemaName</span></span>
<span data-ttu-id="ffbc2-128">Gibt den Namen eines Schemas an.</span><span class="sxs-lookup"><span data-stu-id="ffbc2-128">Specifies the name of a schema.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffbc2-129">-Servername</span><span class="sxs-lookup"><span data-stu-id="ffbc2-129">-ServerName</span></span>
<span data-ttu-id="ffbc2-130">Gibt den Namen des Servers an, der die Datenbank hostet.</span><span class="sxs-lookup"><span data-stu-id="ffbc2-130">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="ffbc2-131">-Tabellenname</span><span class="sxs-lookup"><span data-stu-id="ffbc2-131">-TableName</span></span>
<span data-ttu-id="ffbc2-132">Gibt den Namen einer Azure SQL-Tabelle an.</span><span class="sxs-lookup"><span data-stu-id="ffbc2-132">Specifies the name of an Azure SQL table.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffbc2-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ffbc2-133">-Confirm</span></span>
<span data-ttu-id="ffbc2-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ffbc2-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ffbc2-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffbc2-135">-WhatIf</span></span>
<span data-ttu-id="ffbc2-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ffbc2-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ffbc2-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ffbc2-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ffbc2-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffbc2-138">CommonParameters</span></span>
<span data-ttu-id="ffbc2-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffbc2-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffbc2-140">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ffbc2-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffbc2-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ffbc2-141">INPUTS</span></span>

### <span data-ttu-id="ffbc2-142">System. String</span><span class="sxs-lookup"><span data-stu-id="ffbc2-142">System.String</span></span>

## <span data-ttu-id="ffbc2-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ffbc2-143">OUTPUTS</span></span>

### <span data-ttu-id="ffbc2-144">Microsoft. Azure. Commands. SQL. datamasking. Model. DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="ffbc2-144">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="ffbc2-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="ffbc2-145">NOTES</span></span>

## <span data-ttu-id="ffbc2-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ffbc2-146">RELATED LINKS</span></span>

[<span data-ttu-id="ffbc2-147">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="ffbc2-147">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="ffbc2-148">Neu – AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="ffbc2-148">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="ffbc2-149">Satz-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="ffbc2-149">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="ffbc2-150">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="ffbc2-150">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


