---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/get-azapplicationinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsLinkedStorageAccount.md
ms.openlocfilehash: 7e879cd4e513ebdad297933269e373c625f2e407
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98306819"
---
# <span data-ttu-id="a2197-101">Get-AzApplicationInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a2197-101">Get-AzApplicationInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="a2197-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2197-102">SYNOPSIS</span></span>
<span data-ttu-id="a2197-103">Verknüpftes Speicherkonto mit Anwendungserkenntnissen</span><span class="sxs-lookup"><span data-stu-id="a2197-103">Get application insights linked storage account</span></span>

## <span data-ttu-id="a2197-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a2197-104">SYNTAX</span></span>

### <span data-ttu-id="a2197-105">ByResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a2197-105">ByResourceNameParameterSet (Default)</span></span>
```
Get-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName <String> -ComponentName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2197-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2197-106">ByInputObjectParameterSet</span></span>
```
Get-AzApplicationInsightsLinkedStorageAccount -InputObject <PSApplicationInsightsComponent>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2197-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2197-107">ByResourceIdParameterSet</span></span>
```
Get-AzApplicationInsightsLinkedStorageAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a2197-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a2197-108">DESCRIPTION</span></span>
<span data-ttu-id="a2197-109">Verknüpftes Speicherkonto mit Anwendungserkenntnissen</span><span class="sxs-lookup"><span data-stu-id="a2197-109">Get application insights linked storage account</span></span>

## <span data-ttu-id="a2197-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a2197-110">EXAMPLES</span></span>

### <span data-ttu-id="a2197-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a2197-111">Example 1</span></span>
```powershell
Get-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName "rgName" -Name "componentName"
```

<span data-ttu-id="a2197-112">Verknüpftes Speicherkonto erhalten, das der Komponente "componentName" zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="a2197-112">Get linked storage account associated with component "componentName"</span></span>

## <span data-ttu-id="a2197-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a2197-113">PARAMETERS</span></span>

### <span data-ttu-id="a2197-114">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="a2197-114">-ComponentName</span></span>
<span data-ttu-id="a2197-115">Komponentenname</span><span class="sxs-lookup"><span data-stu-id="a2197-115">Component Name</span></span>

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

### <span data-ttu-id="a2197-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2197-116">-DefaultProfile</span></span>
<span data-ttu-id="a2197-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a2197-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2197-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a2197-118">-InputObject</span></span>
<span data-ttu-id="a2197-119">PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="a2197-119">PSApplicationInsightsComponent</span></span>

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

### <span data-ttu-id="a2197-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2197-120">-ResourceGroupName</span></span>
<span data-ttu-id="a2197-121">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="a2197-121">Resource Group Name</span></span>

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

### <span data-ttu-id="a2197-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a2197-122">-ResourceId</span></span>
<span data-ttu-id="a2197-123">Component ResourceId</span><span class="sxs-lookup"><span data-stu-id="a2197-123">Component ResourceId</span></span>

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

### <span data-ttu-id="a2197-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2197-124">CommonParameters</span></span>
<span data-ttu-id="a2197-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2197-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2197-126">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a2197-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2197-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a2197-127">INPUTS</span></span>

### <span data-ttu-id="a2197-128">System.String</span><span class="sxs-lookup"><span data-stu-id="a2197-128">System.String</span></span>

### <span data-ttu-id="a2197-129">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="a2197-129">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="a2197-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a2197-130">OUTPUTS</span></span>

### <span data-ttu-id="a2197-131">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="a2197-131">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span></span>

## <span data-ttu-id="a2197-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a2197-132">NOTES</span></span>

## <span data-ttu-id="a2197-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a2197-133">RELATED LINKS</span></span>
