---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/new-azdatasharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSubscription.md
ms.openlocfilehash: a7b3a60d97692d01eb8be374ab9670af4b331f95
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941851"
---
# <span data-ttu-id="b6614-101">New-AzDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="b6614-101">New-AzDataShareSubscription</span></span>

## <span data-ttu-id="b6614-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6614-102">SYNOPSIS</span></span>
<span data-ttu-id="b6614-103">Erstellt ein neues Freigabeabonnement.</span><span class="sxs-lookup"><span data-stu-id="b6614-103">Creates a new share subscription.</span></span>

## <span data-ttu-id="b6614-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b6614-104">SYNTAX</span></span>

```
New-AzDataShareSubscription -ResourceGroupName <String> -AccountName <String> -Name <String>
 -InvitationId <String> -SourceShareLocation <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6614-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b6614-105">DESCRIPTION</span></span>
<span data-ttu-id="b6614-106">Das **Cmdlet New-AzDataShareSubscription** erstellt ein Freigabeabonnement in einem angegebenen Datenfreigabekonto und der Einladungs-ID.</span><span class="sxs-lookup"><span data-stu-id="b6614-106">The **New-AzDataShareSubscription** cmdlet creates a share subscription in specified data share account and invitation id.</span></span>

## <span data-ttu-id="b6614-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b6614-107">EXAMPLES</span></span>

### <span data-ttu-id="b6614-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b6614-108">Example 1</span></span>
```
PS C:\> New-AzDataShareSubscription -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShareSubscription" -InvitationId "167e06ff-567f-4bc7-be0c-645a6de710f3"
CreatedAt               : 6/30/2019 12:42:12 AM
CreatedBy               : adstest@microsoft.com
InvitationId            : 167e06ff-567f-4bc7-be0c-645a6de710f3
ProvisioningState       : Succeeded
ShareName               : AdsShare
ShareSender             : adsprovider@microsoft.com
ShareSenderCompanyName  : ADS Company
ShareDescription        : Test description  
ShareTerms              : Test terms of use
ShareSubscriptionStatus : Active
ShareKind               : CopyBased
Id                      : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shareSubscriptions/AdsShareSubscription
Name                    : AdsShareSubscription
Type                    : Microsoft.DataShare/ShareSubscriptions
```

<span data-ttu-id="b6614-109">Mit diesen Befehlen wird ein neues Freigabeabonnement adsShareSubscription für invitaionId unter WikiAds des Datenfreigabekontos erstellt.</span><span class="sxs-lookup"><span data-stu-id="b6614-109">This commands creates a new share subscription AdsShareSubscription for invitaionId under data share account WikiAds.</span></span>

## <span data-ttu-id="b6614-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b6614-110">PARAMETERS</span></span>

### <span data-ttu-id="b6614-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b6614-111">-AccountName</span></span>
<span data-ttu-id="b6614-112">Name des Azure-Datenfreigabekontos</span><span class="sxs-lookup"><span data-stu-id="b6614-112">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6614-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6614-113">-DefaultProfile</span></span>
<span data-ttu-id="b6614-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b6614-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6614-115">-InvitationId</span><span class="sxs-lookup"><span data-stu-id="b6614-115">-InvitationId</span></span>
<span data-ttu-id="b6614-116">Einladung zur Azure-Datenfreigabe</span><span class="sxs-lookup"><span data-stu-id="b6614-116">Azure data share invitationId</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6614-117">-Name</span><span class="sxs-lookup"><span data-stu-id="b6614-117">-Name</span></span>
<span data-ttu-id="b6614-118">Azure Data Share Subscription Name</span><span class="sxs-lookup"><span data-stu-id="b6614-118">Azure data share subscription name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6614-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6614-119">-ResourceGroupName</span></span>
<span data-ttu-id="b6614-120">Der Ressourcengruppenname des Azure Data Share-Kontos</span><span class="sxs-lookup"><span data-stu-id="b6614-120">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6614-121">-SourceShareLocation</span><span class="sxs-lookup"><span data-stu-id="b6614-121">-SourceShareLocation</span></span>
<span data-ttu-id="b6614-122">Speicherort der Azure-Datenfreigabe</span><span class="sxs-lookup"><span data-stu-id="b6614-122">Azure data share location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6614-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b6614-123">-Confirm</span></span>
<span data-ttu-id="b6614-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b6614-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6614-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6614-125">-WhatIf</span></span>
<span data-ttu-id="b6614-126">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b6614-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6614-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b6614-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6614-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6614-128">CommonParameters</span></span>
<span data-ttu-id="b6614-129">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6614-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6614-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b6614-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6614-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b6614-131">INPUTS</span></span>

### <span data-ttu-id="b6614-132">Keine</span><span class="sxs-lookup"><span data-stu-id="b6614-132">None</span></span>

## <span data-ttu-id="b6614-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b6614-133">OUTPUTS</span></span>

### <span data-ttu-id="b6614-134">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="b6614-134">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="b6614-135">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b6614-135">NOTES</span></span>

## <span data-ttu-id="b6614-136">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b6614-136">RELATED LINKS</span></span>
