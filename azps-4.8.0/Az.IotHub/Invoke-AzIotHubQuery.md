---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubQuery.md
ms.openlocfilehash: 6445e6281ff69f4eef54a5694f953beaa08ad098
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94175123"
---
# <span data-ttu-id="23baa-101">Invoke-AzIotHubQuery</span><span class="sxs-lookup"><span data-stu-id="23baa-101">Invoke-AzIotHubQuery</span></span>

## <span data-ttu-id="23baa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="23baa-102">SYNOPSIS</span></span>
<span data-ttu-id="23baa-103">Abfragen eines vielseitigen Hubs mithilfe einer leistungsfähigen SQL-ähnlichen Sprache.</span><span class="sxs-lookup"><span data-stu-id="23baa-103">Query an IoT Hub using a powerful SQL-like language.</span></span>

## <span data-ttu-id="23baa-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="23baa-104">SYNTAX</span></span>

### <span data-ttu-id="23baa-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="23baa-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubQuery [-ResourceGroupName] <String> [-IotHubName] <String> [-Query] <String> [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23baa-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="23baa-106">InputObjectSet</span></span>
```
Invoke-AzIotHubQuery [-InputObject] <PSIotHub> [-Query] <String> [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23baa-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="23baa-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubQuery [-ResourceId] <String> [-Query] <String> [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23baa-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="23baa-108">DESCRIPTION</span></span>
<span data-ttu-id="23baa-109">Abfragen eines großen Hubs mithilfe einer leistungsfähigen SQL-ähnlichen Sprache, um Informationen zu Geräte-und Modul Zwillingen, Aufträgen und dem Nachrichtenrouting abzurufen.</span><span class="sxs-lookup"><span data-stu-id="23baa-109">Query an IoT Hub using a powerful SQL-like language to retrieve information regarding device and module twins, jobs and message routing.</span></span>
<span data-ttu-id="23baa-110">Weitere Informationen finden Sie unter https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-query-language .</span><span class="sxs-lookup"><span data-stu-id="23baa-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-query-language for more information.</span></span>

## <span data-ttu-id="23baa-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="23baa-111">EXAMPLES</span></span>

### <span data-ttu-id="23baa-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="23baa-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Query "select * from devices"
```

<span data-ttu-id="23baa-113">Abfragen aller Geräte Zwillings Daten in einem Azure-viel-Hub</span><span class="sxs-lookup"><span data-stu-id="23baa-113">Query all device twin data in an Azure IoT Hub.</span></span>

### <span data-ttu-id="23baa-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="23baa-114">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Query "select * from devices.modules where devices.deviceId = 'myDevice1'" -Top 2
```

<span data-ttu-id="23baa-115">Abfrage der obersten zwei Modul Daten auf einem Zielgerät</span><span class="sxs-lookup"><span data-stu-id="23baa-115">Query top 2 module twin data on a target device.</span></span>

## <span data-ttu-id="23baa-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="23baa-116">PARAMETERS</span></span>

### <span data-ttu-id="23baa-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23baa-117">-DefaultProfile</span></span>
<span data-ttu-id="23baa-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="23baa-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23baa-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="23baa-119">-InputObject</span></span>
<span data-ttu-id="23baa-120">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="23baa-120">IotHub object</span></span>

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

### <span data-ttu-id="23baa-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="23baa-121">-IotHubName</span></span>
<span data-ttu-id="23baa-122">Name des viel-Hubs</span><span class="sxs-lookup"><span data-stu-id="23baa-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="23baa-123">-Query</span><span class="sxs-lookup"><span data-stu-id="23baa-123">-Query</span></span>
<span data-ttu-id="23baa-124">Benutzerabfrage, die ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="23baa-124">User query to be executed.</span></span>

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

### <span data-ttu-id="23baa-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23baa-125">-ResourceGroupName</span></span>
<span data-ttu-id="23baa-126">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="23baa-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="23baa-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="23baa-127">-ResourceId</span></span>
<span data-ttu-id="23baa-128">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="23baa-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="23baa-129">-Top</span><span class="sxs-lookup"><span data-stu-id="23baa-129">-Top</span></span>
<span data-ttu-id="23baa-130">Die maximale Anzahl von Elementen, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="23baa-130">Maximum number of elements to return.</span></span>
<span data-ttu-id="23baa-131">Standardmäßig hat Query keine Cap.</span><span class="sxs-lookup"><span data-stu-id="23baa-131">By default query has no cap.</span></span>

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

### <span data-ttu-id="23baa-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="23baa-132">-Confirm</span></span>
<span data-ttu-id="23baa-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="23baa-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23baa-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23baa-134">-WhatIf</span></span>
<span data-ttu-id="23baa-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="23baa-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="23baa-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="23baa-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23baa-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23baa-137">CommonParameters</span></span>
<span data-ttu-id="23baa-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23baa-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23baa-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23baa-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23baa-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="23baa-140">INPUTS</span></span>

### <span data-ttu-id="23baa-141">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="23baa-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="23baa-142">System. String</span><span class="sxs-lookup"><span data-stu-id="23baa-142">System.String</span></span>

## <span data-ttu-id="23baa-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="23baa-143">OUTPUTS</span></span>

### <span data-ttu-id="23baa-144">System. String</span><span class="sxs-lookup"><span data-stu-id="23baa-144">System.String</span></span>

## <span data-ttu-id="23baa-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="23baa-145">NOTES</span></span>

## <span data-ttu-id="23baa-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="23baa-146">RELATED LINKS</span></span>
