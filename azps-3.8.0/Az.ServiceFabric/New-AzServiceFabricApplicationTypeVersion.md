---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricapplicationtypeversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationTypeVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationTypeVersion.md
ms.openlocfilehash: 69bbcbbd508a5bf32163b91378aab62dbdcb3a64
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996428"
---
# <span data-ttu-id="6c8a1-101">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="6c8a1-101">New-AzServiceFabricApplicationTypeVersion</span></span>

## <span data-ttu-id="6c8a1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6c8a1-102">SYNOPSIS</span></span>
<span data-ttu-id="6c8a1-103">Erstellen Sie unter der angegebenen Ressourcengruppe und dem Cluster eine neue Version des Anwendungstyps.</span><span class="sxs-lookup"><span data-stu-id="6c8a1-103">Create new application type version under the specified resource group and cluster.</span></span>

## <span data-ttu-id="6c8a1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6c8a1-104">SYNTAX</span></span>

```
New-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> [-Version] <String> -PackageUrl <String> [-DefaultParameter <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c8a1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6c8a1-105">DESCRIPTION</span></span>
<span data-ttu-id="6c8a1-106">Dieses Cmdlet erstellt unter Verwendung des in-PackageUrl angegebenen Pakets eine neue Version des Anwendungstyps, auf die über einen Ruhe Endpunkt zugegriffen werden kann, damit Azure Resource Manager während der Bereitstellung verwendet werden kann, und die Anwendung verpackt und mit der Erweiterung. sfpkg gezippt enthält.</span><span class="sxs-lookup"><span data-stu-id="6c8a1-106">This cmdlet creates a new application type version using the package specified in -PackageUrl, this should be accessible through a REST endpoint for Azure Resource Manager to consume during deployment and contained The application packaged and zipped with the extension .sfpkg.</span></span> <span data-ttu-id="6c8a1-107">Mit diesem Befehl wird der Anwendungstyp erstellt, wenn er noch nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="6c8a1-107">This command will create the application type if it doesn't exist already.</span></span>

## <span data-ttu-id="6c8a1-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6c8a1-108">EXAMPLES</span></span>

### <span data-ttu-id="6c8a1-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6c8a1-109">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $version = "v1"
PS C:\> $packageUrl = "https://sftestapp.blob.core.windows.net/sftestapp/testApp_1.0.sfpkg"
PS C:\> New-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Version $version -PackageUrl $packageUrl -Verbose
```

<span data-ttu-id="6c8a1-110">In diesem Beispiel wird eine Anwendungstypen Version "V1" unter Typ "testAppType" erstellt.</span><span class="sxs-lookup"><span data-stu-id="6c8a1-110">This example will create an application type version "v1" under type "testAppType".</span></span> <span data-ttu-id="6c8a1-111">Die Version im Anwendungsmanifest, die im Paket enthalten ist, sollte die gleiche Version wie die in-Version angegebene Version aufweisen.</span><span class="sxs-lookup"><span data-stu-id="6c8a1-111">The version in the application manifest contained in the package should have the same version as the one specified in -Version.</span></span>

## <span data-ttu-id="6c8a1-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="6c8a1-112">PARAMETERS</span></span>

### <span data-ttu-id="6c8a1-113">-Clustername</span><span class="sxs-lookup"><span data-stu-id="6c8a1-113">-ClusterName</span></span>
<span data-ttu-id="6c8a1-114">Geben Sie den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="6c8a1-114">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="6c8a1-115">-Defaultparameter</span><span class="sxs-lookup"><span data-stu-id="6c8a1-115">-DefaultParameter</span></span>
<span data-ttu-id="6c8a1-116">Geben Sie die Standardwerte der Anwendungsparameter als Schlüssel-Wert-Paare an.</span><span class="sxs-lookup"><span data-stu-id="6c8a1-116">Specify the default values of the application parameters as key/value pairs.</span></span>
<span data-ttu-id="6c8a1-117">Diese Parameter müssen im Anwendungsmanifest vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="6c8a1-117">These parameters must exist in the application manifest.</span></span>

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

### <span data-ttu-id="6c8a1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c8a1-118">-DefaultProfile</span></span>
<span data-ttu-id="6c8a1-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6c8a1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c8a1-120">-Force</span><span class="sxs-lookup"><span data-stu-id="6c8a1-120">-Force</span></span>
<span data-ttu-id="6c8a1-121">Ohne Eingabeaufforderungen fortfahren</span><span class="sxs-lookup"><span data-stu-id="6c8a1-121">Continue without prompts</span></span>

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

### <span data-ttu-id="6c8a1-122">-Name</span><span class="sxs-lookup"><span data-stu-id="6c8a1-122">-Name</span></span>
<span data-ttu-id="6c8a1-123">Geben Sie den Namen des Anwendungstyps an.</span><span class="sxs-lookup"><span data-stu-id="6c8a1-123">Specify the name of the application type</span></span>

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

### <span data-ttu-id="6c8a1-124">-PackageUrl</span><span class="sxs-lookup"><span data-stu-id="6c8a1-124">-PackageUrl</span></span>
<span data-ttu-id="6c8a1-125">Angeben der URL der sfpkg-Datei des Anwendungspakets</span><span class="sxs-lookup"><span data-stu-id="6c8a1-125">Specify the url of the application package sfpkg file</span></span>

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

### <span data-ttu-id="6c8a1-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c8a1-126">-ResourceGroupName</span></span>
<span data-ttu-id="6c8a1-127">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="6c8a1-127">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="6c8a1-128">-Version</span><span class="sxs-lookup"><span data-stu-id="6c8a1-128">-Version</span></span>
<span data-ttu-id="6c8a1-129">Angeben der Version des Anwendungstyps</span><span class="sxs-lookup"><span data-stu-id="6c8a1-129">Specify the application type version</span></span>

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

### <span data-ttu-id="6c8a1-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6c8a1-130">-Confirm</span></span>
<span data-ttu-id="6c8a1-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6c8a1-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c8a1-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c8a1-132">-WhatIf</span></span>
<span data-ttu-id="6c8a1-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6c8a1-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c8a1-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6c8a1-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c8a1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c8a1-135">CommonParameters</span></span>
<span data-ttu-id="6c8a1-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c8a1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c8a1-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c8a1-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c8a1-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6c8a1-138">INPUTS</span></span>

### <span data-ttu-id="6c8a1-139">System. String</span><span class="sxs-lookup"><span data-stu-id="6c8a1-139">System.String</span></span>

### <span data-ttu-id="6c8a1-140">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="6c8a1-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="6c8a1-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6c8a1-141">OUTPUTS</span></span>

### <span data-ttu-id="6c8a1-142">Microsoft. Azure. Commands. ServiceFabric. Models. PSApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="6c8a1-142">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span></span>

## <span data-ttu-id="6c8a1-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="6c8a1-143">NOTES</span></span>

## <span data-ttu-id="6c8a1-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6c8a1-144">RELATED LINKS</span></span>
