---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzSecurityWorkspaceSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityWorkspaceSetting.md
ms.openlocfilehash: 75e68cfac55c8fb7086f02d5e70dc466f335d1de
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100150817"
---
# <span data-ttu-id="ea645-101">Remove-AzSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="ea645-101">Remove-AzSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="ea645-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea645-102">SYNOPSIS</span></span>
<span data-ttu-id="ea645-103">Löscht die Einstellung des Sicherheitsarbeitsbereichs für dieses Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ea645-103">Deletes the security workspace setting for this subscription.</span></span>

## <span data-ttu-id="ea645-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ea645-104">SYNTAX</span></span>

### <span data-ttu-id="ea645-105">SubscriptionLevelResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="ea645-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityWorkspaceSetting -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea645-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ea645-106">ResourceId</span></span>
```
Remove-AzSecurityWorkspaceSetting -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea645-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="ea645-107">InputObject</span></span>
```
Remove-AzSecurityWorkspaceSetting -InputObject <PSSecurityWorkspaceSetting> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea645-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ea645-108">DESCRIPTION</span></span>
<span data-ttu-id="ea645-109">Löscht die Einstellung des Sicherheitsarbeitsbereichs für dieses Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ea645-109">Deletes the security workspace setting for this subscription.</span></span>
<span data-ttu-id="ea645-110">Durch diese Aktion müssen die neu installierten Sicherheits-Agents dem Standardarbeitsbereich dieses Abonnements berichte.</span><span class="sxs-lookup"><span data-stu-id="ea645-110">This action will make the newly installed security agents to report to the default workspace of this subscription.</span></span>

## <span data-ttu-id="ea645-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ea645-111">EXAMPLES</span></span>

### <span data-ttu-id="ea645-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ea645-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityWorkspaceSetting -Name "default"
```

<span data-ttu-id="ea645-113">Löscht die Einstellung des Sicherheitsarbeitsbereichs für dieses Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ea645-113">Deletes the security workspace setting for this subscription.</span></span>

## <span data-ttu-id="ea645-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ea645-114">PARAMETERS</span></span>

### <span data-ttu-id="ea645-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea645-115">-DefaultProfile</span></span>
<span data-ttu-id="ea645-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ea645-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea645-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ea645-117">-InputObject</span></span>
<span data-ttu-id="ea645-118">Eingabeobjekt.</span><span class="sxs-lookup"><span data-stu-id="ea645-118">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ea645-119">-Name</span><span class="sxs-lookup"><span data-stu-id="ea645-119">-Name</span></span>
<span data-ttu-id="ea645-120">Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="ea645-120">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea645-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ea645-121">-PassThru</span></span>
<span data-ttu-id="ea645-122">Gibt zurück, ob der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="ea645-122">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="ea645-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ea645-123">-ResourceId</span></span>
<span data-ttu-id="ea645-124">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="ea645-124">Resource ID.</span></span>

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

### <span data-ttu-id="ea645-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ea645-125">-Confirm</span></span>
<span data-ttu-id="ea645-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ea645-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea645-127">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="ea645-127">-WhatIf</span></span>
<span data-ttu-id="ea645-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ea645-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ea645-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ea645-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea645-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea645-130">CommonParameters</span></span>
<span data-ttu-id="ea645-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea645-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea645-132">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ea645-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea645-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ea645-133">INPUTS</span></span>

### <span data-ttu-id="ea645-134">System.String</span><span class="sxs-lookup"><span data-stu-id="ea645-134">System.String</span></span>

### <span data-ttu-id="ea645-135">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="ea645-135">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="ea645-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ea645-136">OUTPUTS</span></span>

### <span data-ttu-id="ea645-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ea645-137">System.Boolean</span></span>

## <span data-ttu-id="ea645-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ea645-138">NOTES</span></span>

## <span data-ttu-id="ea645-139">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ea645-139">RELATED LINKS</span></span>
