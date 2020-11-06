---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 848A6972-AB29-46FB-8E03-FF2ADB113A0E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 0c04697f36558c7eb4c296e2837595541381a3d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476510"
---
# <span data-ttu-id="1e7e3-101">Get-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="1e7e3-101">Get-AzureRmSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="1e7e3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1e7e3-102">SYNOPSIS</span></span>
<span data-ttu-id="1e7e3-103">Ruft die Regeln für die Daten Maskierung aus einer Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="1e7e3-103">Gets the data masking rules from a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1e7e3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1e7e3-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseDataMaskingRule [-SchemaName <String>] [-TableName <String>] [-ColumnName <String>]
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e7e3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1e7e3-105">DESCRIPTION</span></span>
<span data-ttu-id="1e7e3-106">Das Cmdlet " **Get-AzureRmSqlDatabaseDataMaskingRule** " erhält entweder eine bestimmte Daten Maskierungs Regel oder alle Daten Maskierungs Regeln für eine Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="1e7e3-106">The **Get-AzureRmSqlDatabaseDataMaskingRule** cmdlet gets either a specific data masking rule or all of the data masking rules for an Azure SQL database.</span></span>
<span data-ttu-id="1e7e3-107">Um das Cmdlet zu verwenden, verwenden Sie die *ResourceGroupName* -, *Servername* -und *DatabaseName* -Parameter, um die Datenbank zu identifizieren, und den Parameter " *rulecode* ", um anzugeben, welche Regel dieses Cmdlet zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="1e7e3-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database, and the *RuleId* parameter to specify which rule this cmdlet returns.</span></span>
<span data-ttu-id="1e7e3-108">Wenn Sie keine Regel- *Nr* angeben, werden alle Daten Maskierungs Regeln für diese Azure SQL-Datenbank zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1e7e3-108">If you do not provide *RuleId* , all the data masking rules for that Azure SQL database are returned.</span></span>

<span data-ttu-id="1e7e3-109">Dieses Cmdlet wird auch vom SQL Server Stretch-Datenbankdienst auf Azure unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1e7e3-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="1e7e3-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1e7e3-110">EXAMPLES</span></span>

### <span data-ttu-id="1e7e3-111">Beispiel 1: Abrufen aller Regeln für die Daten Maskierung aus einer Datenbank</span><span class="sxs-lookup"><span data-stu-id="1e7e3-111">Example 1: Get all data masking rules from a database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName      : database01
ResourceGroupName : resourcegroup01
ServerName        : server01
SchemaName        : dbo
TableName         : table1
ColumnName        : column1
MaskingFunction   : Default
PrefixSize        :
SuffixSize        :
ReplacementString :
NumberFrom        :
NumberTo          :

DatabaseName      : database01
ResourceGroupName : resourcegroup01
ServerName        : server01
SchemaName        : dbo
TableName         : table2
ColumnName        : column2
MaskingFunction   : Default
PrefixSize        :
SuffixSize        :
ReplacementString :
NumberFrom        :
NumberTo          :
```

### <span data-ttu-id="1e7e3-112">Beispiel 2: Abrufen der für das Schema "dbo" definierten Daten Maskierungs Regel, Tabelle "Tabelle1" und Spalte "Spalte1"</span><span class="sxs-lookup"><span data-stu-id="1e7e3-112">Example 2: Get the data masking rule defined on schema "dbo", table "table1" and column "column1".</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SchemaName "dbo" -TableName  "table1" -ColumnName "column1"
DatabaseName      : database01
ResourceGroupName : resourcegroup01
ServerName        : server01
SchemaName        : dbo
TableName         : table1
ColumnName        : column1
MaskingFunction   : Default
PrefixSize        :
SuffixSize        :
ReplacementString :
NumberFrom        :
NumberTo          :
```

## <span data-ttu-id="1e7e3-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="1e7e3-113">PARAMETERS</span></span>

### <span data-ttu-id="1e7e3-114">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="1e7e3-114">-ColumnName</span></span>
<span data-ttu-id="1e7e3-115">Gibt den Namen der Spalte an, auf die die Maskierungs Regel ausgerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="1e7e3-115">Specifies the name of the column targeted by the masking rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e7e3-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1e7e3-116">-DatabaseName</span></span>
<span data-ttu-id="1e7e3-117">Gibt den Namen der Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="1e7e3-117">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="1e7e3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e7e3-118">-DefaultProfile</span></span>
<span data-ttu-id="1e7e3-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="1e7e3-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1e7e3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e7e3-120">-ResourceGroupName</span></span>
<span data-ttu-id="1e7e3-121">Gibt den Namen der Ressourcengruppe an, der die Datenbank zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="1e7e3-121">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="1e7e3-122">-Schemaname</span><span class="sxs-lookup"><span data-stu-id="1e7e3-122">-SchemaName</span></span>
<span data-ttu-id="1e7e3-123">Gibt den Namen eines Schemas an.</span><span class="sxs-lookup"><span data-stu-id="1e7e3-123">Specifies the name of a schema.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e7e3-124">-Servername</span><span class="sxs-lookup"><span data-stu-id="1e7e3-124">-ServerName</span></span>
<span data-ttu-id="1e7e3-125">Gibt den Namen des Servers an.</span><span class="sxs-lookup"><span data-stu-id="1e7e3-125">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="1e7e3-126">-Tabellenname</span><span class="sxs-lookup"><span data-stu-id="1e7e3-126">-TableName</span></span>
<span data-ttu-id="1e7e3-127">Gibt den Namen einer Azure SQL-Tabelle an.</span><span class="sxs-lookup"><span data-stu-id="1e7e3-127">Specifies the name of an Azure SQL table.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e7e3-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1e7e3-128">-Confirm</span></span>
<span data-ttu-id="1e7e3-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1e7e3-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e7e3-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e7e3-130">-WhatIf</span></span>
<span data-ttu-id="1e7e3-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1e7e3-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e7e3-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1e7e3-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e7e3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e7e3-133">CommonParameters</span></span>
<span data-ttu-id="1e7e3-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e7e3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e7e3-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e7e3-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e7e3-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1e7e3-136">INPUTS</span></span>

###  
<span data-ttu-id="1e7e3-137">Keine.</span><span class="sxs-lookup"><span data-stu-id="1e7e3-137">None.</span></span>

## <span data-ttu-id="1e7e3-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1e7e3-138">OUTPUTS</span></span>

### <span data-ttu-id="1e7e3-139">Microsoft. Azure. Commands. SQL. Security. Model. DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="1e7e3-139">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="1e7e3-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="1e7e3-140">NOTES</span></span>

## <span data-ttu-id="1e7e3-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1e7e3-141">RELATED LINKS</span></span>

[<span data-ttu-id="1e7e3-142">Get-AzureRmSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="1e7e3-142">Get-AzureRmSqlDatabaseDataMaskingPolicy</span></span>](./Get-AzureRmSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="1e7e3-143">Neu – AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="1e7e3-143">New-AzureRmSqlDatabaseDataMaskingRule</span></span>](./New-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="1e7e3-144">Remove-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="1e7e3-144">Remove-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Remove-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="1e7e3-145">Satz-AzureRmSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="1e7e3-145">Set-AzureRmSqlDatabaseDataMaskingPolicy</span></span>](./Set-AzureRmSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="1e7e3-146">Satz-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="1e7e3-146">Set-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Set-AzureRmSqlDatabaseDataMaskingRule.md)


