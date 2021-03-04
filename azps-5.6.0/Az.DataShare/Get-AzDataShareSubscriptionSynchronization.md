---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/get-azdatasharesubscriptionsynchronization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronization.md
ms.openlocfilehash: 8a80277508f9cd2998668185af6a8c0b5bbec128
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923755"
---
# <span data-ttu-id="677a2-101">Get-AzDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="677a2-101">Get-AzDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="677a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="677a2-102">SYNOPSIS</span></span>
<span data-ttu-id="677a2-103">Ruft Informationen zur Synchronisierung ab, die im Freigabeabonnement ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="677a2-103">Gets information about synchronization runs in share subscription.</span></span>

## <span data-ttu-id="677a2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="677a2-104">SYNTAX</span></span>

### <span data-ttu-id="677a2-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="677a2-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSubscriptionSynchronization -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="677a2-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="677a2-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSubscriptionSynchronization -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="677a2-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="677a2-107">DESCRIPTION</span></span>
<span data-ttu-id="677a2-108">Das **Get-AzDataShareSubscriptionSynchronization-Cmdlet** bietet Informationen zu allen Synchronisierungsläufen in einem Freigabeabonnement unter einem Datenfreigabekonto für den Verbraucher.</span><span class="sxs-lookup"><span data-stu-id="677a2-108">The **Get-AzDataShareSubscriptionSynchronization** cmdlet provides informaiton about all synchronization runs in a share subscription under a data share account on the consumer.</span></span>

## <span data-ttu-id="677a2-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="677a2-109">EXAMPLES</span></span>

### <span data-ttu-id="677a2-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="677a2-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSubscriptionSynchronization -ResourceGroupName "ADS" -AccountName "WikiAds"  -ShareSubscriptionName "AdsShareSubscription"

durationMs        : 83660
endTime           : 7/10/2019 9:01:23 AM
message           :
startTime         : 7/10/2019 9:00:04 AM
status            : Succeeded
synchronizationId : b087e1a5-9144-4e1d-86d1-2a4adcf551d4
```

<span data-ttu-id="677a2-111">Dieser Befehl enthält Informationen zu allen Synchronisierungsläufen für ein Freigabeabonnement AdsShareSubscription unter WikiAds des Datenfreigabekontos.</span><span class="sxs-lookup"><span data-stu-id="677a2-111">This command provides information about all the synchronization runs for a share subscription AdsShareSubscription under data share account WikiAds.</span></span>

## <span data-ttu-id="677a2-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="677a2-112">PARAMETERS</span></span>

### <span data-ttu-id="677a2-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="677a2-113">-AccountName</span></span>
<span data-ttu-id="677a2-114">Name des Azure-Datenfreigabekontos</span><span class="sxs-lookup"><span data-stu-id="677a2-114">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="677a2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="677a2-115">-DefaultProfile</span></span>
<span data-ttu-id="677a2-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="677a2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="677a2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="677a2-117">-ResourceGroupName</span></span>
<span data-ttu-id="677a2-118">Der Ressourcengruppenname des Azure Data Share-Kontos</span><span class="sxs-lookup"><span data-stu-id="677a2-118">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="677a2-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="677a2-119">-ResourceId</span></span>
<span data-ttu-id="677a2-120">Azure Data Share Subscription Resource ID</span><span class="sxs-lookup"><span data-stu-id="677a2-120">Azure data share subscription resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="677a2-121">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="677a2-121">-ShareSubscriptionName</span></span>
<span data-ttu-id="677a2-122">Azure Data Share Subscription Name</span><span class="sxs-lookup"><span data-stu-id="677a2-122">Azure data share subscription name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="677a2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="677a2-123">CommonParameters</span></span>
<span data-ttu-id="677a2-124">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="677a2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="677a2-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="677a2-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="677a2-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="677a2-126">INPUTS</span></span>

### <span data-ttu-id="677a2-127">System.String</span><span class="sxs-lookup"><span data-stu-id="677a2-127">System.String</span></span>

## <span data-ttu-id="677a2-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="677a2-128">OUTPUTS</span></span>

### <span data-ttu-id="677a2-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="677a2-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="677a2-130">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="677a2-130">NOTES</span></span>

## <span data-ttu-id="677a2-131">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="677a2-131">RELATED LINKS</span></span>
