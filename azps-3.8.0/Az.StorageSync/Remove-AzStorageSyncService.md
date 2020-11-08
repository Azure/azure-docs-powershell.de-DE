---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/remove-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncService.md
ms.openlocfilehash: f64c085f742eeabea235660d4af7ba6bd5970fdf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003381"
---
# <span data-ttu-id="c1c1c-101">Remove-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="c1c1c-101">Remove-AzStorageSyncService</span></span>

## <span data-ttu-id="c1c1c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c1c1c-102">SYNOPSIS</span></span>
<span data-ttu-id="c1c1c-103">Mit diesem Befehl wird der angegebene Speicher Synchronisierungsdienst gelöscht.</span><span class="sxs-lookup"><span data-stu-id="c1c1c-103">This command will delete the specified storage sync service.</span></span>

## <span data-ttu-id="c1c1c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c1c1c-104">SYNTAX</span></span>

### <span data-ttu-id="c1c1c-105">StringParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c1c1c-105">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1c1c-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1c1c-106">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncService [-InputObject] <PSStorageSyncService> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1c1c-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1c1c-107">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncService [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1c1c-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c1c1c-108">DESCRIPTION</span></span>
<span data-ttu-id="c1c1c-109">Mit diesem Befehl wird der angegebene Speicher Synchronisierungsdienst gelöscht.</span><span class="sxs-lookup"><span data-stu-id="c1c1c-109">This command will delete the specified storage sync service.</span></span> <span data-ttu-id="c1c1c-110">Ein Speicher Synchronisierungsdienst kann nur entfernt werden, wenn alle enthaltenen Synchronisierungsgruppen und registrierten Server zuerst gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="c1c1c-110">A storage sync service can only be removed when all of the contained sync groups and registered servers are deleted first.</span></span>

## <span data-ttu-id="c1c1c-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c1c1c-111">EXAMPLES</span></span>

### <span data-ttu-id="c1c1c-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c1c1c-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncService -Force -ResourceGroupName "myResourceGroup" -Name "myStorageSyncServiceName"
```

<span data-ttu-id="c1c1c-113">Mit diesem Befehl wird der Speicher Synchronisierungsdienst entfernt.</span><span class="sxs-lookup"><span data-stu-id="c1c1c-113">This command will remove the storage sync service.</span></span>

## <span data-ttu-id="c1c1c-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="c1c1c-114">PARAMETERS</span></span>

### <span data-ttu-id="c1c1c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c1c1c-115">-AsJob</span></span>
<span data-ttu-id="c1c1c-116">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="c1c1c-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c1c1c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1c1c-117">-DefaultProfile</span></span>
<span data-ttu-id="c1c1c-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c1c1c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1c1c-119">-Force</span><span class="sxs-lookup"><span data-stu-id="c1c1c-119">-Force</span></span>
<span data-ttu-id="c1c1c-120">Supply-Force, um die Bestätigung dieses Befehls zu überspringen.</span><span class="sxs-lookup"><span data-stu-id="c1c1c-120">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="c1c1c-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c1c1c-121">-InputObject</span></span>
<span data-ttu-id="c1c1c-122">StorageSyncService-Eingabeobjekt, das normalerweise durch die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="c1c1c-122">StorageSyncService Input Object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="c1c1c-123">-Name</span><span class="sxs-lookup"><span data-stu-id="c1c1c-123">-Name</span></span>
<span data-ttu-id="c1c1c-124">Der Name des StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="c1c1c-124">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="c1c1c-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c1c1c-125">-PassThru</span></span>
<span data-ttu-id="c1c1c-126">Bei normaler Ausführung gibt dieses Cmdlet keinen Wert für Success zurück.</span><span class="sxs-lookup"><span data-stu-id="c1c1c-126">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="c1c1c-127">Wenn Sie den passthru-Parameter angeben, schreibt das Cmdlet nach der erfolgreichen Ausführung einen Wert in die Pipeline.</span><span class="sxs-lookup"><span data-stu-id="c1c1c-127">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="c1c1c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1c1c-128">-ResourceGroupName</span></span>
<span data-ttu-id="c1c1c-129">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c1c1c-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="c1c1c-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="c1c1c-130">-ResourceId</span></span>
<span data-ttu-id="c1c1c-131">StorageSyncService-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="c1c1c-131">StorageSyncService Resource Id</span></span>

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

### <span data-ttu-id="c1c1c-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c1c1c-132">-Confirm</span></span>
<span data-ttu-id="c1c1c-133">Fordert zur Bestätigung auf, bevor das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c1c1c-133">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1c1c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1c1c-134">-WhatIf</span></span>
<span data-ttu-id="c1c1c-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c1c1c-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c1c1c-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c1c1c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1c1c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1c1c-137">CommonParameters</span></span>
<span data-ttu-id="c1c1c-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1c1c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1c1c-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1c1c-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1c1c-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c1c1c-140">INPUTS</span></span>

### <span data-ttu-id="c1c1c-141">Microsoft. Azure. Commands. StorageSync. Models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="c1c1c-141">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

### <span data-ttu-id="c1c1c-142">System. String</span><span class="sxs-lookup"><span data-stu-id="c1c1c-142">System.String</span></span>

### <span data-ttu-id="c1c1c-143">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="c1c1c-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c1c1c-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c1c1c-144">OUTPUTS</span></span>

### <span data-ttu-id="c1c1c-145">System. Object</span><span class="sxs-lookup"><span data-stu-id="c1c1c-145">System.Object</span></span>
## <span data-ttu-id="c1c1c-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="c1c1c-146">NOTES</span></span>

## <span data-ttu-id="c1c1c-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c1c1c-147">RELATED LINKS</span></span>
