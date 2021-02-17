---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatasharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSubscription.md
ms.openlocfilehash: e6b911831a84ce708af93ef6cc7b9f9be919758b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100165281"
---
# <span data-ttu-id="95aa3-101">New-AzDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="95aa3-101">New-AzDataShareSubscription</span></span>

## <span data-ttu-id="95aa3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95aa3-102">SYNOPSIS</span></span>
<span data-ttu-id="95aa3-103">Erstellt ein neues Freigabeabonnement.</span><span class="sxs-lookup"><span data-stu-id="95aa3-103">Creates a new share subscription.</span></span>

## <span data-ttu-id="95aa3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="95aa3-104">SYNTAX</span></span>

```
New-AzDataShareSubscription -ResourceGroupName <String> -AccountName <String> -Name <String>
 -InvitationId <String> -SourceShareLocation <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95aa3-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="95aa3-105">DESCRIPTION</span></span>
<span data-ttu-id="95aa3-106">Das **Cmdlet "New-AzDataShareSubscription"** erstellt ein Freigabeabonnement in einem angegebenen Datenfreigabekonto und einer Einladungs-ID.</span><span class="sxs-lookup"><span data-stu-id="95aa3-106">The **New-AzDataShareSubscription** cmdlet creates a share subscription in specified data share account and invitation id.</span></span>

## <span data-ttu-id="95aa3-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="95aa3-107">EXAMPLES</span></span>

### <span data-ttu-id="95aa3-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="95aa3-108">Example 1</span></span>
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

<span data-ttu-id="95aa3-109">Mit diesen Befehlen wird unter "WikiAds" für das Datenfreigabekonto ein neues AdsShareSubscription für in adsshareSubscription erstellt.</span><span class="sxs-lookup"><span data-stu-id="95aa3-109">This commands creates a new share subscription AdsShareSubscription for invitaionId under data share account WikiAds.</span></span>

## <span data-ttu-id="95aa3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="95aa3-110">PARAMETERS</span></span>

### <span data-ttu-id="95aa3-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="95aa3-111">-AccountName</span></span>
<span data-ttu-id="95aa3-112">Name des Azure-Datenfreigabekontos</span><span class="sxs-lookup"><span data-stu-id="95aa3-112">Azure data share account name</span></span>

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

### <span data-ttu-id="95aa3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95aa3-113">-DefaultProfile</span></span>
<span data-ttu-id="95aa3-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="95aa3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95aa3-115">-InvitationId</span><span class="sxs-lookup"><span data-stu-id="95aa3-115">-InvitationId</span></span>
<span data-ttu-id="95aa3-116">Azure data share invitationId</span><span class="sxs-lookup"><span data-stu-id="95aa3-116">Azure data share invitationId</span></span>

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

### <span data-ttu-id="95aa3-117">-Name</span><span class="sxs-lookup"><span data-stu-id="95aa3-117">-Name</span></span>
<span data-ttu-id="95aa3-118">Name des Azure Data Share-Abonnements</span><span class="sxs-lookup"><span data-stu-id="95aa3-118">Azure data share subscription name</span></span>

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

### <span data-ttu-id="95aa3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95aa3-119">-ResourceGroupName</span></span>
<span data-ttu-id="95aa3-120">Der Ressourcengruppenname des Azure Data Share-Kontos</span><span class="sxs-lookup"><span data-stu-id="95aa3-120">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="95aa3-121">-SourceShareLocation</span><span class="sxs-lookup"><span data-stu-id="95aa3-121">-SourceShareLocation</span></span>
<span data-ttu-id="95aa3-122">Speicherort der Azure-Datenfreigabe</span><span class="sxs-lookup"><span data-stu-id="95aa3-122">Azure data share location</span></span>

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

### <span data-ttu-id="95aa3-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="95aa3-123">-Confirm</span></span>
<span data-ttu-id="95aa3-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="95aa3-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95aa3-125">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="95aa3-125">-WhatIf</span></span>
<span data-ttu-id="95aa3-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="95aa3-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95aa3-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="95aa3-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95aa3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95aa3-128">CommonParameters</span></span>
<span data-ttu-id="95aa3-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95aa3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95aa3-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="95aa3-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95aa3-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="95aa3-131">INPUTS</span></span>

### <span data-ttu-id="95aa3-132">Keine</span><span class="sxs-lookup"><span data-stu-id="95aa3-132">None</span></span>

## <span data-ttu-id="95aa3-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="95aa3-133">OUTPUTS</span></span>

### <span data-ttu-id="95aa3-134">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="95aa3-134">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="95aa3-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="95aa3-135">NOTES</span></span>

## <span data-ttu-id="95aa3-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="95aa3-136">RELATED LINKS</span></span>
