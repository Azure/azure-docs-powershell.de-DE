---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/invoke-aziothubquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubQuery.md
ms.openlocfilehash: 955e09ab17644009f281223581ae2f5f45adfb33
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918936"
---
# <span data-ttu-id="c734b-101">Invoke-AzIotHubQuery</span><span class="sxs-lookup"><span data-stu-id="c734b-101">Invoke-AzIotHubQuery</span></span>

## <span data-ttu-id="c734b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c734b-102">SYNOPSIS</span></span>
<span data-ttu-id="c734b-103">Abfragen eines IoT-Hubs mit einer leistungsfähigen SQL sprache.</span><span class="sxs-lookup"><span data-stu-id="c734b-103">Query an IoT Hub using a powerful SQL-like language.</span></span>

## <span data-ttu-id="c734b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c734b-104">SYNTAX</span></span>

### <span data-ttu-id="c734b-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c734b-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubQuery [-ResourceGroupName] <String> [-IotHubName] <String> [-Query] <String> [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c734b-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c734b-106">InputObjectSet</span></span>
```
Invoke-AzIotHubQuery [-InputObject] <PSIotHub> [-Query] <String> [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c734b-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c734b-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubQuery [-ResourceId] <String> [-Query] <String> [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c734b-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c734b-108">DESCRIPTION</span></span>
<span data-ttu-id="c734b-109">Abfragen eines IoT Hubs mithilfe einer leistungsfähigen SQL-igen Sprache, um Informationen zu Geräte- und Modulzungen, Aufträgen und Nachrichtenrouting abzurufen.</span><span class="sxs-lookup"><span data-stu-id="c734b-109">Query an IoT Hub using a powerful SQL-like language to retrieve information regarding device and module twins, jobs and message routing.</span></span>
<span data-ttu-id="c734b-110">Weitere https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-query-language Informationen finden Sie unter.</span><span class="sxs-lookup"><span data-stu-id="c734b-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-query-language for more information.</span></span>

## <span data-ttu-id="c734b-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c734b-111">EXAMPLES</span></span>

### <span data-ttu-id="c734b-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c734b-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Query "select * from devices"
```

<span data-ttu-id="c734b-113">Abfragen aller Gerätezungsdaten in einem Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="c734b-113">Query all device twin data in an Azure IoT Hub.</span></span>

### <span data-ttu-id="c734b-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="c734b-114">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Query "select * from devices.modules where devices.deviceId = 'myDevice1'" -Top 2
```

<span data-ttu-id="c734b-115">Abfrage der top 2-Modul-Doppeldaten auf einem Zielgerät.</span><span class="sxs-lookup"><span data-stu-id="c734b-115">Query top 2 module twin data on a target device.</span></span>

## <span data-ttu-id="c734b-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c734b-116">PARAMETERS</span></span>

### <span data-ttu-id="c734b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c734b-117">-DefaultProfile</span></span>
<span data-ttu-id="c734b-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c734b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c734b-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c734b-119">-InputObject</span></span>
<span data-ttu-id="c734b-120">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="c734b-120">IotHub object</span></span>

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

### <span data-ttu-id="c734b-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="c734b-121">-IotHubName</span></span>
<span data-ttu-id="c734b-122">Name des Iot-Hubs</span><span class="sxs-lookup"><span data-stu-id="c734b-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="c734b-123">-Query</span><span class="sxs-lookup"><span data-stu-id="c734b-123">-Query</span></span>
<span data-ttu-id="c734b-124">Benutzerabfrage, die ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c734b-124">User query to be executed.</span></span>

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

### <span data-ttu-id="c734b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c734b-125">-ResourceGroupName</span></span>
<span data-ttu-id="c734b-126">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="c734b-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="c734b-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c734b-127">-ResourceId</span></span>
<span data-ttu-id="c734b-128">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="c734b-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="c734b-129">-Top</span><span class="sxs-lookup"><span data-stu-id="c734b-129">-Top</span></span>
<span data-ttu-id="c734b-130">Maximale Anzahl der zurückzukehrenden Elemente.</span><span class="sxs-lookup"><span data-stu-id="c734b-130">Maximum number of elements to return.</span></span>
<span data-ttu-id="c734b-131">Standardmäßig verfügt die Abfrage über keine Obergrenze.</span><span class="sxs-lookup"><span data-stu-id="c734b-131">By default query has no cap.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c734b-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c734b-132">-Confirm</span></span>
<span data-ttu-id="c734b-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c734b-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c734b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c734b-134">-WhatIf</span></span>
<span data-ttu-id="c734b-135">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c734b-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c734b-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c734b-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c734b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c734b-137">CommonParameters</span></span>
<span data-ttu-id="c734b-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c734b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c734b-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c734b-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c734b-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c734b-140">INPUTS</span></span>

### <span data-ttu-id="c734b-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="c734b-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="c734b-142">System.String</span><span class="sxs-lookup"><span data-stu-id="c734b-142">System.String</span></span>

## <span data-ttu-id="c734b-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c734b-143">OUTPUTS</span></span>

### <span data-ttu-id="c734b-144">System.String</span><span class="sxs-lookup"><span data-stu-id="c734b-144">System.String</span></span>

## <span data-ttu-id="c734b-145">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c734b-145">NOTES</span></span>

## <span data-ttu-id="c734b-146">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c734b-146">RELATED LINKS</span></span>
