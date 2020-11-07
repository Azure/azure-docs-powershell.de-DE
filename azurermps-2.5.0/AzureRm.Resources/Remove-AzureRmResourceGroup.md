---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 880D321E-30F2-4CAE-B14A-5F6DD8E1DB99
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermresourcegroup
schema: 2.0.0
ms.openlocfilehash: d2038823b769a93d290b9685acf75bbfa86532de
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850216"
---
# <span data-ttu-id="478ec-101">Remove-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="478ec-101">Remove-AzureRmResourceGroup</span></span>

## <span data-ttu-id="478ec-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="478ec-102">SYNOPSIS</span></span>
<span data-ttu-id="478ec-103">Entfernt eine Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="478ec-103">Removes a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="478ec-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="478ec-104">SYNTAX</span></span>

### <span data-ttu-id="478ec-105">RemoveByResourceGroupName (Standard)</span><span class="sxs-lookup"><span data-stu-id="478ec-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzureRmResourceGroup [-Name] <String> [-Force] [-AsJob] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="478ec-106">RemoveByResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="478ec-106">RemoveByResourceGroupId</span></span>
```
Remove-AzureRmResourceGroup [-Id] <String> [-Force] [-AsJob] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="478ec-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="478ec-107">DESCRIPTION</span></span>
<span data-ttu-id="478ec-108">Das Cmdlet **Remove-AzureRmResourceGroup** entfernt eine Azure-Ressourcengruppe und deren Ressourcen aus dem aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="478ec-108">The **Remove-AzureRmResourceGroup** cmdlet removes an Azure resource group and its resources from the current subscription.</span></span>
<span data-ttu-id="478ec-109">Verwenden Sie das Remove-AzureRmResource-Cmdlet, um eine Ressource zu löschen, aber die Ressourcengruppe zu belegen.</span><span class="sxs-lookup"><span data-stu-id="478ec-109">To delete a resource, but leave the resource group, use the Remove-AzureRmResource cmdlet.</span></span>

## <span data-ttu-id="478ec-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="478ec-110">EXAMPLES</span></span>

### <span data-ttu-id="478ec-111">Beispiel 1: Entfernen einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="478ec-111">Example 1: Remove a resource group</span></span>
```
PS C:\>Remove-AzureRmResourceGroup -Name "ContosoRG01"
```

<span data-ttu-id="478ec-112">Dieser Befehl entfernt die ContosoRG01-Ressourcengruppe aus dem Abonnement.</span><span class="sxs-lookup"><span data-stu-id="478ec-112">This command removes the ContosoRG01 resource group from the subscription.</span></span>
<span data-ttu-id="478ec-113">Das Cmdlet fordert Sie zur Bestätigung auf und gibt keine Ausgabe zurück.</span><span class="sxs-lookup"><span data-stu-id="478ec-113">The cmdlet prompts you for confirmation and returns no output.</span></span>

### <span data-ttu-id="478ec-114">Beispiel 2: Entfernen einer Ressourcengruppe ohne Bestätigung</span><span class="sxs-lookup"><span data-stu-id="478ec-114">Example 2: Remove a resource group without confirmation</span></span>
```
PS C:\>Get-AzureRmResourceGroup -Name "ContosoRG01" | Remove-AzureRmResourceGroup -Verbose -Force
```

<span data-ttu-id="478ec-115">Dieser Befehl verwendet das Get-AzureRmResourceGroup-Cmdlet, um die Ressourcengruppe ContosoRG01 abzurufen, und übergibt Sie dann mithilfe des Pipelineoperators an **Remove-AzureRmResourceGroup** .</span><span class="sxs-lookup"><span data-stu-id="478ec-115">This command uses the Get-AzureRmResourceGroup cmdlet to get the resource group ContosoRG01, and then passes it to **Remove-AzureRmResourceGroup** by using the pipeline operator.</span></span>
<span data-ttu-id="478ec-116">Der allgemeine Parameter *verbose* ruft Statusinformationen zum Vorgang ab, und der Parameter *Force* unterdrückt die Bestätigungsaufforderung.</span><span class="sxs-lookup"><span data-stu-id="478ec-116">The *Verbose* common parameter gets status information about the operation, and the *Force* parameter suppresses the confirmation prompt.</span></span>

### <span data-ttu-id="478ec-117">Beispiel 3: Entfernen aller Ressourcengruppen</span><span class="sxs-lookup"><span data-stu-id="478ec-117">Example 3: Remove all resource groups</span></span>
```
PS C:\>Get-AzureRmResourceGroup | Remove-AzureRmResourceGroup
```

<span data-ttu-id="478ec-118">Dieser Befehl verwendet das Cmdlet " **Get-AzureRmResourceGroup** ", um alle Ressourcengruppen abzurufen, und übergibt Sie dann mithilfe des Pipelineoperators an **Remove-AzureRmResourceGroup** .</span><span class="sxs-lookup"><span data-stu-id="478ec-118">This command uses the **Get-AzureRmResourceGroup** cmdlet to get all resource groups, and then passes them to **Remove-AzureRmResourceGroup** by using the pipeline operator.</span></span>

## <span data-ttu-id="478ec-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="478ec-119">PARAMETERS</span></span>

### <span data-ttu-id="478ec-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="478ec-120">-ApiVersion</span></span>
<span data-ttu-id="478ec-121">Gibt die API-Version an, die vom Ressourcenanbieter unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="478ec-121">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="478ec-122">Sie können eine andere Version als die Standard Version angeben.</span><span class="sxs-lookup"><span data-stu-id="478ec-122">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="478ec-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="478ec-123">-AsJob</span></span>
<span data-ttu-id="478ec-124">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="478ec-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="478ec-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="478ec-125">-DefaultProfile</span></span>
<span data-ttu-id="478ec-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="478ec-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="478ec-127">-Force</span><span class="sxs-lookup"><span data-stu-id="478ec-127">-Force</span></span>
<span data-ttu-id="478ec-128">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="478ec-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="478ec-129">-ID</span><span class="sxs-lookup"><span data-stu-id="478ec-129">-Id</span></span>
<span data-ttu-id="478ec-130">Gibt die ID der zu entfernenden Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="478ec-130">Specifies the ID of resource group to remove.</span></span>
<span data-ttu-id="478ec-131">Platzhalterzeichen sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="478ec-131">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="478ec-132">-Name</span><span class="sxs-lookup"><span data-stu-id="478ec-132">-Name</span></span>
<span data-ttu-id="478ec-133">Gibt die Namen der zu entfernenden Ressourcengruppen an.</span><span class="sxs-lookup"><span data-stu-id="478ec-133">Specifies the names of resource groups to remove.</span></span>
<span data-ttu-id="478ec-134">Platzhalterzeichen sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="478ec-134">Wildcard characters are not permitted.</span></span>

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

### <span data-ttu-id="478ec-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="478ec-135">-Pre</span></span>
<span data-ttu-id="478ec-136">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="478ec-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="478ec-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="478ec-137">-Confirm</span></span>
<span data-ttu-id="478ec-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="478ec-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="478ec-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="478ec-139">-WhatIf</span></span>
<span data-ttu-id="478ec-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="478ec-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="478ec-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="478ec-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="478ec-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="478ec-142">CommonParameters</span></span>
<span data-ttu-id="478ec-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="478ec-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="478ec-144">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="478ec-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="478ec-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="478ec-145">INPUTS</span></span>

## <span data-ttu-id="478ec-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="478ec-146">OUTPUTS</span></span>

## <span data-ttu-id="478ec-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="478ec-147">NOTES</span></span>

## <span data-ttu-id="478ec-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="478ec-148">RELATED LINKS</span></span>

[<span data-ttu-id="478ec-149">Get-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="478ec-149">Get-AzureRmResourceGroup</span></span>](./Get-AzureRmResourceGroup.md)

[<span data-ttu-id="478ec-150">Neu – AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="478ec-150">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="478ec-151">Satz-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="478ec-151">Set-AzureRmResourceGroup</span></span>](./Set-AzureRmResourceGroup.md)


