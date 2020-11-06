---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 880D321E-30F2-4CAE-B14A-5F6DD8E1DB99
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroup.md
ms.openlocfilehash: 6938cf80f3fa6fb20252e1e4a212133ecd1c62a9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500714"
---
# <span data-ttu-id="0709b-101">Remove-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0709b-101">Remove-AzureRmResourceGroup</span></span>

## <span data-ttu-id="0709b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0709b-102">SYNOPSIS</span></span>
<span data-ttu-id="0709b-103">Entfernt eine Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0709b-103">Removes a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0709b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0709b-104">SYNTAX</span></span>

### <span data-ttu-id="0709b-105">Listet die Ressourcengruppe auf, die auf dem Namen basiert.</span><span class="sxs-lookup"><span data-stu-id="0709b-105">Lists the resource group based in the name.</span></span> <span data-ttu-id="0709b-106">Standard</span><span class="sxs-lookup"><span data-stu-id="0709b-106">(Default)</span></span>
```
Remove-AzureRmResourceGroup [-Name] <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0709b-107">Listet die Ressourcengruppe auf, die in der ID basiert.</span><span class="sxs-lookup"><span data-stu-id="0709b-107">Lists the resource group based in the Id.</span></span>
```
Remove-AzureRmResourceGroup [-Id] <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0709b-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0709b-108">DESCRIPTION</span></span>
<span data-ttu-id="0709b-109">Das Cmdlet **Remove-AzureRmResourceGroup** entfernt eine Azure-Ressourcengruppe und deren Ressourcen aus dem aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0709b-109">The **Remove-AzureRmResourceGroup** cmdlet removes an Azure resource group and its resources from the current subscription.</span></span>
<span data-ttu-id="0709b-110">Verwenden Sie das Remove-AzureRmResource-Cmdlet, um eine Ressource zu löschen, aber die Ressourcengruppe zu belegen.</span><span class="sxs-lookup"><span data-stu-id="0709b-110">To delete a resource, but leave the resource group, use the Remove-AzureRmResource cmdlet.</span></span>

## <span data-ttu-id="0709b-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0709b-111">EXAMPLES</span></span>

### <span data-ttu-id="0709b-112">Beispiel 1: Entfernen einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="0709b-112">Example 1: Remove a resource group</span></span>
```
PS C:\>Remove-AzureRmResourceGroup -Name "ContosoRG01"
```

<span data-ttu-id="0709b-113">Dieser Befehl entfernt die ContosoRG01-Ressourcengruppe aus dem Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0709b-113">This command removes the ContosoRG01 resource group from the subscription.</span></span>
<span data-ttu-id="0709b-114">Das Cmdlet fordert Sie zur Bestätigung auf und gibt keine Ausgabe zurück.</span><span class="sxs-lookup"><span data-stu-id="0709b-114">The cmdlet prompts you for confirmation and returns no output.</span></span>

### <span data-ttu-id="0709b-115">Beispiel 2: Entfernen einer Ressourcengruppe ohne Bestätigung</span><span class="sxs-lookup"><span data-stu-id="0709b-115">Example 2: Remove a resource group without confirmation</span></span>
```
PS C:\>Get-AzureRmResourceGroup -Name "ContosoRG01" | Remove-AzureRmResourceGroup -Verbose -Force
```

<span data-ttu-id="0709b-116">Dieser Befehl verwendet das Get-AzureRmResourceGroup-Cmdlet, um die Ressourcengruppe ContosoRG01 abzurufen, und übergibt Sie dann mithilfe des Pipelineoperators an **Remove-AzureRmResourceGroup** .</span><span class="sxs-lookup"><span data-stu-id="0709b-116">This command uses the Get-AzureRmResourceGroup cmdlet to get the resource group ContosoRG01, and then passes it to **Remove-AzureRmResourceGroup** by using the pipeline operator.</span></span>
<span data-ttu-id="0709b-117">Der allgemeine Parameter *verbose* ruft Statusinformationen zum Vorgang ab, und der Parameter *Force* unterdrückt die Bestätigungsaufforderung.</span><span class="sxs-lookup"><span data-stu-id="0709b-117">The *Verbose* common parameter gets status information about the operation, and the *Force* parameter suppresses the confirmation prompt.</span></span>

### <span data-ttu-id="0709b-118">Beispiel 3: Entfernen aller Ressourcengruppen</span><span class="sxs-lookup"><span data-stu-id="0709b-118">Example 3: Remove all resource groups</span></span>
```
PS C:\>Get-AzureRmResourceGroup | Remove-AzureRmResourceGroup
```

<span data-ttu-id="0709b-119">Dieser Befehl verwendet das Cmdlet " **Get-AzureRmResourceGroup** ", um alle Ressourcengruppen abzurufen, und übergibt Sie dann mithilfe des Pipelineoperators an **Remove-AzureRmResourceGroup** .</span><span class="sxs-lookup"><span data-stu-id="0709b-119">This command uses the **Get-AzureRmResourceGroup** cmdlet to get all resource groups, and then passes them to **Remove-AzureRmResourceGroup** by using the pipeline operator.</span></span>

## <span data-ttu-id="0709b-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="0709b-120">PARAMETERS</span></span>

### <span data-ttu-id="0709b-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="0709b-121">-ApiVersion</span></span>
<span data-ttu-id="0709b-122">Gibt die API-Version an, die vom Ressourcenanbieter unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="0709b-122">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="0709b-123">Sie können eine andere Version als die Standard Version angeben.</span><span class="sxs-lookup"><span data-stu-id="0709b-123">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="0709b-124">-Force</span><span class="sxs-lookup"><span data-stu-id="0709b-124">-Force</span></span>
<span data-ttu-id="0709b-125">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="0709b-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0709b-126">-ID</span><span class="sxs-lookup"><span data-stu-id="0709b-126">-Id</span></span>
<span data-ttu-id="0709b-127">Gibt die ID der zu entfernenden Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="0709b-127">Specifies the ID of resource group to remove.</span></span>
<span data-ttu-id="0709b-128">Platzhalterzeichen sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="0709b-128">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resource group based in the Id.
Aliases: ResourceGroupId, ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0709b-129">-Name</span><span class="sxs-lookup"><span data-stu-id="0709b-129">-Name</span></span>
<span data-ttu-id="0709b-130">Gibt die Namen der zu entfernenden Ressourcengruppen an.</span><span class="sxs-lookup"><span data-stu-id="0709b-130">Specifies the names of resource groups to remove.</span></span>
<span data-ttu-id="0709b-131">Platzhalterzeichen sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="0709b-131">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resource group based in the name.
Aliases: ResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0709b-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="0709b-132">-Pre</span></span>
<span data-ttu-id="0709b-133">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="0709b-133">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="0709b-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0709b-134">-Confirm</span></span>
<span data-ttu-id="0709b-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0709b-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0709b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0709b-136">-WhatIf</span></span>
<span data-ttu-id="0709b-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0709b-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0709b-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0709b-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0709b-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0709b-139">-DefaultProfile</span></span>
<span data-ttu-id="0709b-140">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0709b-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0709b-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0709b-141">CommonParameters</span></span>
<span data-ttu-id="0709b-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0709b-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0709b-143">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0709b-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0709b-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0709b-144">INPUTS</span></span>

### <span data-ttu-id="0709b-145">Keine</span><span class="sxs-lookup"><span data-stu-id="0709b-145">None</span></span>

## <span data-ttu-id="0709b-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0709b-146">OUTPUTS</span></span>

### <span data-ttu-id="0709b-147">Keine</span><span class="sxs-lookup"><span data-stu-id="0709b-147">None</span></span>

## <span data-ttu-id="0709b-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="0709b-148">NOTES</span></span>

## <span data-ttu-id="0709b-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0709b-149">RELATED LINKS</span></span>

[<span data-ttu-id="0709b-150">Get-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0709b-150">Get-AzureRmResourceGroup</span></span>](./Get-AzureRmResourceGroup.md)

[<span data-ttu-id="0709b-151">Neu – AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0709b-151">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="0709b-152">Satz-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0709b-152">Set-AzureRmResourceGroup</span></span>](./Set-AzureRmResourceGroup.md)


