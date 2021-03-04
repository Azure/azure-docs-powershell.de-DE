---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/rename-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Rename-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Rename-AzContext.md
ms.openlocfilehash: 2ff8297ff04f18a903cca3a262d5232ace7c6ef1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925384"
---
# <span data-ttu-id="3d387-101">Rename-AzContext</span><span class="sxs-lookup"><span data-stu-id="3d387-101">Rename-AzContext</span></span>

## <span data-ttu-id="3d387-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d387-102">SYNOPSIS</span></span>
<span data-ttu-id="3d387-103">Benennen Sie einen Azure-Kontext um.</span><span class="sxs-lookup"><span data-stu-id="3d387-103">Rename an Azure context.</span></span>  <span data-ttu-id="3d387-104">Standardmäßig werden Kontexte nach Benutzerkonto und Abonnement benannt.</span><span class="sxs-lookup"><span data-stu-id="3d387-104">By default contexts are named by user account and subscription.</span></span>

## <span data-ttu-id="3d387-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3d387-105">SYNTAX</span></span>

### <span data-ttu-id="3d387-106">RenameByInputObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="3d387-106">RenameByInputObject (Default)</span></span>
```
Rename-AzContext -InputObject <PSAzureContext> [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-TargetName] <String> [<CommonParameters>]
```

### <span data-ttu-id="3d387-107">RenameByName</span><span class="sxs-lookup"><span data-stu-id="3d387-107">RenameByName</span></span>
```
Rename-AzContext [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-SourceName] <String> [-TargetName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="3d387-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3d387-108">DESCRIPTION</span></span>
<span data-ttu-id="3d387-109">Benennen Sie einen Azure-Kontext um.</span><span class="sxs-lookup"><span data-stu-id="3d387-109">Rename an Azure context.</span></span>  <span data-ttu-id="3d387-110">Standardmäßig werden Kontexte nach Benutzerkonto und Abonnement benannt.</span><span class="sxs-lookup"><span data-stu-id="3d387-110">By default contexts are named by user account and subscription.</span></span>

## <span data-ttu-id="3d387-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3d387-111">EXAMPLES</span></span>

### <span data-ttu-id="3d387-112">Beispiel 1: Umbenennen eines Kontexts mit benannten Parametern</span><span class="sxs-lookup"><span data-stu-id="3d387-112">Example 1: Rename a context using named parameters</span></span>
```powershell
PS C:\> Rename-AzContext -SourceName "[user1@contoso.org; 12345-6789-2345-3567890]" -TargetName "Work"
```

<span data-ttu-id="3d387-113">Benennen Sie den Kontext für user1@contoso.org " mit Abonnement '12345-6789-2345-3567890' in "Arbeit" um.</span><span class="sxs-lookup"><span data-stu-id="3d387-113">Rename the context for 'user1@contoso.org' with subscription '12345-6789-2345-3567890' to 'Work'.</span></span>  <span data-ttu-id="3d387-114">Nach diesem Befehl können Sie den Kontext mithilfe von "Select-AzContext Work" als Ziel verwenden.</span><span class="sxs-lookup"><span data-stu-id="3d387-114">After this command, you will be able to target the context using 'Select-AzContext Work'.</span></span>  <span data-ttu-id="3d387-115">Beachten Sie, dass Sie die Werte für "SourceName" mithilfe des Tabstoppabschlusses tabstoppen können.</span><span class="sxs-lookup"><span data-stu-id="3d387-115">Note that you can tab through the values for 'SourceName' using tab completion.</span></span>

### <span data-ttu-id="3d387-116">Beispiel 2: Umbenennen eines Kontexts mithilfe von Positionsparametern</span><span class="sxs-lookup"><span data-stu-id="3d387-116">Example 2: Rename a context using positional parameters</span></span>
```powershell
PS C:\> Rename-AzContext "My context" "Work"
```

<span data-ttu-id="3d387-117">Benennen Sie den Kontext mit dem Namen "Mein Kontext" in "Arbeit" um.</span><span class="sxs-lookup"><span data-stu-id="3d387-117">Rename the context named "My context" to "Work".</span></span>  <span data-ttu-id="3d387-118">Nach diesem Befehl können Sie den Kontext mithilfe Select-AzContext</span><span class="sxs-lookup"><span data-stu-id="3d387-118">After this command, you will be able to target the context using Select-AzContext Work</span></span>

## <span data-ttu-id="3d387-119">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="3d387-119">PARAMETERS</span></span>

### <span data-ttu-id="3d387-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d387-120">-DefaultProfile</span></span>
<span data-ttu-id="3d387-121">Die Anmeldeinformationen, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="3d387-121">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3d387-122">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="3d387-122">-Force</span></span>
<span data-ttu-id="3d387-123">Umbenennen des Kontexts auch dann, wenn der Zielkontext bereits vorhanden ist</span><span class="sxs-lookup"><span data-stu-id="3d387-123">Rename the context even if the target context already exists</span></span>

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

### <span data-ttu-id="3d387-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3d387-124">-InputObject</span></span>
<span data-ttu-id="3d387-125">Ein Kontextobjekt, das normalerweise über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="3d387-125">A context object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext
Parameter Sets: RenameByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3d387-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3d387-126">-PassThru</span></span>
<span data-ttu-id="3d387-127">Geben Sie den umbenannten Kontext zurück.</span><span class="sxs-lookup"><span data-stu-id="3d387-127">Return the renamed context.</span></span>

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

### <span data-ttu-id="3d387-128">-Scope</span><span class="sxs-lookup"><span data-stu-id="3d387-128">-Scope</span></span>
<span data-ttu-id="3d387-129">Bestimmt den Umfang von Kontextänderungen, z. B. ob Änderungen nur für den aktuellen Prozess oder für alle von diesem Benutzer gestarteten Sitzungen gelten</span><span class="sxs-lookup"><span data-stu-id="3d387-129">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="3d387-130">-SourceName</span><span class="sxs-lookup"><span data-stu-id="3d387-130">-SourceName</span></span>
<span data-ttu-id="3d387-131">Der Name des Kontexts</span><span class="sxs-lookup"><span data-stu-id="3d387-131">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: RenameByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d387-132">-TargetName</span><span class="sxs-lookup"><span data-stu-id="3d387-132">-TargetName</span></span>
<span data-ttu-id="3d387-133">Der neue Name des Kontexts</span><span class="sxs-lookup"><span data-stu-id="3d387-133">The new name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d387-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3d387-134">-Confirm</span></span>
<span data-ttu-id="3d387-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3d387-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d387-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d387-136">-WhatIf</span></span>
<span data-ttu-id="3d387-137">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3d387-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d387-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3d387-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d387-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d387-139">CommonParameters</span></span>
<span data-ttu-id="3d387-140">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d387-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d387-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3d387-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d387-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3d387-142">INPUTS</span></span>

### <span data-ttu-id="3d387-143">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="3d387-143">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="3d387-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3d387-144">OUTPUTS</span></span>

### <span data-ttu-id="3d387-145">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="3d387-145">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="3d387-146">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="3d387-146">NOTES</span></span>

## <span data-ttu-id="3d387-147">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="3d387-147">RELATED LINKS</span></span>
