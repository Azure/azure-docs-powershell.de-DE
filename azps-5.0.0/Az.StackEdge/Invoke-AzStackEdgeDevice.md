---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/invoke-azstackedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeDevice.md
ms.openlocfilehash: f25aeb501ff046a25330ad5db47bbdb06fbe7b35
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302386"
---
# <span data-ttu-id="cc0d7-101">Invoke-AzStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="cc0d7-101">Invoke-AzStackEdgeDevice</span></span>

## <span data-ttu-id="cc0d7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cc0d7-102">SYNOPSIS</span></span>
<span data-ttu-id="cc0d7-103">Ruft bestimmte Aktionen auf dem Gerät auf.</span><span class="sxs-lookup"><span data-stu-id="cc0d7-103">Invokes specific actions on the device.</span></span>

## <span data-ttu-id="cc0d7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cc0d7-104">SYNTAX</span></span>

### <span data-ttu-id="cc0d7-105">InvokeScanForUpdateParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="cc0d7-105">InvokeScanForUpdateParameterSet (Default)</span></span>
```
Invoke-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc0d7-106">InvokeFetchUpdatesByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc0d7-106">InvokeFetchUpdatesByResourceIdParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -ResourceId <String> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc0d7-107">InvokeInstallUpdatesByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc0d7-107">InvokeInstallUpdatesByResourceIdParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -ResourceId <String> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc0d7-108">InvokeScanForUpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc0d7-108">InvokeScanForUpdateByResourceIdParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -ResourceId <String> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc0d7-109">InvokeInstallUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc0d7-109">InvokeInstallUpdateParameterSet</span></span>
```
Invoke-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc0d7-110">InvokeFetchUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc0d7-110">InvokeFetchUpdateParameterSet</span></span>
```
Invoke-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc0d7-111">InvokeFetchUpdatesByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc0d7-111">InvokeFetchUpdatesByDeviceObjectParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -DeviceObject <PSStackEdgeDevice> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc0d7-112">InvokeScanForUpdateByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc0d7-112">InvokeScanForUpdateByDeviceObjectParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -DeviceObject <PSStackEdgeDevice> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc0d7-113">InvokeInstallUpdatesByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc0d7-113">InvokeInstallUpdatesByDeviceObjectParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -DeviceObject <PSStackEdgeDevice> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc0d7-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cc0d7-114">DESCRIPTION</span></span>
<span data-ttu-id="cc0d7-115">Das Cmdlet **Invoke-AzStackEdgeDevice** ruft Aktionen auf, um die Updates auf dem Stack-Edge-Gerät zu überprüfen, herunterzuladen und zu installieren.</span><span class="sxs-lookup"><span data-stu-id="cc0d7-115">The **Invoke-AzStackEdgeDevice** cmdlet invokes actions to scan, download �and install the updates on the Stack Edge device.</span></span> <span data-ttu-id="cc0d7-116">Eine automatische Überprüfung wird täglich auf dem Gerät ausgeführt, und Sie können den Scan explizit auslösen, indem Sie dieses Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cc0d7-116">An automatic scan runs on the device daily, you can trigger the scan explicitly by running this cmdlet.</span></span>

## <span data-ttu-id="cc0d7-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cc0d7-117">EXAMPLES</span></span>

### <span data-ttu-id="cc0d7-118">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="cc0d7-118">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -ScanForUpdate
```

### <span data-ttu-id="cc0d7-119">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="cc0d7-119">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -FetchUpdate
```

### <span data-ttu-id="cc0d7-120">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="cc0d7-120">Example 3</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -InstallUpdate
```

## <span data-ttu-id="cc0d7-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="cc0d7-121">PARAMETERS</span></span>

### <span data-ttu-id="cc0d7-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cc0d7-122">-AsJob</span></span>
<span data-ttu-id="cc0d7-123">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="cc0d7-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cc0d7-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc0d7-124">-DefaultProfile</span></span>
<span data-ttu-id="cc0d7-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cc0d7-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc0d7-126">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="cc0d7-126">-DeviceObject</span></span>
<span data-ttu-id="cc0d7-127">Bitte geben Sie das entsprechende Device-Objekt an</span><span class="sxs-lookup"><span data-stu-id="cc0d7-127">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice
Parameter Sets: InvokeFetchUpdatesByDeviceObjectParameterSet, InvokeScanForUpdateByDeviceObjectParameterSet, InvokeInstallUpdatesByDeviceObjectParameterSet
Aliases: Device

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cc0d7-128">-FetchUpdate</span><span class="sxs-lookup"><span data-stu-id="cc0d7-128">-FetchUpdate</span></span>
<span data-ttu-id="cc0d7-129">Herunterladen der Updates auf einem Stack Edge/Gateway-Gerät</span><span class="sxs-lookup"><span data-stu-id="cc0d7-129">Downloads the updates on a Stack edge/gateway device</span></span>

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

### <span data-ttu-id="cc0d7-130">-InstallUpdate</span><span class="sxs-lookup"><span data-stu-id="cc0d7-130">-InstallUpdate</span></span>
<span data-ttu-id="cc0d7-131">Installiert die Updates auf dem Stack Edge/Gateway-Gerät</span><span class="sxs-lookup"><span data-stu-id="cc0d7-131">Installs the updates on the Stack edge/gateway device</span></span>

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

### <span data-ttu-id="cc0d7-132">-Name</span><span class="sxs-lookup"><span data-stu-id="cc0d7-132">-Name</span></span>
<span data-ttu-id="cc0d7-133">Geräte Name</span><span class="sxs-lookup"><span data-stu-id="cc0d7-133">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeScanForUpdateParameterSet, InvokeInstallUpdateParameterSet, InvokeFetchUpdateParameterSet
Aliases: DeviceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc0d7-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cc0d7-134">-PassThru</span></span>
<span data-ttu-id="cc0d7-135">gibt "true" zurück, wenn erfolgreich</span><span class="sxs-lookup"><span data-stu-id="cc0d7-135">returns true if successful</span></span>

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

### <span data-ttu-id="cc0d7-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc0d7-136">-ResourceGroupName</span></span>
<span data-ttu-id="cc0d7-137">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="cc0d7-137">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeScanForUpdateParameterSet, InvokeInstallUpdateParameterSet, InvokeFetchUpdateParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc0d7-138">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="cc0d7-138">-ResourceId</span></span>
<span data-ttu-id="cc0d7-139">Azure-Hilfsquelle</span><span class="sxs-lookup"><span data-stu-id="cc0d7-139">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeFetchUpdatesByResourceIdParameterSet, InvokeInstallUpdatesByResourceIdParameterSet, InvokeScanForUpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc0d7-140">-ScanForUpdate</span><span class="sxs-lookup"><span data-stu-id="cc0d7-140">-ScanForUpdate</span></span>
<span data-ttu-id="cc0d7-141">Sucht nach Updates auf einem Stack Edge/Gateway-Gerät.</span><span class="sxs-lookup"><span data-stu-id="cc0d7-141">Scans for updates on a Stack edge/gateway device.</span></span>

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

### <span data-ttu-id="cc0d7-142">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="cc0d7-142">-Confirm</span></span>
<span data-ttu-id="cc0d7-143">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cc0d7-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc0d7-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc0d7-144">-WhatIf</span></span>
<span data-ttu-id="cc0d7-145">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cc0d7-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cc0d7-146">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cc0d7-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc0d7-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc0d7-147">CommonParameters</span></span>
<span data-ttu-id="cc0d7-148">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc0d7-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc0d7-149">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cc0d7-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc0d7-150">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cc0d7-150">INPUTS</span></span>

### <span data-ttu-id="cc0d7-151">Keine</span><span class="sxs-lookup"><span data-stu-id="cc0d7-151">None</span></span>

## <span data-ttu-id="cc0d7-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cc0d7-152">OUTPUTS</span></span>

### <span data-ttu-id="cc0d7-153">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cc0d7-153">System.Boolean</span></span>

## <span data-ttu-id="cc0d7-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="cc0d7-154">NOTES</span></span>

## <span data-ttu-id="cc0d7-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cc0d7-155">RELATED LINKS</span></span>
