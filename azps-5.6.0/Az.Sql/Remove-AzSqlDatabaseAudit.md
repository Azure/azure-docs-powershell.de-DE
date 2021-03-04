---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/powershell/module/az.sql/Remove-AzSqlDatabaseAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseAudit.md
ms.openlocfilehash: 9688475a1d8bae19b10bc5626dca643ac947156d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923320"
---
# <span data-ttu-id="8a930-101">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="8a930-101">Remove-AzSqlDatabaseAudit</span></span>

## <span data-ttu-id="8a930-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a930-102">SYNOPSIS</span></span>
<span data-ttu-id="8a930-103">Entfernt die Überwachungseinstellungen einer Azure SQL Datenbank.</span><span class="sxs-lookup"><span data-stu-id="8a930-103">Removes the auditing settings of an Azure SQL database.</span></span>

## <span data-ttu-id="8a930-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8a930-104">SYNTAX</span></span>

### <span data-ttu-id="8a930-105">DatabaseParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="8a930-105">DatabaseParameterSet (Default)</span></span>
```
Remove-AzSqlDatabaseAudit [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a930-106">DatabaseObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a930-106">DatabaseObjectParameterSet</span></span>
```
Remove-AzSqlDatabaseAudit -DatabaseObject <AzureSqlDatabaseModel> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a930-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8a930-107">DESCRIPTION</span></span>
<span data-ttu-id="8a930-108">Das **Cmdlet Remove-AzSqlDatabaseAudit** entfernt die Überwachungseinstellungen einer Azure SQL Datenbank.</span><span class="sxs-lookup"><span data-stu-id="8a930-108">The **Remove-AzSqlDatabaseAudit** cmdlet removes the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="8a930-109">Um das Cmdlet zu verwenden, verwenden Sie die *Parameter ResourceGroupName,* *ServerName* und *DatabaseName,* um die Datenbank zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="8a930-109">To use the cmdlet, use the *ResourceGroupName*, *ServerName*, and *DatabaseName* parameters to identify the database.</span></span>

## <span data-ttu-id="8a930-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8a930-110">EXAMPLES</span></span>

### <span data-ttu-id="8a930-111">Beispiel 1: Entfernen der Überwachungseinstellungen einer Azure SQL Datenbank</span><span class="sxs-lookup"><span data-stu-id="8a930-111">Example 1: Remove the auditing settings of an Azure SQL database</span></span>
```
PS C:\>Remove-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

### <span data-ttu-id="8a930-112">Beispiel 2: Entfernen der Überwachungseinstellungen einer Azure SQL Pipeline</span><span class="sxs-lookup"><span data-stu-id="8a930-112">Example 2: Remove, through pipeline, the auditing settings of an Azure SQL database</span></span>
```
PS C:\> Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Remove-AzSqlDatabaseAudit
```

## <span data-ttu-id="8a930-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="8a930-113">PARAMETERS</span></span>

### <span data-ttu-id="8a930-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8a930-114">-DatabaseName</span></span>
<span data-ttu-id="8a930-115">SQL Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="8a930-115">SQL Database name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a930-116">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="8a930-116">-DatabaseObject</span></span>
<span data-ttu-id="8a930-117">Das Datenbankobjekt zum Verwalten seiner Überwachungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="8a930-117">The database object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: DatabaseObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8a930-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a930-118">-DefaultProfile</span></span>
<span data-ttu-id="8a930-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8a930-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a930-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a930-120">-ResourceGroupName</span></span>
<span data-ttu-id="8a930-121">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8a930-121">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a930-122">-Servername</span><span class="sxs-lookup"><span data-stu-id="8a930-122">-ServerName</span></span>
<span data-ttu-id="8a930-123">SQL Servername.</span><span class="sxs-lookup"><span data-stu-id="8a930-123">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a930-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8a930-124">-Confirm</span></span>
<span data-ttu-id="8a930-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8a930-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a930-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a930-126">-WhatIf</span></span>
<span data-ttu-id="8a930-127">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8a930-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8a930-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8a930-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a930-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a930-129">CommonParameters</span></span>
<span data-ttu-id="8a930-130">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a930-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a930-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8a930-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a930-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8a930-132">INPUTS</span></span>

### <span data-ttu-id="8a930-133">System.String</span><span class="sxs-lookup"><span data-stu-id="8a930-133">System.String</span></span>

### <span data-ttu-id="8a930-134">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="8a930-134">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="8a930-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8a930-135">OUTPUTS</span></span>

### <span data-ttu-id="8a930-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8a930-136">System.Boolean</span></span>

## <span data-ttu-id="8a930-137">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="8a930-137">NOTES</span></span>

## <span data-ttu-id="8a930-138">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="8a930-138">RELATED LINKS</span></span>
