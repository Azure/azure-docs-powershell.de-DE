---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 089954C3-7F3E-46C2-AA93-C0151EACDA2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzResourceGroupDeployment.md
ms.openlocfilehash: fa189637c9c2c1b63ab0e8dd0b00fab3f4505da0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98307120"
---
# <span data-ttu-id="fc358-101">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="fc358-101">Stop-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="fc358-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc358-102">SYNOPSIS</span></span>
<span data-ttu-id="fc358-103">Bricht die Bereitstellung einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="fc358-103">Cancels a resource group deployment.</span></span>

## <span data-ttu-id="fc358-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fc358-104">SYNTAX</span></span>

### <span data-ttu-id="fc358-105">StopByResourceGroupDeploymentName (Standard)</span><span class="sxs-lookup"><span data-stu-id="fc358-105">StopByResourceGroupDeploymentName (Default)</span></span>
```
Stop-AzResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc358-106">StopByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="fc358-106">StopByResourceGroupDeploymentId</span></span>
```
Stop-AzResourceGroupDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc358-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fc358-107">DESCRIPTION</span></span>
<span data-ttu-id="fc358-108">Das **Cmdlet "Stop-AzResourceGroupDeployment"** bricht eine Azure-Ressourcengruppenbereitstellung ab, die gestartet, aber nicht abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="fc358-108">The **Stop-AzResourceGroupDeployment** cmdlet cancels an Azure resource group deployment that has started but not completed.</span></span>
<span data-ttu-id="fc358-109">Um eine Bereitstellung zu beenden, muss die Bereitstellung einen unvollständigen Bereitstellungszustand haben, z. B. "Provisioning", und keinen abgeschlossenen Zustand, z. B. "Provisioned" oder "Failed".</span><span class="sxs-lookup"><span data-stu-id="fc358-109">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>
<span data-ttu-id="fc358-110">Eine Azure-Ressource ist eine vom Benutzer verwaltete Entität, z. B. eine Website, eine Datenbank oder ein Datenbankserver.</span><span class="sxs-lookup"><span data-stu-id="fc358-110">An Azure resource is a user-managed entity, such as a website, database, or database server.</span></span>
<span data-ttu-id="fc358-111">Eine Ressourcengruppe ist eine Sammlung von Ressourcen, die als Einheit bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="fc358-111">A resource group is a collection of resources that are deployed as a unit.</span></span>
<span data-ttu-id="fc358-112">Verwenden Sie zum Bereitstellen einer Ressourcengruppe das New-AzResourceGroupDeployment Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc358-112">To deploy a resource group, use the New-AzResourceGroupDeployment cmdlet.</span></span>
<span data-ttu-id="fc358-113">Das New-AzResource erstellt eine neue Ressource, löst jedoch keinen Bereitstellungsvorgang für Ressourcengruppen aus, der mit diesem Cmdlet beendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="fc358-113">The New-AzResource cmdlet creates a new resource, but it does not trigger a resource group deployment operation that this cmdlet can stop.</span></span>
<span data-ttu-id="fc358-114">Dieses Cmdlet stoppt nur eine ausgeführte Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="fc358-114">This cmdlet stops only one running deployment.</span></span>
<span data-ttu-id="fc358-115">Verwenden Sie den *Parameter "Name",* um eine bestimmte Bereitstellung zu beenden.</span><span class="sxs-lookup"><span data-stu-id="fc358-115">Use the *Name* parameter to stop a specific deployment.</span></span>
<span data-ttu-id="fc358-116">Wenn Sie den Parameter *"Name"* weglassen, sucht **"Stop-AzResourceGroupDeployment"** nach einer laufenden Bereitstellung und beendet sie.</span><span class="sxs-lookup"><span data-stu-id="fc358-116">If you omit the *Name* parameter, **Stop-AzResourceGroupDeployment** searches for a running deployment and stops it.</span></span>
<span data-ttu-id="fc358-117">Wenn das Cmdlet mehr als eine ausgeführte Bereitstellung findet, schlägt der Befehl fehl.</span><span class="sxs-lookup"><span data-stu-id="fc358-117">If the cmdlet finds more than one running deployment, the command fails.</span></span>

## <span data-ttu-id="fc358-118">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fc358-118">EXAMPLES</span></span>

### <span data-ttu-id="fc358-119">Beispiel 1: Starten und Beenden einer Ressourcengruppenbereitstellung</span><span class="sxs-lookup"><span data-stu-id="fc358-119">Example 1: Starting and stopping a resource group deployment</span></span>

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

## <span data-ttu-id="fc358-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fc358-120">PARAMETERS</span></span>

### <span data-ttu-id="fc358-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc358-121">-DefaultProfile</span></span>
<span data-ttu-id="fc358-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="fc358-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fc358-123">-ID</span><span class="sxs-lookup"><span data-stu-id="fc358-123">-Id</span></span>
<span data-ttu-id="fc358-124">Gibt die ID der zu beendenden Ressourcengruppenbereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="fc358-124">Specifies the ID of the resource group deployment to stop.</span></span>

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

### <span data-ttu-id="fc358-125">-Name</span><span class="sxs-lookup"><span data-stu-id="fc358-125">-Name</span></span>
<span data-ttu-id="fc358-126">Gibt den Namen der zu beendenden Ressourcengruppenbereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="fc358-126">Specifies the name of the resource group deployment to stop.</span></span>
<span data-ttu-id="fc358-127">Wenn Sie diesen Parameter nicht angeben, sucht dieses Cmdlet in der Ressourcengruppe nach einer laufenden Bereitstellung und beendet diesen.</span><span class="sxs-lookup"><span data-stu-id="fc358-127">If you do not specify this parameter, this cmdlet searches for a running deployment in the resource group and stops it.</span></span>
<span data-ttu-id="fc358-128">Wenn mehr als eine ausgeführte Bereitstellung gefunden wird, schlägt der Befehl fehl.</span><span class="sxs-lookup"><span data-stu-id="fc358-128">If it finds more than one running deployment, the command fails.</span></span>
<span data-ttu-id="fc358-129">Um den Bereitstellungsnamen zu erhalten, verwenden Sie das Get-AzResourceGroupDeployment Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc358-129">To get the deployment name, use the Get-AzResourceGroupDeployment cmdlet.</span></span>

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

### <span data-ttu-id="fc358-130">-Pre</span><span class="sxs-lookup"><span data-stu-id="fc358-130">-Pre</span></span>
<span data-ttu-id="fc358-131">Gibt an, dass dieses Cmdlet Vorabversions-API-Versionen berücksichtigt, wenn automatisch bestimmt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="fc358-131">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="fc358-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc358-132">-ResourceGroupName</span></span>
<span data-ttu-id="fc358-133">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="fc358-133">Specifies the name of the resource group.</span></span>
<span data-ttu-id="fc358-134">Dieses Cmdlet beendet die Bereitstellung der Ressourcengruppe, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="fc358-134">This cmdlet stops the deployment of the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="fc358-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fc358-135">-Confirm</span></span>
<span data-ttu-id="fc358-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fc358-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc358-137">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="fc358-137">-WhatIf</span></span>
<span data-ttu-id="fc358-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fc358-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc358-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fc358-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc358-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc358-140">CommonParameters</span></span>
<span data-ttu-id="fc358-141">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc358-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc358-142">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fc358-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc358-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fc358-143">INPUTS</span></span>

### <span data-ttu-id="fc358-144">System.String</span><span class="sxs-lookup"><span data-stu-id="fc358-144">System.String</span></span>

## <span data-ttu-id="fc358-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fc358-145">OUTPUTS</span></span>

### <span data-ttu-id="fc358-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fc358-146">System.Boolean</span></span>

## <span data-ttu-id="fc358-147">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="fc358-147">NOTES</span></span>

## <span data-ttu-id="fc358-148">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="fc358-148">RELATED LINKS</span></span>

[<span data-ttu-id="fc358-149">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="fc358-149">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="fc358-150">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="fc358-150">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="fc358-151">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="fc358-151">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="fc358-152">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="fc358-152">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="fc358-153">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="fc358-153">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="fc358-154">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="fc358-154">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


