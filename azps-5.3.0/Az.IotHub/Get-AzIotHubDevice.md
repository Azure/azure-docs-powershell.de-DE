---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDevice.md
ms.openlocfilehash: 792992208f4862a0b818aeb890c34cfa361242ca
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472413"
---
# <span data-ttu-id="e2dbe-101">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="e2dbe-101">Get-AzIotHubDevice</span></span>

## <span data-ttu-id="e2dbe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2dbe-102">SYNOPSIS</span></span>
<span data-ttu-id="e2dbe-103">Listet alle Geräte oder ein bestimmtes Gerät auf, die in einem Azure IoT Hub enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="e2dbe-103">Lists all devices or a particular device contained within an Azure IoT Hub.</span></span> 

## <span data-ttu-id="e2dbe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e2dbe-104">SYNTAX</span></span>

### <span data-ttu-id="e2dbe-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e2dbe-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e2dbe-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e2dbe-106">InputObjectSet</span></span>
```
Get-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e2dbe-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="e2dbe-107">ResourceIdSet</span></span>
```
Get-AzIotHubDevice [-ResourceId] <String> [-DeviceId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e2dbe-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e2dbe-108">DESCRIPTION</span></span>
<span data-ttu-id="e2dbe-109">Erfahren Sie mehr über die Details eines Iot Hub-Geräts, oder listen Sie alle Geräte in einem Iot Hub auf.</span><span class="sxs-lookup"><span data-stu-id="e2dbe-109">Get the details of an Iot Hub device or list all devices in an Iot Hub.</span></span>

## <span data-ttu-id="e2dbe-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e2dbe-110">EXAMPLES</span></span>

### <span data-ttu-id="e2dbe-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e2dbe-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"

Device Id Status   Connection State Authentication       Edge Enabled Last Activity Time
--------- ------   ---------------- --------------       ------------ ------------------
device1   Enabled  Disconnected     CertificateAuthority True         1/1/0001 12:00:00 AM
device2   Disabled Disconnected     Sas                  False        1/1/0001 12:00:00 AM
device3   Enabled  Disconnected     SelfSigned           False        1/1/0001 12:00:00 AM
```

<span data-ttu-id="e2dbe-112">Zeigen Sie alle Geräte in einem Iot Hub an.</span><span class="sxs-lookup"><span data-stu-id="e2dbe-112">Show all devices in an Iot Hub.</span></span>

### <span data-ttu-id="e2dbe-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="e2dbe-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"

DeviceId                   : myDevice1
GenerationId               : 637148941292917073
ETag                       : "NzIyMDI4MTk3"
LastActivityTime           : 1/1/0001 12:00:00 AM
ConnectionState            : Disconnected
ConnectionStateUpdatedTime : 1/1/0001 12:00:00 AM
Status                     : Disabled
StatusReason               : Reason1
StatusUpdatedTime          : 1/17/2020 10:15:04 PM
CloudToDeviceMessageCount  : 0
Authentication             : Sas
EdgeEnabled                : False
DeviceScope                :
```

<span data-ttu-id="e2dbe-114">Erfahren Sie mehr über die Details eines IoT Hub-Geräts.</span><span class="sxs-lookup"><span data-stu-id="e2dbe-114">Get the details of an IoT Hub device.</span></span>

## <span data-ttu-id="e2dbe-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e2dbe-115">PARAMETERS</span></span>

### <span data-ttu-id="e2dbe-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2dbe-116">-DefaultProfile</span></span>
<span data-ttu-id="e2dbe-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e2dbe-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2dbe-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="e2dbe-118">-DeviceId</span></span>
<span data-ttu-id="e2dbe-119">Zielgerät-ID.</span><span class="sxs-lookup"><span data-stu-id="e2dbe-119">Target Device Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2dbe-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e2dbe-120">-InputObject</span></span>
<span data-ttu-id="e2dbe-121">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="e2dbe-121">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2dbe-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="e2dbe-122">-IotHubName</span></span>
<span data-ttu-id="e2dbe-123">Name des Iot Hub</span><span class="sxs-lookup"><span data-stu-id="e2dbe-123">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2dbe-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2dbe-124">-ResourceGroupName</span></span>
<span data-ttu-id="e2dbe-125">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="e2dbe-125">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2dbe-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e2dbe-126">-ResourceId</span></span>
<span data-ttu-id="e2dbe-127">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="e2dbe-127">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2dbe-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2dbe-128">CommonParameters</span></span>
<span data-ttu-id="e2dbe-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2dbe-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2dbe-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2dbe-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2dbe-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e2dbe-131">INPUTS</span></span>

### <span data-ttu-id="e2dbe-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="e2dbe-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="e2dbe-133">System.String</span><span class="sxs-lookup"><span data-stu-id="e2dbe-133">System.String</span></span>

## <span data-ttu-id="e2dbe-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e2dbe-134">OUTPUTS</span></span>

### <span data-ttu-id="e2dbe-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSDEntfernung</span><span class="sxs-lookup"><span data-stu-id="e2dbe-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

### <span data-ttu-id="e2dbe-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDEntfernung[]</span><span class="sxs-lookup"><span data-stu-id="e2dbe-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevices[]</span></span>

## <span data-ttu-id="e2dbe-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e2dbe-137">NOTES</span></span>

## <span data-ttu-id="e2dbe-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e2dbe-138">RELATED LINKS</span></span>
