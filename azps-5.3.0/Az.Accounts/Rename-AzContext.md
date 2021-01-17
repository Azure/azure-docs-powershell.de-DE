---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/rename-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Rename-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Rename-AzContext.md
ms.openlocfilehash: 09c0faec1ab424ef1bfb10fec35dd59646e4711c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469184"
---
# <span data-ttu-id="dc3d0-101">Rename-AzContext</span><span class="sxs-lookup"><span data-stu-id="dc3d0-101">Rename-AzContext</span></span>

## <span data-ttu-id="dc3d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc3d0-102">SYNOPSIS</span></span>
<span data-ttu-id="dc3d0-103">Benennen Sie einen Azure-Kontext um.</span><span class="sxs-lookup"><span data-stu-id="dc3d0-103">Rename an Azure context.</span></span>  <span data-ttu-id="dc3d0-104">Standardmäßig werden Kontexte nach Benutzerkonto und Abonnement benannt.</span><span class="sxs-lookup"><span data-stu-id="dc3d0-104">By default contexts are named by user account and subscription.</span></span>

## <span data-ttu-id="dc3d0-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dc3d0-105">SYNTAX</span></span>

### <span data-ttu-id="dc3d0-106">RenameByInputObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="dc3d0-106">RenameByInputObject (Default)</span></span>
```
Rename-AzContext -InputObject <PSAzureContext> [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-TargetName] <String> [<CommonParameters>]
```

### <span data-ttu-id="dc3d0-107">RenameByName</span><span class="sxs-lookup"><span data-stu-id="dc3d0-107">RenameByName</span></span>
```
Rename-AzContext [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-SourceName] <String> [-TargetName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="dc3d0-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dc3d0-108">DESCRIPTION</span></span>
<span data-ttu-id="dc3d0-109">Benennen Sie einen Azure-Kontext um.</span><span class="sxs-lookup"><span data-stu-id="dc3d0-109">Rename an Azure context.</span></span>  <span data-ttu-id="dc3d0-110">Standardmäßig werden Kontexte nach Benutzerkonto und Abonnement benannt.</span><span class="sxs-lookup"><span data-stu-id="dc3d0-110">By default contexts are named by user account and subscription.</span></span>

## <span data-ttu-id="dc3d0-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="dc3d0-111">EXAMPLES</span></span>

### <span data-ttu-id="dc3d0-112">Beispiel 1: Umbenennen eines Kontexts mit benannten Parametern</span><span class="sxs-lookup"><span data-stu-id="dc3d0-112">Example 1: Rename a context using named parameters</span></span>
```powershell
PS C:\> Rename-AzContext -SourceName "[user1@contoso.org; 12345-6789-2345-3567890]" -TargetName "Work"
```

<span data-ttu-id="dc3d0-113">Benennen Sie den Kontext für ' mit dem Abonnement user1@contoso.org '12345-6789-2345-3567890' in 'Arbeit' um.</span><span class="sxs-lookup"><span data-stu-id="dc3d0-113">Rename the context for 'user1@contoso.org' with subscription '12345-6789-2345-3567890' to 'Work'.</span></span>  <span data-ttu-id="dc3d0-114">Nach diesem Befehl können Sie den Kontext mit "Select-AzContext Work" als Ziel verwenden.</span><span class="sxs-lookup"><span data-stu-id="dc3d0-114">After this command, you will be able to target the context using 'Select-AzContext Work'.</span></span>  <span data-ttu-id="dc3d0-115">Beachten Sie, dass Sie die Werte für "SourceName" mithilfe der Tabulatorenvollständigung mit TAB durchwerten können.</span><span class="sxs-lookup"><span data-stu-id="dc3d0-115">Note that you can tab through the values for 'SourceName' using tab completion.</span></span>

### <span data-ttu-id="dc3d0-116">Beispiel 2: Umbenennen eines Kontexts mithilfe von Positionsparametern</span><span class="sxs-lookup"><span data-stu-id="dc3d0-116">Example 2: Rename a context using positional parameters</span></span>
```powershell
PS C:\> Rename-AzContext "My context" "Work"
```

<span data-ttu-id="dc3d0-117">Benennen Sie den Kontext in "Mein Kontext" in "Arbeit" um.</span><span class="sxs-lookup"><span data-stu-id="dc3d0-117">Rename the context named "My context" to "Work".</span></span>  <span data-ttu-id="dc3d0-118">Nach diesem Befehl können Sie den Kontext mithilfe des Befehls "Select-AzContext"</span><span class="sxs-lookup"><span data-stu-id="dc3d0-118">After this command, you will be able to target the context using Select-AzContext Work</span></span>

## <span data-ttu-id="dc3d0-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dc3d0-119">PARAMETERS</span></span>

### <span data-ttu-id="dc3d0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc3d0-120">-DefaultProfile</span></span>
<span data-ttu-id="dc3d0-121">Die Anmeldeinformationen, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="dc3d0-121">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dc3d0-122">-Force</span><span class="sxs-lookup"><span data-stu-id="dc3d0-122">-Force</span></span>
<span data-ttu-id="dc3d0-123">Umbenennen des Kontexts auch dann, wenn der Zielkontext bereits vorhanden ist</span><span class="sxs-lookup"><span data-stu-id="dc3d0-123">Rename the context even if the target context already exists</span></span>

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

### <span data-ttu-id="dc3d0-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dc3d0-124">-InputObject</span></span>
<span data-ttu-id="dc3d0-125">Ein Kontextobjekt, das normalerweise über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="dc3d0-125">A context object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="dc3d0-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dc3d0-126">-PassThru</span></span>
<span data-ttu-id="dc3d0-127">Geben Sie den umbenannten Kontext zurück.</span><span class="sxs-lookup"><span data-stu-id="dc3d0-127">Return the renamed context.</span></span>

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

### <span data-ttu-id="dc3d0-128">-Scope</span><span class="sxs-lookup"><span data-stu-id="dc3d0-128">-Scope</span></span>
<span data-ttu-id="dc3d0-129">Bestimmt den Umfang von Kontextänderungen, z. B. ob Änderungen nur für den aktuellen Prozess oder für alle von diesem Benutzer gestarteten Sitzungen gelten.</span><span class="sxs-lookup"><span data-stu-id="dc3d0-129">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="dc3d0-130">-SourceName</span><span class="sxs-lookup"><span data-stu-id="dc3d0-130">-SourceName</span></span>
<span data-ttu-id="dc3d0-131">Der Name des Kontexts</span><span class="sxs-lookup"><span data-stu-id="dc3d0-131">The name of the context</span></span>

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

### <span data-ttu-id="dc3d0-132">-TargetName</span><span class="sxs-lookup"><span data-stu-id="dc3d0-132">-TargetName</span></span>
<span data-ttu-id="dc3d0-133">Der neue Name des Kontexts</span><span class="sxs-lookup"><span data-stu-id="dc3d0-133">The new name of the context</span></span>

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

### <span data-ttu-id="dc3d0-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dc3d0-134">-Confirm</span></span>
<span data-ttu-id="dc3d0-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dc3d0-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc3d0-136">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="dc3d0-136">-WhatIf</span></span>
<span data-ttu-id="dc3d0-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dc3d0-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc3d0-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dc3d0-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc3d0-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc3d0-139">CommonParameters</span></span>
<span data-ttu-id="dc3d0-140">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc3d0-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc3d0-141">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc3d0-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc3d0-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="dc3d0-142">INPUTS</span></span>

### <span data-ttu-id="dc3d0-143">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="dc3d0-143">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="dc3d0-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="dc3d0-144">OUTPUTS</span></span>

### <span data-ttu-id="dc3d0-145">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="dc3d0-145">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="dc3d0-146">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="dc3d0-146">NOTES</span></span>

## <span data-ttu-id="dc3d0-147">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="dc3d0-147">RELATED LINKS</span></span>
