---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 20CB842B-F7A9-4052-85D9-0DF9586D5FEA
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeployment.md
ms.openlocfilehash: 82df573a658fda9af97778e59819e45359c226fd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100153689"
---
# <span data-ttu-id="db490-101">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="db490-101">Get-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="db490-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db490-102">SYNOPSIS</span></span>
<span data-ttu-id="db490-103">Ruft die Bereitstellungen in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="db490-103">Gets the deployments in a resource group.</span></span>

## <span data-ttu-id="db490-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="db490-104">SYNTAX</span></span>

### <span data-ttu-id="db490-105">GetByResourceGroupDeploymentName (Standard)</span><span class="sxs-lookup"><span data-stu-id="db490-105">GetByResourceGroupDeploymentName (Default)</span></span>
```
Get-AzResourceGroupDeployment [-ResourceGroupName] <String> [[-Name] <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="db490-106">GetByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="db490-106">GetByResourceGroupDeploymentId</span></span>
```
Get-AzResourceGroupDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="db490-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="db490-107">DESCRIPTION</span></span>
<span data-ttu-id="db490-108">Das **Cmdlet "Get-AzResourceGroupDeployment"** ruft die Bereitstellungen in einer Azure-Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="db490-108">The **Get-AzResourceGroupDeployment** cmdlet gets the deployments in an Azure resource group.</span></span>
<span data-ttu-id="db490-109">Geben Sie den *Parameter "Name"* oder *"ID"* an, um die Ergebnisse zu filtern.</span><span class="sxs-lookup"><span data-stu-id="db490-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="db490-110">Standardmäßig ruft **"Get-AzResourceGroupDeployment"** alle Bereitstellungen für eine bestimmte Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="db490-110">By default, **Get-AzResourceGroupDeployment** gets all deployments for a specified resource group.</span></span>
<span data-ttu-id="db490-111">Eine Azure-Ressource ist eine vom Benutzer verwaltete Azure-Entität, z. B. ein Datenbankserver, eine Datenbank oder eine Website.</span><span class="sxs-lookup"><span data-stu-id="db490-111">An Azure resource is a user-managed Azure entity, such as a database server, database, or web site.</span></span>
<span data-ttu-id="db490-112">Eine Azure-Ressourcengruppe ist eine Sammlung von Azure-Ressourcen, die als Einheit bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="db490-112">An Azure resource group is a collection of Azure resources that are deployed as a unit.</span></span>
<span data-ttu-id="db490-113">Eine Bereitstellung ist der Vorgang, der die Ressourcen in der Ressourcengruppe zur Verwendung zur Verfügung stellt.</span><span class="sxs-lookup"><span data-stu-id="db490-113">A deployment is the operation that makes the resources in the resource group available for use.</span></span>
<span data-ttu-id="db490-114">Weitere Informationen zu Azure-Ressourcen und -Ressourcengruppen finden Sie im New-AzResourceGroup-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db490-114">For more information about Azure resources and Azure resource groups, see the New-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="db490-115">Sie können dieses Cmdlet für die Nachverfolgung verwenden.</span><span class="sxs-lookup"><span data-stu-id="db490-115">You can use this cmdlet for tracking.</span></span>
<span data-ttu-id="db490-116">Verwenden Sie zum Debuggen dieses Cmdlet zusammen mit Get-AzLog Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db490-116">For debugging, use this cmdlet with the Get-AzLog cmdlet.</span></span>

## <span data-ttu-id="db490-117">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="db490-117">EXAMPLES</span></span>

### <span data-ttu-id="db490-118">Beispiel 1: Alle Bereitstellungen für eine Ressourcengruppe erhalten</span><span class="sxs-lookup"><span data-stu-id="db490-118">Example 1: Get all deployments for a resource group</span></span>
```
PS C:\>Get-AzResourceGroupDeployment -ResourceGroupName "ContosoLabsRG"
```

<span data-ttu-id="db490-119">Dieser Befehl ruft alle Bereitstellungen für die Ressourcengruppe "ContosoLabsRG" ab.</span><span class="sxs-lookup"><span data-stu-id="db490-119">This command gets all deployments for the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="db490-120">Die Ausgabe zeigt eine Bereitstellung für einen WordPress-Blog, in dem eine Katalogvorlage verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="db490-120">The output shows a deployment for a WordPress blog that used a gallery template.</span></span>

### <span data-ttu-id="db490-121">Beispiel 2: Benennen einer Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="db490-121">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzResourceGroupDeployment -ResourceGroupName "ContosoLabsRG" -Name "DeployWebsite01"
```

<span data-ttu-id="db490-122">Dieser Befehl ruft die Bereitstellung "DeployWebsite01" der Ressourcengruppe "ContosoLabsRG" ab.</span><span class="sxs-lookup"><span data-stu-id="db490-122">This command gets the DeployWebsite01 deployment of the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="db490-123">Sie können einer Bereitstellung einen Namen zuweisen, wenn Sie sie mithilfe der **Cmdlets "New-AzResourceGroup"** oder **"New-AzResourceGroupDeployment"** erstellen.</span><span class="sxs-lookup"><span data-stu-id="db490-123">You can assign a name to a deployment when you create it by using the **New-AzResourceGroup** or **New-AzResourceGroupDeployment** cmdlets.</span></span>
<span data-ttu-id="db490-124">Wenn Sie keinen Namen zuweisen, geben die Cmdlets einen Standardnamen basierend auf der Vorlage an, die zum Erstellen der Bereitstellung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="db490-124">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="db490-125">Beispiel 3: Erhalten der Bereitstellungen aller Ressourcengruppen</span><span class="sxs-lookup"><span data-stu-id="db490-125">Example 3: Get the deployments of all resource groups</span></span>
```
PS C:\>Get-AzResourceGroup | Get-AzResourceGroupDeployment | Format-Table ResourceGroupName, DeploymentName, ProvisioningState
```

<span data-ttu-id="db490-126">Dieser Befehl ruft alle Ressourcengruppen in Ihrem Abonnement mithilfe des Cmdlets Get-AzResourceGroup ab.</span><span class="sxs-lookup"><span data-stu-id="db490-126">This command gets all resource groups in your subscription by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="db490-127">Der Befehl übergibt die Ressourcengruppen mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db490-127">The command passes the resource groups to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="db490-128">Das aktuelle Cmdlet ruft alle Bereitstellungen aller Ressourcengruppen im Abonnement ab und übergibt die Ergebnisse an das cmdlet Format-Table, um die Eigenschaftswerte **"ResourceGroupName",** **"DeploymentName"** und **"ProvisioningState"** angezeigt zu werden.</span><span class="sxs-lookup"><span data-stu-id="db490-128">The current cmdlet gets all deployments of all resource groups in the subscription, and passes the results to the Format-Table cmdlet to display their **ResourceGroupName**, **DeploymentName**, and **ProvisioningState** property values.</span></span>

## <span data-ttu-id="db490-129">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="db490-129">PARAMETERS</span></span>

### <span data-ttu-id="db490-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db490-130">-DefaultProfile</span></span>
<span data-ttu-id="db490-131">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="db490-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="db490-132">-ID</span><span class="sxs-lookup"><span data-stu-id="db490-132">-Id</span></span>
<span data-ttu-id="db490-133">Gibt die ID der Ressourcengruppenbereitstellung an, die sie erhalten soll.</span><span class="sxs-lookup"><span data-stu-id="db490-133">Specifies the ID of the resource group deployment to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db490-134">-Name</span><span class="sxs-lookup"><span data-stu-id="db490-134">-Name</span></span>
<span data-ttu-id="db490-135">Gibt den Namen der Bereitstellung an, die sie erhalten soll.</span><span class="sxs-lookup"><span data-stu-id="db490-135">Specifies the name of the deployment to get.</span></span>
<span data-ttu-id="db490-136">Platzhalterzeichen sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="db490-136">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupDeploymentName
Aliases: DeploymentName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db490-137">-Pre</span><span class="sxs-lookup"><span data-stu-id="db490-137">-Pre</span></span>
<span data-ttu-id="db490-138">Gibt an, dass dieses Cmdlet Vorabversions-API-Versionen berücksichtigt, wenn automatisch bestimmt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="db490-138">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="db490-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db490-139">-ResourceGroupName</span></span>
<span data-ttu-id="db490-140">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="db490-140">Specifies the name of a resource group.</span></span>
<span data-ttu-id="db490-141">Das Cmdlet ruft die Bereitstellungen für die Ressourcengruppe ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="db490-141">The cmdlet gets the deployments for the resource group that this parameter specifies.</span></span>
<span data-ttu-id="db490-142">Platzhalterzeichen sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="db490-142">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="db490-143">Dieser Parameter ist erforderlich, und Sie können in jedem Befehl nur eine Ressourcengruppe angeben.</span><span class="sxs-lookup"><span data-stu-id="db490-143">This parameter is required and you can specify only one resource group in each command.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db490-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db490-144">CommonParameters</span></span>
<span data-ttu-id="db490-145">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db490-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db490-146">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="db490-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db490-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="db490-147">INPUTS</span></span>

### <span data-ttu-id="db490-148">System.String</span><span class="sxs-lookup"><span data-stu-id="db490-148">System.String</span></span>

## <span data-ttu-id="db490-149">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="db490-149">OUTPUTS</span></span>

### <span data-ttu-id="db490-150">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="db490-150">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroupDeployment</span></span>

## <span data-ttu-id="db490-151">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="db490-151">NOTES</span></span>

## <span data-ttu-id="db490-152">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="db490-152">RELATED LINKS</span></span>

[<span data-ttu-id="db490-153">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="db490-153">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)

[<span data-ttu-id="db490-154">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="db490-154">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="db490-155">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="db490-155">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="db490-156">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="db490-156">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="db490-157">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="db490-157">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="db490-158">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="db490-158">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


