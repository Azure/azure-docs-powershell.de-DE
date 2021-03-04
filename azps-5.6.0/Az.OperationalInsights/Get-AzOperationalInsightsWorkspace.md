---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: F94415DA-1A4A-4D37-A626-1EDF5D1EFE74
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 4082e7fc36228953ea33f8f3252bab642ca50e2c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943966"
---
# <span data-ttu-id="c6f70-101">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="c6f70-101">Get-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="c6f70-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6f70-102">SYNOPSIS</span></span>
<span data-ttu-id="c6f70-103">Ruft Informationen zu einem Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="c6f70-103">Gets information about a workspace.</span></span>

## <span data-ttu-id="c6f70-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c6f70-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6f70-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c6f70-105">DESCRIPTION</span></span>
<span data-ttu-id="c6f70-106">Das **Get-AzOperationalInsightsWorkspace-Cmdlet** ruft Informationen zu einem vorhandenen Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="c6f70-106">The **Get-AzOperationalInsightsWorkspace** cmdlet gets information about an existing workspace.</span></span>
<span data-ttu-id="c6f70-107">Wenn Sie einen Arbeitsbereichsnamen angeben, ruft dieses Cmdlet Informationen zu diesem Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="c6f70-107">If you specify a workspace name, this cmdlet gets information about that workspace.</span></span>
<span data-ttu-id="c6f70-108">Wenn Sie keinen Namen angeben, ruft dieses Cmdlet Informationen zu allen Arbeitsbereichen in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="c6f70-108">If you do not specify a name, this cmdlet gets information about all workspaces in a resource group.</span></span>
<span data-ttu-id="c6f70-109">Wenn Sie keinen Namen und keine Ressourcengruppe angeben, ruft dieses Cmdlet Informationen zu allen Arbeitsbereichen in einem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="c6f70-109">If you do not specify a name and resource group, this cmdlet gets information about all workspaces in a subscription.</span></span>

## <span data-ttu-id="c6f70-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c6f70-110">EXAMPLES</span></span>

### <span data-ttu-id="c6f70-111">Beispiel 1: Benennen eines Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="c6f70-111">Example 1: Get a workspace by name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -Name "MyWorkspace" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="c6f70-112">Dieser Befehl ruft einen Arbeitsbereich mit dem Namen "MyWorkspace" in der Ressourcengruppe "ContosoResourceGroup" ab.</span><span class="sxs-lookup"><span data-stu-id="c6f70-112">This command gets a workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="c6f70-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c6f70-113">PARAMETERS</span></span>

### <span data-ttu-id="c6f70-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6f70-114">-DefaultProfile</span></span>
<span data-ttu-id="c6f70-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="c6f70-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c6f70-116">-Name</span><span class="sxs-lookup"><span data-stu-id="c6f70-116">-Name</span></span>
<span data-ttu-id="c6f70-117">Gibt den Namen des Arbeitsbereichs an.</span><span class="sxs-lookup"><span data-stu-id="c6f70-117">Specifies the workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6f70-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6f70-118">-ResourceGroupName</span></span>
<span data-ttu-id="c6f70-119">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="c6f70-119">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6f70-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6f70-120">CommonParameters</span></span>
<span data-ttu-id="c6f70-121">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6f70-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6f70-122">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6f70-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6f70-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c6f70-123">INPUTS</span></span>

### <span data-ttu-id="c6f70-124">System.String</span><span class="sxs-lookup"><span data-stu-id="c6f70-124">System.String</span></span>

## <span data-ttu-id="c6f70-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c6f70-125">OUTPUTS</span></span>

### <span data-ttu-id="c6f70-126">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="c6f70-126">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="c6f70-127">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c6f70-127">NOTES</span></span>

## <span data-ttu-id="c6f70-128">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c6f70-128">RELATED LINKS</span></span>

[<span data-ttu-id="c6f70-129">Azure Operational Insights-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="c6f70-129">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


