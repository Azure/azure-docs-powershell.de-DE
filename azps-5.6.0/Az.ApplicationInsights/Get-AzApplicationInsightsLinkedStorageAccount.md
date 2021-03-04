---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/powershell/module/az.applicationinsights/get-azapplicationinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsLinkedStorageAccount.md
ms.openlocfilehash: a059209e993f17ffb5eed1b29d1854f8387f3d8c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925232"
---
# <span data-ttu-id="8dd4d-101">Get-AzApplicationInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8dd4d-101">Get-AzApplicationInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="8dd4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8dd4d-102">SYNOPSIS</span></span>
<span data-ttu-id="8dd4d-103">Verknüpftes Speicherkonto für Anwendungseinblicke</span><span class="sxs-lookup"><span data-stu-id="8dd4d-103">Get application insights linked storage account</span></span>

## <span data-ttu-id="8dd4d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8dd4d-104">SYNTAX</span></span>

### <span data-ttu-id="8dd4d-105">ByResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="8dd4d-105">ByResourceNameParameterSet (Default)</span></span>
```
Get-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName <String> -ComponentName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8dd4d-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8dd4d-106">ByInputObjectParameterSet</span></span>
```
Get-AzApplicationInsightsLinkedStorageAccount -InputObject <PSApplicationInsightsComponent>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8dd4d-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8dd4d-107">ByResourceIdParameterSet</span></span>
```
Get-AzApplicationInsightsLinkedStorageAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8dd4d-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8dd4d-108">DESCRIPTION</span></span>
<span data-ttu-id="8dd4d-109">Verknüpftes Speicherkonto für Anwendungseinblicke</span><span class="sxs-lookup"><span data-stu-id="8dd4d-109">Get application insights linked storage account</span></span>

## <span data-ttu-id="8dd4d-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8dd4d-110">EXAMPLES</span></span>

### <span data-ttu-id="8dd4d-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8dd4d-111">Example 1</span></span>
```powershell
Get-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName "rgName" -Name "componentName"
```

<span data-ttu-id="8dd4d-112">Verknüpftes Speicherkonto erhalten, das der Komponente "componentName" zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="8dd4d-112">Get linked storage account associated with component "componentName"</span></span>

## <span data-ttu-id="8dd4d-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="8dd4d-113">PARAMETERS</span></span>

### <span data-ttu-id="8dd4d-114">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="8dd4d-114">-ComponentName</span></span>
<span data-ttu-id="8dd4d-115">Komponentenname</span><span class="sxs-lookup"><span data-stu-id="8dd4d-115">Component Name</span></span>

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

### <span data-ttu-id="8dd4d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dd4d-116">-DefaultProfile</span></span>
<span data-ttu-id="8dd4d-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8dd4d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8dd4d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8dd4d-118">-InputObject</span></span>
<span data-ttu-id="8dd4d-119">PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="8dd4d-119">PSApplicationInsightsComponent</span></span>

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

### <span data-ttu-id="8dd4d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8dd4d-120">-ResourceGroupName</span></span>
<span data-ttu-id="8dd4d-121">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="8dd4d-121">Resource Group Name</span></span>

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

### <span data-ttu-id="8dd4d-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8dd4d-122">-ResourceId</span></span>
<span data-ttu-id="8dd4d-123">Component ResourceId</span><span class="sxs-lookup"><span data-stu-id="8dd4d-123">Component ResourceId</span></span>

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

### <span data-ttu-id="8dd4d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dd4d-124">CommonParameters</span></span>
<span data-ttu-id="8dd4d-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8dd4d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dd4d-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8dd4d-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dd4d-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8dd4d-127">INPUTS</span></span>

### <span data-ttu-id="8dd4d-128">System.String</span><span class="sxs-lookup"><span data-stu-id="8dd4d-128">System.String</span></span>

### <span data-ttu-id="8dd4d-129">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="8dd4d-129">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="8dd4d-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8dd4d-130">OUTPUTS</span></span>

### <span data-ttu-id="8dd4d-131">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="8dd4d-131">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span></span>

## <span data-ttu-id="8dd4d-132">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="8dd4d-132">NOTES</span></span>

## <span data-ttu-id="8dd4d-133">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="8dd4d-133">RELATED LINKS</span></span>
