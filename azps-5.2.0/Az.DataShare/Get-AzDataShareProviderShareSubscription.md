---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatashareprovidersharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareProviderShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareProviderShareSubscription.md
ms.openlocfilehash: 5422b43019b7b667ba7ea787663e91e2b6beb118
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357662"
---
# <span data-ttu-id="93167-101">Get-AzDataShareProviderShareSubscription</span><span class="sxs-lookup"><span data-stu-id="93167-101">Get-AzDataShareProviderShareSubscription</span></span>

## <span data-ttu-id="93167-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93167-102">SYNOPSIS</span></span>
<span data-ttu-id="93167-103">Ruft auf Anbieterseite Informationen zu Abonnements für Endverbraucherfreigaben ab.</span><span class="sxs-lookup"><span data-stu-id="93167-103">Gets information about consumer share subscriptions on provider side.</span></span>

## <span data-ttu-id="93167-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="93167-104">SYNTAX</span></span>

### <span data-ttu-id="93167-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="93167-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareProviderShareSubscription -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 [-ShareSubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="93167-106">ByProviderShareSubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="93167-106">ByProviderShareSubscriptionIdParameterSet</span></span>
```
Get-AzDataShareProviderShareSubscription [-ShareSubscriptionId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93167-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="93167-107">DESCRIPTION</span></span>
<span data-ttu-id="93167-108">Das **Cmdlet "Get-AzDataShareProviderSubscription"** ruft auf Anbieterseite Informationen zu Consumer-Share-Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="93167-108">The **Get-AzDataShareProviderSubscription** cmdlet gets information about consumer share subscriptions on provider side.</span></span> <span data-ttu-id="93167-109">Wenn Sie die Untergeordnete Freigabe-ID angeben, ruft dieses Cmdlet Informationen über das Freigabeabonnement ab.</span><span class="sxs-lookup"><span data-stu-id="93167-109">If you specify the share subscrption id, this cmdlet gets information about the share subscription.</span></span> <span data-ttu-id="93167-110">Wenn Sie die ID für das Freigabeabonnement nicht angeben, ruft dieses Cmdlet Informationen zu allen Abonnements für Endverbraucherfreigaben ab, die der Freigabe zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="93167-110">If you do not specify the share subscription id, this cmdlet gets information about all the consumer share subscriptions in associated with the share.</span></span>

## <span data-ttu-id="93167-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="93167-111">EXAMPLES</span></span>

### <span data-ttu-id="93167-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="93167-112">Example 1</span></span>
```
PS C:\> Get-AzDataShareProviderShareSubscription -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -ShareSubscriptionId "/subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shares/AdsShare/shareSubscriptions/505c3500-b2ff-46ab-96bf-50f5ec89d75a"

Company                   : ADS Test
CreatedAt                 : 6/30/2019 12:42:12 AM
CreatedBy                 : adstest@microsoft.com
SharedAt                  : 6/30/2019 12:41:37 AM
SharedBy                  : adsprovider@microsoft.com
ShareSubscriptionObjectId : 505c3500-b2ff-46ab-96bf-50f5ec89d75a
ShareSubscriptionStatus   : Active
Id                        : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shares/AdsShare/shareSubscriptions/505c3500-b2ff-46ab-96bf-50f5ec89d75a
Name                      : AdsShareSubscription
Type                      : Microsoft.DataShare/ShareSubscriptions
```

<span data-ttu-id="93167-113">Diese Befehle enthalten Informationen über das Abonnement für die Freigabe von Endverbrauchern, das der Freigabe von AdsShare im WikiAds des Datenfreigabekontos zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="93167-113">This commands provides information about consumer share subscription associated with share AdsShare in data share account WikiAds.</span></span>

## <span data-ttu-id="93167-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="93167-114">PARAMETERS</span></span>

### <span data-ttu-id="93167-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="93167-115">-AccountName</span></span>
<span data-ttu-id="93167-116">Azure DataShare-Kontoname.</span><span class="sxs-lookup"><span data-stu-id="93167-116">Azure DataShare Account name.</span></span>

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

### <span data-ttu-id="93167-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93167-117">-DefaultProfile</span></span>
<span data-ttu-id="93167-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="93167-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93167-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93167-119">-ResourceGroupName</span></span>
<span data-ttu-id="93167-120">Die Ressourcengruppe des Azure DataShare-Kontos.</span><span class="sxs-lookup"><span data-stu-id="93167-120">The resource group of the Azure DataShare Account.</span></span>

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

### <span data-ttu-id="93167-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="93167-121">-ResourceId</span></span>
<span data-ttu-id="93167-122">Die Ressourcen-ID der Freigabe</span><span class="sxs-lookup"><span data-stu-id="93167-122">The resource id of the share</span></span>

```yaml
Type: System.String
Parameter Sets: ByProviderShareSubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93167-123">-ShareName</span><span class="sxs-lookup"><span data-stu-id="93167-123">-ShareName</span></span>
<span data-ttu-id="93167-124">Azure DataShare-Name.</span><span class="sxs-lookup"><span data-stu-id="93167-124">Azure DataShare name.</span></span>

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

### <span data-ttu-id="93167-125">-ShareSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="93167-125">-ShareSubscriptionId</span></span>
<span data-ttu-id="93167-126">Die ID des Abonnements für Verbraucherfreigaben</span><span class="sxs-lookup"><span data-stu-id="93167-126">The id of consumer share subscription</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93167-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93167-127">CommonParameters</span></span>
<span data-ttu-id="93167-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93167-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93167-129">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="93167-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93167-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="93167-130">INPUTS</span></span>

### <span data-ttu-id="93167-131">System.String</span><span class="sxs-lookup"><span data-stu-id="93167-131">System.String</span></span>

## <span data-ttu-id="93167-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="93167-132">OUTPUTS</span></span>

### <span data-ttu-id="93167-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span><span class="sxs-lookup"><span data-stu-id="93167-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span></span>

## <span data-ttu-id="93167-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="93167-134">NOTES</span></span>

## <span data-ttu-id="93167-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="93167-135">RELATED LINKS</span></span>
