---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 848A6972-AB29-46FB-8E03-FF2ADB113A0E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: ced87eb217347629752683be5c72229da92dea64
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481474"
---
# <span data-ttu-id="86c67-101">Get-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="86c67-101">Get-AzureRmSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="86c67-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="86c67-102">SYNOPSIS</span></span>
<span data-ttu-id="86c67-103">Ruft die Regeln für die Daten Maskierung aus einer Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="86c67-103">Gets the data masking rules from a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="86c67-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="86c67-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseDataMaskingRule [-SchemaName <String>] [-TableName <String>] [-ColumnName <String>]
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86c67-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="86c67-105">DESCRIPTION</span></span>
<span data-ttu-id="86c67-106">Das Cmdlet " **Get-AzureRmSqlDatabaseDataMaskingRule** " erhält entweder eine bestimmte Daten Maskierungs Regel oder alle Daten Maskierungs Regeln für eine Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="86c67-106">The **Get-AzureRmSqlDatabaseDataMaskingRule** cmdlet gets either a specific data masking rule or all of the data masking rules for an Azure SQL database.</span></span>
<span data-ttu-id="86c67-107">Um das Cmdlet zu verwenden, verwenden Sie die *ResourceGroupName* -, *Servername* -und *DatabaseName* -Parameter, um die Datenbank zu identifizieren, und den Parameter " *rulecode* ", um anzugeben, welche Regel dieses Cmdlet zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="86c67-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database, and the *RuleId* parameter to specify which rule this cmdlet returns.</span></span>
<span data-ttu-id="86c67-108">Wenn Sie keine Regel- *Nr* angeben, werden alle Daten Maskierungs Regeln für diese Azure SQL-Datenbank zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="86c67-108">If you do not provide *RuleId* , all the data masking rules for that Azure SQL database are returned.</span></span>

<span data-ttu-id="86c67-109">Dieses Cmdlet wird auch vom SQL Server Stretch-Datenbankdienst auf Azure unterstützt.</span><span class="sxs-lookup"><span data-stu-id="86c67-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="86c67-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="86c67-110">EXAMPLES</span></span>

### <span data-ttu-id="86c67-111">Beispiel 1: Abrufen aller Regeln für die Daten Maskierung aus einer Datenbank</span><span class="sxs-lookup"><span data-stu-id="86c67-111">Example 1: Get all data masking rules from a database</span></span>
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

### <span data-ttu-id="86c67-112">Beispiel 2: Abrufen der für das Schema "dbo" definierten Daten Maskierungs Regel, Tabelle "Tabelle1" und Spalte "Spalte1"</span><span class="sxs-lookup"><span data-stu-id="86c67-112">Example 2: Get the data masking rule defined on schema "dbo", table "table1" and column "column1".</span></span>
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

## <span data-ttu-id="86c67-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="86c67-113">PARAMETERS</span></span>

### <span data-ttu-id="86c67-114">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="86c67-114">-ColumnName</span></span>
<span data-ttu-id="86c67-115">Gibt den Namen der Spalte an, auf die die Maskierungs Regel ausgerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="86c67-115">Specifies the name of the column targeted by the masking rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86c67-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="86c67-116">-DatabaseName</span></span>
<span data-ttu-id="86c67-117">Gibt den Namen der Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="86c67-117">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="86c67-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86c67-118">-ResourceGroupName</span></span>
<span data-ttu-id="86c67-119">Gibt den Namen der Ressourcengruppe an, der die Datenbank zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="86c67-119">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="86c67-120">-Schemaname</span><span class="sxs-lookup"><span data-stu-id="86c67-120">-SchemaName</span></span>
<span data-ttu-id="86c67-121">Gibt den Namen eines Schemas an.</span><span class="sxs-lookup"><span data-stu-id="86c67-121">Specifies the name of a schema.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86c67-122">-Servername</span><span class="sxs-lookup"><span data-stu-id="86c67-122">-ServerName</span></span>
<span data-ttu-id="86c67-123">Gibt den Namen des Servers an.</span><span class="sxs-lookup"><span data-stu-id="86c67-123">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="86c67-124">-Tabellenname</span><span class="sxs-lookup"><span data-stu-id="86c67-124">-TableName</span></span>
<span data-ttu-id="86c67-125">Gibt den Namen einer Azure SQL-Tabelle an.</span><span class="sxs-lookup"><span data-stu-id="86c67-125">Specifies the name of an Azure SQL table.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86c67-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="86c67-126">-Confirm</span></span>
<span data-ttu-id="86c67-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="86c67-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86c67-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86c67-128">-WhatIf</span></span>
<span data-ttu-id="86c67-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="86c67-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86c67-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="86c67-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86c67-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86c67-131">-DefaultProfile</span></span>
<span data-ttu-id="86c67-132">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="86c67-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="86c67-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86c67-133">CommonParameters</span></span>
<span data-ttu-id="86c67-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86c67-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86c67-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86c67-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86c67-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="86c67-136">INPUTS</span></span>

###  
<span data-ttu-id="86c67-137">Keine.</span><span class="sxs-lookup"><span data-stu-id="86c67-137">None.</span></span>

## <span data-ttu-id="86c67-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="86c67-138">OUTPUTS</span></span>

### <span data-ttu-id="86c67-139">Microsoft. Azure. Commands. SQL. Security. Model. DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="86c67-139">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="86c67-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="86c67-140">NOTES</span></span>

## <span data-ttu-id="86c67-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="86c67-141">RELATED LINKS</span></span>

[<span data-ttu-id="86c67-142">Get-AzureRmSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="86c67-142">Get-AzureRmSqlDatabaseDataMaskingPolicy</span></span>](./Get-AzureRmSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="86c67-143">Neu – AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="86c67-143">New-AzureRmSqlDatabaseDataMaskingRule</span></span>](./New-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="86c67-144">Remove-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="86c67-144">Remove-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Remove-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="86c67-145">Satz-AzureRmSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="86c67-145">Set-AzureRmSqlDatabaseDataMaskingPolicy</span></span>](./Set-AzureRmSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="86c67-146">Satz-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="86c67-146">Set-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Set-AzureRmSqlDatabaseDataMaskingRule.md)


