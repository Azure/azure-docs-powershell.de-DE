---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 5C1C51FE-747F-4176-84ED-A28AA3475581
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsDataSource.md
ms.openlocfilehash: bba48b31158226d1ea63f70ceafe3355990fea6e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359174"
---
# <span data-ttu-id="f11cb-101">Remove-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="f11cb-101">Remove-AzOperationalInsightsDataSource</span></span>

## <span data-ttu-id="f11cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f11cb-102">SYNOPSIS</span></span>
<span data-ttu-id="f11cb-103">Löscht eine Datenquelle.</span><span class="sxs-lookup"><span data-stu-id="f11cb-103">Deletes a data source.</span></span>

## <span data-ttu-id="f11cb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f11cb-104">SYNTAX</span></span>

### <span data-ttu-id="f11cb-105">ByWorkspaceName (Standard)</span><span class="sxs-lookup"><span data-stu-id="f11cb-105">ByWorkspaceName (Default)</span></span>
```
Remove-AzOperationalInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String> [-Name] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f11cb-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="f11cb-106">ByWorkspaceObject</span></span>
```
Remove-AzOperationalInsightsDataSource [-Workspace] <PSWorkspace> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f11cb-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f11cb-107">DESCRIPTION</span></span>
<span data-ttu-id="f11cb-108">Das **Cmdlet "Remove-AzOperationalInsightsDataSource"** löscht eine Datenquelle.</span><span class="sxs-lookup"><span data-stu-id="f11cb-108">The **Remove-AzOperationalInsightsDataSource** cmdlet deletes a data source.</span></span>

## <span data-ttu-id="f11cb-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f11cb-109">EXAMPLES</span></span>

## <span data-ttu-id="f11cb-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f11cb-110">PARAMETERS</span></span>

### <span data-ttu-id="f11cb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f11cb-111">-DefaultProfile</span></span>
<span data-ttu-id="f11cb-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="f11cb-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f11cb-113">-Force</span><span class="sxs-lookup"><span data-stu-id="f11cb-113">-Force</span></span>
<span data-ttu-id="f11cb-114">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="f11cb-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f11cb-115">-Name</span><span class="sxs-lookup"><span data-stu-id="f11cb-115">-Name</span></span>
<span data-ttu-id="f11cb-116">Gibt den Namen einer zu löschenden Datenquelle an.</span><span class="sxs-lookup"><span data-stu-id="f11cb-116">Specifies the name of a data source to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f11cb-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f11cb-117">-ResourceGroupName</span></span>
<span data-ttu-id="f11cb-118">Gibt den Namen einer Ressourcengruppe an, die Computer enthält.</span><span class="sxs-lookup"><span data-stu-id="f11cb-118">Specifies the name of a resource group that contains computers.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f11cb-119">-Workspace</span><span class="sxs-lookup"><span data-stu-id="f11cb-119">-Workspace</span></span>
<span data-ttu-id="f11cb-120">Gibt einen Arbeitsbereich an, in dem dieses Cmdlet betrieben wird.</span><span class="sxs-lookup"><span data-stu-id="f11cb-120">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f11cb-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f11cb-121">-WorkspaceName</span></span>
<span data-ttu-id="f11cb-122">Gibt den Namen eines Arbeitsbereichs an, in dem dieses Cmdlet betrieben wird.</span><span class="sxs-lookup"><span data-stu-id="f11cb-122">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f11cb-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f11cb-123">-Confirm</span></span>
<span data-ttu-id="f11cb-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f11cb-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f11cb-125">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f11cb-125">-WhatIf</span></span>
<span data-ttu-id="f11cb-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f11cb-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f11cb-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f11cb-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f11cb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f11cb-128">CommonParameters</span></span>
<span data-ttu-id="f11cb-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f11cb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f11cb-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f11cb-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f11cb-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f11cb-131">INPUTS</span></span>

### <span data-ttu-id="f11cb-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="f11cb-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="f11cb-133">System.String</span><span class="sxs-lookup"><span data-stu-id="f11cb-133">System.String</span></span>

## <span data-ttu-id="f11cb-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f11cb-134">OUTPUTS</span></span>

### <span data-ttu-id="f11cb-135">System.Void</span><span class="sxs-lookup"><span data-stu-id="f11cb-135">System.Void</span></span>

## <span data-ttu-id="f11cb-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f11cb-136">NOTES</span></span>
* <span data-ttu-id="f11cb-137">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, operational, insights</span><span class="sxs-lookup"><span data-stu-id="f11cb-137">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="f11cb-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f11cb-138">RELATED LINKS</span></span>

[<span data-ttu-id="f11cb-139">Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="f11cb-139">Get-AzOperationalInsightsDataSource</span></span>](./Get-AzOperationalInsightsDataSource.md)

[<span data-ttu-id="f11cb-140">Set-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="f11cb-140">Set-AzOperationalInsightsDataSource</span></span>](./Set-AzOperationalInsightsDataSource.md)


