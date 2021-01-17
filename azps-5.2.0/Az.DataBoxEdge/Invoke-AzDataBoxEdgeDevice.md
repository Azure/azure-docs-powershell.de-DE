---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/invoke-azdataboxedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeDevice.md
ms.openlocfilehash: 29bf8cf612d3569480c62784466879095ebcdb6e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98308435"
---
# <span data-ttu-id="e724b-101">Invoke-AzDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="e724b-101">Invoke-AzDataBoxEdgeDevice</span></span>

## <span data-ttu-id="e724b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e724b-102">SYNOPSIS</span></span>
<span data-ttu-id="e724b-103">Ruft bestimmte Aktionen auf dem Gerät auf.</span><span class="sxs-lookup"><span data-stu-id="e724b-103">Invokes specific actions on the device.</span></span>

## <span data-ttu-id="e724b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e724b-104">SYNTAX</span></span>

### <span data-ttu-id="e724b-105">InvokeScanForUpdateParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e724b-105">InvokeScanForUpdateParameterSet (Default)</span></span>
```
Invoke-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e724b-106">InvokeFetchUpdatesByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e724b-106">InvokeFetchUpdatesByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -ResourceId <String> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e724b-107">InvokeInstallUpdatesByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e724b-107">InvokeInstallUpdatesByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -ResourceId <String> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e724b-108">InvokeScanForUpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e724b-108">InvokeScanForUpdateByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -ResourceId <String> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e724b-109">InvokeInstallUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="e724b-109">InvokeInstallUpdateParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e724b-110">InvokeFetchUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="e724b-110">InvokeFetchUpdateParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e724b-111">InvokeFetchUpdatesByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e724b-111">InvokeFetchUpdatesByDeviceObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -DeviceObject <PSDataBoxEdgeDevice> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e724b-112">InvokeScanForUpdateByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e724b-112">InvokeScanForUpdateByDeviceObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -DeviceObject <PSDataBoxEdgeDevice> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e724b-113">InvokeInstallUpdatesByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e724b-113">InvokeInstallUpdatesByDeviceObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -DeviceObject <PSDataBoxEdgeDevice> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e724b-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e724b-114">DESCRIPTION</span></span>
<span data-ttu-id="e724b-115">Das **Cmdlet Invoke-AzDataBoxEdgeDevice** ruft Aktionen zum Überprüfen, Herunterladen und Installieren der Updates auf dem Data Box Edge-Gerät auf.</span><span class="sxs-lookup"><span data-stu-id="e724b-115">The **Invoke-AzDataBoxEdgeDevice** cmdlet invokes actions to scan, download �and install the updates on the Data Box Edge device.</span></span> <span data-ttu-id="e724b-116">Eine automatische Überprüfung wird täglich auf dem Gerät ausgeführt. Sie können die Überprüfung explizit auslösen, indem Sie dieses Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e724b-116">An automatic scan runs on the device daily, you can trigger the scan explicitly by running this cmdlet.</span></span>

## <span data-ttu-id="e724b-117">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e724b-117">EXAMPLES</span></span>

### <span data-ttu-id="e724b-118">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e724b-118">Example 1</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -ScanForUpdate
```

### <span data-ttu-id="e724b-119">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="e724b-119">Example 2</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -FetchUpdate
```

### <span data-ttu-id="e724b-120">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="e724b-120">Example 3</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -InstallUpdate
```

## <span data-ttu-id="e724b-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e724b-121">PARAMETERS</span></span>

### <span data-ttu-id="e724b-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e724b-122">-AsJob</span></span>
<span data-ttu-id="e724b-123">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="e724b-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e724b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e724b-124">-DefaultProfile</span></span>
<span data-ttu-id="e724b-125">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e724b-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e724b-126">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="e724b-126">-DeviceObject</span></span>
<span data-ttu-id="e724b-127">Geben Sie ein entsprechendes Geräteobjekt an.</span><span class="sxs-lookup"><span data-stu-id="e724b-127">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice
Parameter Sets: InvokeFetchUpdatesByDeviceObjectParameterSet, InvokeScanForUpdateByDeviceObjectParameterSet, InvokeInstallUpdatesByDeviceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e724b-128">-FetchUpdate</span><span class="sxs-lookup"><span data-stu-id="e724b-128">-FetchUpdate</span></span>
<span data-ttu-id="e724b-129">Lädt die Updates auf einem Datenfeld-Edge-/Gatewaygerät herunter.</span><span class="sxs-lookup"><span data-stu-id="e724b-129">Downloads the updates on a data box edge/gateway device</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: InvokeFetchUpdatesByResourceIdParameterSet, InvokeFetchUpdateParameterSet, InvokeFetchUpdatesByDeviceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e724b-130">-InstallUpdate</span><span class="sxs-lookup"><span data-stu-id="e724b-130">-InstallUpdate</span></span>
<span data-ttu-id="e724b-131">Installiert die Updates auf dem Datenfeld-Edge-/Gatewaygerät.</span><span class="sxs-lookup"><span data-stu-id="e724b-131">Installs the updates on the data box edge/gateway device</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: InvokeInstallUpdatesByResourceIdParameterSet, InvokeInstallUpdateParameterSet, InvokeInstallUpdatesByDeviceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e724b-132">-Name</span><span class="sxs-lookup"><span data-stu-id="e724b-132">-Name</span></span>
<span data-ttu-id="e724b-133">Gerätename</span><span class="sxs-lookup"><span data-stu-id="e724b-133">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeScanForUpdateParameterSet, InvokeInstallUpdateParameterSet, InvokeFetchUpdateParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e724b-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e724b-134">-PassThru</span></span>
<span data-ttu-id="e724b-135">gibt "true" zurück, wenn dies erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="e724b-135">returns true if successful</span></span>

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

### <span data-ttu-id="e724b-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e724b-136">-ResourceGroupName</span></span>
<span data-ttu-id="e724b-137">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="e724b-137">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeScanForUpdateParameterSet, InvokeInstallUpdateParameterSet, InvokeFetchUpdateParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e724b-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e724b-138">-ResourceId</span></span>
<span data-ttu-id="e724b-139">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="e724b-139">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeFetchUpdatesByResourceIdParameterSet, InvokeInstallUpdatesByResourceIdParameterSet, InvokeScanForUpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e724b-140">-ScanForUpdate</span><span class="sxs-lookup"><span data-stu-id="e724b-140">-ScanForUpdate</span></span>
<span data-ttu-id="e724b-141">Sucht auf einem Datenfeld-Edge-/Gatewaygerät nach Updates.</span><span class="sxs-lookup"><span data-stu-id="e724b-141">Scans for updates on a data box edge/gateway device.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: InvokeScanForUpdateParameterSet, InvokeScanForUpdateByResourceIdParameterSet, InvokeScanForUpdateByDeviceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e724b-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e724b-142">-Confirm</span></span>
<span data-ttu-id="e724b-143">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e724b-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e724b-144">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="e724b-144">-WhatIf</span></span>
<span data-ttu-id="e724b-145">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e724b-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e724b-146">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e724b-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e724b-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e724b-147">CommonParameters</span></span>
<span data-ttu-id="e724b-148">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e724b-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e724b-149">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e724b-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e724b-150">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e724b-150">INPUTS</span></span>

### <span data-ttu-id="e724b-151">Keine</span><span class="sxs-lookup"><span data-stu-id="e724b-151">None</span></span>

## <span data-ttu-id="e724b-152">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e724b-152">OUTPUTS</span></span>

### <span data-ttu-id="e724b-153">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e724b-153">System.Boolean</span></span>

## <span data-ttu-id="e724b-154">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e724b-154">NOTES</span></span>

## <span data-ttu-id="e724b-155">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e724b-155">RELATED LINKS</span></span>
