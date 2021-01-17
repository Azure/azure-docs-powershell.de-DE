---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdeviceconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceConnectionString.md
ms.openlocfilehash: 53887f7dc63ba849c9eac021f6f309497b512763
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472412"
---
# <span data-ttu-id="4ac36-101">Get-AzIotHubDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="4ac36-101">Get-AzIotHubDeviceConnectionString</span></span>

## <span data-ttu-id="4ac36-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ac36-102">SYNOPSIS</span></span>
<span data-ttu-id="4ac36-103">Holen Sie sich die Verbindungszeichenfolge eines Ziel-IoT-Geräts in einem Iot-Hub.</span><span class="sxs-lookup"><span data-stu-id="4ac36-103">Get the connection string of a target IoT device in an Iot Hub.</span></span>

## <span data-ttu-id="4ac36-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4ac36-104">SYNTAX</span></span>

### <span data-ttu-id="4ac36-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="4ac36-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceConnectionString [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>]
 [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4ac36-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4ac36-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceConnectionString [-InputObject] <PSIotHub> [-DeviceId <String>] [-KeyType <PSKeyType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4ac36-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="4ac36-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceConnectionString [-ResourceId] <String> [-DeviceId <String>] [-KeyType <PSKeyType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ac36-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4ac36-108">DESCRIPTION</span></span>
<span data-ttu-id="4ac36-109">Listen Sie die Verbindungszeichenfolge aller Geräte oder eines IoT-Zielgeräts auf, das in einem Azure IoT Hub enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="4ac36-109">List connection string of all devices or a target IoT device contained within an Azure IoT Hub.</span></span>

## <span data-ttu-id="4ac36-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4ac36-110">EXAMPLES</span></span>

### <span data-ttu-id="4ac36-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4ac36-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceConnectionString -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"

Device Id Connection String
--------- -----------------
device1   HostName=myiothub.azure-devices.net;DeviceId=device1;SharedAccessKey=/X4y******     
device2   HostName=myiothub.azure-devices.net;DeviceId=device2;x509=true
```

<span data-ttu-id="4ac36-112">Anzeigen aller Geräteverbindungszeichenfolgen in einem Iot-Hub.</span><span class="sxs-lookup"><span data-stu-id="4ac36-112">Show all devices connection string in an Iot Hub.</span></span>

### <span data-ttu-id="4ac36-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="4ac36-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubDCS -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "device1" -KeyType secondary

Device Id Connection String
--------- -----------------
device1   HostName=myiothub.azure-devices.net;DeviceId=device1;SharedAccessKey=/X4y******
```

<span data-ttu-id="4ac36-114">Holen Sie sich die sekundäre Verbindungszeichenfolge eines IoT-Geräts.</span><span class="sxs-lookup"><span data-stu-id="4ac36-114">Get the secondary connection string of an IoT device.</span></span>

## <span data-ttu-id="4ac36-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4ac36-115">PARAMETERS</span></span>

### <span data-ttu-id="4ac36-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ac36-116">-DefaultProfile</span></span>
<span data-ttu-id="4ac36-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4ac36-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ac36-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="4ac36-118">-DeviceId</span></span>
<span data-ttu-id="4ac36-119">Zielgerät-ID.</span><span class="sxs-lookup"><span data-stu-id="4ac36-119">Target Device Id.</span></span>

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

### <span data-ttu-id="4ac36-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4ac36-120">-InputObject</span></span>
<span data-ttu-id="4ac36-121">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="4ac36-121">IotHub object</span></span>

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

### <span data-ttu-id="4ac36-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="4ac36-122">-IotHubName</span></span>
<span data-ttu-id="4ac36-123">Name des Iot Hub</span><span class="sxs-lookup"><span data-stu-id="4ac36-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="4ac36-124">-KeyType</span><span class="sxs-lookup"><span data-stu-id="4ac36-124">-KeyType</span></span>
<span data-ttu-id="4ac36-125">Schlüsseltyp der Richtlinie für den freigegebenen Zugriff für die Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="4ac36-125">Shared access policy key type for auth.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSKeyType
Parameter Sets: (All)
Aliases:
Accepted values: primary, secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ac36-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ac36-126">-ResourceGroupName</span></span>
<span data-ttu-id="4ac36-127">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="4ac36-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="4ac36-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4ac36-128">-ResourceId</span></span>
<span data-ttu-id="4ac36-129">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="4ac36-129">IotHub Resource Id</span></span>

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

### <span data-ttu-id="4ac36-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ac36-130">CommonParameters</span></span>
<span data-ttu-id="4ac36-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ac36-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ac36-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ac36-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ac36-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4ac36-133">INPUTS</span></span>

### <span data-ttu-id="4ac36-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="4ac36-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="4ac36-135">System.String</span><span class="sxs-lookup"><span data-stu-id="4ac36-135">System.String</span></span>

## <span data-ttu-id="4ac36-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4ac36-136">OUTPUTS</span></span>

### <span data-ttu-id="4ac36-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="4ac36-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceConnectionString</span></span>

## <span data-ttu-id="4ac36-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4ac36-138">NOTES</span></span>

## <span data-ttu-id="4ac36-139">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4ac36-139">RELATED LINKS</span></span>
