---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Remove-AzSecurityWorkspaceSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityWorkspaceSetting.md
ms.openlocfilehash: b351cfaa5d94c7104972158dc9dee6363a7d466b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934656"
---
# <span data-ttu-id="e53ce-101">Remove-AzSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="e53ce-101">Remove-AzSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="e53ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e53ce-102">SYNOPSIS</span></span>
<span data-ttu-id="e53ce-103">Löscht die Einstellung für den Sicherheitsarbeitsbereich für dieses Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e53ce-103">Deletes the security workspace setting for this subscription.</span></span>

## <span data-ttu-id="e53ce-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e53ce-104">SYNTAX</span></span>

### <span data-ttu-id="e53ce-105">SubscriptionLevelResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="e53ce-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityWorkspaceSetting -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e53ce-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="e53ce-106">ResourceId</span></span>
```
Remove-AzSecurityWorkspaceSetting -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e53ce-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="e53ce-107">InputObject</span></span>
```
Remove-AzSecurityWorkspaceSetting -InputObject <PSSecurityWorkspaceSetting> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e53ce-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e53ce-108">DESCRIPTION</span></span>
<span data-ttu-id="e53ce-109">Löscht die Einstellung für den Sicherheitsarbeitsbereich für dieses Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e53ce-109">Deletes the security workspace setting for this subscription.</span></span>
<span data-ttu-id="e53ce-110">Mit dieser Aktion müssen die neu installierten Sicherheitsmitarbeiter dem Standardarbeitsbereich dieses Abonnements melden.</span><span class="sxs-lookup"><span data-stu-id="e53ce-110">This action will make the newly installed security agents to report to the default workspace of this subscription.</span></span>

## <span data-ttu-id="e53ce-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e53ce-111">EXAMPLES</span></span>

### <span data-ttu-id="e53ce-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e53ce-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityWorkspaceSetting -Name "default"
```

<span data-ttu-id="e53ce-113">Löscht die Einstellung für den Sicherheitsarbeitsbereich für dieses Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e53ce-113">Deletes the security workspace setting for this subscription.</span></span>

## <span data-ttu-id="e53ce-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e53ce-114">PARAMETERS</span></span>

### <span data-ttu-id="e53ce-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e53ce-115">-DefaultProfile</span></span>
<span data-ttu-id="e53ce-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e53ce-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e53ce-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e53ce-117">-InputObject</span></span>
<span data-ttu-id="e53ce-118">Eingabeobjekt.</span><span class="sxs-lookup"><span data-stu-id="e53ce-118">Input Object.</span></span>

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

### <span data-ttu-id="e53ce-119">-Name</span><span class="sxs-lookup"><span data-stu-id="e53ce-119">-Name</span></span>
<span data-ttu-id="e53ce-120">Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="e53ce-120">Resource name.</span></span>

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

### <span data-ttu-id="e53ce-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e53ce-121">-PassThru</span></span>
<span data-ttu-id="e53ce-122">Gibt zurück, ob der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="e53ce-122">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="e53ce-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e53ce-123">-ResourceId</span></span>
<span data-ttu-id="e53ce-124">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="e53ce-124">Resource ID.</span></span>

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

### <span data-ttu-id="e53ce-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e53ce-125">-Confirm</span></span>
<span data-ttu-id="e53ce-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e53ce-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e53ce-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e53ce-127">-WhatIf</span></span>
<span data-ttu-id="e53ce-128">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e53ce-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e53ce-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e53ce-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e53ce-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e53ce-130">CommonParameters</span></span>
<span data-ttu-id="e53ce-131">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e53ce-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e53ce-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e53ce-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e53ce-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e53ce-133">INPUTS</span></span>

### <span data-ttu-id="e53ce-134">System.String</span><span class="sxs-lookup"><span data-stu-id="e53ce-134">System.String</span></span>

### <span data-ttu-id="e53ce-135">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="e53ce-135">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="e53ce-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e53ce-136">OUTPUTS</span></span>

### <span data-ttu-id="e53ce-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e53ce-137">System.Boolean</span></span>

## <span data-ttu-id="e53ce-138">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="e53ce-138">NOTES</span></span>

## <span data-ttu-id="e53ce-139">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="e53ce-139">RELATED LINKS</span></span>
