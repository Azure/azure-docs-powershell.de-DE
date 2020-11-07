---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShare.md
ms.openlocfilehash: b16e5a9ff2c6e5a898baf56cf237676665bc12c2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651402"
---
# <span data-ttu-id="4e521-101">Remove-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="4e521-101">Remove-AzDataShare</span></span>

## <span data-ttu-id="4e521-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4e521-102">SYNOPSIS</span></span>
<span data-ttu-id="4e521-103">Entfernt eine Datenfreigabe.</span><span class="sxs-lookup"><span data-stu-id="4e521-103">Removes a data share.</span></span>

## <span data-ttu-id="4e521-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4e521-104">SYNTAX</span></span>

### <span data-ttu-id="4e521-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="4e521-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e521-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4e521-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShare -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e521-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4e521-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShare -InputObject <PSDataShare> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e521-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4e521-108">DESCRIPTION</span></span>
<span data-ttu-id="4e521-109">Das Cmdlet " **Remove-AzDataShare** " entfernt eine Datenfreigabe.</span><span class="sxs-lookup"><span data-stu-id="4e521-109">The **Remove-AzDataShare** cmdlet removes a data share.</span></span>

## <span data-ttu-id="4e521-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4e521-110">EXAMPLES</span></span>

### <span data-ttu-id="4e521-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4e521-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShare -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShare"
Are you sure you want to remove data share "AdsShare"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="4e521-112">Dieser Befehl entfernt die Datenfreigabe mit dem Namen AdsShare aus dem Azure Data Share-Konto WikiAds.</span><span class="sxs-lookup"><span data-stu-id="4e521-112">This commands removes the data share named AdsShare from the azure data share account WikiAds.</span></span> 

## <span data-ttu-id="4e521-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="4e521-113">PARAMETERS</span></span>

### <span data-ttu-id="4e521-114">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="4e521-114">-AccountName</span></span>
<span data-ttu-id="4e521-115">Name des Azure-Datenfreigabe Kontos</span><span class="sxs-lookup"><span data-stu-id="4e521-115">Azure data share account name</span></span>

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

### <span data-ttu-id="4e521-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4e521-116">-AsJob</span></span>
<span data-ttu-id="4e521-117">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="4e521-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="4e521-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e521-118">-DefaultProfile</span></span>
<span data-ttu-id="4e521-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4e521-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e521-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4e521-120">-InputObject</span></span>
<span data-ttu-id="4e521-121">Azure Data Share-Objekt ' ' ' YAML-Typ: PSDataShare-Parameter Sätze: ByObjectParameterSet-Aliase:</span><span class="sxs-lookup"><span data-stu-id="4e521-121">Azure data share object\` \`\`yaml Type: PSDataShare Parameter Sets: ByObjectParameterSet Aliases:</span></span> 

<span data-ttu-id="4e521-122">Erforderlich: true-Position: benannter Standardwert: keine Pipelineeingabe akzeptieren: wahr (ByValue) akzeptiert Platzhalterzeichen: falsch</span><span class="sxs-lookup"><span data-stu-id="4e521-122">Required: True Position: Named Default value: None Accept pipeline input: True (ByValue) Accept wildcard characters: False</span></span>


### <span data-ttu-id="4e521-123">-Name</span><span class="sxs-lookup"><span data-stu-id="4e521-123">-Name</span></span>
<span data-ttu-id="4e521-124">Name der Azure-Datenfreigabe</span><span class="sxs-lookup"><span data-stu-id="4e521-124">Azure data share name</span></span>

<span data-ttu-id="4e521-125">YAML Type: String-Parameter Sätze: ByFieldsParameterSet-Aliase:</span><span class="sxs-lookup"><span data-stu-id="4e521-125">yaml Type: String Parameter Sets: ByFieldsParameterSet Aliases:</span></span> 

<span data-ttu-id="4e521-126">Erforderlich: true-Position: benannter Standardwert: None akzeptiert Pipelineeingabe: false akzeptieren Platzhalterzeichen: falsch</span><span class="sxs-lookup"><span data-stu-id="4e521-126">Required: True Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>


### <span data-ttu-id="4e521-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4e521-127">-PassThru</span></span>
<span data-ttu-id="4e521-128">Objekt zurückgeben (sofern angegeben).</span><span class="sxs-lookup"><span data-stu-id="4e521-128">Return object (if specified).</span></span>

<span data-ttu-id="4e521-129">YAML-Typ: Switchparameter-Parameter Sätze: (alle) Aliase:</span><span class="sxs-lookup"><span data-stu-id="4e521-129">yaml Type: SwitchParameter Parameter Sets: (All) Aliases:</span></span> 

<span data-ttu-id="4e521-130">Erforderlich: falsche Position: benannter Standardwert: keiner akzeptiert Pipelineeingabe: false akzeptieren Platzhalterzeichen: falsch</span><span class="sxs-lookup"><span data-stu-id="4e521-130">Required: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>


### <span data-ttu-id="4e521-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e521-131">-ResourceGroupName</span></span>
<span data-ttu-id="4e521-132">Der Name der Ressourcengruppe des Azure Data Share-Kontos</span><span class="sxs-lookup"><span data-stu-id="4e521-132">The resource group name of the azure data share account</span></span>

<span data-ttu-id="4e521-133">YAML Type: String-Parameter Sätze: ByFieldsParameterSet-Aliase:</span><span class="sxs-lookup"><span data-stu-id="4e521-133">yaml Type: String Parameter Sets: ByFieldsParameterSet Aliases:</span></span> 

<span data-ttu-id="4e521-134">Erforderlich: true-Position: benannter Standardwert: None akzeptiert Pipelineeingabe: false akzeptieren Platzhalterzeichen: falsch</span><span class="sxs-lookup"><span data-stu-id="4e521-134">Required: True Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>


### <span data-ttu-id="4e521-135">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="4e521-135">-ResourceId</span></span>
<span data-ttu-id="4e521-136">Die Ressourcen-ID der Azure-Datenfreigabe</span><span class="sxs-lookup"><span data-stu-id="4e521-136">The resource id of the Azure data share</span></span>

<span data-ttu-id="4e521-137">YAML Type: String-Parameter Sätze: ByResourceIdParameterSet-Aliase:</span><span class="sxs-lookup"><span data-stu-id="4e521-137">yaml Type: String Parameter Sets: ByResourceIdParameterSet Aliases:</span></span> 

<span data-ttu-id="4e521-138">Erforderlich: true-Position: benannter Standardwert: keine Pipelineeingabe akzeptieren: wahr (ByPropertyName) akzeptiert Platzhalterzeichen: falsch</span><span class="sxs-lookup"><span data-stu-id="4e521-138">Required: True Position: Named Default value: None Accept pipeline input: True (ByPropertyName) Accept wildcard characters: False</span></span>


### <span data-ttu-id="4e521-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4e521-139">-Confirm</span></span>
<span data-ttu-id="4e521-140">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4e521-140">Prompts you for confirmation before running the cmdlet.</span></span>

<span data-ttu-id="4e521-141">YAML Type: Switchparameter-Parameter Sätze: (alle) Aliase: CF</span><span class="sxs-lookup"><span data-stu-id="4e521-141">yaml Type: SwitchParameter Parameter Sets: (All) Aliases: cf</span></span>

<span data-ttu-id="4e521-142">Erforderlich: falsche Position: benannter Standardwert: keiner akzeptiert Pipelineeingabe: false akzeptieren Platzhalterzeichen: falsch</span><span class="sxs-lookup"><span data-stu-id="4e521-142">Required: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>


### <span data-ttu-id="4e521-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e521-143">-WhatIf</span></span>
<span data-ttu-id="4e521-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4e521-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e521-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4e521-145">The cmdlet is not run.</span></span>

<span data-ttu-id="4e521-146">YAML Type: Switchparameter-Parameter Sätze: (alle) Aliase: Wi</span><span class="sxs-lookup"><span data-stu-id="4e521-146">yaml Type: SwitchParameter Parameter Sets: (All) Aliases: wi</span></span>

<span data-ttu-id="4e521-147">Erforderlich: falsche Position: benannter Standardwert: keiner akzeptiert Pipelineeingabe: false akzeptieren Platzhalterzeichen: falsch</span><span class="sxs-lookup"><span data-stu-id="4e521-147">Required: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>
```

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

### <span data-ttu-id="4e521-148">-Name</span><span class="sxs-lookup"><span data-stu-id="4e521-148">-Name</span></span>
<span data-ttu-id="4e521-149">Name der Azure-Datenfreigabe</span><span class="sxs-lookup"><span data-stu-id="4e521-149">Azure data share name</span></span>

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

### <span data-ttu-id="4e521-150">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4e521-150">-PassThru</span></span>
<span data-ttu-id="4e521-151">Objekt zurückgeben (sofern angegeben).</span><span class="sxs-lookup"><span data-stu-id="4e521-151">Return object (if specified).</span></span>

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

### <span data-ttu-id="4e521-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e521-152">-ResourceGroupName</span></span>
<span data-ttu-id="4e521-153">Der Name der Ressourcengruppe des Azure Data Share-Kontos</span><span class="sxs-lookup"><span data-stu-id="4e521-153">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="4e521-154">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="4e521-154">-ResourceId</span></span>
<span data-ttu-id="4e521-155">Die Ressourcen-ID der Azure-Datenfreigabe</span><span class="sxs-lookup"><span data-stu-id="4e521-155">The resource id of the Azure data share</span></span>

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

### <span data-ttu-id="4e521-156">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4e521-156">-Confirm</span></span>
<span data-ttu-id="4e521-157">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4e521-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e521-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e521-158">-WhatIf</span></span>
<span data-ttu-id="4e521-159">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4e521-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4e521-160">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4e521-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e521-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e521-161">CommonParameters</span></span>
<span data-ttu-id="4e521-162">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e521-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e521-163">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e521-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e521-164">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4e521-164">INPUTS</span></span>

### <span data-ttu-id="4e521-165">System. String</span><span class="sxs-lookup"><span data-stu-id="4e521-165">System.String</span></span>

### <span data-ttu-id="4e521-166">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="4e521-166">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="4e521-167">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4e521-167">OUTPUTS</span></span>

### <span data-ttu-id="4e521-168">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4e521-168">System.Boolean</span></span>

## <span data-ttu-id="4e521-169">Notizen</span><span class="sxs-lookup"><span data-stu-id="4e521-169">NOTES</span></span>

## <span data-ttu-id="4e521-170">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4e521-170">RELATED LINKS</span></span>
