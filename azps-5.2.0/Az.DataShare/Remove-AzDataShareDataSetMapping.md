---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharedatasetmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSetMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSetMapping.md
ms.openlocfilehash: 16b212a0c5549f74b56e8c80be8d949a025ecb24
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98294275"
---
# <span data-ttu-id="468fd-101">Remove-AzDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="468fd-101">Remove-AzDataShareDataSetMapping</span></span>

## <span data-ttu-id="468fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="468fd-102">SYNOPSIS</span></span>
<span data-ttu-id="468fd-103">Entfernt eine Datasetzuordnung</span><span class="sxs-lookup"><span data-stu-id="468fd-103">Removes a dataset mapping</span></span>

## <span data-ttu-id="468fd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="468fd-104">SYNTAX</span></span>

### <span data-ttu-id="468fd-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="468fd-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="468fd-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="468fd-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareDataSetMapping -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="468fd-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="468fd-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareDataSetMapping -InputObject <PSDataShareDataSetMapping> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="468fd-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="468fd-108">DESCRIPTION</span></span>
<span data-ttu-id="468fd-109">Das **Cmdlet "Remove-AzDataShareDataSetMapping"** entfernt Datasetzuordnungen.</span><span class="sxs-lookup"><span data-stu-id="468fd-109">The **Remove-AzDataShareDataSetMapping** cmdlet removes a dataset mappings.</span></span>

## <span data-ttu-id="468fd-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="468fd-110">EXAMPLES</span></span>

### <span data-ttu-id="468fd-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="468fd-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareDataSetMapping -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -Name "DSM"
Are you sure you want to remove dataset mapping "DSM"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="468fd-112">Mit diesen Befehlen wird das Dataset namens DSM aus sharesubscription WikiAds entfernt.</span><span class="sxs-lookup"><span data-stu-id="468fd-112">This commands removes the dataset named DSM from sharesubscription WikiAds.</span></span> 

## <span data-ttu-id="468fd-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="468fd-113">PARAMETERS</span></span>

### <span data-ttu-id="468fd-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="468fd-114">-AccountName</span></span>
<span data-ttu-id="468fd-115">Name des Azure-Datenfreigabekontos</span><span class="sxs-lookup"><span data-stu-id="468fd-115">Azure data share account name</span></span>

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

### <span data-ttu-id="468fd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="468fd-116">-DefaultProfile</span></span>
<span data-ttu-id="468fd-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="468fd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="468fd-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="468fd-118">-InputObject</span></span>
<span data-ttu-id="468fd-119">Das Zuordnungsobjekt für azure-Datensets</span><span class="sxs-lookup"><span data-stu-id="468fd-119">The azure data set mapping object</span></span>


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

### <span data-ttu-id="468fd-120">-Name</span><span class="sxs-lookup"><span data-stu-id="468fd-120">-Name</span></span>
<span data-ttu-id="468fd-121">Name der Zuordnung von Azure-Datensets</span><span class="sxs-lookup"><span data-stu-id="468fd-121">Azure data set mapping name</span></span>

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

### <span data-ttu-id="468fd-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="468fd-122">-PassThru</span></span>
<span data-ttu-id="468fd-123">Rückgabeobjekt (sofern angegeben)</span><span class="sxs-lookup"><span data-stu-id="468fd-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="468fd-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="468fd-124">-ResourceGroupName</span></span>
<span data-ttu-id="468fd-125">Der Ressourcengruppenname des Azure Data Share-Kontos</span><span class="sxs-lookup"><span data-stu-id="468fd-125">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="468fd-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="468fd-126">-ResourceId</span></span>
<span data-ttu-id="468fd-127">Die Ressourcen-ID der Azure-Datensetzuordnung</span><span class="sxs-lookup"><span data-stu-id="468fd-127">The resource id of the azure data set mapping</span></span>

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

### <span data-ttu-id="468fd-128">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="468fd-128">-ShareSubscriptionName</span></span>
<span data-ttu-id="468fd-129">Name des Azure Data Share-Abonnements</span><span class="sxs-lookup"><span data-stu-id="468fd-129">Azure data share subscription name</span></span>

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

### <span data-ttu-id="468fd-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="468fd-130">-Confirm</span></span>
<span data-ttu-id="468fd-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="468fd-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="468fd-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="468fd-132">-WhatIf</span></span>
<span data-ttu-id="468fd-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="468fd-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="468fd-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="468fd-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="468fd-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="468fd-135">CommonParameters</span></span>
<span data-ttu-id="468fd-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="468fd-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="468fd-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="468fd-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="468fd-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="468fd-138">INPUTS</span></span>

### <span data-ttu-id="468fd-139">System.String</span><span class="sxs-lookup"><span data-stu-id="468fd-139">System.String</span></span>

### <span data-ttu-id="468fd-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="468fd-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span></span>

## <span data-ttu-id="468fd-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="468fd-141">OUTPUTS</span></span>

### <span data-ttu-id="468fd-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="468fd-142">System.Boolean</span></span>

## <span data-ttu-id="468fd-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="468fd-143">NOTES</span></span>

## <span data-ttu-id="468fd-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="468fd-144">RELATED LINKS</span></span>
