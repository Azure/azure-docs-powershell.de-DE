---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Remove-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: 7220304c4dbc234a3513d2dfc35e6d71180159e2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944746"
---
# <span data-ttu-id="84616-101">Remove-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="84616-101">Remove-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="84616-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84616-102">SYNOPSIS</span></span>
<span data-ttu-id="84616-103">Löscht eine JIT-Netzwerkzugriffsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="84616-103">Deletes a JIT network access policy.</span></span>

## <span data-ttu-id="84616-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="84616-104">SYNTAX</span></span>

### <span data-ttu-id="84616-105">ResourceGroupLevelResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="84616-105">ResourceGroupLevelResource (Default)</span></span>
```
Remove-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84616-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="84616-106">ResourceId</span></span>
```
Remove-AzJitNetworkAccessPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84616-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="84616-107">InputObject</span></span>
```
Remove-AzJitNetworkAccessPolicy -InputObject <PSSecurityJitNetworkAccessPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84616-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="84616-108">DESCRIPTION</span></span>
<span data-ttu-id="84616-109">Löscht eine Just In Time-Netzwerkzugriffsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="84616-109">Deletes a Just In Time network access policy.</span></span>
<span data-ttu-id="84616-110">Nach dieser Aktion kann ein Benutzer keine temporäre Netzwerkverbindung für die VMs anfordern, die innerhalb der gelöschten Richtlinie konfiguriert wurden.</span><span class="sxs-lookup"><span data-stu-id="84616-110">After this action a user will not be able to request temporary network connection on the VMs that were configured inside the deleted policy.</span></span>

## <span data-ttu-id="84616-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="84616-111">EXAMPLES</span></span>

### <span data-ttu-id="84616-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="84616-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default"
```

<span data-ttu-id="84616-113">Löscht eine Just In Time-Netzwerkzugriffsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="84616-113">Deletes a Just In Time network access policy.</span></span>

## <span data-ttu-id="84616-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="84616-114">PARAMETERS</span></span>

### <span data-ttu-id="84616-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84616-115">-DefaultProfile</span></span>
<span data-ttu-id="84616-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="84616-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84616-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="84616-117">-InputObject</span></span>
<span data-ttu-id="84616-118">Eingabeobjekt.</span><span class="sxs-lookup"><span data-stu-id="84616-118">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="84616-119">-Location</span><span class="sxs-lookup"><span data-stu-id="84616-119">-Location</span></span>
<span data-ttu-id="84616-120">Ort.</span><span class="sxs-lookup"><span data-stu-id="84616-120">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84616-121">-Name</span><span class="sxs-lookup"><span data-stu-id="84616-121">-Name</span></span>
<span data-ttu-id="84616-122">Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="84616-122">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84616-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="84616-123">-PassThru</span></span>
<span data-ttu-id="84616-124">Gibt zurück, ob der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="84616-124">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="84616-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84616-125">-ResourceGroupName</span></span>
<span data-ttu-id="84616-126">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="84616-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84616-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="84616-127">-ResourceId</span></span>
<span data-ttu-id="84616-128">Die Ressourcen-ID der Jit-Netzwerkzugriffsrichtlinienressource.</span><span class="sxs-lookup"><span data-stu-id="84616-128">The resource id of the jit Network Access Policy resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84616-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="84616-129">-Confirm</span></span>
<span data-ttu-id="84616-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="84616-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84616-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84616-131">-WhatIf</span></span>
<span data-ttu-id="84616-132">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="84616-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="84616-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="84616-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84616-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84616-134">CommonParameters</span></span>
<span data-ttu-id="84616-135">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84616-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84616-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="84616-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84616-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="84616-137">INPUTS</span></span>

### <span data-ttu-id="84616-138">System.String</span><span class="sxs-lookup"><span data-stu-id="84616-138">System.String</span></span>

### <span data-ttu-id="84616-139">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="84616-139">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="84616-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="84616-140">OUTPUTS</span></span>

### <span data-ttu-id="84616-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="84616-141">System.Boolean</span></span>

## <span data-ttu-id="84616-142">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="84616-142">NOTES</span></span>

## <span data-ttu-id="84616-143">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="84616-143">RELATED LINKS</span></span>
