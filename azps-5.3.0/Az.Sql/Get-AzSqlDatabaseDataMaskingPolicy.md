---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: FFC02A5D-A12F-494D-8542-76A5B89E32DC
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasedatamaskingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseDataMaskingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseDataMaskingPolicy.md
ms.openlocfilehash: 8fb1b8125a6fd0c42bedc00733f3a128846673e4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98375079"
---
# <span data-ttu-id="15f94-101">Get-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="15f94-101">Get-AzSqlDatabaseDataMaskingPolicy</span></span>

## <span data-ttu-id="15f94-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15f94-102">SYNOPSIS</span></span>
<span data-ttu-id="15f94-103">Ruft die Datenmaskierungsrichtlinie für eine Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="15f94-103">Gets the data masking policy for a database.</span></span>

## <span data-ttu-id="15f94-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="15f94-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseDataMaskingPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="15f94-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="15f94-105">DESCRIPTION</span></span>
<span data-ttu-id="15f94-106">Das **Cmdlet "Get-AzSqlDatabaseDataMaskingPolicy"** ruft die Datenmaskierungsrichtlinie einer Azure SQL ab.</span><span class="sxs-lookup"><span data-stu-id="15f94-106">The **Get-AzSqlDatabaseDataMaskingPolicy** cmdlet gets the data masking policy of an Azure SQL database.</span></span>
<span data-ttu-id="15f94-107">Um dieses Cmdlet zu verwenden, verwenden Sie die Parameter *"ResourceGroupName",* *"ServerName"* und *"DatabaseName",* um die Datenbank zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="15f94-107">To use this cmdlet, use the *ResourceGroupName*, *ServerName*, and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="15f94-108">Dieses Cmdlet wird auch vom Dienst SQL Server Stretch Database in Azure unterstützt.</span><span class="sxs-lookup"><span data-stu-id="15f94-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="15f94-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="15f94-109">EXAMPLES</span></span>

### <span data-ttu-id="15f94-110">Beispiel 1: Erhalten der Datenmaskierungsrichtlinie für eine Azure SQL Datenbank</span><span class="sxs-lookup"><span data-stu-id="15f94-110">Example 1: Get the data masking policy for an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseDataMaskingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName      : Database01
ResourceGroupName : ResourceGroup01
ServerName        : Server01
DataMaskingState  : Enabled
PrivilegedUsers  :
```

<span data-ttu-id="15f94-111">Dieser Befehl ruft die Datenformatierungsrichtlinie aus datenbankdatenbank01 in der Ressourcengruppe "ResourceGroup01" auf Server Server01 ab.</span><span class="sxs-lookup"><span data-stu-id="15f94-111">This command gets the data masking policy from database Database01 in resource group ResourceGroup01 on server Server01.</span></span>

## <span data-ttu-id="15f94-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="15f94-112">PARAMETERS</span></span>

### <span data-ttu-id="15f94-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="15f94-113">-DatabaseName</span></span>
<span data-ttu-id="15f94-114">Gibt den Namen der Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="15f94-114">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="15f94-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15f94-115">-DefaultProfile</span></span>
<span data-ttu-id="15f94-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="15f94-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="15f94-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15f94-117">-ResourceGroupName</span></span>
<span data-ttu-id="15f94-118">Gibt den Namen der Ressourcengruppe an, der die Datenbank zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="15f94-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="15f94-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="15f94-119">-ServerName</span></span>
<span data-ttu-id="15f94-120">Gibt den Namen des Servers an, auf dem sich die Datenbank befindet.</span><span class="sxs-lookup"><span data-stu-id="15f94-120">Specifies the name of the server where the database is located.</span></span>

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

### <span data-ttu-id="15f94-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="15f94-121">-Confirm</span></span>
<span data-ttu-id="15f94-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="15f94-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15f94-123">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="15f94-123">-WhatIf</span></span>
<span data-ttu-id="15f94-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="15f94-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15f94-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="15f94-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15f94-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15f94-126">CommonParameters</span></span>
<span data-ttu-id="15f94-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15f94-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15f94-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="15f94-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15f94-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="15f94-129">INPUTS</span></span>

### <span data-ttu-id="15f94-130">System.String</span><span class="sxs-lookup"><span data-stu-id="15f94-130">System.String</span></span>

## <span data-ttu-id="15f94-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="15f94-131">OUTPUTS</span></span>

### <span data-ttu-id="15f94-132">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="15f94-132">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingPolicyModel</span></span>

## <span data-ttu-id="15f94-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="15f94-133">NOTES</span></span>

## <span data-ttu-id="15f94-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="15f94-134">RELATED LINKS</span></span>

[<span data-ttu-id="15f94-135">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="15f94-135">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="15f94-136">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="15f94-136">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="15f94-137">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="15f94-137">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="15f94-138">Set-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="15f94-138">Set-AzSqlDatabaseDataMaskingPolicy</span></span>](./Set-AzSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="15f94-139">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="15f94-139">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)


