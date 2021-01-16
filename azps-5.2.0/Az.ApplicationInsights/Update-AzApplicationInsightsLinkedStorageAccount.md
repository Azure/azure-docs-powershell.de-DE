---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/update-azapplicationinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Update-AzApplicationInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Update-AzApplicationInsightsLinkedStorageAccount.md
ms.openlocfilehash: 5ef27923fbffc92a0190419cc5949c0b841b95dc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98306715"
---
# <span data-ttu-id="69525-101">Update-AzApplicationInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="69525-101">Update-AzApplicationInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="69525-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69525-102">SYNOPSIS</span></span>
<span data-ttu-id="69525-103">Aktualisieren des verknüpften Speicherkontos für Anwendungserkenntnisse</span><span class="sxs-lookup"><span data-stu-id="69525-103">Update application insights linked storage account</span></span>

## <span data-ttu-id="69525-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="69525-104">SYNTAX</span></span>

### <span data-ttu-id="69525-105">ByResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="69525-105">ByResourceNameParameterSet (Default)</span></span>
```
Update-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName <String> -ComponentName <String>
 -LinkedStorageAccountResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="69525-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="69525-106">ByInputObjectParameterSet</span></span>
```
Update-AzApplicationInsightsLinkedStorageAccount -InputObject <PSApplicationInsightsComponent>
 -LinkedStorageAccountResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="69525-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="69525-107">ByResourceIdParameterSet</span></span>
```
Update-AzApplicationInsightsLinkedStorageAccount -ResourceId <String> -LinkedStorageAccountResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69525-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="69525-108">DESCRIPTION</span></span>
<span data-ttu-id="69525-109">Aktualisieren des verknüpften Speicherkontos für Anwendungserkenntnisse</span><span class="sxs-lookup"><span data-stu-id="69525-109">Update application insights linked storage account</span></span>

## <span data-ttu-id="69525-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="69525-110">EXAMPLES</span></span>

### <span data-ttu-id="69525-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="69525-111">Example 1</span></span>
```powershell
$account = Get-AzStorageAccount -ResourceGroupName "rgName" -Name "accountName"

Get-AzApplicationInsights -ResourceGroupName "rgName" -Name "componentName" | Update-AzApplicationInsightsLinkedStorageAccount -LinkedStorageAccountResourceId $account.Id
```

<span data-ttu-id="69525-112">Aktualisieren Sie das verknüpfte Speicherkonto unter "componentName" der Komponente, um $account</span><span class="sxs-lookup"><span data-stu-id="69525-112">Update linked storage account under component "componentName" to associate with $account</span></span>

## <span data-ttu-id="69525-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="69525-113">PARAMETERS</span></span>

### <span data-ttu-id="69525-114">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="69525-114">-ComponentName</span></span>
<span data-ttu-id="69525-115">Komponentenname</span><span class="sxs-lookup"><span data-stu-id="69525-115">Component Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69525-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69525-116">-DefaultProfile</span></span>
<span data-ttu-id="69525-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="69525-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69525-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="69525-118">-InputObject</span></span>
<span data-ttu-id="69525-119">PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="69525-119">PSApplicationInsightsComponent</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="69525-120">-LinkedStorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="69525-120">-LinkedStorageAccountResourceId</span></span>
<span data-ttu-id="69525-121">Storage Account ResourceId</span><span class="sxs-lookup"><span data-stu-id="69525-121">Storage Account ResourceId</span></span>

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

### <span data-ttu-id="69525-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69525-122">-ResourceGroupName</span></span>
<span data-ttu-id="69525-123">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="69525-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69525-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="69525-124">-ResourceId</span></span>
<span data-ttu-id="69525-125">Component ResourceId</span><span class="sxs-lookup"><span data-stu-id="69525-125">Component ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69525-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="69525-126">-Confirm</span></span>
<span data-ttu-id="69525-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="69525-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69525-128">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="69525-128">-WhatIf</span></span>
<span data-ttu-id="69525-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="69525-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69525-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="69525-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69525-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69525-131">CommonParameters</span></span>
<span data-ttu-id="69525-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69525-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69525-133">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="69525-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69525-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="69525-134">INPUTS</span></span>

### <span data-ttu-id="69525-135">System.String</span><span class="sxs-lookup"><span data-stu-id="69525-135">System.String</span></span>

### <span data-ttu-id="69525-136">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="69525-136">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="69525-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="69525-137">OUTPUTS</span></span>

### <span data-ttu-id="69525-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="69525-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span></span>

## <span data-ttu-id="69525-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="69525-139">NOTES</span></span>

## <span data-ttu-id="69525-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="69525-140">RELATED LINKS</span></span>
