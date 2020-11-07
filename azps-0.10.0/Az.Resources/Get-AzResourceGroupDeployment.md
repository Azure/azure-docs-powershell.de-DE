---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 20CB842B-F7A9-4052-85D9-0DF9586D5FEA
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzResourceGroupDeployment.md
ms.openlocfilehash: 2703a5f32142ddd8d5754c89924360564b45d0f9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843419"
---
# <span data-ttu-id="8b0d3-101">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8b0d3-101">Get-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="8b0d3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8b0d3-102">SYNOPSIS</span></span>
<span data-ttu-id="8b0d3-103">Ruft die Bereitstellungen in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="8b0d3-103">Gets the deployments in a resource group.</span></span>

## <span data-ttu-id="8b0d3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8b0d3-104">SYNTAX</span></span>

### <span data-ttu-id="8b0d3-105">GetByResourceGroupDeploymentName (Standard)</span><span class="sxs-lookup"><span data-stu-id="8b0d3-105">GetByResourceGroupDeploymentName (Default)</span></span>
```
Get-AzResourceGroupDeployment [-ResourceGroupName] <String> [[-Name] <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b0d3-106">GetByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="8b0d3-106">GetByResourceGroupDeploymentId</span></span>
```
Get-AzResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b0d3-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8b0d3-107">DESCRIPTION</span></span>
<span data-ttu-id="8b0d3-108">Das Cmdlet " **Get-AzResourceGroupDeployment** " Ruft die Bereitstellungen in einer Azure-Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="8b0d3-108">The **Get-AzResourceGroupDeployment** cmdlet gets the deployments in an Azure resource group.</span></span>
<span data-ttu-id="8b0d3-109">Geben Sie den *Namen* oder den *ID-* Parameter an, um die Ergebnisse zu filtern.</span><span class="sxs-lookup"><span data-stu-id="8b0d3-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="8b0d3-110">Standardmäßig ruft **Get-AzResourceGroupDeployment** alle Bereitstellungen für eine angegebene Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="8b0d3-110">By default, **Get-AzResourceGroupDeployment** gets all deployments for a specified resource group.</span></span>
<span data-ttu-id="8b0d3-111">Eine Azure-Ressource ist eine vom Benutzer verwaltete Azure-Entität, beispielsweise ein Datenbankserver, eine Datenbank oder eine Website.</span><span class="sxs-lookup"><span data-stu-id="8b0d3-111">An Azure resource is a user-managed Azure entity, such as a database server, database, or web site.</span></span>
<span data-ttu-id="8b0d3-112">Eine Azure-Ressourcengruppe ist eine Sammlung von Azure-Ressourcen, die als Einheit bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="8b0d3-112">An Azure resource group is a collection of Azure resources that are deployed as a unit.</span></span>
<span data-ttu-id="8b0d3-113">Bei einer Bereitstellung handelt es sich um den Vorgang, der die Ressourcen in der Ressourcengruppe zur Verwendung zur Verfügung stellt.</span><span class="sxs-lookup"><span data-stu-id="8b0d3-113">A deployment is the operation that makes the resources in the resource group available for use.</span></span>
<span data-ttu-id="8b0d3-114">Weitere Informationen zu Azure-Ressourcen und Azure-Ressourcengruppen finden Sie unter New-AzResourceGroup-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b0d3-114">For more information about Azure resources and Azure resource groups, see the New-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="8b0d3-115">Sie können dieses Cmdlet für die Nachverfolgung verwenden.</span><span class="sxs-lookup"><span data-stu-id="8b0d3-115">You can use this cmdlet for tracking.</span></span>
<span data-ttu-id="8b0d3-116">Verwenden Sie zum Debuggen dieses Cmdlet mit dem Cmdlet "Get-AzLog".</span><span class="sxs-lookup"><span data-stu-id="8b0d3-116">For debugging, use this cmdlet with the Get-AzLog cmdlet.</span></span>

## <span data-ttu-id="8b0d3-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8b0d3-117">EXAMPLES</span></span>

### <span data-ttu-id="8b0d3-118">Beispiel 1: Abrufen aller Bereitstellungen für eine Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="8b0d3-118">Example 1: Get all deployments for a resource group</span></span>
```
PS C:\>Get-AzResourceGroupDeployment -ResourceGroupName "ContosoLabsRG"
```

<span data-ttu-id="8b0d3-119">Dieser Befehl ruft alle Bereitstellungen für die ContosoLabsRG-Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="8b0d3-119">This command gets all deployments for the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="8b0d3-120">Die Ausgabe zeigt eine Bereitstellung für einen WordPress-Blog, in dem eine Katalogvorlage verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8b0d3-120">The output shows a deployment for a WordPress blog that used a gallery template.</span></span>

### <span data-ttu-id="8b0d3-121">Beispiel 2: Abrufen einer Bereitstellung nach Name</span><span class="sxs-lookup"><span data-stu-id="8b0d3-121">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzResourceGroupDeployment -ResourceGroupName "ContosoLabsRG" -Name "DeployWebsite01"
```

<span data-ttu-id="8b0d3-122">Dieser Befehl ruft die DeployWebsite01-Bereitstellung der ContosoLabsRG-Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="8b0d3-122">This command gets the DeployWebsite01 deployment of the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="8b0d3-123">Sie können einer Bereitstellung einen Namen zuweisen, wenn Sie Sie mithilfe der Cmdlets **New-AzResourceGroup** oder **New-AzResourceGroupDeployment** erstellen.</span><span class="sxs-lookup"><span data-stu-id="8b0d3-123">You can assign a name to a deployment when you create it by using the **New-AzResourceGroup** or **New-AzResourceGroupDeployment** cmdlets.</span></span>
<span data-ttu-id="8b0d3-124">Wenn Sie keinen Namen zuweisen, geben die Cmdlets einen Standardnamen basierend auf der Vorlage an, die zum Erstellen der Bereitstellung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8b0d3-124">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="8b0d3-125">Beispiel 3: Abrufen der Bereitstellungen aller Ressourcengruppen</span><span class="sxs-lookup"><span data-stu-id="8b0d3-125">Example 3: Get the deployments of all resource groups</span></span>
```
PS C:\>Get-AzResourceGroup | Get-AzResourceGroupDeployment | Format-Table ResourceGroupName, DeploymentName, ProvisioningState
```

<span data-ttu-id="8b0d3-126">Dieser Befehl ruft mithilfe des Get-AzResourceGroup-Cmdlets alle Ressourcengruppen in Ihrem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="8b0d3-126">This command gets all resource groups in your subscription by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="8b0d3-127">Der Befehl übergibt die Ressourcengruppen mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b0d3-127">The command passes the resource groups to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="8b0d3-128">Das aktuelle Cmdlet ruft alle Bereitstellungen aller Ressourcengruppen im Abonnement ab und übergibt die Ergebnisse an das Format-Table-Cmdlet, um deren **ResourceGroupName** -, **deploymentname** -und **ProvisioningState** -Eigenschaftenwerte anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="8b0d3-128">The current cmdlet gets all deployments of all resource groups in the subscription, and passes the results to the Format-Table cmdlet to display their **ResourceGroupName** , **DeploymentName** , and **ProvisioningState** property values.</span></span>

## <span data-ttu-id="8b0d3-129">Parameter</span><span class="sxs-lookup"><span data-stu-id="8b0d3-129">PARAMETERS</span></span>

### <span data-ttu-id="8b0d3-130">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="8b0d3-130">-ApiVersion</span></span>
<span data-ttu-id="8b0d3-131">Gibt die API-Version an, die vom Ressourcenanbieter unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="8b0d3-131">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="8b0d3-132">Sie können eine andere Version als die Standard Version angeben.</span><span class="sxs-lookup"><span data-stu-id="8b0d3-132">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="8b0d3-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b0d3-133">-DefaultProfile</span></span>
<span data-ttu-id="8b0d3-134">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="8b0d3-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b0d3-135">-ID</span><span class="sxs-lookup"><span data-stu-id="8b0d3-135">-Id</span></span>
<span data-ttu-id="8b0d3-136">Gibt die ID der Ressourcengruppen Bereitstellung an, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="8b0d3-136">Specifies the ID of the resource group deployment to get.</span></span>

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

### <span data-ttu-id="8b0d3-137">-Name</span><span class="sxs-lookup"><span data-stu-id="8b0d3-137">-Name</span></span>
<span data-ttu-id="8b0d3-138">Gibt den Namen der Bereitstellung an, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="8b0d3-138">Specifies the name of the deployment to get.</span></span>
<span data-ttu-id="8b0d3-139">Platzhalterzeichen sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="8b0d3-139">Wildcard characters are not permitted.</span></span>

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

### <span data-ttu-id="8b0d3-140">-Pre</span><span class="sxs-lookup"><span data-stu-id="8b0d3-140">-Pre</span></span>
<span data-ttu-id="8b0d3-141">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="8b0d3-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="8b0d3-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b0d3-142">-ResourceGroupName</span></span>
<span data-ttu-id="8b0d3-143">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="8b0d3-143">Specifies the name of a resource group.</span></span>
<span data-ttu-id="8b0d3-144">Das Cmdlet ruft die Bereitstellungen für die Ressourcengruppe ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="8b0d3-144">The cmdlet gets the deployments for the resource group that this parameter specifies.</span></span>
<span data-ttu-id="8b0d3-145">Platzhalterzeichen sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="8b0d3-145">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="8b0d3-146">Dieser Parameter ist erforderlich, und Sie können in jedem Befehl nur eine Ressourcengruppe angeben.</span><span class="sxs-lookup"><span data-stu-id="8b0d3-146">This parameter is required and you can specify only one resource group in each command.</span></span>

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

### <span data-ttu-id="8b0d3-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b0d3-147">CommonParameters</span></span>
<span data-ttu-id="8b0d3-148">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b0d3-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b0d3-149">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b0d3-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b0d3-150">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8b0d3-150">INPUTS</span></span>

### <span data-ttu-id="8b0d3-151">Keine</span><span class="sxs-lookup"><span data-stu-id="8b0d3-151">None</span></span>

## <span data-ttu-id="8b0d3-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8b0d3-152">OUTPUTS</span></span>

### <span data-ttu-id="8b0d3-153">Microsoft. Azure. Commands. ResourceManagement. Models.</span><span class="sxs-lookup"><span data-stu-id="8b0d3-153">Microsoft.Azure.Commands.ResourceManagement.Models.</span></span> <span data-ttu-id="8b0d3-154">PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8b0d3-154">PSResourceGroupDeployment</span></span>

## <span data-ttu-id="8b0d3-155">Notizen</span><span class="sxs-lookup"><span data-stu-id="8b0d3-155">NOTES</span></span>

## <span data-ttu-id="8b0d3-156">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8b0d3-156">RELATED LINKS</span></span>

[<span data-ttu-id="8b0d3-157">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8b0d3-157">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)

[<span data-ttu-id="8b0d3-158">Neu – AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8b0d3-158">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="8b0d3-159">Neu – AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8b0d3-159">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="8b0d3-160">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8b0d3-160">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="8b0d3-161">Stopp-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8b0d3-161">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="8b0d3-162">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8b0d3-162">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


