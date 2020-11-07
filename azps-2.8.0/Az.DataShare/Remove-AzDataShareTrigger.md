---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareTrigger.md
ms.openlocfilehash: a1ec489b91d2d510c16709fa0923117bbbaa804a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651386"
---
# <span data-ttu-id="03d1f-101">Remove-AzDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="03d1f-101">Remove-AzDataShareTrigger</span></span>

## <span data-ttu-id="03d1f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="03d1f-102">SYNOPSIS</span></span>
<span data-ttu-id="03d1f-103">entfernt einen Trigger</span><span class="sxs-lookup"><span data-stu-id="03d1f-103">removes a trigger</span></span>

## <span data-ttu-id="03d1f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="03d1f-104">SYNTAX</span></span>

### <span data-ttu-id="03d1f-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="03d1f-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareTrigger -ResourceGroupName <String> -AccountName <String> [-ShareSubscriptionName <String>]
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="03d1f-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="03d1f-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareTrigger -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03d1f-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="03d1f-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareTrigger -InputObject <PSDataShareTrigger> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03d1f-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="03d1f-108">DESCRIPTION</span></span>
<span data-ttu-id="03d1f-109">Das Cmdlet " **Remove-AzDataShareTrigger** " entfernt einen DataShare-Trigger.</span><span class="sxs-lookup"><span data-stu-id="03d1f-109">The **Remove-AzDataShareTrigger** cmdlet removes a datashare trigger</span></span>

## <span data-ttu-id="03d1f-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="03d1f-110">EXAMPLES</span></span>

### <span data-ttu-id="03d1f-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="03d1f-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareTrigger -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -Name "AdsTrigger"

Are you sure you want to remove trigger "AdsTrigger"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="03d1f-112">Dieser Befehl entfernt einen Trigger mit dem Namen AdsTrigger aus der Freigabe Abonnement-AdsShareSubscription.</span><span class="sxs-lookup"><span data-stu-id="03d1f-112">This commands removes a trigger named AdsTrigger from share subscription AdsShareSubscription.</span></span> 

## <span data-ttu-id="03d1f-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="03d1f-113">PARAMETERS</span></span>

### <span data-ttu-id="03d1f-114">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="03d1f-114">-AccountName</span></span>
<span data-ttu-id="03d1f-115">Name des Azure-Datenfreigabe Kontos</span><span class="sxs-lookup"><span data-stu-id="03d1f-115">Azure data share account name</span></span>

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

### <span data-ttu-id="03d1f-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="03d1f-116">-AsJob</span></span>
<span data-ttu-id="03d1f-117">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="03d1f-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="03d1f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03d1f-118">-DefaultProfile</span></span>
<span data-ttu-id="03d1f-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="03d1f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03d1f-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="03d1f-120">-InputObject</span></span>
<span data-ttu-id="03d1f-121">Azure Data Share Trigger-Objekt</span><span class="sxs-lookup"><span data-stu-id="03d1f-121">Azure data share trigger object</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="03d1f-122">-Name</span><span class="sxs-lookup"><span data-stu-id="03d1f-122">-Name</span></span>
<span data-ttu-id="03d1f-123">Name des Azure Data Freigabe-Triggers</span><span class="sxs-lookup"><span data-stu-id="03d1f-123">Azure data share trigger name</span></span>

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

### <span data-ttu-id="03d1f-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="03d1f-124">-PassThru</span></span>
<span data-ttu-id="03d1f-125">Objekt zurückgeben (sofern angegeben).</span><span class="sxs-lookup"><span data-stu-id="03d1f-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="03d1f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03d1f-126">-ResourceGroupName</span></span>
<span data-ttu-id="03d1f-127">Der Name der Ressourcengruppe des Azure Data Share-Kontos</span><span class="sxs-lookup"><span data-stu-id="03d1f-127">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="03d1f-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="03d1f-128">-ResourceId</span></span>
<span data-ttu-id="03d1f-129">Die Ressourcen-ID des Azure Data Freigabe-Triggers</span><span class="sxs-lookup"><span data-stu-id="03d1f-129">The resource id of azure data share trigger</span></span>

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

### <span data-ttu-id="03d1f-130">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="03d1f-130">-ShareSubscriptionName</span></span>
<span data-ttu-id="03d1f-131">Name des Azure Data Share-Abonnements</span><span class="sxs-lookup"><span data-stu-id="03d1f-131">Azure data share subscription name</span></span>

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

### <span data-ttu-id="03d1f-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="03d1f-132">-Confirm</span></span>
<span data-ttu-id="03d1f-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="03d1f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03d1f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03d1f-134">-WhatIf</span></span>
<span data-ttu-id="03d1f-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="03d1f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03d1f-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="03d1f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03d1f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03d1f-137">CommonParameters</span></span>
<span data-ttu-id="03d1f-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03d1f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03d1f-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03d1f-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03d1f-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="03d1f-140">INPUTS</span></span>

### <span data-ttu-id="03d1f-141">System. String</span><span class="sxs-lookup"><span data-stu-id="03d1f-141">System.String</span></span>

### <span data-ttu-id="03d1f-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="03d1f-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span></span>

## <span data-ttu-id="03d1f-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="03d1f-143">OUTPUTS</span></span>

### <span data-ttu-id="03d1f-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="03d1f-144">System.Boolean</span></span>

## <span data-ttu-id="03d1f-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="03d1f-145">NOTES</span></span>

## <span data-ttu-id="03d1f-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="03d1f-146">RELATED LINKS</span></span>
