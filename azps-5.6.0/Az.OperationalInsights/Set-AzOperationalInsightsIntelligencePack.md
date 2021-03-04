---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 23ED4D24-66BD-46E9-BB57-6E0DA679B733
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/set-azoperationalinsightsintelligencepack
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsIntelligencePack.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsIntelligencePack.md
ms.openlocfilehash: ee65492adc8c2756a2d19871e4c673668d471c84
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937867"
---
# <span data-ttu-id="123a0-101">Set-AzOperationalInsightsIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="123a0-101">Set-AzOperationalInsightsIntelligencePack</span></span>

## <span data-ttu-id="123a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="123a0-102">SYNOPSIS</span></span>
<span data-ttu-id="123a0-103">Aktiviert oder deaktiviert das angegebene Intelligence Pack.</span><span class="sxs-lookup"><span data-stu-id="123a0-103">Enables or disables the specified Intelligence Pack.</span></span>

## <span data-ttu-id="123a0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="123a0-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsIntelligencePack [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-IntelligencePackName] <String> [-Enabled] <Boolean> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="123a0-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="123a0-105">DESCRIPTION</span></span>
<span data-ttu-id="123a0-106">Das **Cmdlet Set-AzOperationalInsightsIntelligencePack** aktiviert das  angegebene Intelligence Pack, wenn Enabled  auf $True festgelegt ist, und deaktiviert es, wenn Enabled auf $False.</span><span class="sxs-lookup"><span data-stu-id="123a0-106">The **Set-AzOperationalInsightsIntelligencePack** cmdlet enables the specified Intelligence Pack if *Enabled* is set to $True and disables it if *Enabled* is set to $False.</span></span>

## <span data-ttu-id="123a0-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="123a0-107">EXAMPLES</span></span>

### <span data-ttu-id="123a0-108">Beispiel 1: Festlegen von Intelligence Packs</span><span class="sxs-lookup"><span data-stu-id="123a0-108">Example 1: Set Intelligence Packs</span></span>
```
PS C:\>Set-AzOperationalInsightsIntelligencePack -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -IntelligencePackName "ContosoWorkspace" -Enabled $True
```

<span data-ttu-id="123a0-109">Mit diesem Befehl wird das angegebene Intelligence Pack aktiviert.</span><span class="sxs-lookup"><span data-stu-id="123a0-109">This command enables the specified Intelligence Pack.</span></span>

## <span data-ttu-id="123a0-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="123a0-110">PARAMETERS</span></span>

### <span data-ttu-id="123a0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="123a0-111">-DefaultProfile</span></span>
<span data-ttu-id="123a0-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="123a0-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="123a0-113">-Enabled</span><span class="sxs-lookup"><span data-stu-id="123a0-113">-Enabled</span></span>
```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="123a0-114">-IntelligencePackName</span><span class="sxs-lookup"><span data-stu-id="123a0-114">-IntelligencePackName</span></span>
<span data-ttu-id="123a0-115">Gibt den Namen des Intelligence Pack an.</span><span class="sxs-lookup"><span data-stu-id="123a0-115">Specifies the Intelligence Pack name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="123a0-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="123a0-116">-ResourceGroupName</span></span>
<span data-ttu-id="123a0-117">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="123a0-117">Specifies the resource group name</span></span>

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

### <span data-ttu-id="123a0-118">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="123a0-118">-WorkspaceName</span></span>
<span data-ttu-id="123a0-119">Gibt den Namen des Arbeitsbereichs an.</span><span class="sxs-lookup"><span data-stu-id="123a0-119">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="123a0-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="123a0-120">CommonParameters</span></span>
<span data-ttu-id="123a0-121">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="123a0-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="123a0-122">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="123a0-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="123a0-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="123a0-123">INPUTS</span></span>

### <span data-ttu-id="123a0-124">System.String</span><span class="sxs-lookup"><span data-stu-id="123a0-124">System.String</span></span>

### <span data-ttu-id="123a0-125">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="123a0-125">System.Boolean</span></span>

## <span data-ttu-id="123a0-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="123a0-126">OUTPUTS</span></span>

### <span data-ttu-id="123a0-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="123a0-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack</span></span>

## <span data-ttu-id="123a0-128">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="123a0-128">NOTES</span></span>

## <span data-ttu-id="123a0-129">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="123a0-129">RELATED LINKS</span></span>

[<span data-ttu-id="123a0-130">Azure Operational Insights-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="123a0-130">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


