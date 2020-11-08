---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountNetworkRuleSet.md
ms.openlocfilehash: 24b2cb6efca1213365c99a2c095f90e675c317c7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008361"
---
# <span data-ttu-id="5b57b-101">Get-AzCognitiveServicesAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="5b57b-101">Get-AzCognitiveServicesAccountNetworkRuleSet</span></span>

## <span data-ttu-id="5b57b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5b57b-102">SYNOPSIS</span></span>
<span data-ttu-id="5b57b-103">Abrufen der NetworkRule-Eigenschaft eines kognitiven Dienstkontos</span><span class="sxs-lookup"><span data-stu-id="5b57b-103">Get the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="5b57b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5b57b-104">SYNTAX</span></span>

```
Get-AzCognitiveServicesAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b57b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5b57b-105">DESCRIPTION</span></span>
<span data-ttu-id="5b57b-106">Das Cmdlet " **Get-AzCognitiveServicesAccountNetworkRuleSet** " Ruft die NetworkRule-Eigenschaft eines kognitiven Dienstkontos ab.</span><span class="sxs-lookup"><span data-stu-id="5b57b-106">The **Get-AzCognitiveServicesAccountNetworkRuleSet** cmdlet gets the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="5b57b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5b57b-107">EXAMPLES</span></span>

### <span data-ttu-id="5b57b-108">Beispiel 1: Abrufen der NetworkRule-Eigenschaft eines angegebenen Cognitive Services-Kontos</span><span class="sxs-lookup"><span data-stu-id="5b57b-108">Example 1: Get NetworkRule property of a specified Cognitive Services account</span></span>
```
PS C:\> Get-AzCognitiveServicesAccountNetworkRuleSet  -ResourceGroupName "rg1" -Name "myaccount"
```

<span data-ttu-id="5b57b-109">Dieser Befehl ruft die NetworkRule-Eigenschaft eines angegebenen Cognitive Services-Kontos ab.</span><span class="sxs-lookup"><span data-stu-id="5b57b-109">This command gets NetworkRule property of a specified Cognitive Services account</span></span>

## <span data-ttu-id="5b57b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="5b57b-110">PARAMETERS</span></span>

### <span data-ttu-id="5b57b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b57b-111">-DefaultProfile</span></span>
<span data-ttu-id="5b57b-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5b57b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b57b-113">-Name</span><span class="sxs-lookup"><span data-stu-id="5b57b-113">-Name</span></span>
<span data-ttu-id="5b57b-114">Name des Cognitive Services-Kontos.</span><span class="sxs-lookup"><span data-stu-id="5b57b-114">Cognitive Services Account Name.</span></span>

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

### <span data-ttu-id="5b57b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b57b-115">-ResourceGroupName</span></span>
<span data-ttu-id="5b57b-116">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5b57b-116">Resource Group Name.</span></span>

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

### <span data-ttu-id="5b57b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b57b-117">CommonParameters</span></span>
<span data-ttu-id="5b57b-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b57b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b57b-119">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5b57b-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b57b-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5b57b-120">INPUTS</span></span>

### <span data-ttu-id="5b57b-121">System. String</span><span class="sxs-lookup"><span data-stu-id="5b57b-121">System.String</span></span>

## <span data-ttu-id="5b57b-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5b57b-122">OUTPUTS</span></span>

### <span data-ttu-id="5b57b-123">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="5b57b-123">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="5b57b-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="5b57b-124">NOTES</span></span>

## <span data-ttu-id="5b57b-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5b57b-125">RELATED LINKS</span></span>
