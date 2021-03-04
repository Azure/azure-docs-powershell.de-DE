---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/powershell/module/az.applicationinsights/new-azapplicationinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsLinkedStorageAccount.md
ms.openlocfilehash: ed7114f37cebb093c8ba27ed60c0328234571f06
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938344"
---
# <span data-ttu-id="d22f8-101">New-AzApplicationInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d22f8-101">New-AzApplicationInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="d22f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d22f8-102">SYNOPSIS</span></span>
<span data-ttu-id="d22f8-103">Erstellen eines verknüpften Speicherkontos für Anwendungseinblicke</span><span class="sxs-lookup"><span data-stu-id="d22f8-103">Create an application insights linked storage account</span></span>

## <span data-ttu-id="d22f8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d22f8-104">SYNTAX</span></span>

### <span data-ttu-id="d22f8-105">ByResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d22f8-105">ByResourceNameParameterSet (Default)</span></span>
```
New-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName <String> -ComponentName <String>
 -LinkedStorageAccountResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d22f8-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d22f8-106">ByInputObjectParameterSet</span></span>
```
New-AzApplicationInsightsLinkedStorageAccount -InputObject <PSApplicationInsightsComponent>
 -LinkedStorageAccountResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d22f8-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d22f8-107">ByResourceIdParameterSet</span></span>
```
New-AzApplicationInsightsLinkedStorageAccount -ResourceId <String> -LinkedStorageAccountResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d22f8-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d22f8-108">DESCRIPTION</span></span>
<span data-ttu-id="d22f8-109">Erstellen eines verknüpften Speicherkontos für Anwendungseinblicke</span><span class="sxs-lookup"><span data-stu-id="d22f8-109">Create an application insights linked storage account</span></span>

## <span data-ttu-id="d22f8-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d22f8-110">EXAMPLES</span></span>

### <span data-ttu-id="d22f8-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d22f8-111">Example 1</span></span>
```powershell
$account = Get-AzStorageAccount -ResourceGroupName "rgName" -Name "accountName"

Get-AzApplicationInsights -ResourceGroupName "rgName" -Name "componentName" | New-AzApplicationInsightsLinkedStorageAccount -LinkedStorageAccountResourceId $account.Id
```

<span data-ttu-id="d22f8-112">Erstellen eines verknüpften Speicherkontos $account Komponente "componentName"</span><span class="sxs-lookup"><span data-stu-id="d22f8-112">Create linked storage account $account under component "componentName"</span></span>

## <span data-ttu-id="d22f8-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d22f8-113">PARAMETERS</span></span>

### <span data-ttu-id="d22f8-114">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="d22f8-114">-ComponentName</span></span>
<span data-ttu-id="d22f8-115">Komponentenname</span><span class="sxs-lookup"><span data-stu-id="d22f8-115">Component Name</span></span>

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

### <span data-ttu-id="d22f8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d22f8-116">-DefaultProfile</span></span>
<span data-ttu-id="d22f8-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d22f8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d22f8-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d22f8-118">-InputObject</span></span>
<span data-ttu-id="d22f8-119">PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="d22f8-119">PSApplicationInsightsComponent</span></span>

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

### <span data-ttu-id="d22f8-120">-LinkedStorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="d22f8-120">-LinkedStorageAccountResourceId</span></span>
<span data-ttu-id="d22f8-121">ResourceId des Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="d22f8-121">Storage Account ResourceId</span></span>

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

### <span data-ttu-id="d22f8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d22f8-122">-ResourceGroupName</span></span>
<span data-ttu-id="d22f8-123">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="d22f8-123">Resource Group Name</span></span>

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

### <span data-ttu-id="d22f8-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d22f8-124">-ResourceId</span></span>
<span data-ttu-id="d22f8-125">Component ResourceId</span><span class="sxs-lookup"><span data-stu-id="d22f8-125">Component ResourceId</span></span>

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

### <span data-ttu-id="d22f8-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d22f8-126">-Confirm</span></span>
<span data-ttu-id="d22f8-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d22f8-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d22f8-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d22f8-128">-WhatIf</span></span>
<span data-ttu-id="d22f8-129">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d22f8-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d22f8-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d22f8-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d22f8-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d22f8-131">CommonParameters</span></span>
<span data-ttu-id="d22f8-132">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d22f8-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d22f8-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d22f8-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d22f8-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d22f8-134">INPUTS</span></span>

### <span data-ttu-id="d22f8-135">System.String</span><span class="sxs-lookup"><span data-stu-id="d22f8-135">System.String</span></span>

### <span data-ttu-id="d22f8-136">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="d22f8-136">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="d22f8-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d22f8-137">OUTPUTS</span></span>

### <span data-ttu-id="d22f8-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="d22f8-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span></span>

## <span data-ttu-id="d22f8-139">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="d22f8-139">NOTES</span></span>

## <span data-ttu-id="d22f8-140">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="d22f8-140">RELATED LINKS</span></span>
