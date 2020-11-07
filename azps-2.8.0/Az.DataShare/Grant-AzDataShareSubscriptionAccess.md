---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/grant-azdatasharesubscriptionaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Grant-AzDataShareSubscriptionAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Grant-AzDataShareSubscriptionAccess.md
ms.openlocfilehash: befe472f3340ae41e669ffa584e500051a7728d4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651422"
---
# <span data-ttu-id="0f065-101">Grant-AzDataShareSubscriptionAccess</span><span class="sxs-lookup"><span data-stu-id="0f065-101">Grant-AzDataShareSubscriptionAccess</span></span>

## <span data-ttu-id="0f065-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0f065-102">SYNOPSIS</span></span>
<span data-ttu-id="0f065-103">Gewährt einem gesperrten Freigabe Abonnement Zugriff auf die Quell Freigabe</span><span class="sxs-lookup"><span data-stu-id="0f065-103">Grants a revoked share subscription access to source share</span></span>

## <span data-ttu-id="0f065-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0f065-104">SYNTAX</span></span>

### <span data-ttu-id="0f065-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="0f065-105">ByFieldsParameterSet (Default)</span></span>
```
Grant-AzDataShareSubscriptionAccess -ResourceGroupName <String> -AccountName <String> [-ShareName <String>]
 -ShareSubscriptionId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0f065-106">ByProviderShareSubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f065-106">ByProviderShareSubscriptionIdParameterSet</span></span>
```
Grant-AzDataShareSubscriptionAccess -ShareSubscriptionId <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f065-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0f065-107">DESCRIPTION</span></span>
<span data-ttu-id="0f065-108">Das Cmdlet **Grant-AzDataShareSubscriptionAccess** gewährt einem Freigabe Abonnement Zugriff auf die Quell Freigabe.</span><span class="sxs-lookup"><span data-stu-id="0f065-108">The **Grant-AzDataShareSubscriptionAccess** cmdlet grants a share subscription access to source share</span></span>

## <span data-ttu-id="0f065-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0f065-109">EXAMPLES</span></span>

### <span data-ttu-id="0f065-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0f065-110">Example 1</span></span>
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

<span data-ttu-id="0f065-111">Gewährt Zugriff auf das von ID 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12 identifizierte Freigabe Abonnement</span><span class="sxs-lookup"><span data-stu-id="0f065-111">Grants access to share subscription identified by id 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12</span></span>

## <span data-ttu-id="0f065-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="0f065-112">PARAMETERS</span></span>

### <span data-ttu-id="0f065-113">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="0f065-113">-AccountName</span></span>
<span data-ttu-id="0f065-114">Name des Azure-Datenfreigabe Kontos</span><span class="sxs-lookup"><span data-stu-id="0f065-114">Azure data share account name</span></span>

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

### <span data-ttu-id="0f065-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f065-115">-DefaultProfile</span></span>
<span data-ttu-id="0f065-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0f065-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f065-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f065-117">-ResourceGroupName</span></span>
<span data-ttu-id="0f065-118">Der Name der Ressourcengruppe des Azure Data Share-Kontos</span><span class="sxs-lookup"><span data-stu-id="0f065-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="0f065-119">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="0f065-119">-ResourceId</span></span>
<span data-ttu-id="0f065-120">Die Ressourcen-ID der Azure-Datenfreigabe</span><span class="sxs-lookup"><span data-stu-id="0f065-120">The resource id of the azure data share</span></span>

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

### <span data-ttu-id="0f065-121">-Freigabename</span><span class="sxs-lookup"><span data-stu-id="0f065-121">-ShareName</span></span>
<span data-ttu-id="0f065-122">Name der Azure-Datenfreigabe</span><span class="sxs-lookup"><span data-stu-id="0f065-122">Azure data share name</span></span>

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

### <span data-ttu-id="0f065-123">-ShareSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0f065-123">-ShareSubscriptionId</span></span>
<span data-ttu-id="0f065-124">Die Freigabe-Abonnement-ID des Anbieter Freigabe-Abonnements</span><span class="sxs-lookup"><span data-stu-id="0f065-124">The share subscription id of the provider share subscription</span></span>

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

### <span data-ttu-id="0f065-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0f065-125">-Confirm</span></span>
<span data-ttu-id="0f065-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0f065-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f065-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f065-127">-WhatIf</span></span>
<span data-ttu-id="0f065-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0f065-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0f065-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0f065-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f065-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f065-130">CommonParameters</span></span>
<span data-ttu-id="0f065-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f065-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f065-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f065-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f065-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0f065-133">INPUTS</span></span>

### <span data-ttu-id="0f065-134">System. String</span><span class="sxs-lookup"><span data-stu-id="0f065-134">System.String</span></span>

## <span data-ttu-id="0f065-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0f065-135">OUTPUTS</span></span>

### <span data-ttu-id="0f065-136">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span><span class="sxs-lookup"><span data-stu-id="0f065-136">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span></span>

## <span data-ttu-id="0f065-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="0f065-137">NOTES</span></span>

## <span data-ttu-id="0f065-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0f065-138">RELATED LINKS</span></span>
