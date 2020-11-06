---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Update-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Update-AzureRmMlWebService.md
ms.openlocfilehash: 75f94e5c93f81fa88dd33c3c0b94cb2b36ca291f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499994"
---
# <span data-ttu-id="cd900-101">Update-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="cd900-101">Update-AzureRmMlWebService</span></span>

## <span data-ttu-id="cd900-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cd900-102">SYNOPSIS</span></span>
<span data-ttu-id="cd900-103">Aktualisiert Eigenschaften einer vorhandenen Web Service-Ressource.</span><span class="sxs-lookup"><span data-stu-id="cd900-103">Updates properties of an existing web service resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd900-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cd900-104">SYNTAX</span></span>

### <span data-ttu-id="cd900-105">Aktualisieren Sie bestimmte Eigenschaften von.</span><span class="sxs-lookup"><span data-stu-id="cd900-105">Update specific properties of the .</span></span>
```
Update-AzureRmMlWebService -ResourceGroupName <String> -Name <String> [-Title <String>] [-Description <String>]
 [-IsReadOnly] [-Keys <WebServiceKeys>] [-StorageAccountKey <String>] [-Diagnostics <DiagnosticsConfiguration>]
 [-RealtimeConfiguration <RealtimeConfiguration>] [-Assets <Hashtable>]
 [-Input <ServiceInputOutputSpecification>] [-Output <ServiceInputOutputSpecification>]
 [-Parameters <Hashtable>] [-Package <GraphPackage>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd900-106">Erstellen Sie einen neuen Azure-ml-Webservice aus einer Webservice-Instanzen Definition.</span><span class="sxs-lookup"><span data-stu-id="cd900-106">Create a new Azure ML webservice from a WebService instance definition.</span></span>
```
Update-AzureRmMlWebService -ResourceGroupName <String> -Name <String> -ServiceUpdates <WebService> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd900-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cd900-107">DESCRIPTION</span></span>
<span data-ttu-id="cd900-108">Mit dem Update-AzureRmMlWebService-Cmdlet können Sie die nicht statischen Eigenschaften eines Webdiensts aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="cd900-108">The Update-AzureRmMlWebService cmdlet allows you to update the non-static properties of a web service.</span></span>
<span data-ttu-id="cd900-109">Das Cmdlet funktioniert als Patch-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="cd900-109">The cmdlet works as a patch operation.</span></span>
<span data-ttu-id="cd900-110">Übergeben Sie nur die Eigenschaften, die Sie ändern möchten.</span><span class="sxs-lookup"><span data-stu-id="cd900-110">Pass only the properties that you want modified.</span></span>

## <span data-ttu-id="cd900-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cd900-111">EXAMPLES</span></span>

### <span data-ttu-id="cd900-112">--------------------------Beispiel 1: selektive Aktualisierungs Argumente--------------------------</span><span class="sxs-lookup"><span data-stu-id="cd900-112">--------------------------  Example 1: Selective update arguments  --------------------------</span></span>
<span data-ttu-id="cd900-113">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="cd900-113">@{paragraph=PS C:\\\>}</span></span>





```
Update-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Description "new update to description" -Keys @{Primary='changed primary key'} -Diagnostics @{Level='All'}
```

<span data-ttu-id="cd900-114">Hier werden die Beschreibung, der primäre Zugriffsschlüssel und die Diagnose Sammlung für alle Ablaufverfolgungen während der Laufzeit des Webdiensts geändert.</span><span class="sxs-lookup"><span data-stu-id="cd900-114">Here, we change the description, primary access key and enable the diagnostics collection for all traces during runtime for the web service.</span></span>

### <span data-ttu-id="cd900-115">--------------------------Beispiel 2: Update auf Grundlage einer Webdienst Instanz--------------------------</span><span class="sxs-lookup"><span data-stu-id="cd900-115">--------------------------  Example 2: Update based on a web service instance  --------------------------</span></span>
<span data-ttu-id="cd900-116">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="cd900-116">@{paragraph=PS C:\\\>}</span></span>





```
$updates = @{ Properties = @{ Title="New Title"; RealtimeConfiguration = @{ MaxConcurrentCalls=25 }}}

Update-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -ServiceUpdates $updates
```

<span data-ttu-id="cd900-117">Im Beispiel wird zunächst eine Webdienstdefinition erstellt, die nur die zu aktualisierende Felder enthält, und anschließend wird die Update-AzureRmMlWebService aufgerufen, um Sie mithilfe des ServiceUpdates-Parameters anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="cd900-117">The example first creates a web service definition, that only contains the fields to be updated, and then calls the Update-AzureRmMlWebService to apply them using the ServiceUpdates parameter.</span></span>

## <span data-ttu-id="cd900-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="cd900-118">PARAMETERS</span></span>

### <span data-ttu-id="cd900-119">-Ressourcen</span><span class="sxs-lookup"><span data-stu-id="cd900-119">-Assets</span></span>
<span data-ttu-id="cd900-120">Die Gruppe von Ressourcen (z. b. Module, Datasets), aus denen sich der Webdienst befindet.</span><span class="sxs-lookup"><span data-stu-id="cd900-120">The set of assets (e.g. modules, datasets) that make up the web service.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd900-121">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cd900-121">-Description</span></span>
<span data-ttu-id="cd900-122">Der neue Wert für die Beschreibung des Webdiensts.</span><span class="sxs-lookup"><span data-stu-id="cd900-122">The new value for the web service's description.</span></span>
<span data-ttu-id="cd900-123">Dies ist im Prahlerei-API-Schema des Diensts sichtbar.</span><span class="sxs-lookup"><span data-stu-id="cd900-123">This is visible in the service's Swagger API schema.</span></span>

```yaml
Type: System.String
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd900-124">-Diagnose</span><span class="sxs-lookup"><span data-stu-id="cd900-124">-Diagnostics</span></span>
<span data-ttu-id="cd900-125">Die Einstellungen, mit denen die Auflistung der Diagnoseablaufverfolgungen für den Webdienst gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="cd900-125">The settings that control the diagnostics traces collection for the web service.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.DiagnosticsConfiguration
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd900-126">-Force</span><span class="sxs-lookup"><span data-stu-id="cd900-126">-Force</span></span>
<span data-ttu-id="cd900-127">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="cd900-127">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="cd900-128">-Eingabe</span><span class="sxs-lookup"><span data-stu-id="cd900-128">-Input</span></span>
<span data-ttu-id="cd900-129">Die Definition für die Eingabe (n) des Webdiensts, die als Prahlerei-Schema Konstrukt bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="cd900-129">The definition for the web service's input(s), provided as a Swagger schema construct.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.ServiceInputOutputSpecification
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd900-130">-IsReadOnly</span><span class="sxs-lookup"><span data-stu-id="cd900-130">-IsReadOnly</span></span>
<span data-ttu-id="cd900-131">Gibt an, dass dieser Web Service ReadOnly ist.</span><span class="sxs-lookup"><span data-stu-id="cd900-131">Specifies that this web serviceis readonly.</span></span>
<span data-ttu-id="cd900-132">Nach dem festlegen kann der Webdienst mehr aktualisiert werden, einschließlich der Änderung des Werts dieser Eigenschaft und kann nur gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="cd900-132">Once set, the web service can longer be updated, including changing the value of this property, and can only be deleted.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd900-133">-Keys</span><span class="sxs-lookup"><span data-stu-id="cd900-133">-Keys</span></span>
<span data-ttu-id="cd900-134">Aktualisiert eine oder beide Zugriffstasten, die zur Authentifizierung von Anrufen an die Runtime-APIs des Diensts verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cd900-134">Updates one or both of the access keys used to authenticate calls to the service's runtime APIs.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebServiceKeys
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd900-135">-Name</span><span class="sxs-lookup"><span data-stu-id="cd900-135">-Name</span></span>
<span data-ttu-id="cd900-136">Der Name der Webdienst Ressource, die aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="cd900-136">The name of the web service resource to be updated.</span></span>

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

### <span data-ttu-id="cd900-137">-Output</span><span class="sxs-lookup"><span data-stu-id="cd900-137">-Output</span></span>
<span data-ttu-id="cd900-138">Die Definition für die Ausgabe (n) des Webdiensts, die als Prahlerei-Schema Konstrukt bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="cd900-138">The definition for the web service's output(s), provided as a Swagger schema construct.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.ServiceInputOutputSpecification
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd900-139">-Paket</span><span class="sxs-lookup"><span data-stu-id="cd900-139">-Package</span></span>
<span data-ttu-id="cd900-140">Die Definition des Graph-Pakets, das diesen Webdienst definiert.</span><span class="sxs-lookup"><span data-stu-id="cd900-140">The definition of the graph package that defines this web service.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.GraphPackage
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd900-141">-Parameter</span><span class="sxs-lookup"><span data-stu-id="cd900-141">-Parameters</span></span>
<span data-ttu-id="cd900-142">Der für den Webdienst definierte Satz globaler Parameterwerte als globaler Parameter Name – \> Standardwert Sammlung.</span><span class="sxs-lookup"><span data-stu-id="cd900-142">The set of global parameters values defined for the web service, given as a global parameter name -\> default value collection.</span></span>
<span data-ttu-id="cd900-143">Wenn kein Standardwert angegeben wird, gilt der Parameter als erforderlich.</span><span class="sxs-lookup"><span data-stu-id="cd900-143">If no default value is specified, the parameter is considered to be required.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd900-144">-RealtimeConfiguration</span><span class="sxs-lookup"><span data-stu-id="cd900-144">-RealtimeConfiguration</span></span>
<span data-ttu-id="cd900-145">Updates für die Konfiguration des Echt Zeit Endpunkts des Diensts.</span><span class="sxs-lookup"><span data-stu-id="cd900-145">Updates for the configuration of the service's realtime endpoint.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.RealtimeConfiguration
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd900-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd900-146">-ResourceGroupName</span></span>
<span data-ttu-id="cd900-147">Die Ressourcengruppe mit dem Webdienst, der aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="cd900-147">The resource group that contains the web service to be updated.</span></span>

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

### <span data-ttu-id="cd900-148">-ServiceUpdates</span><span class="sxs-lookup"><span data-stu-id="cd900-148">-ServiceUpdates</span></span>
<span data-ttu-id="cd900-149">Eine Gruppe von Updates, die für den Webdienst gelten, der als Webdienst Definitions Instanz bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="cd900-149">A set of updates to apply to the web service provided as a web service definition instance.</span></span>
<span data-ttu-id="cd900-150">Nur nicht statische Felder werden geändert.</span><span class="sxs-lookup"><span data-stu-id="cd900-150">Only non-static fields are modified.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: Create a new Azure ML webservice from a WebService instance definition.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd900-151">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="cd900-151">-StorageAccountKey</span></span>
<span data-ttu-id="cd900-152">Dreht die Zugriffstaste für das dem Webdienst zugeordnete Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="cd900-152">Rotates the access key for the storage account associated with the web service.</span></span>

```yaml
Type: System.String
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd900-153">-Title</span><span class="sxs-lookup"><span data-stu-id="cd900-153">-Title</span></span>
<span data-ttu-id="cd900-154">Der neue Wert für den Titel des Webdiensts.</span><span class="sxs-lookup"><span data-stu-id="cd900-154">The new value for the web service's title.</span></span>
<span data-ttu-id="cd900-155">Dies ist im Prahlerei-API-Schema des Diensts sichtbar.</span><span class="sxs-lookup"><span data-stu-id="cd900-155">This is visible in the service's Swagger API schema.</span></span>

```yaml
Type: System.String
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd900-156">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="cd900-156">-Confirm</span></span>
<span data-ttu-id="cd900-157">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cd900-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd900-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd900-158">-WhatIf</span></span>
<span data-ttu-id="cd900-159">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cd900-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd900-160">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cd900-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd900-161">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd900-161">-DefaultProfile</span></span>
<span data-ttu-id="cd900-162">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cd900-162">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd900-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd900-163">CommonParameters</span></span>
<span data-ttu-id="cd900-164">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd900-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd900-165">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd900-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd900-166">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cd900-166">INPUTS</span></span>

### <span data-ttu-id="cd900-167">Webservice</span><span class="sxs-lookup"><span data-stu-id="cd900-167">WebService</span></span>
<span data-ttu-id="cd900-168">Der Parameter "ServiceUpdates" akzeptiert den Wert vom Typ "Webservice" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="cd900-168">Parameter 'ServiceUpdates' accepts value of type 'WebService' from the pipeline</span></span>

## <span data-ttu-id="cd900-169">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cd900-169">OUTPUTS</span></span>

### <span data-ttu-id="cd900-170">Microsoft. Azure. Management. MachineLearning. Webservices. Models. WebService</span><span class="sxs-lookup"><span data-stu-id="cd900-170">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>
<span data-ttu-id="cd900-171">Eine zusammenfassende Beschreibung des Azure Machine Learning-Webdiensts.</span><span class="sxs-lookup"><span data-stu-id="cd900-171">A summary description of the Azure Machine Learning web service.</span></span>
<span data-ttu-id="cd900-172">Ähnlich wie die Beschreibung, die durch Aufrufen des Get-AzureRmMlWebService-Cmdlets für einen vorhandenen Webdienst zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="cd900-172">Similar to the description returned by calling the Get-AzureRmMlWebService cmdlet on an existing web service.</span></span>
<span data-ttu-id="cd900-173">Diese Beschreibung enthält keine vertraulichen Eigenschaften wie die Anmeldeinformationen des speicherkontos und die Zugriffstasten des Diensts.</span><span class="sxs-lookup"><span data-stu-id="cd900-173">This description does not contain sensitive properties such as storage account's credentials and the service's access keys.</span></span>

## <span data-ttu-id="cd900-174">Notizen</span><span class="sxs-lookup"><span data-stu-id="cd900-174">NOTES</span></span>
<span data-ttu-id="cd900-175">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="cd900-175">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="cd900-176">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cd900-176">RELATED LINKS</span></span>

