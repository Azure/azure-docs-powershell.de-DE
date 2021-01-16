---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/grant-azdatasharesubscriptionaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Grant-AzDataShareSubscriptionAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Grant-AzDataShareSubscriptionAccess.md
ms.openlocfilehash: 4ad530fdd27c3b87b8e96e1752c00fc149c1dd42
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98290332"
---
# <span data-ttu-id="c58be-101">Grant-AzDataShareSubscriptionAccess</span><span class="sxs-lookup"><span data-stu-id="c58be-101">Grant-AzDataShareSubscriptionAccess</span></span>

## <span data-ttu-id="c58be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c58be-102">SYNOPSIS</span></span>
<span data-ttu-id="c58be-103">Gewährt einem widerrufenen Freigabeabonnement Zugriff auf die Quellfreigabe</span><span class="sxs-lookup"><span data-stu-id="c58be-103">Grants a revoked share subscription access to source share</span></span>

## <span data-ttu-id="c58be-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c58be-104">SYNTAX</span></span>

### <span data-ttu-id="c58be-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c58be-105">ByFieldsParameterSet (Default)</span></span>
```
Grant-AzDataShareSubscriptionAccess -ResourceGroupName <String> -AccountName <String> [-ShareName <String>]
 -ShareSubscriptionId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c58be-106">ByProviderShareSubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c58be-106">ByProviderShareSubscriptionIdParameterSet</span></span>
```
Grant-AzDataShareSubscriptionAccess -ShareSubscriptionId <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c58be-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c58be-107">DESCRIPTION</span></span>
<span data-ttu-id="c58be-108">Das **Cmdlet Grant-AzDataShareSubscriptionAccess** gewährt einem Freigabeabonnement Zugriff auf die Quellfreigabe</span><span class="sxs-lookup"><span data-stu-id="c58be-108">The **Grant-AzDataShareSubscriptionAccess** cmdlet grants a share subscription access to source share</span></span>

## <span data-ttu-id="c58be-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c58be-109">EXAMPLES</span></span>

### <span data-ttu-id="c58be-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c58be-110">Example 1</span></span>
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

<span data-ttu-id="c58be-111">Gewährten Zugriff auf das Freigabeabonnement( id 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12)</span><span class="sxs-lookup"><span data-stu-id="c58be-111">Grants access to share subscription identified by id 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12</span></span>

## <span data-ttu-id="c58be-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c58be-112">PARAMETERS</span></span>

### <span data-ttu-id="c58be-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c58be-113">-AccountName</span></span>
<span data-ttu-id="c58be-114">Name des Azure-Datenfreigabekontos</span><span class="sxs-lookup"><span data-stu-id="c58be-114">Azure data share account name</span></span>

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

### <span data-ttu-id="c58be-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c58be-115">-DefaultProfile</span></span>
<span data-ttu-id="c58be-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c58be-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c58be-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c58be-117">-ResourceGroupName</span></span>
<span data-ttu-id="c58be-118">Der Ressourcengruppenname des Azure Data Share-Kontos</span><span class="sxs-lookup"><span data-stu-id="c58be-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="c58be-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c58be-119">-ResourceId</span></span>
<span data-ttu-id="c58be-120">Die Ressourcen-ID der Azure-Datenfreigabe</span><span class="sxs-lookup"><span data-stu-id="c58be-120">The resource id of the azure data share</span></span>

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

### <span data-ttu-id="c58be-121">-ShareName</span><span class="sxs-lookup"><span data-stu-id="c58be-121">-ShareName</span></span>
<span data-ttu-id="c58be-122">Name der Azure-Datenfreigabe</span><span class="sxs-lookup"><span data-stu-id="c58be-122">Azure data share name</span></span>

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

### <span data-ttu-id="c58be-123">-ShareSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c58be-123">-ShareSubscriptionId</span></span>
<span data-ttu-id="c58be-124">Die ID des Freigabeabonnements des Anbieterfreigabeabonnements</span><span class="sxs-lookup"><span data-stu-id="c58be-124">The share subscription id of the provider share subscription</span></span>

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

### <span data-ttu-id="c58be-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c58be-125">-Confirm</span></span>
<span data-ttu-id="c58be-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c58be-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c58be-127">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="c58be-127">-WhatIf</span></span>
<span data-ttu-id="c58be-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c58be-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c58be-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c58be-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c58be-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c58be-130">CommonParameters</span></span>
<span data-ttu-id="c58be-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c58be-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c58be-132">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c58be-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c58be-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c58be-133">INPUTS</span></span>

### <span data-ttu-id="c58be-134">System.String</span><span class="sxs-lookup"><span data-stu-id="c58be-134">System.String</span></span>

## <span data-ttu-id="c58be-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c58be-135">OUTPUTS</span></span>

### <span data-ttu-id="c58be-136">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span><span class="sxs-lookup"><span data-stu-id="c58be-136">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span></span>

## <span data-ttu-id="c58be-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c58be-137">NOTES</span></span>

## <span data-ttu-id="c58be-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c58be-138">RELATED LINKS</span></span>
