---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubQuery.md
ms.openlocfilehash: 6445e6281ff69f4eef54a5694f953beaa08ad098
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94180461"
---
# <span data-ttu-id="f431e-101">Invoke-AzIotHubQuery</span><span class="sxs-lookup"><span data-stu-id="f431e-101">Invoke-AzIotHubQuery</span></span>

## <span data-ttu-id="f431e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f431e-102">SYNOPSIS</span></span>
<span data-ttu-id="f431e-103">Abfragen eines vielseitigen Hubs mithilfe einer leistungsfähigen SQL-ähnlichen Sprache.</span><span class="sxs-lookup"><span data-stu-id="f431e-103">Query an IoT Hub using a powerful SQL-like language.</span></span>

## <span data-ttu-id="f431e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f431e-104">SYNTAX</span></span>

### <span data-ttu-id="f431e-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f431e-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubQuery [-ResourceGroupName] <String> [-IotHubName] <String> [-Query] <String> [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f431e-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f431e-106">InputObjectSet</span></span>
```
Invoke-AzIotHubQuery [-InputObject] <PSIotHub> [-Query] <String> [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f431e-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="f431e-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubQuery [-ResourceId] <String> [-Query] <String> [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f431e-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f431e-108">DESCRIPTION</span></span>
<span data-ttu-id="f431e-109">Abfragen eines großen Hubs mithilfe einer leistungsfähigen SQL-ähnlichen Sprache, um Informationen zu Geräte-und Modul Zwillingen, Aufträgen und dem Nachrichtenrouting abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f431e-109">Query an IoT Hub using a powerful SQL-like language to retrieve information regarding device and module twins, jobs and message routing.</span></span>
<span data-ttu-id="f431e-110">Weitere Informationen finden Sie unter https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-query-language .</span><span class="sxs-lookup"><span data-stu-id="f431e-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-query-language for more information.</span></span>

## <span data-ttu-id="f431e-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f431e-111">EXAMPLES</span></span>

### <span data-ttu-id="f431e-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f431e-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Query "select * from devices"
```

<span data-ttu-id="f431e-113">Abfragen aller Geräte Zwillings Daten in einem Azure-viel-Hub</span><span class="sxs-lookup"><span data-stu-id="f431e-113">Query all device twin data in an Azure IoT Hub.</span></span>

### <span data-ttu-id="f431e-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="f431e-114">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Query "select * from devices.modules where devices.deviceId = 'myDevice1'" -Top 2
```

<span data-ttu-id="f431e-115">Abfrage der obersten zwei Modul Daten auf einem Zielgerät</span><span class="sxs-lookup"><span data-stu-id="f431e-115">Query top 2 module twin data on a target device.</span></span>

## <span data-ttu-id="f431e-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="f431e-116">PARAMETERS</span></span>

### <span data-ttu-id="f431e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f431e-117">-DefaultProfile</span></span>
<span data-ttu-id="f431e-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f431e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f431e-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f431e-119">-InputObject</span></span>
<span data-ttu-id="f431e-120">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="f431e-120">IotHub object</span></span>

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

### <span data-ttu-id="f431e-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="f431e-121">-IotHubName</span></span>
<span data-ttu-id="f431e-122">Name des viel-Hubs</span><span class="sxs-lookup"><span data-stu-id="f431e-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="f431e-123">-Query</span><span class="sxs-lookup"><span data-stu-id="f431e-123">-Query</span></span>
<span data-ttu-id="f431e-124">Benutzerabfrage, die ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f431e-124">User query to be executed.</span></span>

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

### <span data-ttu-id="f431e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f431e-125">-ResourceGroupName</span></span>
<span data-ttu-id="f431e-126">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="f431e-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="f431e-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="f431e-127">-ResourceId</span></span>
<span data-ttu-id="f431e-128">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="f431e-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="f431e-129">-Top</span><span class="sxs-lookup"><span data-stu-id="f431e-129">-Top</span></span>
<span data-ttu-id="f431e-130">Die maximale Anzahl von Elementen, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f431e-130">Maximum number of elements to return.</span></span>
<span data-ttu-id="f431e-131">Standardmäßig hat Query keine Cap.</span><span class="sxs-lookup"><span data-stu-id="f431e-131">By default query has no cap.</span></span>

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

### <span data-ttu-id="f431e-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f431e-132">-Confirm</span></span>
<span data-ttu-id="f431e-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f431e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f431e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f431e-134">-WhatIf</span></span>
<span data-ttu-id="f431e-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f431e-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f431e-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f431e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f431e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f431e-137">CommonParameters</span></span>
<span data-ttu-id="f431e-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f431e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f431e-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f431e-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f431e-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f431e-140">INPUTS</span></span>

### <span data-ttu-id="f431e-141">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="f431e-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="f431e-142">System. String</span><span class="sxs-lookup"><span data-stu-id="f431e-142">System.String</span></span>

## <span data-ttu-id="f431e-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f431e-143">OUTPUTS</span></span>

### <span data-ttu-id="f431e-144">System. String</span><span class="sxs-lookup"><span data-stu-id="f431e-144">System.String</span></span>

## <span data-ttu-id="f431e-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="f431e-145">NOTES</span></span>

## <span data-ttu-id="f431e-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f431e-146">RELATED LINKS</span></span>
