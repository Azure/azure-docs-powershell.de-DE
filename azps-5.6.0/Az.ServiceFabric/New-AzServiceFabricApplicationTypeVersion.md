---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/new-azservicefabricapplicationtypeversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationTypeVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationTypeVersion.md
ms.openlocfilehash: d13e2e4473c390a27be4741de703818bda769efa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922299"
---
# <span data-ttu-id="0b2d0-101">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="0b2d0-101">New-AzServiceFabricApplicationTypeVersion</span></span>

## <span data-ttu-id="0b2d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b2d0-102">SYNOPSIS</span></span>
<span data-ttu-id="0b2d0-103">Erstellen Sie eine neue Anwendungstypversion unter der angegebenen Ressourcengruppe und dem angegebenen Cluster.</span><span class="sxs-lookup"><span data-stu-id="0b2d0-103">Create new application type version under the specified resource group and cluster.</span></span>

## <span data-ttu-id="0b2d0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0b2d0-104">SYNTAX</span></span>

```
New-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> [-Version] <String> -PackageUrl <String> [-DefaultParameter <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b2d0-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0b2d0-105">DESCRIPTION</span></span>
<span data-ttu-id="0b2d0-106">Dieses Cmdlet erstellt eine neue Anwendungstypversion mit dem in -PackageUrl angegebenen Paket. Dies sollte über einen REST-Endpunkt für Azure Resource Manager zugänglich sein, der während der Bereitstellung verwendet werden kann und die Mit der Erweiterung ".sfpkg" verpackte und gezippte Anwendung enthält.</span><span class="sxs-lookup"><span data-stu-id="0b2d0-106">This cmdlet creates a new application type version using the package specified in -PackageUrl, this should be accessible through a REST endpoint for Azure Resource Manager to consume during deployment and contained The application packaged and zipped with the extension .sfpkg.</span></span> <span data-ttu-id="0b2d0-107">Mit diesem Befehl wird der Anwendungstyp erstellt, wenn er noch nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="0b2d0-107">This command will create the application type if it doesn't exist already.</span></span>

## <span data-ttu-id="0b2d0-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0b2d0-108">EXAMPLES</span></span>

### <span data-ttu-id="0b2d0-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0b2d0-109">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $version = "v1"
PS C:\> $packageUrl = "https://sftestapp.blob.core.windows.net/sftestapp/testApp_1.0.sfpkg"
PS C:\> New-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Version $version -PackageUrl $packageUrl -Verbose
```

<span data-ttu-id="0b2d0-110">In diesem Beispiel wird eine Anwendungstypversion "v1" unter dem Typ "testAppType" erstellt.</span><span class="sxs-lookup"><span data-stu-id="0b2d0-110">This example will create an application type version "v1" under type "testAppType".</span></span> <span data-ttu-id="0b2d0-111">Die im Paket enthaltene Version im Anwendungsmanifest sollte dieselbe Version wie die version haben, die in -Version angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="0b2d0-111">The version in the application manifest contained in the package should have the same version as the one specified in -Version.</span></span>

## <span data-ttu-id="0b2d0-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="0b2d0-112">PARAMETERS</span></span>

### <span data-ttu-id="0b2d0-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="0b2d0-113">-ClusterName</span></span>
<span data-ttu-id="0b2d0-114">Geben Sie den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="0b2d0-114">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="0b2d0-115">-DefaultParameter</span><span class="sxs-lookup"><span data-stu-id="0b2d0-115">-DefaultParameter</span></span>
<span data-ttu-id="0b2d0-116">Geben Sie die Standardwerte der Anwendungsparameter als Schlüssel-Wert-Paare an.</span><span class="sxs-lookup"><span data-stu-id="0b2d0-116">Specify the default values of the application parameters as key/value pairs.</span></span>
<span data-ttu-id="0b2d0-117">Diese Parameter müssen im Anwendungsmanifest vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="0b2d0-117">These parameters must exist in the application manifest.</span></span>

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

### <span data-ttu-id="0b2d0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b2d0-118">-DefaultProfile</span></span>
<span data-ttu-id="0b2d0-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0b2d0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b2d0-120">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="0b2d0-120">-Force</span></span>
<span data-ttu-id="0b2d0-121">Fortsetzen ohne Eingabeaufforderungen</span><span class="sxs-lookup"><span data-stu-id="0b2d0-121">Continue without prompts</span></span>

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

### <span data-ttu-id="0b2d0-122">-Name</span><span class="sxs-lookup"><span data-stu-id="0b2d0-122">-Name</span></span>
<span data-ttu-id="0b2d0-123">Angeben des Namens des Anwendungstyps</span><span class="sxs-lookup"><span data-stu-id="0b2d0-123">Specify the name of the application type</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b2d0-124">-PackageUrl</span><span class="sxs-lookup"><span data-stu-id="0b2d0-124">-PackageUrl</span></span>
<span data-ttu-id="0b2d0-125">Angeben der URL der Datei "sfpkg" des Anwendungspakets</span><span class="sxs-lookup"><span data-stu-id="0b2d0-125">Specify the url of the application package sfpkg file</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b2d0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b2d0-126">-ResourceGroupName</span></span>
<span data-ttu-id="0b2d0-127">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="0b2d0-127">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="0b2d0-128">-Version</span><span class="sxs-lookup"><span data-stu-id="0b2d0-128">-Version</span></span>
<span data-ttu-id="0b2d0-129">Angeben der Anwendungstypversion</span><span class="sxs-lookup"><span data-stu-id="0b2d0-129">Specify the application type version</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationTypeVersion

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b2d0-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0b2d0-130">-Confirm</span></span>
<span data-ttu-id="0b2d0-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0b2d0-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b2d0-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b2d0-132">-WhatIf</span></span>
<span data-ttu-id="0b2d0-133">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0b2d0-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b2d0-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0b2d0-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b2d0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b2d0-135">CommonParameters</span></span>
<span data-ttu-id="0b2d0-136">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b2d0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b2d0-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0b2d0-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b2d0-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0b2d0-138">INPUTS</span></span>

### <span data-ttu-id="0b2d0-139">System.String</span><span class="sxs-lookup"><span data-stu-id="0b2d0-139">System.String</span></span>

### <span data-ttu-id="0b2d0-140">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="0b2d0-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="0b2d0-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0b2d0-141">OUTPUTS</span></span>

### <span data-ttu-id="0b2d0-142">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="0b2d0-142">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span></span>

## <span data-ttu-id="0b2d0-143">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="0b2d0-143">NOTES</span></span>

## <span data-ttu-id="0b2d0-144">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="0b2d0-144">RELATED LINKS</span></span>
