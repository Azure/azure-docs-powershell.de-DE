---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/get-azdataboxedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeDevice.md
ms.openlocfilehash: f02cda5fe04ed72a5e6defd382c372b40c9c039b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942643"
---
# <span data-ttu-id="3e179-101">Get-AzDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="3e179-101">Get-AzDataBoxEdgeDevice</span></span>

## <span data-ttu-id="3e179-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e179-102">SYNOPSIS</span></span>
<span data-ttu-id="3e179-103">Ruft die Informationen auf verfügbaren Data Box Edge-Geräten ab.</span><span class="sxs-lookup"><span data-stu-id="3e179-103">Gets the information on available Data Box Edge devices.</span></span>

## <span data-ttu-id="3e179-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3e179-104">SYNTAX</span></span>

### <span data-ttu-id="3e179-105">ListByParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="3e179-105">ListByParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeDevice [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3e179-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e179-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e179-107">GetExtendedInfoByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e179-107">GetExtendedInfoByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-ExtendedInfo] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3e179-108">GetNetworkSettingByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e179-108">GetNetworkSettingByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-NetworkSetting] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3e179-109">GetSummaryUpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e179-109">GetSummaryUpdateByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-UpdateSummary] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3e179-110">GetAlertByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e179-110">GetAlertByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-Alert] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3e179-111">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e179-111">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e179-112">GetSummaryUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e179-112">GetSummaryUpdateParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-UpdateSummary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e179-113">GetNetworkSettingParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e179-113">GetNetworkSettingParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-NetworkSetting]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e179-114">GetExtendedInfoParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e179-114">GetExtendedInfoParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-ExtendedInfo]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e179-115">GetAlertParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e179-115">GetAlertParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-Alert]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e179-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3e179-116">DESCRIPTION</span></span>
<span data-ttu-id="3e179-117">Das **Get-AzDataBoxEdgeDevice-Cmdlet** ruft die Informationen zu den verfügbaren Data Box Edge-Geräten ab.</span><span class="sxs-lookup"><span data-stu-id="3e179-117">The **Get-AzDataBoxEdgeDevice** cmdlet gets the information about the available Data Box Edge Devices.</span></span> <span data-ttu-id="3e179-118">Sie können den Namen des Geräts zusammen mit dem Ressourcengruppennamen angeben, um die Informationen auf einem bestimmten Gerät zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="3e179-118">You can specify the Name of the device along with the Resource Group Name to get the information on a specific device.</span></span> 

## <span data-ttu-id="3e179-119">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3e179-119">EXAMPLES</span></span>

### <span data-ttu-id="3e179-120">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3e179-120">Example 1</span></span>
```powershell
PS C:\>Get-AzDataBoxEdgeDevice
Name               ResourceGroupName  Model   Location
----               -----------------  -----   --------
deviceNameOne      resourceGroupName1 Edge    eastus
deviceNameTwo      resourceGroupName2 Edge    westus
deviceNameThree    resourceGroupName3 Gateway eastus
```

### <span data-ttu-id="3e179-121">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="3e179-121">Example 2</span></span>
```powershell
PS C:\>Get-AzDataBoxEdgeDevice -ResourceId /subscriptions/subscriptionId/resourcegroups/resourceGroupName/providers/Microsoft.DataBoxEdge/dataBoxEdgeDevices/deviceName
Name            ResourceGroupName    Model   Location
----            -----------------    -----   --------
deviceName      resourceGroupName    Edge    eastus
```

### <span data-ttu-id="3e179-122">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="3e179-122">Example 3</span></span>
```powershell
PS C:\>Get-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -DeviceName deviceName
Name            ResourceGroupName    Model   Location
----            -----------------    -----   --------
deviceName      resourceGroupName    Edge    eastus
```

## <span data-ttu-id="3e179-123">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="3e179-123">PARAMETERS</span></span>

### <span data-ttu-id="3e179-124">-Warnung</span><span class="sxs-lookup"><span data-stu-id="3e179-124">-Alert</span></span>
<span data-ttu-id="3e179-125">Abrufen der Benachrichtigungen auf dem Edge-/Gatewaygerät des Datenfelds</span><span class="sxs-lookup"><span data-stu-id="3e179-125">Fetch the alerts on the data box edge/gateway device</span></span>

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

### <span data-ttu-id="3e179-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e179-126">-DefaultProfile</span></span>
<span data-ttu-id="3e179-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3e179-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e179-128">-ExtendedInfo</span><span class="sxs-lookup"><span data-stu-id="3e179-128">-ExtendedInfo</span></span>
<span data-ttu-id="3e179-129">Ruft zusätzliche Informationen für das angegebene Data Box Edge/Data Box Gateway-Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="3e179-129">Gets additional information for the specified Data Box Edge/Data Box Gateway device</span></span>

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

### <span data-ttu-id="3e179-130">-Name</span><span class="sxs-lookup"><span data-stu-id="3e179-130">-Name</span></span>
<span data-ttu-id="3e179-131">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="3e179-131">Resource Group Name</span></span>

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

### <span data-ttu-id="3e179-132">-NetworkSetting</span><span class="sxs-lookup"><span data-stu-id="3e179-132">-NetworkSetting</span></span>
<span data-ttu-id="3e179-133">Ruft die Netzwerkeinstellungen des angegebenen Data Box Edge/Data Box Gateway-Geräts ab.</span><span class="sxs-lookup"><span data-stu-id="3e179-133">Gets the network settings of the specified Data Box Edge/Data Box Gateway device</span></span>

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

### <span data-ttu-id="3e179-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e179-134">-ResourceGroupName</span></span>
<span data-ttu-id="3e179-135">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="3e179-135">Resource Group Name</span></span>

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

### <span data-ttu-id="3e179-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3e179-136">-ResourceId</span></span>
<span data-ttu-id="3e179-137">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="3e179-137">Azure ResourceId</span></span>

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

### <span data-ttu-id="3e179-138">-UpdateSummary</span><span class="sxs-lookup"><span data-stu-id="3e179-138">-UpdateSummary</span></span>
<span data-ttu-id="3e179-139">Ruft Informationen zur Verfügbarkeit von Updates ab, die auf der letzten Überprüfung des Geräts basieren.</span><span class="sxs-lookup"><span data-stu-id="3e179-139">Gets information about the availability of updates based on the last scan of the device.</span></span> <span data-ttu-id="3e179-140">Außerdem werden Informationen zu laufenden Download- oder Installationsaufträgen auf dem Gerät angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3e179-140">It also gets information about any ongoing download or install jobs on the device.</span></span>

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

### <span data-ttu-id="3e179-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e179-141">CommonParameters</span></span>
<span data-ttu-id="3e179-142">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e179-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e179-143">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3e179-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e179-144">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3e179-144">INPUTS</span></span>

### <span data-ttu-id="3e179-145">Keine</span><span class="sxs-lookup"><span data-stu-id="3e179-145">None</span></span>

## <span data-ttu-id="3e179-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3e179-146">OUTPUTS</span></span>

### <span data-ttu-id="3e179-147">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="3e179-147">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

### <span data-ttu-id="3e179-148">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeNetworkAdapter</span><span class="sxs-lookup"><span data-stu-id="3e179-148">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeNetworkAdapter</span></span>

### <span data-ttu-id="3e179-149">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDeviceExtendedInfo</span><span class="sxs-lookup"><span data-stu-id="3e179-149">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDeviceExtendedInfo</span></span>

### <span data-ttu-id="3e179-150">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUpdateSummary</span><span class="sxs-lookup"><span data-stu-id="3e179-150">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUpdateSummary</span></span>

### <span data-ttu-id="3e179-151">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeAlert</span><span class="sxs-lookup"><span data-stu-id="3e179-151">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeAlert</span></span>

## <span data-ttu-id="3e179-152">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="3e179-152">NOTES</span></span>

## <span data-ttu-id="3e179-153">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="3e179-153">RELATED LINKS</span></span>
