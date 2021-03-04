---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/new-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplication.md
ms.openlocfilehash: e1e6efbdeaed90fe7591ed2dd5a645955dd5a314
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933696"
---
# <span data-ttu-id="4bb7f-101">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="4bb7f-101">New-AzServiceFabricApplication</span></span>

## <span data-ttu-id="4bb7f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4bb7f-102">SYNOPSIS</span></span>
<span data-ttu-id="4bb7f-103">Erstellen Sie eine neue Service Fabric-Anwendung unter der angegebenen Ressourcengruppe und dem angegebenen Cluster.</span><span class="sxs-lookup"><span data-stu-id="4bb7f-103">Create new service fabric application under the specified resource group and cluster.</span></span>

## <span data-ttu-id="4bb7f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4bb7f-104">SYNTAX</span></span>

### <span data-ttu-id="4bb7f-105">SkipAppTypeVersion (Standard)</span><span class="sxs-lookup"><span data-stu-id="4bb7f-105">SkipAppTypeVersion (Default)</span></span>
```
New-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ApplicationTypeName] <String> [-ApplicationTypeVersion] <String> -Name <String>
 [-ApplicationParameter <Hashtable>] [-MinimumNodeCount <Int64>] [-MaximumNodeCount <Int64>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4bb7f-106">CreateAppTypeVersion</span><span class="sxs-lookup"><span data-stu-id="4bb7f-106">CreateAppTypeVersion</span></span>
```
New-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ApplicationTypeName] <String> [-ApplicationTypeVersion] <String> -Name <String>
 [-ApplicationParameter <Hashtable>] -PackageUrl <String> [-MinimumNodeCount <Int64>]
 [-MaximumNodeCount <Int64>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4bb7f-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4bb7f-107">DESCRIPTION</span></span>
<span data-ttu-id="4bb7f-108">Dieses Cmdlet erstellt eine neue Service Fabric-Anwendung unter der angegebenen Ressourcengruppe und dem angegebenen Cluster.</span><span class="sxs-lookup"><span data-stu-id="4bb7f-108">This cmdlet creates a new service fabric application under the specified resource group and cluster.</span></span> <span data-ttu-id="4bb7f-109">Der Parameter -PackageUrl kann zum Erstellen der Typversion verwendet werden. Wenn die Typversion bereits beendet wird, aber im Zustand "Fehlgeschlagen" angezeigt wird, fragt das Cmdlet, ob der Benutzer die Typversion neu erstellen möchte.</span><span class="sxs-lookup"><span data-stu-id="4bb7f-109">The parameter -PackageUrl can be used to create the type version, If the type version already exits but its in 'Failed' state the cmdlet will ask if the user wants to recreate the type version.</span></span> <span data-ttu-id="4bb7f-110">Wenn der Vorgang im Zustand "Fehlgeschlagen" fortgesetzt wird, beendet der Befehl den Prozess und gibt eine Ausnahme aus.</span><span class="sxs-lookup"><span data-stu-id="4bb7f-110">If it continues in 'Failed' state, the command will stop the process and throw an exception.</span></span>

## <span data-ttu-id="4bb7f-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4bb7f-111">EXAMPLES</span></span>

### <span data-ttu-id="4bb7f-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4bb7f-112">Example 1</span></span>
```powershell
PS C:\> New-AzServiceFabricApplication -ResourceGroupName "testRG" -ClusterName "testCluster" -ApplicationTypeName "TestAppType" -ApplicationTypeVersion "v1" -Name "testApp" -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="4bb7f-113">In diesem Beispiel wird die Anwendung "testApp" unter der Ressourcengruppe "testRG" und dem Cluster "testCluster" erstellt.</span><span class="sxs-lookup"><span data-stu-id="4bb7f-113">This example creates the application "testApp" under resource group "testRG" and cluster "testCluster".</span></span> <span data-ttu-id="4bb7f-114">Der Anwendungstyp "TestAppType", Version "v1", sollte bereits im Cluster vorhanden sein, und die Anwendungsparameter sollten im Anwendungsmanifest definiert werden, andernfalls besteht ein Fehler beim Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4bb7f-114">The application type "TestAppType" version "v1" should already exist in the cluster, and the application parameters should be defined in the application manifest otherwise the cmdlet will fail.</span></span>

### <span data-ttu-id="4bb7f-115">Beispiel 2: Geben Sie -PackageUrl an, um die Anwendungstypversion zu erstellen, bevor Sie die Anwendung erstellen.</span><span class="sxs-lookup"><span data-stu-id="4bb7f-115">Example 2: Specify -PackageUrl to create the application type version before creating the application.</span></span>
```powershell
PS C:\> New-AzServiceFabricApplication -ResourceGroupName "testRG" -ClusterName "testCluster" -ApplicationTypeName "TestAppType" -ApplicationTypeVersion "v1" -Name "testApp" -PackageUrl "https://sftestapp.blob.core.windows.net/sftestapp/testApp_1.0.sfpkg" -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="4bb7f-116">In diesem Beispiel wird der Anwendungstyp "TestAppType"- Version "v1" mit der bereitgestellten Paket-URL erstellt.</span><span class="sxs-lookup"><span data-stu-id="4bb7f-116">This example creates the application type "TestAppType"  version "v1" using the package url provided.</span></span> <span data-ttu-id="4bb7f-117">Danach wird der normale Prozess zum Erstellen der Anwendung fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="4bb7f-117">After this, it will continue the normal process to create the application.</span></span> <span data-ttu-id="4bb7f-118">Wenn die Anwendungstypversion bereits beendet wird und der Bereitstellungszustand in "Fehlgeschlagen" angezeigt wird, werden Sie aufgefordert, zu entscheiden, ob der Benutzer die Typversion neu erstellen möchte.</span><span class="sxs-lookup"><span data-stu-id="4bb7f-118">If the application type version already exits and the provisioning state its in 'Failed' it will prompt to decide if the user wants to recreate the type version.</span></span>

## <span data-ttu-id="4bb7f-119">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="4bb7f-119">PARAMETERS</span></span>

### <span data-ttu-id="4bb7f-120">-ApplicationParameter</span><span class="sxs-lookup"><span data-stu-id="4bb7f-120">-ApplicationParameter</span></span>
<span data-ttu-id="4bb7f-121">Geben Sie die Anwendungsparameter als Schlüssel-Wert-Paare an.</span><span class="sxs-lookup"><span data-stu-id="4bb7f-121">Specify the application parameters as key/value pairs.</span></span>
<span data-ttu-id="4bb7f-122">Diese Parameter müssen im Anwendungsmanifest vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="4bb7f-122">These parameters must exist in the application manifest.</span></span>

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

### <span data-ttu-id="4bb7f-123">-ApplicationTypeName</span><span class="sxs-lookup"><span data-stu-id="4bb7f-123">-ApplicationTypeName</span></span>
<span data-ttu-id="4bb7f-124">Angeben des Namens des Anwendungstyps</span><span class="sxs-lookup"><span data-stu-id="4bb7f-124">Specify the name of the application type</span></span>

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

### <span data-ttu-id="4bb7f-125">-ApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="4bb7f-125">-ApplicationTypeVersion</span></span>
<span data-ttu-id="4bb7f-126">Angeben der Anwendungstypversion</span><span class="sxs-lookup"><span data-stu-id="4bb7f-126">Specify the application type version</span></span>

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

### <span data-ttu-id="4bb7f-127">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="4bb7f-127">-ClusterName</span></span>
<span data-ttu-id="4bb7f-128">Geben Sie den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="4bb7f-128">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="4bb7f-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bb7f-129">-DefaultProfile</span></span>
<span data-ttu-id="4bb7f-130">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4bb7f-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4bb7f-131">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="4bb7f-131">-Force</span></span>
<span data-ttu-id="4bb7f-132">Fortsetzen ohne Eingabeaufforderungen</span><span class="sxs-lookup"><span data-stu-id="4bb7f-132">Continue without prompts</span></span>

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

### <span data-ttu-id="4bb7f-133">-MaximumNodeCount</span><span class="sxs-lookup"><span data-stu-id="4bb7f-133">-MaximumNodeCount</span></span>
<span data-ttu-id="4bb7f-134">Gibt die maximale Anzahl von Knoten an, auf denen eine Anwendung platzieren werden soll</span><span class="sxs-lookup"><span data-stu-id="4bb7f-134">Specifies the maximum number of nodes on which to place an application</span></span>

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

### <span data-ttu-id="4bb7f-135">-MinimumNodeCount</span><span class="sxs-lookup"><span data-stu-id="4bb7f-135">-MinimumNodeCount</span></span>
<span data-ttu-id="4bb7f-136">Gibt die Mindestanzahl von Knoten an, für die Service Fabric Kapazität für diese Anwendung reserviert</span><span class="sxs-lookup"><span data-stu-id="4bb7f-136">Specifies the minimum number of nodes where Service Fabric will reserve capacity for this application</span></span>

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

### <span data-ttu-id="4bb7f-137">-Name</span><span class="sxs-lookup"><span data-stu-id="4bb7f-137">-Name</span></span>
<span data-ttu-id="4bb7f-138">Angeben des Namens der Anwendung</span><span class="sxs-lookup"><span data-stu-id="4bb7f-138">Specify the name of the application</span></span>

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

### <span data-ttu-id="4bb7f-139">-PackageUrl</span><span class="sxs-lookup"><span data-stu-id="4bb7f-139">-PackageUrl</span></span>
<span data-ttu-id="4bb7f-140">Angeben der URL der Datei "sfpkg" des Anwendungspakets</span><span class="sxs-lookup"><span data-stu-id="4bb7f-140">Specify the url of the application package sfpkg file</span></span>

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

### <span data-ttu-id="4bb7f-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bb7f-141">-ResourceGroupName</span></span>
<span data-ttu-id="4bb7f-142">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="4bb7f-142">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="4bb7f-143">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4bb7f-143">-Confirm</span></span>
<span data-ttu-id="4bb7f-144">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4bb7f-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4bb7f-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4bb7f-145">-WhatIf</span></span>
<span data-ttu-id="4bb7f-146">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4bb7f-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4bb7f-147">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4bb7f-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4bb7f-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bb7f-148">CommonParameters</span></span>
<span data-ttu-id="4bb7f-149">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4bb7f-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bb7f-150">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4bb7f-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bb7f-151">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4bb7f-151">INPUTS</span></span>

### <span data-ttu-id="4bb7f-152">System.String</span><span class="sxs-lookup"><span data-stu-id="4bb7f-152">System.String</span></span>

### <span data-ttu-id="4bb7f-153">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="4bb7f-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4bb7f-154">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4bb7f-154">OUTPUTS</span></span>

### <span data-ttu-id="4bb7f-155">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span><span class="sxs-lookup"><span data-stu-id="4bb7f-155">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="4bb7f-156">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="4bb7f-156">NOTES</span></span>

## <span data-ttu-id="4bb7f-157">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="4bb7f-157">RELATED LINKS</span></span>
