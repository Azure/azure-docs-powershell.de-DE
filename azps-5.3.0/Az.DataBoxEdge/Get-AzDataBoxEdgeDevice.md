---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeDevice.md
ms.openlocfilehash: 314ebb4412b88e5476a63cf5a1025f26e2c41e69
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470642"
---
# <span data-ttu-id="bd75e-101">Get-AzDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="bd75e-101">Get-AzDataBoxEdgeDevice</span></span>

## <span data-ttu-id="bd75e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd75e-102">SYNOPSIS</span></span>
<span data-ttu-id="bd75e-103">Ruft die Informationen zu verfügbaren Data Box Edge-Geräten ab.</span><span class="sxs-lookup"><span data-stu-id="bd75e-103">Gets the information on available Data Box Edge devices.</span></span>

## <span data-ttu-id="bd75e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bd75e-104">SYNTAX</span></span>

### <span data-ttu-id="bd75e-105">ListByParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="bd75e-105">ListByParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeDevice [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bd75e-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd75e-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bd75e-107">GetExtendedInfoByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd75e-107">GetExtendedInfoByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-ExtendedInfo] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bd75e-108">GetNetworkSettingByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd75e-108">GetNetworkSettingByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-NetworkSetting] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bd75e-109">GetSummaryUpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd75e-109">GetSummaryUpdateByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-UpdateSummary] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bd75e-110">GetAlertByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd75e-110">GetAlertByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-Alert] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bd75e-111">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd75e-111">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bd75e-112">GetSummaryUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd75e-112">GetSummaryUpdateParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-UpdateSummary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bd75e-113">GetNetworkSettingParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd75e-113">GetNetworkSettingParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-NetworkSetting]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bd75e-114">GetExtendedInfoParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd75e-114">GetExtendedInfoParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-ExtendedInfo]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bd75e-115">GetAlertParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd75e-115">GetAlertParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-Alert]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd75e-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bd75e-116">DESCRIPTION</span></span>
<span data-ttu-id="bd75e-117">Das **Cmdlet "Get-AzDataBoxEdgeDevice"** ruft die Informationen zu den verfügbaren Datenfeld-Edgegeräten ab.</span><span class="sxs-lookup"><span data-stu-id="bd75e-117">The **Get-AzDataBoxEdgeDevice** cmdlet gets the information about the available Data Box Edge Devices.</span></span> <span data-ttu-id="bd75e-118">Sie können den Namen des Geräts zusammen mit dem Namen der Ressourcengruppe angeben, um die Informationen auf einem bestimmten Gerät zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="bd75e-118">You can specify the Name of the device along with the Resource Group Name to get the information on a specific device.</span></span> 

## <span data-ttu-id="bd75e-119">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bd75e-119">EXAMPLES</span></span>

### <span data-ttu-id="bd75e-120">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="bd75e-120">Example 1</span></span>
```powershell
PS C:\>Get-AzDataBoxEdgeDevice
Name               ResourceGroupName  Model   Location
----               -----------------  -----   --------
deviceNameOne      resourceGroupName1 Edge    eastus
deviceNameTwo      resourceGroupName2 Edge    westus
deviceNameThree    resourceGroupName3 Gateway eastus
```

### <span data-ttu-id="bd75e-121">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="bd75e-121">Example 2</span></span>
```powershell
PS C:\>Get-AzDataBoxEdgeDevice -ResourceId /subscriptions/subscriptionId/resourcegroups/resourceGroupName/providers/Microsoft.DataBoxEdge/dataBoxEdgeDevices/deviceName
Name            ResourceGroupName    Model   Location
----            -----------------    -----   --------
deviceName      resourceGroupName    Edge    eastus
```

### <span data-ttu-id="bd75e-122">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="bd75e-122">Example 3</span></span>
```powershell
PS C:\>Get-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -DeviceName deviceName
Name            ResourceGroupName    Model   Location
----            -----------------    -----   --------
deviceName      resourceGroupName    Edge    eastus
```

## <span data-ttu-id="bd75e-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bd75e-123">PARAMETERS</span></span>

### <span data-ttu-id="bd75e-124">-Alert</span><span class="sxs-lookup"><span data-stu-id="bd75e-124">-Alert</span></span>
<span data-ttu-id="bd75e-125">Abrufen der Benachrichtigungen auf dem Datenfeldrand/Gatewaygerät</span><span class="sxs-lookup"><span data-stu-id="bd75e-125">Fetch the alerts on the data box edge/gateway device</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetAlertByResourceIdParameterSet, GetAlertParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd75e-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd75e-126">-DefaultProfile</span></span>
<span data-ttu-id="bd75e-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bd75e-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd75e-128">-ExtendedInfo</span><span class="sxs-lookup"><span data-stu-id="bd75e-128">-ExtendedInfo</span></span>
<span data-ttu-id="bd75e-129">Ruft zusätzliche Informationen für das angegebene Edge-/Datenfeld-Gatewaygerät im Datenfeld ab.</span><span class="sxs-lookup"><span data-stu-id="bd75e-129">Gets additional information for the specified Data Box Edge/Data Box Gateway device</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetExtendedInfoByResourceIdParameterSet, GetExtendedInfoParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd75e-130">-Name</span><span class="sxs-lookup"><span data-stu-id="bd75e-130">-Name</span></span>
<span data-ttu-id="bd75e-131">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="bd75e-131">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetSummaryUpdateParameterSet, GetNetworkSettingParameterSet, GetExtendedInfoParameterSet, GetAlertParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd75e-132">-NetworkSetting</span><span class="sxs-lookup"><span data-stu-id="bd75e-132">-NetworkSetting</span></span>
<span data-ttu-id="bd75e-133">Ruft die Netzwerkeinstellungen des angegebenen Edge-/Datenfeld-Gatewaygeräts im Datenfeld ab.</span><span class="sxs-lookup"><span data-stu-id="bd75e-133">Gets the network settings of the specified Data Box Edge/Data Box Gateway device</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetNetworkSettingByResourceIdParameterSet, GetNetworkSettingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd75e-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd75e-134">-ResourceGroupName</span></span>
<span data-ttu-id="bd75e-135">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="bd75e-135">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListByParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetSummaryUpdateParameterSet, GetNetworkSettingParameterSet, GetExtendedInfoParameterSet, GetAlertParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd75e-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bd75e-136">-ResourceId</span></span>
<span data-ttu-id="bd75e-137">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="bd75e-137">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet, GetExtendedInfoByResourceIdParameterSet, GetNetworkSettingByResourceIdParameterSet, GetSummaryUpdateByResourceIdParameterSet, GetAlertByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd75e-138">-UpdateSummary</span><span class="sxs-lookup"><span data-stu-id="bd75e-138">-UpdateSummary</span></span>
<span data-ttu-id="bd75e-139">Ruft Informationen zur Verfügbarkeit von Updates basierend auf der letzten Überprüfung des Geräts ab.</span><span class="sxs-lookup"><span data-stu-id="bd75e-139">Gets information about the availability of updates based on the last scan of the device.</span></span> <span data-ttu-id="bd75e-140">Außerdem werden Informationen zu laufenden Download- oder Installationsaufträgen auf dem Gerät angezeigt.</span><span class="sxs-lookup"><span data-stu-id="bd75e-140">It also gets information about any ongoing download or install jobs on the device.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetSummaryUpdateByResourceIdParameterSet, GetSummaryUpdateParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd75e-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd75e-141">CommonParameters</span></span>
<span data-ttu-id="bd75e-142">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd75e-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd75e-143">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bd75e-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd75e-144">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bd75e-144">INPUTS</span></span>

### <span data-ttu-id="bd75e-145">Keine</span><span class="sxs-lookup"><span data-stu-id="bd75e-145">None</span></span>

## <span data-ttu-id="bd75e-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bd75e-146">OUTPUTS</span></span>

### <span data-ttu-id="bd75e-147">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="bd75e-147">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

### <span data-ttu-id="bd75e-148">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeNetworkAdapter</span><span class="sxs-lookup"><span data-stu-id="bd75e-148">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeNetworkAdapter</span></span>

### <span data-ttu-id="bd75e-149">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDeviceExtendedInfo</span><span class="sxs-lookup"><span data-stu-id="bd75e-149">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDeviceExtendedInfo</span></span>

### <span data-ttu-id="bd75e-150">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUpdateSummary</span><span class="sxs-lookup"><span data-stu-id="bd75e-150">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUpdateSummary</span></span>

### <span data-ttu-id="bd75e-151">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeAlert</span><span class="sxs-lookup"><span data-stu-id="bd75e-151">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeAlert</span></span>

## <span data-ttu-id="bd75e-152">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="bd75e-152">NOTES</span></span>

## <span data-ttu-id="bd75e-153">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="bd75e-153">RELATED LINKS</span></span>
