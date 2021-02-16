---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatashareinvitation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareInvitation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareInvitation.md
ms.openlocfilehash: a94699bfa4b2637a0d0d51b8f52392bb02f51100
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100161801"
---
# <span data-ttu-id="22fa3-101">Remove-AzDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="22fa3-101">Remove-AzDataShareInvitation</span></span>

## <span data-ttu-id="22fa3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22fa3-102">SYNOPSIS</span></span>
<span data-ttu-id="22fa3-103">eine Einladung entfernt</span><span class="sxs-lookup"><span data-stu-id="22fa3-103">removes an invitation</span></span>

## <span data-ttu-id="22fa3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="22fa3-104">SYNTAX</span></span>

### <span data-ttu-id="22fa3-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="22fa3-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareInvitation -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="22fa3-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="22fa3-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareInvitation -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22fa3-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="22fa3-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareInvitation -InputObject <PSDataShareInvitation> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22fa3-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="22fa3-108">DESCRIPTION</span></span>
<span data-ttu-id="22fa3-109">Das **Cmdlet "Remove-AzDataShareInvitation"** entfernt eine Datenfreigabeeinladung.</span><span class="sxs-lookup"><span data-stu-id="22fa3-109">The **Remove-AzDataShareInvitation** cmdlet removes a datashare invitation.</span></span>

## <span data-ttu-id="22fa3-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="22fa3-110">EXAMPLES</span></span>

### <span data-ttu-id="22fa3-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="22fa3-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareDataSetMapping -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "ADSInvite"
Are you sure you want to remove dataset mapping "ADSInvite"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="22fa3-112">Mit diesen Befehlen wird eine Einladung mit dem Namen ADSInvite aus der Freigabe von AdsShare entfernt.</span><span class="sxs-lookup"><span data-stu-id="22fa3-112">This commands removes an invitation named ADSInvite from share AdsShare.</span></span> 

## <span data-ttu-id="22fa3-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="22fa3-113">PARAMETERS</span></span>

### <span data-ttu-id="22fa3-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="22fa3-114">-AccountName</span></span>
<span data-ttu-id="22fa3-115">Name des Azure-Datenfreigabekontos</span><span class="sxs-lookup"><span data-stu-id="22fa3-115">Azure data share account name</span></span>

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

### <span data-ttu-id="22fa3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22fa3-116">-DefaultProfile</span></span>
<span data-ttu-id="22fa3-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="22fa3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22fa3-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="22fa3-118">-InputObject</span></span>
<span data-ttu-id="22fa3-119">Einladungsobjekt für die Freigabe von Azure-Daten</span><span class="sxs-lookup"><span data-stu-id="22fa3-119">Azure data share invitation object</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="22fa3-120">-Name</span><span class="sxs-lookup"><span data-stu-id="22fa3-120">-Name</span></span>
<span data-ttu-id="22fa3-121">Name der Einladung zur Freigabe von Azure-Daten</span><span class="sxs-lookup"><span data-stu-id="22fa3-121">Azure data share invitation name</span></span>

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

### <span data-ttu-id="22fa3-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="22fa3-122">-PassThru</span></span>
<span data-ttu-id="22fa3-123">Rückgabeobjekt (sofern angegeben)</span><span class="sxs-lookup"><span data-stu-id="22fa3-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="22fa3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22fa3-124">-ResourceGroupName</span></span>
<span data-ttu-id="22fa3-125">Der Ressourcengruppenname des Azure Data Share-Kontos</span><span class="sxs-lookup"><span data-stu-id="22fa3-125">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="22fa3-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="22fa3-126">-ResourceId</span></span>
<span data-ttu-id="22fa3-127">Die Ressourcen-ID der Azure-Datenfreigabeeinladung</span><span class="sxs-lookup"><span data-stu-id="22fa3-127">The resource id of the azure data share invitation</span></span>

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

### <span data-ttu-id="22fa3-128">-ShareName</span><span class="sxs-lookup"><span data-stu-id="22fa3-128">-ShareName</span></span>
<span data-ttu-id="22fa3-129">Name der Azure-Datenfreigabe.</span><span class="sxs-lookup"><span data-stu-id="22fa3-129">Azure data share name.</span></span>

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

### <span data-ttu-id="22fa3-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="22fa3-130">-Confirm</span></span>
<span data-ttu-id="22fa3-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="22fa3-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22fa3-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="22fa3-132">-WhatIf</span></span>
<span data-ttu-id="22fa3-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="22fa3-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22fa3-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="22fa3-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22fa3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22fa3-135">CommonParameters</span></span>
<span data-ttu-id="22fa3-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22fa3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22fa3-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="22fa3-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22fa3-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="22fa3-138">INPUTS</span></span>

### <span data-ttu-id="22fa3-139">System.String</span><span class="sxs-lookup"><span data-stu-id="22fa3-139">System.String</span></span>

### <span data-ttu-id="22fa3-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="22fa3-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span></span>

## <span data-ttu-id="22fa3-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="22fa3-141">OUTPUTS</span></span>

### <span data-ttu-id="22fa3-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="22fa3-142">System.Boolean</span></span>

## <span data-ttu-id="22fa3-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="22fa3-143">NOTES</span></span>

## <span data-ttu-id="22fa3-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="22fa3-144">RELATED LINKS</span></span>
