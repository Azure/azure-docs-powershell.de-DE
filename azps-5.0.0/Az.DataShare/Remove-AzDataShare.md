---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShare.md
ms.openlocfilehash: 2679a3f63be3b7332020354e325e33573911334b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297418"
---
# <span data-ttu-id="0fbdc-101">Remove-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="0fbdc-101">Remove-AzDataShare</span></span>

## <span data-ttu-id="0fbdc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0fbdc-102">SYNOPSIS</span></span>
<span data-ttu-id="0fbdc-103">Entfernt eine Datenfreigabe.</span><span class="sxs-lookup"><span data-stu-id="0fbdc-103">Removes a data share.</span></span>

## <span data-ttu-id="0fbdc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0fbdc-104">SYNTAX</span></span>

### <span data-ttu-id="0fbdc-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="0fbdc-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0fbdc-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0fbdc-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShare -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0fbdc-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0fbdc-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShare -InputObject <PSDataShare> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0fbdc-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0fbdc-108">DESCRIPTION</span></span>
<span data-ttu-id="0fbdc-109">Das Cmdlet " **Remove-AzDataShare** " entfernt eine Datenfreigabe.</span><span class="sxs-lookup"><span data-stu-id="0fbdc-109">The **Remove-AzDataShare** cmdlet removes a data share.</span></span>

## <span data-ttu-id="0fbdc-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0fbdc-110">EXAMPLES</span></span>

### <span data-ttu-id="0fbdc-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0fbdc-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShare -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShare"
Are you sure you want to remove data share "AdsShare"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="0fbdc-112">Dieser Befehl entfernt die Datenfreigabe mit dem Namen AdsShare aus dem Azure Data Share-Konto WikiAds.</span><span class="sxs-lookup"><span data-stu-id="0fbdc-112">This commands removes the data share named AdsShare from the azure data share account WikiAds.</span></span> 

## <span data-ttu-id="0fbdc-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="0fbdc-113">PARAMETERS</span></span>

### <span data-ttu-id="0fbdc-114">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="0fbdc-114">-AccountName</span></span>
<span data-ttu-id="0fbdc-115">Name des Azure-Datenfreigabe Kontos</span><span class="sxs-lookup"><span data-stu-id="0fbdc-115">Azure data share account name</span></span>

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

### <span data-ttu-id="0fbdc-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0fbdc-116">-AsJob</span></span>
<span data-ttu-id="0fbdc-117">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="0fbdc-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="0fbdc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fbdc-118">-DefaultProfile</span></span>
<span data-ttu-id="0fbdc-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0fbdc-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0fbdc-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0fbdc-120">-InputObject</span></span>
<span data-ttu-id="0fbdc-121">Azure Data Share-Objekt ' ' ' YAML-Typ: PSDataShare-Parameter Sätze: ByObjectParameterSet-Aliase:</span><span class="sxs-lookup"><span data-stu-id="0fbdc-121">Azure data share object\` \`\`yaml Type: PSDataShare Parameter Sets: ByObjectParameterSet Aliases:</span></span> 

<span data-ttu-id="0fbdc-122">Erforderlich: true-Position: benannter Standardwert: keine Pipelineeingabe akzeptieren: wahr (ByValue) akzeptiert Platzhalterzeichen: falsch</span><span class="sxs-lookup"><span data-stu-id="0fbdc-122">Required: True Position: Named Default value: None Accept pipeline input: True (ByValue) Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="0fbdc-123">-Name</span><span class="sxs-lookup"><span data-stu-id="0fbdc-123">-Name</span></span>
<span data-ttu-id="0fbdc-124">Name der Azure-Datenfreigabe</span><span class="sxs-lookup"><span data-stu-id="0fbdc-124">Azure data share name</span></span>

<span data-ttu-id="0fbdc-125">YAML Type: String-Parameter Sätze: ByFieldsParameterSet-Aliase:</span><span class="sxs-lookup"><span data-stu-id="0fbdc-125">yaml Type: String Parameter Sets: ByFieldsParameterSet Aliases:</span></span> 

<span data-ttu-id="0fbdc-126">Erforderlich: true-Position: benannter Standardwert: None akzeptiert Pipelineeingabe: false akzeptieren Platzhalterzeichen: falsch</span><span class="sxs-lookup"><span data-stu-id="0fbdc-126">Required: True Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="0fbdc-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0fbdc-127">-PassThru</span></span>
<span data-ttu-id="0fbdc-128">Objekt zurückgeben (sofern angegeben).</span><span class="sxs-lookup"><span data-stu-id="0fbdc-128">Return object (if specified).</span></span>

<span data-ttu-id="0fbdc-129">YAML-Typ: Switchparameter-Parameter Sätze: (alle) Aliase:</span><span class="sxs-lookup"><span data-stu-id="0fbdc-129">yaml Type: SwitchParameter Parameter Sets: (All) Aliases:</span></span> 

<span data-ttu-id="0fbdc-130">Erforderlich: falsche Position: benannter Standardwert: keiner akzeptiert Pipelineeingabe: false akzeptieren Platzhalterzeichen: falsch</span><span class="sxs-lookup"><span data-stu-id="0fbdc-130">Required: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="0fbdc-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fbdc-131">-ResourceGroupName</span></span>
<span data-ttu-id="0fbdc-132">Der Name der Ressourcengruppe des Azure Data Share-Kontos</span><span class="sxs-lookup"><span data-stu-id="0fbdc-132">The resource group name of the azure data share account</span></span>

<span data-ttu-id="0fbdc-133">YAML Type: String-Parameter Sätze: ByFieldsParameterSet-Aliase:</span><span class="sxs-lookup"><span data-stu-id="0fbdc-133">yaml Type: String Parameter Sets: ByFieldsParameterSet Aliases:</span></span> 

<span data-ttu-id="0fbdc-134">Erforderlich: true-Position: benannter Standardwert: None akzeptiert Pipelineeingabe: false akzeptieren Platzhalterzeichen: falsch</span><span class="sxs-lookup"><span data-stu-id="0fbdc-134">Required: True Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="0fbdc-135">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="0fbdc-135">-ResourceId</span></span>
<span data-ttu-id="0fbdc-136">Die Ressourcen-ID der Azure-Datenfreigabe</span><span class="sxs-lookup"><span data-stu-id="0fbdc-136">The resource id of the Azure data share</span></span>

<span data-ttu-id="0fbdc-137">YAML Type: String-Parameter Sätze: ByResourceIdParameterSet-Aliase:</span><span class="sxs-lookup"><span data-stu-id="0fbdc-137">yaml Type: String Parameter Sets: ByResourceIdParameterSet Aliases:</span></span> 

<span data-ttu-id="0fbdc-138">Erforderlich: true-Position: benannter Standardwert: keine Pipelineeingabe akzeptieren: wahr (ByPropertyName) akzeptiert Platzhalterzeichen: falsch</span><span class="sxs-lookup"><span data-stu-id="0fbdc-138">Required: True Position: Named Default value: None Accept pipeline input: True (ByPropertyName) Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="0fbdc-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0fbdc-139">-Confirm</span></span>
<span data-ttu-id="0fbdc-140">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0fbdc-140">Prompts you for confirmation before running the cmdlet.</span></span>

<span data-ttu-id="0fbdc-141">YAML Type: Switchparameter-Parameter Sätze: (alle) Aliase: CF</span><span class="sxs-lookup"><span data-stu-id="0fbdc-141">yaml Type: SwitchParameter Parameter Sets: (All) Aliases: cf</span></span>

<span data-ttu-id="0fbdc-142">Erforderlich: falsche Position: benannter Standardwert: keiner akzeptiert Pipelineeingabe: false akzeptieren Platzhalterzeichen: falsch</span><span class="sxs-lookup"><span data-stu-id="0fbdc-142">Required: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="0fbdc-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0fbdc-143">-WhatIf</span></span>
<span data-ttu-id="0fbdc-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0fbdc-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0fbdc-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0fbdc-145">The cmdlet is not run.</span></span>

<span data-ttu-id="0fbdc-146">YAML Type: Switchparameter-Parameter Sätze: (alle) Aliase: Wi</span><span class="sxs-lookup"><span data-stu-id="0fbdc-146">yaml Type: SwitchParameter Parameter Sets: (All) Aliases: wi</span></span>

<span data-ttu-id="0fbdc-147">Erforderlich: falsche Position: benannter Standardwert: keiner akzeptiert Pipelineeingabe: false akzeptieren Platzhalterzeichen: falsch</span><span class="sxs-lookup"><span data-stu-id="0fbdc-147">Required: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>




<span data-ttu-id="0fbdc-148">YAML-Typ: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare-Parameter Sätze: ByObjectParameterSet-Aliase:</span><span class="sxs-lookup"><span data-stu-id="0fbdc-148">yaml Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare Parameter Sets: ByObjectParameterSet Aliases:</span></span>

<span data-ttu-id="0fbdc-149">Erforderlich: true-Position: benannter Standardwert: keine Pipelineeingabe akzeptieren: wahr (ByValue) akzeptiert Platzhalterzeichen: falsch</span><span class="sxs-lookup"><span data-stu-id="0fbdc-149">Required: True Position: Named Default value: None Accept pipeline input: True (ByValue) Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="0fbdc-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fbdc-150">CommonParameters</span></span>
<span data-ttu-id="0fbdc-151">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fbdc-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fbdc-152">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0fbdc-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fbdc-153">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0fbdc-153">INPUTS</span></span>

### <span data-ttu-id="0fbdc-154">System. String</span><span class="sxs-lookup"><span data-stu-id="0fbdc-154">System.String</span></span>

### <span data-ttu-id="0fbdc-155">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="0fbdc-155">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="0fbdc-156">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0fbdc-156">OUTPUTS</span></span>

### <span data-ttu-id="0fbdc-157">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0fbdc-157">System.Boolean</span></span>

## <span data-ttu-id="0fbdc-158">Notizen</span><span class="sxs-lookup"><span data-stu-id="0fbdc-158">NOTES</span></span>

## <span data-ttu-id="0fbdc-159">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0fbdc-159">RELATED LINKS</span></span>
