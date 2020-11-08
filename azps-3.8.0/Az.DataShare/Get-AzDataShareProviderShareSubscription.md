---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatashareprovidersharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareProviderShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareProviderShareSubscription.md
ms.openlocfilehash: a94d879573be2d640269510283e341cbad8aa052
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995870"
---
# <span data-ttu-id="c36be-101">Get-AzDataShareProviderShareSubscription</span><span class="sxs-lookup"><span data-stu-id="c36be-101">Get-AzDataShareProviderShareSubscription</span></span>

## <span data-ttu-id="c36be-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c36be-102">SYNOPSIS</span></span>
<span data-ttu-id="c36be-103">Ruft Informationen zu Verbraucher Freigabe Abonnements auf Anbieterseite ab.</span><span class="sxs-lookup"><span data-stu-id="c36be-103">Gets information about consumer share subscriptions on provider side.</span></span>

## <span data-ttu-id="c36be-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c36be-104">SYNTAX</span></span>

### <span data-ttu-id="c36be-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c36be-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareProviderShareSubscription -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 [-ShareSubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c36be-106">ByProviderShareSubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c36be-106">ByProviderShareSubscriptionIdParameterSet</span></span>
```
Get-AzDataShareProviderShareSubscription [-ShareSubscriptionId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c36be-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c36be-107">DESCRIPTION</span></span>
<span data-ttu-id="c36be-108">Das Cmdlet " **Get-AzDataShareProviderSubscription** " Ruft Informationen zu Consumer-Freigabe Abonnements auf Anbieterseite ab.</span><span class="sxs-lookup"><span data-stu-id="c36be-108">The **Get-AzDataShareProviderSubscription** cmdlet gets information about consumer share subscriptions on provider side.</span></span> <span data-ttu-id="c36be-109">Wenn Sie die Freigabe-Abonnenten-ID angeben, ruft dieses Cmdlet Informationen zum Freigabe Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="c36be-109">If you specify the share subscrption id, this cmdlet gets information about the share subscription.</span></span> <span data-ttu-id="c36be-110">Wenn Sie die Freigabe Abonnement-ID nicht angeben, ruft dieses Cmdlet Informationen zu allen Consumer-Freigabe Abonnements auf, die der Freigabe zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="c36be-110">If you do not specify the share subscription id, this cmdlet gets information about all the consumer share subscriptions in associated with the share.</span></span>

## <span data-ttu-id="c36be-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c36be-111">EXAMPLES</span></span>

### <span data-ttu-id="c36be-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c36be-112">Example 1</span></span>
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

<span data-ttu-id="c36be-113">Dieser Befehl enthält Informationen zum Consumer-Share-Abonnement, das mit Freigabe-AdsShare in Datenfreigabe Konto WikiAds verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="c36be-113">This commands provides information about consumer share subscription associated with share AdsShare in data share account WikiAds.</span></span>

## <span data-ttu-id="c36be-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="c36be-114">PARAMETERS</span></span>

### <span data-ttu-id="c36be-115">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="c36be-115">-AccountName</span></span>
<span data-ttu-id="c36be-116">Azure DataShare-Konto Name.</span><span class="sxs-lookup"><span data-stu-id="c36be-116">Azure DataShare Account name.</span></span>

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

### <span data-ttu-id="c36be-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c36be-117">-DefaultProfile</span></span>
<span data-ttu-id="c36be-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c36be-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c36be-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c36be-119">-ResourceGroupName</span></span>
<span data-ttu-id="c36be-120">Die Ressourcengruppe des Azure DataShare-Kontos.</span><span class="sxs-lookup"><span data-stu-id="c36be-120">The resource group of the Azure DataShare Account.</span></span>

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

### <span data-ttu-id="c36be-121">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="c36be-121">-ResourceId</span></span>
<span data-ttu-id="c36be-122">Die Ressourcen-ID der Freigabe</span><span class="sxs-lookup"><span data-stu-id="c36be-122">The resource id of the share</span></span>

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

### <span data-ttu-id="c36be-123">-Freigabename</span><span class="sxs-lookup"><span data-stu-id="c36be-123">-ShareName</span></span>
<span data-ttu-id="c36be-124">Azure DataShare-Name.</span><span class="sxs-lookup"><span data-stu-id="c36be-124">Azure DataShare name.</span></span>

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

### <span data-ttu-id="c36be-125">-ShareSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c36be-125">-ShareSubscriptionId</span></span>
<span data-ttu-id="c36be-126">Die ID des Consumer-Share-Abonnements</span><span class="sxs-lookup"><span data-stu-id="c36be-126">The id of consumer share subscription</span></span>

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

### <span data-ttu-id="c36be-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c36be-127">CommonParameters</span></span>
<span data-ttu-id="c36be-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c36be-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c36be-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c36be-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c36be-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c36be-130">INPUTS</span></span>

### <span data-ttu-id="c36be-131">System. String</span><span class="sxs-lookup"><span data-stu-id="c36be-131">System.String</span></span>

## <span data-ttu-id="c36be-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c36be-132">OUTPUTS</span></span>

### <span data-ttu-id="c36be-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span><span class="sxs-lookup"><span data-stu-id="c36be-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span></span>

## <span data-ttu-id="c36be-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="c36be-134">NOTES</span></span>

## <span data-ttu-id="c36be-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c36be-135">RELATED LINKS</span></span>
