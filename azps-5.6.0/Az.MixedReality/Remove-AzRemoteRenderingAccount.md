---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/powershell/module/az.mixedreality/remove-azremoterenderingaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzRemoteRenderingAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzRemoteRenderingAccount.md
ms.openlocfilehash: ef14039cc1f46c3a891090475814d6e9553da431
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101946037"
---
# <span data-ttu-id="f07d6-101">Remove-AzRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="f07d6-101">Remove-AzRemoteRenderingAccount</span></span>

## <span data-ttu-id="f07d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f07d6-102">SYNOPSIS</span></span>
<span data-ttu-id="f07d6-103">Remoterenderingkonto löschen</span><span class="sxs-lookup"><span data-stu-id="f07d6-103">Delete Remote Rendering Account</span></span>

## <span data-ttu-id="f07d6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f07d6-104">SYNTAX</span></span>

### <span data-ttu-id="f07d6-105">DefaultParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f07d6-105">DefaultParameterSet (Default)</span></span>
```
Remove-AzRemoteRenderingAccount -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f07d6-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f07d6-106">ResourceIdParameterSet</span></span>
```
Remove-AzRemoteRenderingAccount -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f07d6-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="f07d6-107">PipelineParameterSet</span></span>
```
Remove-AzRemoteRenderingAccount -InputObject <PSRemoteRenderingAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f07d6-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f07d6-108">DESCRIPTION</span></span>
<span data-ttu-id="f07d6-109">Löschen Sie das angegebene Remoterenderingkonto aus einer bestimmten Abonnement- und Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f07d6-109">Delete specified Remote Rendering Account from certain Subscription and Resource Group.</span></span>

## <span data-ttu-id="f07d6-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f07d6-110">EXAMPLES</span></span>

### <span data-ttu-id="f07d6-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f07d6-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzRemoteRenderingAccount -ResourceGroup rg1 -Name example
```

<span data-ttu-id="f07d6-112">Löschen Des Remoterenderingkontos "Beispiel" aus dem aktuellen Abonnement und der Ressourcengruppe "rg1".</span><span class="sxs-lookup"><span data-stu-id="f07d6-112">Delete Remote Rendering Account "example" from current Subscription and Resource Group "rg1".</span></span>

## <span data-ttu-id="f07d6-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f07d6-113">PARAMETERS</span></span>

### <span data-ttu-id="f07d6-114">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f07d6-114">-Confirm</span></span>
<span data-ttu-id="f07d6-115">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f07d6-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f07d6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f07d6-116">-DefaultProfile</span></span>
<span data-ttu-id="f07d6-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f07d6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f07d6-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f07d6-118">-InputObject</span></span>
<span data-ttu-id="f07d6-119">Das benutzerdefinierte Domänenobjekt.</span><span class="sxs-lookup"><span data-stu-id="f07d6-119">The custom domain object.</span></span>

```yaml
Type: PSRemoteRenderingAccount
Parameter Sets: PipelineParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f07d6-120">-Name</span><span class="sxs-lookup"><span data-stu-id="f07d6-120">-Name</span></span>
<span data-ttu-id="f07d6-121">Name des Remoterenderingkontos.</span><span class="sxs-lookup"><span data-stu-id="f07d6-121">Remote Rendering Account Name.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases: RemoteRenderingAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f07d6-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f07d6-122">-PassThru</span></span>
<span data-ttu-id="f07d6-123">Rückgabeobjekt, wenn angegeben.</span><span class="sxs-lookup"><span data-stu-id="f07d6-123">Return object if specified.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f07d6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f07d6-124">-ResourceGroupName</span></span>
<span data-ttu-id="f07d6-125">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="f07d6-125">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f07d6-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f07d6-126">-ResourceId</span></span>
<span data-ttu-id="f07d6-127">Ressourcen-ID des Remoterenderingkontos.</span><span class="sxs-lookup"><span data-stu-id="f07d6-127">Resource ID of Remote Rendering Account.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f07d6-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f07d6-128">-WhatIf</span></span>
<span data-ttu-id="f07d6-129">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f07d6-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f07d6-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f07d6-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f07d6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f07d6-131">CommonParameters</span></span>
<span data-ttu-id="f07d6-132">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f07d6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="f07d6-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f07d6-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f07d6-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f07d6-134">INPUTS</span></span>

### <span data-ttu-id="f07d6-135">System.String</span><span class="sxs-lookup"><span data-stu-id="f07d6-135">System.String</span></span>

### <span data-ttu-id="f07d6-136">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="f07d6-136">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span></span>

### <span data-ttu-id="f07d6-137">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f07d6-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f07d6-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f07d6-138">OUTPUTS</span></span>

### <span data-ttu-id="f07d6-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f07d6-139">System.Boolean</span></span>

## <span data-ttu-id="f07d6-140">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f07d6-140">NOTES</span></span>

## <span data-ttu-id="f07d6-141">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f07d6-141">RELATED LINKS</span></span>
