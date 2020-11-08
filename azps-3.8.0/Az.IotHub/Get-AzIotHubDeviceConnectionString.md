---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdeviceconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceConnectionString.md
ms.openlocfilehash: 53887f7dc63ba849c9eac021f6f309497b512763
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003206"
---
# <span data-ttu-id="b028c-101">Get-AzIotHubDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="b028c-101">Get-AzIotHubDeviceConnectionString</span></span>

## <span data-ttu-id="b028c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b028c-102">SYNOPSIS</span></span>
<span data-ttu-id="b028c-103">Rufen Sie die Verbindungszeichenfolge eines Ziel-viel-Geräts in einem viel Hub ab.</span><span class="sxs-lookup"><span data-stu-id="b028c-103">Get the connection string of a target IoT device in an Iot Hub.</span></span>

## <span data-ttu-id="b028c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b028c-104">SYNTAX</span></span>

### <span data-ttu-id="b028c-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b028c-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceConnectionString [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>]
 [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b028c-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b028c-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceConnectionString [-InputObject] <PSIotHub> [-DeviceId <String>] [-KeyType <PSKeyType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b028c-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b028c-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceConnectionString [-ResourceId] <String> [-DeviceId <String>] [-KeyType <PSKeyType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b028c-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b028c-108">DESCRIPTION</span></span>
<span data-ttu-id="b028c-109">Auflisten der Verbindungszeichenfolge aller Geräte oder eines Ziel-viel-Geräts, das sich in einem Azure-viel-Hub befindet</span><span class="sxs-lookup"><span data-stu-id="b028c-109">List connection string of all devices or a target IoT device contained within an Azure IoT Hub.</span></span>

## <span data-ttu-id="b028c-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b028c-110">EXAMPLES</span></span>

### <span data-ttu-id="b028c-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b028c-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceConnectionString -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"

Device Id Connection String
--------- -----------------
device1   HostName=myiothub.azure-devices.net;DeviceId=device1;SharedAccessKey=/X4y******     
device2   HostName=myiothub.azure-devices.net;DeviceId=device2;x509=true
```

<span data-ttu-id="b028c-112">Alle Geräte-Verbindungszeichenfolge in einem viel Hub anzeigen.</span><span class="sxs-lookup"><span data-stu-id="b028c-112">Show all devices connection string in an Iot Hub.</span></span>

### <span data-ttu-id="b028c-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="b028c-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubDCS -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "device1" -KeyType secondary

Device Id Connection String
--------- -----------------
device1   HostName=myiothub.azure-devices.net;DeviceId=device1;SharedAccessKey=/X4y******
```

<span data-ttu-id="b028c-114">Rufen Sie die sekundäre Verbindungszeichenfolge eines viel-Geräts ab.</span><span class="sxs-lookup"><span data-stu-id="b028c-114">Get the secondary connection string of an IoT device.</span></span>

## <span data-ttu-id="b028c-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="b028c-115">PARAMETERS</span></span>

### <span data-ttu-id="b028c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b028c-116">-DefaultProfile</span></span>
<span data-ttu-id="b028c-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b028c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b028c-118">-Geräte-Nr</span><span class="sxs-lookup"><span data-stu-id="b028c-118">-DeviceId</span></span>
<span data-ttu-id="b028c-119">Zielgeräte-ID.</span><span class="sxs-lookup"><span data-stu-id="b028c-119">Target Device Id.</span></span>

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

### <span data-ttu-id="b028c-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b028c-120">-InputObject</span></span>
<span data-ttu-id="b028c-121">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="b028c-121">IotHub object</span></span>

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

### <span data-ttu-id="b028c-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="b028c-122">-IotHubName</span></span>
<span data-ttu-id="b028c-123">Name des viel-Hubs</span><span class="sxs-lookup"><span data-stu-id="b028c-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="b028c-124">-KeyType</span><span class="sxs-lookup"><span data-stu-id="b028c-124">-KeyType</span></span>
<span data-ttu-id="b028c-125">Gemeinsamer Zugriffsrichtlinien Schlüsseltyp für auth.</span><span class="sxs-lookup"><span data-stu-id="b028c-125">Shared access policy key type for auth.</span></span>

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

### <span data-ttu-id="b028c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b028c-126">-ResourceGroupName</span></span>
<span data-ttu-id="b028c-127">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="b028c-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="b028c-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="b028c-128">-ResourceId</span></span>
<span data-ttu-id="b028c-129">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="b028c-129">IotHub Resource Id</span></span>

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

### <span data-ttu-id="b028c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b028c-130">CommonParameters</span></span>
<span data-ttu-id="b028c-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b028c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b028c-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b028c-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b028c-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b028c-133">INPUTS</span></span>

### <span data-ttu-id="b028c-134">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="b028c-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="b028c-135">System. String</span><span class="sxs-lookup"><span data-stu-id="b028c-135">System.String</span></span>

## <span data-ttu-id="b028c-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b028c-136">OUTPUTS</span></span>

### <span data-ttu-id="b028c-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="b028c-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceConnectionString</span></span>

## <span data-ttu-id="b028c-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="b028c-138">NOTES</span></span>

## <span data-ttu-id="b028c-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b028c-139">RELATED LINKS</span></span>
