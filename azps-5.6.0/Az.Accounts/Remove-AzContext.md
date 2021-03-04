---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/remove-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Remove-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Remove-AzContext.md
ms.openlocfilehash: f5307df3a91503f072c8292fe37957ce9af0df49
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920080"
---
# <span data-ttu-id="414b7-101">Remove-AzContext</span><span class="sxs-lookup"><span data-stu-id="414b7-101">Remove-AzContext</span></span>

## <span data-ttu-id="414b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="414b7-102">SYNOPSIS</span></span>
<span data-ttu-id="414b7-103">Entfernen eines Kontexts aus der Gruppe verfügbarer Kontexte</span><span class="sxs-lookup"><span data-stu-id="414b7-103">Remove a context from the set of available contexts</span></span>

## <span data-ttu-id="414b7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="414b7-104">SYNTAX</span></span>

### <span data-ttu-id="414b7-105">RemoveByInputObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="414b7-105">RemoveByInputObject (Default)</span></span>
```
Remove-AzContext -InputObject <PSAzureContext> [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="414b7-106">RemoveByName</span><span class="sxs-lookup"><span data-stu-id="414b7-106">RemoveByName</span></span>
```
Remove-AzContext [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="414b7-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="414b7-107">DESCRIPTION</span></span>
<span data-ttu-id="414b7-108">Entfernen eines Azure-Kontexts aus der Gruppe von Kontexten</span><span class="sxs-lookup"><span data-stu-id="414b7-108">Remove an azure context from the set of contexts</span></span>

## <span data-ttu-id="414b7-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="414b7-109">EXAMPLES</span></span>

### <span data-ttu-id="414b7-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="414b7-110">Example 1</span></span>
```
PS C:\> Remove-AzContext -Name Default
```

<span data-ttu-id="414b7-111">Entfernen des Kontexts "Standard"</span><span class="sxs-lookup"><span data-stu-id="414b7-111">Remove the context named default</span></span>

## <span data-ttu-id="414b7-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="414b7-112">PARAMETERS</span></span>

### <span data-ttu-id="414b7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="414b7-113">-DefaultProfile</span></span>
<span data-ttu-id="414b7-114">Die Anmeldeinformationen, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="414b7-114">The credentials, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="414b7-115">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="414b7-115">-Force</span></span>
<span data-ttu-id="414b7-116">Entfernen des Kontexts, auch wenn er die Standardeinstellung ist</span><span class="sxs-lookup"><span data-stu-id="414b7-116">Remove context even if it is the default</span></span>

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

### <span data-ttu-id="414b7-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="414b7-117">-InputObject</span></span>
<span data-ttu-id="414b7-118">Ein Kontextobjekt, das normalerweise über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="414b7-118">A context object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="414b7-119">-Name</span><span class="sxs-lookup"><span data-stu-id="414b7-119">-Name</span></span>
<span data-ttu-id="414b7-120">Der Name des Kontexts</span><span class="sxs-lookup"><span data-stu-id="414b7-120">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="414b7-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="414b7-121">-PassThru</span></span>
<span data-ttu-id="414b7-122">Zurückgeben des entfernten Kontexts</span><span class="sxs-lookup"><span data-stu-id="414b7-122">Return the removed context</span></span>

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

### <span data-ttu-id="414b7-123">-Scope</span><span class="sxs-lookup"><span data-stu-id="414b7-123">-Scope</span></span>
<span data-ttu-id="414b7-124">Bestimmt den Umfang von Kontextänderungen, z. B. ob Änderungen nur für den aktuellen Prozess oder für alle von diesem Benutzer gestarteten Sitzungen gelten</span><span class="sxs-lookup"><span data-stu-id="414b7-124">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="414b7-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="414b7-125">-Confirm</span></span>
<span data-ttu-id="414b7-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="414b7-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="414b7-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="414b7-127">-WhatIf</span></span>
<span data-ttu-id="414b7-128">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="414b7-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="414b7-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="414b7-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="414b7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="414b7-130">CommonParameters</span></span>
<span data-ttu-id="414b7-131">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="414b7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="414b7-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="414b7-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="414b7-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="414b7-133">INPUTS</span></span>

### <span data-ttu-id="414b7-134">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="414b7-134">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="414b7-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="414b7-135">OUTPUTS</span></span>

### <span data-ttu-id="414b7-136">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="414b7-136">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="414b7-137">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="414b7-137">NOTES</span></span>

## <span data-ttu-id="414b7-138">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="414b7-138">RELATED LINKS</span></span>
