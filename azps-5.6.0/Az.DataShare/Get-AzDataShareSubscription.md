---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/get-azdatasharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscription.md
ms.openlocfilehash: 4777b7becf1d0e08d88035253a314a21301bae04
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921256"
---
# <span data-ttu-id="b074b-101">Get-AzDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="b074b-101">Get-AzDataShareSubscription</span></span>

## <span data-ttu-id="b074b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b074b-102">SYNOPSIS</span></span>
<span data-ttu-id="b074b-103">Ruft Informationen zum Freigabeabonnement im Datenfreigabekonto ab.</span><span class="sxs-lookup"><span data-stu-id="b074b-103">Gets information about share subscription in data share account.</span></span>

## <span data-ttu-id="b074b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b074b-104">SYNTAX</span></span>

### <span data-ttu-id="b074b-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b074b-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSubscription -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b074b-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b074b-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSubscription -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b074b-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b074b-107">DESCRIPTION</span></span>
<span data-ttu-id="b074b-108">Das **Get-AzDataShareSubscription-Cmdlet** enthält Informationen zum Teilen eines Abonnements in einem Datenfreigabekonto.</span><span class="sxs-lookup"><span data-stu-id="b074b-108">The **Get-AzDataShareSubscription** cmdlet provides information about share subscription in a data share account.</span></span> <span data-ttu-id="b074b-109">Wenn der Name des Freigabeabonnements angegeben wird, enthält das Cmdlet Informationen zum jeweiligen Freigabeabonnement.</span><span class="sxs-lookup"><span data-stu-id="b074b-109">If share subscription name is provided, the cmdlet gives information about the particular share subscription.</span></span> <span data-ttu-id="b074b-110">Andernfalls stellt das Cmdlet eine Liste der Freigabeabonnements im Datenfreigabekonto zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="b074b-110">Otherwise, the cmdlet provides a list of share subscriptions in the data share account.</span></span>

## <span data-ttu-id="b074b-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b074b-111">EXAMPLES</span></span>

### <span data-ttu-id="b074b-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b074b-112">Example 1</span></span>
```
PS C:\> Get-AzDataShareSubscription -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShareSubscription"

CreatedAt               : 7/9/2019 12:32:53 AM
CreatedBy               : adstest@microsoft.com
InvitationId            : 0c14f5b6-0e22-49ab-8043-d6edad51db13
ProvisioningState       : Succeeded
ShareName               : AdsShare
ShareSender             : adsprovider@microsoft.com
ShareSenderCompanyName  : ADS Test
ShareDescription        : Ads description
ShareTerms              : Ads terms of use
ShareSubscriptionStatus : Active
ShareKind               : CopyBased
Id                      : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shareSubscriptions/AdsShareSubscription
Name                    : AdsShareSubscription
Type                    : Microsoft.DataShare/ShareSubscriptions
```

<span data-ttu-id="b074b-113">Dieser Befehl enthält Informationen zum Teilen des Abonnements AdsShareSubscription im WikiAds des Datenfreigabekontos.</span><span class="sxs-lookup"><span data-stu-id="b074b-113">This command provides information about share subscription AdsShareSubscription in data share account WikiAds.</span></span>

## <span data-ttu-id="b074b-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b074b-114">PARAMETERS</span></span>

### <span data-ttu-id="b074b-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b074b-115">-AccountName</span></span>
<span data-ttu-id="b074b-116">Name des Azure-Datenfreigabekontos</span><span class="sxs-lookup"><span data-stu-id="b074b-116">Azure data share account name</span></span>

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

### <span data-ttu-id="b074b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b074b-117">-DefaultProfile</span></span>
<span data-ttu-id="b074b-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b074b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b074b-119">-Name</span><span class="sxs-lookup"><span data-stu-id="b074b-119">-Name</span></span>
<span data-ttu-id="b074b-120">Azure Data Share Subscription Name</span><span class="sxs-lookup"><span data-stu-id="b074b-120">Azure data share subscription name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b074b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b074b-121">-ResourceGroupName</span></span>
<span data-ttu-id="b074b-122">Der Ressourcengruppenname des Azure Data Share-Kontos</span><span class="sxs-lookup"><span data-stu-id="b074b-122">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="b074b-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b074b-123">-ResourceId</span></span>
<span data-ttu-id="b074b-124">Die Ressourcen-ID des Azure Data Share-Abonnements</span><span class="sxs-lookup"><span data-stu-id="b074b-124">The resource id of the azure data share subscription</span></span>

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

### <span data-ttu-id="b074b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b074b-125">CommonParameters</span></span>
<span data-ttu-id="b074b-126">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b074b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b074b-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b074b-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b074b-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b074b-128">INPUTS</span></span>

### <span data-ttu-id="b074b-129">System.String</span><span class="sxs-lookup"><span data-stu-id="b074b-129">System.String</span></span>

## <span data-ttu-id="b074b-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b074b-130">OUTPUTS</span></span>

### <span data-ttu-id="b074b-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="b074b-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span></span>

## <span data-ttu-id="b074b-132">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b074b-132">NOTES</span></span>

## <span data-ttu-id="b074b-133">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b074b-133">RELATED LINKS</span></span>
