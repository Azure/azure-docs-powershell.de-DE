---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 20CB842B-F7A9-4052-85D9-0DF9586D5FEA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresourcegroupdeployment
schema: 2.0.0
ms.openlocfilehash: 9da5ee691b440ee24933d658dec3c85b1a7c8ced
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848392"
---
# <span data-ttu-id="e9d7a-101">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e9d7a-101">Get-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="e9d7a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e9d7a-102">SYNOPSIS</span></span>
<span data-ttu-id="e9d7a-103">Ruft die Bereitstellungen in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="e9d7a-103">Gets the deployments in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e9d7a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e9d7a-104">SYNTAX</span></span>

### <span data-ttu-id="e9d7a-105">GetByResourceGroupDeploymentName (Standard)</span><span class="sxs-lookup"><span data-stu-id="e9d7a-105">GetByResourceGroupDeploymentName (Default)</span></span>
```
Get-AzureRmResourceGroupDeployment [-ResourceGroupName] <String> [[-Name] <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e9d7a-106">GetByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="e9d7a-106">GetByResourceGroupDeploymentId</span></span>
```
Get-AzureRmResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e9d7a-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e9d7a-107">DESCRIPTION</span></span>
<span data-ttu-id="e9d7a-108">Das Cmdlet " **Get-AzureRmResourceGroupDeployment** " Ruft die Bereitstellungen in einer Azure-Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="e9d7a-108">The **Get-AzureRmResourceGroupDeployment** cmdlet gets the deployments in an Azure resource group.</span></span>
<span data-ttu-id="e9d7a-109">Geben Sie den *Namen* oder den *ID-* Parameter an, um die Ergebnisse zu filtern.</span><span class="sxs-lookup"><span data-stu-id="e9d7a-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="e9d7a-110">Standardmäßig ruft **Get-AzureRmResourceGroupDeployment** alle Bereitstellungen für eine angegebene Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="e9d7a-110">By default, **Get-AzureRmResourceGroupDeployment** gets all deployments for a specified resource group.</span></span>
<span data-ttu-id="e9d7a-111">Eine Azure-Ressource ist eine vom Benutzer verwaltete Azure-Entität, beispielsweise ein Datenbankserver, eine Datenbank oder eine Website.</span><span class="sxs-lookup"><span data-stu-id="e9d7a-111">An Azure resource is a user-managed Azure entity, such as a database server, database, or web site.</span></span>
<span data-ttu-id="e9d7a-112">Eine Azure-Ressourcengruppe ist eine Sammlung von Azure-Ressourcen, die als Einheit bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="e9d7a-112">An Azure resource group is a collection of Azure resources that are deployed as a unit.</span></span>
<span data-ttu-id="e9d7a-113">Bei einer Bereitstellung handelt es sich um den Vorgang, der die Ressourcen in der Ressourcengruppe zur Verwendung zur Verfügung stellt.</span><span class="sxs-lookup"><span data-stu-id="e9d7a-113">A deployment is the operation that makes the resources in the resource group available for use.</span></span>
<span data-ttu-id="e9d7a-114">Weitere Informationen zu Azure-Ressourcen und Azure-Ressourcengruppen finden Sie unter New-AzureRmResourceGroup-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9d7a-114">For more information about Azure resources and Azure resource groups, see the New-AzureRmResourceGroup cmdlet.</span></span>
<span data-ttu-id="e9d7a-115">Sie können dieses Cmdlet für die Nachverfolgung verwenden.</span><span class="sxs-lookup"><span data-stu-id="e9d7a-115">You can use this cmdlet for tracking.</span></span>
<span data-ttu-id="e9d7a-116">Verwenden Sie zum Debuggen dieses Cmdlet mit dem Cmdlet "Get-AzureRmLog".</span><span class="sxs-lookup"><span data-stu-id="e9d7a-116">For debugging, use this cmdlet with the Get-AzureRmLog cmdlet.</span></span>

## <span data-ttu-id="e9d7a-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e9d7a-117">EXAMPLES</span></span>

### <span data-ttu-id="e9d7a-118">Beispiel 1: Abrufen aller Bereitstellungen für eine Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="e9d7a-118">Example 1: Get all deployments for a resource group</span></span>
```
PS C:\>Get-AzureRmResourceGroupDeployment -ResourceGroupName "ContosoLabsRG"
```

<span data-ttu-id="e9d7a-119">Dieser Befehl ruft alle Bereitstellungen für die ContosoLabsRG-Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="e9d7a-119">This command gets all deployments for the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="e9d7a-120">Die Ausgabe zeigt eine Bereitstellung für einen WordPress-Blog, in dem eine Katalogvorlage verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e9d7a-120">The output shows a deployment for a WordPress blog that used a gallery template.</span></span>

### <span data-ttu-id="e9d7a-121">Beispiel 2: Abrufen einer Bereitstellung nach Name</span><span class="sxs-lookup"><span data-stu-id="e9d7a-121">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzureRmResourceGroupDeployment -ResourceGroupName "ContosoLabsRG" -Name "DeployWebsite01"
```

<span data-ttu-id="e9d7a-122">Dieser Befehl ruft die DeployWebsite01-Bereitstellung der ContosoLabsRG-Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="e9d7a-122">This command gets the DeployWebsite01 deployment of the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="e9d7a-123">Sie können einer Bereitstellung einen Namen zuweisen, wenn Sie Sie mithilfe der Cmdlets **New-AzureRmResourceGroup** oder **New-AzureRmResourceGroupDeployment** erstellen.</span><span class="sxs-lookup"><span data-stu-id="e9d7a-123">You can assign a name to a deployment when you create it by using the **New-AzureRmResourceGroup** or **New-AzureRmResourceGroupDeployment** cmdlets.</span></span>
<span data-ttu-id="e9d7a-124">Wenn Sie keinen Namen zuweisen, geben die Cmdlets einen Standardnamen basierend auf der Vorlage an, die zum Erstellen der Bereitstellung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e9d7a-124">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="e9d7a-125">Beispiel 3: Abrufen der Bereitstellungen aller Ressourcengruppen</span><span class="sxs-lookup"><span data-stu-id="e9d7a-125">Example 3: Get the deployments of all resource groups</span></span>
```
PS C:\>Get-AzureRmResourceGroup | Get-AzureRmResourceGroupDeployment | Format-Table ResourceGroupName, DeploymentName, ProvisioningState
```

<span data-ttu-id="e9d7a-126">Dieser Befehl ruft mithilfe des Get-AzureRmResourceGroup-Cmdlets alle Ressourcengruppen in Ihrem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="e9d7a-126">This command gets all resource groups in your subscription by using the Get-AzureRmResourceGroup cmdlet.</span></span>
<span data-ttu-id="e9d7a-127">Der Befehl übergibt die Ressourcengruppen mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9d7a-127">The command passes the resource groups to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="e9d7a-128">Das aktuelle Cmdlet ruft alle Bereitstellungen aller Ressourcengruppen im Abonnement ab und übergibt die Ergebnisse an das Format-Table-Cmdlet, um deren **ResourceGroupName** -, **deploymentname** -und **ProvisioningState** -Eigenschaftenwerte anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="e9d7a-128">The current cmdlet gets all deployments of all resource groups in the subscription, and passes the results to the Format-Table cmdlet to display their **ResourceGroupName** , **DeploymentName** , and **ProvisioningState** property values.</span></span>

## <span data-ttu-id="e9d7a-129">Parameter</span><span class="sxs-lookup"><span data-stu-id="e9d7a-129">PARAMETERS</span></span>

### <span data-ttu-id="e9d7a-130">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e9d7a-130">-ApiVersion</span></span>
<span data-ttu-id="e9d7a-131">Gibt die API-Version an, die vom Ressourcenanbieter unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="e9d7a-131">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="e9d7a-132">Sie können eine andere Version als die Standard Version angeben.</span><span class="sxs-lookup"><span data-stu-id="e9d7a-132">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="e9d7a-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9d7a-133">-DefaultProfile</span></span>
<span data-ttu-id="e9d7a-134">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="e9d7a-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e9d7a-135">-ID</span><span class="sxs-lookup"><span data-stu-id="e9d7a-135">-Id</span></span>
<span data-ttu-id="e9d7a-136">Gibt die ID der Ressourcengruppen Bereitstellung an, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="e9d7a-136">Specifies the ID of the resource group deployment to get.</span></span>

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

### <span data-ttu-id="e9d7a-137">-Name</span><span class="sxs-lookup"><span data-stu-id="e9d7a-137">-Name</span></span>
<span data-ttu-id="e9d7a-138">Gibt den Namen der Bereitstellung an, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="e9d7a-138">Specifies the name of the deployment to get.</span></span>
<span data-ttu-id="e9d7a-139">Platzhalterzeichen sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="e9d7a-139">Wildcard characters are not permitted.</span></span>

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

### <span data-ttu-id="e9d7a-140">-Pre</span><span class="sxs-lookup"><span data-stu-id="e9d7a-140">-Pre</span></span>
<span data-ttu-id="e9d7a-141">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="e9d7a-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="e9d7a-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9d7a-142">-ResourceGroupName</span></span>
<span data-ttu-id="e9d7a-143">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="e9d7a-143">Specifies the name of a resource group.</span></span>
<span data-ttu-id="e9d7a-144">Das Cmdlet ruft die Bereitstellungen für die Ressourcengruppe ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="e9d7a-144">The cmdlet gets the deployments for the resource group that this parameter specifies.</span></span>
<span data-ttu-id="e9d7a-145">Platzhalterzeichen sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="e9d7a-145">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="e9d7a-146">Dieser Parameter ist erforderlich, und Sie können in jedem Befehl nur eine Ressourcengruppe angeben.</span><span class="sxs-lookup"><span data-stu-id="e9d7a-146">This parameter is required and you can specify only one resource group in each command.</span></span>

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

### <span data-ttu-id="e9d7a-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9d7a-147">CommonParameters</span></span>
<span data-ttu-id="e9d7a-148">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9d7a-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9d7a-149">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9d7a-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9d7a-150">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e9d7a-150">INPUTS</span></span>

### <span data-ttu-id="e9d7a-151">Keine</span><span class="sxs-lookup"><span data-stu-id="e9d7a-151">None</span></span>

## <span data-ttu-id="e9d7a-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e9d7a-152">OUTPUTS</span></span>

### <span data-ttu-id="e9d7a-153">Microsoft. Azure. Commands. ResourceManagement. Models.</span><span class="sxs-lookup"><span data-stu-id="e9d7a-153">Microsoft.Azure.Commands.ResourceManagement.Models.</span></span> <span data-ttu-id="e9d7a-154">PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e9d7a-154">PSResourceGroupDeployment</span></span>

## <span data-ttu-id="e9d7a-155">Notizen</span><span class="sxs-lookup"><span data-stu-id="e9d7a-155">NOTES</span></span>

## <span data-ttu-id="e9d7a-156">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e9d7a-156">RELATED LINKS</span></span>

[<span data-ttu-id="e9d7a-157">Get-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e9d7a-157">Get-AzureRmResourceGroup</span></span>](./Get-AzureRmResourceGroup.md)

[<span data-ttu-id="e9d7a-158">Neu – AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e9d7a-158">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="e9d7a-159">Neu – AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e9d7a-159">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="e9d7a-160">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e9d7a-160">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="e9d7a-161">Stopp-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e9d7a-161">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="e9d7a-162">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e9d7a-162">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


