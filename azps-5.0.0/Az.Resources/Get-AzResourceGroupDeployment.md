---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 20CB842B-F7A9-4052-85D9-0DF9586D5FEA
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeployment.md
ms.openlocfilehash: 82df573a658fda9af97778e59819e45359c226fd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301120"
---
# <span data-ttu-id="68fe7-101">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="68fe7-101">Get-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="68fe7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="68fe7-102">SYNOPSIS</span></span>
<span data-ttu-id="68fe7-103">Ruft die Bereitstellungen in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="68fe7-103">Gets the deployments in a resource group.</span></span>

## <span data-ttu-id="68fe7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="68fe7-104">SYNTAX</span></span>

### <span data-ttu-id="68fe7-105">GetByResourceGroupDeploymentName (Standard)</span><span class="sxs-lookup"><span data-stu-id="68fe7-105">GetByResourceGroupDeploymentName (Default)</span></span>
```
Get-AzResourceGroupDeployment [-ResourceGroupName] <String> [[-Name] <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68fe7-106">GetByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="68fe7-106">GetByResourceGroupDeploymentId</span></span>
```
Get-AzResourceGroupDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="68fe7-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="68fe7-107">DESCRIPTION</span></span>
<span data-ttu-id="68fe7-108">Das Cmdlet " **Get-AzResourceGroupDeployment** " Ruft die Bereitstellungen in einer Azure-Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="68fe7-108">The **Get-AzResourceGroupDeployment** cmdlet gets the deployments in an Azure resource group.</span></span>
<span data-ttu-id="68fe7-109">Geben Sie den *Namen* oder den *ID-* Parameter an, um die Ergebnisse zu filtern.</span><span class="sxs-lookup"><span data-stu-id="68fe7-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="68fe7-110">Standardmäßig ruft **Get-AzResourceGroupDeployment** alle Bereitstellungen für eine angegebene Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="68fe7-110">By default, **Get-AzResourceGroupDeployment** gets all deployments for a specified resource group.</span></span>
<span data-ttu-id="68fe7-111">Eine Azure-Ressource ist eine vom Benutzer verwaltete Azure-Entität, beispielsweise ein Datenbankserver, eine Datenbank oder eine Website.</span><span class="sxs-lookup"><span data-stu-id="68fe7-111">An Azure resource is a user-managed Azure entity, such as a database server, database, or web site.</span></span>
<span data-ttu-id="68fe7-112">Eine Azure-Ressourcengruppe ist eine Sammlung von Azure-Ressourcen, die als Einheit bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="68fe7-112">An Azure resource group is a collection of Azure resources that are deployed as a unit.</span></span>
<span data-ttu-id="68fe7-113">Bei einer Bereitstellung handelt es sich um den Vorgang, der die Ressourcen in der Ressourcengruppe zur Verwendung zur Verfügung stellt.</span><span class="sxs-lookup"><span data-stu-id="68fe7-113">A deployment is the operation that makes the resources in the resource group available for use.</span></span>
<span data-ttu-id="68fe7-114">Weitere Informationen zu Azure-Ressourcen und Azure-Ressourcengruppen finden Sie unter New-AzResourceGroup-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68fe7-114">For more information about Azure resources and Azure resource groups, see the New-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="68fe7-115">Sie können dieses Cmdlet für die Nachverfolgung verwenden.</span><span class="sxs-lookup"><span data-stu-id="68fe7-115">You can use this cmdlet for tracking.</span></span>
<span data-ttu-id="68fe7-116">Verwenden Sie zum Debuggen dieses Cmdlet mit dem Cmdlet "Get-AzLog".</span><span class="sxs-lookup"><span data-stu-id="68fe7-116">For debugging, use this cmdlet with the Get-AzLog cmdlet.</span></span>

## <span data-ttu-id="68fe7-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="68fe7-117">EXAMPLES</span></span>

### <span data-ttu-id="68fe7-118">Beispiel 1: Abrufen aller Bereitstellungen für eine Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="68fe7-118">Example 1: Get all deployments for a resource group</span></span>
```
PS C:\>Get-AzResourceGroupDeployment -ResourceGroupName "ContosoLabsRG"
```

<span data-ttu-id="68fe7-119">Dieser Befehl ruft alle Bereitstellungen für die ContosoLabsRG-Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="68fe7-119">This command gets all deployments for the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="68fe7-120">Die Ausgabe zeigt eine Bereitstellung für einen WordPress-Blog, in dem eine Katalogvorlage verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="68fe7-120">The output shows a deployment for a WordPress blog that used a gallery template.</span></span>

### <span data-ttu-id="68fe7-121">Beispiel 2: Abrufen einer Bereitstellung nach Name</span><span class="sxs-lookup"><span data-stu-id="68fe7-121">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzResourceGroupDeployment -ResourceGroupName "ContosoLabsRG" -Name "DeployWebsite01"
```

<span data-ttu-id="68fe7-122">Dieser Befehl ruft die DeployWebsite01-Bereitstellung der ContosoLabsRG-Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="68fe7-122">This command gets the DeployWebsite01 deployment of the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="68fe7-123">Sie können einer Bereitstellung einen Namen zuweisen, wenn Sie Sie mithilfe der Cmdlets **New-AzResourceGroup** oder **New-AzResourceGroupDeployment** erstellen.</span><span class="sxs-lookup"><span data-stu-id="68fe7-123">You can assign a name to a deployment when you create it by using the **New-AzResourceGroup** or **New-AzResourceGroupDeployment** cmdlets.</span></span>
<span data-ttu-id="68fe7-124">Wenn Sie keinen Namen zuweisen, geben die Cmdlets einen Standardnamen basierend auf der Vorlage an, die zum Erstellen der Bereitstellung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="68fe7-124">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="68fe7-125">Beispiel 3: Abrufen der Bereitstellungen aller Ressourcengruppen</span><span class="sxs-lookup"><span data-stu-id="68fe7-125">Example 3: Get the deployments of all resource groups</span></span>
```
PS C:\>Get-AzResourceGroup | Get-AzResourceGroupDeployment | Format-Table ResourceGroupName, DeploymentName, ProvisioningState
```

<span data-ttu-id="68fe7-126">Dieser Befehl ruft mithilfe des Get-AzResourceGroup-Cmdlets alle Ressourcengruppen in Ihrem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="68fe7-126">This command gets all resource groups in your subscription by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="68fe7-127">Der Befehl übergibt die Ressourcengruppen mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68fe7-127">The command passes the resource groups to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="68fe7-128">Das aktuelle Cmdlet ruft alle Bereitstellungen aller Ressourcengruppen im Abonnement ab und übergibt die Ergebnisse an das Format-Table-Cmdlet, um deren **ResourceGroupName** -, **deploymentname** -und **ProvisioningState** -Eigenschaftenwerte anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="68fe7-128">The current cmdlet gets all deployments of all resource groups in the subscription, and passes the results to the Format-Table cmdlet to display their **ResourceGroupName** , **DeploymentName** , and **ProvisioningState** property values.</span></span>

## <span data-ttu-id="68fe7-129">Parameter</span><span class="sxs-lookup"><span data-stu-id="68fe7-129">PARAMETERS</span></span>

### <span data-ttu-id="68fe7-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68fe7-130">-DefaultProfile</span></span>
<span data-ttu-id="68fe7-131">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="68fe7-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="68fe7-132">-ID</span><span class="sxs-lookup"><span data-stu-id="68fe7-132">-Id</span></span>
<span data-ttu-id="68fe7-133">Gibt die ID der Ressourcengruppen Bereitstellung an, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="68fe7-133">Specifies the ID of the resource group deployment to get.</span></span>

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

### <span data-ttu-id="68fe7-134">-Name</span><span class="sxs-lookup"><span data-stu-id="68fe7-134">-Name</span></span>
<span data-ttu-id="68fe7-135">Gibt den Namen der Bereitstellung an, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="68fe7-135">Specifies the name of the deployment to get.</span></span>
<span data-ttu-id="68fe7-136">Platzhalterzeichen sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="68fe7-136">Wildcard characters are not permitted.</span></span>

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

### <span data-ttu-id="68fe7-137">-Pre</span><span class="sxs-lookup"><span data-stu-id="68fe7-137">-Pre</span></span>
<span data-ttu-id="68fe7-138">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="68fe7-138">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="68fe7-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68fe7-139">-ResourceGroupName</span></span>
<span data-ttu-id="68fe7-140">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="68fe7-140">Specifies the name of a resource group.</span></span>
<span data-ttu-id="68fe7-141">Das Cmdlet ruft die Bereitstellungen für die Ressourcengruppe ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="68fe7-141">The cmdlet gets the deployments for the resource group that this parameter specifies.</span></span>
<span data-ttu-id="68fe7-142">Platzhalterzeichen sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="68fe7-142">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="68fe7-143">Dieser Parameter ist erforderlich, und Sie können in jedem Befehl nur eine Ressourcengruppe angeben.</span><span class="sxs-lookup"><span data-stu-id="68fe7-143">This parameter is required and you can specify only one resource group in each command.</span></span>

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

### <span data-ttu-id="68fe7-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68fe7-144">CommonParameters</span></span>
<span data-ttu-id="68fe7-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68fe7-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68fe7-146">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="68fe7-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68fe7-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="68fe7-147">INPUTS</span></span>

### <span data-ttu-id="68fe7-148">System. String</span><span class="sxs-lookup"><span data-stu-id="68fe7-148">System.String</span></span>

## <span data-ttu-id="68fe7-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="68fe7-149">OUTPUTS</span></span>

### <span data-ttu-id="68fe7-150">Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="68fe7-150">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroupDeployment</span></span>

## <span data-ttu-id="68fe7-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="68fe7-151">NOTES</span></span>

## <span data-ttu-id="68fe7-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="68fe7-152">RELATED LINKS</span></span>

[<span data-ttu-id="68fe7-153">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="68fe7-153">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)

[<span data-ttu-id="68fe7-154">Neu – AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="68fe7-154">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="68fe7-155">Neu – AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="68fe7-155">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="68fe7-156">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="68fe7-156">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="68fe7-157">Stopp-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="68fe7-157">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="68fe7-158">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="68fe7-158">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


