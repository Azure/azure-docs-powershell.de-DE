---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountUsage.md
ms.openlocfilehash: 7d197cdb7ee8fbfa63d8a3b36da5f038a5a0b8de
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93652242"
---
# <span data-ttu-id="81623-101">Get-AzCognitiveServicesAccountUsage</span><span class="sxs-lookup"><span data-stu-id="81623-101">Get-AzCognitiveServicesAccountUsage</span></span>

## <span data-ttu-id="81623-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="81623-102">SYNOPSIS</span></span>
<span data-ttu-id="81623-103">Abrufen der aktuellen Verwendungen für ein Cognitive Services-Konto</span><span class="sxs-lookup"><span data-stu-id="81623-103">Get current usages for a Cognitive Services account.</span></span>

## <span data-ttu-id="81623-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="81623-104">SYNTAX</span></span>

### <span data-ttu-id="81623-105">ResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="81623-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzCognitiveServicesAccountUsage [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="81623-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="81623-106">InputObjectParameterSet</span></span>
```
Get-AzCognitiveServicesAccountUsage [-InputObject] <PSCognitiveServicesAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="81623-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="81623-107">ResourceIdParameterSet</span></span>
```
Get-AzCognitiveServicesAccountUsage [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="81623-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="81623-108">DESCRIPTION</span></span>
<span data-ttu-id="81623-109">Das Cmdlet " **Get-AzCognitiveServicesAccountUsage** " Ruft aktuelle Verwendungen für ein Cognitive Services-Konto ab.</span><span class="sxs-lookup"><span data-stu-id="81623-109">The **Get-AzCognitiveServicesAccountUsage** cmdlet gets current usages for a Cognitive Services account.</span></span>

## <span data-ttu-id="81623-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="81623-110">EXAMPLES</span></span>

### <span data-ttu-id="81623-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="81623-111">Example 1</span></span>
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

### <span data-ttu-id="81623-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="81623-112">Example 2</span></span>
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

### <span data-ttu-id="81623-113">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="81623-113">Example 3</span></span>
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

## <span data-ttu-id="81623-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="81623-114">PARAMETERS</span></span>

### <span data-ttu-id="81623-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81623-115">-DefaultProfile</span></span>
<span data-ttu-id="81623-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="81623-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81623-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="81623-117">-InputObject</span></span>
<span data-ttu-id="81623-118">Cognitive Services-Kontoobjekt.</span><span class="sxs-lookup"><span data-stu-id="81623-118">Cognitive Services Account Object.</span></span>

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

### <span data-ttu-id="81623-119">-Name</span><span class="sxs-lookup"><span data-stu-id="81623-119">-Name</span></span>
<span data-ttu-id="81623-120">Name des Cognitive Services-Kontos.</span><span class="sxs-lookup"><span data-stu-id="81623-120">Cognitive Services Account Name.</span></span>

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

### <span data-ttu-id="81623-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81623-121">-ResourceGroupName</span></span>
<span data-ttu-id="81623-122">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="81623-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="81623-123">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="81623-123">-ResourceId</span></span>
<span data-ttu-id="81623-124">Ressourcen-ID des Cognitive Services-Kontos.</span><span class="sxs-lookup"><span data-stu-id="81623-124">Cognitive Services Account Resource ID.</span></span>

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

### <span data-ttu-id="81623-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81623-125">CommonParameters</span></span>
<span data-ttu-id="81623-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81623-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81623-127">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="81623-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81623-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="81623-128">INPUTS</span></span>

### <span data-ttu-id="81623-129">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="81623-129">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

### <span data-ttu-id="81623-130">System. String</span><span class="sxs-lookup"><span data-stu-id="81623-130">System.String</span></span>

## <span data-ttu-id="81623-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="81623-131">OUTPUTS</span></span>

### <span data-ttu-id="81623-132">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSCognitiveServicesUsage</span><span class="sxs-lookup"><span data-stu-id="81623-132">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesUsage</span></span>

## <span data-ttu-id="81623-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="81623-133">NOTES</span></span>

## <span data-ttu-id="81623-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="81623-134">RELATED LINKS</span></span>
