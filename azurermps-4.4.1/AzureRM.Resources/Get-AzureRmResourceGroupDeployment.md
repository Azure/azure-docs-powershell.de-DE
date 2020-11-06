---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 20CB842B-F7A9-4052-85D9-0DF9586D5FEA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: e64fdd0300f2ccad4c3904d472563bbc30374b67
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500757"
---
# <span data-ttu-id="29b65-101">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="29b65-101">Get-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="29b65-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="29b65-102">SYNOPSIS</span></span>
<span data-ttu-id="29b65-103">Ruft die Bereitstellungen in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="29b65-103">Gets the deployments in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29b65-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="29b65-104">SYNTAX</span></span>

### <span data-ttu-id="29b65-105">Der Parametersatz für den Bereitstellungsnamen.</span><span class="sxs-lookup"><span data-stu-id="29b65-105">The deployment name parameter set.</span></span> <span data-ttu-id="29b65-106">Standard</span><span class="sxs-lookup"><span data-stu-id="29b65-106">(Default)</span></span>
```
Get-AzureRmResourceGroupDeployment [-ResourceGroupName] <String> [[-Name] <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29b65-107">Der Parametersatz für die Bereitstellungs-ID.</span><span class="sxs-lookup"><span data-stu-id="29b65-107">The deployment Id parameter set.</span></span>
```
Get-AzureRmResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29b65-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="29b65-108">DESCRIPTION</span></span>
<span data-ttu-id="29b65-109">Das Cmdlet " **Get-AzureRmResourceGroupDeployment** " Ruft die Bereitstellungen in einer Azure-Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="29b65-109">The **Get-AzureRmResourceGroupDeployment** cmdlet gets the deployments in an Azure resource group.</span></span>
<span data-ttu-id="29b65-110">Geben Sie den *Namen* oder den *ID-* Parameter an, um die Ergebnisse zu filtern.</span><span class="sxs-lookup"><span data-stu-id="29b65-110">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="29b65-111">Standardmäßig ruft **Get-AzureRmResourceGroupDeployment** alle Bereitstellungen für eine angegebene Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="29b65-111">By default, **Get-AzureRmResourceGroupDeployment** gets all deployments for a specified resource group.</span></span>

<span data-ttu-id="29b65-112">Eine Azure-Ressource ist eine vom Benutzer verwaltete Azure-Entität, beispielsweise ein Datenbankserver, eine Datenbank oder eine Website.</span><span class="sxs-lookup"><span data-stu-id="29b65-112">An Azure resource is a user-managed Azure entity, such as a database server, database, or web site.</span></span>
<span data-ttu-id="29b65-113">Eine Azure-Ressourcengruppe ist eine Sammlung von Azure-Ressourcen, die als Einheit bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="29b65-113">An Azure resource group is a collection of Azure resources that are deployed as a unit.</span></span>

<span data-ttu-id="29b65-114">Bei einer Bereitstellung handelt es sich um den Vorgang, der die Ressourcen in der Ressourcengruppe zur Verwendung zur Verfügung stellt.</span><span class="sxs-lookup"><span data-stu-id="29b65-114">A deployment is the operation that makes the resources in the resource group available for use.</span></span>
<span data-ttu-id="29b65-115">Weitere Informationen zu Azure-Ressourcen und Azure-Ressourcengruppen finden Sie unter New-AzureRmResourceGroup-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29b65-115">For more information about Azure resources and Azure resource groups, see the New-AzureRmResourceGroup cmdlet.</span></span>

<span data-ttu-id="29b65-116">Sie können dieses Cmdlet für die Nachverfolgung verwenden.</span><span class="sxs-lookup"><span data-stu-id="29b65-116">You can use this cmdlet for tracking.</span></span>
<span data-ttu-id="29b65-117">Verwenden Sie zum Debuggen dieses Cmdlet mit dem Cmdlet "Get-AzureRmLog".</span><span class="sxs-lookup"><span data-stu-id="29b65-117">For debugging, use this cmdlet with the Get-AzureRmLog cmdlet.</span></span>

## <span data-ttu-id="29b65-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="29b65-118">EXAMPLES</span></span>

### <span data-ttu-id="29b65-119">Beispiel 1: Abrufen aller Bereitstellungen für eine Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="29b65-119">Example 1: Get all deployments for a resource group</span></span>
```
PS C:\>Get-AzureRmResourceGroupDeployment -ResourceGroupName "ContosoLabsRG"
```

<span data-ttu-id="29b65-120">Dieser Befehl ruft alle Bereitstellungen für die ContosoLabsRG-Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="29b65-120">This command gets all deployments for the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="29b65-121">Die Ausgabe zeigt eine Bereitstellung für einen WordPress-Blog, in dem eine Katalogvorlage verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="29b65-121">The output shows a deployment for a WordPress blog that used a gallery template.</span></span>

### <span data-ttu-id="29b65-122">Beispiel 2: Abrufen einer Bereitstellung nach Name</span><span class="sxs-lookup"><span data-stu-id="29b65-122">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzureRmResourceGroupDeployment -ResourceGroupName "ContosoLabsRG" -Name "DeployWebsite01"
```

<span data-ttu-id="29b65-123">Dieser Befehl ruft die DeployWebsite01-Bereitstellung der ContosoLabsRG-Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="29b65-123">This command gets the DeployWebsite01 deployment of the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="29b65-124">Sie können einer Bereitstellung einen Namen zuweisen, wenn Sie Sie mithilfe der Cmdlets **New-AzureRmResourceGroup** oder **New-AzureRmResourceGroupDeployment** erstellen.</span><span class="sxs-lookup"><span data-stu-id="29b65-124">You can assign a name to a deployment when you create it by using the **New-AzureRmResourceGroup** or **New-AzureRmResourceGroupDeployment** cmdlets.</span></span>
<span data-ttu-id="29b65-125">Wenn Sie keinen Namen zuweisen, geben die Cmdlets einen Standardnamen basierend auf der Vorlage an, die zum Erstellen der Bereitstellung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="29b65-125">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="29b65-126">Beispiel 3: Abrufen der Bereitstellungen aller Ressourcengruppen</span><span class="sxs-lookup"><span data-stu-id="29b65-126">Example 3: Get the deployments of all resource groups</span></span>
```
PS C:\>Get-AzureRmResourceGroup | Get-AzureRmResourceGroupDeployment | Format-Table ResourceGroupName, DeploymentName, ProvisioningState
```

<span data-ttu-id="29b65-127">Dieser Befehl ruft mithilfe des Get-AzureRmResourceGroup-Cmdlets alle Ressourcengruppen in Ihrem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="29b65-127">This command gets all resource groups in your subscription by using the Get-AzureRmResourceGroup cmdlet.</span></span>
<span data-ttu-id="29b65-128">Der Befehl übergibt die Ressourcengruppen mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29b65-128">The command passes the resource groups to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="29b65-129">Das aktuelle Cmdlet ruft alle Bereitstellungen aller Ressourcengruppen im Abonnement ab und übergibt die Ergebnisse an das Format-Table-Cmdlet, um deren **ResourceGroupName** -, **deploymentname** -und **ProvisioningState** -Eigenschaftenwerte anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="29b65-129">The current cmdlet gets all deployments of all resource groups in the subscription, and passes the results to the Format-Table cmdlet to display their **ResourceGroupName** , **DeploymentName** , and **ProvisioningState** property values.</span></span>

## <span data-ttu-id="29b65-130">Parameter</span><span class="sxs-lookup"><span data-stu-id="29b65-130">PARAMETERS</span></span>

### <span data-ttu-id="29b65-131">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="29b65-131">-ApiVersion</span></span>
<span data-ttu-id="29b65-132">Gibt die API-Version an, die vom Ressourcenanbieter unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="29b65-132">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="29b65-133">Sie können eine andere Version als die Standard Version angeben.</span><span class="sxs-lookup"><span data-stu-id="29b65-133">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="29b65-134">-ID</span><span class="sxs-lookup"><span data-stu-id="29b65-134">-Id</span></span>
<span data-ttu-id="29b65-135">Gibt die ID der Ressourcengruppen Bereitstellung an, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="29b65-135">Specifies the ID of the resource group deployment to get.</span></span>

```yaml
Type: System.String
Parameter Sets: The deployment Id parameter set.
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29b65-136">-Name</span><span class="sxs-lookup"><span data-stu-id="29b65-136">-Name</span></span>
<span data-ttu-id="29b65-137">Gibt den Namen der Bereitstellung an, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="29b65-137">Specifies the name of the deployment to get.</span></span>
<span data-ttu-id="29b65-138">Platzhalterzeichen sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="29b65-138">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: The deployment name parameter set.
Aliases: DeploymentName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29b65-139">-Pre</span><span class="sxs-lookup"><span data-stu-id="29b65-139">-Pre</span></span>
<span data-ttu-id="29b65-140">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="29b65-140">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="29b65-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29b65-141">-ResourceGroupName</span></span>
<span data-ttu-id="29b65-142">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="29b65-142">Specifies the name of a resource group.</span></span>
<span data-ttu-id="29b65-143">Das Cmdlet ruft die Bereitstellungen für die Ressourcengruppe ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="29b65-143">The cmdlet gets the deployments for the resource group that this parameter specifies.</span></span>
<span data-ttu-id="29b65-144">Platzhalterzeichen sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="29b65-144">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="29b65-145">Dieser Parameter ist erforderlich, und Sie können in jedem Befehl nur eine Ressourcengruppe angeben.</span><span class="sxs-lookup"><span data-stu-id="29b65-145">This parameter is required and you can specify only one resource group in each command.</span></span>

```yaml
Type: System.String
Parameter Sets: The deployment name parameter set.
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29b65-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29b65-146">-DefaultProfile</span></span>
<span data-ttu-id="29b65-147">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="29b65-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="29b65-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29b65-148">CommonParameters</span></span>
<span data-ttu-id="29b65-149">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29b65-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29b65-150">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29b65-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29b65-151">Eingaben</span><span class="sxs-lookup"><span data-stu-id="29b65-151">INPUTS</span></span>

### <span data-ttu-id="29b65-152">Keine</span><span class="sxs-lookup"><span data-stu-id="29b65-152">None</span></span>

## <span data-ttu-id="29b65-153">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="29b65-153">OUTPUTS</span></span>

### <span data-ttu-id="29b65-154">Microsoft. Azure. Commands. ResourceManagement. Models. PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="29b65-154">Microsoft.Azure.Commands.ResourceManagement.Models.PSResourceGroupDeployment</span></span>
<span data-ttu-id="29b65-155">Das Cmdlet gibt Ressourcengruppen Bereitstellungen zurück.</span><span class="sxs-lookup"><span data-stu-id="29b65-155">The cmdlet returns resource group deployments.</span></span>

## <span data-ttu-id="29b65-156">Notizen</span><span class="sxs-lookup"><span data-stu-id="29b65-156">NOTES</span></span>

## <span data-ttu-id="29b65-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="29b65-157">RELATED LINKS</span></span>

[<span data-ttu-id="29b65-158">Get-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="29b65-158">Get-AzureRmResourceGroup</span></span>](./Get-AzureRmResourceGroup.md)

[<span data-ttu-id="29b65-159">Neu – AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="29b65-159">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="29b65-160">Neu – AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="29b65-160">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="29b65-161">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="29b65-161">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="29b65-162">Stopp-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="29b65-162">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="29b65-163">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="29b65-163">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


