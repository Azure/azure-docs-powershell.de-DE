---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 1B138185-E836-414F-93CD-7BAE7F474E73
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasedatamaskingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingPolicy.md
ms.openlocfilehash: d4a167871e452cb12533e38793fae463ba6f8dc8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98458396"
---
# <span data-ttu-id="0eae2-101">Set-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="0eae2-101">Set-AzSqlDatabaseDataMaskingPolicy</span></span>

## <span data-ttu-id="0eae2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0eae2-102">SYNOPSIS</span></span>
<span data-ttu-id="0eae2-103">Legt die Datenmaskierung für eine Datenbank fest.</span><span class="sxs-lookup"><span data-stu-id="0eae2-103">Sets data masking for a database.</span></span>

## <span data-ttu-id="0eae2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0eae2-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseDataMaskingPolicy [-PassThru] [-PrivilegedUsers <String>] [-DataMaskingState <String>]
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0eae2-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0eae2-105">DESCRIPTION</span></span>
<span data-ttu-id="0eae2-106">Das **Cmdlet "Set-AzSqlDatabaseDataMaskingPolicy"** legt die Datenmaskierungsrichtlinie für eine Azure SQL fest.</span><span class="sxs-lookup"><span data-stu-id="0eae2-106">The **Set-AzSqlDatabaseDataMaskingPolicy** cmdlet sets the data masking policy for an Azure SQL database.</span></span>
<span data-ttu-id="0eae2-107">Um dieses Cmdlet zu verwenden, verwenden Sie die Parameter *"ResourceGroupName",* *"ServerName"* und *"DatabaseName",* um die Datenbank zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="0eae2-107">To use this cmdlet, use the *ResourceGroupName*, *ServerName*, and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="0eae2-108">Sie können den Parameter *"DataMaskingState"* festlegen, um anzugeben, ob Datenmaskierungsvorgänge aktiviert oder deaktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="0eae2-108">You can set the *DataMaskingState* parameter to specify whether data masking operations are enabled or disabled.</span></span>
<span data-ttu-id="0eae2-109">Wenn das Cmdlet erfolgreich ist und der *Parameter "PassThru"* verwendet wird, wird zusätzlich zu den Datenbankbezeichnern ein Objekt zurückgegeben, das die aktuelle Datenmaskierungsrichtlinie beschreibt.</span><span class="sxs-lookup"><span data-stu-id="0eae2-109">If the cmdlet succeeds and the *PassThru* parameter is used, it returns an object describing the current data masking policy in addition to the database identifiers.</span></span>
<span data-ttu-id="0eae2-110">Datenbankbezeichner umfassen, sind aber nicht beschränkt **auf, ResourceGroupName,** **ServerName** und **DatabaseName.**</span><span class="sxs-lookup"><span data-stu-id="0eae2-110">Database identifiers include, but are not limited to, **ResourceGroupName**, **ServerName**, and **DatabaseName**.</span></span>
<span data-ttu-id="0eae2-111">Dieses Cmdlet wird auch vom Dienst SQL Server Stretch Database in Azure unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0eae2-111">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="0eae2-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0eae2-112">EXAMPLES</span></span>

### <span data-ttu-id="0eae2-113">Beispiel 1: Festlegen der Datenmaskierungsrichtlinie für eine Datenbank</span><span class="sxs-lookup"><span data-stu-id="0eae2-113">Example 1: Set the data masking policy for a database</span></span>
```
PS C:\>Set-AzSqlDatabaseDataMaskingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01 -PrivilegedUsers "public" -DataMaskingState "Enabled"
```

<span data-ttu-id="0eae2-114">Mit diesem Befehl wird die Datenmaskierungsrichtlinie für eine Datenbank mit dem Namen "database01" auf dem Server "server01" definiert.</span><span class="sxs-lookup"><span data-stu-id="0eae2-114">This command sets the data masking policy for a database named database01 on the server named server01.</span></span>

## <span data-ttu-id="0eae2-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0eae2-115">PARAMETERS</span></span>

### <span data-ttu-id="0eae2-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0eae2-116">-DatabaseName</span></span>
<span data-ttu-id="0eae2-117">Gibt den Namen der Datenbank an, in der die Richtlinie festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="0eae2-117">Specifies the name of the database where the policy is set.</span></span>

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

### <span data-ttu-id="0eae2-118">-DataMaskingState</span><span class="sxs-lookup"><span data-stu-id="0eae2-118">-DataMaskingState</span></span>
<span data-ttu-id="0eae2-119">Gibt an, ob der Datenmaskierungsvorgang aktiviert oder deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="0eae2-119">Specifies whether data masking operation is enabled or disabled.</span></span>
<span data-ttu-id="0eae2-120">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="0eae2-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0eae2-121">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="0eae2-121">Enabled</span></span>
- <span data-ttu-id="0eae2-122">Deaktiviert Der Standardwert ist "Enabled".</span><span class="sxs-lookup"><span data-stu-id="0eae2-122">Disabled The default value is Enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0eae2-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0eae2-123">-DefaultProfile</span></span>
<span data-ttu-id="0eae2-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="0eae2-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0eae2-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0eae2-125">-PassThru</span></span>
<span data-ttu-id="0eae2-126">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="0eae2-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0eae2-127">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="0eae2-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0eae2-128">-PrivilegedUsers</span><span class="sxs-lookup"><span data-stu-id="0eae2-128">-PrivilegedUsers</span></span>
<span data-ttu-id="0eae2-129">Gibt eine durch Semikolons getrennte Liste mit privilegierten Benutzer-IDs an.</span><span class="sxs-lookup"><span data-stu-id="0eae2-129">Specifies a semicolon-separated list of privileged user IDs.</span></span>
<span data-ttu-id="0eae2-130">Diese Benutzer können die Maskierungsdaten anzeigen.</span><span class="sxs-lookup"><span data-stu-id="0eae2-130">These users are allowed to view the masking data.</span></span>

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

### <span data-ttu-id="0eae2-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0eae2-131">-ResourceGroupName</span></span>
<span data-ttu-id="0eae2-132">Gibt den Namen der Ressourcengruppe an, der die Datenbank zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="0eae2-132">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="0eae2-133">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0eae2-133">-ServerName</span></span>
<span data-ttu-id="0eae2-134">Gibt den Namen des Servers an, auf dem die Datenbank hosten soll.</span><span class="sxs-lookup"><span data-stu-id="0eae2-134">Specifies the name of the server hosting the database.</span></span>

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

### <span data-ttu-id="0eae2-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0eae2-135">-Confirm</span></span>
<span data-ttu-id="0eae2-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0eae2-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0eae2-137">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="0eae2-137">-WhatIf</span></span>
<span data-ttu-id="0eae2-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0eae2-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0eae2-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0eae2-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0eae2-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0eae2-140">CommonParameters</span></span>
<span data-ttu-id="0eae2-141">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0eae2-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0eae2-142">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0eae2-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0eae2-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0eae2-143">INPUTS</span></span>

### <span data-ttu-id="0eae2-144">System.String</span><span class="sxs-lookup"><span data-stu-id="0eae2-144">System.String</span></span>

## <span data-ttu-id="0eae2-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0eae2-145">OUTPUTS</span></span>

### <span data-ttu-id="0eae2-146">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="0eae2-146">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingPolicyModel</span></span>

## <span data-ttu-id="0eae2-147">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0eae2-147">NOTES</span></span>

## <span data-ttu-id="0eae2-148">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0eae2-148">RELATED LINKS</span></span>

[<span data-ttu-id="0eae2-149">Get-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="0eae2-149">Get-AzSqlDatabaseDataMaskingPolicy</span></span>](./Get-AzSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="0eae2-150">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="0eae2-150">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="0eae2-151">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="0eae2-151">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="0eae2-152">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="0eae2-152">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="0eae2-153">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="0eae2-153">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="0eae2-154">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="0eae2-154">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


