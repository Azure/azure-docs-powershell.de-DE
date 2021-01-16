---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/remove-azremoterenderingaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzRemoteRenderingAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzRemoteRenderingAccount.md
ms.openlocfilehash: bfcbaa723dc2d06d74ba4d515affd2f19a51ec3e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98297484"
---
# <span data-ttu-id="668c4-101">Remove-AzRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="668c4-101">Remove-AzRemoteRenderingAccount</span></span>

## <span data-ttu-id="668c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="668c4-102">SYNOPSIS</span></span>
<span data-ttu-id="668c4-103">Konto für Remoterendering löschen</span><span class="sxs-lookup"><span data-stu-id="668c4-103">Delete Remote Rendering Account</span></span>

## <span data-ttu-id="668c4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="668c4-104">SYNTAX</span></span>

### <span data-ttu-id="668c4-105">DefaultParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="668c4-105">DefaultParameterSet (Default)</span></span>
```
Remove-AzRemoteRenderingAccount -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="668c4-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="668c4-106">ResourceIdParameterSet</span></span>
```
Remove-AzRemoteRenderingAccount -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="668c4-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="668c4-107">PipelineParameterSet</span></span>
```
Remove-AzRemoteRenderingAccount -InputObject <PSRemoteRenderingAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="668c4-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="668c4-108">DESCRIPTION</span></span>
<span data-ttu-id="668c4-109">Löschen Sie das angegebene Remoterenderingkonto aus bestimmten Abonnement- und Ressourcengruppen.</span><span class="sxs-lookup"><span data-stu-id="668c4-109">Delete specified Remote Rendering Account from certain Subscription and Resource Group.</span></span>

## <span data-ttu-id="668c4-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="668c4-110">EXAMPLES</span></span>

### <span data-ttu-id="668c4-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="668c4-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzRemoteRenderingAccount -ResourceGroup rg1 -Name example
```

<span data-ttu-id="668c4-112">Löschen Sie "Beispiel" für das Remoterenderingkonto aus der aktuellen Abonnement- und Ressourcengruppe "rg1".</span><span class="sxs-lookup"><span data-stu-id="668c4-112">Delete Remote Rendering Account "example" from current Subscription and Resource Group "rg1".</span></span>

## <span data-ttu-id="668c4-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="668c4-113">PARAMETERS</span></span>

### <span data-ttu-id="668c4-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="668c4-114">-Confirm</span></span>
<span data-ttu-id="668c4-115">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="668c4-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="668c4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="668c4-116">-DefaultProfile</span></span>
<span data-ttu-id="668c4-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="668c4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="668c4-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="668c4-118">-InputObject</span></span>
<span data-ttu-id="668c4-119">Das benutzerdefinierte Domänenobjekt.</span><span class="sxs-lookup"><span data-stu-id="668c4-119">The custom domain object.</span></span>

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

### <span data-ttu-id="668c4-120">-Name</span><span class="sxs-lookup"><span data-stu-id="668c4-120">-Name</span></span>
<span data-ttu-id="668c4-121">Kontoname des Remoterenderings.</span><span class="sxs-lookup"><span data-stu-id="668c4-121">Remote Rendering Account Name.</span></span>

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

### <span data-ttu-id="668c4-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="668c4-122">-PassThru</span></span>
<span data-ttu-id="668c4-123">Rückgabeobjekt bei Angabe</span><span class="sxs-lookup"><span data-stu-id="668c4-123">Return object if specified.</span></span>

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

### <span data-ttu-id="668c4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="668c4-124">-ResourceGroupName</span></span>
<span data-ttu-id="668c4-125">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="668c4-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="668c4-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="668c4-126">-ResourceId</span></span>
<span data-ttu-id="668c4-127">Ressourcen-ID des Remoterenderingkontos.</span><span class="sxs-lookup"><span data-stu-id="668c4-127">Resource ID of Remote Rendering Account.</span></span>

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

### <span data-ttu-id="668c4-128">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="668c4-128">-WhatIf</span></span>
<span data-ttu-id="668c4-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="668c4-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="668c4-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="668c4-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="668c4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="668c4-131">CommonParameters</span></span>
<span data-ttu-id="668c4-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="668c4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="668c4-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="668c4-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="668c4-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="668c4-134">INPUTS</span></span>

### <span data-ttu-id="668c4-135">System.String</span><span class="sxs-lookup"><span data-stu-id="668c4-135">System.String</span></span>

### <span data-ttu-id="668c4-136">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="668c4-136">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span></span>

### <span data-ttu-id="668c4-137">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="668c4-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="668c4-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="668c4-138">OUTPUTS</span></span>

### <span data-ttu-id="668c4-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="668c4-139">System.Boolean</span></span>

## <span data-ttu-id="668c4-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="668c4-140">NOTES</span></span>

## <span data-ttu-id="668c4-141">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="668c4-141">RELATED LINKS</span></span>
