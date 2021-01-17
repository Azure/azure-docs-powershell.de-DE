---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/revoke-azdatasharesubscriptionaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Revoke-AzDataShareSubscriptionAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Revoke-AzDataShareSubscriptionAccess.md
ms.openlocfilehash: 540426cc8612f4cee7364a7875bb9a142bca07ef
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360840"
---
# <span data-ttu-id="dad5c-101">Revoke-AzDataShareSubscriptionAccess</span><span class="sxs-lookup"><span data-stu-id="dad5c-101">Revoke-AzDataShareSubscriptionAccess</span></span>

## <span data-ttu-id="dad5c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dad5c-102">SYNOPSIS</span></span>
<span data-ttu-id="dad5c-103">Widerruft den Zugriff auf das Freigabeabonnement auf die Quellfreigabe</span><span class="sxs-lookup"><span data-stu-id="dad5c-103">Revokes share subscription access to source share</span></span>

## <span data-ttu-id="dad5c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dad5c-104">SYNTAX</span></span>

### <span data-ttu-id="dad5c-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="dad5c-105">ByFieldsParameterSet (Default)</span></span>
```
Revoke-AzDataShareSubscriptionAccess -ResourceGroupName <String> -AccountName <String> [-ShareName <String>]
 -ShareSubscriptionId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dad5c-106">ByProviderShareSubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dad5c-106">ByProviderShareSubscriptionIdParameterSet</span></span>
```
Revoke-AzDataShareSubscriptionAccess -ShareSubscriptionId <String> -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dad5c-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dad5c-107">DESCRIPTION</span></span>
<span data-ttu-id="dad5c-108">Das **Cmdlet Revoke-AzDataShareSubscriptionAccess** gewährt einem Freigabeabonnement Zugriff auf die Quellfreigabe</span><span class="sxs-lookup"><span data-stu-id="dad5c-108">The **Revoke-AzDataShareSubscriptionAccess** cmdlet grants a share subscription access to source share</span></span>

## <span data-ttu-id="dad5c-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="dad5c-109">EXAMPLES</span></span>

### <span data-ttu-id="dad5c-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="dad5c-110">Example 1</span></span>
```
PS C:\> Revoke-AzDataShareSubscriptionAccess -ResourceGroupName "ADS" -AccountName "WikiAdsAccount" -ShareName "AdsShare" -ShareSubscriptionId 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12

Company                   : ADS
CreatedAt                 : 6/15/2019 1:02:28 AM
CreatedBy                 : abc@microsoft.com
SharedAt                  : 6/15/2019 12:08:48 AM
SharedBy                  : abc@microsoft.com
ShareSubscriptionObjectId : 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12
ShareSubscriptionStatus   : Revoked
Id                        : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAdsAccount/shares/AdsShare/shareSubscriptions/8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12
Name                      : AdsShare
Type                      : Microsoft.DataShare/ShareSubscriptions
```

<span data-ttu-id="dad5c-111">Widerruft den Zugriff auf das Share-Abonnement, gekennzeichnet durch id 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12</span><span class="sxs-lookup"><span data-stu-id="dad5c-111">Revokes access of share subscription identified by id 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12</span></span>

## <span data-ttu-id="dad5c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dad5c-112">PARAMETERS</span></span>

### <span data-ttu-id="dad5c-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="dad5c-113">-AccountName</span></span>
<span data-ttu-id="dad5c-114">Name des Azure-Datenfreigabekontos</span><span class="sxs-lookup"><span data-stu-id="dad5c-114">Azure data share account name</span></span>

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

### <span data-ttu-id="dad5c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dad5c-115">-AsJob</span></span>
<span data-ttu-id="dad5c-116">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="dad5c-116">{{Fill AsJob Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dad5c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dad5c-117">-DefaultProfile</span></span>
<span data-ttu-id="dad5c-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dad5c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dad5c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dad5c-119">-ResourceGroupName</span></span>
<span data-ttu-id="dad5c-120">Der Ressourcengruppenname des Azure Data Share-Kontos</span><span class="sxs-lookup"><span data-stu-id="dad5c-120">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="dad5c-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dad5c-121">-ResourceId</span></span>
<span data-ttu-id="dad5c-122">Die Ressourcen-ID der Azure Data Share</span><span class="sxs-lookup"><span data-stu-id="dad5c-122">The resource id of the azure data share</span></span>

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

### <span data-ttu-id="dad5c-123">-ShareName</span><span class="sxs-lookup"><span data-stu-id="dad5c-123">-ShareName</span></span>
<span data-ttu-id="dad5c-124">Name der Azure-Datenfreigabe</span><span class="sxs-lookup"><span data-stu-id="dad5c-124">Azure data share name</span></span>

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

### <span data-ttu-id="dad5c-125">-ShareSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dad5c-125">-ShareSubscriptionId</span></span>
<span data-ttu-id="dad5c-126">Die ID des Freigabeabonnements des Anbieterfreigabeabonnements</span><span class="sxs-lookup"><span data-stu-id="dad5c-126">The share subscription id of the provider share subscription</span></span>

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

### <span data-ttu-id="dad5c-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dad5c-127">-Confirm</span></span>
<span data-ttu-id="dad5c-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dad5c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dad5c-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="dad5c-129">-WhatIf</span></span>
<span data-ttu-id="dad5c-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dad5c-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dad5c-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dad5c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dad5c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dad5c-132">CommonParameters</span></span>
<span data-ttu-id="dad5c-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dad5c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dad5c-134">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dad5c-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dad5c-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="dad5c-135">INPUTS</span></span>

### <span data-ttu-id="dad5c-136">System.String</span><span class="sxs-lookup"><span data-stu-id="dad5c-136">System.String</span></span>

## <span data-ttu-id="dad5c-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="dad5c-137">OUTPUTS</span></span>

### <span data-ttu-id="dad5c-138">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span><span class="sxs-lookup"><span data-stu-id="dad5c-138">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span></span>

## <span data-ttu-id="dad5c-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="dad5c-139">NOTES</span></span>

## <span data-ttu-id="dad5c-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="dad5c-140">RELATED LINKS</span></span>
