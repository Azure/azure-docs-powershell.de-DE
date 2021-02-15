---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountNetworkRuleSet.md
ms.openlocfilehash: 24b2cb6efca1213365c99a2c095f90e675c317c7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100171360"
---
# <span data-ttu-id="fbca6-101">Get-AzCognitiveServicesAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="fbca6-101">Get-AzCognitiveServicesAccountNetworkRuleSet</span></span>

## <span data-ttu-id="fbca6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fbca6-102">SYNOPSIS</span></span>
<span data-ttu-id="fbca6-103">Erhalten der Eigenschaft "NetworkRule" eines Cognitive Services-Kontos</span><span class="sxs-lookup"><span data-stu-id="fbca6-103">Get the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="fbca6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fbca6-104">SYNTAX</span></span>

```
Get-AzCognitiveServicesAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fbca6-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fbca6-105">DESCRIPTION</span></span>
<span data-ttu-id="fbca6-106">Das **Cmdlet "Get-AzCognitiveServicesAccountNetworkRuleSet"** ruft die "NetworkRule"-Eigenschaft eines Cognitive Services-Kontos ab.</span><span class="sxs-lookup"><span data-stu-id="fbca6-106">The **Get-AzCognitiveServicesAccountNetworkRuleSet** cmdlet gets the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="fbca6-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fbca6-107">EXAMPLES</span></span>

### <span data-ttu-id="fbca6-108">Beispiel 1: Erhalten der Eigenschaft "NetworkRule" eines angegebenen Cognitive Services-Kontos</span><span class="sxs-lookup"><span data-stu-id="fbca6-108">Example 1: Get NetworkRule property of a specified Cognitive Services account</span></span>
```
PS C:\> Get-AzCognitiveServicesAccountNetworkRuleSet  -ResourceGroupName "rg1" -Name "myaccount"
```

<span data-ttu-id="fbca6-109">Dieser Befehl ruft die Eigenschaft "NetworkRule" eines angegebenen Cognitive Services-Kontos ab.</span><span class="sxs-lookup"><span data-stu-id="fbca6-109">This command gets NetworkRule property of a specified Cognitive Services account</span></span>

## <span data-ttu-id="fbca6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fbca6-110">PARAMETERS</span></span>

### <span data-ttu-id="fbca6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbca6-111">-DefaultProfile</span></span>
<span data-ttu-id="fbca6-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fbca6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fbca6-113">-Name</span><span class="sxs-lookup"><span data-stu-id="fbca6-113">-Name</span></span>
<span data-ttu-id="fbca6-114">Name des Cognitive Services-Kontos.</span><span class="sxs-lookup"><span data-stu-id="fbca6-114">Cognitive Services Account Name.</span></span>

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

### <span data-ttu-id="fbca6-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbca6-115">-ResourceGroupName</span></span>
<span data-ttu-id="fbca6-116">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="fbca6-116">Resource Group Name.</span></span>

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

### <span data-ttu-id="fbca6-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbca6-117">CommonParameters</span></span>
<span data-ttu-id="fbca6-118">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbca6-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbca6-119">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fbca6-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbca6-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fbca6-120">INPUTS</span></span>

### <span data-ttu-id="fbca6-121">System.String</span><span class="sxs-lookup"><span data-stu-id="fbca6-121">System.String</span></span>

## <span data-ttu-id="fbca6-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fbca6-122">OUTPUTS</span></span>

### <span data-ttu-id="fbca6-123">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="fbca6-123">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="fbca6-124">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="fbca6-124">NOTES</span></span>

## <span data-ttu-id="fbca6-125">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="fbca6-125">RELATED LINKS</span></span>
