---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharedatasetmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSetMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSetMapping.md
ms.openlocfilehash: 16b212a0c5549f74b56e8c80be8d949a025ecb24
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008028"
---
# <span data-ttu-id="5bcea-101">Remove-AzDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="5bcea-101">Remove-AzDataShareDataSetMapping</span></span>

## <span data-ttu-id="5bcea-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5bcea-102">SYNOPSIS</span></span>
<span data-ttu-id="5bcea-103">Entfernt eine Daten satzzuordnung</span><span class="sxs-lookup"><span data-stu-id="5bcea-103">Removes a dataset mapping</span></span>

## <span data-ttu-id="5bcea-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5bcea-104">SYNTAX</span></span>

### <span data-ttu-id="5bcea-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="5bcea-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5bcea-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5bcea-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareDataSetMapping -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5bcea-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5bcea-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareDataSetMapping -InputObject <PSDataShareDataSetMapping> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5bcea-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5bcea-108">DESCRIPTION</span></span>
<span data-ttu-id="5bcea-109">Das Cmdlet **Remove-AzDataShareDataSetMapping** entfernt eine DataSet-Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="5bcea-109">The **Remove-AzDataShareDataSetMapping** cmdlet removes a dataset mappings.</span></span>

## <span data-ttu-id="5bcea-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5bcea-110">EXAMPLES</span></span>

### <span data-ttu-id="5bcea-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5bcea-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareDataSetMapping -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -Name "DSM"
Are you sure you want to remove dataset mapping "DSM"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="5bcea-112">Mit diesen Befehlen wird das DataSet DSM aus sharesubscription WikiAds entfernt.</span><span class="sxs-lookup"><span data-stu-id="5bcea-112">This commands removes the dataset named DSM from sharesubscription WikiAds.</span></span> 

## <span data-ttu-id="5bcea-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="5bcea-113">PARAMETERS</span></span>

### <span data-ttu-id="5bcea-114">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="5bcea-114">-AccountName</span></span>
<span data-ttu-id="5bcea-115">Name des Azure-Datenfreigabe Kontos</span><span class="sxs-lookup"><span data-stu-id="5bcea-115">Azure data share account name</span></span>

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

### <span data-ttu-id="5bcea-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bcea-116">-DefaultProfile</span></span>
<span data-ttu-id="5bcea-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5bcea-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5bcea-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5bcea-118">-InputObject</span></span>
<span data-ttu-id="5bcea-119">Das Azure-Daten Satz-Zuordnungsobjekt</span><span class="sxs-lookup"><span data-stu-id="5bcea-119">The azure data set mapping object</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5bcea-120">-Name</span><span class="sxs-lookup"><span data-stu-id="5bcea-120">-Name</span></span>
<span data-ttu-id="5bcea-121">Name der Azure-Daten satzzuordnung</span><span class="sxs-lookup"><span data-stu-id="5bcea-121">Azure data set mapping name</span></span>

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

### <span data-ttu-id="5bcea-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5bcea-122">-PassThru</span></span>
<span data-ttu-id="5bcea-123">Objekt zurückgeben (sofern angegeben).</span><span class="sxs-lookup"><span data-stu-id="5bcea-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="5bcea-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bcea-124">-ResourceGroupName</span></span>
<span data-ttu-id="5bcea-125">Der Name der Ressourcengruppe des Azure Data Share-Kontos</span><span class="sxs-lookup"><span data-stu-id="5bcea-125">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="5bcea-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="5bcea-126">-ResourceId</span></span>
<span data-ttu-id="5bcea-127">Die Ressourcen-ID der Azure-Daten satzzuordnung</span><span class="sxs-lookup"><span data-stu-id="5bcea-127">The resource id of the azure data set mapping</span></span>

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

### <span data-ttu-id="5bcea-128">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="5bcea-128">-ShareSubscriptionName</span></span>
<span data-ttu-id="5bcea-129">Name des Azure Data Share-Abonnements</span><span class="sxs-lookup"><span data-stu-id="5bcea-129">Azure data share subscription name</span></span>

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

### <span data-ttu-id="5bcea-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5bcea-130">-Confirm</span></span>
<span data-ttu-id="5bcea-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5bcea-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5bcea-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5bcea-132">-WhatIf</span></span>
<span data-ttu-id="5bcea-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5bcea-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5bcea-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5bcea-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5bcea-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bcea-135">CommonParameters</span></span>
<span data-ttu-id="5bcea-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5bcea-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bcea-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5bcea-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bcea-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5bcea-138">INPUTS</span></span>

### <span data-ttu-id="5bcea-139">System. String</span><span class="sxs-lookup"><span data-stu-id="5bcea-139">System.String</span></span>

### <span data-ttu-id="5bcea-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="5bcea-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span></span>

## <span data-ttu-id="5bcea-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5bcea-141">OUTPUTS</span></span>

### <span data-ttu-id="5bcea-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5bcea-142">System.Boolean</span></span>

## <span data-ttu-id="5bcea-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="5bcea-143">NOTES</span></span>

## <span data-ttu-id="5bcea-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5bcea-144">RELATED LINKS</span></span>
