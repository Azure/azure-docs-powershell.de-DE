---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/new-azapplicationinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsLinkedStorageAccount.md
ms.openlocfilehash: 652a5668bd641ae1b68093f431e0aa0963aca50b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98306787"
---
# <span data-ttu-id="6a99d-101">New-AzApplicationInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6a99d-101">New-AzApplicationInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="6a99d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a99d-102">SYNOPSIS</span></span>
<span data-ttu-id="6a99d-103">Erstellen eines verknüpften Speicherkontos für Anwendungserkenntnisse</span><span class="sxs-lookup"><span data-stu-id="6a99d-103">Create an application insights linked storage account</span></span>

## <span data-ttu-id="6a99d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6a99d-104">SYNTAX</span></span>

### <span data-ttu-id="6a99d-105">ByResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="6a99d-105">ByResourceNameParameterSet (Default)</span></span>
```
New-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName <String> -ComponentName <String>
 -LinkedStorageAccountResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6a99d-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6a99d-106">ByInputObjectParameterSet</span></span>
```
New-AzApplicationInsightsLinkedStorageAccount -InputObject <PSApplicationInsightsComponent>
 -LinkedStorageAccountResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6a99d-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6a99d-107">ByResourceIdParameterSet</span></span>
```
New-AzApplicationInsightsLinkedStorageAccount -ResourceId <String> -LinkedStorageAccountResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a99d-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6a99d-108">DESCRIPTION</span></span>
<span data-ttu-id="6a99d-109">Erstellen eines verknüpften Speicherkontos für Anwendungserkenntnisse</span><span class="sxs-lookup"><span data-stu-id="6a99d-109">Create an application insights linked storage account</span></span>

## <span data-ttu-id="6a99d-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6a99d-110">EXAMPLES</span></span>

### <span data-ttu-id="6a99d-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6a99d-111">Example 1</span></span>
```powershell
$account = Get-AzStorageAccount -ResourceGroupName "rgName" -Name "accountName"

Get-AzApplicationInsights -ResourceGroupName "rgName" -Name "componentName" | New-AzApplicationInsightsLinkedStorageAccount -LinkedStorageAccountResourceId $account.Id
```

<span data-ttu-id="6a99d-112">Erstellen eines verknüpften Speicherkontos $account "componentName" der Komponente</span><span class="sxs-lookup"><span data-stu-id="6a99d-112">Create linked storage account $account under component "componentName"</span></span>

## <span data-ttu-id="6a99d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6a99d-113">PARAMETERS</span></span>

### <span data-ttu-id="6a99d-114">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="6a99d-114">-ComponentName</span></span>
<span data-ttu-id="6a99d-115">Komponentenname</span><span class="sxs-lookup"><span data-stu-id="6a99d-115">Component Name</span></span>

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

### <span data-ttu-id="6a99d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a99d-116">-DefaultProfile</span></span>
<span data-ttu-id="6a99d-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6a99d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a99d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6a99d-118">-InputObject</span></span>
<span data-ttu-id="6a99d-119">PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="6a99d-119">PSApplicationInsightsComponent</span></span>

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

### <span data-ttu-id="6a99d-120">-LinkedStorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="6a99d-120">-LinkedStorageAccountResourceId</span></span>
<span data-ttu-id="6a99d-121">Storage Account ResourceId</span><span class="sxs-lookup"><span data-stu-id="6a99d-121">Storage Account ResourceId</span></span>

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

### <span data-ttu-id="6a99d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a99d-122">-ResourceGroupName</span></span>
<span data-ttu-id="6a99d-123">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="6a99d-123">Resource Group Name</span></span>

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

### <span data-ttu-id="6a99d-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6a99d-124">-ResourceId</span></span>
<span data-ttu-id="6a99d-125">Component ResourceId</span><span class="sxs-lookup"><span data-stu-id="6a99d-125">Component ResourceId</span></span>

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

### <span data-ttu-id="6a99d-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6a99d-126">-Confirm</span></span>
<span data-ttu-id="6a99d-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6a99d-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a99d-128">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="6a99d-128">-WhatIf</span></span>
<span data-ttu-id="6a99d-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6a99d-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a99d-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6a99d-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a99d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a99d-131">CommonParameters</span></span>
<span data-ttu-id="6a99d-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a99d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a99d-133">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6a99d-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a99d-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6a99d-134">INPUTS</span></span>

### <span data-ttu-id="6a99d-135">System.String</span><span class="sxs-lookup"><span data-stu-id="6a99d-135">System.String</span></span>

### <span data-ttu-id="6a99d-136">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="6a99d-136">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="6a99d-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6a99d-137">OUTPUTS</span></span>

### <span data-ttu-id="6a99d-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="6a99d-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span></span>

## <span data-ttu-id="6a99d-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6a99d-139">NOTES</span></span>

## <span data-ttu-id="6a99d-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6a99d-140">RELATED LINKS</span></span>
