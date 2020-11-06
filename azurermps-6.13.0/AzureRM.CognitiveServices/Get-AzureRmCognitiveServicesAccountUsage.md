---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/get-azurermcognitiveservicesaccountusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountUsage.md
ms.openlocfilehash: 1cdfaa6b57a0bcf6d50e0e3a77f80c1a5c069069
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477909"
---
# <span data-ttu-id="d1adf-101">Get-AzureRmCognitiveServicesAccountUsage</span><span class="sxs-lookup"><span data-stu-id="d1adf-101">Get-AzureRmCognitiveServicesAccountUsage</span></span>

## <span data-ttu-id="d1adf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d1adf-102">SYNOPSIS</span></span>
<span data-ttu-id="d1adf-103">Abrufen der aktuellen Verwendungen für ein Cognitive Services-Konto</span><span class="sxs-lookup"><span data-stu-id="d1adf-103">Get current usages for a Cognitive Services account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d1adf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d1adf-104">SYNTAX</span></span>

### <span data-ttu-id="d1adf-105">ResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d1adf-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzureRmCognitiveServicesAccountUsage [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1adf-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1adf-106">InputObjectParameterSet</span></span>
```
Get-AzureRmCognitiveServicesAccountUsage [-InputObject] <PSCognitiveServicesAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1adf-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1adf-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmCognitiveServicesAccountUsage [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d1adf-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d1adf-108">DESCRIPTION</span></span>
<span data-ttu-id="d1adf-109">Das Cmdlet " **Get-AzureRmCognitiveServicesAccountUsage** " Ruft aktuelle Verwendungen für ein Cognitive Services-Konto ab.</span><span class="sxs-lookup"><span data-stu-id="d1adf-109">The **Get-AzureRmCognitiveServicesAccountUsage** cmdlet gets current usages for a Cognitive Services account.</span></span>

## <span data-ttu-id="d1adf-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d1adf-110">EXAMPLES</span></span>

### <span data-ttu-id="d1adf-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d1adf-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmCognitiveServicesAccountUsage -ResourceGroupName TestUsages -Name TestCVUsages_Prediction

CurrentValue  : 0
Name          : CustomVision.Prediction.Transactions
Limit         : 10000
Status        : Included
Unit          : Count
QuotaPeriod   : 30.00:00:00
NextResetTime : 0001-01-01T00:00:00Z
```

### <span data-ttu-id="d1adf-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="d1adf-112">Example 2</span></span>
```powershell
PS C:\GitHub> $acc = Get-AzureRmCognitiveServicesAccount -ResourceGroupName TestUsages -Name TestCVUsages_Prediction

PS C:\GitHub> Get-AzureRmCognitiveServicesAccountUsage -InputObject $acc


CurrentValue  : 0
Name          : CustomVision.Prediction.Transactions
Limit         : 10000
Status        : Included
Unit          : Count
QuotaPeriod   : 30.00:00:00
NextResetTime : 0001-01-01T00:00:00Z
```

### <span data-ttu-id="d1adf-113">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="d1adf-113">Example 3</span></span>
```powershell
PS C:\GitHub> $acc = Get-AzureRmCognitiveServicesAccount -ResourceGroupName TestUsages -Name TestCVUsages_Prediction

PS C:\GitHub> Get-AzureRmCognitiveServicesAccountUsage -ResourceId $acc.Id


CurrentValue  : 0
Name          : CustomVision.Prediction.Transactions
Limit         : 10000
Status        : Included
Unit          : Count
QuotaPeriod   : 30.00:00:00
NextResetTime : 0001-01-01T00:00:00Z
```

## <span data-ttu-id="d1adf-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="d1adf-114">PARAMETERS</span></span>

### <span data-ttu-id="d1adf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1adf-115">-DefaultProfile</span></span>
<span data-ttu-id="d1adf-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d1adf-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1adf-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d1adf-117">-InputObject</span></span>
<span data-ttu-id="d1adf-118">Cognitive Services-Kontoobjekt.</span><span class="sxs-lookup"><span data-stu-id="d1adf-118">Cognitive Services Account Object.</span></span>

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

### <span data-ttu-id="d1adf-119">-Name</span><span class="sxs-lookup"><span data-stu-id="d1adf-119">-Name</span></span>
<span data-ttu-id="d1adf-120">Name des Cognitive Services-Kontos.</span><span class="sxs-lookup"><span data-stu-id="d1adf-120">Cognitive Services Account Name.</span></span>

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

### <span data-ttu-id="d1adf-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1adf-121">-ResourceGroupName</span></span>
<span data-ttu-id="d1adf-122">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d1adf-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="d1adf-123">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="d1adf-123">-ResourceId</span></span>
<span data-ttu-id="d1adf-124">Ressourcen-ID des Cognitive Services-Kontos.</span><span class="sxs-lookup"><span data-stu-id="d1adf-124">Cognitive Services Account Resource ID.</span></span>

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

### <span data-ttu-id="d1adf-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1adf-125">CommonParameters</span></span>
<span data-ttu-id="d1adf-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1adf-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1adf-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1adf-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1adf-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d1adf-128">INPUTS</span></span>

### <span data-ttu-id="d1adf-129">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="d1adf-129">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>
<span data-ttu-id="d1adf-130">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d1adf-130">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="d1adf-131">System. String</span><span class="sxs-lookup"><span data-stu-id="d1adf-131">System.String</span></span>

## <span data-ttu-id="d1adf-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d1adf-132">OUTPUTS</span></span>

### <span data-ttu-id="d1adf-133">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSCognitiveServicesUsage</span><span class="sxs-lookup"><span data-stu-id="d1adf-133">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesUsage</span></span>

## <span data-ttu-id="d1adf-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="d1adf-134">NOTES</span></span>

## <span data-ttu-id="d1adf-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d1adf-135">RELATED LINKS</span></span>
