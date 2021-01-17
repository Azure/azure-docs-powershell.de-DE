---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/remove-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncService.md
ms.openlocfilehash: f64c085f742eeabea235660d4af7ba6bd5970fdf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471687"
---
# <span data-ttu-id="86d3d-101">Remove-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="86d3d-101">Remove-AzStorageSyncService</span></span>

## <span data-ttu-id="86d3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86d3d-102">SYNOPSIS</span></span>
<span data-ttu-id="86d3d-103">Mit diesem Befehl wird der angegebene Speichersynchronisierungsdienst gelöscht.</span><span class="sxs-lookup"><span data-stu-id="86d3d-103">This command will delete the specified storage sync service.</span></span>

## <span data-ttu-id="86d3d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="86d3d-104">SYNTAX</span></span>

### <span data-ttu-id="86d3d-105">StringParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="86d3d-105">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86d3d-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="86d3d-106">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncService [-InputObject] <PSStorageSyncService> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86d3d-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="86d3d-107">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncService [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86d3d-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="86d3d-108">DESCRIPTION</span></span>
<span data-ttu-id="86d3d-109">Mit diesem Befehl wird der angegebene Speichersynchronisierungsdienst gelöscht.</span><span class="sxs-lookup"><span data-stu-id="86d3d-109">This command will delete the specified storage sync service.</span></span> <span data-ttu-id="86d3d-110">Ein Speichersynchronisierungsdienst kann nur entfernt werden, wenn zuerst alle enthaltenen Synchronisierungsgruppen und registrierten Server gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="86d3d-110">A storage sync service can only be removed when all of the contained sync groups and registered servers are deleted first.</span></span>

## <span data-ttu-id="86d3d-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="86d3d-111">EXAMPLES</span></span>

### <span data-ttu-id="86d3d-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="86d3d-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncService -Force -ResourceGroupName "myResourceGroup" -Name "myStorageSyncServiceName"
```

<span data-ttu-id="86d3d-113">Mit diesem Befehl wird der Speichersynchronisierungsdienst entfernt.</span><span class="sxs-lookup"><span data-stu-id="86d3d-113">This command will remove the storage sync service.</span></span>

## <span data-ttu-id="86d3d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="86d3d-114">PARAMETERS</span></span>

### <span data-ttu-id="86d3d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="86d3d-115">-AsJob</span></span>
<span data-ttu-id="86d3d-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="86d3d-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="86d3d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86d3d-117">-DefaultProfile</span></span>
<span data-ttu-id="86d3d-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="86d3d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="86d3d-119">-Force</span><span class="sxs-lookup"><span data-stu-id="86d3d-119">-Force</span></span>
<span data-ttu-id="86d3d-120">Liefern Sie "-Force", um die Bestätigung dieses Befehls zu überspringen.</span><span class="sxs-lookup"><span data-stu-id="86d3d-120">Supply -Force to skip confirmation of this command.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86d3d-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="86d3d-121">-InputObject</span></span>
<span data-ttu-id="86d3d-122">StorageSyncService-Eingabeobjekt, das normalerweise über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="86d3d-122">StorageSyncService Input Object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="86d3d-123">-Name</span><span class="sxs-lookup"><span data-stu-id="86d3d-123">-Name</span></span>
<span data-ttu-id="86d3d-124">Name des StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="86d3d-124">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: StorageSyncServiceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86d3d-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="86d3d-125">-PassThru</span></span>
<span data-ttu-id="86d3d-126">Bei normaler Ausführung gibt dieses Cmdlet keinen Wert für den Erfolg zurück.</span><span class="sxs-lookup"><span data-stu-id="86d3d-126">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="86d3d-127">Wenn Sie den Parameter "PassThru" angeben, schreibt das Cmdlet nach erfolgreicher Ausführung einen Wert in die Pipeline.</span><span class="sxs-lookup"><span data-stu-id="86d3d-127">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="86d3d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86d3d-128">-ResourceGroupName</span></span>
<span data-ttu-id="86d3d-129">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="86d3d-129">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86d3d-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="86d3d-130">-ResourceId</span></span>
<span data-ttu-id="86d3d-131">StorageSyncService-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="86d3d-131">StorageSyncService Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86d3d-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="86d3d-132">-Confirm</span></span>
<span data-ttu-id="86d3d-133">Fordert vor dem Ausführen des Cmdlets zur Bestätigung auf.</span><span class="sxs-lookup"><span data-stu-id="86d3d-133">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86d3d-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="86d3d-134">-WhatIf</span></span>
<span data-ttu-id="86d3d-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="86d3d-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="86d3d-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="86d3d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86d3d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86d3d-137">CommonParameters</span></span>
<span data-ttu-id="86d3d-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86d3d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86d3d-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86d3d-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86d3d-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="86d3d-140">INPUTS</span></span>

### <span data-ttu-id="86d3d-141">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="86d3d-141">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

### <span data-ttu-id="86d3d-142">System.String</span><span class="sxs-lookup"><span data-stu-id="86d3d-142">System.String</span></span>

### <span data-ttu-id="86d3d-143">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="86d3d-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="86d3d-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="86d3d-144">OUTPUTS</span></span>

### <span data-ttu-id="86d3d-145">System.Object</span><span class="sxs-lookup"><span data-stu-id="86d3d-145">System.Object</span></span>
## <span data-ttu-id="86d3d-146">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="86d3d-146">NOTES</span></span>

## <span data-ttu-id="86d3d-147">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="86d3d-147">RELATED LINKS</span></span>
