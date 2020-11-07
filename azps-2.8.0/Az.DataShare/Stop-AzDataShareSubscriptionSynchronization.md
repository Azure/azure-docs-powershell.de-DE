---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/stop-azdatasharesubscriptionsynchronization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Stop-AzDataShareSubscriptionSynchronization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Stop-AzDataShareSubscriptionSynchronization.md
ms.openlocfilehash: 01ca3c42db57760f23e49f93fc7e4d533b4047b3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651380"
---
# <span data-ttu-id="1ae81-101">Stop-AzDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="1ae81-101">Stop-AzDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="1ae81-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1ae81-102">SYNOPSIS</span></span>
<span data-ttu-id="1ae81-103">Beendet die laufende Synchronisierung für ein Freigabe Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1ae81-103">Stops ongoing synchronization for a share subscription.</span></span> <span data-ttu-id="1ae81-104">Ein Freigabe Abonnement kann über seine Ressourcen-ID oder seinen Namen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="1ae81-104">A share subscription can be specified through its resource id or its name.</span></span>

## <span data-ttu-id="1ae81-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1ae81-105">SYNTAX</span></span>

### <span data-ttu-id="1ae81-106">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="1ae81-106">ByFieldsParameterSet (Default)</span></span>
```
Stop-AzDataShareSubscriptionSynchronization -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -SynchronizationId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ae81-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ae81-107">ByResourceIdParameterSet</span></span>
```
Stop-AzDataShareSubscriptionSynchronization -SynchronizationId <String> -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ae81-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ae81-108">ByObjectParameterSet</span></span>
```
Stop-AzDataShareSubscriptionSynchronization -InputObject <PSDataShareSubscription> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ae81-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1ae81-109">DESCRIPTION</span></span>
<span data-ttu-id="1ae81-110">Das Cmdlet " **Stop-AzDataShareSubscriptionSynchronization** " beendet die laufende Synchronisierung für ein Freigabe Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1ae81-110">The **Stop-AzDataShareSubscriptionSynchronization** cmdlet stops ongoing synchronization for a share subscription</span></span>

## <span data-ttu-id="1ae81-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1ae81-111">EXAMPLES</span></span>

### <span data-ttu-id="1ae81-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1ae81-112">Example 1</span></span>
```
PS C:\> Stop-AzDataShareSubscriptionSynchronization -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -SynchronizationId 20a4416b-b33b-4539-a908-71dc8ef698fb

Confirm
AdsShareSubscription
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

durationMs        : 231869
endTime           : 
message           :
startTime         : 7/9/2019 11:40:53 PM
status            : Canceled
synchronizationId : 20a4416b-b33b-4539-a908-71dc8ef698fb
```

<span data-ttu-id="1ae81-113">Beendet die laufende Synchronisierung, die durch ID-20a4416b-b33b-4539-a908-71dc8ef698fb identifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="1ae81-113">Stops ongoing synchronization identified by id - 20a4416b-b33b-4539-a908-71dc8ef698fb</span></span>

## <span data-ttu-id="1ae81-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="1ae81-114">PARAMETERS</span></span>

### <span data-ttu-id="1ae81-115">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="1ae81-115">-AccountName</span></span>
<span data-ttu-id="1ae81-116">Name des Azure-Datenfreigabe Kontos</span><span class="sxs-lookup"><span data-stu-id="1ae81-116">Azure data share account name</span></span>

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

### <span data-ttu-id="1ae81-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1ae81-117">-AsJob</span></span>
<span data-ttu-id="1ae81-118">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="1ae81-118">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="1ae81-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ae81-119">-DefaultProfile</span></span>
<span data-ttu-id="1ae81-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1ae81-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ae81-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1ae81-121">-InputObject</span></span>
<span data-ttu-id="1ae81-122">Azure Data Share-Abonnementobjekt</span><span class="sxs-lookup"><span data-stu-id="1ae81-122">Azure data share subscription object</span></span>


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

### <span data-ttu-id="1ae81-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ae81-123">-ResourceGroupName</span></span>
<span data-ttu-id="1ae81-124">Der Name der Ressourcengruppe des Azure Data Share-Kontos</span><span class="sxs-lookup"><span data-stu-id="1ae81-124">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="1ae81-125">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="1ae81-125">-ResourceId</span></span>
<span data-ttu-id="1ae81-126">Die Ressourcen-ID des Azure Share-Abonnements</span><span class="sxs-lookup"><span data-stu-id="1ae81-126">The resource id of the azure share subscription</span></span>

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

### <span data-ttu-id="1ae81-127">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="1ae81-127">-ShareSubscriptionName</span></span>
<span data-ttu-id="1ae81-128">Name des Azure Data Share-Abonnements</span><span class="sxs-lookup"><span data-stu-id="1ae81-128">Azure data share subscription name</span></span>

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

### <span data-ttu-id="1ae81-129">-Synchronisierungs-Nr</span><span class="sxs-lookup"><span data-stu-id="1ae81-129">-SynchronizationId</span></span>
<span data-ttu-id="1ae81-130">Synchronisierungs-ID, die angehalten werden muss</span><span class="sxs-lookup"><span data-stu-id="1ae81-130">Synchronization id that needs to be stopped</span></span>

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

### <span data-ttu-id="1ae81-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1ae81-131">-Confirm</span></span>
<span data-ttu-id="1ae81-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1ae81-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ae81-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ae81-133">-WhatIf</span></span>
<span data-ttu-id="1ae81-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1ae81-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ae81-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1ae81-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ae81-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ae81-136">CommonParameters</span></span>
<span data-ttu-id="1ae81-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ae81-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ae81-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ae81-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ae81-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1ae81-139">INPUTS</span></span>

### <span data-ttu-id="1ae81-140">System. String</span><span class="sxs-lookup"><span data-stu-id="1ae81-140">System.String</span></span>

### <span data-ttu-id="1ae81-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="1ae81-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span></span>

## <span data-ttu-id="1ae81-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1ae81-142">OUTPUTS</span></span>

### <span data-ttu-id="1ae81-143">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="1ae81-143">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="1ae81-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="1ae81-144">NOTES</span></span>

## <span data-ttu-id="1ae81-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1ae81-145">RELATED LINKS</span></span>
