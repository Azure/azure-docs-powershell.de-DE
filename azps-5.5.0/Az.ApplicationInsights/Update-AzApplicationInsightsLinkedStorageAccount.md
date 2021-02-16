---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/update-azapplicationinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Update-AzApplicationInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Update-AzApplicationInsightsLinkedStorageAccount.md
ms.openlocfilehash: 5ef27923fbffc92a0190419cc5949c0b841b95dc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149457"
---
# <span data-ttu-id="2fca3-101">Update-AzApplicationInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2fca3-101">Update-AzApplicationInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="2fca3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2fca3-102">SYNOPSIS</span></span>
<span data-ttu-id="2fca3-103">Aktualisieren eines verknüpften Speicherkontos mit Anwendungserkenntnissen</span><span class="sxs-lookup"><span data-stu-id="2fca3-103">Update application insights linked storage account</span></span>

## <span data-ttu-id="2fca3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2fca3-104">SYNTAX</span></span>

### <span data-ttu-id="2fca3-105">ByResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="2fca3-105">ByResourceNameParameterSet (Default)</span></span>
```
Update-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName <String> -ComponentName <String>
 -LinkedStorageAccountResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2fca3-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2fca3-106">ByInputObjectParameterSet</span></span>
```
Update-AzApplicationInsightsLinkedStorageAccount -InputObject <PSApplicationInsightsComponent>
 -LinkedStorageAccountResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2fca3-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2fca3-107">ByResourceIdParameterSet</span></span>
```
Update-AzApplicationInsightsLinkedStorageAccount -ResourceId <String> -LinkedStorageAccountResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2fca3-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2fca3-108">DESCRIPTION</span></span>
<span data-ttu-id="2fca3-109">Aktualisieren eines verknüpften Speicherkontos mit Anwendungserkenntnissen</span><span class="sxs-lookup"><span data-stu-id="2fca3-109">Update application insights linked storage account</span></span>

## <span data-ttu-id="2fca3-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2fca3-110">EXAMPLES</span></span>

### <span data-ttu-id="2fca3-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2fca3-111">Example 1</span></span>
```powershell
$account = Get-AzStorageAccount -ResourceGroupName "rgName" -Name "accountName"

Get-AzApplicationInsights -ResourceGroupName "rgName" -Name "componentName" | Update-AzApplicationInsightsLinkedStorageAccount -LinkedStorageAccountResourceId $account.Id
```

<span data-ttu-id="2fca3-112">Aktualisieren Sie das verknüpfte Speicherkonto unter "componentName" der Komponente, um es $account</span><span class="sxs-lookup"><span data-stu-id="2fca3-112">Update linked storage account under component "componentName" to associate with $account</span></span>

## <span data-ttu-id="2fca3-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2fca3-113">PARAMETERS</span></span>

### <span data-ttu-id="2fca3-114">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="2fca3-114">-ComponentName</span></span>
<span data-ttu-id="2fca3-115">Komponentenname</span><span class="sxs-lookup"><span data-stu-id="2fca3-115">Component Name</span></span>

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

### <span data-ttu-id="2fca3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fca3-116">-DefaultProfile</span></span>
<span data-ttu-id="2fca3-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2fca3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2fca3-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2fca3-118">-InputObject</span></span>
<span data-ttu-id="2fca3-119">PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="2fca3-119">PSApplicationInsightsComponent</span></span>

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

### <span data-ttu-id="2fca3-120">-LinkedStorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="2fca3-120">-LinkedStorageAccountResourceId</span></span>
<span data-ttu-id="2fca3-121">Storage Account ResourceId</span><span class="sxs-lookup"><span data-stu-id="2fca3-121">Storage Account ResourceId</span></span>

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

### <span data-ttu-id="2fca3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fca3-122">-ResourceGroupName</span></span>
<span data-ttu-id="2fca3-123">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="2fca3-123">Resource Group Name</span></span>

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

### <span data-ttu-id="2fca3-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2fca3-124">-ResourceId</span></span>
<span data-ttu-id="2fca3-125">Component ResourceId</span><span class="sxs-lookup"><span data-stu-id="2fca3-125">Component ResourceId</span></span>

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

### <span data-ttu-id="2fca3-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2fca3-126">-Confirm</span></span>
<span data-ttu-id="2fca3-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2fca3-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2fca3-128">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="2fca3-128">-WhatIf</span></span>
<span data-ttu-id="2fca3-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2fca3-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2fca3-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2fca3-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2fca3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fca3-131">CommonParameters</span></span>
<span data-ttu-id="2fca3-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fca3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fca3-133">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2fca3-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fca3-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2fca3-134">INPUTS</span></span>

### <span data-ttu-id="2fca3-135">System.String</span><span class="sxs-lookup"><span data-stu-id="2fca3-135">System.String</span></span>

### <span data-ttu-id="2fca3-136">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="2fca3-136">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="2fca3-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2fca3-137">OUTPUTS</span></span>

### <span data-ttu-id="2fca3-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="2fca3-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span></span>

## <span data-ttu-id="2fca3-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2fca3-139">NOTES</span></span>

## <span data-ttu-id="2fca3-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2fca3-140">RELATED LINKS</span></span>
