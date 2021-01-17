---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 0F9D72C1-2E42-4A67-9FDE-6344F5DE6C30
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsintelligencepack
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsIntelligencePack.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsIntelligencePack.md
ms.openlocfilehash: e197a5df0993ffbb97415bdc4e72ed9ea7603713
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98370277"
---
# <span data-ttu-id="272b0-101">Get-AzOperationalInsightsIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="272b0-101">Get-AzOperationalInsightsIntelligencePack</span></span>

## <span data-ttu-id="272b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="272b0-102">SYNOPSIS</span></span>
<span data-ttu-id="272b0-103">Ruft die verfügbaren Intelligence Packs ab.</span><span class="sxs-lookup"><span data-stu-id="272b0-103">Gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="272b0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="272b0-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsIntelligencePack [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="272b0-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="272b0-105">DESCRIPTION</span></span>
<span data-ttu-id="272b0-106">Das **Cmdlet "Get-AzOperationalInsightsIntelligencePack"** ruft die verfügbaren Intelligence Packs ab.</span><span class="sxs-lookup"><span data-stu-id="272b0-106">The **Get-AzOperationalInsightsIntelligencePack** cmdlet gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="272b0-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="272b0-107">EXAMPLES</span></span>

### <span data-ttu-id="272b0-108">Beispiel 1: Erhalten von Intelligence Packs</span><span class="sxs-lookup"><span data-stu-id="272b0-108">Example 1: Get Intelligence Packs</span></span>
```
PS C:\>Get-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="272b0-109">Dieser Befehl ruft die verfügbaren Intelligence Packs ab.</span><span class="sxs-lookup"><span data-stu-id="272b0-109">This command gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="272b0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="272b0-110">PARAMETERS</span></span>

### <span data-ttu-id="272b0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="272b0-111">-DefaultProfile</span></span>
<span data-ttu-id="272b0-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="272b0-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="272b0-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="272b0-113">-ResourceGroupName</span></span>
<span data-ttu-id="272b0-114">Gibt den Namen einer Azure-Ressourcengruppe an, die einen Arbeitsbereich enthält.</span><span class="sxs-lookup"><span data-stu-id="272b0-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="272b0-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="272b0-115">-WorkspaceName</span></span>
<span data-ttu-id="272b0-116">Gibt den Namen des Arbeitsbereichs an.</span><span class="sxs-lookup"><span data-stu-id="272b0-116">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="272b0-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="272b0-117">CommonParameters</span></span>
<span data-ttu-id="272b0-118">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="272b0-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="272b0-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="272b0-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="272b0-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="272b0-120">INPUTS</span></span>

### <span data-ttu-id="272b0-121">System.String</span><span class="sxs-lookup"><span data-stu-id="272b0-121">System.String</span></span>

## <span data-ttu-id="272b0-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="272b0-122">OUTPUTS</span></span>

### <span data-ttu-id="272b0-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="272b0-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack</span></span>

## <span data-ttu-id="272b0-124">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="272b0-124">NOTES</span></span>

## <span data-ttu-id="272b0-125">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="272b0-125">RELATED LINKS</span></span>

[<span data-ttu-id="272b0-126">Azure Operational Insights-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="272b0-126">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


