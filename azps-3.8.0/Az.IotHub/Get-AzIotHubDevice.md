---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDevice.md
ms.openlocfilehash: 792992208f4862a0b818aeb890c34cfa361242ca
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996599"
---
# <span data-ttu-id="4f055-101">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="4f055-101">Get-AzIotHubDevice</span></span>

## <span data-ttu-id="4f055-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4f055-102">SYNOPSIS</span></span>
<span data-ttu-id="4f055-103">Listet alle Geräte oder ein bestimmtes Gerät auf, die in einem Azure-viel-Hub enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="4f055-103">Lists all devices or a particular device contained within an Azure IoT Hub.</span></span> 

## <span data-ttu-id="4f055-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4f055-104">SYNTAX</span></span>

### <span data-ttu-id="4f055-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="4f055-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4f055-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4f055-106">InputObjectSet</span></span>
```
Get-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4f055-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="4f055-107">ResourceIdSet</span></span>
```
Get-AzIotHubDevice [-ResourceId] <String> [-DeviceId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4f055-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4f055-108">DESCRIPTION</span></span>
<span data-ttu-id="4f055-109">Rufen Sie die Details eines viel Hub-Geräts ab, oder Listen Sie alle Geräte in einem viel Hub auf.</span><span class="sxs-lookup"><span data-stu-id="4f055-109">Get the details of an Iot Hub device or list all devices in an Iot Hub.</span></span>

## <span data-ttu-id="4f055-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4f055-110">EXAMPLES</span></span>

### <span data-ttu-id="4f055-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4f055-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"

Device Id Status   Connection State Authentication       Edge Enabled Last Activity Time
--------- ------   ---------------- --------------       ------------ ------------------
device1   Enabled  Disconnected     CertificateAuthority True         1/1/0001 12:00:00 AM
device2   Disabled Disconnected     Sas                  False        1/1/0001 12:00:00 AM
device3   Enabled  Disconnected     SelfSigned           False        1/1/0001 12:00:00 AM
```

<span data-ttu-id="4f055-112">Alle Geräte in einem viel Hub anzeigen</span><span class="sxs-lookup"><span data-stu-id="4f055-112">Show all devices in an Iot Hub.</span></span>

### <span data-ttu-id="4f055-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="4f055-113">Example 2</span></span>
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

<span data-ttu-id="4f055-114">Rufen Sie die Details eines viel Hub-Geräts ab.</span><span class="sxs-lookup"><span data-stu-id="4f055-114">Get the details of an IoT Hub device.</span></span>

## <span data-ttu-id="4f055-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="4f055-115">PARAMETERS</span></span>

### <span data-ttu-id="4f055-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f055-116">-DefaultProfile</span></span>
<span data-ttu-id="4f055-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4f055-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f055-118">-Geräte-Nr</span><span class="sxs-lookup"><span data-stu-id="4f055-118">-DeviceId</span></span>
<span data-ttu-id="4f055-119">Zielgeräte-ID.</span><span class="sxs-lookup"><span data-stu-id="4f055-119">Target Device Id.</span></span>

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

### <span data-ttu-id="4f055-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4f055-120">-InputObject</span></span>
<span data-ttu-id="4f055-121">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="4f055-121">IotHub object</span></span>

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

### <span data-ttu-id="4f055-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="4f055-122">-IotHubName</span></span>
<span data-ttu-id="4f055-123">Name des viel-Hubs</span><span class="sxs-lookup"><span data-stu-id="4f055-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="4f055-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f055-124">-ResourceGroupName</span></span>
<span data-ttu-id="4f055-125">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="4f055-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="4f055-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="4f055-126">-ResourceId</span></span>
<span data-ttu-id="4f055-127">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="4f055-127">IotHub Resource Id</span></span>

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

### <span data-ttu-id="4f055-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f055-128">CommonParameters</span></span>
<span data-ttu-id="4f055-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f055-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f055-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f055-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f055-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4f055-131">INPUTS</span></span>

### <span data-ttu-id="4f055-132">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="4f055-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="4f055-133">System. String</span><span class="sxs-lookup"><span data-stu-id="4f055-133">System.String</span></span>

## <span data-ttu-id="4f055-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4f055-134">OUTPUTS</span></span>

### <span data-ttu-id="4f055-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span><span class="sxs-lookup"><span data-stu-id="4f055-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

### <span data-ttu-id="4f055-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDe []</span><span class="sxs-lookup"><span data-stu-id="4f055-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevices[]</span></span>

## <span data-ttu-id="4f055-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="4f055-137">NOTES</span></span>

## <span data-ttu-id="4f055-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4f055-138">RELATED LINKS</span></span>
