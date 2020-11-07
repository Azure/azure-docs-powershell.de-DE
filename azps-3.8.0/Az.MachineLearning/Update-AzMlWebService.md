---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/update-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlWebService.md
ms.openlocfilehash: a170d21a2301541f1346905ed701d477ecba4204
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846227"
---
# <span data-ttu-id="46a6b-101">Update-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="46a6b-101">Update-AzMlWebService</span></span>

## <span data-ttu-id="46a6b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="46a6b-102">SYNOPSIS</span></span>
<span data-ttu-id="46a6b-103">Aktualisiert Eigenschaften einer vorhandenen Web Service-Ressource.</span><span class="sxs-lookup"><span data-stu-id="46a6b-103">Updates properties of an existing web service resource.</span></span>

## <span data-ttu-id="46a6b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="46a6b-104">SYNTAX</span></span>

### <span data-ttu-id="46a6b-105">UpdateFromParameters</span><span class="sxs-lookup"><span data-stu-id="46a6b-105">UpdateFromParameters</span></span>
```
Update-AzMlWebService -ResourceGroupName <String> -Name <String> [-Title <String>] [-Description <String>]
 [-IsReadOnly] [-Keys <WebServiceKeys>] [-StorageAccountKey <String>] [-Diagnostics <DiagnosticsConfiguration>]
 [-RealtimeConfiguration <RealtimeConfiguration>] [-Assets <Hashtable>]
 [-Input <ServiceInputOutputSpecification>] [-Output <ServiceInputOutputSpecification>]
 [-Parameters <Hashtable>] [-Package <GraphPackage>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46a6b-106">UpdateFromObject</span><span class="sxs-lookup"><span data-stu-id="46a6b-106">UpdateFromObject</span></span>
```
Update-AzMlWebService -ResourceGroupName <String> -Name <String> -ServiceUpdates <WebService> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46a6b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="46a6b-107">DESCRIPTION</span></span>
<span data-ttu-id="46a6b-108">Mit dem Update-AzMlWebService-Cmdlet können Sie die nicht statischen Eigenschaften eines Webdiensts aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="46a6b-108">The Update-AzMlWebService cmdlet allows you to update the non-static properties of a web service.</span></span>
<span data-ttu-id="46a6b-109">Das Cmdlet funktioniert als Patch-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="46a6b-109">The cmdlet works as a patch operation.</span></span>
<span data-ttu-id="46a6b-110">Übergeben Sie nur die Eigenschaften, die Sie ändern möchten.</span><span class="sxs-lookup"><span data-stu-id="46a6b-110">Pass only the properties that you want modified.</span></span>

## <span data-ttu-id="46a6b-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="46a6b-111">EXAMPLES</span></span>

### <span data-ttu-id="46a6b-112">Beispiel 1: selektive Aktualisierungs Argumente</span><span class="sxs-lookup"><span data-stu-id="46a6b-112">Example 1: Selective update arguments</span></span>
```
Update-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Description "new update to description" -Keys @{Primary='changed primary key'} -Diagnostics @{Level='All'}
```

<span data-ttu-id="46a6b-113">Hier werden die Beschreibung, der primäre Zugriffsschlüssel und die Diagnose Sammlung für alle Ablaufverfolgungen während der Laufzeit des Webdiensts geändert.</span><span class="sxs-lookup"><span data-stu-id="46a6b-113">Here, we change the description, primary access key and enable the diagnostics collection for all traces during runtime for the web service.</span></span>

### <span data-ttu-id="46a6b-114">Beispiel 2: Aktualisieren basierend auf einer Webdienst Instanz</span><span class="sxs-lookup"><span data-stu-id="46a6b-114">Example 2: Update based on a web service instance</span></span>
```
$updates = @{ Properties = @{ Title="New Title"; RealtimeConfiguration = @{ MaxConcurrentCalls=25 }}}

Update-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -ServiceUpdates $updates
```

<span data-ttu-id="46a6b-115">Im Beispiel wird zunächst eine Webdienstdefinition erstellt, die nur die zu aktualisierende Felder enthält, und anschließend wird die Update-AzMlWebService aufgerufen, um Sie mithilfe des ServiceUpdates-Parameters anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="46a6b-115">The example first creates a web service definition, that only contains the fields to be updated, and then calls the Update-AzMlWebService to apply them using the ServiceUpdates parameter.</span></span>

## <span data-ttu-id="46a6b-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="46a6b-116">PARAMETERS</span></span>

### <span data-ttu-id="46a6b-117">-Ressourcen</span><span class="sxs-lookup"><span data-stu-id="46a6b-117">-Assets</span></span>
<span data-ttu-id="46a6b-118">Die Gruppe von Ressourcen (z. b. Module, Datasets), aus denen sich der Webdienst befindet.</span><span class="sxs-lookup"><span data-stu-id="46a6b-118">The set of assets (e.g. modules, datasets) that make up the web service.</span></span>

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

### <span data-ttu-id="46a6b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46a6b-119">-DefaultProfile</span></span>
<span data-ttu-id="46a6b-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="46a6b-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="46a6b-121">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="46a6b-121">-Description</span></span>
<span data-ttu-id="46a6b-122">Der neue Wert für die Beschreibung des Webdiensts.</span><span class="sxs-lookup"><span data-stu-id="46a6b-122">The new value for the web service's description.</span></span>
<span data-ttu-id="46a6b-123">Dies ist im Prahlerei-API-Schema des Diensts sichtbar.</span><span class="sxs-lookup"><span data-stu-id="46a6b-123">This is visible in the service's Swagger API schema.</span></span>

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

### <span data-ttu-id="46a6b-124">-Diagnose</span><span class="sxs-lookup"><span data-stu-id="46a6b-124">-Diagnostics</span></span>
<span data-ttu-id="46a6b-125">Die Einstellungen, mit denen die Auflistung der Diagnoseablaufverfolgungen für den Webdienst gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="46a6b-125">The settings that control the diagnostics traces collection for the web service.</span></span>

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

### <span data-ttu-id="46a6b-126">-Force</span><span class="sxs-lookup"><span data-stu-id="46a6b-126">-Force</span></span>
<span data-ttu-id="46a6b-127">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="46a6b-127">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="46a6b-128">-Eingabe</span><span class="sxs-lookup"><span data-stu-id="46a6b-128">-Input</span></span>
<span data-ttu-id="46a6b-129">Die Definition für die Eingabe (n) des Webdiensts, die als Prahlerei-Schema Konstrukt bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="46a6b-129">The definition for the web service's input(s), provided as a Swagger schema construct.</span></span>

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

### <span data-ttu-id="46a6b-130">-IsReadOnly</span><span class="sxs-lookup"><span data-stu-id="46a6b-130">-IsReadOnly</span></span>
<span data-ttu-id="46a6b-131">Gibt an, dass dieser Webdienst schreibgeschützt ist.</span><span class="sxs-lookup"><span data-stu-id="46a6b-131">Specifies that this web service is readonly.</span></span>
<span data-ttu-id="46a6b-132">Nach dem festlegen kann der Webdienst mehr aktualisiert werden, einschließlich der Änderung des Werts dieser Eigenschaft und kann nur gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="46a6b-132">Once set, the web service can longer be updated, including changing the value of this property, and can only be deleted.</span></span>

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

### <span data-ttu-id="46a6b-133">-Keys</span><span class="sxs-lookup"><span data-stu-id="46a6b-133">-Keys</span></span>
<span data-ttu-id="46a6b-134">Aktualisiert eine oder beide Zugriffstasten, die zur Authentifizierung von Anrufen an die Runtime-APIs des Diensts verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="46a6b-134">Updates one or both of the access keys used to authenticate calls to the service's runtime APIs.</span></span>

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

### <span data-ttu-id="46a6b-135">-Name</span><span class="sxs-lookup"><span data-stu-id="46a6b-135">-Name</span></span>
<span data-ttu-id="46a6b-136">Der Name der Webdienst Ressource, die aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="46a6b-136">The name of the web service resource to be updated.</span></span>

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

### <span data-ttu-id="46a6b-137">-Output</span><span class="sxs-lookup"><span data-stu-id="46a6b-137">-Output</span></span>
<span data-ttu-id="46a6b-138">Die Definition für die Ausgabe (n) des Webdiensts, die als Prahlerei-Schema Konstrukt bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="46a6b-138">The definition for the web service's output(s), provided as a Swagger schema construct.</span></span>

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

### <span data-ttu-id="46a6b-139">-Paket</span><span class="sxs-lookup"><span data-stu-id="46a6b-139">-Package</span></span>
<span data-ttu-id="46a6b-140">Die Definition des Graph-Pakets, das diesen Webdienst definiert.</span><span class="sxs-lookup"><span data-stu-id="46a6b-140">The definition of the graph package that defines this web service.</span></span>

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

### <span data-ttu-id="46a6b-141">-Parameter</span><span class="sxs-lookup"><span data-stu-id="46a6b-141">-Parameters</span></span>
<span data-ttu-id="46a6b-142">Der für den Webdienst definierte Satz globaler Parameterwerte als globaler Parameter Name – \> Standardwert Sammlung.</span><span class="sxs-lookup"><span data-stu-id="46a6b-142">The set of global parameters values defined for the web service, given as a global parameter name -\> default value collection.</span></span>
<span data-ttu-id="46a6b-143">Wenn kein Standardwert angegeben wird, gilt der Parameter als erforderlich.</span><span class="sxs-lookup"><span data-stu-id="46a6b-143">If no default value is specified, the parameter is considered to be required.</span></span>

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

### <span data-ttu-id="46a6b-144">-RealtimeConfiguration</span><span class="sxs-lookup"><span data-stu-id="46a6b-144">-RealtimeConfiguration</span></span>
<span data-ttu-id="46a6b-145">Updates für die Konfiguration des Echt Zeit Endpunkts des Diensts.</span><span class="sxs-lookup"><span data-stu-id="46a6b-145">Updates for the configuration of the service's realtime endpoint.</span></span>

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

### <span data-ttu-id="46a6b-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46a6b-146">-ResourceGroupName</span></span>
<span data-ttu-id="46a6b-147">Die Ressourcengruppe mit dem Webdienst, der aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="46a6b-147">The resource group that contains the web service to be updated.</span></span>

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

### <span data-ttu-id="46a6b-148">-ServiceUpdates</span><span class="sxs-lookup"><span data-stu-id="46a6b-148">-ServiceUpdates</span></span>
<span data-ttu-id="46a6b-149">Eine Gruppe von Updates, die für den Webdienst gelten, der als Webdienst Definitions Instanz bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="46a6b-149">A set of updates to apply to the web service provided as a web service definition instance.</span></span>
<span data-ttu-id="46a6b-150">Nur nicht statische Felder werden geändert.</span><span class="sxs-lookup"><span data-stu-id="46a6b-150">Only non-static fields are modified.</span></span>

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

### <span data-ttu-id="46a6b-151">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="46a6b-151">-StorageAccountKey</span></span>
<span data-ttu-id="46a6b-152">Dreht die Zugriffstaste für das dem Webdienst zugeordnete Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="46a6b-152">Rotates the access key for the storage account associated with the web service.</span></span>

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

### <span data-ttu-id="46a6b-153">-Title</span><span class="sxs-lookup"><span data-stu-id="46a6b-153">-Title</span></span>
<span data-ttu-id="46a6b-154">Der neue Wert für den Titel des Webdiensts.</span><span class="sxs-lookup"><span data-stu-id="46a6b-154">The new value for the web service's title.</span></span>
<span data-ttu-id="46a6b-155">Dies ist im Prahlerei-API-Schema des Diensts sichtbar.</span><span class="sxs-lookup"><span data-stu-id="46a6b-155">This is visible in the service's Swagger API schema.</span></span>

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

### <span data-ttu-id="46a6b-156">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="46a6b-156">-Confirm</span></span>
<span data-ttu-id="46a6b-157">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="46a6b-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46a6b-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46a6b-158">-WhatIf</span></span>
<span data-ttu-id="46a6b-159">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="46a6b-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46a6b-160">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="46a6b-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46a6b-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46a6b-161">CommonParameters</span></span>
<span data-ttu-id="46a6b-162">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46a6b-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46a6b-163">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46a6b-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46a6b-164">Eingaben</span><span class="sxs-lookup"><span data-stu-id="46a6b-164">INPUTS</span></span>

### <span data-ttu-id="46a6b-165">Microsoft. Azure. Management. MachineLearning. Webservices. Models. WebService</span><span class="sxs-lookup"><span data-stu-id="46a6b-165">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="46a6b-166">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="46a6b-166">OUTPUTS</span></span>

### <span data-ttu-id="46a6b-167">Microsoft. Azure. Management. MachineLearning. Webservices. Models. WebService</span><span class="sxs-lookup"><span data-stu-id="46a6b-167">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="46a6b-168">Notizen</span><span class="sxs-lookup"><span data-stu-id="46a6b-168">NOTES</span></span>
<span data-ttu-id="46a6b-169">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="46a6b-169">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="46a6b-170">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="46a6b-170">RELATED LINKS</span></span>
