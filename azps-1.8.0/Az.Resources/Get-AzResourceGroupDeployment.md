---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 20CB842B-F7A9-4052-85D9-0DF9586D5FEA
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeployment.md
ms.openlocfilehash: e6f6be148757bb2f30ac0f09575907669ddc195b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659631"
---
# <span data-ttu-id="b1f89-101">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b1f89-101">Get-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="b1f89-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b1f89-102">SYNOPSIS</span></span>
<span data-ttu-id="b1f89-103">Ruft die Bereitstellungen in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="b1f89-103">Gets the deployments in a resource group.</span></span>

## <span data-ttu-id="b1f89-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b1f89-104">SYNTAX</span></span>

### <span data-ttu-id="b1f89-105">GetByResourceGroupDeploymentName (Standard)</span><span class="sxs-lookup"><span data-stu-id="b1f89-105">GetByResourceGroupDeploymentName (Default)</span></span>
```
Get-AzResourceGroupDeployment [-ResourceGroupName] <String> [[-Name] <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1f89-106">GetByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="b1f89-106">GetByResourceGroupDeploymentId</span></span>
```
Get-AzResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1f89-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b1f89-107">DESCRIPTION</span></span>
<span data-ttu-id="b1f89-108">Das Cmdlet " **Get-AzResourceGroupDeployment** " Ruft die Bereitstellungen in einer Azure-Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="b1f89-108">The **Get-AzResourceGroupDeployment** cmdlet gets the deployments in an Azure resource group.</span></span>
<span data-ttu-id="b1f89-109">Geben Sie den *Namen* oder den *ID-* Parameter an, um die Ergebnisse zu filtern.</span><span class="sxs-lookup"><span data-stu-id="b1f89-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="b1f89-110">Standardmäßig ruft **Get-AzResourceGroupDeployment** alle Bereitstellungen für eine angegebene Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="b1f89-110">By default, **Get-AzResourceGroupDeployment** gets all deployments for a specified resource group.</span></span>
<span data-ttu-id="b1f89-111">Eine Azure-Ressource ist eine vom Benutzer verwaltete Azure-Entität, beispielsweise ein Datenbankserver, eine Datenbank oder eine Website.</span><span class="sxs-lookup"><span data-stu-id="b1f89-111">An Azure resource is a user-managed Azure entity, such as a database server, database, or web site.</span></span>
<span data-ttu-id="b1f89-112">Eine Azure-Ressourcengruppe ist eine Sammlung von Azure-Ressourcen, die als Einheit bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="b1f89-112">An Azure resource group is a collection of Azure resources that are deployed as a unit.</span></span>
<span data-ttu-id="b1f89-113">Bei einer Bereitstellung handelt es sich um den Vorgang, der die Ressourcen in der Ressourcengruppe zur Verwendung zur Verfügung stellt.</span><span class="sxs-lookup"><span data-stu-id="b1f89-113">A deployment is the operation that makes the resources in the resource group available for use.</span></span>
<span data-ttu-id="b1f89-114">Weitere Informationen zu Azure-Ressourcen und Azure-Ressourcengruppen finden Sie unter New-AzResourceGroup-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1f89-114">For more information about Azure resources and Azure resource groups, see the New-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="b1f89-115">Sie können dieses Cmdlet für die Nachverfolgung verwenden.</span><span class="sxs-lookup"><span data-stu-id="b1f89-115">You can use this cmdlet for tracking.</span></span>
<span data-ttu-id="b1f89-116">Verwenden Sie zum Debuggen dieses Cmdlet mit dem Cmdlet "Get-AzLog".</span><span class="sxs-lookup"><span data-stu-id="b1f89-116">For debugging, use this cmdlet with the Get-AzLog cmdlet.</span></span>

## <span data-ttu-id="b1f89-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b1f89-117">EXAMPLES</span></span>

### <span data-ttu-id="b1f89-118">Beispiel 1: Abrufen aller Bereitstellungen für eine Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="b1f89-118">Example 1: Get all deployments for a resource group</span></span>
```
PS C:\>Get-AzResourceGroupDeployment -ResourceGroupName "ContosoLabsRG"
```

<span data-ttu-id="b1f89-119">Dieser Befehl ruft alle Bereitstellungen für die ContosoLabsRG-Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="b1f89-119">This command gets all deployments for the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="b1f89-120">Die Ausgabe zeigt eine Bereitstellung für einen WordPress-Blog, in dem eine Katalogvorlage verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b1f89-120">The output shows a deployment for a WordPress blog that used a gallery template.</span></span>

### <span data-ttu-id="b1f89-121">Beispiel 2: Abrufen einer Bereitstellung nach Name</span><span class="sxs-lookup"><span data-stu-id="b1f89-121">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzResourceGroupDeployment -ResourceGroupName "ContosoLabsRG" -Name "DeployWebsite01"
```

<span data-ttu-id="b1f89-122">Dieser Befehl ruft die DeployWebsite01-Bereitstellung der ContosoLabsRG-Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="b1f89-122">This command gets the DeployWebsite01 deployment of the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="b1f89-123">Sie können einer Bereitstellung einen Namen zuweisen, wenn Sie Sie mithilfe der Cmdlets **New-AzResourceGroup** oder **New-AzResourceGroupDeployment** erstellen.</span><span class="sxs-lookup"><span data-stu-id="b1f89-123">You can assign a name to a deployment when you create it by using the **New-AzResourceGroup** or **New-AzResourceGroupDeployment** cmdlets.</span></span>
<span data-ttu-id="b1f89-124">Wenn Sie keinen Namen zuweisen, geben die Cmdlets einen Standardnamen basierend auf der Vorlage an, die zum Erstellen der Bereitstellung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b1f89-124">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="b1f89-125">Beispiel 3: Abrufen der Bereitstellungen aller Ressourcengruppen</span><span class="sxs-lookup"><span data-stu-id="b1f89-125">Example 3: Get the deployments of all resource groups</span></span>
```
PS C:\>Get-AzResourceGroup | Get-AzResourceGroupDeployment | Format-Table ResourceGroupName, DeploymentName, ProvisioningState
```

<span data-ttu-id="b1f89-126">Dieser Befehl ruft mithilfe des Get-AzResourceGroup-Cmdlets alle Ressourcengruppen in Ihrem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="b1f89-126">This command gets all resource groups in your subscription by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="b1f89-127">Der Befehl übergibt die Ressourcengruppen mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1f89-127">The command passes the resource groups to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b1f89-128">Das aktuelle Cmdlet ruft alle Bereitstellungen aller Ressourcengruppen im Abonnement ab und übergibt die Ergebnisse an das Format-Table-Cmdlet, um deren **ResourceGroupName** -, **deploymentname** -und **ProvisioningState** -Eigenschaftenwerte anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="b1f89-128">The current cmdlet gets all deployments of all resource groups in the subscription, and passes the results to the Format-Table cmdlet to display their **ResourceGroupName** , **DeploymentName** , and **ProvisioningState** property values.</span></span>

## <span data-ttu-id="b1f89-129">Parameter</span><span class="sxs-lookup"><span data-stu-id="b1f89-129">PARAMETERS</span></span>

### <span data-ttu-id="b1f89-130">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b1f89-130">-ApiVersion</span></span>
<span data-ttu-id="b1f89-131">Gibt die API-Version an, die vom Ressourcenanbieter unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="b1f89-131">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="b1f89-132">Sie können eine andere Version als die Standard Version angeben.</span><span class="sxs-lookup"><span data-stu-id="b1f89-132">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="b1f89-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1f89-133">-DefaultProfile</span></span>
<span data-ttu-id="b1f89-134">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="b1f89-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b1f89-135">-ID</span><span class="sxs-lookup"><span data-stu-id="b1f89-135">-Id</span></span>
<span data-ttu-id="b1f89-136">Gibt die ID der Ressourcengruppen Bereitstellung an, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="b1f89-136">Specifies the ID of the resource group deployment to get.</span></span>

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

### <span data-ttu-id="b1f89-137">-Name</span><span class="sxs-lookup"><span data-stu-id="b1f89-137">-Name</span></span>
<span data-ttu-id="b1f89-138">Gibt den Namen der Bereitstellung an, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="b1f89-138">Specifies the name of the deployment to get.</span></span>
<span data-ttu-id="b1f89-139">Platzhalterzeichen sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="b1f89-139">Wildcard characters are not permitted.</span></span>

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

### <span data-ttu-id="b1f89-140">-Pre</span><span class="sxs-lookup"><span data-stu-id="b1f89-140">-Pre</span></span>
<span data-ttu-id="b1f89-141">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="b1f89-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="b1f89-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1f89-142">-ResourceGroupName</span></span>
<span data-ttu-id="b1f89-143">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="b1f89-143">Specifies the name of a resource group.</span></span>
<span data-ttu-id="b1f89-144">Das Cmdlet ruft die Bereitstellungen für die Ressourcengruppe ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="b1f89-144">The cmdlet gets the deployments for the resource group that this parameter specifies.</span></span>
<span data-ttu-id="b1f89-145">Platzhalterzeichen sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="b1f89-145">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="b1f89-146">Dieser Parameter ist erforderlich, und Sie können in jedem Befehl nur eine Ressourcengruppe angeben.</span><span class="sxs-lookup"><span data-stu-id="b1f89-146">This parameter is required and you can specify only one resource group in each command.</span></span>

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

### <span data-ttu-id="b1f89-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1f89-147">CommonParameters</span></span>
<span data-ttu-id="b1f89-148">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1f89-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1f89-149">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1f89-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1f89-150">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b1f89-150">INPUTS</span></span>

### <span data-ttu-id="b1f89-151">System. String</span><span class="sxs-lookup"><span data-stu-id="b1f89-151">System.String</span></span>

## <span data-ttu-id="b1f89-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b1f89-152">OUTPUTS</span></span>

### <span data-ttu-id="b1f89-153">Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b1f89-153">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroupDeployment</span></span>

## <span data-ttu-id="b1f89-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="b1f89-154">NOTES</span></span>

## <span data-ttu-id="b1f89-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b1f89-155">RELATED LINKS</span></span>

[<span data-ttu-id="b1f89-156">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b1f89-156">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)

[<span data-ttu-id="b1f89-157">Neu – AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b1f89-157">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="b1f89-158">Neu – AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b1f89-158">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="b1f89-159">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b1f89-159">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="b1f89-160">Stopp-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b1f89-160">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="b1f89-161">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b1f89-161">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


