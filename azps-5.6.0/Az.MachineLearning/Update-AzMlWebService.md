---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/powershell/module/az.machinelearning/update-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlWebService.md
ms.openlocfilehash: 510e33655fd2e76383fa89a972c477e65d67f070
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931008"
---
# <span data-ttu-id="e4d11-101">Update-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="e4d11-101">Update-AzMlWebService</span></span>

## <span data-ttu-id="e4d11-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4d11-102">SYNOPSIS</span></span>
<span data-ttu-id="e4d11-103">Aktualisiert die Eigenschaften einer vorhandenen Webdienstressource.</span><span class="sxs-lookup"><span data-stu-id="e4d11-103">Updates properties of an existing web service resource.</span></span>

## <span data-ttu-id="e4d11-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e4d11-104">SYNTAX</span></span>

### <span data-ttu-id="e4d11-105">UpdateFromParameters</span><span class="sxs-lookup"><span data-stu-id="e4d11-105">UpdateFromParameters</span></span>
```
Update-AzMlWebService -ResourceGroupName <String> -Name <String> [-Title <String>] [-Description <String>]
 [-IsReadOnly] [-Keys <WebServiceKeys>] [-StorageAccountKey <String>] [-Diagnostics <DiagnosticsConfiguration>]
 [-RealtimeConfiguration <RealtimeConfiguration>] [-Assets <Hashtable>]
 [-Input <ServiceInputOutputSpecification>] [-Output <ServiceInputOutputSpecification>]
 [-Parameters <Hashtable>] [-Package <GraphPackage>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4d11-106">UpdateFromObject</span><span class="sxs-lookup"><span data-stu-id="e4d11-106">UpdateFromObject</span></span>
```
Update-AzMlWebService -ResourceGroupName <String> -Name <String> -ServiceUpdates <WebService> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4d11-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e4d11-107">DESCRIPTION</span></span>
<span data-ttu-id="e4d11-108">Das Update-AzMlWebService-Cmdlet ermöglicht es Ihnen, die nicht statischen Eigenschaften eines Webdiensts zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="e4d11-108">The Update-AzMlWebService cmdlet allows you to update the non-static properties of a web service.</span></span>
<span data-ttu-id="e4d11-109">Das Cmdlet funktioniert als Patchvorgang.</span><span class="sxs-lookup"><span data-stu-id="e4d11-109">The cmdlet works as a patch operation.</span></span>
<span data-ttu-id="e4d11-110">Übergeben Sie nur die Eigenschaften, die Sie ändern möchten.</span><span class="sxs-lookup"><span data-stu-id="e4d11-110">Pass only the properties that you want modified.</span></span>

## <span data-ttu-id="e4d11-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e4d11-111">EXAMPLES</span></span>

### <span data-ttu-id="e4d11-112">Beispiel 1: Selektive Aktualisierungsargumente</span><span class="sxs-lookup"><span data-stu-id="e4d11-112">Example 1: Selective update arguments</span></span>
```
Update-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Description "new update to description" -Keys @{Primary='changed primary key'} -Diagnostics @{Level='All'}
```

<span data-ttu-id="e4d11-113">Hier ändern wir die Beschreibung, den primären Zugriffsschlüssel und aktivieren die Diagnosesammlung für alle Ablaufverfolgungen während der Laufzeit für den Webdienst.</span><span class="sxs-lookup"><span data-stu-id="e4d11-113">Here, we change the description, primary access key and enable the diagnostics collection for all traces during runtime for the web service.</span></span>

### <span data-ttu-id="e4d11-114">Beispiel 2: Aktualisieren basierend auf einer Webdienstinstanz</span><span class="sxs-lookup"><span data-stu-id="e4d11-114">Example 2: Update based on a web service instance</span></span>
```
$updates = @{ Properties = @{ Title="New Title"; RealtimeConfiguration = @{ MaxConcurrentCalls=25 }}}

Update-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -ServiceUpdates $updates
```

<span data-ttu-id="e4d11-115">Im Beispiel wird zuerst eine Webdienstdefinition erstellt, die nur die zu aktualisierenden Felder enthält, und ruft dann die Update-AzMlWebService auf, um sie mit dem Parameter ServiceUpdates anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="e4d11-115">The example first creates a web service definition, that only contains the fields to be updated, and then calls the Update-AzMlWebService to apply them using the ServiceUpdates parameter.</span></span>

## <span data-ttu-id="e4d11-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e4d11-116">PARAMETERS</span></span>

### <span data-ttu-id="e4d11-117">-Assets</span><span class="sxs-lookup"><span data-stu-id="e4d11-117">-Assets</span></span>
<span data-ttu-id="e4d11-118">Die Gruppe der Ressourcen (z. B. Module, Datasets), aus der der Webdienst ist.</span><span class="sxs-lookup"><span data-stu-id="e4d11-118">The set of assets (e.g. modules, datasets) that make up the web service.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4d11-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4d11-119">-DefaultProfile</span></span>
<span data-ttu-id="e4d11-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="e4d11-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e4d11-121">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e4d11-121">-Description</span></span>
<span data-ttu-id="e4d11-122">Der neue Wert für die Beschreibung des Webdiensts.</span><span class="sxs-lookup"><span data-stu-id="e4d11-122">The new value for the web service's description.</span></span>
<span data-ttu-id="e4d11-123">Dies ist im Swagger-API-Schema des Diensts sichtbar.</span><span class="sxs-lookup"><span data-stu-id="e4d11-123">This is visible in the service's Swagger API schema.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4d11-124">-Diagnose</span><span class="sxs-lookup"><span data-stu-id="e4d11-124">-Diagnostics</span></span>
<span data-ttu-id="e4d11-125">Die Einstellungen, die die Diagnoseverfolgungssammlung für den Webdienst steuern.</span><span class="sxs-lookup"><span data-stu-id="e4d11-125">The settings that control the diagnostics traces collection for the web service.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.DiagnosticsConfiguration
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4d11-126">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="e4d11-126">-Force</span></span>
<span data-ttu-id="e4d11-127">Bitten Sie nicht um Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="e4d11-127">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="e4d11-128">-Eingabe</span><span class="sxs-lookup"><span data-stu-id="e4d11-128">-Input</span></span>
<span data-ttu-id="e4d11-129">Die Definition für die Eingaben des Webdiensts, die als Einschwaggerschemakonstrukt bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="e4d11-129">The definition for the web service's input(s), provided as a Swagger schema construct.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.ServiceInputOutputSpecification
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4d11-130">-IsReadOnly</span><span class="sxs-lookup"><span data-stu-id="e4d11-130">-IsReadOnly</span></span>
<span data-ttu-id="e4d11-131">Gibt an, dass dieser Webdienst gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="e4d11-131">Specifies that this web service is readonly.</span></span>
<span data-ttu-id="e4d11-132">Nach dem Festlegen kann der Webdienst länger aktualisiert werden, einschließlich der Änderung des Werts dieser Eigenschaft, und kann nur gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="e4d11-132">Once set, the web service can longer be updated, including changing the value of this property, and can only be deleted.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4d11-133">-Keys</span><span class="sxs-lookup"><span data-stu-id="e4d11-133">-Keys</span></span>
<span data-ttu-id="e4d11-134">Aktualisiert einen oder beide Zugriffstasten, die zum Authentifizieren von Aufrufen der Laufzeit-APIs des Diensts verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e4d11-134">Updates one or both of the access keys used to authenticate calls to the service's runtime APIs.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebServiceKeys
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4d11-135">-Name</span><span class="sxs-lookup"><span data-stu-id="e4d11-135">-Name</span></span>
<span data-ttu-id="e4d11-136">Der Name der zu aktualisierende Webdienstressource.</span><span class="sxs-lookup"><span data-stu-id="e4d11-136">The name of the web service resource to be updated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4d11-137">-Ausgabe</span><span class="sxs-lookup"><span data-stu-id="e4d11-137">-Output</span></span>
<span data-ttu-id="e4d11-138">Die Definition für die Ausgabe(en) des Webdiensts, die als Einschwaggerschemakonstrukt bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="e4d11-138">The definition for the web service's output(s), provided as a Swagger schema construct.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.ServiceInputOutputSpecification
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4d11-139">-Package</span><span class="sxs-lookup"><span data-stu-id="e4d11-139">-Package</span></span>
<span data-ttu-id="e4d11-140">Die Definition des Diagrammpakets, das diesen Webdienst definiert.</span><span class="sxs-lookup"><span data-stu-id="e4d11-140">The definition of the graph package that defines this web service.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.GraphPackage
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4d11-141">-Parameter</span><span class="sxs-lookup"><span data-stu-id="e4d11-141">-Parameters</span></span>
<span data-ttu-id="e4d11-142">Die Gruppe der für den Webdienst definierten globalen Parameterwerte, die als globaler Parametername angegeben werden – \> Standardwertsammlung.</span><span class="sxs-lookup"><span data-stu-id="e4d11-142">The set of global parameters values defined for the web service, given as a global parameter name -\> default value collection.</span></span>
<span data-ttu-id="e4d11-143">Wenn kein Standardwert angegeben ist, wird der Parameter als erforderlich betrachtet.</span><span class="sxs-lookup"><span data-stu-id="e4d11-143">If no default value is specified, the parameter is considered to be required.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4d11-144">-RealtimeConfiguration</span><span class="sxs-lookup"><span data-stu-id="e4d11-144">-RealtimeConfiguration</span></span>
<span data-ttu-id="e4d11-145">Updates für die Konfiguration des Echtzeitendpunkts des Diensts.</span><span class="sxs-lookup"><span data-stu-id="e4d11-145">Updates for the configuration of the service's realtime endpoint.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.RealtimeConfiguration
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4d11-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4d11-146">-ResourceGroupName</span></span>
<span data-ttu-id="e4d11-147">Die Ressourcengruppe, die den zu aktualisierende Webdienst enthält.</span><span class="sxs-lookup"><span data-stu-id="e4d11-147">The resource group that contains the web service to be updated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4d11-148">-ServiceUpdates</span><span class="sxs-lookup"><span data-stu-id="e4d11-148">-ServiceUpdates</span></span>
<span data-ttu-id="e4d11-149">Eine Reihe von Updates, die für den Webdienst gelten sollen, der als Webdienstdefinitionsinstanz bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="e4d11-149">A set of updates to apply to the web service provided as a web service definition instance.</span></span>
<span data-ttu-id="e4d11-150">Nur nicht statische Felder werden geändert.</span><span class="sxs-lookup"><span data-stu-id="e4d11-150">Only non-static fields are modified.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: UpdateFromObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e4d11-151">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="e4d11-151">-StorageAccountKey</span></span>
<span data-ttu-id="e4d11-152">Dreht den Zugriffsschlüssel für das speicherkonto, das dem Webdienst zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="e4d11-152">Rotates the access key for the storage account associated with the web service.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4d11-153">-Title</span><span class="sxs-lookup"><span data-stu-id="e4d11-153">-Title</span></span>
<span data-ttu-id="e4d11-154">Der neue Wert für den Titel des Webdiensts.</span><span class="sxs-lookup"><span data-stu-id="e4d11-154">The new value for the web service's title.</span></span>
<span data-ttu-id="e4d11-155">Dies ist im Swagger-API-Schema des Diensts sichtbar.</span><span class="sxs-lookup"><span data-stu-id="e4d11-155">This is visible in the service's Swagger API schema.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4d11-156">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e4d11-156">-Confirm</span></span>
<span data-ttu-id="e4d11-157">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e4d11-157">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4d11-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4d11-158">-WhatIf</span></span>
<span data-ttu-id="e4d11-159">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e4d11-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4d11-160">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e4d11-160">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4d11-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4d11-161">CommonParameters</span></span>
<span data-ttu-id="e4d11-162">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4d11-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4d11-163">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4d11-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4d11-164">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e4d11-164">INPUTS</span></span>

### <span data-ttu-id="e4d11-165">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span><span class="sxs-lookup"><span data-stu-id="e4d11-165">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="e4d11-166">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e4d11-166">OUTPUTS</span></span>

### <span data-ttu-id="e4d11-167">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span><span class="sxs-lookup"><span data-stu-id="e4d11-167">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="e4d11-168">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="e4d11-168">NOTES</span></span>
<span data-ttu-id="e4d11-169">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span><span class="sxs-lookup"><span data-stu-id="e4d11-169">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="e4d11-170">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="e4d11-170">RELATED LINKS</span></span>
