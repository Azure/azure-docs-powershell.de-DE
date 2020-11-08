---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/revoke-azdatasharesubscriptionaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Revoke-AzDataShareSubscriptionAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Revoke-AzDataShareSubscriptionAccess.md
ms.openlocfilehash: 540426cc8612f4cee7364a7875bb9a142bca07ef
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008019"
---
# <span data-ttu-id="1570b-101">Revoke-AzDataShareSubscriptionAccess</span><span class="sxs-lookup"><span data-stu-id="1570b-101">Revoke-AzDataShareSubscriptionAccess</span></span>

## <span data-ttu-id="1570b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1570b-102">SYNOPSIS</span></span>
<span data-ttu-id="1570b-103">Widerrufen des Freigabe Abonnements Zugriff auf die Quell Freigabe</span><span class="sxs-lookup"><span data-stu-id="1570b-103">Revokes share subscription access to source share</span></span>

## <span data-ttu-id="1570b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1570b-104">SYNTAX</span></span>

### <span data-ttu-id="1570b-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="1570b-105">ByFieldsParameterSet (Default)</span></span>
```
Revoke-AzDataShareSubscriptionAccess -ResourceGroupName <String> -AccountName <String> [-ShareName <String>]
 -ShareSubscriptionId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1570b-106">ByProviderShareSubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1570b-106">ByProviderShareSubscriptionIdParameterSet</span></span>
```
Revoke-AzDataShareSubscriptionAccess -ShareSubscriptionId <String> -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1570b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1570b-107">DESCRIPTION</span></span>
<span data-ttu-id="1570b-108">Das Cmdlet **REVOKE-AzDataShareSubscriptionAccess** gewährt einem Freigabe Abonnement Zugriff auf die Quell Freigabe.</span><span class="sxs-lookup"><span data-stu-id="1570b-108">The **Revoke-AzDataShareSubscriptionAccess** cmdlet grants a share subscription access to source share</span></span>

## <span data-ttu-id="1570b-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1570b-109">EXAMPLES</span></span>

### <span data-ttu-id="1570b-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1570b-110">Example 1</span></span>
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

<span data-ttu-id="1570b-111">Widerruf des Zugriffs auf das von ID 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12 identifizierte Freigabe Abonnement</span><span class="sxs-lookup"><span data-stu-id="1570b-111">Revokes access of share subscription identified by id 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12</span></span>

## <span data-ttu-id="1570b-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="1570b-112">PARAMETERS</span></span>

### <span data-ttu-id="1570b-113">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="1570b-113">-AccountName</span></span>
<span data-ttu-id="1570b-114">Name des Azure-Datenfreigabe Kontos</span><span class="sxs-lookup"><span data-stu-id="1570b-114">Azure data share account name</span></span>

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

### <span data-ttu-id="1570b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1570b-115">-AsJob</span></span>
<span data-ttu-id="1570b-116">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="1570b-116">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="1570b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1570b-117">-DefaultProfile</span></span>
<span data-ttu-id="1570b-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1570b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1570b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1570b-119">-ResourceGroupName</span></span>
<span data-ttu-id="1570b-120">Der Name der Ressourcengruppe des Azure Data Share-Kontos</span><span class="sxs-lookup"><span data-stu-id="1570b-120">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="1570b-121">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="1570b-121">-ResourceId</span></span>
<span data-ttu-id="1570b-122">Die Ressourcen-ID der Azure-Datenfreigabe</span><span class="sxs-lookup"><span data-stu-id="1570b-122">The resource id of the azure data share</span></span>

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

### <span data-ttu-id="1570b-123">-Freigabename</span><span class="sxs-lookup"><span data-stu-id="1570b-123">-ShareName</span></span>
<span data-ttu-id="1570b-124">Name der Azure-Datenfreigabe</span><span class="sxs-lookup"><span data-stu-id="1570b-124">Azure data share name</span></span>

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

### <span data-ttu-id="1570b-125">-ShareSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1570b-125">-ShareSubscriptionId</span></span>
<span data-ttu-id="1570b-126">Die Freigabe-Abonnement-ID des Anbieter Freigabe-Abonnements</span><span class="sxs-lookup"><span data-stu-id="1570b-126">The share subscription id of the provider share subscription</span></span>

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

### <span data-ttu-id="1570b-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1570b-127">-Confirm</span></span>
<span data-ttu-id="1570b-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1570b-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1570b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1570b-129">-WhatIf</span></span>
<span data-ttu-id="1570b-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1570b-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1570b-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1570b-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1570b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1570b-132">CommonParameters</span></span>
<span data-ttu-id="1570b-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1570b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1570b-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1570b-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1570b-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1570b-135">INPUTS</span></span>

### <span data-ttu-id="1570b-136">System. String</span><span class="sxs-lookup"><span data-stu-id="1570b-136">System.String</span></span>

## <span data-ttu-id="1570b-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1570b-137">OUTPUTS</span></span>

### <span data-ttu-id="1570b-138">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span><span class="sxs-lookup"><span data-stu-id="1570b-138">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span></span>

## <span data-ttu-id="1570b-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="1570b-139">NOTES</span></span>

## <span data-ttu-id="1570b-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1570b-140">RELATED LINKS</span></span>
