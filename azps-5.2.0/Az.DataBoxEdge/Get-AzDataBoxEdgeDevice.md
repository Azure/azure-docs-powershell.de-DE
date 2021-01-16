---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeDevice.md
ms.openlocfilehash: 314ebb4412b88e5476a63cf5a1025f26e2c41e69
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98292930"
---
# <span data-ttu-id="4a204-101">Get-AzDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="4a204-101">Get-AzDataBoxEdgeDevice</span></span>

## <span data-ttu-id="4a204-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a204-102">SYNOPSIS</span></span>
<span data-ttu-id="4a204-103">Ruft die Informationen zu verfügbaren Data Box Edge-Geräten ab.</span><span class="sxs-lookup"><span data-stu-id="4a204-103">Gets the information on available Data Box Edge devices.</span></span>

## <span data-ttu-id="4a204-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4a204-104">SYNTAX</span></span>

### <span data-ttu-id="4a204-105">ListByParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="4a204-105">ListByParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeDevice [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4a204-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a204-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4a204-107">GetExtendedInfoByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a204-107">GetExtendedInfoByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-ExtendedInfo] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4a204-108">GetNetworkSettingByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a204-108">GetNetworkSettingByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-NetworkSetting] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4a204-109">GetSummaryUpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a204-109">GetSummaryUpdateByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-UpdateSummary] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4a204-110">GetAlertByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a204-110">GetAlertByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-Alert] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4a204-111">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a204-111">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4a204-112">GetSummaryUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a204-112">GetSummaryUpdateParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-UpdateSummary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4a204-113">GetNetworkSettingParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a204-113">GetNetworkSettingParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-NetworkSetting]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4a204-114">GetExtendedInfoParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a204-114">GetExtendedInfoParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-ExtendedInfo]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4a204-115">GetAlertParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a204-115">GetAlertParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-Alert]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a204-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4a204-116">DESCRIPTION</span></span>
<span data-ttu-id="4a204-117">Das **Cmdlet "Get-AzDataBoxEdgeDevice"** ruft die Informationen zu den verfügbaren Datenfeld-Edgegeräten ab.</span><span class="sxs-lookup"><span data-stu-id="4a204-117">The **Get-AzDataBoxEdgeDevice** cmdlet gets the information about the available Data Box Edge Devices.</span></span> <span data-ttu-id="4a204-118">Sie können den Namen des Geräts zusammen mit dem Namen der Ressourcengruppe angeben, um die Informationen auf einem bestimmten Gerät zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4a204-118">You can specify the Name of the device along with the Resource Group Name to get the information on a specific device.</span></span> 

## <span data-ttu-id="4a204-119">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4a204-119">EXAMPLES</span></span>

### <span data-ttu-id="4a204-120">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4a204-120">Example 1</span></span>
```powershell
PS C:\>Get-AzDataBoxEdgeDevice
Name               ResourceGroupName  Model   Location
----               -----------------  -----   --------
deviceNameOne      resourceGroupName1 Edge    eastus
deviceNameTwo      resourceGroupName2 Edge    westus
deviceNameThree    resourceGroupName3 Gateway eastus
```

### <span data-ttu-id="4a204-121">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="4a204-121">Example 2</span></span>
```powershell
PS C:\>Get-AzDataBoxEdgeDevice -ResourceId /subscriptions/subscriptionId/resourcegroups/resourceGroupName/providers/Microsoft.DataBoxEdge/dataBoxEdgeDevices/deviceName
Name            ResourceGroupName    Model   Location
----            -----------------    -----   --------
deviceName      resourceGroupName    Edge    eastus
```

### <span data-ttu-id="4a204-122">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="4a204-122">Example 3</span></span>
```powershell
PS C:\>Get-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -DeviceName deviceName
Name            ResourceGroupName    Model   Location
----            -----------------    -----   --------
deviceName      resourceGroupName    Edge    eastus
```

## <span data-ttu-id="4a204-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4a204-123">PARAMETERS</span></span>

### <span data-ttu-id="4a204-124">-Alert</span><span class="sxs-lookup"><span data-stu-id="4a204-124">-Alert</span></span>
<span data-ttu-id="4a204-125">Abrufen der Benachrichtigungen auf dem Datenfeldrand/Gatewaygerät</span><span class="sxs-lookup"><span data-stu-id="4a204-125">Fetch the alerts on the data box edge/gateway device</span></span>

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

### <span data-ttu-id="4a204-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a204-126">-DefaultProfile</span></span>
<span data-ttu-id="4a204-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4a204-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a204-128">-ExtendedInfo</span><span class="sxs-lookup"><span data-stu-id="4a204-128">-ExtendedInfo</span></span>
<span data-ttu-id="4a204-129">Ruft zusätzliche Informationen für das angegebene Edge-/Datenfeld-Gatewaygerät im Datenfeld ab.</span><span class="sxs-lookup"><span data-stu-id="4a204-129">Gets additional information for the specified Data Box Edge/Data Box Gateway device</span></span>

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

### <span data-ttu-id="4a204-130">-Name</span><span class="sxs-lookup"><span data-stu-id="4a204-130">-Name</span></span>
<span data-ttu-id="4a204-131">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="4a204-131">Resource Group Name</span></span>

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

### <span data-ttu-id="4a204-132">-NetworkSetting</span><span class="sxs-lookup"><span data-stu-id="4a204-132">-NetworkSetting</span></span>
<span data-ttu-id="4a204-133">Ruft die Netzwerkeinstellungen des angegebenen Edge-/Datenfeld-Gatewaygeräts im Datenfeld ab.</span><span class="sxs-lookup"><span data-stu-id="4a204-133">Gets the network settings of the specified Data Box Edge/Data Box Gateway device</span></span>

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

### <span data-ttu-id="4a204-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a204-134">-ResourceGroupName</span></span>
<span data-ttu-id="4a204-135">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="4a204-135">Resource Group Name</span></span>

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

### <span data-ttu-id="4a204-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4a204-136">-ResourceId</span></span>
<span data-ttu-id="4a204-137">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="4a204-137">Azure ResourceId</span></span>

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

### <span data-ttu-id="4a204-138">-UpdateSummary</span><span class="sxs-lookup"><span data-stu-id="4a204-138">-UpdateSummary</span></span>
<span data-ttu-id="4a204-139">Ruft Informationen zur Verfügbarkeit von Updates basierend auf der letzten Überprüfung des Geräts ab.</span><span class="sxs-lookup"><span data-stu-id="4a204-139">Gets information about the availability of updates based on the last scan of the device.</span></span> <span data-ttu-id="4a204-140">Außerdem werden Informationen zu laufenden Download- oder Installationsaufträgen auf dem Gerät angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4a204-140">It also gets information about any ongoing download or install jobs on the device.</span></span>

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

### <span data-ttu-id="4a204-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a204-141">CommonParameters</span></span>
<span data-ttu-id="4a204-142">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a204-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a204-143">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4a204-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a204-144">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4a204-144">INPUTS</span></span>

### <span data-ttu-id="4a204-145">Keine</span><span class="sxs-lookup"><span data-stu-id="4a204-145">None</span></span>

## <span data-ttu-id="4a204-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4a204-146">OUTPUTS</span></span>

### <span data-ttu-id="4a204-147">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="4a204-147">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

### <span data-ttu-id="4a204-148">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeNetworkAdapter</span><span class="sxs-lookup"><span data-stu-id="4a204-148">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeNetworkAdapter</span></span>

### <span data-ttu-id="4a204-149">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDeviceExtendedInfo</span><span class="sxs-lookup"><span data-stu-id="4a204-149">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDeviceExtendedInfo</span></span>

### <span data-ttu-id="4a204-150">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUpdateSummary</span><span class="sxs-lookup"><span data-stu-id="4a204-150">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUpdateSummary</span></span>

### <span data-ttu-id="4a204-151">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeAlert</span><span class="sxs-lookup"><span data-stu-id="4a204-151">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeAlert</span></span>

## <span data-ttu-id="4a204-152">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4a204-152">NOTES</span></span>

## <span data-ttu-id="4a204-153">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4a204-153">RELATED LINKS</span></span>
