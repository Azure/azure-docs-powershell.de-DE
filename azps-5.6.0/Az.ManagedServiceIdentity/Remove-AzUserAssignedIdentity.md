---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServiceIdentity.dll-Help.xml
Module Name: Az.ManagedServiceIdentity
online version: https://docs.microsoft.com/powershell/module/az.managedserviceidentity/remove-azuserassignedidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServiceIdentity/ManagedServiceIdentity/help/Remove-AzUserAssignedIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServiceIdentity/ManagedServiceIdentity/help/Remove-AzUserAssignedIdentity.md
ms.openlocfilehash: 83280df19363285ab23ca1e27441a491a783b03a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924072"
---
# <span data-ttu-id="ab01b-101">Remove-AzUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="ab01b-101">Remove-AzUserAssignedIdentity</span></span>

## <span data-ttu-id="ab01b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab01b-102">SYNOPSIS</span></span>
<span data-ttu-id="ab01b-103">Entfernt eine vom Benutzer zugewiesene Identität.</span><span class="sxs-lookup"><span data-stu-id="ab01b-103">Removes a User Assigned Identity.</span></span>

## <span data-ttu-id="ab01b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ab01b-104">SYNTAX</span></span>

### <span data-ttu-id="ab01b-105">ResourceGroupAndNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ab01b-105">ResourceGroupAndNameParameterSet (Default)</span></span>
```
Remove-AzUserAssignedIdentity [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab01b-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab01b-106">InputObjectParameterSet</span></span>
```
Remove-AzUserAssignedIdentity -InputObject <PsUserAssignedIdentity> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab01b-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab01b-107">ResourceIdParameterSet</span></span>
```
Remove-AzUserAssignedIdentity -ResourceId <String> [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab01b-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ab01b-108">DESCRIPTION</span></span>
<span data-ttu-id="ab01b-109">Die **Remove-AzUserAssignedIdentity** löscht die angegebene benutzer zugewiesene Identität.</span><span class="sxs-lookup"><span data-stu-id="ab01b-109">The **Remove-AzUserAssignedIdentity** deletes the specified User Assigned Identity.</span></span>

## <span data-ttu-id="ab01b-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ab01b-110">EXAMPLES</span></span>

### <span data-ttu-id="ab01b-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ab01b-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzUserAssignedIdentity -ResourceGroupName PSRG -Name ID1
```

<span data-ttu-id="ab01b-112">In diesem Beispiel-Cmdlet wird die **Identitäts-ID1** unter Ressourcengruppe **PSRG gelöscht.**</span><span class="sxs-lookup"><span data-stu-id="ab01b-112">This example cmdlet deletes the identity **ID1** under resource group **PSRG**.</span></span>
<span data-ttu-id="ab01b-113">True</span><span class="sxs-lookup"><span data-stu-id="ab01b-113">True</span></span>

## <span data-ttu-id="ab01b-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ab01b-114">PARAMETERS</span></span>

### <span data-ttu-id="ab01b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ab01b-115">-AsJob</span></span>
<span data-ttu-id="ab01b-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="ab01b-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ab01b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab01b-117">-DefaultProfile</span></span>
<span data-ttu-id="ab01b-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ab01b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab01b-119">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="ab01b-119">-Force</span></span>
<span data-ttu-id="ab01b-120">{{Fill Force Description}}</span><span class="sxs-lookup"><span data-stu-id="ab01b-120">{{Fill Force Description}}</span></span>

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

### <span data-ttu-id="ab01b-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ab01b-121">-InputObject</span></span>
<span data-ttu-id="ab01b-122">Das Identity-Objekt.</span><span class="sxs-lookup"><span data-stu-id="ab01b-122">The Identity object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity
Parameter Sets: InputObjectParameterSet
Aliases: Identity

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ab01b-123">-Name</span><span class="sxs-lookup"><span data-stu-id="ab01b-123">-Name</span></span>
<span data-ttu-id="ab01b-124">Der Name der Identität.</span><span class="sxs-lookup"><span data-stu-id="ab01b-124">The Identity name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupAndNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab01b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab01b-125">-ResourceGroupName</span></span>
<span data-ttu-id="ab01b-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ab01b-126">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupAndNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab01b-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ab01b-127">-ResourceId</span></span>
<span data-ttu-id="ab01b-128">Die Ressourcen-ID der Identität.</span><span class="sxs-lookup"><span data-stu-id="ab01b-128">The Identity's resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab01b-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ab01b-129">-Confirm</span></span>
<span data-ttu-id="ab01b-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ab01b-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab01b-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab01b-131">-WhatIf</span></span>
<span data-ttu-id="ab01b-132">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ab01b-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab01b-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ab01b-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab01b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab01b-134">CommonParameters</span></span>
<span data-ttu-id="ab01b-135">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab01b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab01b-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab01b-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab01b-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ab01b-137">INPUTS</span></span>

### <span data-ttu-id="ab01b-138">Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="ab01b-138">Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity</span></span>

### <span data-ttu-id="ab01b-139">System.String</span><span class="sxs-lookup"><span data-stu-id="ab01b-139">System.String</span></span>

## <span data-ttu-id="ab01b-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ab01b-140">OUTPUTS</span></span>

### <span data-ttu-id="ab01b-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ab01b-141">System.Boolean</span></span>

## <span data-ttu-id="ab01b-142">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ab01b-142">NOTES</span></span>

## <span data-ttu-id="ab01b-143">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ab01b-143">RELATED LINKS</span></span>
