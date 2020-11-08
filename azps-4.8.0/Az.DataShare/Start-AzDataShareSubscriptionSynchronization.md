---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/start-azdatasharesubscriptionsynchronization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Start-AzDataShareSubscriptionSynchronization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Start-AzDataShareSubscriptionSynchronization.md
ms.openlocfilehash: bbbcab1e4355667681acf1cc09a51ec6d6174103
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174768"
---
# <span data-ttu-id="f5045-101">Start-AzDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="f5045-101">Start-AzDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="f5045-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f5045-102">SYNOPSIS</span></span>
<span data-ttu-id="f5045-103">Initiiert die Synchronisierung für ein Freigabe Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f5045-103">Initiates synchronization for a share subscription.</span></span> <span data-ttu-id="f5045-104">Ein Freigabe Abonnement kann über seine Ressourcen-ID oder seinen Namen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f5045-104">A share subscription can be specified through its resource id or its name.</span></span>

## <span data-ttu-id="f5045-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f5045-105">SYNTAX</span></span>

### <span data-ttu-id="f5045-106">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f5045-106">ByFieldsParameterSet (Default)</span></span>
```
Start-AzDataShareSubscriptionSynchronization -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -SynchronizationMode <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5045-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f5045-107">ByResourceIdParameterSet</span></span>
```
Start-AzDataShareSubscriptionSynchronization -SynchronizationMode <String> -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5045-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f5045-108">ByObjectParameterSet</span></span>
```
Start-AzDataShareSubscriptionSynchronization -InputObject <PSDataShareSubscription> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5045-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f5045-109">DESCRIPTION</span></span>
<span data-ttu-id="f5045-110">Das Cmdlet " **Start-AzDataShareSubscriptionSynchronization** " initiiert die Synchronisierung für ein Freigabe Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f5045-110">The **Start-AzDataShareSubscriptionSynchronization** cmdlet initiates synchronization for a share subscription</span></span>

## <span data-ttu-id="f5045-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f5045-111">EXAMPLES</span></span>

### <span data-ttu-id="f5045-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f5045-112">Example 1</span></span>
```
PS C:\> Start-AzDataShareSubscriptionSynchronization -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -SynchronizationMode Incremental

Confirm
AdsShareSubscription
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

durationMs        : 231869
endTime           : 7/9/2019 11:44:41 PM
message           :
startTime         : 7/9/2019 11:40:53 PM
status            : Succeeded
synchronizationId : 20a4416b-b33b-4539-a908-71dc8ef698fb
```

<span data-ttu-id="f5045-113">Mit diesen Befehlen wird die Synchronisierung für einen sharesubscription mit dem Namen AdsShareSubscription in Konto WikiAds initiiert.</span><span class="sxs-lookup"><span data-stu-id="f5045-113">This commands initiates synchronization for a sharesubscription named AdsShareSubscription in account WikiAds.</span></span> 

## <span data-ttu-id="f5045-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="f5045-114">PARAMETERS</span></span>

### <span data-ttu-id="f5045-115">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="f5045-115">-AccountName</span></span>
<span data-ttu-id="f5045-116">Name des Azure-Datenfreigabe Kontos</span><span class="sxs-lookup"><span data-stu-id="f5045-116">Azure data share account name</span></span>

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

### <span data-ttu-id="f5045-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f5045-117">-AsJob</span></span>
<span data-ttu-id="f5045-118">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="f5045-118">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="f5045-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5045-119">-DefaultProfile</span></span>
<span data-ttu-id="f5045-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f5045-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5045-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f5045-121">-InputObject</span></span>
<span data-ttu-id="f5045-122">Azure Data Share-Abonnementobjekt</span><span class="sxs-lookup"><span data-stu-id="f5045-122">Azure data share subscription object</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f5045-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5045-123">-ResourceGroupName</span></span>
<span data-ttu-id="f5045-124">Der Name der Ressourcengruppe des Azure Data Share-Kontos</span><span class="sxs-lookup"><span data-stu-id="f5045-124">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="f5045-125">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="f5045-125">-ResourceId</span></span>
<span data-ttu-id="f5045-126">Die Ressourcen-ID des Azure Share-Abonnements</span><span class="sxs-lookup"><span data-stu-id="f5045-126">The resource id of the azure share subscription</span></span>

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

### <span data-ttu-id="f5045-127">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="f5045-127">-ShareSubscriptionName</span></span>
<span data-ttu-id="f5045-128">Name des Azure Data Share-Abonnements</span><span class="sxs-lookup"><span data-stu-id="f5045-128">Azure data share subscription name</span></span>

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

### <span data-ttu-id="f5045-129">-SynchronizationMode</span><span class="sxs-lookup"><span data-stu-id="f5045-129">-SynchronizationMode</span></span>
<span data-ttu-id="f5045-130">Synchronisierungsmodus (FullSync oder inkrementell)</span><span class="sxs-lookup"><span data-stu-id="f5045-130">Synchronization mode (FullSync or Incremental)</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5045-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f5045-131">-Confirm</span></span>
<span data-ttu-id="f5045-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f5045-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5045-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5045-133">-WhatIf</span></span>
<span data-ttu-id="f5045-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f5045-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5045-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f5045-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5045-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5045-136">CommonParameters</span></span>
<span data-ttu-id="f5045-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5045-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5045-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f5045-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5045-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f5045-139">INPUTS</span></span>

### <span data-ttu-id="f5045-140">System. String</span><span class="sxs-lookup"><span data-stu-id="f5045-140">System.String</span></span>

### <span data-ttu-id="f5045-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="f5045-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span></span>

## <span data-ttu-id="f5045-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f5045-142">OUTPUTS</span></span>

### <span data-ttu-id="f5045-143">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="f5045-143">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="f5045-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="f5045-144">NOTES</span></span>

## <span data-ttu-id="f5045-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f5045-145">RELATED LINKS</span></span>
