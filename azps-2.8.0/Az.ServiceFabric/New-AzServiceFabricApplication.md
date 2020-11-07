---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplication.md
ms.openlocfilehash: 7a337ed6e347d5ab22cd04baac2acb1c7e0b171d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93824711"
---
# <span data-ttu-id="c9478-101">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="c9478-101">New-AzServiceFabricApplication</span></span>

## <span data-ttu-id="c9478-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c9478-102">SYNOPSIS</span></span>
<span data-ttu-id="c9478-103">Erstellen Sie eine neue Service Fabric-Anwendung unter der angegebenen Ressourcengruppe und dem Cluster.</span><span class="sxs-lookup"><span data-stu-id="c9478-103">Create new service fabric application under the specified resource group and cluster.</span></span>

## <span data-ttu-id="c9478-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c9478-104">SYNTAX</span></span>

### <span data-ttu-id="c9478-105">SkipAppTypeVersion (Standard)</span><span class="sxs-lookup"><span data-stu-id="c9478-105">SkipAppTypeVersion (Default)</span></span>
```
New-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ApplicationTypeName] <String> [-ApplicationTypeVersion] <String> -Name <String>
 [-ApplicationParameter <Hashtable>] [-MinimumNodeCount <Int64>] [-MaximumNodeCount <Int64>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9478-106">CreateAppTypeVersion</span><span class="sxs-lookup"><span data-stu-id="c9478-106">CreateAppTypeVersion</span></span>
```
New-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ApplicationTypeName] <String> [-ApplicationTypeVersion] <String> -Name <String>
 [-ApplicationParameter <Hashtable>] -PackageUrl <String> [-MinimumNodeCount <Int64>]
 [-MaximumNodeCount <Int64>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c9478-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c9478-107">DESCRIPTION</span></span>
<span data-ttu-id="c9478-108">Mit diesem Cmdlet wird eine neue Dienst Fabric-Anwendung unter der angegebenen Ressourcengruppe und dem angegebenen Cluster erstellt.</span><span class="sxs-lookup"><span data-stu-id="c9478-108">This cmdlet creates a new service fabric application under the specified resource group and cluster.</span></span> <span data-ttu-id="c9478-109">Der Parameter-PackageUrl kann zum Erstellen der Typversion verwendet werden, wenn die Typversion bereits beendet wird, aber im Zustand "fehlgeschlagen" das Cmdlet fragt, ob der Benutzer die Typversion neu erstellen möchte.</span><span class="sxs-lookup"><span data-stu-id="c9478-109">The parameter -PackageUrl can be used to create the type version, If the type version already exits but its in 'Failed' state the cmdlet will ask if the user wants to recreate the type version.</span></span> <span data-ttu-id="c9478-110">Wenn Sie im Zustand "Fehler" fortgesetzt wird, beendet der Befehl den Prozess und löst eine Ausnahme aus.</span><span class="sxs-lookup"><span data-stu-id="c9478-110">If it continues in 'Failed' state, the command will stop the process and throw an exception.</span></span>

## <span data-ttu-id="c9478-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c9478-111">EXAMPLES</span></span>

### <span data-ttu-id="c9478-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c9478-112">Example 1</span></span>
```powershell
PS C:\> New-AzServiceFabricApplication -ResourceGroupName "testRG" -ClusterName "testCluster" -ApplicationTypeName "TestAppType" -ApplicationTypeVersion "v1" -Name "testApp" -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="c9478-113">In diesem Beispiel wird die Anwendung "testApp" unter Ressourcengruppe "testRG" und Cluster "testCluster" erstellt.</span><span class="sxs-lookup"><span data-stu-id="c9478-113">This example creates the application "testApp" under resource group "testRG" and cluster "testCluster".</span></span> <span data-ttu-id="c9478-114">Der Anwendungstyp "TestAppType" Version "V1" sollte bereits im Cluster vorhanden sein, und die Anwendungsparameter sollten im Anwendungsmanifest definiert werden, andernfalls schlägt das Cmdlet fehl.</span><span class="sxs-lookup"><span data-stu-id="c9478-114">The application type "TestAppType" version "v1" should already exist in the cluster, and the application parameters should be defined in the application manifest otherwise the cmdlet will fail.</span></span>

### <span data-ttu-id="c9478-115">Beispiel 2: Geben Sie-PackageUrl an, um die Version des Anwendungstyps zu erstellen, bevor Sie die Anwendung erstellen.</span><span class="sxs-lookup"><span data-stu-id="c9478-115">Example 2: Specify -PackageUrl to create the application type version before creating the application.</span></span>
```powershell
PS C:\> New-AzServiceFabricApplication -ResourceGroupName "testRG" -ClusterName "testCluster" -ApplicationTypeName "TestAppType" -ApplicationTypeVersion "v1" -Name "testApp" -PackageUrl "https://sftestapp.blob.core.windows.net/sftestapp/testApp_1.0.sfpkg" -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="c9478-116">In diesem Beispiel wird der Anwendungstyp "TestAppType" Version "V1" mit der bereitgestellten Paket-URL erstellt.</span><span class="sxs-lookup"><span data-stu-id="c9478-116">This example creates the application type "TestAppType"  version "v1" using the package url provided.</span></span> <span data-ttu-id="c9478-117">Anschließend wird der normale Prozess zum Erstellen der Anwendung fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="c9478-117">After this, it will continue the normal process to create the application.</span></span> <span data-ttu-id="c9478-118">Wenn die Version des Anwendungstyps bereits beendet wird und der Bereitstellungsstatus in "fehlgeschlagen" angezeigt wird, werden Sie aufgefordert, zu entscheiden, ob der Benutzer die Typversion erneut erstellen möchte.</span><span class="sxs-lookup"><span data-stu-id="c9478-118">If the application type version already exits and the provisioning state its in 'Failed' it will prompt to decide if the user wants to recreate the type version.</span></span>

## <span data-ttu-id="c9478-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="c9478-119">PARAMETERS</span></span>

### <span data-ttu-id="c9478-120">-ApplicationParameter</span><span class="sxs-lookup"><span data-stu-id="c9478-120">-ApplicationParameter</span></span>
<span data-ttu-id="c9478-121">Geben Sie die Anwendungsparameter als Schlüssel-Wert-Paare an.</span><span class="sxs-lookup"><span data-stu-id="c9478-121">Specify the application parameters as key/value pairs.</span></span>
<span data-ttu-id="c9478-122">Diese Parameter müssen im Anwendungsmanifest vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="c9478-122">These parameters must exist in the application manifest.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9478-123">-ApplicationTypeName</span><span class="sxs-lookup"><span data-stu-id="c9478-123">-ApplicationTypeName</span></span>
<span data-ttu-id="c9478-124">Geben Sie den Namen des Anwendungstyps an.</span><span class="sxs-lookup"><span data-stu-id="c9478-124">Specify the name of the application type</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9478-125">-ApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="c9478-125">-ApplicationTypeVersion</span></span>
<span data-ttu-id="c9478-126">Angeben der Version des Anwendungstyps</span><span class="sxs-lookup"><span data-stu-id="c9478-126">Specify the application type version</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9478-127">-Clustername</span><span class="sxs-lookup"><span data-stu-id="c9478-127">-ClusterName</span></span>
<span data-ttu-id="c9478-128">Geben Sie den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="c9478-128">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9478-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9478-129">-DefaultProfile</span></span>
<span data-ttu-id="c9478-130">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c9478-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9478-131">-Force</span><span class="sxs-lookup"><span data-stu-id="c9478-131">-Force</span></span>
<span data-ttu-id="c9478-132">Ohne Eingabeaufforderungen fortfahren</span><span class="sxs-lookup"><span data-stu-id="c9478-132">Continue without prompts</span></span>

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

### <span data-ttu-id="c9478-133">-MaximumNodeCount</span><span class="sxs-lookup"><span data-stu-id="c9478-133">-MaximumNodeCount</span></span>
<span data-ttu-id="c9478-134">Gibt die maximale Anzahl von Knoten an, auf denen eine Anwendung platziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="c9478-134">Specifies the maximum number of nodes on which to place an application</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9478-135">-MinimumNodeCount</span><span class="sxs-lookup"><span data-stu-id="c9478-135">-MinimumNodeCount</span></span>
<span data-ttu-id="c9478-136">Gibt die Mindestanzahl von Knoten an, bei denen Service Fabric Kapazität für diese Anwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="c9478-136">Specifies the minimum number of nodes where Service Fabric will reserve capacity for this application</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9478-137">-Name</span><span class="sxs-lookup"><span data-stu-id="c9478-137">-Name</span></span>
<span data-ttu-id="c9478-138">Angeben des Namens der Anwendung</span><span class="sxs-lookup"><span data-stu-id="c9478-138">Specify the name of the application</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9478-139">-PackageUrl</span><span class="sxs-lookup"><span data-stu-id="c9478-139">-PackageUrl</span></span>
<span data-ttu-id="c9478-140">Angeben der URL der sfpkg-Datei des Anwendungspakets</span><span class="sxs-lookup"><span data-stu-id="c9478-140">Specify the url of the application package sfpkg file</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAppTypeVersion
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9478-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9478-141">-ResourceGroupName</span></span>
<span data-ttu-id="c9478-142">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="c9478-142">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9478-143">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c9478-143">-Confirm</span></span>
<span data-ttu-id="c9478-144">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c9478-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9478-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9478-145">-WhatIf</span></span>
<span data-ttu-id="c9478-146">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c9478-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9478-147">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c9478-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9478-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9478-148">CommonParameters</span></span>
<span data-ttu-id="c9478-149">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9478-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9478-150">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9478-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9478-151">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c9478-151">INPUTS</span></span>

### <span data-ttu-id="c9478-152">System. String</span><span class="sxs-lookup"><span data-stu-id="c9478-152">System.String</span></span>

### <span data-ttu-id="c9478-153">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="c9478-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="c9478-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c9478-154">OUTPUTS</span></span>

### <span data-ttu-id="c9478-155">Microsoft. Azure. Commands. ServiceFabric. Models. PSApplication</span><span class="sxs-lookup"><span data-stu-id="c9478-155">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="c9478-156">Notizen</span><span class="sxs-lookup"><span data-stu-id="c9478-156">NOTES</span></span>

## <span data-ttu-id="c9478-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c9478-157">RELATED LINKS</span></span>
