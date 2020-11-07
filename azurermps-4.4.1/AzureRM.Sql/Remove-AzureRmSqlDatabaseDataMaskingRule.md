---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 4695AFEA-D244-4FCB-AF36-D8CDEBFB392C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 7f5f72652a0b3c8e1944b6091b43f1458fd17839
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665257"
---
# <span data-ttu-id="7022d-101">Remove-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="7022d-101">Remove-AzureRmSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="7022d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7022d-102">SYNOPSIS</span></span>
<span data-ttu-id="7022d-103">Entfernt eine Daten Maskierungs Regel aus einer Datenbank.</span><span class="sxs-lookup"><span data-stu-id="7022d-103">Removes a data masking rule from a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7022d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7022d-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabaseDataMaskingRule [-PassThru] [-Force] -SchemaName <String> -TableName <String>
 -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7022d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7022d-105">DESCRIPTION</span></span>
<span data-ttu-id="7022d-106">Das Cmdlet " **Remove-AzureRmSqlDatabaseDataMaskingRule** " entfernt eine bestimmte Daten Maskierungs Regel aus einer Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="7022d-106">The **Remove-AzureRmSqlDatabaseDataMaskingRule** cmdlet removes a specific data masking rule from an Azure SQL database.</span></span>
<span data-ttu-id="7022d-107">Sie können eine Daten Maskierungs Regel entfernen, indem Sie die *ResourceGroupName* -, *Servername* -, *DatabaseName* -und *Rules* -Parameter verwenden, um die Regel zu identifizieren, die dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="7022d-107">You can remove a data masking rule by using the *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleId* parameters to identify the rule that this cmdlet removes.</span></span>

<span data-ttu-id="7022d-108">Dieses Cmdlet wird auch vom SQL Server Stretch-Datenbankdienst auf Azure unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7022d-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="7022d-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7022d-109">EXAMPLES</span></span>

### <span data-ttu-id="7022d-110">Beispiel 1: Entfernen einer Datenbankdaten-Maskierungs Regel</span><span class="sxs-lookup"><span data-stu-id="7022d-110">Example 1: Remove a database data masking rule</span></span>
```
PS C:\>Remove-AzureRmSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SchemaName "dbo" -TableName  "table1" -ColumnName "column1"
```

<span data-ttu-id="7022d-111">Dieser Befehl entfernt die für die Datenbank-database01 definierten Regelnamen Rule01.</span><span class="sxs-lookup"><span data-stu-id="7022d-111">This command removes rule name Rule01 defined for the database Database01.</span></span>
<span data-ttu-id="7022d-112">Die Datenbank befindet sich auf Server01 und ist der Ressourcengruppe ResourceGroup01 zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="7022d-112">The database is located on Server01 and assigned to resource group ResourceGroup01.</span></span>

## <span data-ttu-id="7022d-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="7022d-113">PARAMETERS</span></span>

### <span data-ttu-id="7022d-114">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="7022d-114">-ColumnName</span></span>
<span data-ttu-id="7022d-115">Gibt den Namen der Spalte an, auf die die Maskierungs Regel ausgerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="7022d-115">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="7022d-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7022d-116">-DatabaseName</span></span>
<span data-ttu-id="7022d-117">Gibt den Namen der Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="7022d-117">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="7022d-118">-Force</span><span class="sxs-lookup"><span data-stu-id="7022d-118">-Force</span></span>
<span data-ttu-id="7022d-119">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="7022d-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7022d-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7022d-120">-PassThru</span></span>
<span data-ttu-id="7022d-121">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="7022d-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7022d-122">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="7022d-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7022d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7022d-123">-ResourceGroupName</span></span>
<span data-ttu-id="7022d-124">Gibt den Namen der Ressourcengruppe an, der die Datenbank zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="7022d-124">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="7022d-125">-Schemaname</span><span class="sxs-lookup"><span data-stu-id="7022d-125">-SchemaName</span></span>
<span data-ttu-id="7022d-126">Gibt den Namen eines Schemas an.</span><span class="sxs-lookup"><span data-stu-id="7022d-126">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="7022d-127">-Servername</span><span class="sxs-lookup"><span data-stu-id="7022d-127">-ServerName</span></span>
<span data-ttu-id="7022d-128">Gibt den Namen des Servers an, der die Datenbank hostet.</span><span class="sxs-lookup"><span data-stu-id="7022d-128">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="7022d-129">-Tabellenname</span><span class="sxs-lookup"><span data-stu-id="7022d-129">-TableName</span></span>
<span data-ttu-id="7022d-130">Gibt den Namen einer Azure SQL-Tabelle an.</span><span class="sxs-lookup"><span data-stu-id="7022d-130">Specifies the name of an Azure SQL table.</span></span>

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

### <span data-ttu-id="7022d-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7022d-131">-Confirm</span></span>
<span data-ttu-id="7022d-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7022d-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7022d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7022d-133">-WhatIf</span></span>
<span data-ttu-id="7022d-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7022d-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7022d-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7022d-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7022d-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7022d-136">-DefaultProfile</span></span>
<span data-ttu-id="7022d-137">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7022d-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7022d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7022d-138">CommonParameters</span></span>
<span data-ttu-id="7022d-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7022d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7022d-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7022d-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7022d-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7022d-141">INPUTS</span></span>

### <span data-ttu-id="7022d-142">Microsoft. Azure. Commands. SQL. Security. Model. DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="7022d-142">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="7022d-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7022d-143">OUTPUTS</span></span>

### <span data-ttu-id="7022d-144">Microsoft. Azure. Commands. SQL. Security. Model. DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="7022d-144">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="7022d-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="7022d-145">NOTES</span></span>

## <span data-ttu-id="7022d-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7022d-146">RELATED LINKS</span></span>

[<span data-ttu-id="7022d-147">Get-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="7022d-147">Get-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Get-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="7022d-148">Neu – AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="7022d-148">New-AzureRmSqlDatabaseDataMaskingRule</span></span>](./New-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="7022d-149">Satz-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="7022d-149">Set-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Set-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="7022d-150">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="7022d-150">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


