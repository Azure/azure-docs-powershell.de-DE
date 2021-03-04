---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/get-azstackedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeDevice.md
ms.openlocfilehash: dbc5e0bf327383adafa980d3475d196173fa0fdb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101948339"
---
# <span data-ttu-id="c1ba7-101">Get-AzStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="c1ba7-101">Get-AzStackEdgeDevice</span></span>

## <span data-ttu-id="c1ba7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1ba7-102">SYNOPSIS</span></span>
<span data-ttu-id="c1ba7-103">Ruft die Informationen auf verfügbaren Stack Edge-Geräten ab.</span><span class="sxs-lookup"><span data-stu-id="c1ba7-103">Gets the information on available Stack Edge devices.</span></span>

## <span data-ttu-id="c1ba7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c1ba7-104">SYNTAX</span></span>

### <span data-ttu-id="c1ba7-105">ListByParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c1ba7-105">ListByParameterSet (Default)</span></span>
```
Get-AzStackEdgeDevice [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c1ba7-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1ba7-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeDevice -ResourceId <String> [-ExtendedInfo] [-NetworkSetting] [-Alert] [-UpdateSummary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1ba7-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1ba7-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-ExtendedInfo] [-NetworkSetting] [-Alert]
 [-UpdateSummary] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1ba7-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c1ba7-108">DESCRIPTION</span></span>
<span data-ttu-id="c1ba7-109">Das **Get-AzStackEdgeDevice-Cmdlet** ruft die Informationen zu den verfügbaren Stack Edge-Geräten ab.</span><span class="sxs-lookup"><span data-stu-id="c1ba7-109">The **Get-AzStackEdgeDevice** cmdlet gets the information about the available Stack Edge Devices.</span></span> <span data-ttu-id="c1ba7-110">Sie können den Namen des Geräts zusammen mit dem Ressourcengruppennamen angeben, um die Informationen auf einem bestimmten Gerät zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c1ba7-110">You can specify the Name of the device along with the Resource Group Name to get the information on a specific device.</span></span> 

## <span data-ttu-id="c1ba7-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c1ba7-111">EXAMPLES</span></span>

### <span data-ttu-id="c1ba7-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c1ba7-112">Example 1</span></span>
```powershell
PS C:\>Get-AzStackEdgeDevice
Name               ResourceGroupName  Model   Location
----               -----------------  -----   --------
deviceNameOne      resourceGroupName1 Edge    eastus
deviceNameTwo      resourceGroupName2 Edge    westus
deviceNameThree    resourceGroupName3 Gateway eastus
```

### <span data-ttu-id="c1ba7-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="c1ba7-113">Example 2</span></span>
```powershell
PS C:\>$device = Get-AzStackEdgeDevice -ResourceGroupName resourceGroupName1 -DeviceName deviceNameOne -Alert -UpdateSummary -NetworkSetting -ExtendedInfo

PS C:\>$device.Alert

Title                            Severity AppearedDateTime      Recommendation
-----                            -------- ----------------      --------------
Lost heartbeat from your device. Critical 02-Jan-20 10:35:20 AM If your device is offline, then the device is not able to communicate with the Azure service. This could be due to one of the following reasons: <br/> &nbs�


PS C:\>$device.NetworkSetting

State    IPv4         IPv6                                 Subnet        Default Gateway Physical address DNS Servers
-----    ----         ----                                 ------        --------------- ---------------- -----------
Disabled 10.150.76.82 2404:f801:4800:1e:8168:dca6:b3b9:d70 255.255.252.0 10.150.76.1     00155D4E262B     10.50.50.50,10.50.10.50

PS C:\>$device.UpdateSummary

DeviceName        Current Version Friendly name      Last Software Scan Last Software Update Pending Updates Pending Update Titles
----------        --------------- -------------      ------------------ -------------------- --------------- ---------------------
deviceNameOne     2.0.998.537     Data Box Edge Mock                                         0

PS C:\>$device.ExtendedInfo

ResourceGroupName   DeviceName        EncryptedCIK Thumbprint     ResourceKey        EncryptedCIK
-----------------   ----------        -----------------------     -----------        ------------
resourceGroupName1  deviceNameOne     EncryptedCIKThumbpring      411182691329779166 EncryptedCIK
```

## <span data-ttu-id="c1ba7-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c1ba7-114">PARAMETERS</span></span>

### <span data-ttu-id="c1ba7-115">-Warnung</span><span class="sxs-lookup"><span data-stu-id="c1ba7-115">-Alert</span></span>
<span data-ttu-id="c1ba7-116">Abrufen der Benachrichtigungen auf dem Stack Edge/Gateway-Gerät</span><span class="sxs-lookup"><span data-stu-id="c1ba7-116">Fetch the alerts on the Stack edge/gateway device</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetByResourceIdParameterSet, GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1ba7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1ba7-117">-DefaultProfile</span></span>
<span data-ttu-id="c1ba7-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c1ba7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1ba7-119">-ExtendedInfo</span><span class="sxs-lookup"><span data-stu-id="c1ba7-119">-ExtendedInfo</span></span>
<span data-ttu-id="c1ba7-120">Ruft zusätzliche Informationen für das angegebene Stack Edge/Stack Gateway-Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="c1ba7-120">Gets additional information for the specified Stack Edge/Stack Gateway device</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetByResourceIdParameterSet, GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1ba7-121">-Name</span><span class="sxs-lookup"><span data-stu-id="c1ba7-121">-Name</span></span>
<span data-ttu-id="c1ba7-122">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="c1ba7-122">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: DeviceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1ba7-123">-NetworkSetting</span><span class="sxs-lookup"><span data-stu-id="c1ba7-123">-NetworkSetting</span></span>
<span data-ttu-id="c1ba7-124">Ruft die Netzwerkeinstellungen des angegebenen Stack Edge/Stack Gateway-Geräts ab.</span><span class="sxs-lookup"><span data-stu-id="c1ba7-124">Gets the network settings of the specified Stack Edge/Stack Gateway device</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetByResourceIdParameterSet, GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1ba7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1ba7-125">-ResourceGroupName</span></span>
<span data-ttu-id="c1ba7-126">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="c1ba7-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListByParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1ba7-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c1ba7-127">-ResourceId</span></span>
<span data-ttu-id="c1ba7-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="c1ba7-128">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1ba7-129">-UpdateSummary</span><span class="sxs-lookup"><span data-stu-id="c1ba7-129">-UpdateSummary</span></span>
<span data-ttu-id="c1ba7-130">Ruft Informationen zur Verfügbarkeit von Updates ab, die auf der letzten Überprüfung des Geräts basieren.</span><span class="sxs-lookup"><span data-stu-id="c1ba7-130">Gets information about the availability of updates based on the last scan of the device.</span></span> <span data-ttu-id="c1ba7-131">Außerdem werden Informationen zu laufenden Download- oder Installationsaufträgen auf dem Gerät angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c1ba7-131">It also gets information about any ongoing download or install jobs on the device.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetByResourceIdParameterSet, GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1ba7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1ba7-132">CommonParameters</span></span>
<span data-ttu-id="c1ba7-133">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1ba7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1ba7-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c1ba7-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1ba7-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c1ba7-135">INPUTS</span></span>

## <span data-ttu-id="c1ba7-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c1ba7-136">OUTPUTS</span></span>

## <span data-ttu-id="c1ba7-137">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c1ba7-137">NOTES</span></span>

## <span data-ttu-id="c1ba7-138">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c1ba7-138">RELATED LINKS</span></span>
