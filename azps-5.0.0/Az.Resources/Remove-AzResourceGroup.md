---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 880D321E-30F2-4CAE-B14A-5F6DD8E1DB99
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroup.md
ms.openlocfilehash: e53e5311b4553dc3803a4a6d9ac31d6a2569bbc0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94180041"
---
# <span data-ttu-id="e7bcf-101">Remove-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e7bcf-101">Remove-AzResourceGroup</span></span>

## <span data-ttu-id="e7bcf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e7bcf-102">SYNOPSIS</span></span>
<span data-ttu-id="e7bcf-103">Entfernt eine Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e7bcf-103">Removes a resource group.</span></span>

## <span data-ttu-id="e7bcf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e7bcf-104">SYNTAX</span></span>

### <span data-ttu-id="e7bcf-105">RemoveByResourceGroupName (Standard)</span><span class="sxs-lookup"><span data-stu-id="e7bcf-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzResourceGroup [-Name] <String> [-Force] [-AsJob] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7bcf-106">RemoveByResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="e7bcf-106">RemoveByResourceGroupId</span></span>
```
Remove-AzResourceGroup -Id <String> [-Force] [-AsJob] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7bcf-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e7bcf-107">DESCRIPTION</span></span>
<span data-ttu-id="e7bcf-108">Das Cmdlet **Remove-AzResourceGroup** entfernt eine Azure-Ressourcengruppe und deren Ressourcen aus dem aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e7bcf-108">The **Remove-AzResourceGroup** cmdlet removes an Azure resource group and its resources from the current subscription.</span></span>
<span data-ttu-id="e7bcf-109">Verwenden Sie das Remove-AzResource-Cmdlet, um eine Ressource zu löschen, aber die Ressourcengruppe zu belegen.</span><span class="sxs-lookup"><span data-stu-id="e7bcf-109">To delete a resource, but leave the resource group, use the Remove-AzResource cmdlet.</span></span>

## <span data-ttu-id="e7bcf-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e7bcf-110">EXAMPLES</span></span>

### <span data-ttu-id="e7bcf-111">Beispiel 1: Entfernen einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="e7bcf-111">Example 1: Remove a resource group</span></span>
```
PS C:\>Remove-AzResourceGroup -Name "ContosoRG01"
```

<span data-ttu-id="e7bcf-112">Dieser Befehl entfernt die ContosoRG01-Ressourcengruppe aus dem Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e7bcf-112">This command removes the ContosoRG01 resource group from the subscription.</span></span>
<span data-ttu-id="e7bcf-113">Das Cmdlet fordert Sie zur Bestätigung auf und gibt keine Ausgabe zurück.</span><span class="sxs-lookup"><span data-stu-id="e7bcf-113">The cmdlet prompts you for confirmation and returns no output.</span></span>

### <span data-ttu-id="e7bcf-114">Beispiel 2: Entfernen einer Ressourcengruppe ohne Bestätigung</span><span class="sxs-lookup"><span data-stu-id="e7bcf-114">Example 2: Remove a resource group without confirmation</span></span>
```
PS C:\>Get-AzResourceGroup -Name "ContosoRG01" | Remove-AzResourceGroup -Force
```

<span data-ttu-id="e7bcf-115">Dieser Befehl verwendet das Get-AzResourceGroup-Cmdlet, um die Ressourcengruppe ContosoRG01 abzurufen, und übergibt Sie dann mithilfe des Pipelineoperators an **Remove-AzResourceGroup** .</span><span class="sxs-lookup"><span data-stu-id="e7bcf-115">This command uses the Get-AzResourceGroup cmdlet to get the resource group ContosoRG01, and then passes it to **Remove-AzResourceGroup** by using the pipeline operator.</span></span> <span data-ttu-id="e7bcf-116">Der Parameter *Force* unterdrückt die Bestätigungsaufforderung.</span><span class="sxs-lookup"><span data-stu-id="e7bcf-116">The *Force* parameter suppresses the confirmation prompt.</span></span>

### <span data-ttu-id="e7bcf-117">Beispiel 3: Entfernen aller Ressourcengruppen</span><span class="sxs-lookup"><span data-stu-id="e7bcf-117">Example 3: Remove all resource groups</span></span>
```
PS C:\>Get-AzResourceGroup | Remove-AzResourceGroup
```

<span data-ttu-id="e7bcf-118">Dieser Befehl verwendet das Cmdlet " **Get-AzResourceGroup** ", um alle Ressourcengruppen abzurufen, und übergibt Sie dann mithilfe des Pipelineoperators an **Remove-AzResourceGroup** .</span><span class="sxs-lookup"><span data-stu-id="e7bcf-118">This command uses the **Get-AzResourceGroup** cmdlet to get all resource groups, and then passes them to **Remove-AzResourceGroup** by using the pipeline operator.</span></span>

## <span data-ttu-id="e7bcf-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="e7bcf-119">PARAMETERS</span></span>

### <span data-ttu-id="e7bcf-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e7bcf-120">-ApiVersion</span></span>
<span data-ttu-id="e7bcf-121">Gibt die API-Version an, die vom Ressourcenanbieter unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="e7bcf-121">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="e7bcf-122">Sie können eine andere Version als die Standard Version angeben.</span><span class="sxs-lookup"><span data-stu-id="e7bcf-122">You can specify a different version than the default version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7bcf-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e7bcf-123">-AsJob</span></span>
<span data-ttu-id="e7bcf-124">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="e7bcf-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e7bcf-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7bcf-125">-DefaultProfile</span></span>
<span data-ttu-id="e7bcf-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="e7bcf-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e7bcf-127">-Force</span><span class="sxs-lookup"><span data-stu-id="e7bcf-127">-Force</span></span>
<span data-ttu-id="e7bcf-128">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="e7bcf-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e7bcf-129">-ID</span><span class="sxs-lookup"><span data-stu-id="e7bcf-129">-Id</span></span>
<span data-ttu-id="e7bcf-130">Gibt die ID der zu entfernenden Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="e7bcf-130">Specifies the ID of resource group to remove.</span></span>
<span data-ttu-id="e7bcf-131">Platzhalterzeichen sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="e7bcf-131">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7bcf-132">-Name</span><span class="sxs-lookup"><span data-stu-id="e7bcf-132">-Name</span></span>
<span data-ttu-id="e7bcf-133">Gibt die Namen der zu entfernenden Ressourcengruppen an.</span><span class="sxs-lookup"><span data-stu-id="e7bcf-133">Specifies the names of resource groups to remove.</span></span>
<span data-ttu-id="e7bcf-134">Platzhalterzeichen sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="e7bcf-134">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupName
Aliases: ResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7bcf-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="e7bcf-135">-Pre</span></span>
<span data-ttu-id="e7bcf-136">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="e7bcf-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="e7bcf-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e7bcf-137">-Confirm</span></span>
<span data-ttu-id="e7bcf-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e7bcf-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7bcf-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7bcf-139">-WhatIf</span></span>
<span data-ttu-id="e7bcf-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e7bcf-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7bcf-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e7bcf-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7bcf-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7bcf-142">CommonParameters</span></span>
<span data-ttu-id="e7bcf-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7bcf-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7bcf-144">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e7bcf-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7bcf-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e7bcf-145">INPUTS</span></span>

### <span data-ttu-id="e7bcf-146">System. String</span><span class="sxs-lookup"><span data-stu-id="e7bcf-146">System.String</span></span>

## <span data-ttu-id="e7bcf-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e7bcf-147">OUTPUTS</span></span>

### <span data-ttu-id="e7bcf-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e7bcf-148">System.Boolean</span></span>

## <span data-ttu-id="e7bcf-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="e7bcf-149">NOTES</span></span>

## <span data-ttu-id="e7bcf-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e7bcf-150">RELATED LINKS</span></span>

[<span data-ttu-id="e7bcf-151">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e7bcf-151">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)

[<span data-ttu-id="e7bcf-152">Neu – AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e7bcf-152">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="e7bcf-153">Satz-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e7bcf-153">Set-AzResourceGroup</span></span>](./Set-AzResourceGroup.md)


