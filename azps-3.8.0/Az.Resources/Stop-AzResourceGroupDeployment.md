---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 089954C3-7F3E-46C2-AA93-C0151EACDA2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzResourceGroupDeployment.md
ms.openlocfilehash: 01f2aa36a063caec233aa8c1600d4a01727a549b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996413"
---
# <span data-ttu-id="e6bf5-101">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e6bf5-101">Stop-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="e6bf5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e6bf5-102">SYNOPSIS</span></span>
<span data-ttu-id="e6bf5-103">Bricht die Bereitstellung einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="e6bf5-103">Cancels a resource group deployment.</span></span>

## <span data-ttu-id="e6bf5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e6bf5-104">SYNTAX</span></span>

### <span data-ttu-id="e6bf5-105">StopByResourceGroupDeploymentName (Standard)</span><span class="sxs-lookup"><span data-stu-id="e6bf5-105">StopByResourceGroupDeploymentName (Default)</span></span>
```
Stop-AzResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6bf5-106">StopByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="e6bf5-106">StopByResourceGroupDeploymentId</span></span>
```
Stop-AzResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6bf5-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e6bf5-107">DESCRIPTION</span></span>
<span data-ttu-id="e6bf5-108">Das Cmdlet " **Stop-AzResourceGroupDeployment** " bricht eine Azure Resource Group-Bereitstellung ab, die gestartet, aber nicht abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="e6bf5-108">The **Stop-AzResourceGroupDeployment** cmdlet cancels an Azure resource group deployment that has started but not completed.</span></span>
<span data-ttu-id="e6bf5-109">Damit eine Bereitstellung beendet werden kann, muss die Bereitstellung einen unvollständigen Bereitstellungsstatus aufweisen, beispielsweise die Bereitstellung und nicht den Status abgeschlossen, wie bereitgestellt oder fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="e6bf5-109">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>
<span data-ttu-id="e6bf5-110">Eine Azure-Ressource ist eine vom Benutzer verwaltete Entität, beispielsweise eine Website, eine Datenbank oder ein Datenbankserver.</span><span class="sxs-lookup"><span data-stu-id="e6bf5-110">An Azure resource is a user-managed entity, such as a website, database, or database server.</span></span>
<span data-ttu-id="e6bf5-111">Eine Ressourcengruppe ist eine Sammlung von Ressourcen, die als Einheit bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="e6bf5-111">A resource group is a collection of resources that are deployed as a unit.</span></span>
<span data-ttu-id="e6bf5-112">Verwenden Sie das New-AzResourceGroupDeployment-Cmdlet, um eine Ressourcengruppe bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="e6bf5-112">To deploy a resource group, use the New-AzResourceGroupDeployment cmdlet.</span></span>
<span data-ttu-id="e6bf5-113">Das New-AzResource-Cmdlet erstellt eine neue Ressource, löst aber keinen Bereitstellungsvorgang der Ressourcengruppe aus, den dieses Cmdlet beenden kann.</span><span class="sxs-lookup"><span data-stu-id="e6bf5-113">The New-AzResource cmdlet creates a new resource, but it does not trigger a resource group deployment operation that this cmdlet can stop.</span></span>
<span data-ttu-id="e6bf5-114">Dieses Cmdlet beendet nur eine ausgeführte Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="e6bf5-114">This cmdlet stops only one running deployment.</span></span>
<span data-ttu-id="e6bf5-115">Verwenden Sie den Parameter *Name* , um eine bestimmte Bereitstellung zu beenden.</span><span class="sxs-lookup"><span data-stu-id="e6bf5-115">Use the *Name* parameter to stop a specific deployment.</span></span>
<span data-ttu-id="e6bf5-116">Wenn Sie den Parameter *Name* nicht angeben, sucht **Stop-AzResourceGroupDeployment** nach einer ausgeführten Bereitstellung und beendet Sie.</span><span class="sxs-lookup"><span data-stu-id="e6bf5-116">If you omit the *Name* parameter, **Stop-AzResourceGroupDeployment** searches for a running deployment and stops it.</span></span>
<span data-ttu-id="e6bf5-117">Wenn das Cmdlet mehr als eine ausgeführte Bereitstellung findet, schlägt der Befehl fehl.</span><span class="sxs-lookup"><span data-stu-id="e6bf5-117">If the cmdlet finds more than one running deployment, the command fails.</span></span>

## <span data-ttu-id="e6bf5-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e6bf5-118">EXAMPLES</span></span>

### <span data-ttu-id="e6bf5-119">Beispiel 1: starten und Beenden einer Ressourcengruppen Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="e6bf5-119">Example 1: Starting and stopping a resource group deployment</span></span>

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

## <span data-ttu-id="e6bf5-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="e6bf5-120">PARAMETERS</span></span>

### <span data-ttu-id="e6bf5-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e6bf5-121">-ApiVersion</span></span>
<span data-ttu-id="e6bf5-122">Gibt die API-Version an, die vom Ressourcenanbieter unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="e6bf5-122">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="e6bf5-123">Sie können eine andere Version als die Standard Version angeben.</span><span class="sxs-lookup"><span data-stu-id="e6bf5-123">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="e6bf5-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6bf5-124">-DefaultProfile</span></span>
<span data-ttu-id="e6bf5-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="e6bf5-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e6bf5-126">-ID</span><span class="sxs-lookup"><span data-stu-id="e6bf5-126">-Id</span></span>
<span data-ttu-id="e6bf5-127">Gibt die ID der Bereitstellung der Ressourcengruppe an, die beendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e6bf5-127">Specifies the ID of the resource group deployment to stop.</span></span>

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

### <span data-ttu-id="e6bf5-128">-Name</span><span class="sxs-lookup"><span data-stu-id="e6bf5-128">-Name</span></span>
<span data-ttu-id="e6bf5-129">Gibt den Namen der Bereitstellung der Ressourcengruppe an, die beendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e6bf5-129">Specifies the name of the resource group deployment to stop.</span></span>
<span data-ttu-id="e6bf5-130">Wenn Sie diesen Parameter nicht angeben, sucht dieses Cmdlet nach einer ausgeführten Bereitstellung in der Ressourcengruppe und beendet Sie.</span><span class="sxs-lookup"><span data-stu-id="e6bf5-130">If you do not specify this parameter, this cmdlet searches for a running deployment in the resource group and stops it.</span></span>
<span data-ttu-id="e6bf5-131">Wenn Sie mehr als eine ausgeführte Bereitstellung findet, schlägt der Befehl fehl.</span><span class="sxs-lookup"><span data-stu-id="e6bf5-131">If it finds more than one running deployment, the command fails.</span></span>
<span data-ttu-id="e6bf5-132">Verwenden Sie das Get-AzResourceGroupDeployment-Cmdlet, um den Bereitstellungsnamen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e6bf5-132">To get the deployment name, use the Get-AzResourceGroupDeployment cmdlet.</span></span>

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

### <span data-ttu-id="e6bf5-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="e6bf5-133">-Pre</span></span>
<span data-ttu-id="e6bf5-134">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="e6bf5-134">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="e6bf5-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6bf5-135">-ResourceGroupName</span></span>
<span data-ttu-id="e6bf5-136">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="e6bf5-136">Specifies the name of the resource group.</span></span>
<span data-ttu-id="e6bf5-137">Dieses Cmdlet beendet die Bereitstellung der Ressourcengruppe, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="e6bf5-137">This cmdlet stops the deployment of the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="e6bf5-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e6bf5-138">-Confirm</span></span>
<span data-ttu-id="e6bf5-139">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e6bf5-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6bf5-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6bf5-140">-WhatIf</span></span>
<span data-ttu-id="e6bf5-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e6bf5-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6bf5-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e6bf5-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6bf5-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6bf5-143">CommonParameters</span></span>
<span data-ttu-id="e6bf5-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6bf5-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6bf5-145">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e6bf5-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6bf5-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e6bf5-146">INPUTS</span></span>

### <span data-ttu-id="e6bf5-147">System. String</span><span class="sxs-lookup"><span data-stu-id="e6bf5-147">System.String</span></span>

## <span data-ttu-id="e6bf5-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e6bf5-148">OUTPUTS</span></span>

### <span data-ttu-id="e6bf5-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e6bf5-149">System.Boolean</span></span>

## <span data-ttu-id="e6bf5-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="e6bf5-150">NOTES</span></span>

## <span data-ttu-id="e6bf5-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e6bf5-151">RELATED LINKS</span></span>

[<span data-ttu-id="e6bf5-152">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e6bf5-152">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="e6bf5-153">Neu – AzResource</span><span class="sxs-lookup"><span data-stu-id="e6bf5-153">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="e6bf5-154">Neu – AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e6bf5-154">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="e6bf5-155">Neu – AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e6bf5-155">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="e6bf5-156">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e6bf5-156">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="e6bf5-157">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e6bf5-157">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


