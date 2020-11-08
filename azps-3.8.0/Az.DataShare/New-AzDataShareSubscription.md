---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatasharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSubscription.md
ms.openlocfilehash: 01cff184a2db4364536d4088103380f3f28b47a7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996531"
---
# <span data-ttu-id="225ff-101">New-AzDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="225ff-101">New-AzDataShareSubscription</span></span>

## <span data-ttu-id="225ff-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="225ff-102">SYNOPSIS</span></span>
<span data-ttu-id="225ff-103">Erstellt ein neues Freigabe Abonnement.</span><span class="sxs-lookup"><span data-stu-id="225ff-103">Creates a new share subscription.</span></span>

## <span data-ttu-id="225ff-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="225ff-104">SYNTAX</span></span>

```
New-AzDataShareSubscription -ResourceGroupName <String> -AccountName <String> -Name <String>
 -InvitationId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="225ff-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="225ff-105">DESCRIPTION</span></span>
<span data-ttu-id="225ff-106">Mit dem Cmdlet **New-AzDataShareSubscription** wird ein Freigabe Abonnement im angegebenen Datenfreigabe Konto und der Einladungs-ID erstellt.</span><span class="sxs-lookup"><span data-stu-id="225ff-106">The **New-AzDataShareSubscription** cmdlet creates a share subscription in specified data share account and invitation id.</span></span>

## <span data-ttu-id="225ff-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="225ff-107">EXAMPLES</span></span>

### <span data-ttu-id="225ff-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="225ff-108">Example 1</span></span>
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

<span data-ttu-id="225ff-109">Dieser Befehl erstellt ein neues Freigabe Abonnement AdsShareSubscription für invitaionId unter Datenfreigabe Konto WikiAds.</span><span class="sxs-lookup"><span data-stu-id="225ff-109">This commands creates a new share subscription AdsShareSubscription for invitaionId under data share account WikiAds.</span></span>

## <span data-ttu-id="225ff-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="225ff-110">PARAMETERS</span></span>

### <span data-ttu-id="225ff-111">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="225ff-111">-AccountName</span></span>
<span data-ttu-id="225ff-112">Name des Azure-Datenfreigabe Kontos</span><span class="sxs-lookup"><span data-stu-id="225ff-112">Azure data share account name</span></span>

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

### <span data-ttu-id="225ff-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="225ff-113">-DefaultProfile</span></span>
<span data-ttu-id="225ff-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="225ff-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="225ff-115">-Einladungs-Nr.</span><span class="sxs-lookup"><span data-stu-id="225ff-115">-InvitationId</span></span>
<span data-ttu-id="225ff-116">Azure Data Freigabe-Einladungs-Nr</span><span class="sxs-lookup"><span data-stu-id="225ff-116">Azure data share invitationId</span></span>

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

### <span data-ttu-id="225ff-117">-Name</span><span class="sxs-lookup"><span data-stu-id="225ff-117">-Name</span></span>
<span data-ttu-id="225ff-118">Name des Azure Data Share-Abonnements</span><span class="sxs-lookup"><span data-stu-id="225ff-118">Azure data share subscription name</span></span>

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

### <span data-ttu-id="225ff-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="225ff-119">-ResourceGroupName</span></span>
<span data-ttu-id="225ff-120">Der Name der Ressourcengruppe des Azure Data Share-Kontos</span><span class="sxs-lookup"><span data-stu-id="225ff-120">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="225ff-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="225ff-121">-Confirm</span></span>
<span data-ttu-id="225ff-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="225ff-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="225ff-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="225ff-123">-WhatIf</span></span>
<span data-ttu-id="225ff-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="225ff-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="225ff-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="225ff-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="225ff-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="225ff-126">CommonParameters</span></span>
<span data-ttu-id="225ff-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="225ff-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="225ff-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="225ff-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="225ff-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="225ff-129">INPUTS</span></span>

### <span data-ttu-id="225ff-130">Keine</span><span class="sxs-lookup"><span data-stu-id="225ff-130">None</span></span>

## <span data-ttu-id="225ff-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="225ff-131">OUTPUTS</span></span>

### <span data-ttu-id="225ff-132">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="225ff-132">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="225ff-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="225ff-133">NOTES</span></span>

## <span data-ttu-id="225ff-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="225ff-134">RELATED LINKS</span></span>
