---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 0F9D72C1-2E42-4A67-9FDE-6344F5DE6C30
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/get-azoperationalinsightsintelligencepack
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsIntelligencePack.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsIntelligencePack.md
ms.openlocfilehash: a56fd0303e6f610468c9f2784396023fd20edef4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925427"
---
# <span data-ttu-id="66540-101">Get-AzOperationalInsightsIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="66540-101">Get-AzOperationalInsightsIntelligencePack</span></span>

## <span data-ttu-id="66540-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66540-102">SYNOPSIS</span></span>
<span data-ttu-id="66540-103">Ruft die verfügbaren Intelligence Packs ab.</span><span class="sxs-lookup"><span data-stu-id="66540-103">Gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="66540-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="66540-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsIntelligencePack [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66540-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="66540-105">DESCRIPTION</span></span>
<span data-ttu-id="66540-106">Das **Cmdlet Get-AzOperationalInsightsIntelligencePack** ruft die verfügbaren Intelligence Packs ab.</span><span class="sxs-lookup"><span data-stu-id="66540-106">The **Get-AzOperationalInsightsIntelligencePack** cmdlet gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="66540-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="66540-107">EXAMPLES</span></span>

### <span data-ttu-id="66540-108">Beispiel 1: Erhalten von Intelligence Packs</span><span class="sxs-lookup"><span data-stu-id="66540-108">Example 1: Get Intelligence Packs</span></span>
```
PS C:\>Get-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="66540-109">Dieser Befehl ruft die verfügbaren Intelligence Packs ab.</span><span class="sxs-lookup"><span data-stu-id="66540-109">This command gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="66540-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="66540-110">PARAMETERS</span></span>

### <span data-ttu-id="66540-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66540-111">-DefaultProfile</span></span>
<span data-ttu-id="66540-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="66540-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="66540-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66540-113">-ResourceGroupName</span></span>
<span data-ttu-id="66540-114">Gibt den Namen einer Azure-Ressourcengruppe an, die einen Arbeitsbereich enthält.</span><span class="sxs-lookup"><span data-stu-id="66540-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66540-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="66540-115">-WorkspaceName</span></span>
<span data-ttu-id="66540-116">Gibt den Namen des Arbeitsbereichs an.</span><span class="sxs-lookup"><span data-stu-id="66540-116">Specifies the workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66540-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66540-117">CommonParameters</span></span>
<span data-ttu-id="66540-118">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66540-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66540-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66540-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66540-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="66540-120">INPUTS</span></span>

### <span data-ttu-id="66540-121">System.String</span><span class="sxs-lookup"><span data-stu-id="66540-121">System.String</span></span>

## <span data-ttu-id="66540-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="66540-122">OUTPUTS</span></span>

### <span data-ttu-id="66540-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="66540-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack</span></span>

## <span data-ttu-id="66540-124">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="66540-124">NOTES</span></span>

## <span data-ttu-id="66540-125">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="66540-125">RELATED LINKS</span></span>

[<span data-ttu-id="66540-126">Azure Operational Insights-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="66540-126">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


