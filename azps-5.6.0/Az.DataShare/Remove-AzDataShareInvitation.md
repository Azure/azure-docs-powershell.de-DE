---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/remove-azdatashareinvitation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareInvitation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareInvitation.md
ms.openlocfilehash: 4736a1b6e8d0a6d34cf1874868596d4139ad5e67
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941835"
---
# <span data-ttu-id="a9db4-101">Remove-AzDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="a9db4-101">Remove-AzDataShareInvitation</span></span>

## <span data-ttu-id="a9db4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9db4-102">SYNOPSIS</span></span>
<span data-ttu-id="a9db4-103">Entfernt eine Einladung</span><span class="sxs-lookup"><span data-stu-id="a9db4-103">removes an invitation</span></span>

## <span data-ttu-id="a9db4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a9db4-104">SYNTAX</span></span>

### <span data-ttu-id="a9db4-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a9db4-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareInvitation -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a9db4-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9db4-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareInvitation -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9db4-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9db4-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareInvitation -InputObject <PSDataShareInvitation> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9db4-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a9db4-108">DESCRIPTION</span></span>
<span data-ttu-id="a9db4-109">Das **Cmdlet Remove-AzDataShareInvitation** entfernt eine Datenfreigabeeinladung.</span><span class="sxs-lookup"><span data-stu-id="a9db4-109">The **Remove-AzDataShareInvitation** cmdlet removes a datashare invitation.</span></span>

## <span data-ttu-id="a9db4-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a9db4-110">EXAMPLES</span></span>

### <span data-ttu-id="a9db4-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a9db4-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareDataSetMapping -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "ADSInvite"
Are you sure you want to remove dataset mapping "ADSInvite"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="a9db4-112">Mit diesen Befehlen wird eine Einladung mit dem Namen ADSInvite aus der Freigabe von AdsShare entfernt.</span><span class="sxs-lookup"><span data-stu-id="a9db4-112">This commands removes an invitation named ADSInvite from share AdsShare.</span></span> 

## <span data-ttu-id="a9db4-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a9db4-113">PARAMETERS</span></span>

### <span data-ttu-id="a9db4-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a9db4-114">-AccountName</span></span>
<span data-ttu-id="a9db4-115">Name des Azure-Datenfreigabekontos</span><span class="sxs-lookup"><span data-stu-id="a9db4-115">Azure data share account name</span></span>

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

### <span data-ttu-id="a9db4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9db4-116">-DefaultProfile</span></span>
<span data-ttu-id="a9db4-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a9db4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9db4-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a9db4-118">-InputObject</span></span>
<span data-ttu-id="a9db4-119">Azure Data Share Invitation Object</span><span class="sxs-lookup"><span data-stu-id="a9db4-119">Azure data share invitation object</span></span>


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

### <span data-ttu-id="a9db4-120">-Name</span><span class="sxs-lookup"><span data-stu-id="a9db4-120">-Name</span></span>
<span data-ttu-id="a9db4-121">Name der Einladung zur Freigabe von Azure-Daten</span><span class="sxs-lookup"><span data-stu-id="a9db4-121">Azure data share invitation name</span></span>

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

### <span data-ttu-id="a9db4-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a9db4-122">-PassThru</span></span>
<span data-ttu-id="a9db4-123">Rückgabeobjekt (sofern angegeben).</span><span class="sxs-lookup"><span data-stu-id="a9db4-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="a9db4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9db4-124">-ResourceGroupName</span></span>
<span data-ttu-id="a9db4-125">Der Ressourcengruppenname des Azure Data Share-Kontos</span><span class="sxs-lookup"><span data-stu-id="a9db4-125">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="a9db4-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a9db4-126">-ResourceId</span></span>
<span data-ttu-id="a9db4-127">Die Ressourcen-ID der Azure-Datenfreigabeeinladung</span><span class="sxs-lookup"><span data-stu-id="a9db4-127">The resource id of the azure data share invitation</span></span>

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

### <span data-ttu-id="a9db4-128">-ShareName</span><span class="sxs-lookup"><span data-stu-id="a9db4-128">-ShareName</span></span>
<span data-ttu-id="a9db4-129">Azure-Datenfreigabename.</span><span class="sxs-lookup"><span data-stu-id="a9db4-129">Azure data share name.</span></span>

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

### <span data-ttu-id="a9db4-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a9db4-130">-Confirm</span></span>
<span data-ttu-id="a9db4-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a9db4-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9db4-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9db4-132">-WhatIf</span></span>
<span data-ttu-id="a9db4-133">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a9db4-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9db4-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a9db4-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9db4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9db4-135">CommonParameters</span></span>
<span data-ttu-id="a9db4-136">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9db4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9db4-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a9db4-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9db4-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a9db4-138">INPUTS</span></span>

### <span data-ttu-id="a9db4-139">System.String</span><span class="sxs-lookup"><span data-stu-id="a9db4-139">System.String</span></span>

### <span data-ttu-id="a9db4-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="a9db4-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span></span>

## <span data-ttu-id="a9db4-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a9db4-141">OUTPUTS</span></span>

### <span data-ttu-id="a9db4-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a9db4-142">System.Boolean</span></span>

## <span data-ttu-id="a9db4-143">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a9db4-143">NOTES</span></span>

## <span data-ttu-id="a9db4-144">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a9db4-144">RELATED LINKS</span></span>
