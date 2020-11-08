---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdevicetwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceTwin.md
ms.openlocfilehash: 6d8397ff8b22895614c67592460eadf76aa3fb92
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166670"
---
# <span data-ttu-id="68a75-101">Get-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="68a75-101">Get-AzIotHubDeviceTwin</span></span>

## <span data-ttu-id="68a75-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="68a75-102">SYNOPSIS</span></span>
<span data-ttu-id="68a75-103">Ruft ein Gerät Twin ab.</span><span class="sxs-lookup"><span data-stu-id="68a75-103">Gets a device twin.</span></span>

## <span data-ttu-id="68a75-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="68a75-104">SYNTAX</span></span>

### <span data-ttu-id="68a75-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="68a75-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68a75-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="68a75-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceTwin [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68a75-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="68a75-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceTwin [-ResourceId] <String> [-DeviceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="68a75-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="68a75-108">DESCRIPTION</span></span>
<span data-ttu-id="68a75-109">Ruft ein Gerät Twin ab.</span><span class="sxs-lookup"><span data-stu-id="68a75-109">Gets a device twin.</span></span> <span data-ttu-id="68a75-110">Weitere Informationen finden Sie unter https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins .</span><span class="sxs-lookup"><span data-stu-id="68a75-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins for more information.</span></span>

## <span data-ttu-id="68a75-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="68a75-111">EXAMPLES</span></span>

### <span data-ttu-id="68a75-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="68a75-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"
```

<span data-ttu-id="68a75-113">Gibt das Twin-Objekt des Geräts zurück.</span><span class="sxs-lookup"><span data-stu-id="68a75-113">Returns the device twin object.</span></span>

## <span data-ttu-id="68a75-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="68a75-114">PARAMETERS</span></span>

### <span data-ttu-id="68a75-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68a75-115">-DefaultProfile</span></span>
<span data-ttu-id="68a75-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="68a75-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68a75-117">-Geräte-Nr</span><span class="sxs-lookup"><span data-stu-id="68a75-117">-DeviceId</span></span>
<span data-ttu-id="68a75-118">Zielgeräte-ID.</span><span class="sxs-lookup"><span data-stu-id="68a75-118">Target Device Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68a75-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="68a75-119">-InputObject</span></span>
<span data-ttu-id="68a75-120">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="68a75-120">IotHub object</span></span>

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

### <span data-ttu-id="68a75-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="68a75-121">-IotHubName</span></span>
<span data-ttu-id="68a75-122">Name des viel-Hubs</span><span class="sxs-lookup"><span data-stu-id="68a75-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="68a75-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68a75-123">-ResourceGroupName</span></span>
<span data-ttu-id="68a75-124">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="68a75-124">Name of the Resource Group</span></span>

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

### <span data-ttu-id="68a75-125">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="68a75-125">-ResourceId</span></span>
<span data-ttu-id="68a75-126">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="68a75-126">IotHub Resource Id</span></span>

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

### <span data-ttu-id="68a75-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68a75-127">CommonParameters</span></span>
<span data-ttu-id="68a75-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68a75-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68a75-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68a75-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68a75-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="68a75-130">INPUTS</span></span>

### <span data-ttu-id="68a75-131">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="68a75-131">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="68a75-132">System. String</span><span class="sxs-lookup"><span data-stu-id="68a75-132">System.String</span></span>

## <span data-ttu-id="68a75-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="68a75-133">OUTPUTS</span></span>

### <span data-ttu-id="68a75-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="68a75-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTwin</span></span>

## <span data-ttu-id="68a75-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="68a75-135">NOTES</span></span>

## <span data-ttu-id="68a75-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="68a75-136">RELATED LINKS</span></span>
