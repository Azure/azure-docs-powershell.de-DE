---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/Az.storagesync/remove-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncService.md
ms.openlocfilehash: 648ef711d030f7600863d286df24cfdf1d2f7927
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929624"
---
# <span data-ttu-id="867fe-101">Remove-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="867fe-101">Remove-AzStorageSyncService</span></span>

## <span data-ttu-id="867fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="867fe-102">SYNOPSIS</span></span>
<span data-ttu-id="867fe-103">Mit diesem Befehl wird der angegebene Speichersynchronisierungsdienst gelöscht.</span><span class="sxs-lookup"><span data-stu-id="867fe-103">This command will delete the specified storage sync service.</span></span>

## <span data-ttu-id="867fe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="867fe-104">SYNTAX</span></span>

### <span data-ttu-id="867fe-105">StringParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="867fe-105">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="867fe-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="867fe-106">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncService [-InputObject] <PSStorageSyncService> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="867fe-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="867fe-107">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncService [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="867fe-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="867fe-108">DESCRIPTION</span></span>
<span data-ttu-id="867fe-109">Mit diesem Befehl wird der angegebene Speichersynchronisierungsdienst gelöscht.</span><span class="sxs-lookup"><span data-stu-id="867fe-109">This command will delete the specified storage sync service.</span></span> <span data-ttu-id="867fe-110">Ein Speichersynchronisierungsdienst kann nur entfernt werden, wenn zuerst alle enthaltenen Synchronisierungsgruppen und registrierten Server gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="867fe-110">A storage sync service can only be removed when all of the contained sync groups and registered servers are deleted first.</span></span>

## <span data-ttu-id="867fe-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="867fe-111">EXAMPLES</span></span>

### <span data-ttu-id="867fe-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="867fe-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncService -Force -ResourceGroupName "myResourceGroup" -Name "myStorageSyncServiceName"
```

<span data-ttu-id="867fe-113">Mit diesem Befehl wird der Speichersynchronisierungsdienst entfernt.</span><span class="sxs-lookup"><span data-stu-id="867fe-113">This command will remove the storage sync service.</span></span>

## <span data-ttu-id="867fe-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="867fe-114">PARAMETERS</span></span>

### <span data-ttu-id="867fe-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="867fe-115">-AsJob</span></span>
<span data-ttu-id="867fe-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="867fe-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="867fe-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="867fe-117">-DefaultProfile</span></span>
<span data-ttu-id="867fe-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="867fe-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="867fe-119">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="867fe-119">-Force</span></span>
<span data-ttu-id="867fe-120">Supply -Force to skip confirmation of this command.</span><span class="sxs-lookup"><span data-stu-id="867fe-120">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="867fe-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="867fe-121">-InputObject</span></span>
<span data-ttu-id="867fe-122">StorageSyncService-Eingabeobjekt, das normalerweise über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="867fe-122">StorageSyncService Input Object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="867fe-123">-Name</span><span class="sxs-lookup"><span data-stu-id="867fe-123">-Name</span></span>
<span data-ttu-id="867fe-124">Name des StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="867fe-124">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="867fe-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="867fe-125">-PassThru</span></span>
<span data-ttu-id="867fe-126">Bei normaler Ausführung gibt dieses Cmdlet keinen Wert für den Erfolg zurück.</span><span class="sxs-lookup"><span data-stu-id="867fe-126">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="867fe-127">Wenn Sie den Parameter PassThru angeben, schreibt das Cmdlet nach der erfolgreichen Ausführung einen Wert in die Pipeline.</span><span class="sxs-lookup"><span data-stu-id="867fe-127">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="867fe-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="867fe-128">-ResourceGroupName</span></span>
<span data-ttu-id="867fe-129">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="867fe-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="867fe-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="867fe-130">-ResourceId</span></span>
<span data-ttu-id="867fe-131">StorageSyncService Resource Id</span><span class="sxs-lookup"><span data-stu-id="867fe-131">StorageSyncService Resource Id</span></span>

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

### <span data-ttu-id="867fe-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="867fe-132">-Confirm</span></span>
<span data-ttu-id="867fe-133">Fordert sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="867fe-133">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="867fe-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="867fe-134">-WhatIf</span></span>
<span data-ttu-id="867fe-135">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="867fe-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="867fe-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="867fe-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="867fe-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="867fe-137">CommonParameters</span></span>
<span data-ttu-id="867fe-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="867fe-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="867fe-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="867fe-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="867fe-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="867fe-140">INPUTS</span></span>

### <span data-ttu-id="867fe-141">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="867fe-141">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

### <span data-ttu-id="867fe-142">System.String</span><span class="sxs-lookup"><span data-stu-id="867fe-142">System.String</span></span>

### <span data-ttu-id="867fe-143">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="867fe-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="867fe-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="867fe-144">OUTPUTS</span></span>

### <span data-ttu-id="867fe-145">System.Object</span><span class="sxs-lookup"><span data-stu-id="867fe-145">System.Object</span></span>
## <span data-ttu-id="867fe-146">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="867fe-146">NOTES</span></span>

## <span data-ttu-id="867fe-147">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="867fe-147">RELATED LINKS</span></span>
