---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountUsage.md
ms.openlocfilehash: 2fc4e536ed3f97b1d0e31ccea382d4dc55d59083
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933219"
---
# <span data-ttu-id="0bebb-101">Get-AzCognitiveServicesAccountUsage</span><span class="sxs-lookup"><span data-stu-id="0bebb-101">Get-AzCognitiveServicesAccountUsage</span></span>

## <span data-ttu-id="0bebb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0bebb-102">SYNOPSIS</span></span>
<span data-ttu-id="0bebb-103">Holen Sie sich die aktuellen Nutzungen für ein Cognitive Services-Konto.</span><span class="sxs-lookup"><span data-stu-id="0bebb-103">Get current usages for a Cognitive Services account.</span></span>

## <span data-ttu-id="0bebb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0bebb-104">SYNTAX</span></span>

### <span data-ttu-id="0bebb-105">ResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="0bebb-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzCognitiveServicesAccountUsage [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0bebb-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0bebb-106">InputObjectParameterSet</span></span>
```
Get-AzCognitiveServicesAccountUsage [-InputObject] <PSCognitiveServicesAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0bebb-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0bebb-107">ResourceIdParameterSet</span></span>
```
Get-AzCognitiveServicesAccountUsage [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0bebb-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0bebb-108">DESCRIPTION</span></span>
<span data-ttu-id="0bebb-109">Das **Get-AzCognitiveServicesAccountUsage-Cmdlet** ruft aktuelle Verwendungen für ein Cognitive Services-Konto ab.</span><span class="sxs-lookup"><span data-stu-id="0bebb-109">The **Get-AzCognitiveServicesAccountUsage** cmdlet gets current usages for a Cognitive Services account.</span></span>

## <span data-ttu-id="0bebb-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0bebb-110">EXAMPLES</span></span>

### <span data-ttu-id="0bebb-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0bebb-111">Example 1</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountUsage -ResourceGroupName TestUsages -Name TestCVUsages_Prediction

CurrentValue  : 0
Name          : CustomVision.Prediction.Transactions
Limit         : 10000
Status        : Included
Unit          : Count
QuotaPeriod   : 30.00:00:00
NextResetTime : 0001-01-01T00:00:00Z
```

### <span data-ttu-id="0bebb-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="0bebb-112">Example 2</span></span>
```powershell
PS C:\GitHub> $acc = Get-AzCognitiveServicesAccount -ResourceGroupName TestUsages -Name TestCVUsages_Prediction

PS C:\GitHub> Get-AzCognitiveServicesAccountUsage -InputObject $acc


CurrentValue  : 0
Name          : CustomVision.Prediction.Transactions
Limit         : 10000
Status        : Included
Unit          : Count
QuotaPeriod   : 30.00:00:00
NextResetTime : 0001-01-01T00:00:00Z
```

### <span data-ttu-id="0bebb-113">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="0bebb-113">Example 3</span></span>
```powershell
PS C:\GitHub> $acc = Get-AzCognitiveServicesAccount -ResourceGroupName TestUsages -Name TestCVUsages_Prediction

PS C:\GitHub> Get-AzCognitiveServicesAccountUsage -ResourceId $acc.Id


CurrentValue  : 0
Name          : CustomVision.Prediction.Transactions
Limit         : 10000
Status        : Included
Unit          : Count
QuotaPeriod   : 30.00:00:00
NextResetTime : 0001-01-01T00:00:00Z
```

## <span data-ttu-id="0bebb-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="0bebb-114">PARAMETERS</span></span>

### <span data-ttu-id="0bebb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bebb-115">-DefaultProfile</span></span>
<span data-ttu-id="0bebb-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0bebb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0bebb-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0bebb-117">-InputObject</span></span>
<span data-ttu-id="0bebb-118">Cognitive Services Account Object.</span><span class="sxs-lookup"><span data-stu-id="0bebb-118">Cognitive Services Account Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0bebb-119">-Name</span><span class="sxs-lookup"><span data-stu-id="0bebb-119">-Name</span></span>
<span data-ttu-id="0bebb-120">Name des Cognitive Services-Kontos.</span><span class="sxs-lookup"><span data-stu-id="0bebb-120">Cognitive Services Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bebb-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0bebb-121">-ResourceGroupName</span></span>
<span data-ttu-id="0bebb-122">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="0bebb-122">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bebb-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0bebb-123">-ResourceId</span></span>
<span data-ttu-id="0bebb-124">Cognitive Services Account Resource ID.</span><span class="sxs-lookup"><span data-stu-id="0bebb-124">Cognitive Services Account Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0bebb-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bebb-125">CommonParameters</span></span>
<span data-ttu-id="0bebb-126">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0bebb-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bebb-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0bebb-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bebb-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0bebb-128">INPUTS</span></span>

### <span data-ttu-id="0bebb-129">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="0bebb-129">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

### <span data-ttu-id="0bebb-130">System.String</span><span class="sxs-lookup"><span data-stu-id="0bebb-130">System.String</span></span>

## <span data-ttu-id="0bebb-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0bebb-131">OUTPUTS</span></span>

### <span data-ttu-id="0bebb-132">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesUsage</span><span class="sxs-lookup"><span data-stu-id="0bebb-132">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesUsage</span></span>

## <span data-ttu-id="0bebb-133">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="0bebb-133">NOTES</span></span>

## <span data-ttu-id="0bebb-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="0bebb-134">RELATED LINKS</span></span>
