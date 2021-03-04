---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/grant-azdatasharesubscriptionaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Grant-AzDataShareSubscriptionAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Grant-AzDataShareSubscriptionAccess.md
ms.openlocfilehash: 00b82731e807aa2351d66744b889f56f440226b2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101946126"
---
# <span data-ttu-id="f2cb1-101">Grant-AzDataShareSubscriptionAccess</span><span class="sxs-lookup"><span data-stu-id="f2cb1-101">Grant-AzDataShareSubscriptionAccess</span></span>

## <span data-ttu-id="f2cb1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2cb1-102">SYNOPSIS</span></span>
<span data-ttu-id="f2cb1-103">Gewährt einem widerrufenen Freigabeabonnement Zugriff auf die Quellfreigabe</span><span class="sxs-lookup"><span data-stu-id="f2cb1-103">Grants a revoked share subscription access to source share</span></span>

## <span data-ttu-id="f2cb1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f2cb1-104">SYNTAX</span></span>

### <span data-ttu-id="f2cb1-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f2cb1-105">ByFieldsParameterSet (Default)</span></span>
```
Grant-AzDataShareSubscriptionAccess -ResourceGroupName <String> -AccountName <String> [-ShareName <String>]
 -ShareSubscriptionId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f2cb1-106">ByProviderShareSubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2cb1-106">ByProviderShareSubscriptionIdParameterSet</span></span>
```
Grant-AzDataShareSubscriptionAccess -ShareSubscriptionId <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2cb1-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f2cb1-107">DESCRIPTION</span></span>
<span data-ttu-id="f2cb1-108">Das **Grant-AzDataShareSubscriptionAccess-Cmdlet** gewährt einem Freigabeabonnement Zugriff auf die Quellfreigabe.</span><span class="sxs-lookup"><span data-stu-id="f2cb1-108">The **Grant-AzDataShareSubscriptionAccess** cmdlet grants a share subscription access to source share</span></span>

## <span data-ttu-id="f2cb1-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f2cb1-109">EXAMPLES</span></span>

### <span data-ttu-id="f2cb1-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f2cb1-110">Example 1</span></span>
```
PS C:\> Grant-AzDataShareSubscriptionAccess -ResourceGroupName "ADS" -AccountName "WikiAdsAccount" -ShareName "AdsShare" -ShareSubscriptionId 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12

Company                   : ADS
CreatedAt                 : 6/15/2019 1:02:28 AM
CreatedBy                 : abc@microsoft.com
SharedAt                  : 6/15/2019 12:08:48 AM
SharedBy                  : abc@microsoft.com
ShareSubscriptionObjectId : 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12
ShareSubscriptionStatus   : Active
Id                        : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAdsAccount/shares/AdsShare/shareSubscriptions/8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12
Name                      : AdsShare
Type                      : Microsoft.DataShare/ShareSubscriptions
```

<span data-ttu-id="f2cb1-111">Gewährt Zugriff auf ein Freigabeabonnement, das mit id 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12 identifiziert wurde</span><span class="sxs-lookup"><span data-stu-id="f2cb1-111">Grants access to share subscription identified by id 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12</span></span>

## <span data-ttu-id="f2cb1-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f2cb1-112">PARAMETERS</span></span>

### <span data-ttu-id="f2cb1-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f2cb1-113">-AccountName</span></span>
<span data-ttu-id="f2cb1-114">Name des Azure-Datenfreigabekontos</span><span class="sxs-lookup"><span data-stu-id="f2cb1-114">Azure data share account name</span></span>

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

### <span data-ttu-id="f2cb1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2cb1-115">-DefaultProfile</span></span>
<span data-ttu-id="f2cb1-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f2cb1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2cb1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2cb1-117">-ResourceGroupName</span></span>
<span data-ttu-id="f2cb1-118">Der Ressourcengruppenname des Azure Data Share-Kontos</span><span class="sxs-lookup"><span data-stu-id="f2cb1-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="f2cb1-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f2cb1-119">-ResourceId</span></span>
<span data-ttu-id="f2cb1-120">Die Ressourcen-ID der Azure-Datenfreigabe</span><span class="sxs-lookup"><span data-stu-id="f2cb1-120">The resource id of the azure data share</span></span>

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

### <span data-ttu-id="f2cb1-121">-ShareName</span><span class="sxs-lookup"><span data-stu-id="f2cb1-121">-ShareName</span></span>
<span data-ttu-id="f2cb1-122">Name der Azure-Datenfreigabe</span><span class="sxs-lookup"><span data-stu-id="f2cb1-122">Azure data share name</span></span>

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

### <span data-ttu-id="f2cb1-123">-ShareSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f2cb1-123">-ShareSubscriptionId</span></span>
<span data-ttu-id="f2cb1-124">Die Freigabeabonnement-ID des Anbieterfreigabeabonnements</span><span class="sxs-lookup"><span data-stu-id="f2cb1-124">The share subscription id of the provider share subscription</span></span>

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

### <span data-ttu-id="f2cb1-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f2cb1-125">-Confirm</span></span>
<span data-ttu-id="f2cb1-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f2cb1-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2cb1-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2cb1-127">-WhatIf</span></span>
<span data-ttu-id="f2cb1-128">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f2cb1-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f2cb1-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f2cb1-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2cb1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2cb1-130">CommonParameters</span></span>
<span data-ttu-id="f2cb1-131">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2cb1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2cb1-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f2cb1-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2cb1-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f2cb1-133">INPUTS</span></span>

### <span data-ttu-id="f2cb1-134">System.String</span><span class="sxs-lookup"><span data-stu-id="f2cb1-134">System.String</span></span>

## <span data-ttu-id="f2cb1-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f2cb1-135">OUTPUTS</span></span>

### <span data-ttu-id="f2cb1-136">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span><span class="sxs-lookup"><span data-stu-id="f2cb1-136">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span></span>

## <span data-ttu-id="f2cb1-137">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f2cb1-137">NOTES</span></span>

## <span data-ttu-id="f2cb1-138">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f2cb1-138">RELATED LINKS</span></span>
