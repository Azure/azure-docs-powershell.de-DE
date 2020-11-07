---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscription.md
ms.openlocfilehash: ba4fc6a58cd345c149e551263ddf5880f099a54e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846091"
---
# <span data-ttu-id="557b2-101">Get-AzDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="557b2-101">Get-AzDataShareSubscription</span></span>

## <span data-ttu-id="557b2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="557b2-102">SYNOPSIS</span></span>
<span data-ttu-id="557b2-103">Ruft Informationen zu einem Freigabe Abonnement im Datenfreigabe Konto ab.</span><span class="sxs-lookup"><span data-stu-id="557b2-103">Gets information about share subscription in data share account.</span></span>

## <span data-ttu-id="557b2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="557b2-104">SYNTAX</span></span>

### <span data-ttu-id="557b2-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="557b2-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSubscription -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="557b2-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="557b2-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSubscription -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="557b2-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="557b2-107">DESCRIPTION</span></span>
<span data-ttu-id="557b2-108">Das Cmdlet " **Get-AzDataShareSubscription** " enthält Informationen zum Freigabe Abonnement in einem Datenfreigabe Konto.</span><span class="sxs-lookup"><span data-stu-id="557b2-108">The **Get-AzDataShareSubscription** cmdlet provides information about share subscription in a data share account.</span></span> <span data-ttu-id="557b2-109">Wenn der Name des Freigabe Abonnements angegeben wird, gibt das Cmdlet Informationen über das jeweilige Freigabe Abonnement aus.</span><span class="sxs-lookup"><span data-stu-id="557b2-109">If share subscription name is provided, the cmdlet gives information about the particular share subscription.</span></span> <span data-ttu-id="557b2-110">Andernfalls stellt das Cmdlet eine Liste der Freigabe Abonnements im Datenfreigabe Konto bereit.</span><span class="sxs-lookup"><span data-stu-id="557b2-110">Otherwise, the cmdlet provides a list of share subscriptions in the data share account.</span></span>

## <span data-ttu-id="557b2-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="557b2-111">EXAMPLES</span></span>

### <span data-ttu-id="557b2-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="557b2-112">Example 1</span></span>
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

<span data-ttu-id="557b2-113">Dieser Befehl enthält Informationen zum Freigeben von Abonnement AdsShareSubscription in Datenfreigabe Konto WikiAds.</span><span class="sxs-lookup"><span data-stu-id="557b2-113">This command provides information about share subscription AdsShareSubscription in data share account WikiAds.</span></span>

## <span data-ttu-id="557b2-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="557b2-114">PARAMETERS</span></span>

### <span data-ttu-id="557b2-115">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="557b2-115">-AccountName</span></span>
<span data-ttu-id="557b2-116">Name des Azure-Datenfreigabe Kontos</span><span class="sxs-lookup"><span data-stu-id="557b2-116">Azure data share account name</span></span>

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

### <span data-ttu-id="557b2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="557b2-117">-DefaultProfile</span></span>
<span data-ttu-id="557b2-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="557b2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="557b2-119">-Name</span><span class="sxs-lookup"><span data-stu-id="557b2-119">-Name</span></span>
<span data-ttu-id="557b2-120">Name des Azure Data Share-Abonnements</span><span class="sxs-lookup"><span data-stu-id="557b2-120">Azure data share subscription name</span></span>

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

### <span data-ttu-id="557b2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="557b2-121">-ResourceGroupName</span></span>
<span data-ttu-id="557b2-122">Der Name der Ressourcengruppe des Azure Data Share-Kontos</span><span class="sxs-lookup"><span data-stu-id="557b2-122">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="557b2-123">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="557b2-123">-ResourceId</span></span>
<span data-ttu-id="557b2-124">Die Ressourcen-ID des Azure Data Share-Abonnements</span><span class="sxs-lookup"><span data-stu-id="557b2-124">The resource id of the azure data share subscription</span></span>

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

### <span data-ttu-id="557b2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="557b2-125">CommonParameters</span></span>
<span data-ttu-id="557b2-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="557b2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="557b2-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="557b2-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="557b2-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="557b2-128">INPUTS</span></span>

### <span data-ttu-id="557b2-129">System. String</span><span class="sxs-lookup"><span data-stu-id="557b2-129">System.String</span></span>

## <span data-ttu-id="557b2-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="557b2-130">OUTPUTS</span></span>

### <span data-ttu-id="557b2-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="557b2-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span></span>

## <span data-ttu-id="557b2-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="557b2-132">NOTES</span></span>

## <span data-ttu-id="557b2-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="557b2-133">RELATED LINKS</span></span>
