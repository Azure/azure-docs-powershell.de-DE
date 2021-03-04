---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModule.md
ms.openlocfilehash: c2515ff590543c448985f0c6635278430d8ae63e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936848"
---
# <span data-ttu-id="c14d7-101">Get-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="c14d7-101">Get-AzIotHubModule</span></span>

## <span data-ttu-id="c14d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c14d7-102">SYNOPSIS</span></span>
<span data-ttu-id="c14d7-103">Hier erhalten Sie die Details eines IoT-Gerätemoduls oder listenmoduls, das sich auf einem IoT-Gerät in einem IoT Hub befindet.</span><span class="sxs-lookup"><span data-stu-id="c14d7-103">Get the details of an IoT device module or list modules located on an IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="c14d7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c14d7-104">SYNTAX</span></span>

### <span data-ttu-id="c14d7-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c14d7-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubModule [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ModuleId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c14d7-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c14d7-106">InputObjectSet</span></span>
```
Get-AzIotHubModule [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c14d7-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c14d7-107">ResourceIdSet</span></span>
```
Get-AzIotHubModule [-ResourceId] <String> [-DeviceId] <String> [-ModuleId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c14d7-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c14d7-108">DESCRIPTION</span></span>
<span data-ttu-id="c14d7-109">Hier erhalten Sie die Details eines IoT-Gerätemoduls oder listenmoduls, das sich auf einem IoT-Gerät in einem IoT Hub befindet.</span><span class="sxs-lookup"><span data-stu-id="c14d7-109">Get the details of an IoT device module or list modules located on an IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="c14d7-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c14d7-110">EXAMPLES</span></span>

### <span data-ttu-id="c14d7-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c14d7-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1"

ModuleId                   : myModule1
DeviceId                   : myDevice1
GenerationId               : 637148941292917073
ETag                       : "NzIyMDI4MTk3"
LastActivityTime           : 1/1/0001 12:00:00 AM
ConnectionState            : Disconnected
ConnectionStateUpdatedTime : 1/1/0001 12:00:00 AM
CloudToDeviceMessageCount  : 0
Authentication             : Sas
ManagedBy                  :
```

<span data-ttu-id="c14d7-112">Hier erhalten Sie die Details eines IoT-Gerätemoduls in einem IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="c14d7-112">Get the details of an IoT device module in an IoT Hub.</span></span>

### <span data-ttu-id="c14d7-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="c14d7-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" 

Module Id Device Id Connection State Authentication Last Activity Time
--------- --------- ---------------- -------------- ------------------
module1   myDevice1 Disconnected     Sas            1/1/0001 12:00:00 AM
module2   myDevice1 Disconnected     Sas            1/1/0001 12:00:00 AM
```

<span data-ttu-id="c14d7-114">Alle Module anzeigen, die sich auf einem IoT-Gerät in einem IoT Hub befinden.</span><span class="sxs-lookup"><span data-stu-id="c14d7-114">Show all modules located on an IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="c14d7-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c14d7-115">PARAMETERS</span></span>

### <span data-ttu-id="c14d7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c14d7-116">-DefaultProfile</span></span>
<span data-ttu-id="c14d7-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c14d7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c14d7-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="c14d7-118">-DeviceId</span></span>
<span data-ttu-id="c14d7-119">Zielgerät-ID.</span><span class="sxs-lookup"><span data-stu-id="c14d7-119">Target Device Id.</span></span>

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

### <span data-ttu-id="c14d7-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c14d7-120">-InputObject</span></span>
<span data-ttu-id="c14d7-121">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="c14d7-121">IotHub object</span></span>

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

### <span data-ttu-id="c14d7-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="c14d7-122">-IotHubName</span></span>
<span data-ttu-id="c14d7-123">Name des Iot-Hubs</span><span class="sxs-lookup"><span data-stu-id="c14d7-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="c14d7-124">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="c14d7-124">-ModuleId</span></span>
<span data-ttu-id="c14d7-125">Zielmodul-ID.</span><span class="sxs-lookup"><span data-stu-id="c14d7-125">Target Module Id.</span></span>

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

### <span data-ttu-id="c14d7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c14d7-126">-ResourceGroupName</span></span>
<span data-ttu-id="c14d7-127">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="c14d7-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="c14d7-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c14d7-128">-ResourceId</span></span>
<span data-ttu-id="c14d7-129">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="c14d7-129">IotHub Resource Id</span></span>

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

### <span data-ttu-id="c14d7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c14d7-130">CommonParameters</span></span>
<span data-ttu-id="c14d7-131">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c14d7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c14d7-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c14d7-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c14d7-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c14d7-133">INPUTS</span></span>

### <span data-ttu-id="c14d7-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="c14d7-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="c14d7-135">System.String</span><span class="sxs-lookup"><span data-stu-id="c14d7-135">System.String</span></span>

## <span data-ttu-id="c14d7-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c14d7-136">OUTPUTS</span></span>

### <span data-ttu-id="c14d7-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSModule</span><span class="sxs-lookup"><span data-stu-id="c14d7-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSModule</span></span>

### <span data-ttu-id="c14d7-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSModules[]</span><span class="sxs-lookup"><span data-stu-id="c14d7-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSModules[]</span></span>

## <span data-ttu-id="c14d7-139">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c14d7-139">NOTES</span></span>

## <span data-ttu-id="c14d7-140">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c14d7-140">RELATED LINKS</span></span>
