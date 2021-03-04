---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountNetworkRuleSet.md
ms.openlocfilehash: 60a61af31b5a7986779b19b893d4c02d0039ae49
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101946253"
---
# <span data-ttu-id="03fb7-101">Get-AzCognitiveServicesAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="03fb7-101">Get-AzCognitiveServicesAccountNetworkRuleSet</span></span>

## <span data-ttu-id="03fb7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03fb7-102">SYNOPSIS</span></span>
<span data-ttu-id="03fb7-103">Die NetworkRule-Eigenschaft eines Cognitive Services-Kontos</span><span class="sxs-lookup"><span data-stu-id="03fb7-103">Get the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="03fb7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="03fb7-104">SYNTAX</span></span>

```
Get-AzCognitiveServicesAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="03fb7-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="03fb7-105">DESCRIPTION</span></span>
<span data-ttu-id="03fb7-106">Das **Get-AzCognitiveServicesAccountNetworkRuleSet-Cmdlet** ruft die NetworkRule-Eigenschaft eines Cognitive Services-Kontos ab.</span><span class="sxs-lookup"><span data-stu-id="03fb7-106">The **Get-AzCognitiveServicesAccountNetworkRuleSet** cmdlet gets the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="03fb7-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="03fb7-107">EXAMPLES</span></span>

### <span data-ttu-id="03fb7-108">Beispiel 1: Get NetworkRule-Eigenschaft eines angegebenen Cognitive Services-Kontos</span><span class="sxs-lookup"><span data-stu-id="03fb7-108">Example 1: Get NetworkRule property of a specified Cognitive Services account</span></span>
```
PS C:\> Get-AzCognitiveServicesAccountNetworkRuleSet  -ResourceGroupName "rg1" -Name "myaccount"
```

<span data-ttu-id="03fb7-109">Dieser Befehl ruft die NetworkRule-Eigenschaft eines angegebenen Cognitive Services-Kontos ab.</span><span class="sxs-lookup"><span data-stu-id="03fb7-109">This command gets NetworkRule property of a specified Cognitive Services account</span></span>

## <span data-ttu-id="03fb7-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="03fb7-110">PARAMETERS</span></span>

### <span data-ttu-id="03fb7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03fb7-111">-DefaultProfile</span></span>
<span data-ttu-id="03fb7-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="03fb7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03fb7-113">-Name</span><span class="sxs-lookup"><span data-stu-id="03fb7-113">-Name</span></span>
<span data-ttu-id="03fb7-114">Name des Cognitive Services-Kontos.</span><span class="sxs-lookup"><span data-stu-id="03fb7-114">Cognitive Services Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03fb7-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03fb7-115">-ResourceGroupName</span></span>
<span data-ttu-id="03fb7-116">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="03fb7-116">Resource Group Name.</span></span>

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

### <span data-ttu-id="03fb7-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03fb7-117">CommonParameters</span></span>
<span data-ttu-id="03fb7-118">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03fb7-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03fb7-119">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="03fb7-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03fb7-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="03fb7-120">INPUTS</span></span>

### <span data-ttu-id="03fb7-121">System.String</span><span class="sxs-lookup"><span data-stu-id="03fb7-121">System.String</span></span>

## <span data-ttu-id="03fb7-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="03fb7-122">OUTPUTS</span></span>

### <span data-ttu-id="03fb7-123">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="03fb7-123">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="03fb7-124">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="03fb7-124">NOTES</span></span>

## <span data-ttu-id="03fb7-125">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="03fb7-125">RELATED LINKS</span></span>
