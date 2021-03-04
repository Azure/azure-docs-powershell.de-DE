---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 089954C3-7F3E-46C2-AA93-C0151EACDA2F
online version: https://docs.microsoft.com/powershell/module/az.resources/stop-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzResourceGroupDeployment.md
ms.openlocfilehash: 9258c15578aaeae5102a5d60b2f18a8a4f179d76
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926427"
---
# <span data-ttu-id="0d1ab-101">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0d1ab-101">Stop-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="0d1ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d1ab-102">SYNOPSIS</span></span>
<span data-ttu-id="0d1ab-103">Bricht eine Ressourcengruppenbereitstellung ab.</span><span class="sxs-lookup"><span data-stu-id="0d1ab-103">Cancels a resource group deployment.</span></span>

## <span data-ttu-id="0d1ab-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0d1ab-104">SYNTAX</span></span>

### <span data-ttu-id="0d1ab-105">StopByResourceGroupDeploymentName (Standard)</span><span class="sxs-lookup"><span data-stu-id="0d1ab-105">StopByResourceGroupDeploymentName (Default)</span></span>
```
Stop-AzResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d1ab-106">StopByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="0d1ab-106">StopByResourceGroupDeploymentId</span></span>
```
Stop-AzResourceGroupDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d1ab-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0d1ab-107">DESCRIPTION</span></span>
<span data-ttu-id="0d1ab-108">Das **Cmdlet Stop-AzResourceGroupDeployment** bricht eine Azure-Ressourcengruppenbereitstellung ab, die gestartet, aber nicht abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="0d1ab-108">The **Stop-AzResourceGroupDeployment** cmdlet cancels an Azure resource group deployment that has started but not completed.</span></span>
<span data-ttu-id="0d1ab-109">Um eine Bereitstellung zu beenden, muss die Bereitstellung über einen unvollständigen Bereitstellungszustand verfügen, z. B. Bereitstellung, und nicht über einen abgeschlossenen Zustand wie "Bereitgestellt" oder "Fehlgeschlagen".</span><span class="sxs-lookup"><span data-stu-id="0d1ab-109">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>
<span data-ttu-id="0d1ab-110">Eine Azure-Ressource ist eine vom Benutzer verwaltete Entität, z. B. eine Website, eine Datenbank oder ein Datenbankserver.</span><span class="sxs-lookup"><span data-stu-id="0d1ab-110">An Azure resource is a user-managed entity, such as a website, database, or database server.</span></span>
<span data-ttu-id="0d1ab-111">Eine Ressourcengruppe ist eine Sammlung von Ressourcen, die als Einheit bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="0d1ab-111">A resource group is a collection of resources that are deployed as a unit.</span></span>
<span data-ttu-id="0d1ab-112">Verwenden Sie zum Bereitstellen einer Ressourcengruppe das New-AzResourceGroupDeployment Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d1ab-112">To deploy a resource group, use the New-AzResourceGroupDeployment cmdlet.</span></span>
<span data-ttu-id="0d1ab-113">Das New-AzResource-Cmdlet erstellt eine neue Ressource, löst jedoch keinen Bereitstellungsvorgang für Ressourcengruppen aus, den dieses Cmdlet beenden kann.</span><span class="sxs-lookup"><span data-stu-id="0d1ab-113">The New-AzResource cmdlet creates a new resource, but it does not trigger a resource group deployment operation that this cmdlet can stop.</span></span>
<span data-ttu-id="0d1ab-114">Dieses Cmdlet beendet nur eine ausgeführte Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="0d1ab-114">This cmdlet stops only one running deployment.</span></span>
<span data-ttu-id="0d1ab-115">Verwenden Sie den *Parameter Name,* um eine bestimmte Bereitstellung zu beenden.</span><span class="sxs-lookup"><span data-stu-id="0d1ab-115">Use the *Name* parameter to stop a specific deployment.</span></span>
<span data-ttu-id="0d1ab-116">Wenn Sie den Parameter *Name* weglassen, sucht **Stop-AzResourceGroupDeployment** nach einer ausgeführten Bereitstellung und beendet sie.</span><span class="sxs-lookup"><span data-stu-id="0d1ab-116">If you omit the *Name* parameter, **Stop-AzResourceGroupDeployment** searches for a running deployment and stops it.</span></span>
<span data-ttu-id="0d1ab-117">Wenn das Cmdlet mehrere ausgeführte Bereitstellungen findet, schlägt der Befehl fehl.</span><span class="sxs-lookup"><span data-stu-id="0d1ab-117">If the cmdlet finds more than one running deployment, the command fails.</span></span>

## <span data-ttu-id="0d1ab-118">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0d1ab-118">EXAMPLES</span></span>

### <span data-ttu-id="0d1ab-119">Beispiel 1: Starten und Beenden einer Ressourcengruppenbereitstellung</span><span class="sxs-lookup"><span data-stu-id="0d1ab-119">Example 1: Starting and stopping a resource group deployment</span></span>

```powershell
PS C:\> New-AzResourceGroupDeployment -Name mynewstorageaccount -ResourceGroupName myrg -TemplateFile .\storage-account-create-azdeploy.json -TemplateParameterFile .\storage-account-create-azdeploy.parameters.json -AsJob

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
1      Long Running... AzureLongRun... Running       True            localhost            New-AzResourceGro...

PS C:\> Stop-AzResourceGroupDeployment -Name mynewstorageaccount -ResourceGroupName myrg
True

PS C:\> Get-Job 1

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
1      Long Running... AzureLongRun... Failed        True            localhost            New-AzResourceGro...
```

## <span data-ttu-id="0d1ab-120">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="0d1ab-120">PARAMETERS</span></span>

### <span data-ttu-id="0d1ab-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d1ab-121">-DefaultProfile</span></span>
<span data-ttu-id="0d1ab-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="0d1ab-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0d1ab-123">-ID</span><span class="sxs-lookup"><span data-stu-id="0d1ab-123">-Id</span></span>
<span data-ttu-id="0d1ab-124">Gibt die ID der Ressourcengruppenbereitstellung an, die beendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0d1ab-124">Specifies the ID of the resource group deployment to stop.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByResourceGroupDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d1ab-125">-Name</span><span class="sxs-lookup"><span data-stu-id="0d1ab-125">-Name</span></span>
<span data-ttu-id="0d1ab-126">Gibt den Namen der Ressourcengruppenbereitstellung an, die beendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0d1ab-126">Specifies the name of the resource group deployment to stop.</span></span>
<span data-ttu-id="0d1ab-127">Wenn Sie diesen Parameter nicht angeben, sucht dieses Cmdlet nach einer ausgeführten Bereitstellung in der Ressourcengruppe und beendet sie.</span><span class="sxs-lookup"><span data-stu-id="0d1ab-127">If you do not specify this parameter, this cmdlet searches for a running deployment in the resource group and stops it.</span></span>
<span data-ttu-id="0d1ab-128">Wenn mehrere ausgeführte Bereitstellungen gefunden werden, schlägt der Befehl fehl.</span><span class="sxs-lookup"><span data-stu-id="0d1ab-128">If it finds more than one running deployment, the command fails.</span></span>
<span data-ttu-id="0d1ab-129">Um den Bereitstellungsnamen zu erhalten, verwenden Sie das Get-AzResourceGroupDeployment Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d1ab-129">To get the deployment name, use the Get-AzResourceGroupDeployment cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByResourceGroupDeploymentName
Aliases: DeploymentName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d1ab-130">-Pre</span><span class="sxs-lookup"><span data-stu-id="0d1ab-130">-Pre</span></span>
<span data-ttu-id="0d1ab-131">Gibt an, dass dieses Cmdlet Vorabversions-API-Versionen berücksichtigt, wenn automatisch bestimmt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0d1ab-131">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="0d1ab-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d1ab-132">-ResourceGroupName</span></span>
<span data-ttu-id="0d1ab-133">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="0d1ab-133">Specifies the name of the resource group.</span></span>
<span data-ttu-id="0d1ab-134">Dieses Cmdlet beendet die Bereitstellung der Ressourcengruppe, die von diesem Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0d1ab-134">This cmdlet stops the deployment of the resource group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByResourceGroupDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d1ab-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0d1ab-135">-Confirm</span></span>
<span data-ttu-id="0d1ab-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0d1ab-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d1ab-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d1ab-137">-WhatIf</span></span>
<span data-ttu-id="0d1ab-138">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0d1ab-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d1ab-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0d1ab-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d1ab-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d1ab-140">CommonParameters</span></span>
<span data-ttu-id="0d1ab-141">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d1ab-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d1ab-142">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0d1ab-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d1ab-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0d1ab-143">INPUTS</span></span>

### <span data-ttu-id="0d1ab-144">System.String</span><span class="sxs-lookup"><span data-stu-id="0d1ab-144">System.String</span></span>

## <span data-ttu-id="0d1ab-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0d1ab-145">OUTPUTS</span></span>

### <span data-ttu-id="0d1ab-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0d1ab-146">System.Boolean</span></span>

## <span data-ttu-id="0d1ab-147">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="0d1ab-147">NOTES</span></span>

## <span data-ttu-id="0d1ab-148">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="0d1ab-148">RELATED LINKS</span></span>

[<span data-ttu-id="0d1ab-149">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0d1ab-149">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="0d1ab-150">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="0d1ab-150">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="0d1ab-151">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0d1ab-151">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="0d1ab-152">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0d1ab-152">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="0d1ab-153">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0d1ab-153">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="0d1ab-154">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0d1ab-154">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


