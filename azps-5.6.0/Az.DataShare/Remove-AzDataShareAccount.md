---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/remove-azdatashareaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareAccount.md
ms.openlocfilehash: 74651ea4a9a108db9cc3f666ad6f78f494fcd676
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928176"
---
# <span data-ttu-id="2bc36-101">Remove-AzDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="2bc36-101">Remove-AzDataShareAccount</span></span>

## <span data-ttu-id="2bc36-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2bc36-102">SYNOPSIS</span></span>
<span data-ttu-id="2bc36-103">Entfernt ein Datenfreigabekonto</span><span class="sxs-lookup"><span data-stu-id="2bc36-103">Removes a datashare account</span></span>

## <span data-ttu-id="2bc36-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2bc36-104">SYNTAX</span></span>

### <span data-ttu-id="2bc36-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="2bc36-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareAccount -ResourceGroupName <String> -Name <String> [-PassThru] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2bc36-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2bc36-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareAccount -ResourceId <String> [-PassThru] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2bc36-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2bc36-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareAccount -InputObject <PSDataShareAccount> [-PassThru] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2bc36-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2bc36-108">DESCRIPTION</span></span>
<span data-ttu-id="2bc36-109">Das **Cmdlet Remove-AzDataShareAccount** entfernt ein Datenfreigabekonto.</span><span class="sxs-lookup"><span data-stu-id="2bc36-109">The **Remove-AzDataShareAccount** cmdlet removes a datashare account.</span></span>

## <span data-ttu-id="2bc36-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2bc36-110">EXAMPLES</span></span>

### <span data-ttu-id="2bc36-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2bc36-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareAccount -Name "WikiADS" -ResourceGroupName "ADS"
Confirm
Are you sure you want to remove datashare account 'WikiADS' in resource group 'ADS'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="2bc36-112">Mit diesem Befehl wird das Datenfreigabekonto mit dem Namen WikiADS aus der Ressourcengruppe ADS entfernt.</span><span class="sxs-lookup"><span data-stu-id="2bc36-112">This command removes the datashare account named WikiADS from the resource group named ADS.</span></span>
<span data-ttu-id="2bc36-113">Dieser Befehl gibt einen Wert von $True.</span><span class="sxs-lookup"><span data-stu-id="2bc36-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="2bc36-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="2bc36-114">PARAMETERS</span></span>

### <span data-ttu-id="2bc36-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2bc36-115">-AsJob</span></span>
<span data-ttu-id="2bc36-116">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="2bc36-116">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="2bc36-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bc36-117">-DefaultProfile</span></span>
<span data-ttu-id="2bc36-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2bc36-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2bc36-119">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="2bc36-119">-Force</span></span>
<span data-ttu-id="2bc36-120">{{Fill Force Description}}</span><span class="sxs-lookup"><span data-stu-id="2bc36-120">{{Fill Force Description}}</span></span>

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

### <span data-ttu-id="2bc36-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2bc36-121">-InputObject</span></span>
<span data-ttu-id="2bc36-122">Das Azure Data Share-Kontoobjekt.</span><span class="sxs-lookup"><span data-stu-id="2bc36-122">The azure data share account object.</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2bc36-123">-Name</span><span class="sxs-lookup"><span data-stu-id="2bc36-123">-Name</span></span>
<span data-ttu-id="2bc36-124">Name des Azure-Datenfreigabekontos.</span><span class="sxs-lookup"><span data-stu-id="2bc36-124">Azure data share account name.</span></span>

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

### <span data-ttu-id="2bc36-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2bc36-125">-PassThru</span></span>
<span data-ttu-id="2bc36-126">Rückgabeobjekt (sofern angegeben).</span><span class="sxs-lookup"><span data-stu-id="2bc36-126">Return object (if specified).</span></span>

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

### <span data-ttu-id="2bc36-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2bc36-127">-ResourceGroupName</span></span>
<span data-ttu-id="2bc36-128">Der Ressourcengruppenname des Azure Data Share-Kontos.</span><span class="sxs-lookup"><span data-stu-id="2bc36-128">The resource group name of azure data share account.</span></span>

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

### <span data-ttu-id="2bc36-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2bc36-129">-ResourceId</span></span>
<span data-ttu-id="2bc36-130">Die Ressourcen-ID des Azure-Datenfreigabekontos.</span><span class="sxs-lookup"><span data-stu-id="2bc36-130">The resource id of the azure data share account.</span></span>

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

### <span data-ttu-id="2bc36-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2bc36-131">-Confirm</span></span>
<span data-ttu-id="2bc36-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2bc36-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2bc36-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2bc36-133">-WhatIf</span></span>
<span data-ttu-id="2bc36-134">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2bc36-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2bc36-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2bc36-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2bc36-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bc36-136">CommonParameters</span></span>
<span data-ttu-id="2bc36-137">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bc36-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bc36-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2bc36-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bc36-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2bc36-139">INPUTS</span></span>

### <span data-ttu-id="2bc36-140">System.String</span><span class="sxs-lookup"><span data-stu-id="2bc36-140">System.String</span></span>

### <span data-ttu-id="2bc36-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="2bc36-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span></span>

## <span data-ttu-id="2bc36-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2bc36-142">OUTPUTS</span></span>

### <span data-ttu-id="2bc36-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2bc36-143">System.Boolean</span></span>

## <span data-ttu-id="2bc36-144">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="2bc36-144">NOTES</span></span>

## <span data-ttu-id="2bc36-145">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="2bc36-145">RELATED LINKS</span></span>
