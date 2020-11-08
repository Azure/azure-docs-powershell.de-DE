---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModule.md
ms.openlocfilehash: ca2381ecff9822bac7a4613566e2da42e79cc5b7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003592"
---
# <span data-ttu-id="b147d-101">Get-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="b147d-101">Get-AzIotHubModule</span></span>

## <span data-ttu-id="b147d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b147d-102">SYNOPSIS</span></span>
<span data-ttu-id="b147d-103">Rufen Sie die Details eines viel Geräte Moduls oder Listen Moduls ab, das sich auf einem viel Gerät in einem viel Hub befindet.</span><span class="sxs-lookup"><span data-stu-id="b147d-103">Get the details of an IoT device module or list modules located on an IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="b147d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b147d-104">SYNTAX</span></span>

### <span data-ttu-id="b147d-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b147d-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubModule [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ModuleId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b147d-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b147d-106">InputObjectSet</span></span>
```
Get-AzIotHubModule [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b147d-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b147d-107">ResourceIdSet</span></span>
```
Get-AzIotHubModule [-ResourceId] <String> [-DeviceId] <String> [-ModuleId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b147d-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b147d-108">DESCRIPTION</span></span>
<span data-ttu-id="b147d-109">Rufen Sie die Details eines viel Geräte Moduls oder Listen Moduls ab, das sich auf einem viel Gerät in einem viel Hub befindet.</span><span class="sxs-lookup"><span data-stu-id="b147d-109">Get the details of an IoT device module or list modules located on an IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="b147d-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b147d-110">EXAMPLES</span></span>

### <span data-ttu-id="b147d-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b147d-111">Example 1</span></span>
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

<span data-ttu-id="b147d-112">Rufen Sie die Details eines viel Geräte Moduls in einem viel Hub ab.</span><span class="sxs-lookup"><span data-stu-id="b147d-112">Get the details of an IoT device module in an IoT Hub.</span></span>

### <span data-ttu-id="b147d-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="b147d-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" 

Module Id Device Id Connection State Authentication Last Activity Time
--------- --------- ---------------- -------------- ------------------
module1   myDevice1 Disconnected     Sas            1/1/0001 12:00:00 AM
module2   myDevice1 Disconnected     Sas            1/1/0001 12:00:00 AM
```

<span data-ttu-id="b147d-114">Alle Module anzeigen, die sich auf einem viel Gerät in einem viel Hub befinden.</span><span class="sxs-lookup"><span data-stu-id="b147d-114">Show all modules located on an IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="b147d-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="b147d-115">PARAMETERS</span></span>

### <span data-ttu-id="b147d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b147d-116">-DefaultProfile</span></span>
<span data-ttu-id="b147d-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b147d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b147d-118">-Geräte-Nr</span><span class="sxs-lookup"><span data-stu-id="b147d-118">-DeviceId</span></span>
<span data-ttu-id="b147d-119">Zielgeräte-ID.</span><span class="sxs-lookup"><span data-stu-id="b147d-119">Target Device Id.</span></span>

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

### <span data-ttu-id="b147d-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b147d-120">-InputObject</span></span>
<span data-ttu-id="b147d-121">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="b147d-121">IotHub object</span></span>

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

### <span data-ttu-id="b147d-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="b147d-122">-IotHubName</span></span>
<span data-ttu-id="b147d-123">Name des viel-Hubs</span><span class="sxs-lookup"><span data-stu-id="b147d-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="b147d-124">-Modul-Nr</span><span class="sxs-lookup"><span data-stu-id="b147d-124">-ModuleId</span></span>
<span data-ttu-id="b147d-125">Ziel Modul-ID.</span><span class="sxs-lookup"><span data-stu-id="b147d-125">Target Module Id.</span></span>

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

### <span data-ttu-id="b147d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b147d-126">-ResourceGroupName</span></span>
<span data-ttu-id="b147d-127">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="b147d-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="b147d-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="b147d-128">-ResourceId</span></span>
<span data-ttu-id="b147d-129">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="b147d-129">IotHub Resource Id</span></span>

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

### <span data-ttu-id="b147d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b147d-130">CommonParameters</span></span>
<span data-ttu-id="b147d-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b147d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b147d-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b147d-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b147d-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b147d-133">INPUTS</span></span>

### <span data-ttu-id="b147d-134">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="b147d-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="b147d-135">System. String</span><span class="sxs-lookup"><span data-stu-id="b147d-135">System.String</span></span>

## <span data-ttu-id="b147d-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b147d-136">OUTPUTS</span></span>

### <span data-ttu-id="b147d-137">Microsoft. Azure. Commands. Management. IotHub. Models. PSModule</span><span class="sxs-lookup"><span data-stu-id="b147d-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSModule</span></span>

### <span data-ttu-id="b147d-138">Microsoft. Azure. Commands. Management. IotHub. Models. PSModules []</span><span class="sxs-lookup"><span data-stu-id="b147d-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSModules[]</span></span>

## <span data-ttu-id="b147d-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="b147d-139">NOTES</span></span>

## <span data-ttu-id="b147d-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b147d-140">RELATED LINKS</span></span>
