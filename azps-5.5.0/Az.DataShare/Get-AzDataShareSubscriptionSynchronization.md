---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesubscriptionsynchronization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronization.md
ms.openlocfilehash: f1527cfcb947f802cb4a2710ab2f25a1d7b9bf75
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100163772"
---
# <span data-ttu-id="b07e9-101">Get-AzDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="b07e9-101">Get-AzDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="b07e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b07e9-102">SYNOPSIS</span></span>
<span data-ttu-id="b07e9-103">Ruft Informationen über Synchronisierungsläufe in einem Freigabeabonnement ab.</span><span class="sxs-lookup"><span data-stu-id="b07e9-103">Gets information about synchronization runs in share subscription.</span></span>

## <span data-ttu-id="b07e9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b07e9-104">SYNTAX</span></span>

### <span data-ttu-id="b07e9-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b07e9-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSubscriptionSynchronization -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b07e9-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b07e9-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSubscriptionSynchronization -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b07e9-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b07e9-107">DESCRIPTION</span></span>
<span data-ttu-id="b07e9-108">Das **Cmdlet "Get-AzDataShareSubscriptionSynchronization"** informiert Sie über alle Synchronisierungsläufe in einem Freigabeabonnement unter einem Datenfreigabekonto für Endverbraucher.</span><span class="sxs-lookup"><span data-stu-id="b07e9-108">The **Get-AzDataShareSubscriptionSynchronization** cmdlet provides informaiton about all synchronization runs in a share subscription under a data share account on the consumer.</span></span>

## <span data-ttu-id="b07e9-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b07e9-109">EXAMPLES</span></span>

### <span data-ttu-id="b07e9-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b07e9-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSubscriptionSynchronization -ResourceGroupName "ADS" -AccountName "WikiAds"  -ShareSubscriptionName "AdsShareSubscription"

durationMs        : 83660
endTime           : 7/10/2019 9:01:23 AM
message           :
startTime         : 7/10/2019 9:00:04 AM
status            : Succeeded
synchronizationId : b087e1a5-9144-4e1d-86d1-2a4adcf551d4
```

<span data-ttu-id="b07e9-111">Dieser Befehl enthält Informationen zu allen Synchronisierungsläufen für ein AdsShareSubscription-Freigabeabonnement unter "WikiAds" des Datenfreigabekontos.</span><span class="sxs-lookup"><span data-stu-id="b07e9-111">This command provides information about all the synchronization runs for a share subscription AdsShareSubscription under data share account WikiAds.</span></span>

## <span data-ttu-id="b07e9-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b07e9-112">PARAMETERS</span></span>

### <span data-ttu-id="b07e9-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b07e9-113">-AccountName</span></span>
<span data-ttu-id="b07e9-114">Name des Azure-Datenfreigabekontos</span><span class="sxs-lookup"><span data-stu-id="b07e9-114">Azure data share account name</span></span>

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

### <span data-ttu-id="b07e9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b07e9-115">-DefaultProfile</span></span>
<span data-ttu-id="b07e9-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b07e9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b07e9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b07e9-117">-ResourceGroupName</span></span>
<span data-ttu-id="b07e9-118">Der Ressourcengruppenname des Azure Data Share-Kontos</span><span class="sxs-lookup"><span data-stu-id="b07e9-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="b07e9-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b07e9-119">-ResourceId</span></span>
<span data-ttu-id="b07e9-120">Ressourcen-ID des Azure-Datenfreigabeabonnements</span><span class="sxs-lookup"><span data-stu-id="b07e9-120">Azure data share subscription resource id</span></span>

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

### <span data-ttu-id="b07e9-121">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="b07e9-121">-ShareSubscriptionName</span></span>
<span data-ttu-id="b07e9-122">Name des Azure Data Share-Abonnements</span><span class="sxs-lookup"><span data-stu-id="b07e9-122">Azure data share subscription name</span></span>

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

### <span data-ttu-id="b07e9-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b07e9-123">CommonParameters</span></span>
<span data-ttu-id="b07e9-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b07e9-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b07e9-125">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b07e9-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b07e9-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b07e9-126">INPUTS</span></span>

### <span data-ttu-id="b07e9-127">System.String</span><span class="sxs-lookup"><span data-stu-id="b07e9-127">System.String</span></span>

## <span data-ttu-id="b07e9-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b07e9-128">OUTPUTS</span></span>

### <span data-ttu-id="b07e9-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="b07e9-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="b07e9-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b07e9-130">NOTES</span></span>

## <span data-ttu-id="b07e9-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b07e9-131">RELATED LINKS</span></span>
