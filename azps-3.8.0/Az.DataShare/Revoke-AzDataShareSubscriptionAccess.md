---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/revoke-azdatasharesubscriptionaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Revoke-AzDataShareSubscriptionAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Revoke-AzDataShareSubscriptionAccess.md
ms.openlocfilehash: 6ac4fdbc119c5cd6639e9b688d60e158eea2a62f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004625"
---
# <span data-ttu-id="894c4-101">Revoke-AzDataShareSubscriptionAccess</span><span class="sxs-lookup"><span data-stu-id="894c4-101">Revoke-AzDataShareSubscriptionAccess</span></span>

## <span data-ttu-id="894c4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="894c4-102">SYNOPSIS</span></span>
<span data-ttu-id="894c4-103">Widerrufen des Freigabe Abonnements Zugriff auf die Quell Freigabe</span><span class="sxs-lookup"><span data-stu-id="894c4-103">Revokes share subscription access to source share</span></span>

## <span data-ttu-id="894c4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="894c4-104">SYNTAX</span></span>

### <span data-ttu-id="894c4-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="894c4-105">ByFieldsParameterSet (Default)</span></span>
```
Revoke-AzDataShareSubscriptionAccess -ResourceGroupName <String> -AccountName <String> [-ShareName <String>]
 -ShareSubscriptionId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="894c4-106">ByProviderShareSubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="894c4-106">ByProviderShareSubscriptionIdParameterSet</span></span>
```
Revoke-AzDataShareSubscriptionAccess -ShareSubscriptionId <String> -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="894c4-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="894c4-107">DESCRIPTION</span></span>
<span data-ttu-id="894c4-108">Das Cmdlet **REVOKE-AzDataShareSubscriptionAccess** gewährt einem Freigabe Abonnement Zugriff auf die Quell Freigabe.</span><span class="sxs-lookup"><span data-stu-id="894c4-108">The **Revoke-AzDataShareSubscriptionAccess** cmdlet grants a share subscription access to source share</span></span>

## <span data-ttu-id="894c4-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="894c4-109">EXAMPLES</span></span>

### <span data-ttu-id="894c4-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="894c4-110">Example 1</span></span>
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

<span data-ttu-id="894c4-111">Widerruf des Zugriffs auf das von ID 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12 identifizierte Freigabe Abonnement</span><span class="sxs-lookup"><span data-stu-id="894c4-111">Revokes access of share subscription identified by id 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12</span></span>

## <span data-ttu-id="894c4-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="894c4-112">PARAMETERS</span></span>

### <span data-ttu-id="894c4-113">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="894c4-113">-AccountName</span></span>
<span data-ttu-id="894c4-114">Name des Azure-Datenfreigabe Kontos</span><span class="sxs-lookup"><span data-stu-id="894c4-114">Azure data share account name</span></span>

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

### <span data-ttu-id="894c4-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="894c4-115">-AsJob</span></span>
<span data-ttu-id="894c4-116">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="894c4-116">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="894c4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="894c4-117">-DefaultProfile</span></span>
<span data-ttu-id="894c4-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="894c4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="894c4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="894c4-119">-ResourceGroupName</span></span>
<span data-ttu-id="894c4-120">Der Name der Ressourcengruppe des Azure Data Share-Kontos</span><span class="sxs-lookup"><span data-stu-id="894c4-120">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="894c4-121">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="894c4-121">-ResourceId</span></span>
<span data-ttu-id="894c4-122">Die Ressourcen-ID der Azure-Datenfreigabe</span><span class="sxs-lookup"><span data-stu-id="894c4-122">The resource id of the azure data share</span></span>

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

### <span data-ttu-id="894c4-123">-Freigabename</span><span class="sxs-lookup"><span data-stu-id="894c4-123">-ShareName</span></span>
<span data-ttu-id="894c4-124">Name der Azure-Datenfreigabe</span><span class="sxs-lookup"><span data-stu-id="894c4-124">Azure data share name</span></span>

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

### <span data-ttu-id="894c4-125">-ShareSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="894c4-125">-ShareSubscriptionId</span></span>
<span data-ttu-id="894c4-126">Die Freigabe-Abonnement-ID des Anbieter Freigabe-Abonnements</span><span class="sxs-lookup"><span data-stu-id="894c4-126">The share subscription id of the provider share subscription</span></span>

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

### <span data-ttu-id="894c4-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="894c4-127">-Confirm</span></span>
<span data-ttu-id="894c4-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="894c4-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="894c4-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="894c4-129">-WhatIf</span></span>
<span data-ttu-id="894c4-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="894c4-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="894c4-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="894c4-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="894c4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="894c4-132">CommonParameters</span></span>
<span data-ttu-id="894c4-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="894c4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="894c4-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="894c4-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="894c4-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="894c4-135">INPUTS</span></span>

### <span data-ttu-id="894c4-136">System. String</span><span class="sxs-lookup"><span data-stu-id="894c4-136">System.String</span></span>

## <span data-ttu-id="894c4-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="894c4-137">OUTPUTS</span></span>

### <span data-ttu-id="894c4-138">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span><span class="sxs-lookup"><span data-stu-id="894c4-138">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span></span>

## <span data-ttu-id="894c4-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="894c4-139">NOTES</span></span>

## <span data-ttu-id="894c4-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="894c4-140">RELATED LINKS</span></span>
