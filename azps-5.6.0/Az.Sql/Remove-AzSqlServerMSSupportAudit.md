---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/powershell/module/az.sql/Remove-AzSqlServerMSSupportAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerMSSupportAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerMSSupportAudit.md
ms.openlocfilehash: d710137307817223df8cefec6767fecb332bfc3e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940963"
---
# <span data-ttu-id="8b274-101">Remove-AzSqlServerMSSupportAudit</span><span class="sxs-lookup"><span data-stu-id="8b274-101">Remove-AzSqlServerMSSupportAudit</span></span>

## <span data-ttu-id="8b274-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b274-102">SYNOPSIS</span></span>
<span data-ttu-id="8b274-103">Entfernt die Überwachungseinstellungen für Microsoft-Supportvorgänge eines Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="8b274-103">Removes the Microsoft support operations auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="8b274-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8b274-104">SYNTAX</span></span>

### <span data-ttu-id="8b274-105">ServerParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="8b274-105">ServerParameterSet (Default)</span></span>
```
Remove-AzSqlServerMSSupportAudit [-ResourceGroupName] <String> [-ServerName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b274-106">ServerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b274-106">ServerObjectParameterSet</span></span>
```
Remove-AzSqlServerMSSupportAudit -ServerObject <AzureSqlServerModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b274-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8b274-107">DESCRIPTION</span></span>
<span data-ttu-id="8b274-108">Das **Cmdlet Remove-AzSqlServerMSSupportAudit** entfernt die Einstellungen für die Überwachung von Microsoft-Supportvorgängen eines Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="8b274-108">The **Remove-AzSqlServerMSSupportAudit** cmdlet removes the  Microsoft support operations auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="8b274-109">Um das Cmdlet zu verwenden, verwenden Sie die *Parameter ResourceGroupName* und *ServerName,* um den Server zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="8b274-109">To use the cmdlet, use the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>

## <span data-ttu-id="8b274-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8b274-110">EXAMPLES</span></span>

### <span data-ttu-id="8b274-111">Beispiel 1: Entfernen der Überwachungseinstellungen für Microsoft-Supportvorgänge eines Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="8b274-111">Example 1: Remove the Microsoft support operations auditing settings of an Azure SQL server</span></span>
```powershell
PS C:\>Remove-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

### <span data-ttu-id="8b274-112">Beispiel 2: Entfernen Der Microsoft-Supportüberwachungseinstellungen eines Azure SQL Pipeline</span><span class="sxs-lookup"><span data-stu-id="8b274-112">Example 2: Remove, through pipeline, the Microsoft support auditing settings of an Azure SQL server</span></span>
```
PS C:\> Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Remove-AzSqlServerMSSupportAudit
```

## <span data-ttu-id="8b274-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="8b274-113">PARAMETERS</span></span>

### <span data-ttu-id="8b274-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8b274-114">-AsJob</span></span>
<span data-ttu-id="8b274-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="8b274-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8b274-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b274-116">-DefaultProfile</span></span>
<span data-ttu-id="8b274-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8b274-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b274-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b274-118">-ResourceGroupName</span></span>
<span data-ttu-id="8b274-119">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8b274-119">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b274-120">-Servername</span><span class="sxs-lookup"><span data-stu-id="8b274-120">-ServerName</span></span>
<span data-ttu-id="8b274-121">SQL Servername.</span><span class="sxs-lookup"><span data-stu-id="8b274-121">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b274-122">-ServerObject</span><span class="sxs-lookup"><span data-stu-id="8b274-122">-ServerObject</span></span>
<span data-ttu-id="8b274-123">Das Serverobjekt zum Verwalten seiner Überwachungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="8b274-123">The server object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: ServerObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8b274-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8b274-124">-Confirm</span></span>
<span data-ttu-id="8b274-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8b274-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b274-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b274-126">-WhatIf</span></span>
<span data-ttu-id="8b274-127">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8b274-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8b274-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8b274-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b274-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b274-129">CommonParameters</span></span>
<span data-ttu-id="8b274-130">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b274-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b274-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8b274-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b274-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8b274-132">INPUTS</span></span>

### <span data-ttu-id="8b274-133">System.String</span><span class="sxs-lookup"><span data-stu-id="8b274-133">System.String</span></span>

### <span data-ttu-id="8b274-134">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="8b274-134">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="8b274-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8b274-135">OUTPUTS</span></span>

### <span data-ttu-id="8b274-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8b274-136">System.Boolean</span></span>

## <span data-ttu-id="8b274-137">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="8b274-137">NOTES</span></span>

## <span data-ttu-id="8b274-138">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="8b274-138">RELATED LINKS</span></span>
