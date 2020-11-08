---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/remove-azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncGroup.md
ms.openlocfilehash: dad4af4f954fae03a68728de928614a81eed5e5a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176208"
---
# <span data-ttu-id="54d5e-101">Remove-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="54d5e-101">Remove-AzStorageSyncGroup</span></span>

## <span data-ttu-id="54d5e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="54d5e-102">SYNOPSIS</span></span>
<span data-ttu-id="54d5e-103">Mit diesem Befehl wird die angegebene Synchronisierungsgruppe gelöscht.</span><span class="sxs-lookup"><span data-stu-id="54d5e-103">This command will delete the specified sync group.</span></span>

## <span data-ttu-id="54d5e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="54d5e-104">SYNTAX</span></span>

### <span data-ttu-id="54d5e-105">StringParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="54d5e-105">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-Name] <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="54d5e-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="54d5e-106">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncGroup [-InputObject] <PSSyncGroup> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54d5e-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="54d5e-107">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncGroup [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54d5e-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="54d5e-108">DESCRIPTION</span></span>
<span data-ttu-id="54d5e-109">Mit diesem Befehl wird die angegebene Synchronisierungsgruppe gelöscht.</span><span class="sxs-lookup"><span data-stu-id="54d5e-109">This command will delete the specified sync group.</span></span> <span data-ttu-id="54d5e-110">Eine Synchronisierungsgruppe kann nur entfernt werden, wenn alle enthaltenen Endpunkte zuerst gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="54d5e-110">A sync group can only be removed when all of the contained endpoints are deleted first.</span></span>

## <span data-ttu-id="54d5e-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="54d5e-111">EXAMPLES</span></span>

### <span data-ttu-id="54d5e-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="54d5e-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncGroup -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -Name "mySyncGroupName"
```

<span data-ttu-id="54d5e-113">Mit diesem Befehl wird die Synchronisierungsgruppe entfernt.</span><span class="sxs-lookup"><span data-stu-id="54d5e-113">This command will remove the sync group.</span></span>

## <span data-ttu-id="54d5e-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="54d5e-114">PARAMETERS</span></span>

### <span data-ttu-id="54d5e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="54d5e-115">-AsJob</span></span>
<span data-ttu-id="54d5e-116">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="54d5e-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="54d5e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54d5e-117">-DefaultProfile</span></span>
<span data-ttu-id="54d5e-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="54d5e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54d5e-119">-Force</span><span class="sxs-lookup"><span data-stu-id="54d5e-119">-Force</span></span>
<span data-ttu-id="54d5e-120">Supply-Force, um die Bestätigung dieses Befehls zu überspringen.</span><span class="sxs-lookup"><span data-stu-id="54d5e-120">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="54d5e-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="54d5e-121">-InputObject</span></span>
<span data-ttu-id="54d5e-122">SyncGroup-Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="54d5e-122">SyncGroup Input Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="54d5e-123">-Name</span><span class="sxs-lookup"><span data-stu-id="54d5e-123">-Name</span></span>
<span data-ttu-id="54d5e-124">Der Name des SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="54d5e-124">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: SyncGroupName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54d5e-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="54d5e-125">-PassThru</span></span>
<span data-ttu-id="54d5e-126">Bei normaler Ausführung gibt dieses Cmdlet keinen Wert für Success zurück.</span><span class="sxs-lookup"><span data-stu-id="54d5e-126">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="54d5e-127">Wenn Sie den passthru-Parameter angeben, schreibt das Cmdlet nach der erfolgreichen Ausführung einen Wert in die Pipeline.</span><span class="sxs-lookup"><span data-stu-id="54d5e-127">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="54d5e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54d5e-128">-ResourceGroupName</span></span>
<span data-ttu-id="54d5e-129">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="54d5e-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="54d5e-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="54d5e-130">-ResourceId</span></span>
<span data-ttu-id="54d5e-131">SyncGroup-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="54d5e-131">SyncGroup Resource Id</span></span>

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

### <span data-ttu-id="54d5e-132">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="54d5e-132">-StorageSyncServiceName</span></span>
<span data-ttu-id="54d5e-133">Der Name des StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="54d5e-133">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54d5e-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="54d5e-134">-Confirm</span></span>
<span data-ttu-id="54d5e-135">Fordert zur Bestätigung auf, bevor das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="54d5e-135">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54d5e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54d5e-136">-WhatIf</span></span>
<span data-ttu-id="54d5e-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="54d5e-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="54d5e-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="54d5e-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54d5e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54d5e-139">CommonParameters</span></span>
<span data-ttu-id="54d5e-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54d5e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54d5e-141">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54d5e-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54d5e-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="54d5e-142">INPUTS</span></span>

### <span data-ttu-id="54d5e-143">Microsoft. Azure. Commands. StorageSync. Models. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="54d5e-143">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="54d5e-144">System. String</span><span class="sxs-lookup"><span data-stu-id="54d5e-144">System.String</span></span>

### <span data-ttu-id="54d5e-145">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="54d5e-145">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="54d5e-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="54d5e-146">OUTPUTS</span></span>

### <span data-ttu-id="54d5e-147">System. Object</span><span class="sxs-lookup"><span data-stu-id="54d5e-147">System.Object</span></span>
## <span data-ttu-id="54d5e-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="54d5e-148">NOTES</span></span>

## <span data-ttu-id="54d5e-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="54d5e-149">RELATED LINKS</span></span>
