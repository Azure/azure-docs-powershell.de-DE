---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/remove-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShare.md
ms.openlocfilehash: 8a46ecacae8df648ab6400cad25c3ca24b3ee3a8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924979"
---
# <span data-ttu-id="c546f-101">Remove-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="c546f-101">Remove-AzDataShare</span></span>

## <span data-ttu-id="c546f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c546f-102">SYNOPSIS</span></span>
<span data-ttu-id="c546f-103">Entfernt eine Datenfreigabe.</span><span class="sxs-lookup"><span data-stu-id="c546f-103">Removes a data share.</span></span>

## <span data-ttu-id="c546f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c546f-104">SYNTAX</span></span>

### <span data-ttu-id="c546f-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c546f-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c546f-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c546f-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShare -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c546f-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c546f-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShare -InputObject <PSDataShare> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c546f-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c546f-108">DESCRIPTION</span></span>
<span data-ttu-id="c546f-109">Das **Cmdlet Remove-AzDataShare** entfernt eine Datenfreigabe.</span><span class="sxs-lookup"><span data-stu-id="c546f-109">The **Remove-AzDataShare** cmdlet removes a data share.</span></span>

## <span data-ttu-id="c546f-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c546f-110">EXAMPLES</span></span>

### <span data-ttu-id="c546f-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c546f-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShare -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShare"
Are you sure you want to remove data share "AdsShare"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="c546f-112">Mit diesen Befehlen wird die Datenfreigabe mit dem Namen AdsShare aus dem Azure-Datenfreigabekonto WikiAds entfernt.</span><span class="sxs-lookup"><span data-stu-id="c546f-112">This commands removes the data share named AdsShare from the azure data share account WikiAds.</span></span> 

## <span data-ttu-id="c546f-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c546f-113">PARAMETERS</span></span>

### <span data-ttu-id="c546f-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c546f-114">-AccountName</span></span>
<span data-ttu-id="c546f-115">Name des Azure-Datenfreigabekontos</span><span class="sxs-lookup"><span data-stu-id="c546f-115">Azure data share account name</span></span>

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

### <span data-ttu-id="c546f-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c546f-116">-AsJob</span></span>
<span data-ttu-id="c546f-117">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="c546f-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="c546f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c546f-118">-DefaultProfile</span></span>
<span data-ttu-id="c546f-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c546f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c546f-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c546f-120">-InputObject</span></span>
<span data-ttu-id="c546f-121">Azure data share object' ''yaml Type: PSDataShare Parameter Sets: ByObjectParameterSet Aliases:</span><span class="sxs-lookup"><span data-stu-id="c546f-121">Azure data share object\` \`\`yaml Type: PSDataShare Parameter Sets: ByObjectParameterSet Aliases:</span></span> 

<span data-ttu-id="c546f-122">Erforderlich: True Position: Named Default value: None Accept pipeline input: True (ByValue) Accept platzhalter characters: False</span><span class="sxs-lookup"><span data-stu-id="c546f-122">Required: True Position: Named Default value: None Accept pipeline input: True (ByValue) Accept wildcard characters: False</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c546f-123">-Name</span><span class="sxs-lookup"><span data-stu-id="c546f-123">-Name</span></span>
<span data-ttu-id="c546f-124">Name der Azure-Datenfreigabe</span><span class="sxs-lookup"><span data-stu-id="c546f-124">Azure data share name</span></span>

<span data-ttu-id="c546f-125">yaml-Typ: Zeichenfolgenparametersätze: ByFieldsParameterSet-Aliase:</span><span class="sxs-lookup"><span data-stu-id="c546f-125">yaml Type: String Parameter Sets: ByFieldsParameterSet Aliases:</span></span> 

<span data-ttu-id="c546f-126">Erforderlich: True Position: Named Default value: None Accept pipeline input: False Accept platzhalter characters: False</span><span class="sxs-lookup"><span data-stu-id="c546f-126">Required: True Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="c546f-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c546f-127">-PassThru</span></span>
<span data-ttu-id="c546f-128">Rückgabeobjekt (sofern angegeben).</span><span class="sxs-lookup"><span data-stu-id="c546f-128">Return object (if specified).</span></span>

<span data-ttu-id="c546f-129">yaml-Typ: Parametersätze für SwitchParameter: (Alle) Aliase:</span><span class="sxs-lookup"><span data-stu-id="c546f-129">yaml Type: SwitchParameter Parameter Sets: (All) Aliases:</span></span> 

<span data-ttu-id="c546f-130">Erforderlich: False Position: Named Default value: None Accept pipeline input: False Accept platzhalter characters: False</span><span class="sxs-lookup"><span data-stu-id="c546f-130">Required: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="c546f-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c546f-131">-ResourceGroupName</span></span>
<span data-ttu-id="c546f-132">Der Ressourcengruppenname des Azure Data Share-Kontos</span><span class="sxs-lookup"><span data-stu-id="c546f-132">The resource group name of the azure data share account</span></span>

<span data-ttu-id="c546f-133">yaml-Typ: Zeichenfolgenparametersätze: ByFieldsParameterSet-Aliase:</span><span class="sxs-lookup"><span data-stu-id="c546f-133">yaml Type: String Parameter Sets: ByFieldsParameterSet Aliases:</span></span> 

<span data-ttu-id="c546f-134">Erforderlich: True Position: Named Default value: None Accept pipeline input: False Accept platzhalter characters: False</span><span class="sxs-lookup"><span data-stu-id="c546f-134">Required: True Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="c546f-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c546f-135">-ResourceId</span></span>
<span data-ttu-id="c546f-136">Die Ressourcen-ID der Azure-Datenfreigabe</span><span class="sxs-lookup"><span data-stu-id="c546f-136">The resource id of the Azure data share</span></span>

<span data-ttu-id="c546f-137">yaml-Typ: Zeichenfolgenparametersätze: ByResourceIdParameterSet-Aliase:</span><span class="sxs-lookup"><span data-stu-id="c546f-137">yaml Type: String Parameter Sets: ByResourceIdParameterSet Aliases:</span></span> 

<span data-ttu-id="c546f-138">Erforderlich: True Position: Named Default value: None Accept pipeline input: True (ByPropertyName) Accept platzhalter characters: False</span><span class="sxs-lookup"><span data-stu-id="c546f-138">Required: True Position: Named Default value: None Accept pipeline input: True (ByPropertyName) Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="c546f-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c546f-139">-Confirm</span></span>
<span data-ttu-id="c546f-140">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c546f-140">Prompts you for confirmation before running the cmdlet.</span></span>

<span data-ttu-id="c546f-141">yaml Type: SwitchParameter Parameter Sets: (All) Aliase: cf</span><span class="sxs-lookup"><span data-stu-id="c546f-141">yaml Type: SwitchParameter Parameter Sets: (All) Aliases: cf</span></span>

<span data-ttu-id="c546f-142">Erforderlich: False Position: Named Default value: None Accept pipeline input: False Accept platzhalter characters: False</span><span class="sxs-lookup"><span data-stu-id="c546f-142">Required: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="c546f-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c546f-143">-WhatIf</span></span>
<span data-ttu-id="c546f-144">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c546f-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c546f-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c546f-145">The cmdlet is not run.</span></span>

<span data-ttu-id="c546f-146">yaml Type: SwitchParameter Parameter Sets: (All) Aliase: wi</span><span class="sxs-lookup"><span data-stu-id="c546f-146">yaml Type: SwitchParameter Parameter Sets: (All) Aliases: wi</span></span>

<span data-ttu-id="c546f-147">Erforderlich: False Position: Named Default value: None Accept pipeline input: False Accept platzhalter characters: False</span><span class="sxs-lookup"><span data-stu-id="c546f-147">Required: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>




<span data-ttu-id="c546f-148">yaml-Typ: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare-Parametersätze: ByObjectParameterSet-Aliase:</span><span class="sxs-lookup"><span data-stu-id="c546f-148">yaml Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare Parameter Sets: ByObjectParameterSet Aliases:</span></span>

<span data-ttu-id="c546f-149">Erforderlich: True Position: Named Default value: None Accept pipeline input: True (ByValue) Accept platzhalter characters: False</span><span class="sxs-lookup"><span data-stu-id="c546f-149">Required: True Position: Named Default value: None Accept pipeline input: True (ByValue) Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="c546f-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c546f-150">CommonParameters</span></span>
<span data-ttu-id="c546f-151">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c546f-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c546f-152">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c546f-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c546f-153">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c546f-153">INPUTS</span></span>

### <span data-ttu-id="c546f-154">System.String</span><span class="sxs-lookup"><span data-stu-id="c546f-154">System.String</span></span>

### <span data-ttu-id="c546f-155">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="c546f-155">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="c546f-156">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c546f-156">OUTPUTS</span></span>

### <span data-ttu-id="c546f-157">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c546f-157">System.Boolean</span></span>

## <span data-ttu-id="c546f-158">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c546f-158">NOTES</span></span>

## <span data-ttu-id="c546f-159">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c546f-159">RELATED LINKS</span></span>
